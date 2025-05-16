<script>
	import { page } from '$app/stores';
</script>	

<footer>
	<div class="footer-copyright">
		<span>Copyright Page Fam Designs, LLC, 2024</span>
	</div>
	<div class="footer-links">
		<a class="header-link" href="https://www.blog.lattisapp.com">
			Home
		</a>
		<a class="header-link" href="https://www.blog.lattisapp.com">
			About
		</a>
		<a class="header-link" href="https://www.blog.lattisapp.com">
			Contact Us
		</a>
	</div>
</footer>

<style>
    	footer {
		display: flex;
		flex-direction: column;
		justify-content: space-between;
		align-items: center;
		padding: 12px;
	}

	.footer-links a {
		padding: 10px;
	}

	@media (min-width: 480px) {
		footer {
			padding: 12px 0;
		}
	}
</style>