<script>
    export let array = ["주하", "서빈", "동현", "대겸"];
</script>

<div class="z-10 w-52 p-5 text-white bg-gray-600 rounded-lg shadow">
    <h5 class="mb-3 text-white">Rating</h5>
    <ul class="space-y-2 text-sm">
        {#each array as text}
            <li class="flex items-center">
                <input
                    id={text}
                    type="radio"
                    value=""
                    name={text}
                    class="w-4 h-4 bg-gray-100 border-gray-300 text-primary-600 focus:ring-primary-500"
                />
                <label for="three-stars" class="flex items-center ml-2">
                    {text}
                </label>
            </li>
        {/each}
    </ul>
</div>
