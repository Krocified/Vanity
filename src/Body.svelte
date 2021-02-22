<script>
    import Gallery from "./Gallery.svelte";
    import TodoList from "./TodoList.svelte";

</script>

<div id="body">
	<div class="row">
        <div class="column left">
            <TodoList/>
        </div>
        <div class="column right">
            <Gallery/>
        </div>
    </div>
</div>

<style>
    #body{
        margin-top: 0;
		width: 100%;
		min-height: 1000px;
    }
    
    .row {
        display: flex;
        height: 100%;
    }

    .column {
        float: left;
        height: 100%;
    }

    .left {
        width: 50%;
        background-color: #6d0000;
        height: 1000px;
        
    }

    .right {
        width: 50%;
        background-color: #520000;
        height: 1000px;
    }

    @media (max-width: 850px) {
		.row {
            display: block;
            height: 100%;
        }

        .column {
            float: left;
            height: 100%;
        }

        .left {
            width: 100%;
        }

        .right {
            width: 100%;
        }
	}
</style>