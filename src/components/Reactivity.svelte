<script>
	let count = 0;
	$: doubled = count * 2;
	$: numbers = [1];

	function handleClick() {
		// event handler code goes here
		count += 1;
	}
	function addNumber() {
		numbers = [...numbers, numbers.length * 2 ];
	}

	$: if (count === 3) {
		alert("count is 3");
	}
</script>

<button on:click={handleClick}>
	my button clicked {count}
	{count === 1 ? "time" : "times"}
</button>
<p> count doubled is {doubled}. it is also {count * 2} </p>
<button on:click={addNumber}>
	{numbers}
</button>

<style>
	button {
		color: tomato;
	}
</style>
