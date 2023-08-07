<script>
  import { writable } from "svelte/store";

    export const data1= writable([
    {
      id: 1,
      title: "Company 1",
      description: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Quisquam, voluptatum.",
    },
    {
      id: 2,
      title: "company 2",
        description: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Quisquam, voluptatum.",
    },
    {
      id: 3,
      title: "Company 3",
        description: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Quisquam, voluptatum.",
      
    },
    ]);
</script>

<div class="sidebar">
    <!-- Search input -->
    <input type="text" placeholder="Search..." />
  
    <!-- List of cards (data1) -->
    {#each $data1 as item}
      <div class="card">
        <h3>{item.title}</h3>
        <p>{item.description}</p>
      </div>
    {/each}
  
    <!-- Add new card button (opens modal) -->
    <button>Add New Card</button>
  </div>