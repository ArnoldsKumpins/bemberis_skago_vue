<template>
  <div>
    <!-- Use the NavigationBar component at the top -->
    <NavigationBar />

    <!-- Section 1: Regular image with a bottom overlay box -->
    <section class="position-relative mb-4">
      <img :src="image1" alt="Image 1" class="img-fluid w-100 custom-img" />
      <!-- The overlay box overlaps the bottom of the image slightly -->
      <div id="img1-box" class="overlay-box position-absolute text-center mx-5">
        <div class="text-normal">Vadlīniju izstrāde un ieviešana Jūsu uzņēmumam,</div>
        <div class="text-large">
          Lai Jūsu uzņēmumu ievērotu <strong>īstie</strong> klienti!
        </div>
      </div>
    </section>

    <!-- Section 2: Image with 30% opacity and overlay content -->
    <section class="position-relative">
      <img
        :src="image2"
        alt="Image 2"
        class="img-fluid w-100 custom-img custom-opacity"
      />
      <div class="overlay-content position-absolute top-50 w-100 text-center">
        <h2 class="img-title">Mēs piedāvājam:</h2>

        <div class="container">
          <div class="row justify-content-center gap-4 gap-md-0">
            <!-- Box 1 (60% width on desktop) -->
            <div class="col-12 col-md-7">
              <div class="custom-box d-flex flex-column position-relative p-4">
                <span class="position-absolute top-0 start-0 p-3 small-text"
                  >Konsultācijas</span
                >
                <span class="text-center mx-auto main-text"
                  >Sabiedriskajās attiecībās</span
                >
              </div>
            </div>

            <!-- Box 2 (40% width on desktop) -->
            <div class="col-12 col-md-5">
              <div class="custom-box d-flex flex-column position-relative p-4">
                <span class="position-absolute top-0 start-0 p-3 small-text"
                  >Uzņēmuma</span
                >
                <span class="text-center mx-auto main-text">Zīmola</span>
                <span class="position-absolute bottom-0 end-0 p-3 small-text"
                  >izveidi</span
                >
              </div>
            </div>

            <!-- Box 3 (Centered below, between Box 1 and Box 2) -->
            <div class="col-12 col-md-5 mx-auto">
              <div id="img2-box3" class="custom-box d-flex flex-column position-relative p-4">
                <span class="text-center mx-auto main-text">Stratēģiskā plāna</span>
                <span class="position-absolute bottom-0 end-0 p-3 small-text"
                  >izstrādi</span
                >
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
import NavigationBar from "@/components/NavigationBar.vue";

export default {
  name: "HomePage",
  components: {
    NavigationBar,
  },
  data() {
    return {
      // Import the images from the assets folder
      image1: require("@/assets/images/image_1.png"),
      image2: require("@/assets/images/image_2.png"),
    };
  },
};
</script>

<style scoped lang="scss" src="@/styles/HomePage.scss"></style>
