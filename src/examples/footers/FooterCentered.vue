<script setup>
defineProps({
  socials: {
    type: Array,
    icon: String,
    link: String,
    default: () => [
      {
        icon: '<i class="fab fa-facebook text-lg opacity-8"></i>',
        link: "",
      },
      {
        icon: '<i class="fab fa-twitter text-lg opacity-8"></i>',
        link: "",
      },
      {
        icon: '<i class="fab fa-dribbble text-lg opacity-8"></i>',
        link: "",
      },
      {
        icon: '<i class="fab fa-github text-lg opacity-8"></i>',
        link: "",
      },
      {
        icon: '<i class="fab fa-youtube text-lg opacity-8"></i>',
        link: "",
      },
    ],
  },
  links: {
    type: Array,
    name: String,
    href: String,
    default: () => [
      { href: "", name: "Company" },
      { href: "", name: "About Us" },
      { href: "", name: "Team" },
      {
        href: "",
        name: "Products",
      },
      { href: "", name: "Blog" },
      { href: "", name: "License" },
    ],
  },
});
</script>
<template>
  <footer class="footer py-5">
    <div class="container">
      <div class="row">
        <div class="col-lg-8 mb-4 mx-auto text-center">
          <a
            v-for="{ name, href } of links"
            :key="name"
            :href="href"
            target="_blank"
            class="text-secondary me-xl-5 me-3 mb-sm-0 mb-2"
          >
            {{ name }}
          </a>
        </div>
        <div class="col-lg-8 mx-auto text-center mb-4 mt-2">
          <a
            v-for="{ icon, link } of socials"
            :key="link"
            :href="link"
            target="_blank"
            class="text-secondary me-xl-4 me-4"
            v-html="icon"
          >
          </a>
        </div>
      </div>
      <div class="row">
        <div class="col-8 mx-auto text-center mt-1">
          <p class="mb-0 text-secondary">
            Copyright © {{ new Date().getFullYear() }} Ceres Agro.
          </p>
        </div>
      </div>
    </div>
  </footer>
</template>
