<script setup>
import { onMounted, onUnmounted,ref } from "vue";

//example components
import NavbarDefault from "../..//examples/navbars/NavbarDefault.vue";
import DefaultFooter from "../../examples/footers/FooterDefault.vue";
import Header from "../../examples/Header.vue";
import FilledInfoCard from "../../examples/cards/infoCards/FilledInfoCard.vue";
import MaterialButton from "@/components/MaterialButton.vue";

//Vue Material Kit 2 components
import MaterialSocialButton from "@/components/MaterialSocialButton.vue";

// sections
import PresentationCounter from "./Sections/PresentationCounter.vue";
import PresentationPages from "./Sections/PresentationPages.vue";
import PresentationExample from "./Sections/PresentationExample.vue";
import data from "./Sections/Data/designBlocksData";
import BuiltByDevelopers from "./Components/BuiltByDevelopers.vue";
import PresentationTestimonials from "./Sections/PresentationTestimonials.vue";
import PresentationInformation from "./Sections/PresentationInformation.vue";

//images src\assets\img\background-pic-g2.jpg
import vueMkHeader from "@/assets/img/vue-mk-header.jpg";
import backgroundPicG2 from "@/assets/img/background-pic-g2.jpg";
import HomeCardPic from "@/assets/img/home-card-pic1.jpg";
import wavesWhite from "@/assets/img/waves-white.svg";
import logoBootstrap from "@/assets/img/logos/bootstrap5.jpg";
import logoTailwind from "@/assets/img/logos/icon-tailwind.jpg";
import logoVue from "@/assets/img/logos/vue.jpg";
import logoAngular from "@/assets/img/logos/angular.jpg";
import logoReact from "@/assets/img/logos/react.jpg";
import logoSketch from "@/assets/img/logos/sketch.jpg";
import AndhraPradesh from "@/assets/img/andhraPradesh.jpeg";
import telangana from "@/assets/img/telangana.jpeg";
import chennai from "@/assets/img/chennai.jpeg";
//hooks
const body = document.getElementsByTagName("body")[0];
onMounted(() => {
  body.classList.add("presentation-page");
  body.classList.add("bg-gray-200");
});
onUnmounted(() => {
  body.classList.remove("presentation-page");
  body.classList.remove("bg-gray-200");
});

const displayedText = ref("");
const fullText = "The future of plant science...";
let index = 0;

function typeText() {
  if (index < fullText.length) {
    displayedText.value += fullText[index];
    index++;
    setTimeout(typeText, 60);
  }
}

onMounted(() => {
  typeText();
});
</script>

<template>
  <div class="container position-sticky z-index-sticky top-0">
    <div class="row">
      <div class="col-12">
        <NavbarDefault :sticky="true" />
      </div>
    </div>
  </div>
  <header>
    <div
      class="page-header min-vh-100"
      :style="`background-image: url(${HomeCardPic})`"
      loading="lazy"
    >
      <span class="mask bg-gradient-dark opacity-5"></span>
      <div class="container">
        <div class="row">
          <div
            class="col-lg-8 col-md-7 d-flex justify-content-center flex-column"
          >
            <h1 class="text-white mb-4" v-html="displayedText"></h1>
            <p class="text-white opacity-8 lead pe-5 me-5">
              Introducing Ceres Agros, India's pioneering 100% water-soluble
              fertilizer solution. Revolutionizing agriculture with innovative
              products that boost yields, improve soil health, and drive
              sustainability.
            </p>
            <div class="buttons">
              <MaterialButton color="white" class="mt-4"
                >Get Started</MaterialButton
              >
              <MaterialButton color="none" class="text-white shadow-none mt-4"
                >Read more</MaterialButton
              >
            </div>
          </div>
        </div>
      </div>
    </div>
  </header>

  <!-- another view  -->

  <!-- <Header>
    <div
      class="page-header min-vh-100"
      :style="`background-image: url(${HomeCardPic})`"
      loading="lazy"
    >
      <div class="container">
        <div class="row">
          <div class="col-lg-7 position-relative">
            <h1
              class="text-white pt-3 mt-n5 me-2"
              :style="{ display: 'inline-block ' }"
            >
              Ceres Agro
            </h1>
            <p class="lead text-white pe-5 mt-5" :style="{ fontWeight: '500' }">
              Introducing Ceres Agro, India's pioneering water-insoluble
              fertilizer solution. Revolutionizing agriculture with innovative
              products that boost yields, improve soil health, and drive
              sustainability."
            </p>
          </div>
        </div>
      </div>
    </div>
  </Header> -->

  <div class="card card-body blur shadow-blur mx-3 mx-md-4 mt-n6">
    <PresentationCounter />
    <PresentationInformation />
    <BuiltByDevelopers />
    <!-- <PresentationExample :data="data" /> -->
    <PresentationPages />
    

    <!-- <div class="container">
      <div class="row">
        <div class="col-lg-4">
          <FilledInfoCard
            class="p-4"
            :color="{ text: 'white', background: 'bg-gradient-success' }"
            :icon="{ component: 'flag', color: 'white' }"
            title="Getting Started"
            description="Check the possible ways of working with our product and the necessary files for building your own project."
            :action="{
              route:
                'https://www.creative-tim.com/learning-lab/vue/overview/material-kit/',
              label: { text: 'Let\'s start', color: 'white' }
            }"
          />
        </div>
        <div class="col-lg-4">
          <FilledInfoCard
            class="px-lg-1 mt-lg-0 mt-4 p-4"
            height="h-100"
            :icon="{ component: 'precision_manufacturing', color: 'success' }"
            title="Plugins"
            description="Get inspiration and have an overview about the plugins that we
                used to create the Material Kit."
            :action="{
              route:
                'https://www.creative-tim.com/learning-lab/vue/input/material-kit/',
              label: { text: 'Read more' }
            }"
          />
        </div>
        <div class="col-lg-4">
          <FilledInfoCard
            class="px-lg-1 mt-lg-0 mt-4 p-4"
            :icon="{ component: 'receipt_long', color: 'success' }"
            title="Utility Classes"
            description="Material Kit is giving you a lot of pre-made elements. For those
                who want flexibility, we included many utility classes."
            :action="{
              route:
                'https://www.creative-tim.com/learning-lab/vue/utilities/material-kit/',
              label: { text: 'Read more' }
            }"
          />
        </div>
      </div>
    </div> -->
    <!-- <PresentationTestimonials /> -->

    <div
      class="container-fluid mt-sm-5 border-radius-xl"
      :style="{
        background: 'linear-gradient(195deg, rgb(66, 66, 74), rgb(25, 25, 25))',
      }"
    >
      <div
        class="page-header py-6 py-md-5 my-sm-3 mb-3 border-radius-xl"
        :style="`background-image: url(${HomeCardPic})`"
        loading="lazy"
      >
        <span class="mask bg-gradient-dark"></span>
        <div class="container">
          <div class="row">
            <div class="d-flex justify-content-center p-5">
              <div class="col-lg-8 ms-lg-5 text-center">
                <h3 class="text-white">
                  Why Choose Ceres Agros for Your Fertilizer Needs?
                </h3>
                <p class="text-white text-md mt-5">
                  Ceres Agros offers innovative, sustainable fertilizer solutions
                  that boost crop yields, improve soil health, and support
                  eco-friendly agriculture. With expert guidance and proven
                  results, we're your partner for agricultural success."
                </p>

                <a
                  href=""
                  class="btn btn-sm mb-0 bg-gradient-success px-5 py-3 mt-4"
                  >Join Our family</a
                >
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <div class="container">
      <div class="row">
        <div class="d-flex flex-column w-100 text-center p-5 mb-8">
          <h3>Available on these Locations</h3>
          <div class="d-flex justify-content-center mt-3 flex-wrap">
            <!-- <a
              href=""
              data-bs-toggle="tooltip"
              data-bs-placement="bottom"
              title="High demand area"
            >
              <img
                :src="chennai"
                alt="title"
                loading="lazy"
                :style="{ height: '120px' }"
              />
            </a> -->
            <a
              class="opacity-5 ms-3"
              href="#"
              data-bs-toggle="tooltip"
              data-bs-placement="bottom"
              title="Coming Soon"
            >
              <img
                :src="telangana"
                alt="title"
                loading="lazy"
                :style="{ height: '120px' }"
              />
            </a>
            <a
              href=""
              class="mx-3"
              data-bs-toggle="tooltip"
              data-bs-placement="bottom"
              title="home ground for us"
            >
              <img
                :src="AndhraPradesh"
                alt="title"
                loading="lazy"
                :style="{ height: '120px' }"
              />
            </a>
          </div>
        </div>
      </div>
    </div>
    <div class="py-5">
      <div class="container">
        <div class="row">
          <div class="col-lg-5 ms-auto">
            <h4 class="mb-1">Thank you for your support!</h4>
            <p class="lead mb-0">We deliver the best agriculture products</p>
          </div>
          <div class="col-lg-5 me-lg-auto my-lg-auto text-lg-end mt-5">
            <MaterialSocialButton
              route=""
              component="twitter"
              color="twitter"
              label="Tweet"
            />
            <MaterialSocialButton
              route=""
              component="facebook-square"
              color="facebook"
              label="Share"
            />
            <MaterialSocialButton
              route=""
              component="instagram"
              color="pinterest"
              label="Insta"
            />
          </div>
        </div>
      </div>
    </div>
  </div>
  <DefaultFooter />
</template>
