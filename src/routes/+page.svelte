<svelte:head>
	<title>Texas Engineering Firm | Wendorf Beward & Partners</title>
	<meta name="description" content="Our Team | Wendorf Beward & Partners" />
</svelte:head>


<style>
    [data-aos="card-animation-left"] {
        /* on mobile */ 
        transform: translateY(50px);
        opacity: 0;

            &.aos-animate {
                transform: translateY(0);
                transition-duration: 1.5s;
                opacity: 1;
            }

        /* on desktop */ 
        @media screen and (min-width: 768px) {
            transform: translateX(-100px);
            &.aos-animate {
                transform: translateX(0);
                transition-delay: 0.1s;
            }
        }
    }

    [data-aos="card-animation-middle"] {
        /* on mobile */ 
        transform: translateY(50px);
        opacity: 0;
            &.aos-animate {
                transform: translateY(0);
                transition-duration: 1.5s;
                opacity: 1;
            }

        /* on desktop */ 
        @media screen and (min-width: 768px) {
            transform: translateX(-100px);
            &.aos-animate {
                transform: translateX(0);
                transition-delay: 0.3s;
            }
        }
    }

    [data-aos="card-animation-right"] {
        /* on mobile */ 
        transform: translateY(50px);
        opacity: 0;
            &.aos-animate {
                transform: translateY(0);
                transition-duration: 1.5s;
                opacity: 1;
            }

        /* on desktop */ 
        @media screen and (min-width: 768px) {
            transform: translateX(-100px);
            &.aos-animate {
                transform: translateX(0);
                transition-delay: 0.5s;
            }
        }
    }
</style>



<div class="pt-5 pb-5" style="min-height: 700px; position: relative;">
    <div style="background: url('/homepage_bg.jpg') no-repeat center center fixed; 
                background-size: cover; position: absolute; top: 0; left: 0; right: 0; bottom: 0; z-index: 0;"></div>
    <div style="position: absolute; top: 0; left: 0; right: 0; bottom: 0; z-index: 1;
                background: white; opacity: 0.7;"></div>
    <div class="container pb-5" style="position: relative; z-index: 2; padding-top: 75px;">
        <div class="row mb-5 justify-content-center">   
            <div class="col-12 col-md-8">
                <div class="text-center">
                    <h1 style="color:black; font-weight: bold; letter-spacing: 2px;" class="pb-4">Flexible Problem-Solving: Empowering Success</h1>
                    <h4 style="color:black; font-weight: 300; letter-spacing: 1px;" class="pb-4">Tailored solutions for a changing world, leveraging decades of expertise and innovative approaches, <strong style="font-weight: bold;">Wendorf Beward & Partners</strong> is your trusted partner in achieving your goals.</h4>
                    
                    <div class="pt-4">
                        <a href="/our-expertise">
                            <button type="button" class="btn btn-reversed shadow-btn">Discover our expertise</button>
                        </a> 
                    </div>
                </div>
            </div>
        </div>
    </div>
</div>



<div class="py-5">
    <div class="container pt-5" data-aos="fade-up" data-aos-duration="750">
        <div class="row mb-5 text-center">
            <h1 style="color: black;">
                How We Work
            </h1>
        </div>
    </div>

    <div class="container pb-5">
        <div class="row mb-3 px-5 px-sm-0">
            <div class="col-sm-12 col-md-4 justify-content-center homepage-cols mb-4">
                <div class="text-center homepage-card" data-aos="card-animation-left" style="border-radius: 20px; padding: 20px; height: 100%">
                    <h4 class="mb-4 mt-3" style="color: white">Outline your goals</h4>
                    <i class="fa-solid fa-bullseye" style="color: white; font-size: 60px;"></i>
                    <p class="mt-4" style="color: white">
                        We meet with you to define project objectives and develop the framework for project execution.</p>
                </div>
            </div>

            <div class="col-sm-12 col-md-4 justify-content-center homepage-cols mb-4">
                <div class="text-center homepage-card" data-aos="card-animation-middle" style="border-radius: 20px; padding: 20px; height: 100%;">
                    <h4 class="mb-4 mt-3" style="color: white">Create a Plan</h4>

                    <i class="fa-solid fa-pencil" style="color: white; font-size: 60px;"></i>

                    <p class="mt-4" style="color: white">
                        A project management plan for every assignment that identifies and clearly describes processes and procedures.</p>
                </div>
            </div>

            <div class="col-sm-12 col-md-4 justify-content-center homepage-cols mb-4">
                <div class="text-center homepage-card" data-aos="card-animation-right" style="border-radius: 20px; padding: 20px; height: 100%;">
                    <h4 class="mb-4 mt-3" style="color: white">Project Delivery</h4>

                    <i class="fa-solid fa-box" style="color: white; font-size: 60px;"></i>

                    <p class="mt-4" style="color: white">
                        A seasoned team of professionals experienced at delivering projects with efficiency and achieving goals.</p>                    
                </div>
            </div>
        </div>
    </div>
</div>


<div class="py-5">
    <div class="container py-5">
        <div class="row mb-3">

            <div class="col-12 col-md-6 align-items-center d-flex justify-content-center order-2 order-md-1" data-aos="fade-up" data-aos-delay="150">
                <div>
                    <img src='/business_team2.jpg' alt="A business team working on a desk."
                        style="max-width: 100%; height: auto;">
                </div>
            </div>

            <div class="col-12 col-md-6 d-flex order-1 order-md-2" data-aos="fade-up" data-aos-delay="150">
                <div class="container">

                    <div class="row">
                        <div class="col-12 text-center mb-4">
                            <h1 style="color: black;">
                                Areas of Expertise
                            </h1>
                        </div>
                    </div>

                    <div class="row mb-sm-0 mb-md-3">
                        <div class="col-md-6 col-sm-12 mb-3 mb-sm-3">
                            <a href="/our-expertise/program-delivery" style="text-decoration: none;">
                                <div class="text-center p-3" style="background-color: #f0f0f0; border-radius: 20px; height: 100%;">
                                    <p style="color: black;">Program Delivery</p>
                                    <i class="fa-solid fa-box" style="color: #EC1C24; font-size: 45px;"></i>
                                </div>
                            </a>
                        </div>

                        <div class="col-md-6 col-sm-12 mb-3 mb-sm-3">
                            <a href="/our-expertise/asset_management" style="text-decoration: none;">
                                <div class="text-center p-3" style="background-color: #f0f0f0; border-radius: 20px; height: 100%;">
                                    <p style="color: black;">Asset Management</p>
                                    <i class="fa-solid fa-list-check" style="color: #EC1C24; font-size: 45px;"></i>
                                </div>
                            </a>
                        </div>
                    </div>

                    <div class="row mb-sm-0 mb-md-3">
                        <div class="col-md-6 col-sm-12 mb-3 mb-sm-3">
                            <a href="/our-expertise/disaster_response" style="text-decoration: none;">
                                <div class="text-center p-3" style="background-color: #f0f0f0; border-radius: 20px; height: 100%;">
                                    <p style="color: black;">Disaster Response and Recovery</p>
                                    <i class="fa-solid fa-cloud-bolt" style="color: #EC1C24; font-size: 45px;"></i>
                                </div>
                            </a>
                        </div>

                        <div class="col-md-6 col-sm-12 mb-3 mb-sm-3">
                            <a href="/our-expertise/performance_improvement" style="text-decoration: none;">
                                <div class="text-center p-3" style="background-color: #f0f0f0; border-radius: 20px; height: 100%;">
                                    <p style="color: black;">Performance Improvement and Expert Witness</p>
                                    <i class="fa-solid fa-chart-line" style="color: #EC1C24; font-size: 45px;"></i>
                                </div>
                            </a>
                        </div>
                    </div>

                    <div class="row pb-5 pb-md-0">
                        <div class="text-center">
                            <a href="/about">
                                <button type="button" class="btn btn-reversed shadow-btn">Meet our talented team</button>
                            </a>  
                        </div>
                    </div>
            
                <!-- Close container div -->
                </div>
            <!-- Close column div -->
            </div>

        </div>
    </div>
</div>


<div class="pt-5 pb-5" style="min-height: 700px; position: relative;">
    <div style="background: url('/apwa1.jpg') no-repeat center center fixed; 
                background-size: cover; position: absolute; top: 0; left: 0; right: 0; bottom: 0; z-index: 0;"></div>
    <div style="position: absolute; top: 0; left: 0; right: 0; bottom: 0; z-index: 1;
                background: white; opacity: 0.7;"></div>
    <div class="container pb-5" style="position: relative; z-index: 2; padding-top: 75px;">
        <div class="row mb-5 justify-content-center">   
            <div class="col-12 col-md-8">
                <div class="text-center">
                    <h1 style="color:black; font-weight: bold; letter-spacing: 2px;" class="pb-4">American Public Works Project of the Year 2023</h1>
                    <h4 style="color:black; font-weight: 300; letter-spacing: 1px;" class="pb-4">American Public Works awarded Wendorf Beward & Partners the 2023 Project of the Year Award for successfully restoring the theater and parking garages damaged by Hurricane Harvey using FEMA Disaster Recovery Funding Reimbursements.</h4>
                    
                    <div class="pt-4" data-aos="fade-up" data-aos-duration="700">
                        <a href="/portfolio#wortham-portfolio-section">
                            <button type="button" class="btn btn-reversed shadow-btn">Explore this award-winning project</button>
                        </a> 
                    </div>
                </div>
            </div>
        </div>
    </div>
</div>
