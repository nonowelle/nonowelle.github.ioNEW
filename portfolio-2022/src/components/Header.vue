<template>
  <header class="header">
    <div class="menu-icon">
      <span></span>
      <span></span>
      <span></span>
    </div>
    <nav class="navbar">
      <ul class="menu">
        <li class="navli">
          <a class="nav" id="liapropos" href="#apropos">À propos</a>
        </li>
        <li class="navli">
          <a class="nav" id="liprojets" href="#projets">Projets</a>
        </li>
        <li class="navli">
          <a class="nav" id="licontact" href="#contact">Contact</a>
        </li>
        <li class="navli">
          <a class="nav" id="licontact" href="en.html">EN</a>
        </li>
        <!-- <li class="navli en"><a class="nav" href="#">En</a></li> -->
        <li class="navli email">Contactez-moi : menoel888@gmail.com</li>
      </ul>
    </nav>
  </header>
</template>

<script>
export default {
  name: "Header",
  props: {
    msg: String,
  },
};
</script>
