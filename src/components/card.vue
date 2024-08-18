<script>
export default {
    props: {
        nivti: {
        reqired: true,
        type: Object,
        }
  },
    
}
</script>


<template>
    <div>
        <div class="card">
            <h1>{{ nivti.firstname }}</h1>
            <h1>{{ nivti.lastname }}</h1>
            <h1>{{ nivti.age }} years old</h1>
        </div>
    </div>
</template>



<style scoped>
.card{
    height: 200px;
    width: 400px;
    background-color: chartreuse;
}

h1{
    text-align: center;
}

</style>