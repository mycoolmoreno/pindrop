<template>
    <div id="city-pages">
        <h1>{{destination.name}}</h1>
        <div class="jumbotron">
            <div class="container">
            <h1 class="display-4"> {{destination.name}} </h1>
            <p class="lead">{{ destination.description}}</p>
            <hr class="my-4">
            <h4>Known for:</h4>
            <ul class="list-group list-group-flush">
                <li class="list-group-item">Something</li>
                <li class="list-group-item">Something</li>
                <li class="list-group-item">Something</li>
            </ul>
            </div>
        </div>

        <!-- <div class="container">
        <h2> Explore some neighborhoods: </h2>
        <div class="row row-cols-1 row-cols-md-2">
        <div v-for="neighborhood in destination.neighborhoods"
                :key="neighborhood.slug" class="col mb-4">
            <div class="card">
            <img :src="neighborhood.image" class="card-img-top" alt="...">
            <div class="card-body">
                <h5 class="card-title">{{neighborhood.name}}</h5>
                <p class="card-text">{{neighborhood.description}}</p>
                <a href="#" class="btn btn-primary" target="_blank">Explore Listings</a>
            </div>
            </div>
        </div>
        </div>
        </div> -->


    </div>
</template>

<script>
import store from '@/store.js'

export default {
    components: {
    },
    data(){
        return {}
    },
    props: {
        slug: {
            type: String, 
            required: true 
        }
    },
    computed: {
        destination(){
            return store.destinations.find(
                destination => destination.slug === this.slug
            )
        }
    }
}

</script>


<style scoped>

</style>