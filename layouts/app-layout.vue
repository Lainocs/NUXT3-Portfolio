<template>
    <div>
        <IncludesHeader />
        <slot></slot>
        <IncludesFooter />
    </div>
</template>

<script>
    export default {
        name: 'app-layout',
    }
</script>