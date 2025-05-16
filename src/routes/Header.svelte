<script>
	import logo from '/images/logo.png';
</script>

<header>
	<div class="brand">
	<div class="brand-image">
		<a href="/">
			<img src={logo} class="logo" alt="Horizon Travel Journal Logo" />
		</a>
	</div>
	</div>
	<div class="header-links">
		<a class="header-link" href="/">
			Home
		</a>
		<a class="header-link" href="/about">
			About
		</a>
		<a class="header-link" href="/contact">
			Contact Us
		</a>
	</div>


	<a href="https://store.horizontraveljournal.com/"><div class="button">
		SHOP
	</div></a>

</header>

<style>
	header {
		display: flex;
		justify-content: space-between;
		align-items: center;
		padding: 0 5em;
		 /* Add padding as needed */
	}

	.brand {
		display: flex;
		align-items: center;
		padding-left: 1em;
	}

	.brand-name {
		font-size: 1.5em;
		font-weight: 500;
		margin-left: 1em;
	}

	.brand-image {
		width: 80px;
		height: 80px;
		object-fit: contain;
		border-radius: 20%;
	}

	.header-links {
		display: flex;
		padding: 1em;
	}

	.header-link {
		padding: 1em;
		text-decoration: none;
		color: var(--color-text);
		font-family: sans-serif;
	}

	.header-link:hover {
		text-decoration: underline;
	
	}

	/*
	a {
		text-decoration: none;
		color: var(--color-text);
		font-family: sans-serif;
	}*/


	.logo {
		width: 80px;
		height: 80px;
		object-fit: contain;
		border-radius: 20%;
	}



	a:hover {
		color: var(--color-text);
	}
</style>
