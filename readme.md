## Implementing International Telephone Input in Form Validation

Creating forms for international audiences can be challenging, as telephone numbers can vary greatly in format and length depending on the country. To ensure that users are able to enter their telephone numbers correctly and that the form can process and validate the numbers properly, it’s important to use an “int-tel-input” field.

One library that can be used for this purpose is the International Phone Number Form Validation library, which is available on GitHub at https://github.com/codewithkim1/International-Phone-Number-Form-Vlidation. To use this library, you can clone it to your local machine using the following command in the terminal:

```bash
git clone https://github.com/codewithkim1/International-Phone-Number-Form-Vlidation.git

```
## Usage 
This command will create a new directory named ‘International-Phone-Number-Form-Vlidation’ on your local machine, which will contain the CSS, JavaScript, and image files that are necessary for the library to work.

To implement the int-tel-input field in your form, you will need to add the following code to the HTML file that contains your form:

```html

<form>
  <div class="form-group">
    <label for="phone">Phone Number:</label>
    <input type="tel" class="form-control" id="phone" name="phone">
  </div>
  <button type="submit" class="btn btn-primary">Submit</button>
</form>

```

You will need to add the following links to the head of your HTML file to include the CSS and JavaScript files for the library:

```html

<link rel="stylesheet" href="International-Phone-Number-Form-Vlidation/css/intlTelInput.css">
<script src="International-Phone-Number-Form-Vlidation/js/intlTelInput.js"></script>

```

You will also need to add a script to your HTML file to initialize the int-tel-input field:

```javascript

<script>
  var input = document.querySelector("#phone");
  window.intlTelInput(input);
</script>

```

This script will initialize the int-tel-input field and make it functional. With this code in place, users will be able to select their country from a drop-down menu and enter their telephone number in the format that is appropriate for that country. The library will automatically validate and format the number as it is entered, so that it can be easily understood and processed by the form.

Additionally, you can also add a validation function to the form to validate the phone number before submitting the form.


```javascript

<script>
  var input = document.querySelector("#phone");
  window.intlTelInput(input);
  var phone = document.querySelector("#phone");
  phone.addEventListener("blur", function() {
    if (input.value) {
      if (!intlTelInputUtils.isValidNumber(input.value)) {
        alert("Invalid phone number");
      } else {
        alert("Valid phone number");
      }
    }
  });
</script>

```

This code will check if the phone number is valid or not before the form is submitted.

## Summary
In summary, using an int-tel-input field in forms can greatly improve the user experience for international audiences and ensure that telephone numbers are entered and processed correctly. The International Phone Number Form Validation library is a useful tool for implementing int-tel-input fields in web forms.


To use this library, you can clone it from GitHub to your local machine and include the necessary CSS and JavaScript files in your HTML file. You will also need to add the int-tel-input field to your form, and initialize it with a script. You can also add validation function to the form to validate the phone number before submitting the form. This will help ensure that users are able to enter their telephone numbers in the correct format and that the form can process and validate the numbers properly.

## License

[MIT](https://choosealicense.com/licenses/mit/)