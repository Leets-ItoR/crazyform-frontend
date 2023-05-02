<script>
    import logo from "../assets/leets.png";

    // Buttons
    import AcceptBtn from "../components/button/Accept.svelte";
    import DenyBtn from "../components/button/Deny.svelte";
    import DisabledBtn from "../components/button/Disabled.svelte";
    import LoadingBtn from "../components/button/Loading.svelte";

    //inputs
    import TextInput from "../components/input/Text.svelte";
    import EmailInput from "../components/input/Email.svelte";
    import PasswordInput from "../components/input/Password.svelte";
</script>

<div class="max-w-5xl mx-auto mt-20">
    <div class="flex items-center gap-6">
        <img src={logo} class="h-6 sm:h-9" alt="ItoR Logo" />
        <p class="text-4xl font-semibold">Design System</p>
    </div>

    <div class="my-10 grid grid-cols-3">
        <div class="" />
        <p class="text-2xl font-medium mb-4 col-span-1">Buttons</p>
        <div class="grid grid-cols-4 gap-4 col-span-2">
            <AcceptBtn />
            <DenyBtn />
            <DisabledBtn />
            <LoadingBtn />
        </div>
    </div>
    <div class="my-10">
        <p class="text-2xl font-medium mb-4">Input</p>

        <div class="grid grid-cols-4 gap-4">
            <TextInput />
            <EmailInput />
            <PasswordInput />
        </div>
    </div>
</div>
