<script>
	import { page } from '$app/stores';
</script>	

<footer>
	<div class="footer-copyright">
		<span>Copyright Page Fam Designs, LLC, 2024</span>
	</div>
	<div class="footer-links">
		<a href="https://www.blog.lattisapp.com">Blog</a>
		<a href="/privacy-policy">Privacy Policy</a>
		<a href="/support">Support</a>
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