<script>
	export let segment;
</script>

<style>
	div {
		display: flex;
		flex-direction: column;
		padding-top: 1rem;
		text-align: center;
	}

	h1 {
		font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
		font-size: 1.2rem;
		text-transform: uppercase;
	}

	ul {
		border-bottom: 1px solid #dfdfdf;
		border-top: 1px solid #dfdfdf;
		display: flex;
		justify-content: center;
		padding-bottom: 1rem;
		padding-top: 1rem;
	}

	li {
		margin-right: 1rem;
	}

	a {
		text-decoration: none;
	}

	.current {
		text-decoration: underline;
	}
</style>

<div>
	<header>
		<svg width="50" height="36" xmlns="http://www.w3.org/2000/svg"><path d="M49.493 10.155a1.26 1.26 0 00-1.53.005l-13.16 10.045L26.164.69c-.41-.92-1.916-.92-2.326 0L15.1 20.433 2.054 10.172a1.269 1.269 0 00-1.968 1.457L9.15 35.044a1.268 1.268 0 001.183.81h29.335a1.263 1.263 0 001.184-.81l9.062-23.415a1.268 1.268 0 00-.421-1.474zM38.798 33.314H11.204L4.126 15.032l10.69 8.404c.308.244.707.327 1.092.238a1.278 1.278 0 00.856-.721l8.238-18.61 8.129 18.363a1.275 1.275 0 001.936.497l10.859-8.291-7.128 18.402z"/></svg>
		<h1>Sapper Demo</h1>
	</header>

	<nav>
		<ul>
			<li>
				<a href="/" class='{ segment === undefined ? 'current' : '' }'>
					Listings
				</a>
			</li>
			<li>
				<a href="about" class='{ segment === 'about' ? 'current' : '' }'>
					About
				</a>
			</li>
		</ul>
	</nav>
</div>
