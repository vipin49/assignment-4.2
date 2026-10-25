1. Aim

To create a job application form using different HTML input types, labels, radio buttons, checkboxes, dropdown menus, a textarea, and a submit button.

2. Requirements

The job application form includes:

Full Name

Email Address

Phone Number

Date of Birth

Portfolio URL

Preferred Shift using radio buttons

Skills using checkboxes

Highest Qualification using a dropdown

Cover Letter using a textarea

A disabled field as an example

Submit button

3. Source Code

Create a file named job-application.html and copy the following complete code into it.

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Job Application Form</title>

    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f0f4f8;
            margin: 0;
            padding: 25px 15px;
        }

        .container {
            max-width: 600px;
            margin: auto;
            background-color: white;
            padding: 30px;
            border-radius: 10px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.12);
        }

        h1 {
            text-align: center;
            color: #1d4ed8;
        }

        .description {
            text-align: center;
            color: #555;
            margin-bottom: 25px;
        }

        .form-group {
            margin-bottom: 18px;
        }

        label {
            display: block;
            margin-bottom: 7px;
            font-weight: bold;
        }

        input[type="text"],
        input[type="email"],
        input[type="tel"],
        input[type="date"],
        input[type="url"],
        select,
        textarea {
            width: 100%;
            padding: 10px;
            border: 1px solid #ccc;
            border-radius: 5px;
            font-size: 15px;
            box-sizing: border-box;
        }

        input:focus,
        select:focus,
        textarea:focus {
            outline: 2px solid #93c5fd;
            border-color: #2563eb;
        }

        .options label {
            display: inline-block;
            font-weight: normal;
            margin-right: 15px;
            margin-bottom: 8px;
        }

        input[type="radio"],
        input[type="checkbox"] {
            margin-right: 5px;
        }

        input:disabled {
            background-color: #e5e7eb;
            color: #666;
            cursor: not-allowed;
        }

        textarea {
            resize: vertical;
        }

        button {
            width: 100%;
            padding: 12px;
            background-color: #2563eb;
            color: white;
            border: none;
            border-radius: 5px;
            font-size: 16px;
            font-weight: bold;
            cursor: pointer;
        }

        button:hover {
            background-color: #1d4ed8;
        }

        footer {
            text-align: center;
            margin-top: 20px;
            color: #666;
            font-size: 13px;
        }
    </style>
</head>

<body>

    <div class="container">

        <h1>Job Application Form</h1>

        <p class="description">
            Please fill in the details to apply for the job.
        </p>

        <form action="#" method="get">

            <div class="form-group">
                <label for="fullName">Full Name:</label>
                <input
                    type="text"
                    id="fullName"
                    name="fullName"
                    placeholder="Enter your full name"
                    autocomplete="name"
                    required
                >
            </div>

            <div class="form-group">
                <label for="email">Email Address:</label>
                <input
                    type="email"
                    id="email"
                    name="email"
                    placeholder="Enter your email address"
                    autocomplete="email"
                    required
                >
            </div>

            <div class="form-group">
                <label for="phone">Phone Number:</label>
                <input
                    type="tel"
                    id="phone"
                    name="phone"
                    placeholder="Enter your phone number"
                    autocomplete="tel"
                    pattern="[0-9]{10}"
                    maxlength="10"
                    title="Enter a 10-digit phone number"
                    required
                >
            </div>

            <div class="form-group">
                <label for="dob">Date of Birth:</label>
                <input
                    type="date"
                    id="dob"
                    name="dateOfBirth"
                    required
                >
            </div>

            <div class="form-group">
                <label for="portfolio">Portfolio URL:</label>
                <input
                    type="url"
                    id="portfolio"
                    name="portfolio"
                    placeholder="https://example.com"
                >
            </div>

            <div class="form-group">
                <label>Preferred Shift:</label>

                <div class="options">
                    <label for="morning">
                        <input
                            type="radio"
                            id="morning"
                            name="preferredShift"
                            value="Morning"
                            required
                        >
                        Morning
                    </label>

                    <label for="evening">
                        <input
                            type="radio"
                            id="evening"
                            name="preferredShift"
                            value="Evening"
                        >
                        Evening
                    </label>

                    <label for="night">
                        <input
                            type="radio"
                            id="night"
                            name="preferredShift"
                            value="Night"
                        >
                        Night
                    </label>
                </div>
            </div>

            <div class="form-group">
                <label>Skills:</label>

                <div class="options">
                    <label for="html">
                        <input
                            type="checkbox"
                            id="html"
                            name="skills"
                            value="HTML"
                        >
                        HTML
                    </label>

                    <label for="css">
                        <input
                            type="checkbox"
                            id="css"
                            name="skills"
                            value="CSS"
                        >
                        CSS
                    </label>

                    <label for="javascript">
                        <input
                            type="checkbox"
                            id="javascript"
                            name="skills"
                            value="JavaScript"
                        >
                        JavaScript
                    </label>

                    <label for="python">
                        <input
                            type="checkbox"
                            id="python"
                            name="skills"
                            value="Python"
                        >
                        Python
                    </label>
                </div>
            </div>

            <div class="form-group">
                <label for="qualification">
                    Highest Qualification:
                </label>

                <select
                    id="qualification"
                    name="qualification"
                    required
                >
                    <option value="">-- Select Qualification --</option>
                    <option value="12th">12th Pass</option>
                    <option value="Diploma">Diploma</option>
                    <option value="Graduate">Graduate</option>
                    <option value="Postgraduate">Postgraduate</option>
                    <option value="Other">Other</option>
                </select>
            </div>

            <div class="form-group">
                <label for="coverLetter">Cover Letter:</label>

                <textarea
                    id="coverLetter"
                    name="coverLetter"
                    rows="5"
                    placeholder="Write a short introduction about yourself..."
                    required
                ></textarea>
            </div>

            <div class="form-group">
                <label for="applicationId">
                    Application ID (Disabled Field):
                </label>

                <input
                    type="text"
                    id="applicationId"
                    name="applicationId"
                    value="Assigned by the employer"
                    disabled
                >
            </div>

            <button type="submit">Submit Application</button>

        </form>

        <footer>
            Job Application Form | HTML Assignment 4.2
        </footer>

    </div>

</body>
</html>

4. Explanation

Full Name: Uses type="text" to accept the applicant's name.

Email Address: Uses type="email" to validate the email format.

Phone Number: Uses type="tel" and a pattern to validate a 10-digit number.

Date of Birth: Uses type="date" to select a date.

Portfolio URL: Uses type="url" to accept a website address.

Radio Buttons: Allow the applicant to select one preferred shift. All radio buttons share the same name attribute.

Checkboxes: Allow the applicant to select multiple skills.

Dropdown: Uses the <select> and <option> tags to choose a qualification.

Cover Letter: Uses <textarea> to accept longer text.

Disabled Field: Uses the disabled attribute to prevent editing the Application ID field.

Labels: Every field has an associated <label> using the matching for and id attributes.

Required Fields: The required attribute ensures that mandatory fields are completed before submission.

Submit Button: Submits the completed form.

5. Testing

Open job-application.html in a web browser.

Verify that all fields and labels are displayed correctly.

Try submitting the form with required fields left empty.

Enter an invalid email address and check the browser validation.

Enter a phone number that is not 10 digits and check the validation.

Select one preferred shift and multiple skills.

Choose a qualification from the dropdown.

Verify that the Application ID field cannot be edited.

Fill in the required details and click Submit Application.

6. Result

The Job Application Form was successfully created using HTML. It demonstrates different input types, date and URL inputs, radio buttons, checkboxes, a dropdown menu, a textarea, labels, required-field validation, a disabled field, and a submit button.

7. Submission

Submit the following files:

job-application.html — the complete job application form.

job-application-screenshot.png — a screenshot of the form displayed in a web browser.

8. Screenshot Instructions

Save the code in job-application.html.

Open the file in a web browser using Live Server or by opening the file directly.

Make sure the form is visible on the screen.

Press Windows + Shift + S to capture a screenshot.

Save the screenshot as job-application-screenshot.png.

Note: This form demonstrates HTML input fields and browser validation. A backend is required to store applications permanently. Disabled fields are not submitted with the form