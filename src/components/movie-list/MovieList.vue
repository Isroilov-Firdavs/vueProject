<template>
    <ul class="list-group movi-list">
        <MovieListItem v-for="movie in movies" v-bind:movie="movie" />
    </ul>
</template>

<script>
    import MovieListItem from '../movi-list-item/MoviListItem.vue'
    export default {
        components: {
            MovieListItem,
        },
        props: {
            movies: {
                type: Array,
                required:true,
            }
        }
    }
</script>

<style scoped>
    .movi-list{
        margin-top: 2rem;
        padding: 1.2rem;
        background-color: #fcfaf5;
        border-radius: 5px;
        box-shadow: 15px 15px 35px rgba(0, 0, 0, 0.15);
    }
</style>