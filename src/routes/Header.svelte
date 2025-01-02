<script lang="ts">
    import VanishingHeader from "./VanishingHeader.svelte";
    import { page } from "$app/stores";
    import { Button, buttonVariants } from "$lib/components/ui/button";
    import Menu from "lucide-svelte/icons/menu";
    import * as Sheet from "$lib/components/ui/sheet";

    let pages = [
        { name: "Home", href: "/" },
        { name: "About", href: "/about-us" },
        { name: "Gallery", href: "/gallery" },
        { name: "Archive", href: "/archive" },
        { name: "Feedback", href: "/feedback" },
    ];

    let activePageHref = $derived($page.url.pathname);
</script>

<VanishingHeader>
    <header class="sticky top-0 p-4 border-b border-border bg-anne-blue">
        <div class="container max-w-screen-2xl flex items-center justify-between">
            <a href="/" class="text-xl font-bold"
                ><img src="/white-logo.png" alt="The Guardianne" class="h-8" /></a
            >
            <Sheet.Root>
                <Sheet.Trigger
                    class="md:hidden {buttonVariants({
                        size: "icon",
                        variant: "secondary"
                    })}"
                >
                    <Menu />
                </Sheet.Trigger>
    
                <Sheet.Content class="bg-anne-blue border-anne-blue/30">
                    <Sheet.Header>
                        <Sheet.Title
                            ><img
                                src="/white-logo.png"
                                alt="The Guardianne"
                                class="h-8"
                            /></Sheet.Title
                        >
                    </Sheet.Header>
                    <div class="mt-3">
                        {#each pages as page}
                            <a
                                href={page.href}
                                class="hover:text-anne-tan text-white transition-colors text-xl font-medium {activePageHref ===
                                page.href
                                    ? 'underline'
                                    : ''}">{page.name}</a
                            >
                            <br />
                        {/each}
                    </div>
                </Sheet.Content>
            </Sheet.Root>
            <div class="ml-2 gap-3 mt-2 hidden md:flex">
                {#each pages as page}
                    <a
                        href={page.href}
                        class="text-white hover:text-anne-tan transition-colors font-medium {activePageHref ===
                        page.href
                            ? 'underline'
                            : ''}">{page.name}</a
                    >
                {/each}
            </div>
        </div>
    </header>    
</VanishingHeader>