<script setup>
import { Brain, FileText, Users, Network, CodeSquare, QrCode } from 'lucide-vue-next'
</script>

<template>
  <div class="space-y-16 pb-12">
    <!-- Header Section -->
    <div class="text-center space-y-4">
      <h2 class="text-indigo-600 font-bold tracking-wider uppercase text-sm flex items-center justify-center gap-2">
        <Brain class="w-4 h-4" />
        O que aprendi nesta disciplina?
      </h2>
      <h3 class="text-3xl font-extrabold text-slate-900">Conceitos & Prática</h3>
    </div>

    <!-- Cards de Conceitos -->
    <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
      <!-- Card 1 -->
      <div class="bg-white p-6 rounded-2xl shadow-sm border border-slate-100 hover:shadow-md transition-shadow group relative overflow-hidden">
        <div class="absolute -right-4 -top-4 w-24 h-24 bg-blue-50 rounded-full group-hover:scale-150 transition-transform duration-500 ease-out z-0"></div>
        <div class="relative z-10">
          <div class="w-12 h-12 bg-blue-100 text-blue-600 rounded-xl flex items-center justify-center mb-4">
            <Brain class="w-6 h-6" />
          </div>
          <h4 class="text-lg font-bold text-slate-900 mb-2">Aprendizagem</h4>
          <p class="text-slate-600 text-sm leading-relaxed">
            Aprendizagem não é apenas receber informações. Aprender é atribuir significado às experiências. Aprendemos quando relacionamos teoria, prática e contexto.
          </p>
        </div>
      </div>

      <!-- Card 2 -->
      <div class="bg-white p-6 rounded-2xl shadow-sm border border-slate-100 hover:shadow-md transition-shadow group relative overflow-hidden">
        <div class="absolute -right-4 -top-4 w-24 h-24 bg-emerald-50 rounded-full group-hover:scale-150 transition-transform duration-500 ease-out z-0"></div>
        <div class="relative z-10">
          <div class="w-12 h-12 bg-emerald-100 text-emerald-600 rounded-xl flex items-center justify-center mb-4">
            <FileText class="w-6 h-6" />
          </div>
          <h4 class="text-lg font-bold text-slate-900 mb-2">Planejamento</h4>
          <p class="text-slate-600 text-sm leading-relaxed">
            Planejar é criar condições para que a aprendizagem aconteça. Planejamento não é rigidez; é intenção pedagógica.
          </p>
        </div>
      </div>

      <!-- Card 3 -->
      <div class="bg-white p-6 rounded-2xl shadow-sm border border-slate-100 hover:shadow-md transition-shadow group relative overflow-hidden">
        <div class="absolute -right-4 -top-4 w-24 h-24 bg-amber-50 rounded-full group-hover:scale-150 transition-transform duration-500 ease-out z-0"></div>
        <div class="relative z-10">
          <div class="w-12 h-12 bg-amber-100 text-amber-600 rounded-xl flex items-center justify-center mb-4">
            <Users class="w-6 h-6" />
          </div>
          <h4 class="text-lg font-bold text-slate-900 mb-2">Metodologia</h4>
          <p class="text-slate-600 text-sm leading-relaxed">
            Metodologias devem aproximar o estudante do conhecimento. O diálogo e a participação tornam a aprendizagem mais significativa.
          </p>
        </div>
      </div>
    </div>

    <!-- EaD na Prática -->
    <div class="bg-slate-900 text-white rounded-3xl p-8 sm:p-10 relative overflow-hidden shadow-xl">
      <!-- Decorative Elements -->
      <div class="absolute top-0 right-0 p-8 opacity-10 pointer-events-none">
        <Network class="w-48 h-48" />
      </div>
      
      <div class="relative z-10 grid grid-cols-1 md:grid-cols-2 gap-10 items-center">
        <div class="space-y-6">
          <h3 class="text-2xl font-bold text-indigo-400">EaD na prática</h3>
          <p class="text-slate-300 text-lg leading-relaxed">
            No meu trabalho cuido das engrenagens que sustentam a EaD do IFRN. Observo diariamente como <span class="text-white font-semibold">tecnologia, organização e pedagogia</span> se encontram em um Ambiente Virtual de Aprendizagem.
          </p>
        </div>
        <div class="flex justify-center md:justify-end">
          <div class="w-full max-w-sm aspect-video bg-slate-800 rounded-xl border border-slate-700 shadow-inner flex items-center justify-center text-slate-500 overflow-hidden relative group">
            <div class="absolute inset-0 bg-gradient-to-tr from-slate-800 to-slate-700 opacity-50 group-hover:opacity-100 transition-opacity"></div>
            <div class="relative flex flex-col items-center gap-2">
              <Network class="w-10 h-10" />
              <span class="text-xs uppercase tracking-widest font-semibold">Moodle AVA</span>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- Seção de Destaque (Hero/Feature) -->
    <div class="relative mt-8">
      <!-- Decoration line -->
      <div class="absolute left-1/2 -top-8 bottom-0 w-px bg-gradient-to-b from-indigo-200 to-transparent hidden lg:block -z-10"></div>
      
      <div class="bg-white rounded-3xl p-8 sm:p-10 shadow-lg border border-slate-100">
        <div class="text-center mb-10">
          <span class="inline-flex items-center gap-2 px-4 py-2 rounded-full bg-indigo-50 text-indigo-700 font-bold text-sm tracking-wide uppercase mb-4">
            Um exemplo concreto
          </span>
          <h3 class="text-3xl font-extrabold text-slate-900">Plugin local_quicknote</h3>
        </div>

        <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 items-center">
          <div class="space-y-6">
            <p class="text-slate-600 text-lg leading-relaxed">
              Ao refletir sobre as atividades de diário de bordo da especialização, identifiquei uma necessidade. Transformei essa observação em um plugin para Moodle.
            </p>
            <p class="text-slate-600 text-lg leading-relaxed">
              O plugin permite que estudantes façam anotações dentro do próprio ambiente do curso. <strong class="text-indigo-600 font-semibold">Mais do que uma funcionalidade, a ideia era tornar o AVA um espaço mais vivo e reflexivo.</strong>
            </p>
            
            <div class="pt-4 flex items-center gap-4">
               <a href="https://moodle.org/plugins/local_quicknote" class="bg-indigo-600 hover:bg-indigo-700 text-white font-medium py-3 px-6 rounded-xl transition-colors shadow-md shadow-indigo-200 flex items-center gap-2">
                 <CodeSquare class="w-5 h-5" />
                 Ver no Moodle Plugins Directory
               </a>
            </div>
          </div>

          <div class="flex flex-col gap-4">
             <!-- Screenshot Placeholder -->
             <div class="w-full aspect-[4/3] bg-slate-100 rounded-2xl border border-slate-200 shadow-inner flex flex-col items-center justify-center text-slate-400 p-6 text-center group hover:bg-slate-50 transition-colors">
                <img src="/img/local_quicknote.png" alt="Interface do Plugin" />
                <span class="font-medium text-slate-500 group-hover:text-slate-700 transition-colors">Interface do Plugin</span>
             </div>
          </div>
        </div>
      </div>
    </div>

  </div>
</template>
