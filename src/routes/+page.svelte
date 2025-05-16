<script>
	import './styles.css';
    import './fonts.css';
    import SlotMachine from './SlotMachine.svelte';
    import Testimonials from './Testimonials.svelte';

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
        <img src='/images/Horizon_Cover.jpg' alt="Journal" />
        <a href="https://store.horizontraveljournal.com/products/horizon-travel-journal" ><div class="button">
            BUY THE JOURNAL
        </div></a>
    </div>
</div>
<div class="details">
    <div class="details-trio">
        <div class="details-item">
            <h3>Travel Companion</h3>
            <img src='/images/Horizon_Packing_List.jpg' alt="Packing List Page" />
            <p>Travel with a companion</p>
        </div>
        <div class="details-item">
            <h3>Guided Journal</h3>
            <img src='/images/Horizon_Return.jpg' alt="Return Page" />
            <p>Journal your travels</p>
        </div>
        <div class="details-item">
            <h3>Travel Keepsake</h3>
            <img src='/images/Horizon_Best_Moments.jpg' alt="The Best Moments Page" />
            <p>Keep your memories</p>
        </div>
    </div>
    <Testimonials />
</div>

<style>
    .hero {
        display: flex;
        justify-content: space-between;
        align-items: center;
        padding: 2rem;
        gap: 2rem;
    }

    .hero-cta {
        flex: 1;
    }

    .hero-img {
        flex: 1;
    }

    .hero-img img {
        max-width: 100%;
        height: auto;
    }

    .details-trio {
        display: grid;
        grid-template-columns: repeat(3, 1fr);
        gap: 2rem;
        padding: 2rem;
    }

    .details-item {
        display: flex;
        flex-direction: column;
        align-items: center;
        text-align: center;
    }

    .details-item img {
        max-width: 100%;
        height: auto;
    }

    /* Media query for mobile */
    @media (max-width: 768px) {
        .hero {
            flex-direction: column;
            text-align: center;
        }

        .hero-img {
            width: 100%;
        }

        .details-trio {
            grid-template-columns: 1fr;
            gap: 3rem;
            max-width: 500px;
            margin: 0 auto;
        }

        .details-item {
            width: 100%;
        }
    }
</style>
