
<svelte:head>
	<title>Our Team | Wendorf Beward & Partners</title>
	<meta name="description" content="Our Team | Wendorf Beward & Partners" />
</svelte:head>

<script>
    import { onMount } from 'svelte';
  
    let dialogTom, dialogNancy, dialogLarry, dialogSuzanne;
  
    function openDialog(dialog) {
      dialog.showModal();
    }
  
    function closeDialog(dialog) {
      dialog.close();
    }
  
    onMount(() => {
      // You can perform additional setup here if needed
    });
  </script>


<div class="py-5 top-of-page-section-white">
    <div class="container">

        <div class="row mb-3 justify-content-center">
            <div class="col-12 align-items-center d-flex justify-content-center">
                <div class="text-center">
                    <h1 class="pb-5">
                        About Wendorf Beward &amp; Partners                
                    </h1>
                </div>
            </div>
        </div>

        <div class="row mb-3 justify-content-center">
            <div class="col-12">
                <p>Wendorf Beward &amp; Partners have significant background in delivery of public services and programs through a combination of over 60 years of working in the industry. Wendorf Beward & Partners approach to service delivery is to bring the best resources to the assignment.</p>
                <p>Our partnering approach includes the client and subconsultants. Continuous attention to client approved scope, budget and schedule lead to meeting client expectations.</p>     
                <div class="py-5">   
                    <h2 class="pt-3 text-center" style="font-size: 18px;">Click each image to view more details</h2>
                </div>
            </div>
        </div>

        <div class="row mb-3 justify-content-center">
            <div class="col-12 col-md-3 pb-5 pb-md-0" data-aos="fade-right" data-aos-delay="100">
                <button style="background: none; border: none; padding: 0;" id="open-tom-dialog" on:click={(() => openDialog(dialogTom))}>
                    <img src="/tom.jpg" alt="A business team working on a desk." style="max-width: 100%; height: auto;">
                </button>   
                <h3 class="text-center pt-3" style="font-size: 22px;">Thomas G. Wendorf. P.E., Principal</h3>                              
            </div>

            <dialog id="tom-dialog" bind:this={dialogTom}>
                <div>
                    <h3>Thomas G. Wendorf. P.E., Principal</h3>
                </div>

                <div>
                    <p>Tom Wendorf is one of those people who is equally at home talking to disaster victims, addressing a society at Harvard University, interacting with government officials or overseeing sophisticated analytics to discover hidden opportunities for funding. After earning his B.S. in Civil Engineering from Texas A&M University and his Masters in Public Administration from the University of Houston, he has spent more than three decades helping organizations in both the public and private arenas meet their most urgent and complex challenges. A past recipient of the Engineer of the Year Award from the Texas Society of Engineers, Tom is known for his extensive track record and for his belief in professional collaboration and “flexible problem solving.”</p>
                </div>

                <div class="mb-3"><a href="/thomas-resume.pdf" download data-sveltekit-reload>View my professional resume</a></div>

                <button id="close-tom-dialog" class="close-button" on:click={() => closeDialog(dialogTom)}>Close</button>
            </dialog>



            <div class="col-12 col-md-3 pb-5 pb-md-0 text-center" data-aos="fade-right" data-aos-delay="300">
                <button style="background: none; border: none; padding: 0;" id="open-nancy-dialog" on:click={() => openDialog(dialogNancy)}>
                    <img src="/nancy.jpg" style="max-width: 100%; height: auto;" alt="Nancy headshot">
                </button>   
                <h3 class="text-center pt-3" style="font-size: 22px;">Nancy A. Beward, C.F.M., President</h3>                              
            </div>

            <dialog id="nancy-dialog" bind:this={dialogNancy}>
                <div><h3>Nancy A. Beward, C.F.M., President</h3></div>

                <div>
                    <p>In her more-than-thirty-plus years in the profession, Nancy Beward has managed and inspected construction projects in Southeast Turkey for the United States Government; was responsible for streets, drainage, customer service and right-of-way management for the City of San Antonio; successfully managed thousands of individual disaster recovery and clean-up projects worth billions dollars for the State of Texas; and helped the Port Authority of New York and New Jersey and New York and New Jersey Transit nearly double the funding for disaster recovery from Super Storm Sandy. Nancy has a BS in Civil Engineering, and is Certified in Floodplain Management by the Association of State Floodplain Managers. Driven by a mission to improve the lives of the citizens she serves, Nancy has a reputation for seeing that all the details are covered and projects are successfully completed on time and on budget.</p>
                </div>

                <div class="mb-3"><a href="/nancy-resume.pdf" download data-sveltekit-reload>View my professional resume</a></div>

                <button id="close-nancy-dialog" class="close-button" on:click={() => closeDialog(dialogNancy)}>Close</button>
            </dialog>

            <div class="col-12 col-md-3 text-center pb-5 pb-md-0" data-aos="fade-right" data-aos-delay="500">
                <button style="background: none; border: none; padding: 0;" id="open-larry-dialog" on:click={() => openDialog(dialogLarry)}>
                    <img src="/larry.jpg" style="max-width: 100%; height: auto;" alt="Larry headshot">
                </button>   
                <h3 class="text-center pt-3" style="font-size: 22px;">Larry W. Beward, V.P. Business Development</h3>                              
            </div>

            <dialog id="larry-dialog" bind:this={dialogLarry}>
                <div><h3>Larry W. Beward, V.P. Business Development</h3></div>

                <div>
                    <p>Larry Beward is a retired Lt. Colonel with the Unites States Air Force. His military career spanned 29 year to include several tours as a commander. While in the Air Force, Larry’s assignments and experience has provided him with a unique skill set that is a perfect fit to lead the business development for Wendorf Beward & Partners. He has more than 45 years of experience in general leadership, management, education, strategic planning, security/safety training, operations management, logistics and customer support. Focused on leadership, Larry has successfully built teams that produce results.</p>
                </div>

                <div class="mb-3"><a href="/larry-resume.pdf" download data-sveltekit-reload>View my professional resume</a></div>

                <button id="close-larry-dialog" class="close-button" on:click={() => closeDialog(dialogLarry)}>Close</button>
            </dialog>

            <div class="col-12 col-md-3 text-center pb-5 pb-md-0" data-aos="fade-right" data-aos-delay="700">
                <button style="background: none; border: none; padding: 0;" id="open-suzanne-dialog" on:click={() => openDialog(dialogSuzanne)}>
                    <img src="/suzanne.jpg" style="max-width: 100%; height: auto;" alt="Suzanne headshot">
                </button>   
                <h3 class="text-center pt-3" style="font-size: 22px;">Suzanne F. Wendorf, Business Manager</h3>                              
            </div>

            <dialog id="suzanne-dialog" bind:this={dialogSuzanne}>
                <div><h3>Suzanne F. Wendorf, Business Manager</h3></div>

                <div>
                    <p>After more than 30 years in the educational field, Suzanne Wendorf is responsible for managing the daily business operations of Wendorf Beward & Partners. Suzanne’s oversight and management of the firm’s activities and client base ensure proper accounting and documentation with all aspects of Wendorf Beward & Partners.</p>
                </div>

                <div class="mb-3"><a href="/suzanne-resume.pdf" download data-sveltekit-reload>View my professional resume</a></div>

                <button id="close-suzanne-dialog" class="close-button" on:click={() => closeDialog(dialogSuzanne)}>Close</button>
            </dialog>
        </div>

        <div class="row mb-3 pt-4 justify-content-center" data-aos="fade-up" data-aos-delay="300">
            <div class="col-12">
                <div class="pb-3">
                    <h2>Our <b>partners</b> give us our purpose</h2>
                </div>
                <p>Partnership is a guiding principle of everything we do at WBP. Tom and Nancy have been sharing their success stories since 1999, in both the public and private sectors. Not only are they adept at collaborating with each other, they have assembled a roster of trusted professionals with whom they partner to expand their reach and expertise. Finally, they hold a strong belief in working in partnership with their clients, providing strong accountability and the ability to make the adjustments that maximize project and program successes.</p>
            </div>
        </div>

    </div>
</div>