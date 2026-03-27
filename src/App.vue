<template>
  <main class="min-h-screen bg-ctp-base font-mono">
    <div class="bg-ctp-base border-b border-ctp-base flex items-center px-2 py-1 overflow-x-auto">
      <div class="flex items-center gap-1 bg-ctp-blue text-ctp-base px-2 sm:px-3 py-0.5 font-bold text-xs sm:text-sm shrink-0">
        <span>1</span>
        <span class="mx-1"></span>
        <span>portfolio</span>
      </div>
      
      <div class="flex items-center gap-1 bg-ctp-surface1 text-ctp-overlay0 px-2 sm:px-3 py-0.5 text-xs sm:text-sm shrink-0">
        <span>2</span>
        <span class="mx-1"></span>
        <span>nvim</span>
      </div>
      
      <div class="flex items-center gap-1 bg-ctp-surface1 text-ctp-overlay0 px-2 sm:px-3 py-0.5 text-xs sm:text-sm shrink-0">
        <span>3</span>
        <span class="mx-1"></span>
        <span>fish</span>
      </div>

      <div class="flex items-center gap-1 bg-ctp-surface1 text-ctp-overlay0 px-2 sm:px-3 py-0.5 text-xs sm:text-sm shrink-0">
        <span>4</span>
        <span class="mx-1"></span>
        <span>npm</span>
      </div>
    </div>

    <div class="px-3 sm:px-4 py-2 text-xs sm:text-sm leading-relaxed">

      <span class="text-fish-teal">~</span>
      <div class="flex items-center mb-2">
        <span class="text-fish-mauve font-bold">❯</span>
        <span class="text-white ml-2">fastfetch</span>
      </div>

      <div class="flex flex-col md:flex-row gap-4 md:gap-8 text-ctp-text">
        <pre class="hidden md:block text-ctp-blue text-base leading-tight">  ⠀⠀⠀⣠⡀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⣀⣀⠀⠀
  ⠀⠀⢰⠏⠙⠳⣄⠀⠀⠀⠀⠀⠀⠀⠀⣤⡀⠀⠀⠀⠀⠀⠀⠀⢀⡴⠚⠉⠈⣷⠀
  ⠀⢀⡟⠀⠀⠀⠈⠹⣆⣀⣠⣤⠤⠤⣤⣧⠉⠳⣄⠀⠀⠀⣀⡶⠋⠀⠀⠀⠀⢸⡀
  ⠀⢸⠇⠀⠀⠀⠀⠀⠈⠙⢦⡀⠀⠀⠀⠈⠀⠀⠙⢦⣀⡶⠋⠀⠀⠀⠀⠀⠀⢸⡇
  ⠀⣞⠀⠀⠀⠀⠀⠀⠀⠀⠈⠃⠀⠀⠀⠀⠀⠀⠀⠘⡿⠃⠀⠀⠀⠀⠀⠀⠀⢸⠇
  ⠀⡇⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⣼⠀
  ⠀⣧⠀⠀⠀⢀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⢀⠀⣀⠀⠀⠀⠀⠀⢠⡏⠀
  ⠀⢹⡄⠀⠀⠙⠛⠻⠶⢦⣤⣄⠀⠀⠀⠀⠀⣤⣶⡿⠿⠟⠿⠂⠀⠀⠀⢠⡞⠀⠀
  ⢀⣀⠻⣤⠀⠀⣠⣤⣶⠾⠛⠁⢠⡴⠦⠄⠀⠉⠛⠻⠿⣶⣦⣤⠀⠠⠴⠟⠛⣶⠀
  ⠸⡏⠉⠉⢁⡀⠈⡁⠀⠀⠀⠀⠀⢀⡀⠀⠀⢀⡀⠀⠀⢠⠟⣷⣠⠖⠀⣴⠚⠁⠀
  ⠀⠙⢷⡜⠙⢧⡞⠕⠀⠀⠺⣤⡶⠋⠙⠓⢲⡞⠁⠀⠀⠀⠀⠛⠁⠀⠀⠘⣧⠀⠀
  ⠀⢠⠏⠀⠀⠀⠀⠀⠀⠀⠀⠀⢻⡄⠀⠀⢸⠀⠀⠀⠀⠀⠀⠀⣀⡶⣤⠤⡼⠀⠀
  ⠀⣼⣠⡴⠶⣄⣶⣄⣀⠀⠀⠀⠈⢧⡄⠀⣼⠀⠀⠀⢀⣀⣠⠴⠋⠁⠉⠀⠁⠀⠀
  ⠀⠀⠀⠀⠀⠀⠹⣆⠉⠛⠦⠀⠀⠀⠙⠋⠁⠀⠀⠀⠻⣅⠀⠀⠀⠀⠀⠀⠀⠀⠀
  ⠀⠀⠀⠀⠀⠀⣠⠞⠃⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠘⣧⠀⠀⠀⠀⠀⠀⠀⠀
  ⠀⠀⠀⠀⠀⠸⢧⣠⣄⣀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠈⢷⠀⠀⠀⠀⠀⠀⠀</pre>

        <div class="leading-relaxed md:mt-20">
          <div class="mb-1"><span class="text-ctp-text font-bold">yyuh@yyuhs-pc</span></div>
          <div class="mb-0.5"><span class="text-ctp-blue"> OS </span> <span class="text-ctp-text">→ Fedora Linux 43 x86_64</span></div>
          <div class="mb-0.5"><span class="text-ctp-blue"> DE </span> <span class="text-ctp-text">→ Hyprland</span></div>
          <div class="mb-0.5"><span class="text-ctp-blue"> Lang </span> <span class="text-ctp-text">→ Java, PHP, Go, JS/TS</span></div>
          <div class="mb-0.5"><span class="text-ctp-blue"> DBs </span> <span class="text-ctp-text">→ MongoDB, MySQL, PostgreSQL, Redis</span></div>
          <div class="mb-0.5"><span class="text-ctp-blue"> Framework </span> <span class="text-ctp-text">→ Vue, Nuxt, Quarkus, Spring</span></div>
          <div class="mb-0.5"><span class="text-ctp-blue"> Infra </span> <span class="text-ctp-text">→ Docker, K8s, Helm</span></div>
          <div class="mb-0.5"><span class="text-ctp-blue"> CI/CD </span> <span class="text-ctp-text">→ GitHub Actions, GitLab CI</span></div>
          <div class="mb-0.5"><span class="text-ctp-blue"> Messaging </span> <span class="text-ctp-text">→ Redis, Kafka</span></div>
        </div>
      </div>

      <span class="text-fish-teal">~</span>
      <div class="flex items-center mb-2">
        <span class="text-fish-mauve font-bold">❯</span>
        <span class="text-white ml-2">cat info.md</span>
      </div>

      <div class="text-ctp-text mb-4 leading-relaxed">
        <div class="mb-3">
          <span class="text-ctp-mauve font-bold"># Links</span>
        </div>
        <div class="mb-2 space-y-1">
          <div>
            <a href="https://gitlab.revived.club/yyuh" target="_blank" class="text-ctp-blue underline hover:text-ctp-sapphire">GitLab</a>
          </div>
          <div>
            <a href="https://github.com/yyuhdev" target="_blank" class="text-ctp-blue underline hover:text-ctp-sapphire">GitHub</a>
          </div>
          <div>
            <a href="mailto:yyuhdev@gmail.com" target="_blank" class="text-ctp-blue underline hover:text-ctp-sapphire">Email</a>
          </div>
        </div>
      </div>

      <div class="mt-4">
        <span class="text-fish-teal">~</span>
        <div class="flex items-center">
          <span class="text-fish-mauve font-bold">❯</span>
          <span class="w-2 h-5 bg-white ml-2"></span>
        </div>
      </div>

    </div>
  </main>
</template>

<style scoped>
</style>
