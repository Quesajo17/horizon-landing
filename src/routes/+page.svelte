<script>
	import './styles.css';
    import './fonts.css';
    import SlotMachine from './SlotMachine.svelte';
    import Testimonials from './Testimonials.svelte';
</script>
<div class="hero">
    <div class="hero-cta">
        <div class="hero-header">
            <span class="hero-title">Horizon is</span><span class="hero-subtitle"><u>a travel journal.</u></span>
        </div>
        <p class="">Here is a travel journal that will be a beautiful keepsake, a lovely journal, and something else.</p>
        <p class="">Using this journal for your reasons is a good thing to do.</p>
    </div>
    <div class="hero-img">
        <img src="https://upload.wikimedia.org/wikipedia/commons/3/3f/Placeholder_view_vector.svg" alt="Journal Image" />
        <div class="button" href="https://www.blog.lattisapp.com">
            BUY THE JOURNAL
        </div>
    </div>
</div>
<div class="details">
    <div class="details-trio">
        <div class="details-item">
            <h3>Travel Companion</h3>
            <img src="https://upload.wikimedia.org/wikipedia/commons/3/3f/Placeholder_view_vector.svg" alt="Journal Image" />
            <p>Travel with a companion</p>
        </div>
        <div class="details-item">
            <h3>Guided Journal</h3>
            <img src="https://upload.wikimedia.org/wikipedia/commons/3/3f/Placeholder_view_vector.svg" alt="Journal Image" />

            <p>Journal your travels</p>
        </div>
        <div class="details-item">
            <h3>Travel Keepsake</h3>
            <img src="https://upload.wikimedia.org/wikipedia/commons/3/3f/Placeholder_view_vector.svg" alt="Journal Image" />
            <p>Keep your memories</p>
        </div>
    </div>
    <Testimonials />
</div>
