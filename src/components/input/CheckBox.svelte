<script>
    export let array = ["주하", "서빈", "동현", "대겸"];
</script>

<div id="dropdown" class="z-10 w-52 p-5 bg-white rounded-lg shadow">
    <h5 class="mb-3 text-sm font-medium text-gray-900">Category</h5>
    <ul class="space-y-2 text-sm">
        {#each array as text}
            <li class="flex items-center">
                <input
                    id={text}
                    type="checkbox"
                    value=""
                    class="w-4 h-4 bg-gray-100 border-gray-300 rounded text-primary-600 focus:ring-primary-500"
                />
                <label
                    for={text}
                    class="ml-2 text-sm font-medium text-gray-900"
                >
                    {text}
                </label>
            </li>
        {/each}
    </ul>
</div>
