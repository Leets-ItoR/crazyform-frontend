<script>
    import Logo from "../components/Icon.svelte";
    import Input from "../components/input/Text.svelte";
    import Visible from "../assets/visible.png";
    import Invisible from "../assets/invisible.png";

    let state = "visible";
    let inputType = "text";

    const toVisible = () => {
        state = "visible";
        inputType = "text";
    };
    const toInvisible = () => {
        state = "invisible";
        inputType = "password";
    };
</script>

<section class="bg-gray-50">
    <div
        class="flex flex-col items-center justify-center px-6 py-8 mx-auto md:h-screen lg:py-0"
    >
        <a
            href="/"
            class="flex items-center mb-6 text-2xl font-semibold text-gray-900"
        >
            <Logo />
        </a>
        <div
            class="w-full bg-white rounded-lg shadow md:mt-0 sm:max-w-md xl:p-0"
        >
            <div class="p-6 space-y-4 md:space-y-6 sm:p-8">
                <h1
                    class="text-xl font-bold leading-tight tracking-tight text-gray-900 md:text-2xl"
                >
                    회원가입
                </h1>
                <div>
                    <label
                        for="email"
                        class="block mb-2 text-sm font-medium text-gray-900"
                        >닉네임</label
                    >
                    <Input type="email" placeholder="ItoR" />
                </div>
                <div>
                    <label
                        for="email"
                        class="block mb-2 text-sm font-medium text-gray-900"
                        >Email</label
                    >
                    <Input type="email" placeholder="name@company.com" />
                </div>
                <div>
                    <label
                        for="password"
                        class="block mb-2 text-sm font-medium text-gray-900"
                        >비밀번호</label
                    >
                    <!-- {#if state == "visible"} -->
                    <label
                        for="password"
                        class="relative block mb-2 text-sm font-medium text-gray-900"
                    >
                        <Input type={inputType} placeholder="••••••••" />
                        {#if state == "visible"}
                            <button
                                class="absolute top-1/4 right-4 w-5 h-5"
                                on:click={toInvisible}
                                ><img src={Visible} alt="visible" /></button
                            >
                        {:else}
                            <button
                                class="absolute top-1/4 right-4 w-5 h-5"
                                on:click={toVisible}
                                ><img src={Invisible} alt="invisible" /></button
                            >
                        {/if}
                    </label>
                </div>
                <div class="pt-2">
                    <button
                        type="submit"
                        class="w-full text-white bg-blue-600 hover:bg-blue-700 focus:ring-4 focus:outline-none focus:ring-blue-300 font-medium rounded-lg text-sm px-5 py-2.5 text-center"
                        >Sign Up</button
                    >
                </div>
            </div>
        </div>
    </div>
</section>
