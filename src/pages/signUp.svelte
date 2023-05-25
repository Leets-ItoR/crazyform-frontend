<script>
    import Logo from "../components/Icon.svelte";
    import Input from "../components/input/Text.svelte";
    import Visible from "../assets/visible.png";
    import Invisible from "../assets/invisible.png";
    import Warning from "../assets/warning.png";
    import axios from "axios";
    import { pop } from "svelte-spa-router";

    // make visible password or not.
    let state = "invisible";
    let inputType = "password";
    const toVisible = () => {
        state = "visible";
        inputType = "text";
    };
    const toInvisible = () => {
        state = "invisible";
        inputType = "password";
    };

    // register
    let name = "",
        email = "",
        password = "";
    let warningMsg = "";
    let warningFlag = false;

    const checkValid = async () => {
        console.log(name, email, password);
        warningFlag = true;
        // 닉네임, 이메일, 비밀번호가 입력이 안되었을 떄
        if (name == "" || email == "" || password == "") {
            if (name == "") throw new Error("닉네임을 입력해주세요.");
            else if (email == "") throw new Error("Email을 입력해주세요.");
            else throw new Error("비밀번호를 입력해주세요.");
        } else {
            const nameReg = /[^0-9A-Za-z]/g;
            const emailReg =
                /^[0-9a-zA-Z]([-_\.]?[0-9a-zA-Z])*@[0-9a-zA-Z]([-_\.]?[0-9a-zA-Z])*\.[a-zA-Z]{2,3}$/i;
            const passwordReg = /^[0-9A-Za-z]/;
            // 닉네임의 길이가 3 미만 10 초과일 때
            if (name.length < 3 || name.length > 10) {
                throw new Error("닉네임은 3 ~ 10 문자로 입력해주세요.");
            }
            // 닉네임에 특수문자가 들어갈 때
            else if (nameReg.test(name)) {
                throw new Error("닉네임은 특수문자가 포함될 수 없습니다.");
            }
            // 이메일 형식이 맞지 않을 때
            else if (!emailReg.test(email)) {
                throw new Error("Email 형식이 올바르지 않습니다.");
            }
            // 비밀번호 길이가 4 미만 15 초과일 때
            else if (password.length < 4 || password.length > 15) {
                throw new Error("비밀번호는 4 ~ 15 문자로 입력해주세요.");
            }
            // 비밀번호가 영어나 숫자로 시작하지 않을 때
            else if (!passwordReg.test(password)) {
                throw new Error("비밀번호는 영어나 숫자로 시작해야 합니다.");
            }
            // 모든 유효성검사가 끝나고, 정보를 벡엔드로 전달
            else {
                warningFlag = false;
                await axios
                    .post("http://13.209.44.41:8080/user/signup", {
                        nickname: name,
                        email: email,
                        password: password,
                    })
                    .then(() => {
                        alert("회원가입이 완료되었습니다.");
                        pop(); // 로그인 페이지로 돌아가기
                    })
                    .catch((e) => {
                        alert("이미 가입된 유저입니다.");
                    });
            }
        }
    };

    $: submit = async () => {
        await checkValid().catch((e) => {
            warningMsg = e.message;
        });
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
                <form
                    on:submit|preventDefault={submit}
                    class="flex flex-col gap-4"
                >
                    <h1
                        class="text-xl font-bold leading-tight tracking-tight text-gray-900 md:text-2xl"
                    >
                        회원가입
                    </h1>
                    {#if warningFlag}
                        <h3 class="flex bg-amber-100 p-2 rounded-lg">
                            <img
                                src={Warning}
                                alt="warning"
                                class="w-5 h-5 mr-2 ml-2"
                            />{warningMsg}
                        </h3>
                    {/if}
                    <div>
                        <label
                            for="name"
                            class="block mb-2 text-sm font-medium text-gray-900"
                            >닉네임</label
                        >
                        <Input
                            bind:value={name}
                            type="text"
                            placeholder="ItoR"
                            id="nickname"
                        />
                    </div>
                    <div>
                        <label
                            for="email"
                            class="block mb-2 text-sm font-medium text-gray-900"
                            >이메일</label
                        >
                        <Input
                            bind:value={email}
                            type="email"
                            placeholder="name@company.com"
                            id="email"
                        />
                    </div>
                    <div>
                        <label
                            for="password"
                            class="block mb-2 text-sm font-medium text-gray-900"
                            >비밀번호</label
                        >
                        <label
                            for="password"
                            class="relative block mb-2 text-sm font-medium text-gray-900"
                        >
                            <Input
                                bind:value={password}
                                type={inputType}
                                placeholder="••••••••"
                                id="password"
                            />
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
                                    ><img
                                        src={Invisible}
                                        alt="invisible"
                                    /></button
                                >
                            {/if}
                        </label>
                    </div>
                    <div class="pt-2">
                        <a href="/login">
                            <button
                                class="w-full text-white bg-blue-600 hover:bg-blue-700 focus:ring-4 focus:outline-none focus:ring-blue-300 font-medium rounded-lg text-sm px-5 py-2.5 text-center"
                                >회원가입</button
                            >
                        </a>
                    </div>
                </form>
            </div>
        </div>
    </div>
</section>
