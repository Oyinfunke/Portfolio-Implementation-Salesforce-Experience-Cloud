
# Portfolio-Implementation-Salesforce-Experience-Cloud
=======
## Overview

This document outlines the implementation details of a Salesforce Experience Cloud portfolio, showcasing key configurations and integrations that enhance lead generation, appointment scheduling, security, and content management.

## Custom Web-to-Lead Form
**Implementation Steps:**
  1. Created a Web-to-Lead form to capture essential lead information, including Name, Email, Phone, Company, and Message.
  
  2. Enhanced the form's design using HTML to improve aesthetics and user experience.
  
  3. Implemented validation rules to ensure data integrity before submission.
  
  4. Embedded the form into the Experience Cloud site for seamless lead capture and integration with Salesforce.

<p align="left"> 
   <b>HTML customized Web-to-lead </b>
      <img src="images/Screenshot from 2025-03-31 11-02-36.png" alt="Web-to-lead form" style="width: 900px; height: 650px"/>
    
</p>

<p align="left"> 

<p text-align='center'>
<b>HTML Web-to-lead code</b>  
</p>

```HTML
<form action="https://webto.salesforce.com/servlet/servlet.WebToLead?encoding=UTF-8&orgId=00DWU00000Baby5" method="POST" style="max-width: 400px; margin: 0 auto; padding: 20px; background-color: #002b56; border: 8px solid; border-image: linear-gradient(to bottom, #389f89, #4abdcd) 1; border-radius: 8px; box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);">
    <input type="hidden" name="oid" value="00DWU00000Baby5">
    <input type="hidden" name="retURL" value="https://grace8-dev-ed.develop.my.site.com/portfolio/s/thank-you">
  
    <div style="display: flex; flex-direction: column; gap: 15px; align-items: center;">
        <div style="display: flex; flex-direction: column; width: 90%;">
            <label for="first_name" style="font-weight: bold; color: #ffffff;">First Name</label>
            <input id="first_name" maxlength="40" name="first_name" type="text" placeholder="Enter your first name" style="padding: 10px; border: 1px solid #ccc; border-radius: 5px; width: 100%;" required>
        </div>
        <div style="display: flex; flex-direction: column; width: 90%;">
            <label for="last_name" style="font-weight: bold; color: #ffffff;">Last Name</label>
            <input id="last_name" maxlength="80" name="last_name" type="text" placeholder="Enter your last name" style="padding: 10px; border: 1px solid #ccc; border-radius: 5px; width: 100%;" required>
        </div>
        <div style="display: flex; flex-direction: column; width: 90%;">
            <label for="email" style="font-weight: bold; color: #ffffff;">Email</label>
            <input id="email" maxlength="80" name="email" type="email" placeholder="Enter your email" style="padding: 10px; border: 1px solid #ccc; border-radius: 5px; width: 100%;" required>
        </div>
        <div style="display: flex; flex-direction: column; width: 90%;">
            <label for="company" style="font-weight: bold; color: #ffffff;">Company</label>
            <input id="company" maxlength="40" name="company" type="text" placeholder="Enter your company name" style="padding: 10px; border: 1px solid #ccc; border-radius: 5px; width: 100%;" >
        </div>
        <button type="submit" style="padding: 12px; background-color: #05f283; color: #1c3369; font-weight: bold; border: none; border-radius: 5px; cursor: pointer; font-size: 16px; width: 100%;">Submit</button>
    </div>
  </form>

</p>
```

  

**Key Learnings:**
  
  1. Improved understanding of HTML form integration with Salesforce.
  
  2. Enhanced lead management within the org.

##  Calendly Integration

**Implementation Steps:**

1. Created a Calendly account and set up scheduling preferences.

2. Embedded [Calendly widget](https://github.com/tcampb/calendly-for-salesforce-flow?tab=readme-ov-file) into the Experience Cloud site for easy access to appointment booking.

3. Utilized automation (Flow ) to log scheduled appointments as Salesforce Events linked to the corresponding Leads or Contacts.

4. Tested the integration to ensure smooth data flow between Calendly and Salesforce.

<p align="left"> 
   <b>Calendly Screen-flow </b>
      <img src="images/Screenshot from 2025-03-31 12-13-54.png" style="width: 900px; height: 650px"/>
    </p>

**Key Learnings:**

1. Gained experience in integrating third-party applications with Salesforce.

2. Improved scheduling efficiency within the Experience Cloud environment.
