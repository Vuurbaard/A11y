<script lang="ts">
	let listItems = ['Item 1', 'Item 2', 'Item 3'];
</script>

<nav aria-label="Main navigation">
    <a href="/">⬅️ Go back</a>
</nav>

<h1>Lists</h1>

<main>
    <section aria-label="Dynamic list">
        <h2>Dynamic list</h2>
        <button on:click={() => listItems = [...listItems, `Item ${listItems.length + 1}`]}>Add item</button>
        <button on:click={() => {listItems.pop(); listItems = listItems} }>Remove item</button>
        <ul aria-live="polite">
            {#each listItems as item}
            <li>{item}</li>
            {/each}
        </ul>
    </section>
</main>