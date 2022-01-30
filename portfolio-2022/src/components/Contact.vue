<template>
  <section class="contact show-on-scroll-left" id="contact">
    <h2 class="title-contact">Contact</h2>
    <p>
      Je suis présentement à la recherche de nouvelles opportunités. N'hésitez
      pas à m'écrire!
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
    <p id="copyright" class="show-on-scroll-left">&copy; Marie-Ève Noël 2021</p>
    <a id="button" ref="button" class="button" v-on:click="scrollToTop"></a>
  </section>
</template>

<script>
export default {
  name: "Contact",
  methods: {
    scrollToTop() {
      //   const btn = this.refs.button;

      //   window.onscroll(function () {
      //     if (window.scrollTop() > 300) {
      //       btn.addClass("show");
      //     } else {
      //       btn.removeClass("show");
      //     }
      //   });

      //   btn.on("click", function (e) {
      //     e.preventDefault();
      //     document.getElementsByTagName("body").animate({ scrollTop: 0 }, "8000");
      //   });
      console.log("scrollingToTop");
    },
  },
};
</script>
