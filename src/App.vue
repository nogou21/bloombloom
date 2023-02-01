<script lang="ts">
import { defineComponent } from 'vue';
import productCard from './components/product_view.vue';
import menuDrawer from './components/menu_drawer.vue';

export default defineComponent({
  data(){
    return{
      visible: false

    }
  },
  components:{
    productCard,
    menuDrawer
  },
  methods:{
    mouseover: function(){
       this.visible = true
    },
    mouseleave: function(){
      this.visible = false
    }
  }
})
</script>

<template>
    <div class="menu-box">
      <span id="menu" v-on:mouseover="mouseover">Menu</span>
    </div>
    <div class="collections-box">
      <div class="blank"></div>
      <div class="title-box">
        <span class="collection-title">Collection Title</span>
      </div>
      <div class="filters"></div>
    </div>
    <div class="products_box">
      <productCard/>
    </div>
    <menuDrawer  v-on:mouseleave="mouseleave" class="toggle-drawer" :class = "{ 'show-menu': visible}"/>
</template>

<style scoped>
.root-window{
  margin: 0 auto;
}
.menu-box{
  height: 3rem;
  display: block;
  border-top: 0.1rem solid black;
  border-bottom: 0.1rem solid black;
  
}
#menu{
  width: 5rem;
  color: black;
  display: block;
  padding-left: 4rem;
  line-height: 3rem;
  cursor: pointer;
}
#menu:hover{
  text-decoration: underline;
  text-underline-offset: 0.25rem;
  text-decoration-thickness: 0.15rem
}
.collections-box{
  height: 3rem;
  border-bottom: 0.1rem solid black;
  display: flex;
  flex-direction: row;
}
.blank{
  height: inherit;
  width: 33%;
  border-right: 0.1rem solid black;
}
.title-box{
  height: inherit;
  width: 33.66%;
  border-right: 0.1rem solid black;
  text-align: center;
}
.collection-title{
  font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
  font-weight: 800;
  line-height: 3rem;
}
.toggle-drawer{
  opacity: 0;
  width: 0vw;
  position: absolute;
  top: 3.8rem;
  transition: all .75s ease;
  background-color: white;
}
.show-menu{
  opacity: 1;
  width: 33vw;
}
</style>
