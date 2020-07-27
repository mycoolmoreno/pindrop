<template>
    <span class="go-back">
        <div class="container">
           <button @click="goBack">Go Back</button> 
        </div>
    </span>
</template>

<script>
export default {
    methods: {
        goBack(){
            return this.$router.go(-1);
        }
    }
};
</script>

<style scoped>
.go-back {
    display: flex;
    cursor: pointer;
    text-align: left;
    background-color: #e9ecef;
}
button {
    border: 0;
    background-color: #e9ecef;
    margin-top: 10px;
}
</style>