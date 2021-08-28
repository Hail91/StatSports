<template>
    <button
        :type="type"
        class="
            inline-flex
            items-center
            px-4
            py-2
            border border-transparent
            text-sm
            font-medium
            rounded-md
            shadow-sm
            text-white
            bg-blue-800
            hover:bg-blue-600
            focus:outline-none
            transition-all
            ease-in-out
        "
    >
        <slot></slot>
    </button>
</template>

<script>
export default {
    props: {
        type: {
            type: String,
            default: "submit",
        },
    },
};
</script>
