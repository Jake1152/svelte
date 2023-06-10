<script>
    import { page } from '$app/stores';
    // const { productId, reviewId } = $page.params.slug;
    // console.log($page.params.slug)
    // 어떤 경로로 해서 들어왔는지 다 알려준다.

    const slugArr = $page.params.slug.split('/');
    console.log($page.params)
    // params안에는 lang이 있다.
    const { lang } = $page.params;
</script>

{#if lang === 'ko'}
     <!-- content here -->
     <h1> 안녕 </h1>
{:else if lang === 'en'}
    <h1> Hi </h1>
{:else if lang === 'es'}
    <h1> Holla </h1>
{/if}


<h1> Docs 페이지 </h1>
<!-- <h1> 제품{productId}의 리뷰 {reviewId}번</h1> -->


{#if slugArr.length === 1}
<h1>Docs 페이지 ; 주제 {slugArr[0]}</h1>
{:else if slugArr.length === 2}
<h1> Docs 페이지 ; 주제 {slugArr[0]}; 소주제 {slugArr[1]} </h1>
{:else}
    let h1 = document.createElement('h1')
    h1.innerText = "Docs 페이지 "
    for (let idx : number = 1; idx < slugArr.length; idx++) {
        h1.innerText += "; 소주제 " {slugArr[idx]}
    }
{/if}
<!-- 
slug갯수만큼 처리할 수 있다.
 -->
