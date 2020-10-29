<template>
  <div id="app">
    <div class="box1" v-on:click.right="openOnRightClick">click on me by right button!</div>
    <div class="box2" v-if="show" v-on:click.right="openOnRightClick">You clicked, right?</div>
  </div>
</template>

<script>


export default {
  name: 'App',
  data() {
    return {
      show: false
    }
  },
  methods: {
    openOnRightClick(e) {
      e.preventDefault();
      this.show = !this.show
    }
  }
}
</script>

<style>
.box1 {
  height: 50px;
  width: 150px;
  background-color: greenyellow;
  display: table-cell;
  text-align: center;
}

.box2 {
  height: 50px;
  width: 150px;
  background-color: indianred;
  display: table-cell;
  text-align: center;
}
</style>
