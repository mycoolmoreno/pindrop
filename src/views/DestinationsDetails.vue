<template>
    <div id="destinations">
        <TheNavigation />
        <GoBack />
        <!-- <TheDestinationsDetails /> -->

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

        <div class="container">
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
        </div>

        <!-- <section class="destination">
            <h1>{{destination.name}}</h1>
            <div class="destination-details">
                <img :src="destination.image" :alt="destination.name">
                <p>{{destination.description}}</p>
            </div>
        </section>
        <section class="experiences">
            <h2> Top neighborhoods in {{ destination.name }} </h2>
            <div class="cards">
                <div v-for="neighborhood in destination.neighborhoods"
                :key="neighborhood.slug"
                class="card">
                    <router-link
                    :to="{
                        name: 'neighborhoodDetails',
                        params: { neighborhoodSlug: neighborhood.slug}
                    }">
                    <img :src="neighborhood.image" :alt="neighborhood.name">
                    <span class="card_text">
                        {{neighborhood.name}}
                    </span>
                    </router-link>
                </div>
            </div>
            <router-view :key="$route.path" />
        </section> -->



    </div>

</template>
<script>
import store from '@/store.js'
import GoBack from '@/components/GoBack.vue'
import TheNavigation from '@/components/TheNavigation.vue'


export default {
    components: {
        TheNavigation,
        GoBack
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

#destinations{
    text-align: left !important;
}

img {
    max-width: 600px;
    height: auto;
    width: 100%;
    max-height: 400px;
}
.destination-details {
    display: flex;
    justify-content: space-between;
}
p {
    margin: 0 40px;
    font-size: 20px;
    text-align: left;
    margin-left: 0 !important;
    padding-left: 0 !important;
}

.cards {
    display: flex;
    justify-content: space-between;
}

.cards img {
    max-height: 200px;
}

.card {
    padding: 0 20px;
    position: relative;
}

.card_text {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    color: white;
    font-size: 25px;
    font-weight: bold;
    text-decoration: none;
}

</style>