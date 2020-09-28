<template>
  <section class="hero">
    <div class="container fade-in" v-show="currentSlide === 0">
      <h1>Welcome to Divi Theatre</h1>
      <p>
        Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod.
      </p>
      <button class="btn-fill" href="#now-featuring-section">
        <svg
          xmlns="http://www.w3.org/2000/svg"
          width="24"
          height="24"
          viewBox="0 0 24 24"
          fill="none"
          stroke="currentColor"
          stroke-width="2"
          stroke-linecap="round"
          stroke-linejoin="round"
          class="feather feather-film"
        >
          <rect x="2" y="2" width="20" height="20" rx="2.18" ry="2.18"></rect>
          <line x1="7" y1="2" x2="7" y2="22"></line>
          <line x1="17" y1="2" x2="17" y2="22"></line>
          <line x1="2" y1="12" x2="22" y2="12"></line>
          <line x1="2" y1="7" x2="7" y2="7"></line>
          <line x1="2" y1="17" x2="7" y2="17"></line>
          <line x1="17" y1="17" x2="22" y2="17"></line>
          <line x1="17" y1="7" x2="22" y2="7"></line></svg
        >Showtimes
      </button>
    </div>
    <div class="container fade-in" v-show="currentSlide === 1">
      <h1>Samuel L. Jackson Mutha</h1>
      <p>
        Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod.
      </p>
      <button class="btn-fill">
        <svg
          xmlns="http://www.w3.org/2000/svg"
          width="24"
          height="24"
          viewBox="0 0 24 24"
          fill="none"
          stroke="currentColor"
          stroke-width="2"
          stroke-linecap="round"
          stroke-linejoin="round"
          class="feather feather-film"
        >
          <rect x="2" y="2" width="20" height="20" rx="2.18" ry="2.18"></rect>
          <line x1="7" y1="2" x2="7" y2="22"></line>
          <line x1="17" y1="2" x2="17" y2="22"></line>
          <line x1="2" y1="12" x2="22" y2="12"></line>
          <line x1="2" y1="7" x2="7" y2="7"></line>
          <line x1="2" y1="17" x2="7" y2="17"></line>
          <line x1="17" y1="17" x2="22" y2="17"></line>
          <line x1="17" y1="7" x2="22" y2="7"></line></svg
        >Even More
      </button>
    </div>
    <div class="container fade-in" v-show="currentSlide === 2">
      <h1>Final Slide... or is it</h1>
      <p>
        Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod.
      </p>
      <button class="btn-fill">
        <svg
          xmlns="http://www.w3.org/2000/svg"
          width="24"
          height="24"
          viewBox="0 0 24 24"
          fill="none"
          stroke="currentColor"
          stroke-width="2"
          stroke-linecap="round"
          stroke-linejoin="round"
          class="feather feather-film"
        >
          <rect x="2" y="2" width="20" height="20" rx="2.18" ry="2.18"></rect>
          <line x1="7" y1="2" x2="7" y2="22"></line>
          <line x1="17" y1="2" x2="17" y2="22"></line>
          <line x1="2" y1="12" x2="22" y2="12"></line>
          <line x1="2" y1="7" x2="7" y2="7"></line>
          <line x1="2" y1="17" x2="7" y2="17"></line>
          <line x1="17" y1="17" x2="22" y2="17"></line>
          <line x1="17" y1="7" x2="22" y2="7"></line></svg
        >Other Title
      </button>
    </div>
    <div class="selector-container">
      <div
        class="selector"
        :class="{ 'full-opacity': currentSlide === 0 }"
        @click="changeSlide(0)"
      ></div>
      <div
        class="selector"
        :class="{ 'full-opacity': currentSlide === 1 }"
        @click="changeSlide(1)"
      ></div>
      <div
        class="selector"
        :class="{ 'full-opacity': currentSlide === 2 }"
        @click="changeSlide(2)"
      ></div>
    </div>
  </section>
</template>

<script>
export default {
  name: "Hero",
  data() {
    return {
      currentSlide: 0,
    };
  },
  methods: {
    changeSlide(slide) {
      this.currentSlide = slide;
    },
  },
};
</script>

<style lang="scss" scoped>
.hero {
  width: 100%;
  height: 100vh;
  background-image: linear-gradient(rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 1)),
    url("../assets/streetlights.jpg");
  background-size: cover;
  padding-top: 200px;
}

p {
  font-size: 1.5rem;
  font-weight: 300;
  letter-spacing: 0.01rem;
  margin: 16px 0 48px 0;
}

.selector-container {
  margin: 0 auto;
  padding: 4px;
  display: flex;
  align-items: center;
  justify-content: center;
  position: relative;
  margin-top: 200px;
}

.selector {
  width: 10px;
  height: 10px;
  border-radius: 50%;
  background: #fff;
  opacity: 0.5;
  margin: 8px;
  cursor: pointer;
}

.full-opacity {
  opacity: 1;
}
</style>