<script setup>
import DefaultReviewCard from "@/examples/cards/reviewCards/DefaultReviewCard.vue";
</script>
<template>
  <section class="py-7">
    <div class="container">
      <div class="row">
        <div class="col-lg-6 mx-auto text-center">
          <h2 class="mb-0">Trusted by over</h2>
          <h2 class="text-gradient text-success mb-3">179,477+ Farmers</h2>
          <p class="lead">
            "Many leading agricultural institutions, top farming organizations,
            and innovative agritech companies trust Ceres Agros products for
            their fertilizer formulations
          </p>
        </div>
      </div>
      <div class="row mt-6">
        <DefaultReviewCard
          name="Nick Willever"
          date="1 day ago"
          review='"This is an excellent product, the documentation is excellent and
          helped me get things done more efficiently."'
          :rating="5.0"
        />
        <DefaultReviewCard
          class="ms-md-auto"
          color="bg-gradient-success"
          name="Ritesh Kushwaha"
          date="1 week ago"
          review='"I had the freedom to customise formulations from R&D team. I
                  could cutomise any formulation which are exclusive for my company
                  and really affordable !!!"'
          :rating="5.0"
        />

        <DefaultReviewCard
          name="Samuel Kamuli"
          date="3 weeks ago"
          review='"Great product. Helped me cut the time to set up a site. I
                  used the components within instead of starting from scratch. I
                  highly recommend for developers who want to spend more time on
                  the backend!."'
          :rating="5.0"
        />
      </div>
      <!-- <hr class="horizontal dark my-5" /> -->
      <!-- <div class="row">
        <div class="col-lg-2 col-md-4 col-6 ms-auto">
          <img
            class="w-100 opacity-6"
            src="@/assets/img/logos/gray-logos/logo-apple.svg"
            alt="Logo"
          />
        </div>
        <div class="col-lg-2 col-md-4 col-6">
          <img
            class="w-100 opacity-6"
            src="@/assets/img/logos/gray-logos/logo-facebook.svg"
            alt="Logo"
          />
        </div>
        <div class="col-lg-2 col-md-4 col-6">
          <img
            class="w-100 opacity-6"
            src="@/assets/img/logos/gray-logos/logo-nasa.svg"
            alt="Logo"
          />
        </div>
        <div class="col-lg-2 col-md-4 col-6 ms-lg-0 ms-md-auto">
          <img
            class="w-100 opacity-6"
            src="@/assets/img/logos/gray-logos/logo-vodafone.svg"
            alt="Logo"
          />
        </div>
        <div class="col-lg-2 col-md-4 col-6 me-md-auto mx-md-0 mx-auto">
          <img
            class="w-100 opacity-6"
            src="@/assets/img/logos/gray-logos/logo-digitalocean.svg"
            alt="Logo"
          />
        </div>
      </div> -->
    </div>
  </section>
</template>
