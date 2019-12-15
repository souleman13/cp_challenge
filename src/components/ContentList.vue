<template>
    <div class='ContentListRoot'>
        <div class='Title' >{{ title }}</div>
        <div class='List' v-for='item in content' :key='item.subtitle'>
            <Item :item='item' />
        </div>
    </div>
</template>

<script>
import Item from './Item'
export default {
  name: 'ContentList',
  props: {
    title: String,
    content: Array
  },
  components: {
      Item
  }
}
</script>
<style scoped>
    .ContentListRoot {
        display: flex;
        flex-flow: column;
        align-items: center;
    }
    .Title {
        font-weight: bold;
        font-size: 20px;
    }

</style>