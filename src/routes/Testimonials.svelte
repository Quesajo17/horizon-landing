<script>
    let testimonials = [
      { text: "Lorem ipsum dolor sit amet, consectetur adipiscing elit.", name: "John Doe" },
      { text: "Integer vitae enim sit amet ex ultricies condimentum.", name: "Jane Smith" },
      { text: "Suspendisse id nisi et magna tincidunt interdum.", name: "Alice Johnson" },
      { text: "Vestibulum eget felis nec libero varius tempor.", name: "Bob Williams" },
      { text: "Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas.", name: "Emily Brown" },
      { text: "Duis malesuada justo eget tortor mollis, nec aliquet nibh tempus.", name: "David Garcia" },
      { text: "Maecenas id libero vel nulla lobortis congue.", name: "Sarah Martinez" },
      { text: "Fusce nec magna sit amet nunc fermentum feugiat.", name: "Michael Davis" },
      { text: "Quisque sit amet sapien in diam cursus blandit.", name: "Emma Taylor" },
      { text: "Etiam tempus nisl at ipsum fermentum, id ultricies libero fringilla.", name: "Olivia Clark" },
      { text: "Nullam quis lectus ut turpis aliquet gravida.", name: "Daniel Wilson" },
      { text: "Aenean id risus vestibulum, tincidunt urna vel, gravida risus.", name: "Sophia Anderson" }
    ];
  
    let testimonialsPerPage = 3;
    let currentPage = 0;
    
    // Reactive declaration to calculate max pages
    $: maxPages = Math.ceil(testimonials.length / testimonialsPerPage);
    $: visibleTestimonials = testimonials.slice(
        currentPage * testimonialsPerPage, 
        (currentPage + 1) * testimonialsPerPage
    );

    function goToPage(pageIndex) {
        currentPage = pageIndex;
    }

    function next() {
        if (currentPage < maxPages - 1) {
            currentPage++;
        }
    }

    function previous() {
        if (currentPage > 0) {
            currentPage--;
        }
    }
</script>
  
<style>
    .testimonials-container {
        position: relative;
        max-width: 1200px;
        margin: 0 auto;
    }

    .testimonials {
        margin: 0 auto;
        display: grid;
        gap: 2rem;
        padding: 2rem;
        grid-template-columns: repeat(3, 1fr);
        position: relative;
    }

    .testimonial {
        padding: 20px;
        border-radius: 8px;
        text-align: center;
    }
  
    .testimonial h3 {
        margin-top: 1rem;
    }

    /* Navigation arrows */
    .nav-button {
        position: absolute;
        top: 50%;
        transform: translateY(-50%);
        display: flex;
        align-items: center;
        justify-content: center;
        width: 32px;
        height: 32px;
        border-radius: 50%;
        border: none;
        background-color: #E5E5E5;
        cursor: pointer;
        opacity: 0.3;
        transition: opacity 0.2s ease;
        padding: 0;
        z-index: 1;
    }

    .nav-button.prev {
        left: 16px;
    }

    .nav-button.next {
        right: 16px;
    }

    .nav-button:hover {
        opacity: 0.8;
    }

    /* Pagination dots */
    .pagination {
        text-align: center;
        margin: 2rem 0;
    }

    .pagination-button {
        display: inline-block;
        width: 10px;
        height: 10px;
        margin: 0 5px;
        background-color: #bbb;
        border: none;
        border-radius: 50%;
        cursor: pointer;
        transition: background-color 0.3s ease;
        padding: 0;
    }

    .pagination-button.active {
        background-color: #333;
    }

    .pagination-button:focus {
        outline: none;
        box-shadow: 0 0 0 2px #333;
    }

    /* Mobile styles */
    @media (max-width: 768px) {
        .testimonials {
            grid-template-columns: 1fr;
            max-width: 500px;
        }

    }
</style>

<div class="testimonials-container">
    <div class="testimonials">
        {#if currentPage > 0}
            <button class="nav-button prev" on:click={previous} aria-label="Previous testimonials">
                <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                    <path d="M15 18L9 12L15 6" stroke="black" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
                </svg>
            </button>
        {/if}

        {#each visibleTestimonials as testimonial}
            <div class="testimonial">
                <p>{testimonial.text}</p>
                <h3>{testimonial.name}</h3>
            </div>
        {/each}

        {#if currentPage < maxPages - 1}
            <button class="nav-button next" on:click={next} aria-label="Next testimonials">
                <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                    <path d="M9 6L15 12L9 18" stroke="black" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
                </svg>
            </button>
        {/if}
    </div>

    <div class="pagination" role="navigation" aria-label="Testimonial navigation">
        {#each Array(maxPages) as _, i}
            <button
                type="button"
                class="pagination-button {i === currentPage ? 'active' : ''}"
                on:click={() => goToPage(i)}
                aria-label="Go to page {i + 1}"
                aria-current={i === currentPage ? 'page' : undefined}
            />
        {/each}
    </div>
</div>