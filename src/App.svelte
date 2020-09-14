<svelte:options tag="svelte-beauty-header"></svelte:options>
<script>
	export let name;
	export let subname;
	export let description;
	export let button;
	export let active;
</script>
{#if !!active}
<main>
	<header>
		<div class="overlay">
	<h1>{name?name: ''}</h1>
	<h3>{subname?subname: ''}</h3>
	<p>{description?description: ''}</p>
		<br>
		<div>
		{#if !!button}
		<button>{button?button:''}</button>
		{/if}
		</div>
	</header>
</main>
{/if}

<style>
	*{padding: 0; margin: 0; box-sizing: border-box;}
	body{height: 900px;}
	header {
		text-align: center;
		width: 100%;
		height: auto;
		background-size: cover;
		background-attachment: fixed;
		position: relative;
		overflow: hidden;
		border-radius: 0 0 85% 85% / 30%;
	}
	header .overlay{
		width: 100%;
		height: 100%;
		padding: 50px;
		color: #FFF;
		text-shadow: 1px 1px 1px #333;
	background-image: linear-gradient( 135deg, #9f05ff69 10%, #fd5e086b 100%);
		
	}

	h1 {
		font-family: 'Dancing Script', cursive;
		font-size: 80px;
		margin-bottom: 30px;
	}

	h3, p {
		font-family: 'Open Sans', sans-serif;
		margin-bottom: 30px;
	}

	button {
		border: none;
		outline: none;
		padding: 10px 20px;
		border-radius: 50px;
		color: #333;
		background: #fff;
		margin-bottom: 50px;
		box-shadow: 0 3px 20px 0 #0000003b;
	}
	button:hover{
		cursor: pointer;
	}
</style>