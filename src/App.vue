  <script>

  export default {
    data() {
      return {
        links: {
          github: {
            link: 'https://github.com/yyuhdev',
            icon: 'fa-brands fa-github'
          },
          twitter: {
            link: 'https://github.com/yyuhdev',
            icon: 'fa-brands fa-twitter'
          },
          discord: {
            link: 'https://github.com/yyuhdev',
            icon: 'fa-brands fa-discord'
          },
          email: {
            link: 'https://github.com/yyuhdev',
            icon: 'fa-solid fa-envelope'
          },
        },
        pages: {
          projects: {
            title: 'Projects',
            destination: '#projects'
          },
          contact: {
            title: 'Contact',
            destination: '#contact'
          },
          about: {
            title: 'About',
            destination: '#about'
          },
          home: {
            title: 'Home',
            destination: '#home'
          },
        }
      }
    }
  }

  </script>

  <template>
    <header>
      <div class="bg-black w-full p-5 text-white flex flex-row border-b-1 border-gray-600/60">

        <div class="flex w-1/2 flex-row">
          <p>Icon</p>
        </div>

        <div class="flex w-1/2 flex-row-reverse gap-5">
          <a v-for="page in pages" class="active:scale-95 transform" :href="page.destination">{{ page.title }}</a>
        </div>
      </div>
    </header>

    <main class="bg-black">
      <section id="home" class="text-white">
        <div class="flex flex-row justify-center items-center h-screen">
          <div class="w-1/2 flex flex-col gap-5">
            <p class="text-8xl font-bold">yyuh</p>
            <p class="text-gray-400 text-5xl">Build. Software. Better.</p>
          </div>
        </div>

      </section>

      <section id="about">

      </section>

      <section id="projects">

      </section>

      <section id="contact">

      </section>
    </main>

    <footer>
      <div class="bg-black w-full p-5 text-white flex flex-row">
        <div class="w-1/2 flex flex-row">
            <div class="flex flex-row gap-1">
              <a v-for="link in links" target="_blank" :href="link.link" class="text-white text-2xl active:scale-95 transform">
                <i :class="link.icon"></i>
              </a>
            </div>
          <div>

          </div>

        </div>
        <div class="w-1/2 flex flex-row-reverse">
          <div class="flex flex-col">
            <p class="text-lg font-bold text-right">yyuh</p>
            <p class="text-gray-400 text-sm">Build. Software. Better.</p>
          </div>
        </div>
      </div>
    </footer>
  </template>

  <style scoped>
  </style>
