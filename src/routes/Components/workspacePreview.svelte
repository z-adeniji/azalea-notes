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

<div class="relative h-[274px] border rounded bg-white" style="width: 23vw">
    <h1 class="absolute bottom-0 left-0 w-full text-centre text-xl pb-5 pl-5">
        Workspace Name
    </h1>
</div>
