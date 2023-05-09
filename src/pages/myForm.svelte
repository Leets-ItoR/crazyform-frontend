<script>
    import Sidebar from "../components/admin/sidebar.svelte";
    import Button from "../components/button/Accept.svelte";
</script>

<Sidebar />
<div class="pl-64 flex mt-1 ml-5 space-x-4">
    <h1 class="font-bold items-center pt-5">My Forms</h1>
    <div class="pt-3">
        <Button innerText="Create Form" size="base" />
    </div>
</div>
<div class="pl-64 bg-gray-100 h-screen space-x-4 mt-4">
    <button
        class="mt-4 p-5 ml-5 bg-white w-1/4 rounded-lg hover:bg-gray-50 focus:ring-4 focus:outline-none focus:ring-gray-200 drop-shadow-lg"
    >
        <p>🥺</p>
        <p>title</p>
    </button>
    <button
        class="mt-4 p-5 ml-5 bg-white w-1/4 rounded-lg hover:bg-gray-50 focus:ring-4 focus:outline-none focus:ring-gray-200 drop-shadow-lg"
    >
        <p>🥺</p>
        <p>title</p>
    </button>
</div>
