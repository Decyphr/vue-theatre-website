<template>
  <section id="now-featuring-section">
    <div class="container">
      <h4>Featured</h4>
      <h2><strong>Now</strong> Showing</h2>
    </div>
    <div class="featured-movies" style="justif-content: space-around">
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
      <div class="extra">
        <p>More...</p>
        <button class="btn-small btn-grey">See All Movies</button>
        <button class="btn-small btn-grey">Coming Soon</button>
        <input
          type="text"
          class="featured-search"
          v:model="featureSearchInput"
          placeholder="Search..."
        />
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "NowFeaturingSection",
  data() {
    return {
      featureSearchInput: "",
      movies: [
        {
          id: "001",
          title: "Lights Out",
          duration: "1hr 35min",
          rating: "PG",
          releaseDate: "Aug. 12, 2019",
          image: "https://picsum.photos/250/400",
        },
        {
          id: "002",
          title: "Headlight",
          duration: "1hr 5min",
          rating: "R",
          releaseDate: "Sept. 17, 2020",
          image: "https://picsum.photos/250/400",
        },
        {
          id: "003",
          title: "Cabin",
          duration: "2hr 15min",
          rating: "PG-13",
          releaseDate: "Nov. 23, 2019",
          image: "https://picsum.photos/250/400",
        },
        {
          id: "004",
          title: "Bridge",
          duration: "1hr 45min",
          rating: "PG",
          releaseDate: "Dec. 14, 2020",
          image: "https://picsum.photos/250/400",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
.featured-movies {
  display: grid;
  grid-template-columns: repeat(5, 1fr);
  grid-gap: 30px;
  padding: 60px;
}

.movie-card {
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

.extra {
  font-size: 1.25rem;
  font-weight: bold;
}

.extra button,
.extra input {
  margin-top: 16px;
}

.featured-search {
  width: 100%;
  color: #fff;
  padding: 8px;
  border: 1px solid #1f1f1f;
  border-radius: 2px;
  background: none;
  text-transform: uppercase;
  font-family: inherit;
  font-size: 0.7rem;
  font-weight: 700;
  letter-spacing: 1.5px;
  transition: 0.2s;

  &:hover,
  &:focus {
    border: 1px solid #f3f3f3;
  }
}
</style>