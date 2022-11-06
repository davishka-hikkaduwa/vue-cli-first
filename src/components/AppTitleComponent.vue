<template>
  <div>
    <div class="red" @click="saluta">
        My First Component
        <div class="inner">Sono Inner</div>
    </div>
    <input class="red active" type="text" v-model="text">
    <div class="inner">Inner Fuori da Red</div>
    <div class="red-square"></div>
  </div>
</template>

<script>
export default {
    name: 'AppTitleComponent',
    data() {
        return {
            text: '',
        };
    },
    methods: {
        saluta() {
            console.log("Hello from your first component");
        },
    },
}
</script>

<style scoped lang="scss">
$bgColor: red;


@mixin ac-square {
    width: 150px;
    height: 150px;
}

.red-square{
    @include ac-square();
    background-color: brown;
}

.red {
    background-color: red;
}

.red .inner{
    background-color: yellowgreen;
}

.red.active{
    background-color: blue;
}

.inner{
     background-color: yellow;
}
</style>