<script setup>
import { MapPin, GraduationCap, Code, Compass, Image as ImageIcon } from 'lucide-vue-next'
</script>

<template>
  <div class="space-y-12 pb-12">
    <!-- Header Section -->
    <div class="text-center space-y-4">
      <h2 class="text-indigo-600 font-bold tracking-wider uppercase text-sm flex items-center justify-center gap-2">
        <Compass class="w-4 h-4" />
        Quem eu sou?
      </h2>
      <h3 class="text-3xl font-extrabold text-slate-900">Minha Trajetória</h3>
    </div>

    <!-- Trajetória Grid -->
    <div class="bg-white rounded-2xl p-6 sm:p-8 shadow-sm border border-slate-100 relative overflow-hidden">
      <!-- Decorator background -->
      <div class="absolute top-0 right-0 -mr-8 -mt-8 w-32 h-32 bg-indigo-50 rounded-full blur-2xl opacity-50"></div>
      
      <div class="flex items-center gap-3 mb-6 relative z-10">
        <span class="inline-flex items-center gap-1.5 px-3 py-1.5 rounded-full bg-indigo-100 text-indigo-700 text-sm font-semibold">
          <MapPin class="w-4 h-4" />
          Mais de 10 anos no IFRN
        </span>
      </div>

      <div class="grid grid-cols-1 md:grid-cols-3 gap-6 relative z-10">
        <!-- Campus 1 -->
        <div class="group border border-slate-200 rounded-xl p-5 hover:border-indigo-300 hover:shadow-md transition-all bg-white flex flex-col items-center text-center">
          <div class="w-12 h-12 rounded-full bg-slate-100 text-slate-400 flex items-center justify-center mb-4 group-hover:bg-indigo-50 group-hover:text-indigo-500 transition-colors">
            <ImageIcon class="w-6 h-6" />
          </div>
          <h4 class="font-bold text-slate-800 mb-1">Técnico em Multimídia</h4>
          <p class="text-sm text-slate-500 flex-grow">Campus Natal-Centro Histórico</p>
        </div>

        <!-- Campus 2 -->
        <div class="group border border-slate-200 rounded-xl p-5 hover:border-indigo-300 hover:shadow-md transition-all bg-white flex flex-col items-center text-center">
          <div class="w-12 h-12 rounded-full bg-slate-100 text-slate-400 flex items-center justify-center mb-4 group-hover:bg-indigo-50 group-hover:text-indigo-500 transition-colors">
            <GraduationCap class="w-6 h-6" />
          </div>
          <h4 class="font-bold text-slate-800 mb-1">Licenciatura em Informática</h4>
          <p class="text-sm text-slate-500 flex-grow">Campus Natal-Zona Norte</p>
        </div>

        <!-- Campus 3 -->
        <div class="group border border-slate-200 rounded-xl p-5 hover:border-indigo-300 hover:shadow-md transition-all bg-white flex flex-col items-center text-center">
          <div class="w-12 h-12 rounded-full bg-slate-100 text-slate-400 flex items-center justify-center mb-4 group-hover:bg-indigo-50 group-hover:text-indigo-500 transition-colors">
            <Code class="w-6 h-6" />
          </div>
          <h4 class="font-bold text-slate-800 mb-1">Especialização em EaD na EPT</h4>
          <p class="text-sm text-slate-500 flex-grow">Campus Natal-Zona Leste</p>
        </div>
      </div>
    </div>

    <!-- Memória de Formação -->
    <div class="space-y-6">
      <h3 class="text-2xl font-bold text-slate-900 border-b pb-2 border-slate-200">Memória de Formação</h3>
      <div class="bg-indigo-900 text-indigo-50 p-6 sm:p-8 rounded-2xl shadow-lg transform rotate-1 hover:rotate-0 transition-transform">
        <p class="text-lg md:text-xl font-medium leading-relaxed">
          "No ensino médio descobri que existem muitas formas de expressão: vídeo, áudio, fotografia, design e programação. Foi durante um projeto de criação de um site que percebi como a web permite reunir todas essas linguagens em um único espaço."
        </p>
      </div>
    </div>

    <!-- Como eu aprendo -->
    <div class="grid grid-cols-1 md:grid-cols-2 gap-8 items-center">
      <div class="space-y-4">
        <h3 class="text-2xl font-bold text-slate-900">Como eu aprendo</h3>
        <p class="text-slate-600 leading-relaxed text-lg">
          Aprendo fazendo. Aprendo quando enfrento problemas que fazem sentido para a minha realidade. 
          <span class="font-semibold text-indigo-600">Criar é minha forma favorita de aprender.</span>
        </p>
      </div>
      <div>
        <blockquote class="border-l-4 border-indigo-500 pl-6 py-2 bg-slate-50 rounded-r-lg italic text-slate-700 shadow-sm">
          "Quem ensina aprende ao ensinar e quem aprende ensina ao aprender."
          <footer class="mt-2 font-semibold text-slate-900 text-sm">— Paulo Freire</footer>
        </blockquote>
      </div>
    </div>

    <!-- Histórias sem ponto final -->
    <div class="bg-white border border-dashed border-slate-300 rounded-2xl p-6 sm:p-8 shadow-sm">
      <h3 class="text-xl font-bold text-slate-900 mb-4 flex items-center gap-2">
        Histórias sem ponto final
      </h3>
      <p class="text-slate-600 leading-relaxed">
        Minha formação não é uma linha reta. Tenho cursos concluídos e trajetórias interrompidas. Também passei por formações que não concluí: Informática para Internet e Jogos Digitais. 
        <span class="block mt-4 font-medium text-slate-800 bg-slate-100 p-3 rounded-lg border-l-4 border-slate-400">
          Nem toda aprendizagem termina com um diploma.
        </span>
      </p>
    </div>

  </div>
</template>
