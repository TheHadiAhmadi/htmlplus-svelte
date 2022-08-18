<script>
    import {Dialog, DialogToggler, DialogHeader, DialogBody, DialogContent, DialogFooter} from '$lib/components'

    let open = false;

    $: console.log('open: ', open)
</script>

<DialogToggler connector="dialog-default">Toggler</DialogToggler>
<Dialog open animation="fade" on:close={console.log} connector="dialog-default">
    <DialogContent>
        <DialogHeader>Header</DialogHeader>

    <DialogBody>
        Dialog Body
    </DialogBody>
    <DialogFooter>
        <DialogToggler connector="dialog-default"></DialogToggler>
    </DialogFooter>

</DialogContent>
</Dialog>