<script lang="ts">
    import WorkspacePreview from "../Components/workspacePreview.svelte";
    import FolderPreview from "../Components/folderPreview.svelte";
    import NotePreview from "../Components/notePreview.svelte";

    interface HomeData {
        contentType: string;
        amountOfData: number;
    }

    let homeData: HomeData[] = [
        { contentType: "workspace", amountOfData: 10 },
        { contentType: "folder", amountOfData: 5 },
        { contentType: "quick-note", amountOfData: 0 },
    ];
</script>

<div class="fixed top-0 w-full z-50 bg-white shadow-md">
    <nav class="flex items-center justify-between px-6 h-[100px]">
        <div class="flex-none"></div>
        <div
            class="absolute left-1/2 transform -translate-x-1/2 text-[30px] font-bold text-center"
        >
            azalea
        </div>
        <div>
            <p class="mr-5">Edit</p>
        </div>
    </nav>
</div>
<main class="flex justify-center flex-grow pt-16">
    <div class="mt-[100px] grid grid-cols-3 gap-4">
        <!--where the folders, workspaces and quick notes will be displayed -->
        <div class="flex flex-col justify-end">
            <FolderPreview />
        </div>
    </div>
</main>
<div
    class="flex items-center justify-center fixed bottom-0 w-full px-6 h-[175px] bg-white shadow-[0_-4px_6px_-2px_rgba(0,0,0,0.1)]"
>
    <footer>
        <div class="grid grid-cols-4 gap-[5vw]">
            <div id="addNewWorkspace" class="flex flex-col items-center">
                <div
                    class="rounded-full bg-black h-[7.5vw] aspect-square"
                ></div>
                <p class="mt-[10px]">Add New Workspace</p>
            </div>
            <div id="addNewFolder" class="flex flex-col items-center">
                <div
                    class="rounded-full bg-black h-[7.5vw] aspect-square"
                ></div>
                <p class="mt-[10px]">Add New Folder</p>
            </div>
            <div id="addNewNote" class="flex flex-col items-center">
                <div
                    class="rounded-full bg-black h-[7.5vw] aspect-square"
                ></div>
                <p class="mt-[10px]">Add New Note</p>
            </div>
            <div id="Import" class="flex flex-col items-center">
                <div
                    class="rounded-full bg-black h-[7.5vw] aspect-square"
                ></div>
                <p class="mt-[10px]">Import</p>
            </div>
        </div>
    </footer>
</div>
