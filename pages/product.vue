    <template> 
        <div class="container d-flex justify-content-center">
            <form class="w-50 my-5 ">
            <div class="input-group flex-nowrap w-100">
                <input type="text" class="form-control shadow-none" placeholder="Search" aria-label="Username"
                aria-describedby="addon-wrapping">
                <button type="submit" class="btn btn-success"><i class="bi bi-search"></i></button>
            </div>
            </form>
        </div>
        <div class="container">
            <div class="grid mb-5">
            <div class="content" v-for="product in Products" :key="product.id">
                <div class="item w-100 h-100 rounded-1" style="border: 0.1px solid black;">
                <div class="content p-3 " style="height: 90%;">
                    <img class="priceimg w-50" :src="product.image">
                    <h5 style="text-align: center; margin-top: 40px;"><a style="color: rgba(233, 60, 60, 0.805);">{{ product.price }}</a></h5>
                    <h6 class="text-center mt-3">{{ product.title }}</h6>
                    <button type="button" class="btn btn-info mt-5 text-white" @click="toggleVisible" >{{ isVisible? "less" : "More" }}</button>
                    <div v-show="isVisible">
                    <h5>Detail :</h5>
                    <p>{{ product.detail }}</p>
                    <p>Status of product : <a style="color: red;"> {{ product.status }}</a> </p>
                    </div>
                </div>
                </div>
            </div>
            </div>
        </div>   
  </template>
  
  <script>
  export default {
    data() {
      return {
        Products: [
          {
            id: "1",
            price:"$11.99",
            title: "Jetline Jetmaster Copper Lighter ",
            image: "https://lmcigars.com/wp-content/uploads/2022/02/jetmaster-090336-600x600.png",
            status: "No Longer Available",
            detail : 'The Jetline Jetmaster Copper Lighter is a single flame torch pocket lighter. It comes with a mega jet burner to give you a large and strong flame.'
          },
          {
            id: "2",
            title: "Otonari ni Ginga",
            image: "",
            studios: "Asahi Productio",
            synopsis : 'Ever since their father died, Ichiro Kuga has struggled to support his two younger siblings on nothing but a small inheritance and his passion.'
    
          },
          {
            id: "3",
            title: "Tonikaku Kawaii",
            image: "",
            studios: "Seven Arcs",
            synopsis : "Nasa Yuzaki is determined to leave his name in the history books. Ranking first in the national mock exam and aiming for a distinguished high school,"
          },
          {
            id: "4",
            title: "Shingeki no Kyojin: The Final Season",
            image: "",
            studios: "MAPPA",
            synopsis : "In the wake of Eren Yeager's cataclysmic actions, his friends and former enemies form an alliance against his genocidal rampage."
  
  
          },
  
        ],
        isVisible: false,
      }
    },
    methods:{
      toggleVisible() {
              this.isVisible = !this.isVisible
          }
    }
  
  }
  </script>
  
  <style scope>
  .grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    column-gap: 16px;
    row-gap: 30px;
  }
  
  .item:hover {
    box-shadow: -2px 5px 32px -11px rgba(0, 0, 0, 0.86);
  }
  
  .item {
    transition: 0.2s;
  }
  
  .priceimg {
    display: block;
    margin-left: auto;
    margin-right: auto;
    width: 50%;
  }
 </style>
