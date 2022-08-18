<script>
    import '@htmlplus/core/dialog-content'

    export let scrollable = false
</script>

<plus-dialog-content {scrollable}>
    <slot/>
</plus-dialog-content>