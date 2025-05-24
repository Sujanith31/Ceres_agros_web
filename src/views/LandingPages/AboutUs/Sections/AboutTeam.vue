<script setup>
// example component
import HorizontalTeamCard from "@/examples/cards/teamCards/HorizontalTeamCard.vue";

// images
import emma from "@/assets/img/team-5.jpg";
import william from "@/assets/img/bruce-mars.jpg";
import ivana from "@/assets/img/ivana-squares.jpg";
import marquez from "@/assets/img/ivana-square.jpg";
import Sunil from "@/assets/img/team-4.jpg";
</script>

<template>
  <section class="pb-5 position-relative bg-gradient-dark mx-n3">
    <div class="container">
      <div class="row">
        <div class="col-md-8 text-start mb-5 mt-5">
          <h3 class="text-white z-index-1 position-relative">
            Meet the Visionaries
          </h3>
          <!-- <p class="text-white opacity-8 mb-0">
            There’s nothing I really wanted to do in life that I wasn’t able to
            get good at. That’s my skill.
          </p> -->
        </div>
      </div>
      <div class="row">
        <div class="col-lg-6 col-12">
          <HorizontalTeamCard
            class="mt-lg-4 mt-5 z-index-2"
            :image="marquez"
            :profile="{ name: 'Devella Sridhar Reddy', link: 'javascript:;' }"
            :position="{ label: 'Founder', color: 'success' }"
            description="Through strong industry relationships and a focus on sourcing excellence, our founder secures the best ingredients and technologies for our fertilizers, ultimately benefiting your Crop's productivity."
          />
        </div>
        <div class="col-lg-6 col-12">
          <HorizontalTeamCard
            class="mt-lg-4 mt-5"
            :image="william"
            :profile="{ name: 'Esukapalli RajaShekar Reddy', link: 'javascript:;' }"
            :position="{ label: 'Partner', color: 'success' }"
            description="Our visionary leader actively explores new horizons, building strong relationships with clients and farmers in emerging regions to understand their needs and foster collaborative growth."
          />
        </div>
      </div>
      <div class="row mt-4">
        <!-- <div class="col-lg-6 col-12">
          <HorizontalTeamCard
            class="mt-4 z-index-2"
            :image="Sunil"
            :profile="{ name: 'Varidireddy Himavanth', link: 'javascript:;' }"
            :position="{ label: 'Finance Director', color: 'success' }"
            description="Leads financial strategy, planning, and management to drive business growth and profitability."
          />
        </div> -->
        <div class="col-lg-6 col-12">
          <HorizontalTeamCard
            class="mt-4"
            :image="emma"
            :profile="{ name: 'Devella Kathyayini', link: 'javascript:;' }"
            :position="{ label: 'Partner', color: 'success' }"
            description="Orchestrating marketing vision and administrative excellence to fuel business expansion and operational synergy."
          />
        </div>
      </div>
      <!-- <div class="row mt-4">
        <div class="col-lg-6 col-12">
          <HorizontalTeamCard
            class="mt-4 z-index-2"
            :image="Sunil"
            :profile="{ name: 'Vengalreddy Suneel', link: 'javascript:;' }"
            :position="{ label: 'Operations Director', color: 'success' }"
            description="Manages and oversees daily operations to ensure efficiency and effectiveness."
          />
        </div>
      </div> -->
    </div>
  </section>
</template>
