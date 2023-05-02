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

<div class="max-w-7xl mx-auto mt-20">
    <div class="flex items-center gap-6">
        <img src={logo} class="h-6 sm:h-9" alt="ItoR Logo" />
        <p class="text-4xl font-semibold">Design System</p>
    </div>

    <div class="my-20 grid grid-cols-3">
        <div><p class="text-2xl font-medium mb-4 col-span-1">Buttons</p></div>

        <div class="col-span-2">
            <table class="text-center w-full">
                <thead>
                    <tr>
                        <th style="width:20%" />
                        <th style="width:16%">Tiny</th>
                        <th style="width:16%">Small</th>
                        <th style="width:16%">Base</th>
                        <th style="width:16%">Large</th>
                        <th style="width:16%">Big</th>
                    </tr>
                </thead>
                <tbody>
                    <tr>
                        <td class="text-center py-3 px-1">Accept</td>
                        <td class="text-center py-3 px-1"
                            ><AcceptBtn size="tiny" /></td
                        >
                        <td class="text-center py-3 px-1"
                            ><AcceptBtn size="small" /></td
                        >
                        <td class="text-center py-3 px-1"
                            ><AcceptBtn size="base" /></td
                        >
                        <td class="text-center py-3 px-1"
                            ><AcceptBtn size="large" /></td
                        >
                        <td class="text-center py-3 px-1"
                            ><AcceptBtn size="big" /></td
                        >
                    </tr>
                    <tr>
                        <td class="text-center py-3 px-1">Deny</td>
                        <td class="text-center py-3 px-1"
                            ><DenyBtn size="tiny" /></td
                        >
                        <td class="text-center py-3 px-1"
                            ><DenyBtn size="small" /></td
                        >
                        <td class="text-center py-3 px-1"
                            ><DenyBtn size="base" /></td
                        >
                        <td class="text-center py-3 px-1"
                            ><DenyBtn size="large" /></td
                        >
                        <td class="text-center py-3 px-1"
                            ><DenyBtn size="big" /></td
                        >
                    </tr>
                    <tr>
                        <td class="text-center py-3 px-1">Disabled</td>
                        <td class="text-center py-3 px-1"
                            ><DisabledBtn size="tiny" /></td
                        >
                        <td class="text-center py-3 px-1"
                            ><DisabledBtn size="small" /></td
                        >
                        <td class="text-center py-3 px-1"
                            ><DisabledBtn size="base" /></td
                        >
                        <td class="text-center py-3 px-1"
                            ><DisabledBtn size="large" /></td
                        >
                        <td class="text-center py-3 px-1"
                            ><DisabledBtn size="big" /></td
                        >
                    </tr>
                    <tr>
                        <td class="text-center py-3 px-1">Loading</td>
                        <td class="text-center py-3 px-1"
                            ><LoadingBtn size="tiny" /></td
                        >
                        <td class="text-center py-3 px-1"
                            ><LoadingBtn size="small" /></td
                        >
                        <td class="text-center py-3 px-1"
                            ><LoadingBtn size="base" /></td
                        >
                        <td class="text-center py-3 px-1"
                            ><LoadingBtn size="large" /></td
                        >
                        <td class="text-center py-3 px-1"
                            ><LoadingBtn size="big" /></td
                        >
                    </tr>
                </tbody>
            </table>
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
