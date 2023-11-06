<section class="contact-form-container">
    <div class="contact-heading-container">
        <h2 class="third-heading">Get in Touch <i class="primary-icon fa-solid fa-paper-plane"></i></h2>
        <h1 class="primary-heading">Contact Us</h1>
        <p class="primary-p">Fill out this form for general inquiries or to get a quote on a load you need delivered</p>
    </div>
    <div class="form-wrapper">
        <form action="">
            <div class="form-list-container">
                <ul class="form-list">
                    <li class="form-list-item">
                        <div class="label-container">
                            <label for="name" class="third-heading">Name <span class="asterisk">*</span></label>
                        </div>
                        <div class="input-container">
                            <div class="input-wrapper">
                                <input type="text" required>
                                <label for="firstName" class="fourth-heading">First Name</label>
                            </div>
                            <div class="input-wrapper">
                                <input type="text" required>
                                <label for="lastName" class="fourth-heading">Last Name</label>
                            </div>
                        </div>
                    </li>
                    <li class="form-list-item">
                        <div class="label-container">
                            <label for="email" class="third-heading">Email <span class="asterisk">*</span></label>
                        </div>
                        <div class="input-container">
                            <div class="input-wrapper">
                                <input type="email" required>
                            </div>
                        </div>
                    </li>
                    <li class="form-list-item">
                        <div class="label-container">
                            <label for="phone" class="third-heading">Phone <span class="asterisk">*</span></label>
                        </div>
                        <div class="input-container">
                            <div class="input-wrapper">
                                <input type="text" name="country_code" title="Error Message" pattern="[1-9]{1}[0-9]{9}" required> 
                            </div>
                        </div>
                    </li>
                    <li class="form-list-item">
                        <div class="label-container">
                            <label for="address" class="third-heading">Address <span class="asterisk">*</span></label>
                        </div>
                        <div class="input-container">
                            <div class="input-wrapper">
                                <input type="text" required>
                                <label for="firstName" class="fourth-heading">City</label>
                            </div>
                            <div class="input-wrapper">                         
                                <select name="" aria-required="true" required>
                                    <option value=""></option>
                                    <option value="Alabama">Alabama</option>
                                    <option value="Alaska">Alaska</option>
                                    <option value="American Samoa">American Samoa</option>
                                    <option value="Arizona">Arizona</option>
                                    <option value="Arkansas">Arkansas</option>
                                    <option value="California">California</option>
                                    <option value="Colorado">Colorado</option>
                                    <option value="Connecticut">Connecticut</option>
                                    <option value="Delaware">Delaware</option>
                                    <option value="District of Columbia">District of Columbia</option>
                                    <option value="Florida">Florida</option>
                                    <option value="Georgia">Georgia</option>
                                    <option value="Guam">Guam</option>
                                    <option value="Hawaii">Hawaii</option>
                                    <option value="Idaho">Idaho</option>
                                    <option value="Illinois">Illinois</option>
                                    <option value="Indiana">Indiana</option>
                                    <option value="Iowa">Iowa</option>
                                    <option value="Kansas">Kansas</option>
                                    <option value="Kentucky">Kentucky</option>
                                    <option value="Louisiana">Louisiana</option>
                                    <option value="Maine">Maine</option>
                                    <option value="Maryland">Maryland</option>
                                    <option value="Massachusetts">Massachusetts</option>
                                    <option value="Michigan">Michigan</option>
                                    <option value="Minnesota">Minnesota</option>
                                    <option value="Mississippi">Mississippi</option>
                                    <option value="Missouri">Missouri</option>
                                    <option value="Montana">Montana</option>
                                    <option value="Nebraska">Nebraska</option>
                                    <option value="Nevada">Nevada</option>
                                    <option value="New Hampshire">New Hampshire</option>
                                    <option value="New Jersey">New Jersey</option>
                                    <option value="New Mexico">New Mexico</option>
                                    <option value="New York">New York</option>
                                    <option value="North Carolina">North Carolina</option>
                                    <option value="North Dakota">North Dakota</option>
                                    <option value="Northern Mariana Islands">Northern Mariana Islands</option>
                                    <option value="Ohio">Ohio</option>
                                    <option value="Oklahoma">Oklahoma</option>
                                    <option value="Oregon">Oregon</option>
                                    <option value="Pennsylvania">Pennsylvania</option>
                                    <option value="Puerto Rico">Puerto Rico</option>
                                    <option value="Rhode Island">Rhode Island</option>
                                    <option value="South Carolina">South Carolina</option>
                                    <option value="South Dakota">South Dakota</option>
                                    <option value="Tennessee">Tennessee</option>
                                    <option value="Texas">Texas</option>
                                    <option value="Utah">Utah</option>
                                    <option value="U.S. Virgin Islands">U.S. Virgin Islands</option>
                                    <option value="Vermont">Vermont</option>
                                    <option value="Virginia">Virginia</option>
                                    <option value="Washington">Washington</option>
                                    <option value="West Virginia">West Virginia</option>
                                    <option value="Wisconsin">Wisconsin</option>
                                    <option value="Wyoming">Wyoming</option>
                                </select>
                                <label for="firstName" class="fourth-heading">State</label>
                            </div>
                            <div class="input-wrapper">
                                <input type="text" required>
                                <label for="firstName" class="fourth-heading">Zip</label>
                            </div>
                        </div>
                    </li>
                    <li class="form-list-item">
                        <div class="label-container">
                            <label for="message" class="third-heading">Your Message <span class="asterisk">*</span></label>
                        </div>
                        <div class="input-container">
                            <div class="input-wrapper">
                                <textarea name="message" id="" cols="30" rows="10" required></textarea>
                            </div>
                        </div>
                    </li>
                    <li class="form-list-item">
                        <div class="input-container">
                            <div class="input-wrapper">
                                <button class="submit-button">Submit</button>
                            </div>
                        </div>
                    </li>
                </ul>
            </div>
        </form>
    </div>
</section>

<style>
    .contact-form-container {
        background: linear-gradient(180deg, #041E42, rgba(37, 42, 51, 0.9));
        display: flex;
        flex-direction: column;
        justify-content: flex-start;
        align-items: center;
        width: 100%;
        padding-top: 160px;
    }

    .contact-heading-container {
        display: flex;
        width: 100%;
        max-width: 400px;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        text-align: center;
        padding: 0px 1.2rem;
    }

    .contact-heading-container .third-heading,
    .contact-heading-container .primary-p {
        color: #f1f1f1;
    }

    .contact-heading-container .primary-icon {
        color: #315187;
    }

    .contact-heading-container .primary-heading {
        color: #a9a9a9;
    }

    .form-wrapper {
        width: 100%;
        height: 100%;
        display: flex;
        flex-direction: column;
        margin: 40px 0px;
        max-width: 800px;
        padding: 0px 1.2rem;
    }

    .form-list {
        display: flex;
        flex-direction: column;
        width: 100%;
        gap: 25px;
    }

    .label-container {
        padding-bottom: 10px;
    }

    .label-container .third-heading {
        color: #f1f1f1;
    }

    .asterisk {
        color: #d44a4a;
    }

    .input-container {
        display: flex;
        justify-content: center;
        align-items: center;
        gap: 15px;
        width: 100%;
    }

    .input-wrapper {
        display: flex;
        flex-direction: column;
        width: 100%;
    }

    .submit-button {
        font-family: 'Inter';
        text-transform: uppercase;
        text-align: center;
        height: 50px;
        width: 140px;
        font-size: 1rem;
        color: #fff;
        background-color: rgb(23, 132, 70);
        transition: all 200ms ease;
        cursor: pointer;
        border-radius: 5px;
        border: 0;
    }

    .submit-button:hover {
        background-color: #f1f1f1;
        color: #041E42;
    }

    input {
        font-family: 'Inter';
        padding: 12px 10px;
        font-size: 15px;
        width: 100%;
        border-radius: 5px;
        border: 0;
    }

    select {
        border-radius: 5px;
        border: 0;
        font-family: 'Inter';
        padding: 12px 10px;
        font-size: 15px;
        width: 100%;
    }

    textarea {
        font-family: 'Inter';
        padding: 12px 10px;
        font-size: 15px;
        width: 100%;
        border-radius: 5px;
        border: 0;
    }

    @media screen and (max-width: 580px) {
        .input-container {
            flex-direction: column;
        }

        .submit-button {
            width: 100%;
        }
    }

</style>