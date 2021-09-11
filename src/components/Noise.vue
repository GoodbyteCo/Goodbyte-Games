<template>
	<div id="noise" role="presentation"></div>
</template>

<style scoped>
	#noise
	{
		position: fixed;
		top: 0;
		left: 0;
		right: 0;
		bottom: 0;
		z-index: 999;

		background-image: url("https://goodbyte.games/assets/Witchcraft/images/noise.jpg");
		background-size: 800px;
		background-repeat: repeat;
		
		opacity: 0.08;
		pointer-events: none;
		animation: noise 7s steps(10) infinite;
	}

	@keyframes noise
	{
		0% { background-position: 0px 0px; }
		10% { background-position: 100px 200px; }
		20% { background-position: 500px 0px; }
		30% { background-position: 300px 100px; }
		40% { background-position: 0px 400px; }
		50% { background-position: 400px 300px; }
		60% { background-position: 200px 200px; }
		70% { background-position: 500px 400px; }
		80% { background-position: 100px 0px; }
		90% { background-position: 300px 300px; }
	}
</style>