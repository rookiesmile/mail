<template>
  <div class="goods-list">
      <goods-list-item v-for="item in goods" :goodsItem="item" :key="item.title"/>
  </div>
</template>

<script>
import GoodsListItem from './GoodsListItem'
export default {
    name: 'GoodsList',
    props: {
        goods: {
            type: Array,
            default() {
                return []
            }
        }
    },
    components: {
        GoodsListItem
    }
}
</script>

<style>
  .goods-list {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-around;
    background-color: var(--color-background);

    padding: 2px;
  }
</style>