<script lang="ts">
    import { Button } from "$lib/components/ui/button";
    import * as Card from "$lib/components/ui/card/index.js";
</script>

<!-- our mission banner -->
<div
    class="w-full flex justify-center bg-fixed h-[60vh] bg-no-repeat bg-cover bg-black/55 text-white"
    style="background-image:url(/bg.png); background-blend-mode: darken; background-position-x: center; background-position-y: bottom;"
>
    <div class="w-full h-full text-center mt-6 p-2">
        <h1 class="text-4xl">Our Mission</h1>
        <br />
        <p>
            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vivamus
            diam nibh, pharetra nec velit a, finibus ultricies eros. Vestibulum
            ante ex, volutpat quis maximus sit amet, porta et leo. Sed mattis,
            sapien id euismod rhoncus, felis nunc maximus lorem, vitae suscipit
            justo libero quis nunc. Fusce feugiat quam enim, eu blandit justo
            bibendum interdum. Fusce id tellus efficitur, dignissim ipsum at,
            pretium erat. Aenean velit dolor, pharetra eget elit quis, cursus
            efficitur turpis. Mauris tempus mollis neque, vitae porta dolor
            accumsan eu. Nullam eu nibh ex. Phasellus volutpat metus mauris.
        </p>
    </div>
</div>

<!-- Latest issues & highlights -->
<div class="grid md:grid-cols-2 gap-2 p-4">
    <Card.Root>
        <Card.Header class="flex justify-between flex-row">
            <div>
                <Card.Title>Our Latest Issue</Card.Title>
                <Card.Description>See what we have in store!</Card.Description>
            </div>
            <div>
                <Button variant="outline">Go to Archive</Button>
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
            <div>
                <Button variant="outline">Go to Archive</Button>
                <Button>Read</Button>
            </div>
        </Card.Header>
        <Card.Content>
            <img alt="Issue two cover" src="/issue2.png" class="rounded-lg" />
        </Card.Content>
    </Card.Root>
</div>
