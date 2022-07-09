<template>
    <div v-for="(item, index) in categories" v-show="show[index]" :key="index">
        <div class="box">
            <p class="title">{{ item }}</p>
            <p class="innerP">{{ msg[index] }}</p>
        </div>
    </div>
</template>

<script>
import data from './data'

    export default {
        name: 'TheCards',
        data() {
            return {
                categories: data.categories,
                show : data.show,
                msg : data.msg
            }
        },
    }
</script>

<style lang="scss" scoped>

</style>