<template>
  <div class="hello">
    <!-- <ares-header title="HelloWorld"></ares-header> -->
    <div class="title">这是一个rem demo</div>
    <div class="items">
      <div v-for="(item, $index) in 2" :key="$index" class="item">
        <div class="avatar">
          <img :src="require('../assets/' + (item%5 + 1) + '.png')">
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data() {
    return {
    };
  },
  methods: {
  },
};
</script>

<style scoped>
.title {
  font-size: 20px;
  text-align: center;
  margin: 20px 0;
  font-weight: bold;
}
.items {
  display: flex;
  & .item {
    flex: 1;
    display: flex;
    font-size: 16px;
    padding: 10px;
    & .avatar img {
      width: 130px;
    }
  }
}
</style>
