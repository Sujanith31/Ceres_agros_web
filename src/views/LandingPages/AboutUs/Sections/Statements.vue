<script setup>
// example components
import DefaultInfoCard from "../../../../examples/cards/infoCards/DefaultInfoCard.vue";
import CenteredBlogCard from "../../../../examples/cards/blogCards/CenteredBlogCard.vue";
import check from "@/assets/img/balcony-garden-4.jpeg";
import picOne from "@/assets/img/statment-1.jpg";
import HappyWorker from "@/assets/img/happyworker.jpeg";
import picThree from "@/assets/img/statment-3.jpg";
import ThreePs from "@/assets/img/threePs.jpg";
</script>
<template>
  <section class="py-7">
    <div class="container">
      <div class="row align-items-center">
        <div class="col-lg-12">
          <div class="row justify-content-start">
            <DefaultInfoCard
              color="info"
              icon="public"
              title="Vision Statement"
              description="To be the world’s most trusted manufacturer of intelligent plant nutrition, driving sustainable growth through innovation and quality.
Empowering agriculture with tomorrow’s technology, today."
            />
          </div>
        </div>
        <div class="col-lg-4 ms-auto mt-lg-0">
          <!-- <CenteredBlogCard
            image="https://images.unsplash.com/photo-1544717302-de2939b7ef71?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=1950&q=80"
            title="Get insights on Search"
            description="Looking for specific information on our water-insoluble fertilizers, application techniques, or crop-specific solutions? Our search tool allows you to quickly navigate our extensive resources and find the precise insights you need to optimize your farm's potential."
          /> -->
          <img
            class="statment-pictures"
            style="height: 40vh"
            :src="picOne"
            alt=""
          />
        </div>
      </div>
    </div>
    <div class="container mt-6">
      <div class="row align-items-center">
        <div class="col-lg-6">
          <div class="row justify-content-start">
            <img style="height: 40vh; width: 500px" :src="ThreePs" alt="" />
          </div>
        </div>
        <div class="col-lg-4 ms-auto mt-lg-0">
          <!-- <CenteredBlogCard
            image="https://images.unsplash.com/photo-1544717302-de2939b7ef71?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=1950&q=80"
            title="Get insights on Search"
            description="Looking for specific information on our water-insoluble fertilizers, application techniques, or crop-specific solutions? Our search tool allows you to quickly navigate our extensive resources and find the precise insights you need to optimize your farm's potential."
          /> -->
          <DefaultInfoCard
            style="width: 500px"
            color="info"
            icon="public"
            title="The 3 P’s of Ceres Agros"
            description="Precision – Tailored nutrient delivery. . . . 
            Performance – Consistent, measurable results.
            Progress – Advancing agriculture for a sustainable future."
          />
        </div>
      </div>
    </div>
    <div class="container mt-6">
      <div class="row align-items-center">
        <div class="col-lg-12">
          <div class="row justify-content-start">
            <DefaultInfoCard
              color="info"
              icon="public"
              title="Our Core Values"
              description="Innovation – We lead with science and stay future focused.  .  .  .
              Integrity – Transparency in every partnership. . .      .   .  .  .  .  .
              Sustainability – Growing responsibly for generations.  .  .  .  . Excellence – Uncompromising quality in every batch.  .  .  .  ."
            />
          </div>
        </div>
        <div class="col-lg-4 ms-auto mt-lg-0">
          <!-- <CenteredBlogCard
            image="https://images.unsplash.com/photo-1544717302-de2939b7ef71?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=1950&q=80"
            title="Get insights on Search"
            description="Looking for specific information on our water-insoluble fertilizers, application techniques, or crop-specific solutions? Our search tool allows you to quickly navigate our extensive resources and find the precise insights you need to optimize your farm's potential."
          /> -->
          <img
            class="statment-pictures"
            style="height: 40vh"
            :src="picThree"
            alt=""
          />
        </div>
      </div>
    </div>
  </section>
</template>
<style scoped>
.statment-pictures {
  margin-top: -160px !important;
}
</style>
