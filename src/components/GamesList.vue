<template>
	<ol class="games" reversed>
		<li>
			<a href="/games/midnight-train" class="title">Midnight Train</a>
			<p>A framework for fluidly moving between game systems within a single, continous narrative.</p>
		</li>
		<li>
			<a href="/games/witchcraft" class="title">Witchcraft</a>
			<p>A game about witches.</p>
		</li>
		<li>
			<a href="/games/silverscreen" class="title">Silverscreen</a>
			<p>A system for collaborative storytelling that focuses on generating cinematic gameplay.</p>
		</li>
	</ol>
</template>

<style scoped>
	ol.games
	{
		list-style: game-number;
		list-style-position: inside;
		text-align: center;
		padding: 10px;
	}

	ol.games li::marker
	{
		font-weight: 600;
		letter-spacing: 0.02em;
	}

	ol.games li
	{
		margin: 120px 0;
		animation: slide-in 2s cubic-bezier(0.2, 0.6, 0, 1) 1;
	}

	.title
	{
		font-family: var(--primary-font);
		color: var(--light-green);
		font-size: 9.2rem;
		letter-spacing: -0.04em;
		line-height: 0.9;
		text-decoration: none;
		display: block;
		position: relative;
		transition: transform 50ms ease-out;
	}

	.title:hover, .title:focus
	{
		color: transparent;
		-webkit-text-stroke: 2px var(--light-green);
		outline: none;
		transform: scale(0.96);
	}

	p
	{
		font-family: var(--primary-font);
		font-size: 1.5rem;
		letter-spacing: 0.01em;
		line-height: 1.5;

		max-width: 40ch;
		margin: 0 auto;
	}

	/* stylelint-disable property-no-unknown -- no safari support, but fallback is ok */
	@counter-style game-number
	{
		system: extends decimal;
		pad: 2 "0";
		prefix: "GAME № ";
		suffix: "";
	}

	@keyframes slide-in
	{
		0%
		{
			transform: translateY(80px);
			opacity: 0;
		}

		10%
		{
			opacity: 0;
		}

		100%
		{
			transform: translateY(0);
			opacity: 1;
		}
	}

	@media screen and (max-width: 700px)
	{
		.title
		{
			font-size: 6rem;
		}
	}

	@media screen and (max-width: 430px)
	{
		.title
		{
			font-size: 5rem;
		}
	}
</style>

