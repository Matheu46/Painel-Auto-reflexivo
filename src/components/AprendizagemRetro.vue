<template>
  <div class="space-y-10">
    <div class="text-center border-b-4 border-double border-yellow-400 pb-4">
      <h2 class="text-3xl text-cyan-300 font-bold font-serif">O QUE APRENDI NESTA DISCIPLINA?</h2>
    </div>

    <!-- Layout com tabela para dar aquele visual HTML < 4.0 -->
    <table width="100%" border="0" cellspacing="10" cellpadding="0">
      <tr>
        <td valign="top" class="bg-gray-800 border-4 border-outset border-gray-400 p-4">
          <h4 class="text-yellow-400 font-bold text-xl mb-2 font-serif">★ Aprendizagem</h4>
          <p class="text-white text-lg">Aprendizagem não é apenas receber informações. Aprender é atribuir significado às experiências. Aprendemos quando relacionamos teoria, prática e contexto.</p>
        </td>
      </tr>
      <tr>
        <td valign="top" class="bg-gray-800 border-4 border-outset border-gray-400 p-4">
          <h4 class="text-yellow-400 font-bold text-xl mb-2 font-serif">★ Planejamento</h4>
          <p class="text-white text-lg">Planejar é criar condições para que a aprendizagem aconteça. Planejamento não é rigidez; é intenção pedagógica.</p>
        </td>
      </tr>
      <tr>
        <td valign="top" class="bg-gray-800 border-4 border-outset border-gray-400 p-4">
          <h4 class="text-yellow-400 font-bold text-xl mb-2 font-serif">★ Metodologia</h4>
          <p class="text-white text-lg">Metodologias devem aproximar o estudante do conhecimento. O diálogo e a participação tornam a aprendizagem mais significativa.</p>
        </td>
      </tr>
    </table>

    <div class="retro-border p-6 mt-8">
      <h3 class="text-2xl text-green-400 underline mb-4 text-center font-bold font-serif">💻 EaD na Prática 💻</h3>
      <p class="text-lg text-white mb-6">
        No meu trabalho cuido das engrenagens que sustentam a EaD do IFRN. Observo diariamente como <span class="text-yellow-400">tecnologia, organização e pedagogia</span> se encontram em um Ambiente Virtual de Aprendizagem.
      </p>
      
      <div class="text-center">
        <!-- Pseudo imagem / ASCII Art -->
        <table border="1" cellpadding="20" class="mx-auto border-4 border-outset border-gray-500 bg-black text-green-500 font-mono">
          <tr>
            <td align="center">
              <pre>
 _________________
|  ___________  |
| | MOODLE    | |
| | AVA       | |
| |___________| |
|_______________|
              </pre>
            </td>
          </tr>
        </table>
      </div>
    </div>

    <!-- Destaque do Plugin (Design berrante) -->
    <div class="border-4 border-dashed border-cyan-400 p-6 mt-8 text-center bg-blue-950">
      <h3 class="text-3xl text-yellow-300 font-bold mb-4 retro-blink font-serif">>>> UM EXEMPLO CONCRETO! <<<</h3>
      <p class="text-white text-lg text-left mb-6">
        Ao refletir sobre as atividades de diário de bordo da especialização, identifiquei uma necessidade. Transformei essa observação em um plugin para Moodle.
        O plugin permite que estudantes façam anotações dentro do próprio ambiente do curso. <br><br>
        <span class="text-yellow-400 font-bold text-xl bg-red-800 p-1">Mais do que uma funcionalidade, a ideia era tornar o AVA um espaço mais vivo e reflexivo.</span>
      </p>
      
      <div class="mt-8 flex flex-col items-center justify-center space-y-6">
        <a href="https://moodle.org/plugins/local_quicknote" target="_blank" class="bg-gray-300 text-black font-bold border-4 border-outset border-gray-400 px-6 py-3 hover:bg-gray-400 text-xl no-underline hover:text-black">
          👉 Ver no Moodle Plugins Directory 👈
        </a>
        
        <div class="border-4 border-outset border-gray-500 p-2 bg-black mt-4">
          <img src="/img/local_quicknote.png" alt="Interface do Plugin" class="max-w-full md:max-w-md border border-gray-600" onerror="this.style.display='none'" />
          <div class="text-cyan-400 font-mono mt-2 text-sm">local_quicknote.exe</div>
        </div>
      </div>
    </div>

  </div>
</template>
