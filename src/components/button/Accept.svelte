<script>
    export let onClick;
    export let innerText = "확인";
    export let classDetail;
    export let size = "base";
</script>

{#if size == "tiny"}
    <button
        type="button"
        on:click={onClick}
        class="{classDetail} px-3 py-2 text-xs font-medium text-center text-white bg-blue-700 rounded-lg hover:bg-blue-800 focus:ring-4 focus:outline-none focus:ring-blue-300"
        >{innerText}</button
    >
{:else if size == "small"}
    <button
        type="button"
        on:click={onClick}
        class="{classDetail} px-3 py-2 text-sm font-medium text-center text-white bg-blue-700 rounded-lg hover:bg-blue-800 focus:ring-4 focus:outline-none focus:ring-blue-300"
        >{innerText}</button
    >
{:else if size == "base"}
    <button
        type="button"
        on:click={onClick}
        class="{classDetail} text-white bg-blue-700 hover:bg-blue-800 focus:ring-4 focus:outline-none focus:ring-blue-300 font-medium rounded-lg text-sm px-5 py-2.5 text-center"
        >{innerText}</button
    >
{:else if size == "large"}
    <button
        type="button"
        on:click={onClick}
        class="{classDetail} px-5 py-3 text-base font-medium text-center text-white bg-blue-700 rounded-lg hover:bg-blue-800 focus:ring-4 focus:outline-none focus:ring-blue-300"
        >{innerText}</button
    >
{:else if size == "big"}
    <button
        type="button"
        on:click={onClick}
        class="{classDetail} text-white bg-blue-700 hover:bg-blue-800 focus:ring-4 focus:outline-none focus:ring-blue-300 font-medium rounded-lg text-base px-6 py-3.5 text-center"
        >{innerText}</button
    >
{/if}
