<script setup>
import { onMounted, onUnmounted } from "vue";

//example components
import DefaultNavbar from "../../../examples/navbars/NavbarDefault.vue";
import DefaultFooter from "../../../examples/footers/FooterDefault.vue";

//image
import bg0 from "@/assets/img/bg9.jpg";
import aboutusLab from "@/assets/img/about-us-lab.jpeg";
import aboutUSBackground from "@/assets/img/aboutus.jpg";
import HomeCardPic from "@/assets/img/home-card-pic1.jpg"
import MET from "@/assets/img/METChart.jpg";

//dep
import Typed from "typed.js";

//sections
import Information from "./Sections/AboutInformation.vue";
import AboutTeam from "./Sections/AboutTeam.vue";
import Featuring from "./Sections/AboutFeaturing.vue";
import Newsletter from "./Sections/AboutNewsletter.vue";

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
      class="page-header min-vh-75"
      :style="{ backgroundImage: `url(${aboutUSBackground})` }"
    >
      <span class="mask bg-gradient-dark opacity-6"></span>
      <div class="container">
        <div class="row justify-content-center">
          <div class="col-lg-9 text-center mx-auto my-auto">
            <h1 class="text-white">About Ceres Agros</h1>
            <p class="lead mb-4 text-white opacity-8">
              Ceres Agros is India’s leading manufacturer of 100% water-soluble
              granular fertilizers, developed using the groundbreaking
              Microphase Enrichment Technology (MET). Our science-driven
              solutions are tailored to meet the evolving demands of modern
              agriculture — ensuring higher efficiency, better yields, and
              sustainable soil health.
            </p>
            <p class="lead mb-4 text-white opacity-8">
              We are not just a fertilizer company. We are a vision, a movement,
              and a mission — one rooted in precision, inspired by performance,
              and dedicated to progress.
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
  <div class="row py-5">
    <div
      class="col-lg-7 col-md-7 z-index-2 position-relative px-md-2 px-sm-5 mx-auto"
    >
      <div class="d-flex justify-content-between align-items-center mb-2">
        <h3 class="mb-0">
          Our Technology: MET (Microphase Enrichment Technology)
        </h3>
      </div>
      <h5 class="mb-0">What is MET?</h5>
      <p class="text-lg mb-0">
        MET is an advanced, layered nutrient delivery system. Every Ceres Agros
        granule is manufactured with multi-phase nutrient compartments, allowing
        for targeted, time-sensitive release of macro and micronutrients such
        as:
      </p>
      <ul>
        <li>Nitrogen (N) – stabilized, non-volatile forms</li>
        <li>Phosphorus (P) – non-DAP phosphorus compounds</li>
        <li>Potassium (K) – neutral pH potassium</li>
        <li>
          Micronutrients – Zn, Fe, Mn, B, Mg, Mo in chelated or protected forms
        </li>
        <li>
          Organic Core – fortified with carbon molecules and bio-enhancers to
          stimulate root interaction and nutrient absorption
        </li>
      </ul>
    </div>
  </div>
  <div class="row py-2">
    <div
      class="col-lg-7 col-md-7 z-index-2 position-relative px-md-2 px-sm-5 mx-auto"
    >
      <h5 class="mb-0">How MET works?</h5>
      <ul>
        <li>Precision layering: Nutrients are embedded in concentric shells</li>
        <li>
          Controlled release: Each layer dissolves in response to soil moisture
          and root interaction
        </li>
        <li>
          Zero waste: Nutrients are released only when the plant needs them —
          avoiding leaching and fixation
        </li>
        <li>
          Uniform impact: Every granule contains a full profile, ensuring
          even plant nutrition
        </li>
      </ul>
    </div>
  </div>
  <div class="row py-2 mb-8">
    <div
      class="col-lg-7 col-md-7 z-index-2 position-relative px-md-2 px-sm-5 mx-auto"
    >
      <h5 class="mb-0">Why It Matters:</h5>
      <ul>
        <li>No urea, no DAP – just pure, plant-friendly compounds</li>
        <li>Works across diverse soil types and climates</li>
        <li>Reduces application frequency and farmer input costs</li>
        <li>
          Promotes balanced plant growth, root health, and
          improved yield quality
        </li>
      </ul>
    </div>
  </div>
  <div class="container mt-sm-5">
    <img :src="MET" alt="" class="pb-6">
  </div>
  <div class="card card-body shadow-xl mx-3 mx-md-4 mt-n6">
    <Information />
    <AboutTeam />
    <Featuring />
    <Newsletter />
  </div>
  <DefaultFooter />
</template>
