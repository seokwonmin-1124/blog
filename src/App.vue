<template>
<TransitionGroup name="vue">
    <div class="content">
        <p class="siteTitle">블로그 카테고리별 글 모아보기 기능 구현</p>
        <TheBtns />
        <TheCards />
    </div>
    <footer>
        <span>Made by <a href="https://github.com/seokwonmin-1124">LESH</a> with <a href="https://bulma.io/">Bulma</a></span>
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
@import url('https://fonts.googleapis.com/css2?family=Noto+Sans+KR&display=swap');

* {
    font-family: 'Noto Sans KR', sans-serif;
}

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

.tag {
    font-size: 0.8rem;
    font-weight: bold;
    margin-left: 10px;
}

.innerP {
    color: gray;
    overflow: hidden;
    text-overflow: ellipsis;
    white-space: normal;
    width: 608px;
    line-height: 1.2;
    height: 3.7em;
    word-wrap: break-word;
    display: -webkit-box;
    -webkit-line-clamp: 3;
    -webkit-box-orient: vertical;
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
