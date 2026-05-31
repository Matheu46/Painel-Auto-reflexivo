<script setup>
import { ref, computed, provide, watch, onMounted } from 'vue'
import SobreMim from './components/SobreMim.vue'
import Aprendizagem from './components/Aprendizagem.vue'
import Sintese from './components/Sintese.vue'
import { User, BookOpen, Lightbulb, Settings } from 'lucide-vue-next'

// Theme Logic
const isRetro = ref(false)

onMounted(() => {
  const savedTheme = localStorage.getItem('theme')
  if (savedTheme === 'retro') {
    isRetro.value = true
  }
  updateBodyClass(isRetro.value)
})

watch(isRetro, (newVal) => {
  localStorage.setItem('theme', newVal ? 'retro' : 'normal')
  updateBodyClass(newVal)
})

function updateBodyClass(retro) {
  if (retro) {
    document.body.classList.add('retro-theme')
  } else {
    document.body.classList.remove('retro-theme')
  }
}

provide('isRetro', isRetro)

const toggleTheme = () => {
  isRetro.value = !isRetro.value
}

// Navigation Logic
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
  <div>
    <!-- Botão flutuante para alternar o tema -->
    <button 
      @click="toggleTheme"
      class="fixed bottom-4 right-4 z-50 p-4 rounded-full shadow-xl transition-all duration-300 flex items-center justify-center cursor-pointer"
      :class="isRetro ? 'bg-yellow-400 text-black border-4 border-outset border-gray-400 hover:bg-yellow-300' : 'bg-indigo-600 text-white hover:bg-indigo-700 hover:scale-110'"
      title="Alternar Tema"
    >
      <span v-if="isRetro" class="font-bold font-serif px-2">Voltar para 2026</span>
      <Settings v-else class="w-6 h-6 animate-spin-slow" />
    </button>

    <!-- LAYOUT MODERNO -->
    <div v-if="!isRetro" class="min-h-screen flex flex-col bg-slate-50 font-sans selection:bg-indigo-200 selection:text-indigo-900">
      
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
                'group relative flex items-center gap-2 py-4 px-4 sm:px-6 border-b-2 font-semibold text-sm transition-all duration-200 ease-in-out whitespace-nowrap outline-none rounded-t-xl cursor-pointer'
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

    <!-- LAYOUT RETRO -->
    <div v-else class="min-h-screen p-4 max-w-5xl mx-auto">
      <!-- Header Retro -->
      <header class="text-center mb-8 border-4 border-ridge border-gray-400 p-4 bg-black bg-opacity-70">
        <h1 class="text-4xl md:text-6xl font-bold text-red-500 mb-4" style="text-shadow: 2px 2px #ffff00;">
          <marquee scrollamount="12">🔥 BEM-VINDO AO MEU PAINEL DE FORMAÇÃO 🔥</marquee>
        </h1>
        <p class="text-xl text-yellow-300 font-bold mb-4 font-serif">
          "Aprendo criando, experimentando, ensinando e resolvendo problemas reais."
        </p>
        
        <div class="flex justify-center mt-4">
          <img src="https://media2.giphy.com/media/v1.Y2lkPTc5MGI3NjExc3ZnODJkZTZianc4ZnkyeGxzbThqbjY5amM0aWEydHNnaHh0NnFiNSZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/Roy1shss4yFWPplOjV/giphy.gif" alt="Under Construction" class="h-16" />
        </div>
      </header>

      <div class="flex flex-col md:flex-row gap-6">
        <!-- Sidebar de Navegação tipo 90s -->
        <nav class="retro-border p-4 w-full md:w-64 flex flex-col space-y-4 shadow-lg h-fit">
          <h3 class="text-center text-yellow-400 font-bold border-b-2 border-gray-400 pb-2 mb-2">~ MENU PRINCIPAL ~</h3>
          <button
            v-for="tab in tabs"
            :key="tab.id"
            @click="currentTab = tab.id"
            :class="[
              currentTab === tab.id ? 'bg-yellow-400 text-blue-900 font-extrabold' : 'hover:bg-blue-800 text-cyan-300',
              'border-2 border-outset border-gray-400 p-2 text-left w-full transition-none font-serif text-lg cursor-pointer'
            ]"
          >
            {{ currentTab === tab.id ? '►' : '▻' }} {{ tab.label }}
          </button>
          
          <div class="mt-8 text-center text-xs text-white">
            <p>Você é o visitante nº:</p>
            <div class="bg-black text-red-500 font-mono text-xl border-2 border-gray-600 inline-block p-1 tracking-widest mt-2 retro-blink">
              0004269
            </div>
          </div>
          
          <div class="mt-8 flex flex-col gap-4 items-center">
            <a href="#"><img src="https://www.w3.org/Icons/valid-html401" alt="Valid HTML" class="h-8 border-0" /></a>
            <a href="#"><img src="https://www.w3.org/Icons/valid-css" alt="Valid CSS" class="h-8 border-0" /></a>
            <a href="#"><img src="https://vanseodesign.com/blog/wp-content/uploads/2011/06/internet-explorer-6-logo.jpg" alt="IE logo" class="h-10 border-0" title="Best viewed in Internet Explorer" /></a>
          </div>
        </nav>

        <!-- Main Content Area sem frescuras modernas -->
        <main class="flex-grow retro-border p-6 shadow-xl bg-opacity-95 min-h-[500px]">
          <component :is="currentComponent" :key="currentTab" />
        </main>
      </div>
      
      <footer class="text-center mt-12 text-sm text-gray-400 border-t-2 border-dashed border-gray-600 pt-4 bg-black bg-opacity-70 p-4">
        <p>Copyright &copy; 2002 Matheus. Todos os direitos reservados.</p>
        <p>Melhor visualizado em Internet Explorer 6.0 ou superior (Resolução 800x600).</p>
        <p class="mt-2 text-xs">Criado com Macromedia Dreamweaver & FrontPage 98</p>
      </footer>
    </div>
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

.animate-spin-slow {
  animation: spin 3s linear infinite;
}
</style>
