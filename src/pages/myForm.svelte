<script>
    import Sidebar from "../components/admin/sidebar.svelte";
    import Button from "../components/button/Accept.svelte";
</script>

<Sidebar />
<div class="pl-64 flex mt-1 ml-10 mr-10 justify-between pt-3">
    <h1 class="font-bold items-center pt-2">My Forms</h1>
    <a href="/createform">
        <Button innerText="Create Form" size="base" />
    </a>
</div>
<div class="pl-64 bg-gray-100 h-screen space-x-4">
    <div class="max-w-7xl mx-auto grid grid-cols-4 gap-4 ml-4 mt-4 pt-4">
        <button
            class="p-10 bg-white col-span-1 rounded-lg hover:bg-gray-50 focus:ring-4 focus:outline-none focus:ring-gray-200 drop-shadow-lg"
        >
            <p>🥺</p>
            <p>title</p>
        </button>
        <button
            class="p-10 bg-white col-span-1 rounded-lg hover:bg-gray-50 focus:ring-2 focus:outline-none focus:ring-gray-100 ring-offset-2 drop-shadow-lg"
        >
            <p>🥺</p>
            <p>title</p>
        </button>
    </div>
</div>
