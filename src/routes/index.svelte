<script>
    import {Dialog, DialogToggler, DialogHeader, DialogBody, DialogContent, DialogFooter} from '$lib/components'
import Counter from '../lib/components/Counter.svelte';

    let open = false;

    $: console.log('open: ', open)
</script>

<DialogToggler connector="dialog-default">Toggler</DialogToggler>
<Dialog open animation="fade" on:close={console.log} connector="dialog-default">
    <DialogContent>
        <DialogHeader>Header</DialogHeader>

    <DialogBody>
        <Counter/>
        Dialog Body
    </DialogBody>
    <DialogFooter>
        <DialogToggler connector="dialog-default"></DialogToggler>
    </DialogFooter>

</DialogContent>
</Dialog>