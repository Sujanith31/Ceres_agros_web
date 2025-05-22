<script setup>
import ExampleCard from "../Components/ExampleCard.vue";
import MaterialBadge from "../../../components/MaterialBadge.vue";

// images
import imgSigninCover from "@/assets/img/signin-cover.png";
// import farmersLand from "@/assets/img/farmers-land.jpeg";
import farmersLand from "@/assets/img/farmers-Home_apge.jpg";
import balconyImage4 from "@/assets/img/balcony-garden-4.jpeg";
import blackCropImage from "@/assets/img/home-card-pic1.jpg";
import happyWorker from "@/assets/img/happyworker.jpeg";
import logoOne from "@/assets/img/logo-one.jpg";
import logoTwo from "@/assets/img/logo-second.jpg";
import logoThree from "@/assets/img/logo-Three.jpg";
import logoFour from "@/assets/img/logo-Four.jpg";
</script>
<template>
  <section class="py-5">
    <div class="container">
      <div class="row">
        <div class="row text-center my-sm-5 mt-5">
          <div class="col-lg-6 mx-auto">
            <div class="badge">
              <MaterialBadge color="success" class="mb-3"
                >Boost Production</MaterialBadge
              >
            </div>
            <h2 class="">ADVANCED NPK SPECIALITY BLENDS WITH MET</h2>
            <p class="lead">
              Turbocharge crops with MET for improved soil health
               consistent higher yeilds - seasons after seasons with our 100% water-soluble fertilisers.
            </p>
          </div>
        </div>
      </div>
    </div>
    <div class="container mt-5">
      <div class="row">
        <div class="col-md-8">
          <div class="row mt-4">
            <div class="col-md-6 mt-md-0 mt-5">
              <ExampleCard
                class="shadow-lg"
                title=""
                :image="logoOne"
                route="about"
              />
            </div>
            <div class="col-md-6 mt-md-0 mt-5">
              <ExampleCard
                class="shadow-lg"
                title=""
                :image="logoTwo"
                route="contactus"
              />
            </div>
          </div>
          <div class="row mt-0">
            <div class="col-md-6 mt-md-0 mt-5">
              <ExampleCard
                classes="mt-5"
                title=""
                :image="logoThree"
                route="signin-basic"
              />
            </div>
            <div class="col-md-6 mt-md-0 mt-5">
              <ExampleCard
                classes="shadow-lg"
                title=""
                :image="logoFour"
                route="author"
              />
            </div>
          </div>
        </div>
        <div class="col-md-3 mx-auto mt-md-0 mt-3">
          <div class="position-sticky" style="top: 100px !important">
            <h3>
              The science of smiles: How our innovative formulas create
              healthier crops and happier farmers.
            </h3>
            <h6 class="text-secondary font-weight-normal">
              Explore these possibilities to see our business impact. Let's
              prioritize your farm's bottom line over pure aesthetics.
            </h6>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
<style scoped>
  .badge{
    font-size: 16px !important;
  }
</style>