<script>
	const name = "TriplexLab"
	const htmlName = "<span style='color:red;'>TriplexLab</span>"
	const urlImg = "https://manbalboy.github.io/assets/img/blog/svelte/svelte.png"

	let count = 0;
	function increaseCount() {
		count++;
	}
	//'$:'으로 프로그램 코드도 제어를 할수가 있다.
	$: if(count >= 5){
		alert("Count는 5보다 클수 없습니다.");
		count = 5
	}
	$: sum = count * 2; //'$:'은 coun변수를 주시하고 있다가 변경사항이 있을때 반영해 줍니다.
</script>

<button type="button" on:click={increaseCount}>Count</button>
<div>Count: {count}</div>
<div>Sum: {sum}</div>

<h1>Hello {name}</h1>
<h1>Hello {@html htmlName}</h1>

<img src={urlImg} alt="" />


<style>

</style>