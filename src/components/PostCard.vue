<template>
    <div class="post-card">
        <h1 class="post-title">{{ title }}</h1>
        <p class="post-summary">{{ summary }}
           {{ summary }}
        </p>

        <img :src="require(`@/assets/img/${rutaImagen}`)" alt="">
    </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

import PostImage from './PostImage.vue';

export default defineComponent ({
    name:'PostCard',
    components:{
        PostImage
    },
    props:{
        title:{
            type:String,
            default:""
        },
        summary:{
            type:String,
            default:""
        },
        text:{
            type: String,
            default:""
        },
        rutaImagen:{
            type:String,
            default:""
        }
    }
})
</script>
0
<style lang="scss" scoped>
    .post-card{
        border-radius: 10px;
        padding: 15px;
        margin: 10px;
        border: solid 10px blueviolet;
        min-width: 50%;
        margin-left: 2%;
    }
    .post-title{
        font-size: 24px; 
        color: brown; 
        text-align: center;

    }
    .post-summary{
        font-size: 24px; 
        color: palevioletred;
        text-align: center;

    }
    img{
        width: 700px;
        height: 300px;
        text-align:center;
        margin-left: 5%;
        

    }
    
</style>
