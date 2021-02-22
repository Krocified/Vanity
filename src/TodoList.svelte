<script>
    import { fade } from 'svelte/transition';

    let todos = [
        {done: false, text: "Escape Tartarus"},
        {done: false, text: "Go Through Asphodel"},
        {done: false, text: "Go Through Elysium"},
        {done: false, text: "Escape Styx"},
        {done: false, text: "Beat Up Hades"},
    ]

    function add(){
        todos = todos.concat({done: false, text: ''})
    }

    function warn(){
        alert("Do your given tasks or clear the list before adding more to it!")
    }
    
    function clear(){
        todos = todos.filter(t=>!t.done)
    }

    function selectAll(){
        todos.forEach(todo => {
            todo.done=true
        });
        todos = todos
    }

    $: remaining = todos.filter(t=>!t.done).length

</script>

<div class="todoList">
    <div class="center">
        <h1>What to do today?</h1>
        {#each todos as todo}
            <div class:done={todo.done}>
                <input type="checkbox" bind:checked={todo.done}>
                <input type="text" placeholder="What needs to be done?" bind:value={todo.text}>
            </div>
        {/each}
        
        {#if remaining===0}
            <p>You've done all your tasks! Good for you!</p>
        {:else if remaining===1}
            <p>Just one more thing!</p>
        {:else}
            <p>You've got {remaining} things to do!</p>
        {/if}
        
        <button on:click={todos.length>=10?warn:add}>Add</button>
        <button on:click="{clear}">Clear</button>
        <button disabled={remaining===0} on:click={selectAll}>Check All</button>
    </div>

    <div class="hypnos">
        {#if todos.length<8}
            <img transition:fade="{{ duration: 150 }}" src="assets/hypnos.png" alt="Hypnos watches your list!" height=400px>
        {/if}
    </div>
</div>
    
<style>

    .todoList{
        position: relative;
    }

    .center{
        text-align: center;
        height:600px;
        display:block;
    }

    .hypnos{
        width: 100%;
        height: 400px;
    }

    img{
        margin-left: 40px;
    }

    input[type=text]{
        margin: 10px auto;
        padding: 10px 15px;
        width: 75%;
        border-radius: 5px;
        border: 1px solid #4b0000;
    }

    button{
        color: white;
        text-transform: uppercase;
        padding: 10px 20px;
        margin: 0px 3px;
        border-radius: 3px;
        border: 0px;
        background-color: #b90000;
    }

    button:disabled{
        background-color: #b9000060;
        color:rgba(245, 245, 245, 0.6);
    }

    p {
        color: white;
        font-size: 17px;
    }

    h1{
        text-align: center;
        font-weight: lighter;
        color: rgb(255, 255, 255);
    }
    
    .done {
		opacity: 0.4;
	}

</style>