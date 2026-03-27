<template>
  <main class="min-h-screen bg-ctp-base font-mono">
    <div class="bg-ctp-base border-b border-ctp-base flex items-center px-2 py-1">
      <div class="flex items-center gap-1 bg-ctp-blue text-ctp-base px-3 py-0.5 font-bold text-sm">
        <span>1</span>
        <span class="mx-1"></span>
        <span>portfolio</span>
      </div>
      
      <div class="flex items-center gap-1 bg-ctp-surface1 text-ctp-overlay0 px-3 py-0.5 text-sm">
        <span>2</span>
        <span class="mx-1"></span>
        <span>nvim</span>
      </div>
      
      <div class="flex items-center gap-1 bg-ctp-surface1 text-ctp-overlay0 px-3 py-0.5 text-sm">
        <span>3</span>
        <span class="mx-1"></span>
        <span>fish</span>
      </div>

      <div class="flex items-center gap-1 bg-ctp-surface1 text-ctp-overlay0 px-3 py-0.5 text-sm">
        <span>4</span>
        <span class="mx-1"></span>
        <span>npm</span>
      </div>
    </div>

    <div class="px-2 py-2 text-sm leading-relaxed" style="padding: 8px;">

      <span class="text-fish-teal">~</span>
      <div class="flex items-center mb-2">
        <span class="text-fish-mauve font-bold">❯</span>
        <span class="text-white ml-2">fastfetch</span>
      </div>

      <div class="flex gap-8 text-ctp-text" style="line-height: 1.2;">
        <pre class="text-ctp-blue" style="font-size: 1rem; line-height: 1.3;">  ⠀⠀⠀⣠⡀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⣀⣀⠀⠀
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

        <div style="line-height: 1.5;">
          <div class="mb-1 mt-20"><span class="text-ctp-text">yyuh@yyuhs-pc</span></div>
          <div class="mb-2"></div>
          <div class="mb-0.5"><span class="text-ctp-blue"> OS </span> <span class="text-ctp-text">→ Fedora Linux 43 (Workstation Edition) x86_64</span></div>
          <div class="mb-0.5"><span class="text-ctp-blue"> DE </span> <span class="text-ctp-text">→ Hyprland</span></div>
          <div class="mb-0.5"><span class="text-ctp-blue"> Lang </span> <span class="text-ctp-text">→ Java, PHP, Protobuf, Go, JS/TS</span></div>
          <div class="mb-0.5"><span class="text-ctp-blue"> DBs </span> <span class="text-ctp-text">→ MongoDB, InfluxDB, MySQL, PostgreSQL, Redis (DragonflyDB), S3</span></div>
          <div class="mb-0.5"><span class="text-ctp-blue"> Framework </span> <span class="text-ctp-text">→ NuxtJS, VueJS, Quarkus, SpringBoot, Laravel</span></div>
          <div class="mb-0.5"><span class="text-ctp-blue"> Infra </span> <span class="text-ctp-text">→ Docker, Kubernetes, Helm</span></div>
          <div class="mb-0.5"><span class="text-ctp-blue"> CI/CD </span> <span class="text-ctp-text">→ GitHub Actions, GitLab CI/CD</span></div>
          <div class="mb-0.5"><span class="text-ctp-blue"> Messaging </span> <span class="text-ctp-text">→ DragonflyDB, Redis, Kafka</span></div>
        </div>
      </div>

      <span class="text-fish-teal">~</span>
      <div class="flex items-center mb-2">
        <span class="text-fish-mauve font-bold">❯</span>
        <span class="text-white ml-2">cat info.md</span>
      </div>

      <div class="text-ctp-text mb-4" style="line-height: 1.6;">
        <div class="mb-3">
          <span class="text-ctp-mauve font-bold"># Links</span>
        </div>
        <div class="mb-2">
          <div>
            <a href="https://gitlab.revived.club/yyuh" target="_blank" class="text-ctp-blue underline">GitLab</a>
          </div>
          <div>
            <a href="https://github.com/yyuhdev" target="_blank" class="text-ctp-blue underline">GitHub</a>
          </div>
          <div>
            <a href="mailto:yyuhdev@gmail.com" target="_blank" class="text-ctp-blue underline">Email</a>
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
