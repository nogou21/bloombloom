<script lang="ts">
import { defineComponent } from 'vue';


export default defineComponent({

    data(){
        return{
            
        }
    }
})

</script>
<template>
    <div class="drawer">
        <ul>
            <li>SPECTACLES</li>
            <li>SUNGLASSES</li>
            <li>HOME TRY ON</li>
            <li>PAIR FOR PAIR</li>
        </ul>
    </div>
</template>

<style scoped>
.drawer{
    height: 90vh;
    z-index: 1;
    border-right: solid 0.1rem black;
}
ul{
    list-style: none;
    width: inherit;
}
li{
    padding-top: 2rem;
    padding-bottom: 2rem;
    cursor: pointer;
    /* border-bottom: solid 0.1rem black; */
}
</style>