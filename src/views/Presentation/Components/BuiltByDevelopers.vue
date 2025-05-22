<script setup>
import cropbush from "@/assets/img/vue-mk-header.jpg"
</script>
<template>
  <div class="container mt-sm-5">
    <div
      class="page-header py-6 py-md-5 my-sm-3 mb-3 border-radius-xl"
      :style="`background-image: url(${cropbush})`"
      loading="lazy"
    >
      <span class="mask bg-gradient-dark"></span>
      <div class="container">
        <div class="row">
          <div class="col-lg-6 ms-lg-5">
            <h4 class="text-white">Built by soil health innovators.</h4>
            <h1 class="text-white">
              We know how to make soil healthy for your crops
            </h1>
            <p class="lead text-white opacity-8">
              We're dedicated to understanding what makes soil thrive. Our
              innovations are all about creating the best foundation for your
              crops to flourish
            </p>
            <a
              href="https://www.creative-tim.com/learning-lab/vue/overview/material-kit/"
              class="text-white icon-move-right"
            >
              Know more
              <i class="fas fa-arrow-right text-sm ms-1"></i>
            </a>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
