<script setup>
import { ref, computed } from 'vue'
import SobreMim from './components/SobreMim.vue'
import Aprendizagem from './components/Aprendizagem.vue'
import Sintese from './components/Sintese.vue'
import { User, BookOpen, Lightbulb } from 'lucide-vue-next'

const tabs = [
  { id: 'sobre-mim', label: 'Sobre Mim', component: SobreMim, icon: User },
  { id: 'aprendizagem', label: 'Aprendizagem', component: Aprendizagem, icon: BookOpen },
  { id: 'sintese', label: 'Síntese', component: Sintese, icon: Lightbulb }
]

const currentTab = ref(tabs[0].id)

const currentComponent = computed(() => {
  return tabs.find(t => t.id === currentTab.value)?.component || SobreMim
})
</script>

<template>
  <div class="min-h-screen flex flex-col bg-slate-50 font-sans selection:bg-indigo-200 selection:text-indigo-900">
    
    <!-- Header Area -->
    <header class="bg-white border-b border-slate-200 sticky top-0 z-30 shadow-sm">
      <div class="max-w-5xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="flex flex-col items-center py-10 space-y-4">
          <div class="h-16 w-16 bg-indigo-600 rounded-2xl shadow-lg shadow-indigo-200 flex items-center justify-center transform -rotate-6 hover:rotate-0 transition-transform duration-300">
            <Lightbulb class="text-white w-8 h-8" />
          </div>
          <h1 class="text-3xl md:text-4xl font-extrabold text-slate-900 tracking-tight text-center">
            Painel de Formação Auto-Reflexiva
          </h1>
          <p class="text-lg md:text-xl text-slate-500 font-medium text-center max-w-2xl italic">
            "Aprendo criando, experimentando, ensinando e resolvendo problemas reais."
          </p>
        </div>
        
        <!-- Navigation Tabs -->
        <nav class="flex justify-center space-x-1 sm:space-x-4 pb-0 overflow-x-auto no-scrollbar" aria-label="Tabs">
          <button
            v-for="tab in tabs"
            :key="tab.id"
            @click="currentTab = tab.id"
            :class="[
              currentTab === tab.id
                ? 'border-indigo-600 text-indigo-600 bg-indigo-50/50'
                : 'border-transparent text-slate-500 hover:text-slate-700 hover:border-slate-300',
              'group relative flex items-center gap-2 py-4 px-4 sm:px-6 border-b-2 font-semibold text-sm transition-all duration-200 ease-in-out whitespace-nowrap outline-none rounded-t-xl'
            ]"
          >
            <component 
              :is="tab.icon" 
              :class="[
                currentTab === tab.id ? 'text-indigo-600' : 'text-slate-400 group-hover:text-slate-500',
                'w-5 h-5 transition-colors duration-200'
              ]" 
            />
            {{ tab.label }}
          </button>
        </nav>
      </div>
    </header>

    <!-- Main Content Area -->
    <main class="flex-grow max-w-5xl mx-auto w-full px-4 sm:px-6 lg:px-8 py-10">
      <div class="relative min-h-[500px]">
        <Transition name="fade-slide" mode="out-in">
          <component :is="currentComponent" :key="currentTab" />
        </Transition>
      </div>
    </main>

  </div>
</template>

<style>
/* Custom transitions for the components */
.fade-slide-enter-active,
.fade-slide-leave-active {
  transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
}

.fade-slide-enter-from {
  opacity: 0;
  transform: translateY(15px);
}

.fade-slide-leave-to {
  opacity: 0;
  transform: translateY(-15px);
}

/* Hide scrollbar for tabs on mobile but keep functionality */
.no-scrollbar::-webkit-scrollbar {
  display: none;
}
.no-scrollbar {
  -ms-overflow-style: none;
  scrollbar-width: none;
}
</style>
