<script setup>
// example components
import DefaultInfoCard from "../../../../examples/cards/infoCards/DefaultInfoCard.vue";
import CenteredBlogCard from "../../../../examples/cards/blogCards/CenteredBlogCard.vue";
</script>
<template>
  <section class="py-7">
    <div class="container">
      <div class="row align-items-center">
        <div class="col-lg-6">
          <div class="row justify-content-start">
            <DefaultInfoCard
              color="info"
              icon="public"
              title="Quality in Every Trait"
              description="At Ceres Agros, we define high yield by quality, not just quantity. A true harvest is measured by size, weight, shape, colour, taste, aroma, and shelf life — and our technology ensures every crop meets these seven essential traits."
            />
            <DefaultInfoCard
              color="info"
              icon="payments"
              title="Nourishing the Soil, Scientifically"
              description="
Our formulations work from the ground up, improving soil porosity, carbon levels, pH balance, and boosting beneficial microflora. This enhances water retention, builds natural disease resistance, and creates a fertile, well-structured soil ready for cropping with slow-release nutrition and root activators.
"
            />
          </div>
          <div class="row justify-content-start mt-4">
            <DefaultInfoCard
              color="info"
              icon="apps"
              title="Phase-Specific Plant Care"
              description="We deliver balanced nutrition tailored to each plant phase, from rooting to fruiting. Our understanding of bio-chemical triggers helps us customize inputs that drive efficient growth at every stage — especially during flowering and fruit development.
"
            />
            <DefaultInfoCard
              color="info"
              icon="3p"
              title="Unlocking Plant Potential"
              description="Ceres Agros solutions also build stress tolerance and improve nutrient uptake efficiency, ensuring faster and complete bio-reactions. The result: healthier plants, stronger yields, and consistent growth throughout the crop cycle."
            />
          </div>
        </div>
        <div class="col-lg-4 ms-auto mt-lg-0 mt-6">
          <CenteredBlogCard
            image="https://images.unsplash.com/photo-1544717302-de2939b7ef71?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=1950&q=80"
            title="Get insights on Search"
            description="Looking for specific information on our 100% water-soluble fertilizers, application techniques, or crop-specific solutions? Our search tool allows you to quickly navigate our extensive resources and find the precise insights you need to optimize your farm's potential."
          />
        </div>
      </div>
    </div>
  </section>
</template>
