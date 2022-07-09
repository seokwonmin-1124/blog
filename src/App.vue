<template>
<TransitionGroup name="vue">
    <div class="content">
        <p class="siteTitle">블로그 카테고리별 글 모아보기 기능 구현</p>
        <TheBtns />
        <TheCards />
    </div>
    <footer>
        <span>Made by&nbsp;</span>
        <a href="https://github.com/seokwonmin-1124">LESH</a>
        <span>&nbsp;design with&nbsp;</span>
        <a href="https://bulma.io/">Bulma</a>
        <span>, made with&nbsp;</span>
        <a href="https://vuejs.org">Vue.js</a>
    </footer>
</TransitionGroup>
</template>

<script>
import TheBtns from './components/TheBtns.vue';
import TheCards from './components/TheCards.vue';

export default {
    name: 'App',
    data() {
        
    },
    components: {
    TheBtns,
    TheCards
},
}
</script>

<style>
@import "https://cdn.jsdelivr.net/npm/bulma@0.9.4/css/bulma.min.css";

.vue-enter-active, .vue-leave-active {
    transition: all 0.2s ease-in-out;
}

.vue-enter, .vue-leave-active {
    opacity: 0;
}

.content {
    margin: 0 auto;
    padding: 1rem;
    max-width: 700px;
    padding-bottom: 30px;
}

.siteTitle {
    font-size: 2rem;
    font-weight: bold;
    margin: 20px;
}

.button {
    margin: 4px;
    width: auto;
}

.btns {
    display: flex;
    flex-direction: row;
    justify-content: center;
}

.box {
    margin: 10px;
    width: auto;
}

.title {
    font-size: 1.2rem;
    font-weight: bold;
}

.title:hover {
    cursor: pointer;
    text-decoration: underline;
}

.innerP {
    color: gray;
}

footer {
    display: flex;
    position: fixed;
    bottom: 0;
    width: 100vw;
    height: 50px;
    align-items: center;
    justify-content: center;
    background-color: #FAFAFA;
}
</style>
