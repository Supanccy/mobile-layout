<template>
  <div class="hello">
    <!-- <ares-header title="HelloWorld"></ares-header> -->
    <!-- <div class="title">这是一个viewport demo</div> -->
    <div class="items">
      <div v-for="(item, $index) in 10" :key="$index" class="item">
        <div class="avatar">
          <img :src="require('../assets/' + (item%5 + 1) + '.png')">
        </div>
        <div class="info">
          <div class="subject">这是一个标题{{item}}</div>
          <div class="detail">这是详细内容这是这是详细内容这是</div>
          <div class="three">disan</div>
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
  /*display: flex;*/
  & .item {
    /*flex: 1;*/
    display: flex;
    font-size: 16px;
    padding: 10px;
    & .avatar img {
      width: 130px;
      /*height: 50px;*/
    }
    & .info {
      text-align: left;
      padding: 3px 10px;
      & .subject {
        color: #000;
        font-size: 16px;
      }
      & .detail {
        margin-top: 10px;
        color: #999;
        font-size: 14px;
      }
      & .three {
        color: #a0a0a0;
        font-size: 12px;
      }
    }
  }  
}
</style>
