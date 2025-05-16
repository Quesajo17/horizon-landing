<script>
	import './styles.css';
    import './fonts.css';
    import SlotMachine from './SlotMachine.svelte';
    import Testimonials from './Testimonials.svelte';
    import { Images } from '$lib/constants';
</script>
<div class="hero">
    <div class="hero-cta">
        <div class="hero-header">
            <span class="hero-title">Horizon is</span><span class="hero-subtitle"><SlotMachine /></span>
        </div>
        <p class="">Here is a travel journal that will be a beautiful keepsake, a lovely journal, and something else.</p>
        <p class="">Using this journal for your reasons is a good thing to do.</p>
    </div>
    <div class="hero-img">
        <img src="../src/lib/images/Horizon_Cover.jpg" alt="Journal" />
        <a href="https://store.horizontraveljournal.com/products/horizon-travel-journal" ><div class="button">
            BUY THE JOURNAL
        </div></a>
    </div>
</div>
<div class="details">
    <div class="details-trio">
        <div class="details-item">
            <h3>Travel Companion</h3>
            <img src={Images.travelCompanion} alt="Packing List Page" />
            <p>Travel with a companion</p>
        </div>
        <div class="details-item">
            <h3>Guided Journal</h3>
            <img src={Images.guidedJournal} alt="Return Page" />
            <p>Journal your travels</p>
        </div>
        <div class="details-item">
            <h3>Travel Keepsake</h3>
            <img src={Images.travelKeepsake} alt="The Best Moments Page" />
            <p>Keep your memories</p>
        </div>
    </div>
    <Testimonials />
</div>
<nav>
    <a href="/">Home</a>
    <a href="/about">About</a>
    <a href="/contact">Contact</a>
</nav>
