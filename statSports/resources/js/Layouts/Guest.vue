<template>
    <div
        class="
            min-h-screen
            flex flex-col
            sm:justify-center
            items-center
            pt-6
            sm:pt-0
            bg-gray-100
        "
    >
        <div class="w-full bg-white shadow-md overflow-hidden sm:rounded-lg">
            <slot />
        </div>
    </div>
</template>

<script>
import { Link } from "@inertiajs/inertia-vue3";

export default {
    components: {
        Link,
    },
};
</script>
