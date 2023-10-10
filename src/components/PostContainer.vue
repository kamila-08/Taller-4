<template>
    <h1 class="linea1">
        La naturaleza
    </h1>
    <div class="post-container">
        <post-card
            v-for="post in posts" :key="post.title"
            :title="post.title"
            :summary="post.summary"
            :rutaImagen="post.image"
            
        />
        <EnlacesInteres :enlaces="enlacesDeInteres" />
        
    </div>

</template>

<script lang="ts">
import { defineComponent } from 'vue';
import PostCard from './PostCard.vue';
import datos from '@/assets/json/datos.json'
import EnlacesInteres from './EnlacesInteres.vue';

export default defineComponent({
    name:'PostContainer',
    components:{
        PostCard,
        EnlacesInteres
    },
    computed:{
        posts: ()=> {
        return datos.map((post:any)=>{
            return post
        })
    },
    enlacesDeInteres: () => {
    return [
    { text: 'Definición de naturaleza', url: 'https://concepto.de/naturaleza/' },
    { text: 'Importancia de la naturaleza', url: 'https://conceptoabc.com/naturaleza/' },
    { text: 'Caracteristicas de la naturaleza', url: 'https://www.significados.com/naturaleza/' },
    { text: 'Factores importantes de la naturaleza', url: 'https://www.fao.org/3/W1309S/w1309s09.htm#'}
  ];
},
    
}

})

</script>

<style lang="scss" scoped>
    .post-container {
        width: 65%;
        display:flex;
        justify-content: center;
        flex-wrap: wrap;
        border-radius: 10px;
        padding: 15px;
        margin: 10px;
        border: solid 10px blueviolet;
        min-width: 50%;
        margin-left: 18%;
        
    }
    .linea1 {
    text-align: center; 
    color: blueviolet; 
    font-size: 30px;
    margin-top: 20px; 
}
</style>
