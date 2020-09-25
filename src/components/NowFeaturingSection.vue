<template>
  <section id="now-featuring-section">
    <div class="container">
      <h4>Featured</h4>
      <h2><strong>Now</strong> Showing</h2>
    </div>
    <div class="flex">
      <div class="movie-card" v-for="movie in movies" :key="movie.id">
        <img :src="movie.image" class="movie-img" />
        <p class="movie-title">{{ movie.title }}</p>
        <p class="movie-description">
          {{ movie.duration }} | {{ movie.rating }}
        </p>
        <p class="movie-description">{{ movie.releaseDate }}</p>
        <br />
        <button class="btn-small">Get Tickets</button>
      </div>
      <div>
        <p class="extra">More...</p>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "NowFeaturingSection",
  data() {
    return {
      movies: [
        {
          id: "001",
          title: "Lights Out",
          duration: "1hr 35min",
          rating: "PG",
          releaseDate: "Aug. 12, 2019",
          image: "https://picsum.photos/300/400",
        },
        {
          id: "002",
          title: "Headlight",
          duration: "1hr 5min",
          rating: "R",
          releaseDate: "Sept. 17, 2020",
          image: "https://picsum.photos/300/400",
        },
        {
          id: "003",
          title: "Cabin",
          duration: "2hr 15min",
          rating: "PG-13",
          releaseDate: "Nov. 23, 2019",
          image: "https://picsum.photos/300/400",
        },
        {
          id: "004",
          title: "Bridge",
          duration: "1hr 45min",
          rating: "PG",
          releaseDate: "Dec. 14, 2020",
          image: "https://picsum.photos/300/400",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
.movie-card {
  margin: 60px 0;
  max-width: 250px;
}

.movie-img {
  width: 100%;
}

.movie-title {
  font-family: "Montserrat", sans-serif;
  font-weight: 600;
  margin-top: 16px;
}
</style>