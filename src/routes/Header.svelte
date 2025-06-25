<script>
	let isMenuOpen = false;
	
	function toggleMenu() {
		isMenuOpen = !isMenuOpen;
	}
</script>

<header>
	<div class="brand">
		<div class="brand-image">
			<a href="/">
				<img src="/images/logo.png" class="logo" alt="Horizon Travel Journal Logo" />
			</a>
		</div>
	</div>

	<!-- Hamburger button for mobile -->
	<button class="hamburger" on:click={toggleMenu} aria-label="Menu">
		<span class="hamburger-line"></span>
		<span class="hamburger-line"></span>
		<span class="hamburger-line"></span>
	</button>

	<!-- Navigation links -->
	<nav class="header-links" class:open={isMenuOpen}>
		<a class="header-link menu-link" href="https://store.horizontraveljournal.com/" on:click={() => isMenuOpen = false}>Shop</a>
		<a class="header-link" href="/" on:click={() => isMenuOpen = false}>Home</a>
		<div class="menu-divider"></div>
		<a class="header-link" href="/about" on:click={() => isMenuOpen = false}>About</a>
		<div class="menu-divider"></div>
		<a class="header-link" href="/contact" on:click={() => isMenuOpen = false}>Contact Us</a>
	</nav>

	<a class="header-button" href="https://store.horizontraveljournal.com/"><div class="button">SHOP</div></a>
</header>

<style>
	header {
		display: flex;
		justify-content: space-between;
		align-items: center;
		padding: 0 5em;
		position: relative;
	}

	.brand {
		display: flex;
		align-items: center;
		padding-left: 1em;
	}

	.brand-image {
		width: 120px;
		height: 120px;
		object-fit: contain;
		border-radius: 20%;
	}

	.logo {
		width: 120px;
		height: 120px;
		object-fit: contain;
		border-radius: 20%;
	}

	.header-links {
		display: flex;
		padding: 1em;
		align-items: center;
		gap: 1em;
	}

	.header-link {
		padding: 1em;
		text-decoration: none;
		font-size: 1rem;
		color: var(--color-text);
		font-family: 'Opti-Goudy', sans-serif;
	}

	.menu-link {
		display: none;
	}

	.header-link:hover {
		text-decoration: underline;
	}

	/* Hamburger button styles */
	.hamburger {
		display: none;
		flex-direction: column;
		justify-content: space-around;
		width: 2rem;
		height: 2rem;
		background: transparent;
		border: none;
		cursor: pointer;
		padding: 0;
		z-index: 10;
	}

	.hamburger-line {
		width: 2rem;
		height: 0.25rem;
		background-color: #000000;
		transition: all 0.3s linear;
		position: relative;
		transform-origin: 1px;
		
	}

	.menu-divider {
		display: none; /* Hidden by default on desktop */
	}

	/* Mobile styles */
	@media (max-width: 768px) {
		header {
			padding: 0 1em;
		}

		.header-button {
			display: none;
		}

		.hamburger {
			display: flex;
		}

		.header-links {
			display: none;
			flex-direction: column;
			position: absolute;
			top: 100%;
			right: 0;
			background: white;
			padding: 1em 0em;
			box-shadow: 0 2px 5px rgba(0,0,0,0.1);
			width: 100%;
			text-align: center;
			z-index: 1;
		}

		.header-links.open {
			display: flex;
		}

		.header-link {
			padding: 0.5em;
			width: 100%;
		}

		.menu-link {
		display: none;
	}

		.button {
			margin-top: 1em;
		}

		.brand-image {
		width: 60px;
		height: 60px;
		object-fit: contain;
		border-radius: 20%;
	}

	.logo {
		width: 60px;
		height: 60px;
		object-fit: contain;
		border-radius: 20%;
	}

		.menu-divider {
			display: block;
			width: 100%;
			height: 1px;
			background-color: #e0e0e0;
			margin: 0;
		}
	}
</style>
