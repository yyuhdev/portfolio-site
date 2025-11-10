<template>
  <header>
    <div class="bg-black w-full p-5 text-white flex justify-between items-center border-b border-gray-600/20 fixed top-0 left-0 z-50">
      <div class="flex items-center gap-3">
        <p class="text-xl font-bold">yyuh</p>
      </div>

      <nav class="hidden md:flex gap-5">
        <a
            v-for="page in pages"
            :key="page.title"
            :href="page.destination"
            class="active:scale-95 transform hover:text-[#cba6f7] transition"
        >
          {{ page.title }}
        </a>
      </nav>

      <button class="md:hidden text-2xl" @click="showMenu = !showMenu">
        <i class="fa-solid" :class="showMenu ? 'fa-xmark' : 'fa-bars'"></i>
      </button>
    </div>

    <transition name="fade">
      <div
          v-if="showMenu"
          class="fixed top-[72px] left-0 w-full bg-black border-b border-gray-700/30 flex flex-col items-center gap-5 p-5 md:hidden z-40"
      >
        <a
            v-for="page in pages"
            :key="page.title"
            :href="page.destination"
            class="text-lg text-white transition"
            @click="showMenu = false"
        >
          {{ page.title }}
        </a>
      </div>
    </transition>
  </header>

  <main class="bg-black pt-24">
    <section id="home" class="text-white">
      <div class="flex flex-col md:flex-row justify-center items-center h-screen text-center md:text-left px-6 md:px-20">
        <div class="md:w-1/2 flex flex-col gap-5 transform -translate-y-10">
          <p class="text-6xl md:text-8xl font-bold">yyuh</p>
          <p class="text-gray-400 text-3xl md:text-5xl">Build. Software. Better.</p>
        </div>
      </div>
    </section>

    <section id="about" class="text-white py-20 px-6 md:px-20">
      <div class="max-w-5xl mx-auto flex flex-col gap-16">
        <div class="flex flex-col gap-5">
          <h1 class="font-semibold text-4xl md:text-5xl">About</h1>
          <p class="text-lg md:text-2xl text-gray-400 leading-relaxed">
            16 y/o dev from Germany who somehow turns caffeine and half-baked ideas into actual code.
            Known for rewriting entire projects at 3am because “the structure felt off.”
            Writes Java like it’s poetry and CSS like it’s black magic.
          </p>

          <blockquote class="border-l-4 border-[#cba6f7] pl-5 italic text-xl md:text-2xl text-gray-300 bg-white/5 p-5 rounded-xl">
            “If it compiles, it’s good enough.”
            <footer class="mt-3 text-right text-gray-400 text-base">— yyuh, 2025</footer>
          </blockquote>
        </div>

        <div class="flex flex-col gap-5">
          <h2 class="text-center text-3xl md:text-4xl font-semibold">Techstack</h2>
          <div class="flex flex-wrap justify-center gap-6 md:gap-10">
            <div v-for="lang in techStack" :key="lang.name" class="text-4xl md:text-5xl">
              <i :class="lang.icon" class="colored"></i>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section id="projects" class="bg-black text-white min-h-screen flex flex-col items-center justify-center p-6 md:p-10">
      <div class="w-full max-w-6xl flex flex-col gap-10 md:gap-16">
        <h1 class="text-4xl md:text-5xl font-bold text-center">Projects</h1>

        <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-6 md:gap-10">
          <div
              v-for="project in projects"
              :key="project.name"
              class="group bg-white/5 rounded-2xl p-6 border border-gray-700/30 hover:border-[#cba6f7]/40 transition"
          >
            <div class="flex flex-col gap-4">
              <div class="flex items-center justify-between">
                <i :class="project.icon" class="text-3xl md:text-4xl text-[#cba6f7]"></i>
                <a
                    :href="project.link"
                    target="_blank"
                    class="text-gray-400 hover:text-[#cba6f7] transition text-base md:text-lg font-semibold active:scale-95 transform"
                >
                  View →
                </a>
              </div>

              <h2 class="text-xl md:text-2xl font-bold">{{ project.name }}</h2>
              <p class="text-gray-400 text-base md:text-lg leading-relaxed">{{ project.desc }}</p>
            </div>
          </div>
        </div>

        <p class="text-gray-400 text-center">
          More on my
          <a target="_blank" href="https://github.com/yyuhdev" class="text-blue-400 hover:underline">
            GitHub
          </a>
          :3
        </p>
      </div>
    </section>
  </main>

  <footer class="bg-black w-full p-6 text-white border-t border-gray-600/20">
    <div class="flex flex-col md:flex-row justify-between items-center gap-6">
      <div class="flex flex-row gap-4 text-2xl">
        <a
            v-for="link in links"
            :key="link.link"
            target="_blank"
            :href="link.link"
            class="active:scale-95 transform hover:text-[#cba6f7] transition"
        >
          <i :class="link.icon"></i>
        </a>
      </div>

      <div class="text-center md:text-right">
        <p class="text-lg font-bold">yyuh</p>
        <p class="text-gray-400 text-sm">Build. Software. Better.</p>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  data() {
    return {
      showMenu: false,
      techStack: [
        { name: 'Java', icon: 'devicon-java-plain' },
        { name: 'JavaScript', icon: 'devicon-javascript-plain' },
        { name: 'Vue.js', icon: 'devicon-vuejs-plain' },
        { name: 'HTML5', icon: 'devicon-html5-plain' },
        { name: 'CSS3', icon: 'devicon-css3-plain' },
        { name: 'Git', icon: 'devicon-git-plain' },
        { name: 'TailwindCSS', icon: 'devicon-tailwindcss-plain' },
        { name: 'Redis', icon: 'devicon-redis-plain' },
        { name: 'Go', icon: 'devicon-go-plain' },
        { name: 'Docker', icon: 'devicon-docker-plain' },
        { name: 'Kubernetes', icon: 'devicon-kubernetes-plain' }
      ],
      projects: {
        portfolio: {
          name: 'Personal Website',
          desc: 'This very site — built with Vue 3 and TailwindCSS for speed and vibes.',
          link: '#',
          icon: 'fa-solid fa-code'
        },
        easySQL: {
          name: 'EasyMySQL',
          desc: 'Simple MySQL Wrapper for Bukkit Plugins using the DAO pattern.',
          link: 'https://github.com/yyuhdev/EasyMySQL',
          icon: 'fa-solid fa-code'
        },
        dotfiles: {
          name: 'Hyprland Dotfiles',
          desc: "My Catppuccin themed dotfiles for Hyprland.",
          link: 'https://github.com/yyuhdev/dotfiles',
          icon: 'fa-solid fa-code'
        },
      },
      links: {
        github: { link: 'https://github.com/yyuhdev', icon: 'fa-brands fa-github' },
        twitter: { link: 'https://github.com/yyuhdev', icon: 'fa-brands fa-twitter' },
        discord: { link: 'https://github.com/yyuhdev', icon: 'fa-brands fa-discord' },
        email: { link: 'https://github.com/yyuhdev', icon: 'fa-solid fa-envelope' },
      },
      pages: {
        projects: { title: 'Projects', destination: '#projects' },
        about: { title: 'About', destination: '#about' },
        home: { title: 'Home', destination: '#home' },
      },
    };
  },
};
</script>

<style scoped>
.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.3s ease;
}
.fade-enter-from,
.fade-leave-to {
  opacity: 0;
}
</style>
