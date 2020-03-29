<template>
  <div class="goods">
    <goods-list-item v-for="item in goods" :goods-item="item"></goods-list-item>
  </div>
</template>

<script>
  import GoodsListItem from './GoodsListItem'

  export default {
    name: "GoodsList",
    components: {
      GoodsListItem,
    },
    props: {
      goods: {
        type: Array,
        default() {
          return [];
        }
      }
    }
  }
</script>

<style scoped>
  .goods{
    display: flex;
    /* 当子组件设置一定宽度时按屏幕大小放入子组件 */
    flex-wrap: wrap;
    /* 均等分一行（中间缝隙均等，两侧没有均等分） */
    justify-content: space-around;
    padding: 2px;
  }

</style>
