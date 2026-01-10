<template>
  <header>
  </header>

  <main class="bg-black text-white font-mono min-h-screen px-4 py-6 sm:p-8">
    <div class="mb-8 text-green-500">
      [yyuh@portfolio ~] $ kubectl logs -it yyuh
    </div>

    <div class="section header text-center mb-12">
      <pre
          class="whitespace-pre text-green-500 leading-tight
         text-xs sm:text-xs md:text-lg">

██╗   ██╗██╗   ██╗██╗   ██╗██╗  ██╗
╚██╗ ██╔╝╚██╗ ██╔╝██║   ██║██║  ██║
 ╚████╔╝  ╚████╔╝ ██║   ██║███████║
  ╚██╔╝    ╚██╔╝  ██║   ██║██╔══██║
   ██║      ██║   ╚██████╔╝██║  ██║
   ╚═╝      ╚═╝    ╚═════╝ ╚═╝  ╚═╝

Java Engineer | Backend & Distributed Systems</pre>
    </div>

    <div class="max-w-4xl mx-auto mb-16">
      <div class="border border-green-500 p-4 sm:p-6 mb-8">
        <h2 class="text-green-500 text-xl mb-4">[ ABOUT ]</h2>
        <p class="text-gray-300 mb-4">
          > I'm yyuh, a 16-yo software engineer from Germany. I have been working with Java for the past 3 years and I
          love it ever since.
        </p>
        <div class="flex flex-wrap gap-3 mt-4">
          <span
              v-for="tech in techStack"
              :key="tech.name"
              class="px-3 py-1 bg-green-900 bg-opacity-20
         border border-green-700 text-green-400
         text-xs sm:text-sm">
            {{ tech.name }}
          </span>
        </div>
      </div>

      <div class="border border-green-500 p-4 sm:p-6 mb-8">
        <h2 class="text-green-500 text-xl mb-4">[ PROJECTS ]</h2>
        <div class="space-y-4">
          <div
              v-for="(project, key) in projects"
              :key="key"
              class="border-l-2 border-cyan-500 pl-4 py-2"
          >
            <h3 class="text-cyan-400 font-bold mb-2">
              {{ project.name }}
            </h3>
            <p class="text-gray-400 mb-2">{{ project.desc }}</p>
            <a :href="project.link" target="_blank"
               class="text-green-500 hover:text-green-400 text-sm">
              → View Project
            </a>
          </div>
        </div>
      </div>

      <div class="border border-green-500 p-4 sm:p-6 mb-8">
        <h2 class="text-green-500 text-xl mb-4">[ CONNECT ]</h2>
        <div class="space-y-2">
          <a v-for="(social, key) in links" :key="key"
             :href="social.link" target="_blank"
             class="block hover:bg-green-900/50 hover:bg-opacity-20 p-3 transition-all group">
            <span class="text-green-500 group-hover:text-green-400">→</span>
            <span class="text-gray-400 ml-2 capitalize group-hover:text-green-300">{{ key }}</span>
            <span class="text-gray-600 ml-2 text-sm group-hover:text-gray-400">{{ social.link }}</span>
          </a>
        </div>
      </div>
    </div>
  </main>
</template>

<script>
export default {
  data() {
    return {
      showMenu: false,
      techStack: [
        {name: 'Java'},
        {name: 'Kubernetes'},
        {name: 'Redis'},
        {name: 'JavaScript'},
        {name: 'PHP'},
        {name: 'Go'},
        {name: 'Nuxt.js'},
        {name: 'Laravel'},
        {name: 'TailwindCSS'},
        {name: 'Docker'}
      ],
      projects: {
        portfolio: {
          name: 'Revived.club',
          desc: 'Minecraft Minigames server built using Java, Redis & Kubernetes.',
          link: 'https://github.com/Revived-club/revived-duels',
        },
        easySQL: {
          name: 'EasyMySQL',
          desc: 'Simple MySQL Wrapper for Bukkit Plugins using the DAO pattern.',
          link: 'https://github.com/yyuhdev/EasyMySQL',
        }
      },
      links: {
        github: {link: 'https://github.com/yyuhdev'},
        email: {link: 'mailto:yyuhdev@gmail.com'},
      },
      pages: {
        projects: {title: 'Projects', destination: '#projects'},
        about: {title: 'About', destination: '#about'},
        home: {title: 'Home', destination: '#home'},
      },
    };
  },
};
</script>

<style scoped>
</style>
