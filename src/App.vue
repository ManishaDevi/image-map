<template>
  <div>
    <h1>{{selected}}</h1>
    <img
      src="https://images-na.ssl-images-amazon.com/images/I/6101KS%2B3xWL._UX679_.jpg"
      width="679"
      height="679"
      usemap="#tShirt"
    >
    <map name="tShirt">
      <!-- Used https://www.image-map.net to generate the coordinates -->
      <area @mouseover="showMessage('Democrat')" coords="258, 180, 436, 215" shape="rect">
      <area @mouseover="showMessage('Republican')" coords="258, 244, 449, 283" shape="rect">
      <area @mouseover="showMessage('Gladiator')" coords="428, 351, 257, 312" shape="rect">
      <area @mouseover="showMessage('Checkbox Democrat')" coords="238, 192, 21" shape="circle">
      <area
        @mouseover="showMessage('Checkbox Republican')"
        coords="224, 244, 223, 278, 253, 282, 252, 244"
        shape="poly"
      >
      <area
        @mouseover="showMessage('Checkbox NO Gladiator')"
        coords="219, 314, 262, 349"
        shape="rect"
      >
      <area
        @mouseover="showMessage('Scandal')"
        coords="256, 353, 319, 393, 448, 396, 465, 347"
        shape="poly"
      >
    </map>
  </div>
</template>

<script>
export default {
  name: "App",
  data: function() {
    return {
      selected: "Hover on different text on t-shirt"
    };
  },
  methods: {
    showMessage: function(message) {
      this.selected = message;
    }
  }
};
</script>

<style scoped>
h1 {
  position: fixed;
  background-color: rgb(255, 255, 255, 0.5);
}
</style>