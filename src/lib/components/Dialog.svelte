<script>
    import '@htmlplus/core/dialog'
import { createEventDispatcher } from 'svelte';

    export let connector;
    export let animation;
    export let sticky;
    export let size;
    export let scrollable;
    export let portalTarget;
    export let portalStrategy;
    export let placement;
    export let portal;
    export let open;
    export let persistent;
    export let fullscreen;
    export let keyboard;
    export let fullWidth;
    export let fullHeight;
    export let backdrop;

    const dispatch = createEventDispatcher()

    function onClose() {
        dispatch('close')
        open = false
    }
    function onClosed() {
        dispatch('closed')
    }    
    function onOpen() {
        dispatch('open')
        open = true;
    }    
    function onOpened() {
        dispatch('opened')
    }
</script>

<plus-dialog {backdrop} full-height={fullHeight} {placement} {open} {keyboard} {persistent} {sticky} {size} {scrollable}  full-width={fullWidth} {fullscreen} {portal} portal-strategy={portalStrategy} portal-target={portalTarget} on:plusClose={onClose} on:plusClosed={onClosed} on:plusOpen={onOpen} on:plusOpened={onOpened} {animation} {connector}>
    <slot/>
</plus-dialog>