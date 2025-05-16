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

    function handleKeydown(event, pageIndex) {
        if (event.key === 'Enter' || event.key === ' ') {
            event.preventDefault();
            goToPage(pageIndex);
        }
    }
</script>
  
<style>
    .testimonials {
        margin: 0 auto;
        display: grid;
        gap: 2rem;
        padding: 2rem;
    }

    /* Desktop */
    .testimonials {
        grid-template-columns: repeat(3, 1fr);
        max-width: 1200px;
    }

    /* Tablet */
    @media (max-width: 1024px) {
        .testimonials {
            grid-template-columns: repeat(2, 1fr);
            max-width: 800px;
        }
    }

    /* Mobile */
    @media (max-width: 768px) {
        .testimonials {
            grid-template-columns: 1fr;
            max-width: 500px;
        }
    }
  
    .testimonial {
        padding: 20px;
        border-radius: 8px;
        text-align: center;
    }
  
    .testimonial h3 {
        margin-top: 1rem;
    }
  
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
</style>
  
<div class="testimonials">
    {#each visibleTestimonials as testimonial, i}
        <div class="testimonial">
            <p>{testimonial.text}</p>
            <h3>{testimonial.name}</h3>
        </div>
    {/each}
</div>

<div class="pagination" role="navigation" aria-label="Testimonial navigation">
    {#each Array(maxPages) as _, i}
        <button
            type="button"
            class="pagination-button {i === currentPage ? 'active' : ''}"
            on:click={() => goToPage(i)}
            on:keydown={(e) => handleKeydown(e, i)}
            aria-label="Go to page {i + 1}"
            aria-current={i === currentPage ? 'page' : undefined}
        />
    {/each}
</div>