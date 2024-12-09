<script lang="ts">
    import { page } from "$app/stores";

    let pages = [
        { name: "Home", href: "/" },
        { name: "About", href: "/about-us" },
        { name: "Gallery", href: "/gallery" },
        { name: "Archive", href: "/archive" },
        { name: "Feedback", href: "/feedback" },
    ];

    let activePageHref = $derived($page.url.pathname);
</script>

<header class="sticky top-0 p-4 border-b border-border">
    <div class="container max-w-screen-2xl flex items-center justify-between">
        <a href="/" class="text-xl font-bold"
            ><img src="/logo.png" alt="The Guardianne" class="h-8" /></a
        >
        <div class="ml-2 flex gap-3 mt-2">
            {#each pages as page}
                <a
                    href={page.href}
                    class="hover:text-black transition-colors text-lg font-medium text-muted-foreground {activePageHref ===
                    page.href
                        ? 'underline text-black'
                        : ''}">{page.name}</a
                >
            {/each}
        </div>
    </div>
</header>
