<script>
    import Step from '../../components/Step.svelte';

   let steps = [
       {
           name: "Lost & Found",
           icon: "fa-solid fa-person-circle-question",
           description:
               "Lost & Found is a user friendly system that helps people to recover their lost and found items or things that are valuable to them.",
       },
       {
           name: "Anime Info",
           icon: "fa-solid fa-book-journal-whills",
           description:
               "This is an HTML file that explains the description and history of an anime to society. It also explains why the anime matters and recommends a few anime for you to watch."
       },
       {
           name: "Profile Navigation",
           icon: "fa-solid fa-street-view",
           description:
               "Profile Navigation is a project that navigates a specific profile by clicking a photo of a certain person. The profile consists of the info of a certain person.",
       },
   ];
</script>

<main class="flex flex-col flex-1 p-4">
   <section class="py-20 lg:py-32 flex flex-col gap-12 sm:gap-16 lg:gap-24" id="portfolio">
       <div class="flex flex-col gap-2 text-center">
           <h6 class="text-base sm:text-xl md:text-2xl">
               A few of my creative endeavors.
           </h6>
           <h3 class="font-semibold text-2xl sm:text-4xl md:text-5xl">
               Curious to <span class="poppins text-violet-400">see</span> my work?
           </h3>
       </div>

       <a
           href="https://www.youtube.com/watch?v=L_jWHffIx5E"
           target="_blank"
           class="mx-auto px-4 py-2 rounded-md border border-solid border-white flex items-center gap-2 sm:mb-0 -mb-4 -mt-10 hover:border-violet-700 duration-200"
       >
           <i class="fa-regular fa-circle-play" />
           <p>Watch the video</p>
       </a>

       <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-8 sm:gap-10 lg:gap-12">
           <Step step={steps[0]}>
               <div class="flex flex-col items-center text-center">
                   <img src="images/lnf.png" alt="Lost & Found Image" class="object-cover rounded-lg w-full max-h-64 sm:max-h-72 lg:max-h-[70vh]" />
                   <p class="mt-4">
                       Lost & Found is a user-friendly system that helps people to recover their lost and found items or things that are valuable to them.
                   </p>
               </div>
           </Step>

           <Step step={steps[1]}>
               <div class="flex flex-col items-center text-center">
                   <img src="images/anime.png" alt="Anime Image" class="object-cover rounded-lg w-full max-h-64 sm:max-h-72 lg:max-h-[70vh]" />
                   <p class="mt-4">
                       This is an HTML file that explains the description and history of an anime to society. It also explains why the anime matters and recommends a few anime for you to watch.
                   </p>
               </div>
           </Step>

           <Step step={steps[2]}>
               <div class="flex flex-col items-center text-center">
                   <img src="images/navi.png" alt="Profile Navigation Image" class="object-cover rounded-lg w-full max-h-64 sm:max-h-72 lg:max-h-[70vh]" />
                   <p class="mt-4">
                       Profile Navigation is a project that navigates a specific profile by clicking a photo of a certain person. The profile consists of the info of a certain person.
                   </p>
               </div>
           </Step>
       </div>
   </section>
</main>
