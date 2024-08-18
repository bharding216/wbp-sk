
<svelte:head>
	<title>Contact | Wendorf Beward & Partners</title>
	<meta name="description" content="Our Team | Wendorf Beward & Partners" />
</svelte:head>

<script src="https://www.google.com/recaptcha/api.js"></script>

<script>
    function onSubmit(token) {
        document.getElementById("contact-form").submit();
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
            <form action="{{ url_for('views.contact') }}" method="POST" id="contact-form">

                <div class="row">
                    <div class="col-6">
                        <div class="form-floating mb-3">
                            <input type="text" class="form-control" id="first_name" name="first_name"
                                placeholder="First Name">
                            <label for="first_name">First Name</label>
                        </div>
                    </div>

                    <div class="col-6">
                        <div class="form-floating mb-3">
                            <input type="text" class="form-control" id="last_name" name="last_name"
                            placeholder="Last Name">
                            <label for="last_name">Last Name</label>
                        </div>
                    </div>
                </div>

                <div class="row">
                    <div class="col">
                        <div class="form-floating mb-3">
                            <input type="email" class="form-control" id="email" name="email"
                            placeholder="Email">
                            <label for="email">Email</label>
                        </div>
                    </div>
                </div>

                <div class="row">
                    <div class="col">
                        <div class="form-floating mb-3">
                            <input type="tel" class="form-control" name="phone" id="phone" 
                            placeholder="Phone Number" maxlength="15"/> 
                            <label for="phone">Phone Number</label>
                        </div>
                    </div>
                </div>

                <div class="row">
                    <div class="col">
                        <div class="form-floating mb-5">
                            <textarea class="form-control" id="message" name="message"
                            placeholder="Tell us about your project" style="height: 150px"></textarea>
                            <label for="message">Tell us about your project</label>
                        </div>
                    </div>
                </div>

                <div class="form-floating mb-3 col-md-12 col-lg-8" style="display: none;">
                    <input type="hidden" name="phone_number" id="phone_number" 
                        value="123-456-7890" placeholder="Phone Number">
                    <label for="phone_number">Phone Number</label>
                </div>  
                
                <div class="form-floating mb-3 col-md-8 col-lg-6">
                    <input type="text" class="form-control" id="panda" name="panda"
                        placeholder="Pandas are black and:">
                    <label for="panda">Pandas are black and:</label>
                </div>

                <button class="g-recaptcha btn btn-reversed shadow-btn" 
                    data-sitekey="{{ recaptcha_site_key }}" 
                    data-callback='onSubmit' 
                    data-action='submit'
                    type="submit">Submit</button>

            </form>
        </div>
    </div>
</div>
