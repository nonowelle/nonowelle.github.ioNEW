<template>
  <section class="contact show-on-scroll-left" id="contact">
    <h2 class="title-contact">Contact</h2>
    <p>
       Don't hesitate to reach out for any question!
    </p>
    <a class="contact-link" href="mailto:menoel888@gmail.com">
      menoel888@gmail.com</a
    >
    <div class="res">
      <a target=" _blank" href=" mailto:menoel888@gmail.com"
        ><i class="far fa-envelope"></i
      ></a>
      <a
        target="_blank"
        href="https://www.linkedin.com/in/marie-ève-noël
                "
        ><i class="fab fa-linkedin"></i
      ></a>
      <a href="https://github.com/nonowelle" target="_blank"
        ><i class="fab fa-github"></i
      ></a>
    </div>
    <p id="copyright" class="show-on-scroll-left">&copy; Marie-Ève Noël 2023</p>
    <a id="button" ref="button" class="button" v-smooth-scroll href="#app"></a>
  </section>
</template>

<script>
export default {
  name: 'Contact',
};
</script>
