<template>
  <nav class="relative flex flex-wrap items-center justify-between px-2 py-3 bg-purple-100">
    <div class="container px-4 mx-auto flex flex-wrap items-center justify-between">
      <div class="w-full relative flex justify-between sm:w-auto  px-4 sm:static sm:block sm:justify-start">
        
        <a class="inline-block">
        <img src="img/logo.png" alt="logo" class="h-8 md:h-12">
        </a>
        <a class="text-sm font-bold leading-relaxed inline-block mr-4 py-2 whitespace-nowrap uppercase text-gray-800" href="#pablo">
          PT Kreasi Kemasan 
        </a>
        <button class=" text-gray-800 cursor-pointer text-xl leading-none px-3 py-1 border border-solid border-transparent rounded bg-transparent block sm:hidden outline-none focus:outline-none" type="button" v-on:click="toggleNavbar()">
          <i class="fas fa-bars"></i>
        </button>
      </div>
      <div v-bind:class="{'hidden': !showMenu, 'flex': showMenu}" class="sm:flex sm:flex-grow items-center">
        <ul class="flex flex-col sm:flex-row list-none ml-auto">
          <li class="nav-item text-gray-800">
            <a class="px-3 py-2 flex items-center text-xs uppercase font-bold leading-snug hover:opacity-75">
              <router-link to="/">
                <i class="fa-solid fa-house-chimney text-lg leading-lg opacity-75" /><span class="ml-2">Beranda</span>
              </router-link>
            </a>
          </li>
          <li class="nav-item text-gray-800">
            <a class="px-3 py-2 flex items-center text-xs uppercase font-bold leading-snug hover:opacity-75">
              <router-link to="/about">
                <i class="fa-solid fa-address-card text-lg leading-lg opacity-75" /><span class="ml-2">Tentang Kami</span>
              </router-link>
              
            </a>
          </li>
          <li class="nav-item text-gray-800">
            <a class="px-3 py-2 flex items-center text-xs uppercase font-bold leading-snug hover:opacity-75">
              <router-link to="/product">
                <i class="fa-solid  fa-city text-lg leading-lg opacity-75" /><span class="ml-2">Produk</span>
              </router-link>
            </a>
          </li>
          
        </ul>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  name: "pink-navbar",
  data() {
    return {
      showMenu: false
    }
  },
  methods: {
    toggleNavbar: function(){
      this.showMenu = !this.showMenu;
    }
  }
}
</script>

<style>

</style>