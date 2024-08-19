
<svelte:head>
	<title>Contact | Wendorf Beward & Partners</title>
	<meta name="description" content="Our Team | Wendorf Beward & Partners" />
</svelte:head>

<script>
    import { onMount } from 'svelte';

    let siteKey = '6LeBnSkqAAAAAAKCHxfT8ezTD8huvP3dbr9S3OZT';

    onMount(async () => {
        const script = document.createElement('script');
        script.src = 'https://www.google.com/recaptcha/api.js';
        script.async = true;
        script.defer = true;

        script.addEventListener('load', () => {
            console.log('reCAPTCHA script loaded');
        });

        document.body.appendChild(script);
    });

    let formData = {
        firstName: '',
        lastName: '',
        email: '',
        message: '',
        phone: '',
        'g-recaptcha-response': '',
    };

    let confirmationMessage = '';
    let errorMessage = '';
    let isLoading = false;
  
    async function handleSubmit(event) {
        event.preventDefault();

        if (isLoading) return;

        isLoading = true;

        const form = new FormData(event.target);

        let firstName = form.get('firstName');
        let lastName = form.get('lastName');
        let email = form.get('email');
        let phone = form.get('phone');
        let message = form.get('message');
        let recaptchaResponse = grecaptcha.getResponse();


        const response = await fetch('https://3fc3rxfu7r62gbm7omld4tgepa0xkaqj.lambda-url.us-east-2.on.aws/', {
            method: 'POST',
            headers: {
                'Content-Type': 'application/json',
            },
            body: JSON.stringify({
                firstName: firstName,
                lastName: lastName,
                email: email,
                phone: phone,
                message: message,
                'g-recaptcha-response': recaptchaResponse,
            }),
        });
        
        if (response.ok) {
            const responseData = await response.json();
            confirmationMessage = responseData.message;

            // Reset form fields
            formData = {
                firstName: '',
                lastName: '',
                email: '',
                message: '',
                phone: '',
                'g-recaptcha-response': '',
            };
        } else {
            errorMessage = 'Our apologies; there was an error processing your request. Please try again later.';
            console.error('Error sending email');
        }

        isLoading = false;  
    }
  </script>

<div class="py-5">
    <div class="container">
        <div class="text-center">
            <h1 class="pb-2">
                Let's Partner Up
            </h1>
        </div>
    </div>
</div>

<div class="container">
    <div class="row justify-content-center pb-5">
        <div class="col-12 col-md-10 col-lg-8">
            <form id="contact-form" on:submit={handleSubmit}>
                <div class="row">
                    <div class="col-6">
                        <div class="form-floating mb-3">
                            <input type="text" class="form-control" id="first_name" name="firstName"
                                placeholder="First Name" bind:value={formData.firstName}>
                            <label for="first_name">First Name</label>
                        </div>
                    </div>

                    <div class="col-6">
                        <div class="form-floating mb-3">
                            <input type="text" class="form-control" id="last_name" name="lastName"
                            placeholder="Last Name" bind:value={formData.lastName}>
                            <label for="last_name">Last Name</label>
                        </div>
                    </div>
                </div>

                <div class="row">
                    <div class="col">
                        <div class="form-floating mb-3">
                            <input type="email" class="form-control" id="email" name="email"
                            placeholder="Email" bind:value={formData.email}>
                            <label for="email">Email</label>
                        </div>
                    </div>
                </div>

                <div class="row">
                    <div class="col">
                        <div class="form-floating mb-3">
                            <input type="tel" class="form-control" name="phone" id="phone" 
                            placeholder="Phone Number" maxlength="15" bind:value={formData.phone}/> 
                            <label for="phone">Phone Number</label>
                        </div>
                    </div>
                </div>

                <div class="row">
                    <div class="col">
                        <div class="form-floating mb-5">
                            <textarea class="form-control" id="message" name="message" bind:value={formData.message}
                            placeholder="Tell us about your project" style="height: 150px"></textarea>
                            <label for="message">Tell us about your project</label>
                        </div>
                    </div>
                </div> 

                <div class="g-recaptcha mb-3" data-sitekey={siteKey}></div>

                <button class="btn btn-reversed shadow-btn" disabled={isLoading}
                    type="submit"
                >
                    Submit
                </button>

                <div class="pt-4">
                {#if confirmationMessage}
                    <p class="confirmation">{confirmationMessage}</p>
                {:else if errorMessage}
                    <p class="error-message">{errorMessage}</p>
                {/if}
                </div>

                {#if isLoading}
                    <div class="spinner-border text-primary" role="status">
                        <span class="visually-hidden">Loading...</span>
                    </div>
                {/if}
            </form>
        </div>
    </div>
</div>


<style>
    .confirmation {
        color: rgb(0, 0, 184)
    }

    .error-message {
        color: rgb(199, 0, 0)
    }
</style>