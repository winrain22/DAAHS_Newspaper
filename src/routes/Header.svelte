<script lang="ts">
    let pages = [
        { name: "Home", href: "/" },
        { name: "About", href: "/about-us" },
        { name: "Gallery", href: "/gallery" },
    ];
</script>

<header class="sticky top-0 p-4 border-b border-border">
    <div class="container max-w-screen-2xl flex items-center">
        <div class="flex items-center gap-2">
            <a href="/" class="text-xl font-bold">Guardianne</a>
            <div class="ml-2 flex gap-2">
                {#each pages as page}
                    <a
                        href={page.href}
                        class="text-lg font-medium text-muted-foreground"
                        >{page.name}</a
                    >
                {/each}
            </div>
        </div>
    </div>
</header>
