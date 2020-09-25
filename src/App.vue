<template>
  <div id="app">
    <Hero />
    <CTASection />
    <NowFeaturingSection />
  </div>
</template>

<script>
import Hero from "./components/Hero";
import CTASection from "./components/CTASection";
import NowFeaturingSection from "./components/NowFeaturingSection";

export default {
  name: "App",
  components: {
    Hero,
    CTASection,
    NowFeaturingSection,
  },
};
</script>

<style lang="scss">
@import url("https://fonts.googleapis.com/css2?family=Montserrat:wght@400;600;800&display=swap");

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;

  &:focus {
    outline: none;
  }
}

body {
  font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Oxygen,
    Ubuntu, Cantarell, "Open Sans", "Helvetica Neue", sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  background: #000;
  color: #fff;
}

h1,
h2,
h3 {
  font-family: "Montserrat", Roboto, Oxygen, Ubuntu, Cantarell, "Open Sans",
    "Helvetica Neue", sans-serif;
  font-weight: 600;
}

h1 {
  font-size: 7rem;
  font-weight: 800;
  letter-spacing: 1px;
  text-transform: uppercase;
}

h2 {
  font-size: 5rem;
  font-weight: 400;
}

h4 {
  color: #f71a2c;
  text-transform: uppercase;
  letter-spacing: 3px;
}

section {
  padding: 90px 140px;
  width: 100%;
}

button {
  padding: 16px 32px;
  border: 1px solid #f71a2c;
  border-radius: 4px;
  background: transparent;
  color: #fff;
  text-transform: uppercase;
  letter-spacing: 1.5px;
  font-size: 1.025rem;
  font-weight: 550;
  cursor: pointer;
  transition: all 200ms ease-in-out;

  &:hover {
    background: #f71a2c;
  }

  &:active {
    transform: translateY(1px);
  }
}

.btn-fill {
  background: #f71a2c;
  display: flex;
  align-items: center;
  justify-content: space-between;

  &:hover {
    box-shadow: 0 0 15px #f71a2c8f;
  }

  svg {
    margin-right: 8px;
  }
}

.btn-small {
  padding: 8px 16px;
}

.container {
  width: 100%;
  max-width: 1160px;
  margin: 0 auto;
}

.flex {
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  justify-content: space-between;
}

// Animations
.fade-in {
  animation: fadeIn 0.7s linear;
}

@keyframes fadeIn {
  from {
    opacity: 0;
  }

  to {
    opacity: 1;
  }
}
</style>
