# TCR_Codesign
HTML to control recaptcha for bot control on small grants co-design survey

1.) Displays reCAPTCHA: The page loads, showing a Google reCAPTCHA widget that the user must complete.
2.) Verification: When the user clicks "Verify," JavaScript checks if the reCAPTCHA was completed.
3.) Show Survey Link: If the reCAPTCHA is successful, a hidden survey link becomes visible.
4.) Open Survey: Clicking the survey link opens the Google Form in a new browser tab.
5.) User Feedback: alert boxes are used to communicate with the user.

## Overview of Script Function 
This HTML code continues to use Google reCAPTCHA for human verification; once verification is confirmed, a link is provided to the user to complete the survey. Here's a breakdown:

1. HTML Structure Changes:

-<title>Verify Access</title>: The page title has been changed from "reCAPTCHA Validation" to   "Verify Access," which is a more general and user-friendly title.
-<a id="survey-button" href="https://your-hidden-google-form-url" target="_blank">Click Here    to Take the Survey</a>:
  The survey button is now an anchor (<a>) tag instead of a <button> tag. This means it's a       direct hyperlink.
  The href attribute is set to "https://your-hidden-google-form-url", which is where the user     will be redirected. Remember to replace this with your actual Google Form URL.
  target="_blank" attribute will open the link in a new browser tab.
  The id is still "survey-button" so it can be manipulated by the Javascript.

2. JavaScript:

document.getElementById('survey-button').style.display = "inline-block";:
Instead of display: "block", the survey link's display is now set to inline-block. This means it will appear in the line of text like an inline element, but it will also respect width and height properties like a block element. This is more appropriate for a link.
alert("You are verified! Click the button to proceed.");:
The alert message has been updated to explicitly tell the user to "Click the button to proceed," providing clearer instructions.
Overall Functionality:

reCAPTCHA Verification: The user still interacts with the reCAPTCHA widget to prove they are a human.
Verification Check: The validateCaptcha() function checks the reCAPTCHA response.
Display Survey Link: If the reCAPTCHA is successful, the survey link (<a> tag) becomes visible using inline-block display.
Open Survey: When the user clicks the survey link, the Google Form opens in a new browser tab due to the target="_blank" attribute.
User Feedback: alert boxes are used to display messages to the user.
