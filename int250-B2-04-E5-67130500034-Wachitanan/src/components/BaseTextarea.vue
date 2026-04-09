<script setup>
import { computed } from "vue"

const props = defineProps({
    label: String,
    type: String,
    desc: String,
    modelValue: String,
    error: String
})

const emit = defineEmits(["update:modelValue"])

const maxLength = 200

const count = computed(() => props.modelValue?.length || 0)

const counterColor = computed(() => {
    if (count.value >= maxLength) return "text-red-500"
    if (count.value >= 180) return "text-orange-500"
    return "text-gray-400"
})
</script>

<template>
    <div class="flex flex-col space-y-2">
        <label class="font-semibold">{{ label }}</label>

        <textarea
            :placeholder="desc"
            :value="modelValue"
            maxlength="200"
            @input="emit('update:modelValue', $event.target.value)"
            :class="[
                'border rounded-md py-1 px-3 h-32',
                error ? 'border-red-500' : 'border-gray-300'
            ]"
        ></textarea>

        <div class="flex justify-between text-sm">
            <p class="text-gray-400">
                Optional: briefly describe your interests or previous experience.
            </p>
            <span :class="counterColor">
                {{ count }}/{{ maxLength }}
            </span>
        </div>

        <p v-if="error" class="text-red-500 text-sm">
            {{ error }}
        </p>
    </div>
</template>

<style scoped></style>