<template>
  <div id="random-items">
    <li v-for="(item,i) in items" v-bind:key="i">
      <p>{{item.item}}</p>
      <p>{{item.cost}}</p>
      <img :src="item.thumbnail" alt="Cant load" />
    </li>
  </div>
</template>

<script>
export default {
  data() {
    return {
      items: [1, 2, 3]
    };
  },

  created() {
    const authStr = "Bearer envatoproduct-b4w5kgaw";
    this.$http
      .get("http://192.168.0.200:3000/data")
      .then(res => {
        console.log("res", res.data);
        this.items = res.data;
      })
      .catch(err => {
        console.log("err", err);
      });
  }
};
</script>

<style scoped>

#random-items{
  align-content: center
}

#random-items li {
  background: beige;
  max-width: 500px;
  margin: 5px;
  padding: 5px;
  list-style: none;
}
</style>