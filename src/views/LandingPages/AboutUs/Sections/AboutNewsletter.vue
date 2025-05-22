<script setup>
import { onMounted } from "vue";
//Vue Material Kit 2 components
import MaterialInput from "@/components/MaterialInput.vue";
import MaterialButton from "@/components/MaterialButton.vue";

// material-input
import setMaterialInput from "@/assets/js/material-input";
onMounted(() => {
  setMaterialInput();
});
</script>
<template>
  <section class="my-5 pt-5">
    <div class="container">
      <div class="row">
        <div class="col-md-6 m-auto">
          <h4>The Future of Farming, In Your Hands Now.</h4>
          <p class="mb-4">
            Want to stay connected and receive updates from our team? Enter your
            email address below to join our community.
          </p>
          <div class="row">
            <div class="col-8">
              <MaterialInput
                class="input-group-outline"
                id="email"
                :label="{ text: 'Email Here...', class: 'form-label' }"
                type="email"
              />
            </div>
            <div class="col-4 ps-0">
              <MaterialButton
                variant="gradient"
                color="success"
                class="mb-0 h-100 position-relative z-index-2"
                >Join US</MaterialButton
              >
            </div>
          </div>
        </div>
        <div class="col-md-5 ms-auto mt-6 md-mt-0">
          <div class="position-relative">
            <img
              class="max-width-50 w-65 position-relative z-index-2"
              src="@/assets/img/macbookb.jpg"
              alt="image"
            />
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
