<template>
<div>
<div class=" bg-white-600 flex items-center justify-center "> 
<p class="underline ...">Galeria de Gifs</p>
</div>

<div class="min-h-screen bg-purple-300 flex items-center justify-center"
    id="inicio"
>
    
  
    <div class="inline-grid grid-cols-3 gap-x-4">
    
      <div v-for="gif in gifs1" v-if="gifs1" >
        <img :src="gif.image_original_url" />
      </div>    
      <div v-for="gif in gifs2" v-if="gifs1">
        <img :src="gif.image_original_url" />
      </div>   
       <div v-for="gif in gifs3" v-if="gifs1"> 
        <img :src="gif.image_original_url" />
      </div>       
       <div v-for="gif in gifs4" v-if="gifs1"> 
        <img :src="gif.image_original_url" />
      </div>   
       <div v-for="gif in gifs5" v-if="gifs1"> 
        <img :src="gif.image_original_url" />
      </div>   
       <div v-for="gif in gifs6" v-if="gifs1">
        <img :src="gif.image_original_url" />
      </div>   
 
    </div>
 
</div>
</div>
</template>

<script>
// class="min-h-screen bg-purple-300 flex items-center justify-center"
import axios from "axios";
export default {
  name: "inicio",
  data() {
    return {
      apiurl: "https://api.giphy.com/v1/gifs/random?api_key=LqIeL80SL0Dwww8KaIc1P5uqXyfxIPVr&tag=&rating=g",
      gifs1: null,
      gifs2: null,
      gifs3: null,
      gifs4: null,
      gifs5: null,
      gifs6: null,
      
    };
  },
  mounted() {
    const url = `${this.apiurl}`;
    axios.get(url).then((response) => ((this.gifs1 = response.data), console.log(response.data)));
    axios.get(url).then((response) => ((this.gifs2 = response.data), console.log(response.data)));
    axios.get(url).then((response) => ((this.gifs3 = response.data), console.log(response.data)));
    axios.get(url).then((response) => ((this.gifs4 = response.data), console.log(response.data)));
    axios.get(url).then((response) => ((this.gifs5 = response.data), console.log(response.data)));
    axios.get(url).then((response) => ((this.gifs6 = response.data), console.log(response.data)));




  },
};
</script>

<style>
.btn-indigo {
  @apply py-2 px-4 bg-indigo-500 text-white font-semibold rounded-lg shadow-md hover:bg-indigo-700 focus:outline-none focus:ring-2 focus:ring-indigo-400 focus:ring-opacity-75;
}
</style>
