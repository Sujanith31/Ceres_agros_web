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
  <section>
    <div class="statments-containers">
      <div class="statment-one">
        <div class="statment-one-left">
          <DefaultInfoCard
            color="info"
            icon="public"
            title="Mission Statement"
            description="To revolutionize agriculture with innovative, sustainable solutions that enhance soil health and crop productivity, ensuring food security for future generations."
          />
        </div>
        <div class="statment-one-right">
          <img :src="picOne" alt="" style="height: 40vh" />
        </div>
      </div>
      <div class="statment-two">
        <div class="statment-one-right">
          <img :src="ThreePs" alt="" style="height: 40vh" />
        </div>
        <div class="statment-one-left">
          <DefaultInfoCard
            color="info"
            icon="public"
            title="The 3 P’s of Ceres Agros"
            description=""
          />
          <ul>
            <li>Precision – Tailored nutrient delivery.</li>
            <li>Performance – Consistent, measurable results.</li>
            <li>Progress – Advancing agriculture for a sustainable future.</li>
          </ul>
        </div>
      </div>
      <div class="statment-one">
        <div class="statment-one-left">
          <DefaultInfoCard
            color="info"
            icon="public"
            title="Our Core Values"
            description=""
          />
          <ul>
            <li>Innovation – We lead with science and stay future focused.</li>
            <li>Integrity – Transparency in every partnership.</li>
            <li>Sustainability – Growing responsibly for generations.</li>
            <li>Excellence – Uncompromising quality in every batch.</li>
          </ul>
        </div>
        <div class="statment-one-right">
          <img :src="picThree" alt="" style="height: 40vh" />
        </div>
      </div>
    </div>
  </section>
</template>
<style scoped>
.statment-pictures {
  margin-top: -160px !important;
}
.statment-two {
  width: 100%;
  /* background-color: aqua; */
  display: flex;
  flex-wrap: wrap;
  justify-content: space-evenly;
  align-items: center;
  margin-bottom: 70px;
}
.statment-one {
  width: 100%;
  /* background-color: aqua; */
  display: flex;
  flex-wrap: wrap-reverse;
  justify-content: space-evenly;
  align-items: center;
  margin-bottom: 70px;
}
.statment-one-left {
  /* background-color: black; */
  width: 550px;
}
.statment-one-right {
  /* background-color: blue; */
}

@media (max-width:450px){
  img{
    width: 300px !important;
    height: 30vh !important;
  }
}
</style>
