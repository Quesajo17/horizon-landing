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
        <a class="button" href="https://store.horizontraveljournal.com/products/horizon-travel-journal">
            BUY THE JOURNAL
        </a>
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
    /* Hero section styles */
    .hero {
        display: flex;
        justify-content: space-between;
        align-items: center;
        padding: 2rem;
        gap: 2rem;
        max-width: 1200px;
        margin: 0 auto;
    }

    .hero-header {
        width: 100%;
        overflow: auto;
        align-items: first baseline;
    }

    .hero-title {
        font-family: 'Moontime', sans-serif;
        font-size: 4rem;
    }

    .hero-subtitle {
        font-family: 'Opti-Goudy', sans-serif;
        font-size: 40px;
        padding-left: 16px;
    }

    .hero-cta {
        flex: 1;
        min-width: 300px;
    }

    .hero-img {
        flex: 1;
        position: relative;
        max-width: 600px;
        width: 100%;
        margin: 0 auto;
        overflow: visible;
    }

    .hero-img img {
        width: 100%;
        height: auto;
        display: inline-block;
        position: relative;
    }

    .hero-img .button {
        position: absolute;
        right: 24px;
        bottom: 24px;
        line-height: 1.25;
        border: none;
        width: 90px;
        border-radius: 4px;
        opacity: 0.8;
        box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
    }

    .hero-img .button:hover {
        opacity: 1;
    }

    /* Details section styles */
    .details {
        width: 100%;
        background-color: var(--color-bg-1);
        padding: 2rem 0;
    }

    .details-trio {
        display: grid;
        grid-template-columns: repeat(3, 1fr);
        gap: 2rem;
        max-width: 1200px;
        margin: 0 auto;
        padding: 2rem;
    }

    .details-item {
        display: flex;
        flex-direction: column;
        align-items: center;
        text-align: center;
    }

    .details-item img {
        width: 150px;
        height: 120px;
        object-fit: contain;
        margin-bottom: 1rem;
    }

    /* Tablet styles */
    @media (max-width: 1024px) {
        .hero {
            padding: 2rem;
            gap: 1rem;
        }
    }

    /* Mobile styles */
    @media (max-width: 768px) {
        .hero {
            flex-direction: column;
            text-align: center;
            padding: 1rem;
        }

        .hero-cta {
            min-width: auto;
        }

        .hero-subtitle {
            font-size: 28px;
        }

        .hero-img {
            width: 100%;
            max-width: 500px;
            margin: 0 auto;
            padding: 0;
        }

        .details-trio {
            grid-template-columns: 1fr;
            gap: 3rem;
            max-width: 500px;
            padding: 1rem;
        }
    }

    /* Small mobile screens */
    @media (max-width: 480px) {
        .hero-img {
            max-width: 100%;
        }
    }
</style>
