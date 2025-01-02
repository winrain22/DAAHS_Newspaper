<script lang="ts">
    import { Button } from "$lib/components/ui/button";
    import * as Card from "$lib/components/ui/card/index.js";
</script>

<style>
    :global(body) {
        background: url("/background.png");
    }
</style>

<div class="h-screen flex justify-center items-center">
    <img src="/guardianne-logo-big.png" alt="Guardianne Logo" class="max-h-full md:h-full" />
</div>

<!-- Latest issues & highlights -->
<div class="grid md:grid-cols-2 gap-2 p-4">
    <Card.Root>
        <Card.Header class="flex justify-between flex-row">
            <div>
                <Card.Title>Our Latest Issue</Card.Title>
                <Card.Description>See what we have in store!</Card.Description>
            </div>
            <div class="text-right">
                <Button variant="outline" class="mb-1">Go to Archive</Button>
                <Button>Read</Button>
            </div>
        </Card.Header>
        <Card.Content>
            <img alt="Issue two cover" src="/issue2.png" class="rounded-lg" />
        </Card.Content>
    </Card.Root>
    <Card.Root>
        <Card.Header class="flex justify-between flex-row">
            <div>
                <Card.Title>Daily Howl</Card.Title>
                <Card.Description>See what we have in store!</Card.Description>
            </div>
            <div class="text-right">
                <Button>Open</Button>
            </div>
        </Card.Header>
        <Card.Content>
            <img alt="Issue two cover" src="/issue2.png" class="rounded-lg" />
        </Card.Content>
    </Card.Root>
</div>
