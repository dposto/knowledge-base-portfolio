# How-To: Screen-Share

This article provides procedures for initiating a screen-share session with a user's computer using Endpoint Central or BeyondTrust.

|                   |                        |
| ----------------- | ---------------------- |
| **Author**        | David Posto            |
| **Document Type** | Knowledge Base Article |
| **Audience**      | Help Desk Agents       |
| **Last Updated**  | June 2026              |

---

## Symptoms

How to initiate a screen-share session with a user's computer.

---

## Solution

### Step 1: Important Information

1. ⚠️ **NEVER take a screenshot of protected health information (PHI).**

1. If the device is a Mac, Apple, or mobile device:

    1. We are unable to screen-share into these devices.

    1. **Note the following in the Service Order:**

        1. The type of device.

        1. That the device cannot be screen-shared into.

    1. Return to the Originating Article and attempt to assist the caller as able.

1. For non-dedicated agents:

    1. Screen-share accounts are provided to dedicated agents only.

    1. If you were prompted to initiate a screen-share, return to the Originating Article and attempt to assist the caller as able.

1. For dedicated agents, if you receive an Admin UAC prompt, see `Article 8163` to use admin credentials.

---

### Step 2: GlobalProtect VPN

1. It may be necessary to disconnect from GlobalProtect VPN to be able to perform troubleshooting steps on the user's system.

1. In such a case:

    1. ⚠️ This code should only be entered by the dedicated agent screen-sharing into the system.

    1. **Note the reason for disconnecting from GlobalProtect VPN in the Service Order.**

    1. In your web browser, open your 1Password extension and enter your password.

    1. On the left side, under *"All Items"*, select **GlobalProtect Disable Passcode**.

    1. Click the password field to copy the code.

        > ![step2-1password-passcode.png](../assets/images/how-to-screen-share/step2-1password-passcode.png)

    1. On the user's system, in the *"Enter the passcode to disconnect"* prompt, paste the code, then click **Disconnect**.

        > ![step2-globalprotect-disconnect.png](../assets/images/how-to-screen-share/step2-globalprotect-disconnect.png)

    1. ⚠️ **You MUST reconnect to GlobalProtect VPN before exiting the screen-share.**

1. Proceed to Step 3.

---

### Step 3: Determine Connection Method

1. To initiate a screen-share with a company-supported computer, proceed to Step 4.

1. To initiate a screen-share with a non-company-supported computer, proceed to Step 5.

---

### Step 4: Connect via Endpoint Central

1. Open a web browser and navigate to `https://endpointcentral.manageengine.com/webclient#`.

    > ![step4-endpoint-central-login.png](../assets/images/how-to-screen-share/step4-endpoint-central-login.png)

1. Sign in using your *"mydomain.local"* username in the form of `pam-wa-(USERNAME)`.

    1. For instructions on retrieving the *"mydomain.local"* username and login information from Desktop, see `Article 8163`.

        > ![step4-mydomain-login.png](../assets/images/how-to-screen-share/step4-mydomain-login.png)

1. You will then be taken to the company login where you will need to sign in with the same credentials.

    > ![step4-company-login.png](../assets/images/how-to-screen-share/step4-company-login.png)

1. Once signed in, select **Tools** at the top, then select **Remote Control**.

    > ![step4-remote-control.png](../assets/images/how-to-screen-share/step4-remote-control.png)

1. Expand the window by clicking the *"less than"* symbol with three horizontal lines.

    > ![step4-expand-window.png](../assets/images/how-to-screen-share/step4-expand-window.png)

1. Have the caller perform the following:

    1. On your computer, click the Windows Start button then search for and select **About your PC**.

    1. Please read me the name to the right of *"Device name"*. **Note the caller's response in the Service Order.**

1. In the *"Devices"* tab, to the right of *"Total Records"* click the magnifying glass symbol.

    > ![step4-devices-search.png](../assets/images/how-to-screen-share/step4-devices-search.png)

1. Search for the computer name noted in Step 4.6.b.

    > ![step4-search-results.png](../assets/images/how-to-screen-share/step4-search-results.png)

    1. If still not found, proceed to Step 5 to connect via BeyondTrust.

1. In the *"Action"* column, click **Connect**.

    > ![step4-connect.png](../assets/images/how-to-screen-share/step4-connect.png)

1. On the *"endpointcentral.manageengine.com wants to.."* prompt, click **Allow**.

1. On the right side of the window, in the *"View"* section, you should see all of the user's monitors listed.

1. You can select any of the screens to view and control the user's system.

1. You will also see a small notification at the bottom of the screen confirming that you are connected.

    > ![step4-connected.png](../assets/images/how-to-screen-share/step4-connected.png)

1. Return to the Originating Article.

---

### Step 5: Connect via BeyondTrust

1. Using the Web Rep Console:

    1. In your browser, navigate to `https://support.beyondtrustcloud.com/login/downloads/console`.

    1. Leave *"Authenticate Using"* to **SAML Credentials** and click **Login**.

        > ![step5-web-console-login.png](../assets/images/how-to-screen-share/step5-web-console-login.png)

    1. If prompted, enter your company credentials.

    1. On the *"Consoles & Downloads"* page, click **Launch Web Rep Console**.

        > ![step5-launch-web-console.png](../assets/images/how-to-screen-share/step5-launch-web-console.png)

    1. Generate a session key by either clicking **Generate Session Key** under *"My Queues"*, or by clicking **Start** at the top-left.

        > ![step5-generate-session-key.png](../assets/images/how-to-screen-share/step5-generate-session-key.png)

    1. Proceed to Step 5.3.

1. Using the Desktop Representative Console:

    1. Open the BeyondTrust Remote Support application.

    1. On the login screen, leave *"Authenticate Using"* to **SAML Credentials** and click **Login**.

        > ![step5-desktop-console-login.png](../assets/images/how-to-screen-share/step5-desktop-console-login.png)

    1. On the browser page that pops up, complete the login using your company credentials.

    1. At the top-left, click **Start**.

    1. In the *"Start Support Session"* window, click **Generated Session Key**.

        > ![step5-desktop-session-key.png](../assets/images/how-to-screen-share/step5-desktop-session-key.png)

    1. Proceed below.

1. The *"Support Session Key"* window will open.

1. ⚠️ Do not send the link via email, especially if you do not have the user on the line (Callback scenarios).

    > ![step5-session-key-window.png](../assets/images/how-to-screen-share/step5-session-key-window.png)

1. Instruct the user: *In your browser, navigate to `https://support.company.com`.*

1. Provide the session key to the user and have them click **Submit**.

    > ![step5-submit-session-key.png](../assets/images/how-to-screen-share/step5-submit-session-key.png)

1. Instruct the user: *In the pop-up, enter your name and click Submit.*

    > ![step5-enter-name.png](../assets/images/how-to-screen-share/step5-enter-name.png)

1. The user will be listed in queue. Double-click the session.

    > ![step5-session-queue.png](../assets/images/how-to-screen-share/step5-session-queue.png)

1. At the top, click the **Web Chat** tab, then click **Full Customer Client**.

    > ![step5-full-customer-client.png](../assets/images/how-to-screen-share/step5-full-customer-client.png)

1. Instruct the user: *On the prompt, click Accept.*

    > ![step5-user-accept.png](../assets/images/how-to-screen-share/step5-user-accept.png)

1. Instruct the user: *A file will download. Click the file to run it when the download is complete.*

    > ![step5-download-run.png](../assets/images/how-to-screen-share/step5-download-run.png)

1. ⚠️ When you have finished with the screen-share, log out of BeyondTrust. Only 10 users can be logged in at a time.

1. Return to the Originating Article.
