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
  
    let currentPage = 0;
    const testimonialsPerPage = 3;
  
    function goToPage(pageIndex) {
      currentPage = pageIndex;
    }
  </script>
  
  <style>
    .testimonials {
        margin: 0 auto;
      display: flex;
      flex-wrap: wrap;
      justify-content: space-between;

    }
  
    .testimonial {
      width: calc(25% - 20px);
      /* margin-bottom: 20px; */
      padding: 20px;
      /* border: 1px solid #ccc; */
      border-radius: 8px;
      /* box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1); */
      /* background-color: #f9f9f9; */
    }
  
    .testimonial h3 {
      margin-bottom: 10px;
    }
  
    .pagination {
      text-align: center;
      margin-bottom: 20px;
    }
  
    .dot {
      display: inline-block;
      width: 10px;
      height: 10px;
      margin: 0 5px;
      background-color: #bbb;
      border-radius: 50%;
      cursor: pointer;
    }
  
    .dot.active {
      background-color: #333;
    }
  </style>
  
  <div class="testimonials">
    {#each testimonials.slice(currentPage * testimonialsPerPage, (currentPage + 1) * testimonialsPerPage) as testimonial, i}
      <div class="testimonial" key={i}>
        <p>{testimonial.text}</p>
        <h3>{testimonial.name}</h3>
      </div>
    {/each}
  </div>
  
  <div class="pagination">
    {#each Array.from({ length: Math.ceil(testimonials.length / testimonialsPerPage) }) as _, i}
      <span class="dot {i === currentPage ? 'active' : ''}" on:click={() => goToPage(i)}></span>
    {/each}
  </div>