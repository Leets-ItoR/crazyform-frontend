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
<div class="pl-64 bg-gray-100 h-screen space-x-4" />
