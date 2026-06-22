# Reconfiguring FOM / WFM to Determine Center's ISP Static Configuration Status

This article provides procedures for determining if the static configuration is set properly in the ISP's network equipment (modem or router) using a Front Office Machine (FOM) or Wi-Fi Machine (WFM).

|                   |                        |
| ----------------- | ---------------------- |
| **Author**        | David Posto            |
| **Document Type** | Knowledge Base Article |
| **Audience**      | Help Desk Agents       |
| **Last Updated**  | June 2026              |

---

## Symptoms

How to determine if the static configuration is set properly in the ISP's network equipment (modem or router).

---

## Solution

### Pre-Step 1: Set Priority

1. Set [Priority] to 1.

---

### Pre-Step 2: Important Information

1. ⚠️ This article is only to be used if the center is already on a backup internet connection (WAN2, hotspot, etc.) and needs to verify the ISP's static configuration before switching back to the primary connection.

1. WAN2 on the Fortigate is a DHCP port which is typically either occupied by a cellular backup or is without a connection.

---

### Pre-Step 3: Verify Store has IP Information from ISP

1. Ask the caller: *Do you have the center's IP information from their internet service provider (ISP)?*

    1. If Yes:

        1. **Note the following information in the Service Order:**

            1. Static IP Address:

            1. Subnet Mask:

            1. Default Gateway:

    1. If No:

        1. Inform the caller:

            > *You will need to contact your ISP and request your Static IP Address, Subnet Mask, and Default Gateway.*

            > *When you have that information, please contact the Service Desk and reference Service Order #######.*

        1. Close the Service Order.

1. Proceed below.

---

### Step 1: Verify the ISP's Modem / Router is Connected to WAN2 of Fortigate and has Connectivity

1. ⚠️ This process is not intended for use with a cellular backup.

    1. If the store is using a cellular backup:

        1. If the store has not yet troubleshot store connectivity, see `Article 4182` for instructions.

        1. If the store needs their cellular backup whitelisted, see `Article 6739` for instructions.

        1. Close the Service Order.

1. Have the caller: *Please verify the network cable from your ISP's modem or router is plugged into WAN2 on the Fortigate.*

1. Wait for a few minutes for the network to come back up, then have the caller: *Perform an internet search to verify the connection is working.*

    1. If the connection was successful:

        1. **Note that connecting to WAN2 established a connection.**

    1. If the connection was unsuccessful:

        1. Inform the caller:

            > *We recommend a cellular backup such as the T-Mobile solution recommended by the franchisor. That can take several days to arrive.*

            > *If you need one sooner, you can go to a different provider.*

            > *After the cellular connection is set up, you will need to connect the cellular device to the WAN2 on the Fortigate.*

        1. See `Article 8524` if the caller needs instructions installing a 4G LTE / 5G connection or whitelisting a cellular backup.

        1. Close the Service Order.

1. Proceed below.

---

### Step 2: Determine if Center has WFM or a FOM

1. Ask the caller: *Are you using a WFM or FOM?*

    1. If FOM, determine which port the device is located on.

        1. Have the caller:

            1. Check the front panel of the Fortigate to determine which ports (1–5) are active.

            1. Disconnect the ethernet cable from the back of the FOM.

            1. On the front panel of the Fortigate, determine which port's LEDs turned off.

            1. The set of LEDs that turned off are the port the FOM is located on.

                1. **Note the port number in the Service Order.**

            1. Reconnect the ethernet cable to the back of the FOM.

        1. Proceed to Step 3.

    1. If WFM, proceed to Step 3.

---

### Step 3: Initiate a Screen-Share Session with the FOM or WFM

1. See `Article 3071` for instructions.

---

### Step 4: Configure the WFM / FOM's Ethernet Network Adapter with the Information Provided by the ISP

1. In the Windows Search Bar at the bottom, search for and select **View network connections**.

1. Right-click the Ethernet network adapter and select **Properties**.

1. Under *"This connection uses the following items:"* click to highlight **Internet Protocol Version 4** and select **Properties**.

1. **Note the IP information currently in use to be used in Step 7:**

    1. Static IP Address:

    1. Subnet Mask:

    1. Default Gateway:

    1. Preferred DNS:

    1. Alternate DNS servers:

1. Change the *"Use the following IP address:"* to match the information provided by the ISP noted in Pre-Step 3.

1. Change the Preferred DNS and Alternate DNS servers to appropriate servers (i.e. 8.8.8.8, 4.2.2.1).

1. Click **OK** to save the changes.

---

### Step 5: Connect FOM / WFM to ISP's Modem / Router

1. Have the caller: *Trace the cable plugged into WAN2 on the Fortigate to your ISP's modem / router.*

1. Ask the caller: *Is the device an Optical Network Terminal (ONT or fiber modem) or does it have only one ethernet port?*

    1. If Yes for either:

        1. Have the caller:

            1. ⚠️ *This process will take the store's entire network down. If the store currently has customers, inform them of the following:*

                1. Wait until there is a lull in customers before we proceed.

                1. If you need to, call the Service Desk back when you are not busy and reference the Service Order Number.

            1. Disconnect the WAN2 cable from your ISP's modem / router and connect your FOM / WFM to the same port on the ISP's modem / router.

            1. If the device is an ONT, remember which port it was plugged into as only that port can be used.

    1. If the device has an available ethernet port and is not an ONT:

        1. Have the caller: *Plug the FOM / WFM directly into an available port on your ISP's modem / router.*

1. Proceed to Step 6.

---

### Step 6: Determine if FOM / WFM is Able to Access the Internet

1. Have the caller: *Attempt to access the webpage https://speedtest.net.*

    1. If site connects:

        1. **Note results after running a speed test:**

            1. Download Mbps:

            1. Upload Mbps:

        1. Proceed to Step 7.

    1. If site does not connect:

        1. Have the caller: *Copy down the error that was received.*

        1. Inform the caller: *Someone at the store needs to reach out to your primary ISP informing them of the static IP configuration issue.*

        1. Proceed to Step 7.

---

### Step 7: Return WFM / FOM Ethernet Adapter Settings to Original Settings

1. Initiate a screen-share with the FOM / WFM if possible.

    1. If the FOM / WFM has connectivity, see `Article 3071` for instructions.

    1. If the FOM / WFM does not have connectivity, provide the instructions below to the caller.

1. In the Windows Search Bar at the bottom, search for and select **View network connections**.

1. Right-click the Ethernet network adapter and select **Properties**.

1. Under *"This connection uses the following items:"* click to highlight **Internet Protocol Version 4** and select **Properties**.

1. Enter the IP information noted in Step 4.

1. Click **OK** to save the changes.

1. If WAN2 of the Fortigate was disconnected from the ISP device in Step 5, proceed to Step 8.

1. If WAN2 of the Fortigate is connected to the ISP, proceed to Step 9.

---

### Step 8: Connect Fortigate WAN2 Back to ISP Network Device if Removed During Step 5

1. If WAN2 of the Fortigate was disconnected from the ISP device in Step 5:

    1. Provide the following instructions:

        1. Disconnect the FOM / WFM from the ISP's modem / router and plug it back into the port of the Fortigate it was originally connected to.

        1. Plug the network cable from WAN2 on the Fortigate back into the ISP's modem / router.

    1. Wait a few minutes for the network to come up.

        1. If the network does not come back up, move to `Article 4182`.

1. Proceed to Step 9.

---

### Step 9: Check Connection to AMS and USM

1. Have the caller: *Check the connection to AMS and USM to see if they are working.*

    1. If both are not working:

        1. Determine the currently used Public IP address and make note of it.

        1. Proceed to Step 10.

    1. If AMS is giving a Dynamics Integration Error, move to `Article 9463`.

    1. If USM is not working, move to `Article 2857`.

1. If the site connected in Step 6, proceed to Step 10.

1. If the site did not connect in Step 6, close the Service Order.

---

### Step 10: Assign Service Order to the Appropriate Resolver Group

1. See `Article 7614` for instructions.
