<script setup lang="ts">
import { computed, ref } from "#imports";

/**
 * Typing for the properties this component
 * accepts.
 */
interface Properties {
    // The text values to cycle between
    values: string[],
    // The duration to display each value for
    duration: number
}

// Using the properties
const { values, duration } = defineProps<Properties>();

// Whether we are deleting the text
let deleting = false;
// The current index of the text in the values array
let index = 0;

const value = ref('');
const complete = computed<boolean>(() => values[index] == value.value)

/**
 * Updates the currently displayed value.
 */
function update() {
    // retrieve the unmodified original text
    const originalValue: string = values[index];
    // The delay before executing the next update
    let delay: number = 300 - Math.random() * 100;
    let newValue: string;
    if (deleting) {
        // Slice the string at one char shorter
        newValue = originalValue.substring(0, value.value.length - 1);
        if (newValue.length == 0) {
            deleting = false;
            if (index + 1 >= values.length) {
                index = 0;
            } else {
                index++
            }
            delay = 500;
        } else {
            delay = (300 - Math.random() * 100) / 2;
        }
    } else {
        // Add another letter from the original value
        newValue = originalValue.substring(0, value.value.length + 1);
        if (newValue == originalValue) {
            delay = duration;
            deleting = true;
        } else {
            delay = 300 - Math.random() * 100;
        }
    }
    // Update the UI value
    value.value = newValue;
    // Execute the next update after the delay
    setTimeout(update, delay);
}

// Execute the first update
update();
</script>
<template>
    <span :class="{typer: true, 'typer--caret': !complete}">{{ value }}</span>
</template>
<style scoped lang="scss">
.typer {
    position: relative;
    margin-right: 4px;
}

.typer--caret::after {
    content: "";
    position: absolute;
    right: -4px;
    width: 2px;
    height: 100%;
    background: currentColor;
    animation: cursor-blink 500ms 500ms infinite;
}

@keyframes cursor-blink {
    0%, 100% {
        opacity: 1;
    }
    50% {
        opacity: 0;
    }
}
</style>