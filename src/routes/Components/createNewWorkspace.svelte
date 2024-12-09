<script lang="ts">
    import { onMount } from "svelte";
    let workspaceName: string = "";

    function createWorkspaceName(event: Event) {
        event.preventDefault();
        console.log("Workspace Name:", workspaceName);
    }
</script>

<div class="w-full h-full">
    <div
        class="flex justify-center items-center w-full h-full bg-white/5 backdrop-blur"
    >
        <div
            class="flex justify-center bg-white h-[25vw] w-[55vw] rounded-lg shadow-[0px_0px_30px_20px_rgba(0,0,0,0.1)]"
        >
            <form
                on:submit={createWorkspaceName}
                class="flex flex-col justify-center items-center"
            >
                <h1 class="text-center mt-10 ml-5 mr-5">
                    What Do You Want To Call Your Workspace?
                </h1>
                <input
                    type="text"
                    bind:value={workspaceName}
                    class="w-[80%] border-2 mt-7 mb-7"
                />
                <button type="submit" class="mb-10 w-[60%] h-[20%] border-2"
                    >Submit</button
                >
            </form>
        </div>
    </div>
</div>
