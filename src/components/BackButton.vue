<template>
	<a href="/">← Back to all games</a>
</template>

<style scoped>
	a
	{
		display: block;
		position: absolute;
		top: 5px; /* stylelint-disable-line */
		left: 5px;

		font-family: -apple-system, BlinkMacSystemFont, Arial, Helvetica, Roboto, sans-serif;
		font-size: 14px;
		font-weight: 600;
		letter-spacing: 0.02em;
		text-transform: uppercase;
		text-rendering: geometricPrecision;
		-webkit-font-smoothing: antialiased;
		-moz-osx-font-smoothing: grayscale;
		font-feature-settings: "kern" 1;
		font-kerning: normal;

		color: inherit;
		border: 2px dashed;
		border-radius: 6px;
		text-decoration: none;
		padding: 10px 15px;

		opacity: 0.8;
	}

	a:hover, a:focus
	{
		opacity: 1;
	}

	@media screen and (max-width: 600px)
	{
		a
		{
			right: 5px; /* stylelint-disable-line */
			text-align: center;
		}
	}
</style>