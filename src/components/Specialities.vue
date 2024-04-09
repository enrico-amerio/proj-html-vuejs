<script>
import {store} from '../data/store'
import SpecialCards from './partials/SpecialCards.vue'
import data from '../assets/db.json'


export default {
  data(){
    return{
      store,
      data 

    }
  },
  components:{
    SpecialCards
  },
  methods:{
    getPathImage(img){
        return new URL(`../assets/img/${img}`, import.meta.url).href
      },
  },
  mounted(){
    console.log(data.specialities);
  }
}
</script>

 <template>
  <div class="container">
    <h2 class="title">Our specialities</h2>
    <p>Lorem ipsum dolor sit amet.</p>
    <div class="line"></div>
    <SpecialCards v-for="card in data.specialities" :key="card.id"
    :img="getPathImage(card.img)"
    :title="card.title"
    :description="card.description"
    /> 
  </div>
</template> 

<style lang="scss" scoped>

</style>