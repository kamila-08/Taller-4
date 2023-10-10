<template>
    <div class="post-image">

    </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
export default defineComponent({
    props: {
        ruta: {
            type:String,
            default:""
        }
    }

})
</script>

<style lang="scss" scoped>
.post-image{
    display: flex;
    justify-content: center;
    img {
        width: 20px;
        height: 50px;

    }
}
</style>
