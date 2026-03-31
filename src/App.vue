<script setup>
import { ref } from 'vue'

const activeTab = ref('portfolio')

const tabs = [
  { id: 'portfolio', number: 1, label: 'portfolio' },
  { id: 'projects', number: 2, label: 'projects' },
  { id: 'fish', number: 3, label: 'fish' },
  { id: 'npm', number: 4, label: 'npm' },
]
</script>

<template>
  <main class="min-h-screen bg-ctp-base font-mono flex flex-col">
    <div class="bg-ctp-base border-b border-ctp-base flex items-center px-2 py-1 overflow-x-auto">
      <button
        v-for="tab in tabs"
        :key="tab.id"
        @click="activeTab = tab.id"
        :class="[
          'flex items-center gap-1 px-2 sm:px-3 py-0.5 text-xs sm:text-sm shrink-0 cursor-pointer',
          activeTab === tab.id
            ? 'bg-ctp-blue text-ctp-base font-bold'
            : 'bg-ctp-surface1 text-ctp-overlay0'
        ]"
      >
        <span>{{ tab.number }}</span>
        <span class="mx-1"></span>
        <span>{{ tab.label }}</span>
      </button>
    </div>

    <div class="px-3 sm:px-4 py-2 text-xs sm:text-sm leading-relaxed flex-grow">

      <div v-if="activeTab === 'portfolio'">
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
            <div class="mb-0.5"><span class="text-ctp-blue"> Infra </span> <span class="text-ctp-text">→ Docker, K8s, Helm, Talos Linux, Tailscale</span></div>
            <div class="mb-0.5"><span class="text-ctp-blue"> CI/CD </span> <span class="text-ctp-text">→ GitHub Actions, GitLab CI, Jenkins</span></div>
            <div class="mb-0.5"><span class="text-ctp-blue"> Messaging </span> <span class="text-ctp-text">→ Redis, Kafka, NATS</span></div>
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
            <span class="w-2 h-5 bg-white ml-2 cursor-blink"></span>
          </div>
        </div>
      </div>

      <div v-else-if="activeTab === 'projects'" class="text-ctp-text">
        <span class="text-fish-teal">~/projects</span>
        <div class="flex items-center mb-2">
          <span class="text-fish-mauve font-bold">❯</span>
          <span class="text-white ml-2">ls -la</span>
        </div>

        <div class="space-y-4">
          <div class="pl-3">
            <div class="text-ctp-mauve font-bold">Revived.club</div>
            <div class="text-ctp-overlay0 text-xs mb-1">Minecraft Minigames Network built for unlimited scalability</div>
            <div class="text-xs">
              <span class="text-ctp-blue">stack:</span>
              <span class="text-ctp-text">Java, Kubernetes, MongoDB, InfluxDB, Redis, NATS</span>
            </div>
            <div class="text-xs">
              <a href="https://gitlab.revived.club/revived.club" class="text-ctp-blue underline hover:text-ctp-sapphire" target="_blank">repos</a>
            </div>
          </div>
          <div class="pl-3">
            <div class="text-ctp-mauve font-bold">Longinus</div>
            <div class="text-ctp-overlay0 text-xs mb-1">Library that contains all my commonly used code</div>
            <div class="text-xs">
              <span class="text-ctp-blue">stack:</span>
              <span class="text-ctp-text">Java, Kubernetes, MongoDB, InfluxDB, Redis, NATS</span>
            </div>
            <div class="text-xs">
              <a href="https://gitlab.revived.club/revived.club/commons" class="text-ctp-blue underline hover:text-ctp-sapphire" target="_blank">repo</a>
            </div>
          </div>
          <div class="pl-3">
            <div class="text-ctp-mauve font-bold">EasyMySQL</div>
            <div class="text-ctp-overlay0 text-xs mb-1">Easy to use MySQL library using the DAO pattern</div>
            <div class="text-xs">
              <span class="text-ctp-blue">stack:</span>
              <span class="text-ctp-text">Java, MySQL</span>
            </div>
            <div class="text-xs">
              <a href="https://github.com/yyuhdev/EasyMySQL" class="text-ctp-blue underline hover:text-ctp-sapphire" target="_blank">repo</a>
            </div>
          </div>
          <div class="pl-3">
            <div class="text-ctp-mauve font-bold">Neovim Config</div>
            <div class="text-ctp-overlay0 text-xs mb-1">Just my nvim configuration, all my plugins etc.</div>
            <div class="text-xs">
              <span class="text-ctp-blue">stack:</span>
              <span class="text-ctp-text">LUA, Lazy</span>
            </div>
            <div class="text-xs">
              <a href="https://gitlab.revived.club/yyuh/nvim" class="text-ctp-blue underline hover:text-ctp-sapphire" target="_blank">repo</a>
            </div>
          </div>
        </div>

        <div class="mt-4">
          <span class="text-fish-teal">~/projects</span>
          <div class="flex items-center">
            <span class="text-fish-mauve font-bold">❯</span>
            <span class="w-2 h-5 bg-white ml-2 cursor-blink"></span>
          </div>
        </div>
      </div>

      <div v-else-if="activeTab === 'fish'">
        <span class="text-fish-teal">~</span>
        <div class="flex items-center">
          <span class="text-fish-mauve font-bold">❯</span>
          <span class="w-2 h-5 bg-white ml-2 cursor-blink"></span>
        </div>
      </div>

      <div v-else-if="activeTab === 'npm'" class="text-ctp-text">
        <div class="mb-2">
          <span class="text-fish-teal">~/portfolio-site</span>
          <div class="flex items-center mb-2">
            <span class="text-fish-mauve font-bold">❯</span>
            <span class="text-white ml-2">npm run dev</span>
          </div>
        </div>

        <div class="space-y-1">
          <div class="mt-2"></div>
          <div class="text-white">> portfolio@0.0.0 dev</div>
          <div class="text-white">> vite</div>
          <div class="mt-3"></div>
          <div class="text-ctp-green">  VITE v7.1.12  <span class="text-ctp-text">ready in</span> <span class="text-ctp-yellow">1005</span> <span class="text-ctp-text">ms</span></div>
          <div class="mt-2"></div>
          <div>  <span class="text-ctp-green">➜</span>  <span class="text-ctp-text font-bold">Local:</span>   <span class="text-ctp-blue">http://localhost:5173/</span></div>
          <div>  <span class="text-ctp-green">➜</span>  <span class="text-ctp-overlay0">Network: use <span class="text-ctp-yellow">--host</span> to expose</span></div>
          <div>  <span class="text-ctp-green">➜</span>  <span class="text-ctp-blue">Vue DevTools: </span><span class="text-ctp-overlay0">Open </span><span class="text-ctp-blue">http://localhost:5173/__devtools__/</span><span class="text-ctp-overlay0"> as a separate window</span></div>
          <div>  <span class="text-ctp-green">➜</span>  <span class="text-ctp-blue">Vue DevTools: </span><span class="text-ctp-overlay0">Press <span class="text-ctp-yellow">Alt(⌥)+Shift(⇧)+D</span> in App to toggle the Vue DevTools</span></div>
          <div>  <span class="text-ctp-overlay0">➜</span>  <span class="text-ctp-overlay0">press</span> <span class="text-ctp-yellow">h + enter</span> <span class="text-ctp-overlay0">to show help</span></div>
        </div>
      </div>

    </div>

    <div class="px-3 sm:px-4 py-2">
      <div class="flex flex-wrap gap-2 items-center">
        <a href="https://yyuh.beer/" target="_blank">
         <img src="/banners/yyuh.gif" alt="yyuh" class="h-8">
        </a>
        <a href="https://www.vim.org/" target="_blank">
          <img src="/banners/vim-tenor.gif" alt="Vi Vim" class="h-8">
        </a>
        <a href="https://www.gnu.org/" target="_blank">
          <img src="/banners/gnu-linux.gif" alt="GNU/Linux" class="h-8">
        </a>
        <a href="https://www.mozilla.org/firefox/" target="_blank">
          <img src="/banners/firefox4.gif" alt="Firefox" class="h-8">
        </a>
        <img src="/banners/anythingbut.gif" alt="Anything But Chrome" class="h-8">
        <img src="/banners/defund_badge.gif" alt="Defund Police" class="h-8">
        <img src="/banners/java2.gif" alt="Get Java" class="h-8">
        <a href="https://artixlinux.org/" target="_blank">
         <img src="/banners/Artix.gif" alt="yyuh" class="h-8">
        </a>
        <img src="/banners/antinazi.gif" alt="Anti Nazi" class="h-8">
        <a href="https://mod.gov.ua/" target="_blank">
         <img src="/banners/nowar.png" alt="yyuh" class="h-8">
        </a>
        <img src="/banners/acab2.gif" alt="yyuh" class="h-8">
        <img src="/banners/palestine.gif" alt="yyuh" class="h-8">
      </div>
    </div>

  </main>
</template>

<style scoped>
</style>
