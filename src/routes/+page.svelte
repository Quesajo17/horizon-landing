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
        <p class="">Build your excitement as you plan, absorb your favorite moments during your trip and bring the best parts back home!</p>
    </div>
    <div class="hero-img">
        <img src='/images/Horizon_Journal.jpg' alt="Journal" />
        <a class="button" href="https://store.horizontraveljournal.com/products/horizon-travel-journal">
            BUY THE JOURNAL
        </a>
    </div>
</div>
<div class="details">
    
    <div class="details-trio">
        <div class="details-item">
            <h3>Before</h3>
            <!-- <img src='/images/Horizon_Packing_List.jpg' alt="Packing List Page" /> -->
            
                <p>
                    Fuel your excitement while recording important preparations before
                    your trip even begins with sections including intention setting, 
                    packing list, itinerary, travel budget, and more. </p>
        </div>
        <div class="details-item">
            <h3>During</h3>
            <!-- <img src='/images/Horizon_Return.jpg' alt="Return Page" /> -->
            <p>Record daily events and important logistics during your trip, and
                reflect on your experiences with over two dozen prompts that tap into
            your thoughts, emotions, and sensations as you travel.</p>
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
    <div class="divider"></div>




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

    .main-quote {
        margin-top: 5rem;
        width: 100%;
        font-family: 'Moontime', sans-serif;
        font-size: 2rem;
        text-align: center;
        align-items: center;
    }

    .main-quote-line-container {
        display: flex;
        flex-direction: column;
        align-items: center;
        padding-left: 4rem;
        padding-right: 4rem;
        max-width: 420px;
        margin: 0 auto;
    }

    .main-quote-line {
       margin: 0;
    }

    .main-quote-attribution {
        margin-top: 0.5rem;
    }

    .divider {
        width: 75%;
        height: 1px;
        background-color: var(--light-color);
        margin: 2rem auto 0;
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
