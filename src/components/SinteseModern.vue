<script setup>
import { Heart, Briefcase, Sparkles, Quote } from 'lucide-vue-next'
</script>

<template>
  <div class="space-y-12 pb-16">
    <!-- Header Section -->
    <div class="text-center space-y-4">
      <h2 class="text-indigo-600 font-bold tracking-wider uppercase text-sm flex items-center justify-center gap-2">
        <Sparkles class="w-4 h-4" />
        Para onde vou?
      </h2>
      <h3 class="text-3xl font-extrabold text-slate-900">Síntese</h3>
    </div>

    <!-- Reflexões em Blocos -->
    <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
      
      <!-- Bloco 1 -->
      <div class="bg-white rounded-3xl p-8 shadow-sm border border-slate-100 hover:shadow-lg transition-all duration-300 group">
        <div class="w-14 h-14 bg-rose-50 text-rose-500 rounded-2xl flex items-center justify-center mb-6 group-hover:scale-110 group-hover:bg-rose-500 group-hover:text-white transition-all duration-300">
          <Heart class="w-7 h-7" />
        </div>
        <h4 class="text-xl font-bold text-slate-900 mb-4">O que mais gostei de aprender</h4>
        <p class="text-slate-600 leading-relaxed text-lg">
          As discussões sobre aprendizagem, memória e experiência. A ideia de que 
          <span class="font-semibold text-rose-500">aprendemos em diálogo com nossas vivências.</span>
        </p>
      </div>

      <!-- Bloco 2 -->
      <div class="bg-white rounded-3xl p-8 shadow-sm border border-slate-100 hover:shadow-lg transition-all duration-300 group">
        <div class="w-14 h-14 bg-indigo-50 text-indigo-500 rounded-2xl flex items-center justify-center mb-6 group-hover:scale-110 group-hover:bg-indigo-500 group-hover:text-white transition-all duration-300">
          <Briefcase class="w-7 h-7" />
        </div>
        <h4 class="text-xl font-bold text-slate-900 mb-4">O que levo para minha prática</h4>
        <p class="text-slate-600 leading-relaxed text-lg">
          Levo a compreensão de que tecnologia não é apenas ferramenta. Os ambientes digitais também são 
          <span class="font-semibold text-indigo-600">espaços de encontro, reflexão e construção coletiva.</span> Quero continuar criando soluções que aproximem pessoas da aprendizagem.
        </p>
      </div>
      
    </div>

    <!-- Hero Footer / Banner de Fechamento -->
    <div class="relative mt-12 bg-indigo-600 rounded-3xl overflow-hidden shadow-2xl shadow-indigo-200">
      <!-- Decorator Circles -->
      <div class="absolute -right-20 -top-20 w-64 h-64 bg-indigo-500 rounded-full opacity-50 mix-blend-multiply blur-3xl"></div>
      <div class="absolute -left-20 -bottom-20 w-64 h-64 bg-purple-500 rounded-full opacity-50 mix-blend-multiply blur-3xl"></div>
      
      <div class="relative z-10 p-10 sm:p-14 text-center flex flex-col items-center">
        <Quote class="w-12 h-12 text-indigo-300 mb-6 opacity-80" />
        <p class="text-xl sm:text-2xl md:text-3xl font-medium text-white leading-tight max-w-4xl font-serif">
          "Minha trajetória mostra que aprender é um processo inacabado — e talvez seja exatamente isso que o torna tão significativo. Entre códigos, plataformas e experiências educativas, <span class="text-indigo-200 font-bold border-b-2 border-indigo-400">continuo aprendendo criando.</span>"
        </p>
      </div>
    </div>

  </div>
</template>
