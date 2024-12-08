<script lang="ts">
    let contentNum: number = 3;
    let displayNum: number = 0;

    switch (true) {
        case contentNum > 3:
            displayNum = 3;
            break;
        case contentNum <= 3:
            displayNum = contentNum;
            break;
        case contentNum <= 0:
            displayNum = 0;
            break;
        default:
            displayNum = 0;
            break;
    }
</script>

<div
    class="relative flex justify-center"
    style="height: calc(250px + {displayNum *
        12}px); width: 23vw;margin-top: {displayNum * 12}px"
>
    {#each Array(displayNum) as _, i}
        {#if i === 0}
            <div
                class="absolute h-full border rounded"
                style="top: {i * -12}px; z-index:
                {-i}; width: calc(100% - {i *
                    40}px); background-color:rgb({255 - i * 5}, {255 -
                    i * 5}, {255 - i * 5})"
            >
                <h1
                    class="absolute bottom-0 left-0 w-full text-centre pb-5 pl-5"
                >
                    Folder Name
                </h1>
            </div>
        {:else}
            <div
                class="absolute h-full border rounded"
                style="top: {i * -12}px; z-index:
            {-i}; width: calc(100% - {i * 40}px); background-color:rgb({255 -
                    i * 5}, {255 - i * 5}, {255 - i * 5})"
            ></div>
        {/if}
    {/each}
</div>
