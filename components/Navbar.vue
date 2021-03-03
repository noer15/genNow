<template>
  <header
    class="bg-gen-now shadow-md app-bar"
    style="box-shadow: 0 0 32px -4px rgba(0, 0, 0, 0.15)"
  >
    <div class="max-w-7xl mx-auto px-2 sm:px-6 lg:px-8 p-2">
      <div class="relative flex items-center justify-between h-16">
        <div class="absolute inset-y-0 left-0 flex items-center sm:hidden">
          <!-- Mobile menu button-->
          <button
            type="button"
            class="inline-flex items-center justify-center p-2 rounded-md text-gray-600 focus:outline-none focus:ring-2 focus:ring-inset focus:ring-white"
            aria-controls="mobile-menu"
            aria-expanded="false"
            @click="toggleMenu()"
          >
            <span class="sr-only">Open main menu</span>
            <svg
              class="block h-6 w-6"
              xmlns="http://www.w3.org/2000/svg"
              fill="none"
              viewBox="0 0 24 24"
              stroke="currentColor"
              aria-hidden="true"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M4 6h16M4 12h16M4 18h16"
              />
            </svg>
            <svg
              class="hidden h-6 w-6"
              xmlns="http://www.w3.org/2000/svg"
              fill="none"
              viewBox="0 0 24 24"
              stroke="currentColor"
              aria-hidden="true"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M6 18L18 6M6 6l12 12"
              />
            </svg>
          </button>
          <span class="block lg:hidden h-8 w-auto text-white text-2xl">
            GEN<span class="font-bold text-white text-2xl">NOW</span>
          </span>
        </div>
        <div
          class="flex-1 flex items-center justify-center sm:items-stretch sm:justify-start"
        >
          <div class="flex-shrink-0 flex items-center">
            <span class="hidden lg:block h-8 w-auto text-white text-2xl">
              GEN<span class="font-bold text-white text-2xl">NOW</span>
            </span>
          </div>
        </div>
        <div
          class="absolute inset-y-0 right-0 flex items-center pr-2 sm:static sm:inset-auto sm:ml-6 sm:pr-0"
        >
          <div
            class="hidden sm:block sm:ml-6"
            :class="{ hidden: !showMenu, flex: showMenu }"
          >
            <div class="flex space-x-4">
              <NuxtLink
                to="/"
                class="text-white px-3 py-2 rounded-sm text-md font-medium hover:text-black hover:bg-gray-300"
                >Beranda</NuxtLink
              >
              <NuxtLink
                to="/"
                class="text-white px-3 py-2 rounded-sm text-md font-medium hover:text-black hover:bg-gray-300"
                >Kelas</NuxtLink
              >
              <NuxtLink
                to="/"
                class="text-white px-3 py-2 rounded-sm text-md font-medium hover:text-black hover:bg-gray-300"
                >About</NuxtLink
              >
              <button class="bg-white-gen p-2 rounded-md text-black py-2">
                Daftar
              </button>
              <button class="bg-orange-gen p-2 rounded-md text-white py-2">
                Masuk
              </button>
            </div>
          </div>

          <!-- Profile dropdown -->
        </div>
      </div>
    </div>

    <!-- Mobile menu, show/hide based on menu state. -->

    <aside
      :class="{ hidden: !showMenu, flex: showMenu }"
      class="lg:hidden app-drawer is-active"
      style="top: 80px"
    >
      <div
        class="app-drawer__overlay w-full h-full lg:hidden"
        style="opacity: 1"
        :class="{ hidden: !showMenu, flex: showMenu }"
        @click="toggleMenu()"
      ></div>
      <nav
        id="nav-content"
        class="app-drawer__content w-4/5"
        style="transform: translateX(0%)"
      >
        <ul class="cursor-pointer">
          <li class="px-4 py-2">
            <NuxtLink to="/" class="text-gray-700">
              <span> Home </span>
            </NuxtLink>
          </li>
          <li class="px-4 py-2">
            <NuxtLink to="/contact" class="text-gray-700">
              <span> Kontak </span>
            </NuxtLink>
          </li>
        </ul>
      </nav>
    </aside>
  </header>
</template>
<script>
export default {
  data() {
    return {
      showMenu: false,
    }
  },
  methods: {
    toggleMenu() {
      this.showMenu = !this.showMenu
    },
  },
}
</script>

<style scoped>
.app-drawer {
  position: fixed;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  z-index: 50;
  border-top: 1px solid #e2e8f0;
}
.app-drawer__content {
  transition: -webkit-transform 0.5s ease;
  transition: transform 0.5s ease;
  -webkit-transform: translateX(-110%);
  -ms-transform: translateX(-110%);
  transform: translateX(-110%);
  position: absolute;
  top: 0;
  left: 0;
  bottom: 0;
  background-color: #fff;
}

.app-drawer__overlay {
  -webkit-transition: opacity 0.3s ease-out;
  transition: opacity 0.3s ease-out;
  opacity: 0;
  background-color: rgba(0, 0, 0, 0.5);
  position: absolute;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
}
.app-drawer__menu-item {
  cursor: pointer;
  display: -webkit-box;
  display: -ms-flexbox;
  display: flex;
  -webkit-box-orient: horizontal;
  -webkit-box-direction: normal;
  -ms-flex-direction: row;
  flex-direction: row;
  -webkit-box-align: center;
  -ms-flex-align: center;
  align-items: center;
  font-size: 1.25rem;
  color: #718096;
  padding: 1rem;
}
</style>
