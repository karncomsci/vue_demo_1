<template>
  <div id="demo5">
    <img v-bind:src="imageUrl" v-bind:height="height" />
    <br />
    <a v-bind:href="link">My website</a>
    <br />
    <a :href="link">My website</a>
    <div :class="[false ? error : '', important]">CodeMobiles</div>
    <div :style="{color, fontSize:fontSize }">Binding Style</div>
    <div :style="isActive ? styleObj : ''">Binding Style Obj</div>
    <button @click="isActive = !isActive">ToggleActive</button>
  </div>
</template>

<script>
export default {
  name: "Demo5",
  data() {
    return {
      imageUrl:
        "http://www.codemobiles.com/biz/images/codemobiles_logo.png?ref=10",
      height: 50,
      link: "http://codemobiles.com",
      error: "error_class",
      important: "important",
      color: "green",
      fontSize: "30px",
      styleObj: {
        backgroundColor:'yellow',
        color: 'green'
      },
      isActive:false
    };
  }
};
</script>

<style>
.error_class{
  background-color: red;
  color: white;
}

.important{
 font-weight: 900; 
}
</style>
