<script>
    import Logo from "../components/Icon.svelte";
    import Input from "../components/input/Text.svelte";

    let email = "",
        password = "";

    $: submit = async () => {
        console.log(email, password);
        await axios.post("http://13.209.44.41:8080/user/login", {
            email,
            password,
        });
        await push("/");
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
                    class="flex justify-center text-xl font-bold leading-tight tracking-tight text-gray-900 md:text-2xl"
                >
                    이메일 주소를 인증해주세요.
                </h1>
                <h3 class="flex justify-center">
                    이메일 인증을 위한 메일이 발송되었습니다.
                    <br />
                    회원가입을 위한 이메일 인증을 진행해주세요.
                </h3>
                <div>
                    <label
                        for="email"
                        class="block mb-2 ml-2 text-sm font-medium text-gray-900"
                        >인증코드</label
                    >
                    <Input type="email" placeholder="인증코드를 입력하세요." />
                </div>
                <div class="pt-2">
                    <button
                        type="submit"
                        class="w-full text-white bg-blue-600 hover:bg-blue-700 focus:ring-4 focus:outline-none focus:ring-blue-300 font-medium rounded-lg text-sm px-5 py-2.5 text-center"
                        >이메일 인증하기</button
                    >
                </div>
            </div>
        </div>
        <div class="flex items-center justify-between gap-3 mt-4">
            <a
                href="/"
                class="text-sm font-medium text-gray-600 hover:underline"
                >비밀번호 찾기</a
            ><span class="font-light text-sm text-gray-300">|</span><a
                href="/signup"
                class="text-sm font-medium text-gray-600 hover:underline"
                >이메일 재전송</a
            >
        </div>
    </div>
</section>
