<template>
    <Head title="Register" />
    <BreezeValidationErrors class="mb-4" />
    <div class="min-h-screen bg-white flex">
        <div
            class="
                flex-1 flex flex-col
                justify-center
                py-12
                px-4
                sm:px-6
                lg:flex-none lg:px-20
                xl:px-24
            "
        >
            <div class="mx-auto w-full max-w-sm lg:w-96">
                <div>
                    <h1 class="text-3xl font-extrabold text-blue-800">
                        StatSports
                    </h1>
                    <h2 class="mt-6 text-2xl font-extrabold text-blue-800">
                        Create an account
                    </h2>
                    <p class="mt-2 text-sm text-gray-600">
                        Or if you already have one
                        {{ " " }}
                        <Link
                            :href="route('login')"
                            class="
                                font-bold
                                text-blue-800
                                hover:text-blue-600
                                transition-all
                                ease-in-out
                            "
                        >
                            Log in here
                        </Link>
                    </p>
                </div>

                <div class="mt-8">
                    <div>
                        <div>
                            <p class="text-sm font-medium text-gray-700">
                                Register with
                            </p>

                            <div class="mt-1 grid grid-cols-2 gap-2">
                                <div>
                                    <a
                                        href="#"
                                        class="
                                            w-full
                                            inline-flex
                                            justify-center
                                            py-2
                                            px-4
                                            border border-gray-300
                                            rounded-md
                                            shadow-sm
                                            bg-white
                                            text-sm
                                            font-medium
                                            text-gray-500
                                            hover:bg-gray-50
                                            transition-all
                                            ease-in-out
                                        "
                                    >
                                        <span class="sr-only"
                                            >Sign in with Facebook</span
                                        >
                                        <svg
                                            class="
                                                w-5
                                                h-5
                                                hover:fill-fb-main
                                                transition-all
                                                ease-in-out
                                            "
                                            aria-hidden="true"
                                            fill="currentColor"
                                            viewBox="0 0 20 20"
                                        >
                                            <path
                                                fill-rule="evenodd"
                                                d="M20 10c0-5.523-4.477-10-10-10S0 4.477 0 10c0 4.991 3.657 9.128 8.438 9.878v-6.987h-2.54V10h2.54V7.797c0-2.506 1.492-3.89 3.777-3.89 1.094 0 2.238.195 2.238.195v2.46h-1.26c-1.243 0-1.63.771-1.63 1.562V10h2.773l-.443 2.89h-2.33v6.988C16.343 19.128 20 14.991 20 10z"
                                                clip-rule="evenodd"
                                            />
                                        </svg>
                                    </a>
                                </div>

                                <div>
                                    <a
                                        href="#"
                                        class="
                                            w-full
                                            inline-flex
                                            justify-center
                                            py-2
                                            px-4
                                            border border-gray-300
                                            rounded-md
                                            shadow-sm
                                            bg-white
                                            text-sm
                                            font-medium
                                            text-gray-500
                                            hover:bg-gray-50
                                            transition-all
                                            ease-in-out
                                        "
                                    >
                                        <span class="sr-only"
                                            >Sign in with Twitter</span
                                        >
                                        <svg
                                            class="
                                                w-5
                                                h-5
                                                hover:fill-tw-main
                                                transition-all
                                                ease-in-out
                                            "
                                            aria-hidden="true"
                                            fill="currentColor"
                                            viewBox="0 0 20 20"
                                        >
                                            <path
                                                d="M6.29 18.251c7.547 0 11.675-6.253 11.675-11.675 0-.178 0-.355-.012-.53A8.348 8.348 0 0020 3.92a8.19 8.19 0 01-2.357.646 4.118 4.118 0 001.804-2.27 8.224 8.224 0 01-2.605.996 4.107 4.107 0 00-6.993 3.743 11.65 11.65 0 01-8.457-4.287 4.106 4.106 0 001.27 5.477A4.073 4.073 0 01.8 7.713v.052a4.105 4.105 0 003.292 4.022 4.095 4.095 0 01-1.853.07 4.108 4.108 0 003.834 2.85A8.233 8.233 0 010 16.407a11.616 11.616 0 006.29 1.84"
                                            />
                                        </svg>
                                    </a>
                                </div>
                            </div>
                        </div>

                        <div class="mt-6 relative">
                            <div
                                class="absolute inset-0 flex items-center"
                                aria-hidden="true"
                            >
                                <div class="w-full border-t border-gray-300" />
                            </div>
                            <div class="relative flex justify-center text-sm">
                                <span class="px-2 bg-white text-gray-500">
                                    Or continue with
                                </span>
                            </div>
                        </div>
                    </div>

                    <div class="mt-6">
                        <form @submit.prevent="submit" class="space-y-6">
                            <div>
                                <label
                                    for="name"
                                    class="
                                        block
                                        text-sm
                                        font-medium
                                        text-gray-700
                                    "
                                >
                                    Name
                                </label>
                                <div class="mt-1">
                                    <input
                                        id="name"
                                        name="name"
                                        type="text"
                                        autocomplete="name"
                                        required
                                        autofocus
                                        v-model="form.name"
                                        class="
                                            appearance-none
                                            block
                                            w-full
                                            px-3
                                            py-2
                                            border border-gray-300
                                            rounded-md
                                            shadow-sm
                                            placeholder-gray-400
                                            focus:outline-none
                                            focus:border-blue-800
                                            sm:text-sm
                                        "
                                    />
                                </div>
                            </div>
                            <div>
                                <label
                                    for="email"
                                    class="
                                        block
                                        text-sm
                                        font-medium
                                        text-gray-700
                                    "
                                >
                                    Email address
                                </label>
                                <div class="mt-1">
                                    <input
                                        id="email"
                                        name="email"
                                        type="email"
                                        autocomplete="username"
                                        v-model="form.email"
                                        required
                                        class="
                                            appearance-none
                                            block
                                            w-full
                                            px-3
                                            py-2
                                            border border-gray-300
                                            rounded-md
                                            shadow-sm
                                            placeholder-gray-400
                                            focus:outline-none
                                            focus:border-blue-800
                                            sm:text-sm
                                        "
                                    />
                                </div>
                            </div>

                            <div class="space-y-1">
                                <label
                                    for="password"
                                    class="
                                        block
                                        text-sm
                                        font-medium
                                        text-gray-700
                                    "
                                >
                                    Password
                                </label>
                                <div class="mt-1">
                                    <input
                                        id="password"
                                        name="password"
                                        type="password"
                                        autocomplete="new-password"
                                        v-model="form.password"
                                        required
                                        class="
                                            appearance-none
                                            block
                                            w-full
                                            px-3
                                            py-2
                                            border border-gray-300
                                            rounded-md
                                            shadow-sm
                                            placeholder-gray-400
                                            focus:border-blue-500
                                            sm:text-sm
                                        "
                                    />
                                </div>
                            </div>

                            <div class="space-y-1">
                                <label
                                    for="password_confirmation"
                                    class="
                                        block
                                        text-sm
                                        font-medium
                                        text-gray-700
                                    "
                                >
                                    Confirm Password
                                </label>
                                <div class="mt-1">
                                    <input
                                        id="password_confirmation"
                                        name="password_confirmation"
                                        type="password"
                                        autocomplete="new-password"
                                        v-model="form.password_confirmation"
                                        required
                                        class="
                                            appearance-none
                                            block
                                            w-full
                                            px-3
                                            py-2
                                            border border-gray-300
                                            rounded-md
                                            shadow-sm
                                            placeholder-gray-400
                                            focus:outline-none
                                            focus:border-blue-800
                                            sm:text-sm
                                        "
                                    />
                                </div>
                            </div>

                            <div class="flex items-center justify-between">
                                <div class="flex items-center">
                                    <input
                                        id="remember-me"
                                        name="remember-me"
                                        type="checkbox"
                                        class="
                                            h-4
                                            w-4
                                            text-blue-800
                                            border-gray-300
                                            rounded
                                            cursor-pointer
                                        "
                                    />
                                    <label
                                        for="remember-me"
                                        class="ml-2 block text-sm text-gray-900"
                                    >
                                        Remember me
                                    </label>
                                </div>

                                <div class="text-sm">
                                    <a
                                        href="#"
                                        class="
                                            font-bold
                                            text-blue-800
                                            hover:text-blue-600
                                            transition-all
                                            ease-in-out
                                        "
                                    >
                                        Forgot your password?
                                    </a>
                                </div>
                            </div>

                            <div>
                                <MainButton
                                    class="ml-4"
                                    :class="{ 'opacity-25': form.processing }"
                                    :disabled="form.processing"
                                >
                                    Create Account
                                </MainButton>
                            </div>
                        </form>
                    </div>
                </div>
            </div>
        </div>
        <div class="hidden lg:block relative w-0 flex-1">
            <img
                class="absolute inset-0 h-full w-full object-cover"
                src="../../../assets/stadium.jpg"
                alt=""
            />
        </div>
    </div>
</template>

<script>
import MainButton from "@/Components/Buttons/Button.vue";
import BreezeGuestLayout from "@/Layouts/Guest.vue";
import BreezeInput from "@/Components/Input.vue";
import BreezeLabel from "@/Components/Label.vue";
import BreezeValidationErrors from "@/Components/ValidationErrors.vue";
import { Head, Link } from "@inertiajs/inertia-vue3";

export default {
    layout: BreezeGuestLayout,

    components: {
        MainButton,
        BreezeInput,
        BreezeLabel,
        BreezeValidationErrors,
        Head,
        Link,
    },

    data() {
        return {
            form: this.$inertia.form({
                name: "",
                email: "",
                password: "",
                password_confirmation: "",
                terms: false,
            }),
        };
    },

    methods: {
        submit() {
            this.form.post(this.route("register"), {
                onFinish: () =>
                    this.form.reset("password", "password_confirmation"),
            });
        },
    },
};
</script>
