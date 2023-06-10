<!-- 
    하위에 공통된 layout을 넣을때 사용한다.
 -->
<header class="layout-header"> 헤더 영역</header>
<slot />
<footer class="layout-footer">푸터 영역</footer>

<style>
    .layout-header {
        background-color: #000000;
        color: #ffffff;
        font-size: 30px;
        text-align: center;
        padding: 10px;
    }

    .layout-footer {
        background-color: #000000;
        color: #ffffff;
        font-size: 30px;
        text-align: center;
        padding: 10px;
    }
</style>
<!-- 슬롯은 구멍
값이 대입됨 
다른 dir밑에 있는 page.svelte에 있는 content가 <slot/> 부분에 삽입된다.Layout
그러므로 slot이라는 테그는 항상 필요하다.
-->