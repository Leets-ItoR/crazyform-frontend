<script>
    export let name = "";
    export let id = "";
    export let placeholder = "내용을 입력하세요";
</script>

<input
    type="text"
    {name}
    {id}
    class="bg-gray-50 border border-gray-300 text-gray-900 sm:text-sm rounded-lg focus:ring-primary-600 focus:border-primary-600 block w-full p-2.5"
    {placeholder}
    required=""
/>
