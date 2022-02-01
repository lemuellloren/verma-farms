<template>
  <nav id="nav" class="d-flex align-items-center">
    <div class="container">
      <!-- * Mobile Menu  -->
      <div id="mobileMenu" class="mobile-menu d-block d-sm-none">
        <div class="mobile-menu__row row d-flex justify-content-center align-items-center">
          <div class="col-2">
            <div id="hamburgerMenu" class="hamburger-menu">
              <span v-on:click="openNav" class="hamburger-menu__icon fas fa-bars"></span>
            </div>
          </div>
          <div class="col-7">
            <div class="logo">
              <img class="logo__img" src="~/assets/images/logo.png" alt="VERMA FARMS">
            </div>
          </div>
          <div class="col-3">
            <div class="bag">
              <img class="bag__icon" src="~/assets/images/svg-gobbler.svg" alt="Bag">
            </div>
          </div>
        </div>
      </div>
      <!-- * Mobile Menu  -->
      <!-- * Desktop Menu  -->
      <div class="desktop-menu d-none d-sm-block">
        <div class="desktop-menu__row row d-flex justify-content-center align-items-center">
          <div class="col-md-6">
            <div class="desktop-menu__main d-flex align-items-center">
              <div class="logo">
                <img class="logo__img" src="~/assets/images/logo.png" alt="VERMA FARMS">
              </div>
              <ul class="desktop-menu__ul d-flex">
                <li class="desktop-menu__li">
                  <NuxtLink class="desktop-menu__menus" to="/">Shop</NuxtLink>
                </li>
                <li class="desktop-menu__li">
                  <NuxtLink class="desktop-menu__menus" to="/">Our Story</NuxtLink>
                </li>
                <li class="desktop-menu__li">
                  <NuxtLink class="desktop-menu__menus" to="/">Learn</NuxtLink>
                </li>
              </ul>
            </div>
          </div>
          <div class="col-md-6">
            <div class="desktop-menu__main desktop-menu__main--right d-flex justify-content-end align-items-center">
              <ul class="desktop-menu__ul d-flex">
                <li class="desktop-menu__li">
                  <NuxtLink class="desktop-menu__menus" to="/">Community</NuxtLink>
                </li>
                <li class="desktop-menu__li">
                  <NuxtLink class="desktop-menu__menus" to="/">Blog</NuxtLink>
                </li>
              </ul>
              <div class="bag">
                <img class="bag__icon" src="~/assets/images/svg-gobbler.svg" alt="Bag">
              </div>
            </div>
          </div>
        </div>
      </div>
      <!-- * Desktop Menu  -->
    </div>
    <!-- OffCanvas  -->
    <div class="sidebar-menu" id="sideBar">
      <div class="sidebar-menu__container">
        <span v-on:click="closeNav" class="close-nav fas fa-chevron-right"></span>
        <div class="mobile-menu-logo">
          <img src="~/assets/images/verma-green-icon.png" alt="Verma Farm" class="mobile-menu-logo__img">
        </div>
        <ul class="sidebar-menu__ul">
          <li class="sidebar-menu__li">
            Shop
          </li>
          <li class="sidebar-menu__li">
            Our Story
          </li>
          <li class="sidebar-menu__li">
            Learn
          </li>
          <li class="sidebar-menu__li">
            Community
          </li>
          <li class="sidebar-menu__li">
            Blog
          </li>
        </ul>
      </div>
    </div>
    <!-- OffCanvas  -->
  </nav>
</template>

<script>
  export default {
    methods: {
      openNav: function () {
        document.getElementById('sideBar').style.width = "250px";
        document.getElementById('mobileMenu').style.marginLeft = "250px";
      },
      closeNav: function () {
        document.getElementById("sideBar").style.width = "0";
        document.getElementById("mobileMenu").style.marginLeft = "0";
      }
    }
  }

</script>
