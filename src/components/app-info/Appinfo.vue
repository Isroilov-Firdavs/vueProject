<template>
    <div class="app-info">
        <p class="fs-3 text-uppercase">Barcha kinolar soni: {{ allMoviesCount }}</p>
        <p class="fs-4 text-uppercase">Ko'rilgan kinolar soni: {{favouriteMoviesCount}}</p>
    </div>
</template>

<script>
    export default {
        props: {
            allMoviesCount: {
                type: Number,
                required: true,
            },
            favouriteMoviesCount: {
                type: Number,
                required: true
            }
        }
    }
</script>


<style>
    .app-info{
        margin-top: 2rem;
        padding: 1.2rem;
        background-color: #fcfaf5;
        border-radius: 5px;
        box-shadow: 15px 15px 35px rgba(0, 0, 0, 0.15);
    }
</style>