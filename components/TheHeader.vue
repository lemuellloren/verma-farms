<template>
  <nav id="nav">
    <div class="container">
      <!-- * Mobile Menu  -->
      <div id="mobileMenu" class="mobile-menu d-block d-sm-none">
        <div class="mobile-menu__row row d-flex justify-content-center align-items-center">
          <div class="col-2">
            <div id="hamburgerMenu" class="hamburger-menu">
              <span v-on:click="openNav" class="hamburger-menu__icon fas fa-bars"></span>
            </div>
          </div>
          <div class="col-8">
            <div class="logo">
              <img class="logo__img" src="~/assets/images/logo.png" alt="VERMA FARMS">
            </div>
          </div>
          <div class="col-2">
            <div class="bag">
              <img class="bag__icon" src="~/assets/images/svg-gobbler.svg" alt="Bag">
            </div>
          </div>
        </div>
      </div>
      <!-- * Mobile Menu  -->
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
    el: '#nav',
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
