<script setup>
import { onMounted, onUnmounted } from "vue";

//example components
import DefaultNavbar from "../../../examples/navbars/NavbarDefault.vue";
import DefaultFooter from "../../../examples/footers/FooterDefault.vue";
import Statements from "./Sections/Statements.vue";
//image

import OurStory from "@/assets/img/OurStory.jpg";

//dep
import Typed from "typed.js";

//sections
import Information from "./Sections/AboutInformation.vue";

const body = document.getElementsByTagName("body")[0];
//hooks
onMounted(() => {
  body.classList.add("about-us");
  body.classList.add("bg-gray-200");

  if (document.getElementById("typed")) {
    // eslint-disable-next-line no-unused-vars
    var typed = new Typed("#typed", {
      stringsElement: "#typed-strings",
      typeSpeed: 90,
      backSpeed: 90,
      backDelay: 200,
      startDelay: 500,
      loop: true,
    });
  }
});

onUnmounted(() => {
  body.classList.remove("about-us");
  body.classList.remove("bg-gray-200");
});
</script>
<template>
  <DefaultNavbar
    :action="{
      route: 'javascript:;',
      label: 'Buy Now',
      color: 'btn-white',
    }"
    transparent
  />
  <header class="bg-gradient-dark">
    <div
      class="page-header min-vh-90"
      :style="{ backgroundImage: `url(${OurStory})` }"
    >
      <span class="mask bg-gradient-dark opacity-6"></span>
      <div class="container">
        <div class="row justify-content-center">
          <div class="col-lg-9 text-center mx-auto my-auto">
            <h1 class="text-white">Our story</h1>
            <p class="lead mb-4 text-white opacity-8">
              The journey of Ceres Agros began with a singular belief: Plant
              science must evolve. As farmers grappled with nutrient loss, poor
              soil response, and unpredictable yields, our founders envisioned a
              fertilizer that could do more — deliver nutrients with intent.
            </p>
            <p class="lead mb-4 text-white opacity-8">
              By merging agronomy with material science, Ceres Agros gave birth
              to MET — Microphase Enrichment Technology, an innovation that
              changed how nutrients behave in the soil. Each granule we
              manufacture is a product of purpose, designed not just to feed the
              plant, but to redefine the way crops grow.
            </p>
            <!-- <button type="submit" class="btn bg-white text-dark">
              Create Account
            </button> -->
            <h6 class="text-white mb-2 mt-5">Find us on</h6>
            <div class="d-flex justify-content-center">
              <a href="javascript:;"
                ><i class="fab fa-facebook text-lg text-white me-4"></i
              ></a>
              <a href="javascript:;"
                ><i class="fab fa-instagram text-lg text-white me-4"></i
              ></a>
              <a href="javascript:;"
                ><i class="fab fa-twitter text-lg text-white me-4"></i
              ></a>
              <a href="javascript:;"
                ><i class="fab fa-google-plus text-lg text-white"></i
              ></a>
            </div>
          </div>
        </div>
      </div>
    </div>
  </header>
  <div class="card card-body shadow-xl mx-3 mx-md-4 mt-n6">
    <!-- <Information /> -->
    <Statements/>
    <!-- <AboutTeam />
    <Featuring />
    <Newsletter /> -->
  </div>
  <DefaultFooter />
</template>
