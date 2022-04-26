<script setup lang="ts">

const TYPER_VALUES: string[] = [
    'Web', 'Kotlin', 'Stonks™',
    'JS', 'PHP', 'Go', 'Cool',
    'Bad', 'Cheat', 'HTML', 'CSS',
    'Rust'
]

</script>
<template>
    <div>
        <ClientOnly>
            <Typer :values="TYPER_VALUES" :duration="2000"/>
        </ClientOnly>
    </div>
</template>
