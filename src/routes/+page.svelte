<script>
    const table = `
O-----O-----O
|.....|.....|
|.O---O---O.|
|.|...|...|.|
|.|.O-O-O.|.|
|.|.|...|.|.|
O-O-O...O-O-O
|.|.|...|.|.|
|.|.O-O-O.|.|
|.|...|...|.|
|.O---O---O.|
|.....|.....|
O-----O-----O
`
.replaceAll('.', 's')
.replaceAll('-', 'v')
.replaceAll('|', 'h')
.replaceAll('O', 'f')

</script>

<h1>Malom Játék</h1>

<div class="grid">
    {#each table.split('\n') as row}
        {#each row.split('') as cell}
            <div class={cell}></div>
        {/each}
    {/each}
</div>


<style>
    div.grid {
        margin: auto;
        display: inline-grid;
        grid-template-columns: repeat(13, 1fr);
        grid-template-rows: repeat(13, 1fr);
        gap: 0px;
    }
    :global(div.grid div) {
        width: 30px;
        height: 30px;
    }
    :global(div.f) {
        border-radius: 15px;
        background: radial-gradient(circle, rgba(255,255,255,1) 0%, rgba(255,255,255,1) 16%, rgba(68,68,68,1) 81%, rgba(68,68,68,1) 83%, rgba(255,255,255,1) 94%, rgba(255,255,255,1) 100%);
    }
    :global(div.s) { 
        background-color: white; 
    } 
    :global(div.h) {
        background: linear-gradient(90deg, rgba(255,255,255,1) 0%, rgba(255,255,255,1) 38%, rgb(183, 183, 183) 42%, rgb(183, 183, 183) 58%, rgba(255,255,255,1) 62%, rgba(255,255,255,1) 100%);
    }
    :global(div.v) {
        background: linear-gradient(0deg, rgba(255,255,255,1) 0%, rgba(255,255,255,1) 38%, rgb(183, 183, 183) 42%, rgb(183, 183, 183) 58%, rgba(255,255,255,1) 62%, rgba(255,255,255,1) 100%);
    }
</style>