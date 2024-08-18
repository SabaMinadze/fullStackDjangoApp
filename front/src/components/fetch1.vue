<script>
import card from '../components/card.vue'

export default {
  name: 'App',
  components: {
    card,
  },
  data() {
    return {
      box: [],
    };  
  },
  async mounted() {
    try {
      const response = await fetch('http://127.0.0.1:8000/api/dataBigBox/?format=json');
      this.box = await response.json();
    } catch (error) {
      console.error('Error fetching data:', error);
    }
  },
};
</script>

<template>
  <div>
    <div class="cards">
        <card v-for="(item, index) in box" :key="index" :nivti="item" class="card2"/>
    </div>
  </div>
</template>



<style scoped>
.cards{
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
} 


.card21 {
  flex: 0 0 calc(33.33% - 10px); /* 33.33% width minus spacing */
  margin-top: 20px;
}

</style>