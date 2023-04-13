<template>
<a 
    class="nav-link" 
    :class="activeClasses"
    aria-current="page" 
    :href="page.link.url"
    :title="`This link goes to the ${page.link.text} page.`"
>{{ page.link.text }}</a>
</template>

<script>
export default {
    props: ['page', 'isActive'],
    computed: {
        activeClasses() {
            return {
                active: this.isActive,
                emphasise: this.isActive
            }
        }
    }
}
</script>

<!-- If you put scoped at the end of style it limits it to the component it is in -->

<style scoped>
.emphasise {
    text-decoration: underline !important;
}
</style>