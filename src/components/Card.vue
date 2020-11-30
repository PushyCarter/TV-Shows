<template>
<div class="container">
    <div class="row row-cols-1 row-cols-md-4">
        <div v-for="show in showList" :key="show.name" class="col mb-4">
            <div class="card h-100">
                <img :src="'https://image.tmdb.org/t/p/w300//' + show.poster_path" class="card-img-top">
                <div class="card-body">
                    <h5 class="card-title">{{show.name}}</h5>
                    <p class="card-text">{{show.overview}}</p>
                </div>
            </div>
        </div>
    </div>
</div>
</template>

<script>
export default {
    name: "Card",
    props: ['showList']
}
</script>