<template>
    <div class='ItemRoot'  >
        <div class='Subtitle'>{{item.subtitle}}</div>
        <div class='Content' :class='{Reverse: item.reverse}'>      
            <div class='Text'>{{item.text}}</div>
            <img alt="Vue logo" :src='item.imgURL'>
        </div>
    </div>
</template>

<script>
export default {
  name: 'Item',
  props: {
    item: {
        subtitle: String,
        imgURL: String,
        text: String,
        reverse: Boolean
        }
    } 
}
</script>
<style scoped>
    .ItemRoot {
        display: flex;
        flex-flow: column nowrap;
        width: 100%;
    }
    .Content {
        display: flex;
        flex-flow: row nowrap;
    }
    .Reverse {
        flex-flow: row-reverse
    }
    .Subtitle {
        font-weight: bold;
    }
    img {
        height: 20vh;
        width: 20vh;
        margin: 0 10px;
    }

</style>