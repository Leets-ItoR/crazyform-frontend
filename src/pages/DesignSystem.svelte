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
        <div>
            <p class="text-2xl font-medium mb-2 col-span-1">Buttons</p>
            <p class="text-gray-500">일반적으로 사용하는 버튼입니다.</p>
        </div>

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
    <div class="my-20 grid grid-cols-3">
        <div>
            <p class="text-2xl font-medium mb-2 col-span-1">Typography</p>
            <p class="text-gray-500">서비스에서 사용하는 텍스트입니다.</p>
        </div>

        <div class="col-span-2">
            <table class="text-center w-full">
                <thead>
                    <tr>
                        <th style="width:20%" />
                        <th style="width:20%" class="font-semibold">Semibold</th
                        >
                        <th style="width:20%" class="font-medium">Medium</th>
                        <th style="width:20%" class="font-normal">Normal</th>
                        <th style="width:20%" class="font-light">Light</th>
                    </tr>
                </thead>
                <tbody>
                    <tr>
                        <td class="py-4 text-center text-4xl">4xl</td>
                        <td class="text-center text-4xl font-semibold">Leets</td
                        >
                        <td class="text-center text-4xl font-medium">Leets</td>
                        <td class="text-center text-4xl font-normal">Leets</td>
                        <td class="text-center text-4xl font-light">Leets</td>
                    </tr>

                    <tr>
                        <td class="py-4 text-center text-3xl">3xl</td>
                        <td class="text-center text-3xl font-semibold">Leets</td
                        >
                        <td class="text-center text-3xl font-medium">Leets</td>
                        <td class="text-center text-3xl font-normal">Leets</td>
                        <td class="text-center text-3xl font-light">Leets</td>
                    </tr>
                    <tr>
                        <td class="py-4 text-center text-xl">xl</td>
                        <td class="text-center text-xl font-semibold">Leets</td>
                        <td class="text-center text-xl font-medium">Leets</td>
                        <td class="text-center text-xl font-normal">Leets</td>
                        <td class="text-center text-xl font-light">Leets</td>
                    </tr>
                    <tr>
                        <td class="py-4 text-center text-lg">lg</td>
                        <td class="text-center text-lg font-semibold">Leets</td>
                        <td class="text-center text-lg font-medium">Leets</td>
                        <td class="text-center text-lg font-normal">Leets</td>
                        <td class="text-center text-lg font-light">Leets</td>
                    </tr>
                    <tr>
                        <td class="py-4 text-center">Base</td>
                        <td class="text-center text-base font-semibold"
                            >Leets</td
                        >
                        <td class="text-center text-base font-medium">Leets</td>
                        <td class="text-center text-base font-normal">Leets</td>
                        <td class="text-center text-base font-light">Leets</td>
                    </tr>
                    <tr>
                        <td class="py-4 text-center text-sm">sm</td>
                        <td class="text-center text-sm font-semibold">Leets</td>
                        <td class="text-center text-sm font-medium">Leets</td>
                        <td class="text-center text-sm font-normal">Leets</td>
                        <td class="text-center text-sm font-light">Leets</td>
                    </tr>
                    <tr>
                        <td class="py-4 text-center text-xs">xs</td>
                        <td class="text-center text-xs font-semibold">Leets</td>
                        <td class="text-center text-xs font-medium">Leets</td>
                        <td class="text-center text-xs font-normal">Leets</td>
                        <td class="text-center text-xs font-light">Leets</td>
                    </tr>
                </tbody>
            </table>
        </div>
    </div>
    <div class="my-10">
        <p class="text-2xl font-medium mb-4">Inputs</p>

        <div class="grid grid-cols-4 gap-4">
            <TextInput />
            <EmailInput />
            <PasswordInput />
        </div>
    </div>
</div>
