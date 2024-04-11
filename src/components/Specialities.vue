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
        return new URL(`../assets/svg/${img}`, import.meta.url).href
      },
  },
 
}
</script>

 <template>
  <div class="container text-center specialities">
    <h2 class="title">Our specialities</h2>
    <p>Lorem ipsum dolor sit amet.</p>
    <div class="line"></div>
    <div class="d-flex flex-wrap justify-content-center ps-5 pe-5">
      <SpecialCards v-for="card in data.specialities" :key="card.id"
      :img="getPathImage(card.img)"
      :title="card.title"
      :description="card.description"
      /> 

    </div>
  </div>
</template> 

<style lang="scss" scoped>
@use '../assets/scss/partials/variables' as * ;
.specialities{
  background: white;
  padding: 100px 0 80px 0;
  z-index: 999;
  margin-top:-40px;
    h2::after{
      content: '.';
      color: $main-orange;
    }
    .line{
      border-bottom: 2px solid $main-orange;
      width: 50px;
      margin: 0 auto;
      margin-bottom: 30px;      
    }

}
</style>