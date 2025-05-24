<script setup>
import logoDark from "@/assets/img/logo-ct-dark.png";
import logoceres from "@/assets/img/ceras-agro-logo.png"
defineProps({
  brand: {
    type: Object,
    name: String,
    logo: String,
    route: "",
    default: () => ({
      name: "Ceres Agros",
      logo: logoceres,
      route: "/"
    })
  },
  socials: {
    type: Array,
    icon: String,
    link: String,
    default: () => [
      {
        icon: '<i class="fab fa-facebook text-lg opacity-8"></i>',
        link: ""
      },
      {
        icon: '<i class="fab fa-twitter text-lg opacity-8"></i>',
        link: ""
      },
      {
        icon: '<i class="fab fa-dribbble text-lg opacity-8"></i>',
        link: ""
      },
      {
        icon: '<i class="fab fa-github text-lg opacity-8"></i>',
        link: ""
      },
      {
        icon: '<i class="fab fa-youtube text-lg opacity-8"></i>',
        link: ""
      }
    ]
  },
  menus: {
    type: Array,
    name: String,
    items: {
      type: Array,
      name: String,
      href: String
    },
    default: () => [
      {
        name: "about us",
        items: [
          // {
          //   name: "about us",
          //   href: ""
          // },
          // {
          //   name: "freebies",
          //   href: ""
          // },
          // {
          //   name: "premium tools",
          //   href: ""
          // },
          // { name: "blog", href: "" }
        ]
      },
      {
        name: "Contact-Us",
        items: [
          // { name: "illustrations", href: "" },
          // {
          //   name: "bits & snippets",
          //   href: ""
          // },
          // {
          //   name: "affiliate program",
          //   href: ""
          // }
        ]
      },
      {
        name: "Blog",
        items: [
          // {
          //   name: "contact us",
          //   href: ""
          // },
          // {
          //   name: "knowledge center",
          //   href: ""
          // },
          // {
          //   name: "custom development",
          //   href: ""
          // },
          // {
          //   name: "sponsorships",
          //   href: ""
          // }
        ]
      },
      {
        name: "Our Story",
        items: [
          // {
          //   name: "terms & conditions",
          //   href: ""
          // },
          // {
          //   name: "privacy policy",
          //   href: ""
          // },
          // {
          //   name: "licenses (EULA)",
          //   href: ""
          // }
        ]
      }
    ]
  }
});
</script>
<template>
  <footer class="footer pt-5 mt-5">
    <div class="container">
      <div class="row">
        <div class="col-md-3 mb-4 ms-auto">
          <div>
            <a :href="brand.route">
              <img :src="brand.logo" class="mb-3" alt="main_logo" :style="{ height: '40px', width: '120px' }" />
            </a>
            <!-- <h6 class="font-weight-bolder mb-4">Ceres Agros</h6> -->
          </div>
          <div>
            <ul class="d-flex flex-row ms-n3 nav">
              <li
                class="nav-item"
                v-for="{ icon, link } of socials"
                :key="link"
              >
                <a
                  class="nav-link pe-1"
                  :href="link"
                  target="_blank"
                  v-html="icon"
                >
                </a>
              </li>
            </ul>
          </div>
        </div>
        <div
          class="col-md-2 col-sm-6 col-6 mb-4"
          v-for="{ name, items } of menus"
          :key="name"
        >
          <h6 class="text-sm">{{ name }}</h6>
          <ul class="flex-column ms-n3 nav">
            <li class="nav-item" v-for="item of items" :key="item.name">
              <a class="nav-link" :href="item.href" target="_blank">
                {{ item.name }}
              </a>
            </li>
          </ul>
        </div>

        <div class="col-12">
          <div class="text-center">
            <p class="text-dark my-4 text-sm font-weight-normal">
              All rights reserved. Copyright ©
              {{ new Date().getFullYear() }}
              Creative Tim
              <a href="" target="_blank"
                >team</a
              >.
            </p>
          </div>
        </div>
      </div>
    </div>
  </footer>
</template>
