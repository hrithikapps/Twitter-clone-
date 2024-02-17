<script>
  import {
    Bell,
    EnvelopeClosed,
    Home,
    MagnifyingGlass,
    Pencil1,
    Reader,
    ThickArrowLeft,
  } from "radix-icons-svelte";

  import { Button } from "$lib/components/ui/button";
  import * as Avatar from "$lib/components/ui/avatar";

  const sidebarOptions = [
    {
      icon: Home,
      title: "home",
      href: "/",
    },
    {
      icon: MagnifyingGlass,
      title: "explorer",
      href: "/",
    },
    {
      icon: Bell,
      title: "notification",
      href: "/",
    },
    {
      icon: EnvelopeClosed,
      title: "messages",
      href: "/",
    },
    {
      icon: Reader,
      title: "Lists",
      href: "/",
    },
    {
      icon: EnvelopeClosed,
      title: "communities",
      href: "/",
    },
    {
      icon: EnvelopeClosed,
      title: "premium",
      href: "/",
    },
    {
      icon: ThickArrowLeft,
      title: "logout",
      href: "/Login",
    },
  ];
</script>

<div
  class="px-3 md:flex-[0.2] h-screen md:px-2 border flex justify-between flex-col sticky z-10 top-0 left-0"
>
  <div class="mt-10">
    {#each sidebarOptions as { icon, title, href }}
      <a
        {href}
        class="flex gap-[22px] p-3 rounded-full w-fit hover:bg-white/10"
      >
        <svelte:component this={icon} class="w-7 h-7" />
        <p class="text-lg capitalize hidden md:inline-block pr-5">{title}</p>
      </a>
    {/each}
  </div>
  <Button class="md:py-6 md:w-full">
    <Pencil1 class="md:mr-2 h-4 w-4" />
    <span class="hidden md:inline">Post </span>
  </Button>

  <div class="flex gap-2 justify-center items-center">
    <Avatar.Root>
      <Avatar.Image src="./xLogo.svg"></Avatar.Image>
      <Avatar.Fallback>IN</Avatar.Fallback>
    </Avatar.Root>
    <div class="hidden md:inline-block">
      <p class="font-medium capitalize">Kumar Hrithik</p>
      <p class="text-gray-800">hrithikk2765@gmail.com</p>
    </div>
  </div>
</div>
