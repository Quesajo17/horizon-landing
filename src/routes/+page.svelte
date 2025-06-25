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
        <p class="">Build your excitement as you plan, absorb your favorite moments while traveling and bring the best parts back home!</p>
    </div>
    <div class="hero-img">
        <img src='/images/Horizon_Journal.jpg' alt="Journal" />
        <a class="button" href="https://store.horizontraveljournal.com/products/horizon-travel-journal">
            BUY THE JOURNAL
        </a>
    </div>
</div>
<div class="details">
    <h1>What's Inside?</h1>
    
    <div class="details-trio">
        <div class="details-item">
            <h3>Before</h3>
            <!-- <img src='/images/Horizon_Packing_List.jpg' alt="Packing List Page" /> -->
            
                <p>
                    Stay organized and inspired with sections for travel essentials: intention 
                    setting, packing list, itinerary, budget, and more.</p>
        </div>
        <div class="details-item">
            <h3>During</h3>
            <!-- <img src='/images/Horizon_Return.jpg' alt="Return Page" /> -->
            <p>Capture your journey with ease — document daily highlights, key logistics, 
                and memorable moments. Reflect deeper with over two dozen prompts designed 
                to explore your thoughts, emotions, and sensory experiences as you travel.</p>
        </div>
        <div class="details-item">
            <h3>After</h3>
            <!-- <img src='/images/Horizon_Best_Moments.jpg' alt="The Best Moments Page" /> -->
            <p>Navigate the often-overlooked journey home, with space 
                to reflect, remember, and weave your travel inspiration into the 
                life you return to.</p>
        </div>
    </div>
        <!--
        <Testimonials />
    -->
    </div>
    <div class="main-quote">
        <div class="main-quote-line-container">
            <p class="main-quote-line">No journey carries one far unless, 
                as it extends into the world around us,
                it goes an equal distance into the world within.</p>
            <p class="main-quote-attribution">-Lillian Smith</p>
        </div>
        
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
        font-size: 1.25rem;
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

    .details h1 {
        text-align: center;
        margin: 0 auto;
    }

    .details h3 {
        font-size: 3rem;
    }

    .details-summary {
        text-align: center;
        margin: 0 auto;
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
        font-size: 1.25rem;
    }

    .details-item img {
        width: 150px;
        height: 120px;
        object-fit: contain;
        margin-bottom: 1rem;
    }

    .main-quote {
        margin-top: 5rem;
        width: 100%;
        font-family: 'Moontime', sans-serif;
        font-size: 3rem;
        text-align: center;
        align-items: center;
    }

    .main-quote-line-container {
        display: flex;
        flex-direction: column;
        align-items: center;
        padding-left: 4rem;
        padding-right: 4rem;
        max-width: 768px;
        margin: 0 auto;
    }

    .main-quote-line {
       margin: 0;
    }

    .main-quote-attribution {
        margin-top: 0.5rem;
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

        .main-quote-line-container {
        padding-left: 1rem;
        padding-right: 1rem;
    }

    }
</style>
