# New Patient Scheduling

This article provides procedures for scheduling new primary care patients, including insurance verification, provider selection, appointment scheduling, and escalation scenarios.

| | |
|---|---|
| **Author** | David Posto |
| **Document Type** | Knowledge Base Article |
| **Audience** | Scheduling Agents |
| **Last Updated** | June 2026 |

---

## Symptoms

A new patient needs to schedule an appointment with a Primary Care Provider (PCP).

---

## Solution

### Pre-Step 1: Cardiac Concerns or Shortness of Breath

- If the patient at any time expresses concern with cardiac issues or shortness of breath:
    - Inform the caller:
        > *Your symptoms suggest a serious condition that requires immediate medical attention. Please hang up the phone and call 911 or go to the nearest emergency room.*
    - Close the Service Order.


---

### Pre-Step 2: Addressing Sensitive Topics

- For information on how to address sensitive topics during calls such as gender or diagnosis, refer to the **[Sensitive Topics Procedure]** article.


---

### Step 1: Determine if New or Existing Patient

- Ask the caller:
    > *Are you needing to schedule an appointment with a new primary care provider?*

- **If Yes**, proceed to Step 2.
- **If the caller is an existing patient:**
    - Inform the caller:
        > *This number is for scheduling new patients. Are you interested in scheduling with a new provider, or would you like to stay with your current provider?*
    - **If the patient wants to stay with their current provider:**
        - Note in the Service Order that the caller is not a new patient.
        - If the practice is open, warm transfer the caller. See **[Warm Transfer Procedures]**.
        - If the office is currently closed, proceed to Step 8.
    - **If the patient would like to schedule with a new provider**, proceed to Step 2.


---

### Step 2: Gather Patient's Insurance and Determine if Accepted

- Refer to the **[Accepted Insurance Reference]** to determine if the caller's insurance is accepted.
- Note the caller's insurance in the Service Order.

- **If accepted:**
    - Inform the patient:
        > *Your insurance is accepted.*
    - Proceed to Step 3.

- **If NOT accepted:**
    - Ask the caller:
        > *Your insurance is not currently accepted. Would you still like to schedule a new appointment?*
    - If Yes, proceed to Step 3.
    - If No:
        - Inform the patient:
            > *Thank you for calling. Have a great day.*
        - Close the Service Order.

- **If the patient does not have insurance**, proceed to Step 3.


---

### Step 3: Determine which Location the Patient Needs to Schedule In

- Inform the caller of the available service area locations.
- Ask the caller:
    > *Which area do you live closest to, or where would you prefer to see the provider?*
- Note the caller's response in the Service Order.


---

### Step 4: Determine which Practice to Schedule With

- Open the **[PCPs Taking New Patients]** internal scheduling reference.
- Navigate to the **PCPs Taking New Patients** tab.
- Practices are grouped by location. Each practice row lists the PCPs currently accepting new patients below it.
- Locate the city or town noted in Step 3 and identify the available practices and their addresses.
- Present the options to the caller and confirm which practice they would prefer.

> ⚠️ **Note:** A practice must have providers listed beneath it to be eligible for new patient scheduling.

- **If you are unable to determine the correct practice:**
    - During standard business hours: Contact the **[Scheduling Supervisor]** for assistance.
    - Outside business hours or if the supervisor is unavailable: Proceed to Step 8.
- Note the selected practice in the Service Order.


---

### Step 5: Determine which Provider to Schedule With

- If the caller requests a specific provider, attempt to schedule with that provider first.
- Review the providers listed under the practice selected in Step 4.
- **If more than one provider is listed:**
    - Check the **Scheduling Priority** column — if a provider is flagged, select them first.
    - If no priority is listed, any available provider may be selected.
- Verify that the patient's age and insurance (noted in Step 2) are accepted by the selected provider, using the **Age / Insurance** column.
- Review the **Special Instructions** column for any notes and communicate relevant information to the caller.
- If the caller requests information about the provider, a biographical link is available in the **Provider Bio Link** column.
- Note the selected provider in the Service Order.
- Proceed to Step 6.


---

### Step 6: Select an Appointment with the Provider

- Click the **Online Scheduling** link for the selected provider to view available appointments.

- **If the message "Sorry, we couldn't find any open appointments." appears:**
    - Repeat Step 5 to check for additional providers at the same practice.
    - If no additional providers are listed, ask the caller:
        > *Would you like to schedule an appointment at a different location?*
        - If Yes: Repeat Steps 4–5 for an alternate practice.
        - If No: Note the preferred practice, desired dates/times, and any issues in the Service Order. Warm transfer if the office is open (see **[Warm Transfer Procedures]**), or proceed to Step 8 if closed.

- Review available appointments with the caller.
    - If **"more..."** appears below a time slot, hover over it to reveal additional times.

- **If no appointment is available within 7 days:**
    - Repeat Step 5 to check for additional providers at the same practice.
    - If no other providers have availability within 7 days, inform the caller of the next available appointment.
        - If acceptable, proceed to Step 6 (selecting the appointment).
        - If not acceptable, ask:
            > *Would you like to schedule at a different location?*
            - If Yes: Repeat Steps 4–5 for an alternate practice.
            - If No:
                - **If the next available appointment is more than 2 weeks out**, ask:
                    > *Would you like to schedule that appointment and be added to a waitlist in case an earlier opening becomes available? If a sooner appointment opens up, you'll receive a text notification to your cell phone.*
                    - If Yes: Note "SMS Waitlist opt-in" and the caller's cell number in the Service Order. Proceed to Step 7.
                    - If No: Note the preferred practice, desired dates/times in the Service Order. Warm transfer if open or proceed to Step 8.
                - **If the next available appointment is less than 2 weeks out**: Note the practice and desired dates/times. Warm transfer if open or proceed to Step 8.

- Proceed to Step 7.


---

### Step 7: Gather Patient Information and Schedule Appointment

- Click the selected appointment.
- In the pop-up, complete the CAPTCHA.
- Verify the provider, appointment date and time, and location are correct.
- In the **Reason for Visit** field, enter the caller's reason (e.g., *"New patient visit"*, or include any additional details the caller provides).
- Click **Continue**.
- Under **"Continue as a Guest"**, click **Continue**.

**Patient Information screen:**

- Ask for and enter the patient's information.
- Fields marked with a red asterisk (\*) are required.

> 🚫 **Do NOT request the patient's Social Security Number.**  
> If the SSN field is required, enter `000-00-0000` or `999-99-9999`.

- Click **Next**.

**Insurance Information screen:**

- Ask for and enter the patient's insurance information (found on their insurance card).
- If the caller has no insurance, select **No Insurance**.
- If the insurance was not found in the **[Accepted Insurance Reference]**, select **Not Listed**.
- Fields marked with a red asterisk (\*) are required.

> 💡 **FYI:** "Subscriber ID" may also appear as "Subscriber Number," "Member Number," "Member ID," "Policy Number," or "Policy ID."

- Click **Schedule it!** to complete the appointment.
- Inform the caller:
    > *You will shortly receive an email confirmation of your appointment, as well as an email with a link to register for the patient portal.*

- **If the caller's insurance was not listed in the reference:**
    - Provide the office phone number and offer a warm transfer if they'd like to speak with someone about their insurance. See **[Warm Transfer Procedures]** if needed.

**If the appointment is successfully scheduled:**

- Note the following in the Service Order:
    - "Appointment Scheduled"
    - Appointment Date
    - Appointment Time
    - Appointment Location
- Close the Service Order.

**If unable to schedule the appointment:**

- Note the following in the Service Order:
    - The practice the patient needs to schedule at
    - Preferred dates and times
    - Any errors or issues encountered
- Warm transfer if the office is open (see **[Warm Transfer Procedures]**), or proceed to Step 8.


---

### Step 8: Escalation

If the issue remains unresolved, follow the appropriate escalation procedure. Refer to the **[Escalation Procedures]** article.
