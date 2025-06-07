<script setup>
// example components
import TransparentBlogCard from "../../../../examples/cards/blogCards/TransparentBlogCard.vue";
import BackgroundBlogCard from "../../../../examples/cards/blogCards/BackgroundBlogCard.vue";

//Vue Material Kit 2 components
import post1 from "@/assets/img/examples/testimonial-6-2.jpg";
import post2 from "@/assets/img/examples/testimonial-6-3.jpg";
import post3 from "@/assets/img/examples/blog-9-4.jpg";
import post4 from "@/assets/img/examples/blog2.jpg";

import booster from "@/assets/img/booster.png";
import IOT from "@/assets/img/IOT.png";
import Tech from "@/assets/img/Tech.png";
</script>
<template>
  <section class="py-3">
    <div class="container">
      <div class="row">
        <div class="col-lg-6">
          <h3 class="mb-5">Check Out latest blogposts</h3>
        </div>
      </div>
      <div class="row">
        <div class="col-lg-4 col-sm-6">
          <TransparentBlogCard
            :image="IOT"
            title="Precision Agriculture with IoT and Smart Sensors"
            description="The integration of Internet of Things (IoT) technologies in agriculture has enabled real-time monitoring of soil and plant health. Biodegradable leaf and soil sensors, developed by research centers like NSF-funded IoT4Ag, can detect nutrient levels and environmental conditions. These sensors, combined with ground and aerial robots, provide farmers with timely insights to adjust practices, enhancing efficiency and sustainability."
            :action="{
              route:
                'https://www.businessinsider.com/iot-technology-precision-agriculture-transforming-farming-2025-5?utm_source=chatgpt.com',
              color: 'success',
              label: 'Read more',
            }"
          />
        </div>
        <div class="col-lg-4 col-sm-6">
          <TransparentBlogCard
            :image="Tech"
            title="CRISPR and Genome Editing Technologies"
            description="CRISPR/Cas genome editing systems have become pivotal in plant genetics, allowing precise, targeted modifications to DNA sequences. These technologies have been applied to develop virus-resistant plants and improve traits such as herbicide tolerance and stress responses across various crops. Offering a more effective and prolonged efficiency compared to previous antiviral approaches, this genome editing system holds promise for alleviating crop losses due to viral infections."
            :action="{
              route: 'https://pubmed.ncbi.nlm.nih.gov/35216418/',
              color: 'success',
              label: 'Read more',
            }"
          />
        </div>
        <div class="col-lg-4 col-sm-6">
          <TransparentBlogCard
            :image="booster"
            title="Discovery of the “Booster” Gene Enhancing Photosynthesis"
            description="Scientists at Oak Ridge National Laboratory identified a naturally occurring gene in poplar trees, termed “Booster,” which significantly enhances photosynthetic activity. This gene boosts plant growth and biomass production, offering potential applications in improving crop yields and carbon sequestration."
            :action="{
              route:
                'https://www.ornl.gov/news/landmark-photosynthesis-gene-discovery-boosts-plant-height-advances-crop-science?utm_source=chatgpt.com ',
              color: 'success',
              label: 'Read more',
            }"
          />
        </div>
        <!-- <div class="col-lg-3 col-md-12 col-12">
          <BackgroundBlogCard
            :image="post4"
            title="Discovery of the “Booster” Gene Enhancing Photosynthesis"
            description="Scientists at Oak Ridge
          National Laboratory identified a naturally occurring gene in poplar
          trees, termed “Booster,” which significantly enhances photosynthetic
          activity. This gene boosts plant growth and biomass production,
          offering potential applications in improving crop yields and carbon
          sequestration."
            :action="{
              route:
                'https://www.ornl.gov/news/landmark-photosynthesis-gene-discovery-boosts-plant-height-advances-crop-science?utm_source=chatgpt.com',
              label: 'Read more',
              color: 'success',
            }"
          /> -->
        <!-- </div> -->
      </div>
    </div>
  </section>
</template>
