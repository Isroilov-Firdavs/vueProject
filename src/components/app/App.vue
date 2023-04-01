<template>
  <div class="app">
    <div class="content">
      <Appinfo :allMoviesCount="movies.length" :favouriteMoviesCount="movies.filter(c => c.favourite).length"/>
      <div class="search-panel">
        <SearchPanel/>
        <AppFilter/>
      </div>
      <MovieList :movies="movies" />
      <MovieAddForm />
    </div>
  </div>
</template>

<script>
  import Appinfo from '@/components/app-info/Appinfo.vue'
  import SearchPanel from '../search-panel/SearchPanel.vue'
  import AppFilter from '../app-filter/AppFilter.vue'
  import MovieList from '../movie-list/MovieList.vue'
  import MovieAddForm from '../movie-add-form/MovieAddForm.vue'
  export default{
    components: {
      Appinfo,
      SearchPanel,
      AppFilter,
      MovieList,
      MovieAddForm,
    },
    data() {
            return {
                movies: [
                    {
                        moviename: "Hello",
                        viewers: 122,
                        favourite: false,
                        like: true,
                    },
                    {
                        moviename: "Omar",
                        viewers: 800,
                        favourite: true,
                        like: true,
                    },
                    {
                        moviename: "Salom",
                        viewers: 500,
                        favourite: false,
                        like: false,
                    },
                    {
                        moviename: "Privet",
                        viewers: 600,
                        favourite: true,
                        like: true,
                    },
                ]
            }
        }
  }
</script>

<style>
.app{
  height: 100vh;
  color: #000;
}
.content{
  width: 1000px;
  min-height: 700px;
  background-color: #fff;
  margin: 0 auto;
  padding: 5rem 0;
}
.search-panel{
  margin-top: 2rem;
  padding: 1.2rem;
  background-color: #fcfaf5;
  border-radius: 5px;
  box-shadow: 15px 15px 35px rgba(0, 0, 0, 0.15);
}
</style>