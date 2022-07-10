<template>
    <div class="btns">
        <button class="button is-small" @click="allSee()">전체 항목 보기</button>
        <span v-for="(category, i) in categories" :key="i">
            <button class="button is-small" @click="changeDisplay(i)">{{ category }}</button>
        </span>
    </div>
</template>

<script>
import data from './json/data.js';

    export default {
        data() {
            return {
                categories: data.categories,
                show : data.show
            };
        },
        methods: {
            changeDisplay(index) {
                for (let i = 0; i < this.show.length; i++) {
                    this.show[i] = true;
                    if (this.show[index]) {
                        // this.show[index]를 제외한 모든 배열의 값을 false로 변경
                        this.show.forEach((item, i) => {
                            if (i !== index) {
                                this.show[i] = false;
                            }
                        });
                    }
                    else {
                        // this.show[index]를 제외한 모든 배열의 값을 true로 변경
                        this.show.forEach((item, i) => {
                            if (i !== index) {
                                this.show[i] = true;
                            }
                        });
                    }
                }
            },
            allSee() {
                for (let i = 0; i < this.show.length; i++) {
                    this.show[i] = true;
                }
            }
        }
    }
</script>

<style>

</style>