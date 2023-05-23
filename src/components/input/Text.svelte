<script>
    export let name = "";
    export let id = "";
    export let type = "text";
    export let placeholder = "내용을 입력하세요";
    export let value = "";
</script>

{#if type === "text"}
    <input
        {name}
        {id}
        type="text"
        bind:value
        class="bg-gray-50 border border-gray-300 text-gray-900 sm:text-sm rounded-lg focus:ring-primary-600 focus:border-primary-600 block w-full p-2.5"
        {placeholder}
        required=""
    />
{:else if type === "email"}
    <input
        {name}
        {id}
        type="email"
        bind:value
        class="bg-gray-50 border border-gray-300 text-gray-900 sm:text-sm rounded-lg focus:ring-primary-600 focus:border-primary-600 block w-full p-2.5"
        {placeholder}
        required=""
    />
{:else if type === "password"}
    <input
        {name}
        {id}
        type="password"
        bind:value
        class="bg-gray-50 border border-gray-300 text-gray-900 sm:text-sm rounded-lg focus:ring-primary-600 focus:border-primary-600 block w-full p-2.5"
        {placeholder}
        required=""
    />
{/if}
