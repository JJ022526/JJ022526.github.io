<script lang="ts">
    export let y: number;

    interface Tab {
        name: string;
        link: string;
    }

    export let tabs: Tab[] = [
        { name: "Portfolio ", link: "#portfolio" },
        { name: "About", link: "#about" },
        { name: "Contact", link: "#contact" }
    ];
</script>


<header
    class={"sticky z-[10] top-0 duration-200 px-6 flex items-center justify-between border-b border-solid " +
        (y > 0
            ? " py-4 bg-slate-950 border-violet-950"
            : " py-6 bg-transparent border-transparent")}
>
<h1 class="font-medium">
    <a href="#home" on:click={(e) => { e.preventDefault(); window.scrollTo({ top: 0, behavior: 'smooth' }) }} class="font-bold poppins text-white hover:text-violet-400">
        Justine Jhess
    </a> 
    <span>Domenden</span>
</h1>


    <div class="sm:flex items-center gap-4 hidden">
        {#each tabs as tab, index}
            <a
                href={tab.link}
                class="duration-200 hover:text-violet-400"
                target={index === 3 ? "_blank" : ""}
            >
                <p>{tab.name}</p>
            </a>
        {/each}
       
    </div>
</header>
