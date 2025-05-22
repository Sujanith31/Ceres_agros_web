<script setup>
import { onMounted } from "vue";

//example components
import DefaultNavbar from "@/examples/navbars/NavbarDefault.vue";
import DefaultFooter from "@/examples/footers/FooterDefault.vue";

//image
import image from "@/assets/img/illustrations/illustration-signin.jpg";
import farmHouse from "@/assets/img/farm-warehouse.jpeg";
import contactCover from "@/assets/img/contact-page-images.jpg";
import contactCover2 from "@/assets/img/contact-page-image-two.jpg";

//material components
import MaterialInput from "@/components/MaterialInput.vue";
import MaterialTextArea from "@/components/MaterialTextArea.vue";
import MaterialButton from "@/components/MaterialButton.vue";

// material-input
import setMaterialInput from "@/assets/js/material-input";
onMounted(() => {
  setMaterialInput();
});
</script>
<template>
  <div class="container position-sticky z-index-sticky top-0">
    <div class="row">
      <div class="col-12">
        <DefaultNavbar
          :sticky="true"
          :action="{
            route: 'https://www.creative-tim.com/product/vue-material-kit-pro',
            color: 'bg-gradient-success',
            label: 'Buy Now',
          }"
        />
      </div>
    </div>
  </div>
  <section>
    <div class="page-header min-vh-100">
      <div class="container">
        <div class="row">
          <div
            class="col-lg-6 position-relative bg-cover px-0"
            :style="{ backgroundImage: `url(${contactCover2})` }"
            loading="lazy"
          >
            <div
              class="z-index-2 text-center d-flex h-100 w-100 d-flex m-auto justify-content-center"
            >
              <div class="mask bg-gradient-dark opacity-8"></div>
              <div
                class="p-5 ps-sm-8 position-relative text-start my-auto z-index-2"
              >
                <h3 class="text-white">Contact Information</h3>
                <p class="text-white opacity-8 mb-4">
                  Fill up the form and our Team will get back to you within 24
                  hours.
                </p>
                <div class="d-flex p-2 text-white">
                  <div>
                    <i class="fas fa-phone text-sm"></i>
                  </div>
                  <div class="ps-3">
                    <span class="text-sm opacity-8">+91 9989595959</span>
                  </div>
                </div>
                <div class="d-flex p-2 text-white">
                  <div>
                    <i class="fas fa-envelope text-sm"></i>
                  </div>
                  <div class="ps-3">
                    <span class="text-sm opacity-8">hello@ceresagros.co</span>
                  </div>
                </div>
                <div class="d-flex p-2 text-white">
                  <div>
                    <i class="fas fa-map-marker-alt text-sm"></i>
                  </div>
                  <div class="ps-3">
                    <span class="text-sm opacity-8"
                      >8th Floor, Vaishnavi Cymbol, Puppalaguda
                      Road,Hyderabad,Telangana, 500089</span
                    >
                  </div>
                </div>
                <div class="mt-4">
                  <MaterialButton
                    color="none"
                    size="lg"
                    class="btn-icon-only btn-link text-white mb-0"
                    data-toggle="tooltip"
                    data-placement="bottom"
                    data-original-title="Log in with Facebook"
                  >
                    <i class="fab fa-facebook"></i>
                  </MaterialButton>
                  <MaterialButton
                    color="none"
                    size="lg"
                    class="btn-icon-only btn-link text-white mb-0"
                    data-toggle="tooltip"
                    data-placement="bottom"
                    data-original-title="Log in with Twitter"
                  >
                    <i class="fab fa-twitter"></i>
                  </MaterialButton>
                  <MaterialButton
                    color="none"
                    size="lg"
                    class="btn-icon-only btn-link text-white mb-0"
                    data-toggle="tooltip"
                    data-placement="bottom"
                    data-original-title="Log in with Dribbble"
                  >
                    <i class="fab fa-dribbble"></i>
                  </MaterialButton>
                  <MaterialButton
                    color="none"
                    size="lg"
                    class="btn-icon-only btn-link text-white mb-0"
                    data-toggle="tooltip"
                    data-placement="bottom"
                    data-original-title="Log in with Instagram"
                  >
                    <i class="fab fa-instagram"></i>
                  </MaterialButton>
                </div>
              </div>
            </div>
          </div>
          <div
            class="mt-8 col-xl-5 col-lg-6 col-md-7 d-flex flex-column ms-auto me-auto ms-lg-auto me-lg-5"
          >
            <div
              class="card d-flex blur justify-content-center shadow-lg my-sm-0 my-sm-6 mt-8 mb-5"
            >
              <div
                class="card-header p-0 position-relative mt-n4 mx-3 z-index-2 bg-transparent"
              >
                <div
                  class="bg-gradient-success shadow-success border-radius-lg p-3"
                >
                  <h3 class="text-white text-success mb-0">Contact us</h3>
                </div>
              </div>
              <div class="card-body">
                <p class="pb-3">
                  For further questions, including partnership opportunities,
                  please email hello@ceresagros.co or contact using our form.
                </p>
                <form id="contact-form" method="post" autocomplete="off">
                  <div class="card-body p-0 my-3">
                    <div class="row">
                      <div class="col-md-6">
                        <MaterialInput
                          class="input-group-static mb-4"
                          type="text"
                          label="Full Name"
                          placeholder="Full Name"
                        />
                      </div>
                      <div class="col-md-6 ps-md-2">
                        <MaterialInput
                          class="input-group-static mb-4"
                          type="email"
                          label="Email"
                          placeholder="hello@ceresagros.co"
                        />
                      </div>
                      <div class="col-md-6 ps-md-2">
                        <MaterialInput
                          class="input-group-static mb-4"
                          type="number"
                          label="Contact"
                          placeholder="+91 999-999-9999"
                        />
                      </div>
                    </div>
                    <div class="form-group mb-0 mt-md-0 mt-4">
                      <MaterialTextArea
                        id="message"
                        class="input-group-static mb-4"
                        :rows="6"
                        placeholder="Describe your enquiry in at least 250 characters"
                        >How can we help you?</MaterialTextArea
                      >
                    </div>
                    <div class="row">
                      <div class="col-md-12 text-center">
                        <MaterialButton
                          variant="gradient"
                          color="success"
                          class="mt-3 mb-0"
                          >Send Message</MaterialButton
                        >
                      </div>
                    </div>
                  </div>
                </form>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
  <DefaultFooter />
</template>
<style>
.class {
  background-repeat: no-repeat;
}
</style>
