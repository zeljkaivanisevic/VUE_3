<template>
  <div class="row">
    <div class="col-8">


       
      <InstagramCard :key="card" :info="card" v-for="card in filteredCards"  />
      

    </div>
    <div class="col-4">
      Trazimo sljedece: {{searchTerm}}
    </div>
  </div>
</template>

<script>
import InstagramCard from '@/components/InstagramCard.vue'
import store from '@/store.js'

export default {
data(){
return store ;  
  
},

computed:{
  filteredCards() {
    return this.cards.filter(card => card.title.includes(this.searchTerm) ||  card.autor.includes(this.searchTerm));
   
  }

},

  name: 'home',
  components: {
    InstagramCard
  }
}
</script>

<style lang="scss">

.card-body {
  padding: 0px;
}


img:hover{
  cursor: pointer;
}


</style>