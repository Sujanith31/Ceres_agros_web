<script setup>
// example component
import DefaultCounterCard from "../../../../examples/cards/counterCards/DefaultCounterCard.vue";
</script>
<template>
  <section class="pt-4 pb-6" id="count-stats">
    <div class="container">
      <!-- <div class="row mb-7">
        <div class="col-lg-2 col-md-4 col-6 mb-4">
          <img
            class="w-100 opacity-7"
            src="@/assets/img/logos/gray-logos/logo-coinbase.svg"
            alt="logo"
          />
        </div>
        <div class="col-lg-2 col-md-4 col-6 mb-4">
          <img
            class="w-100 opacity-7"
            src="@/assets/img/logos/gray-logos/logo-nasa.svg"
            alt="logo"
          />
        </div>
        <div class="col-lg-2 col-md-4 col-6 mb-4">
          <img
            class="w-100 opacity-7"
            src="@/assets/img/logos/gray-logos/logo-netflix.svg"
            alt="logo"
          />
        </div>
        <div class="col-lg-2 col-md-4 col-6 mb-4">
          <img
            class="w-100 opacity-7"
            src="@/assets/img/logos/gray-logos/logo-pinterest.svg"
            alt="logo"
          />
        </div>
        <div class="col-lg-2 col-md-4 col-6 mb-4">
          <img
            class="w-100 opacity-7"
            src="@/assets/img/logos/gray-logos/logo-spotify.svg"
            alt="logo"
          />
        </div>
        <div class="col-lg-2 col-md-4 col-6 mb-4">
          <img
            class="w-100 opacity-7"
            src="@/assets/img/logos/gray-logos/logo-vodafone.svg"
            alt="logo"
          />
        </div>
      </div> -->
      <div class="row justify-content-center text-center">
        <div class="col-md-3">
          <DefaultCounterCard
            title="Hectares Nourished"
            description="Ensuring fertile ground and healthy growth across vast farmlands."
            :count="5234"
            :duration="3000"
          />
        </div>
        <div class="col-md-3">
          <DefaultCounterCard
            title="Crop Varieties Supported"
            description="Formulations tailored to a wide range of crops, ensuring optimal nutrient delivery."
            :count="300"
            suffix="+"
            :duration="3000"
          />
        </div>
        <div class="col-md-3">
          <DefaultCounterCard
            title="Quality Tests Performed"
            description="Ensuring our fertilizers meet the highest standards for optimal plant health."
            :count="1000"
            suffix="+"
            :duration="4000"
          />
        </div>
      </div>
    </div>
  </section>
</template>
