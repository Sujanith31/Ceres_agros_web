<script setup>
import RotatingCard from "../../../examples/cards/rotatingCards/RotatingCard.vue";
import RotatingCardFront from "../../../examples/cards/rotatingCards/RotatingCardFront.vue";
import RotatingCardBack from "../../../examples/cards/rotatingCards/RotatingCardBack.vue";
import DefaultInfoCard from "../../../examples/cards/infoCards/DefaultInfoCard.vue";

//images
import balconyImg1 from "@/assets/img/balcony-garden-1.jpeg";
</script>
<template>
  <section class="my-5 py-5">
    <div class="container">
      <div class="row align-items-center">
        <div class="col-lg-4 ms-auto me-auto p-lg-4 mt-lg-0 mt-4">
          <RotatingCard>
            <RotatingCardFront
              :image="balconyImg1"
              icon="touch_app"
              title="Reimagine Your <br> Harvest"
              description="All the fertilizer solutions you need for a thriving harvest have been re-imagined with Ceres Agros innovative approach, bringing new life to your crops and fields."
            />

            <RotatingCardBack
              image="https://images.unsplash.com/photo-1498889444388-e67ea62c464b?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=1365&q=80"
              title="Discover More"
              description=" Accelerate Your Agricultural Success with Ceres Agros Ready-to-Use Fertilizer Solutions - From Soil Prep to Harvest, We've Got You Covered."
              :action="[
                {
                  route: './/sections/page-sections/hero-sections.html',
                  label: 'Check OUt Now',
                },
              ]"
            />
          </RotatingCard>
        </div>
        <div class="col-lg-6 ms-auto">
          <div class="row justify-content-start">
            <DefaultInfoCard
              icon="content_copy"
              title="Boost Your Yields"
              description="Unlock the full potential of your crops with our high-quality, nutrient-rich fertilizers designed for optimal growth."
            />
            <DefaultInfoCard
              icon="flip_to_front"
              title="Scientifically Formulated"
              description="Our fertilizers are developed through rigorous research and testing to provide the precise balance of nutrients your plants need."
            />
          </div>
          <div class="row justify-content-start mt-5">
            <DefaultInfoCard
              class="mt-3"
              icon="price_change"
              title="Invest in Growth"
              description="Maximize your return on investment with our cost-effective fertilizers that deliver exceptional results and long-term soil health."
            />
            <DefaultInfoCard
              class="mt-3"
              icon="devices"
              title="Reliable Delivery & Support"
              description="We ensure timely delivery of our fertilizers and provide expert support to help you achieve your farming goals."
            />
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
