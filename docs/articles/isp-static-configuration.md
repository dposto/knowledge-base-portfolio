# Verifying ISP Static IP Configuration Using a Back Office Workstation

This article provides procedures for verifying whether a site's ISP-provided static IP configuration is correctly configured and reachable by directly connecting a workstation to the ISP equipment.

|                       |                        |
| --------------------- | ---------------------- |
| **Author**            | David Posto            |
| **Document Type**     | Knowledge Base Article |
| **Audience**          | IT Support Agents      |
| **Portfolio Version** | June 2026              |

---

## Symptoms

Use this procedure when troubleshooting a site that may have an ISP-side static IP configuration issue.

This process may be required when:

1. The site is operating on a backup internet connection.
2. The site is connected through a secondary WAN interface.
3. The site is completely offline.
4. Connectivity issues suggest a static IP configuration problem.

---

## Solution

### Pre-Step 1: Set Priority

1. Set the Service Order priority to **Priority 1**.

---

### Pre-Step 2: Verify Eligibility

1. Verify one of the following conditions exists:

   1. The site is already operating on a backup internet connection.
   2. The site is completely offline.

> **Note:** In many environments, a secondary WAN interface is configured using DHCP and can be used for temporary connectivity testing.

---

### Pre-Step 3: Verify ISP Static IP Information

1. Ask the caller:

   > *Do you have the site's static IP information from the ISP?*

2. Record the following information:

   1. Static IP Address
   2. Subnet Mask
   3. Default Gateway

3. If the caller does not have the information:

   1. Inform the caller:

      > *You'll need to contact your ISP and request your static IP address, subnet mask, and default gateway information.*

   2. Document the interaction.

   3. Close the Service Order.

---

### Step 1: Verify Secondary WAN Connectivity

1. Confirm the following:

   1. The ISP modem or router is connected to the secondary WAN interface.
   2. The secondary WAN connection is active.

2. Have the caller perform an internet search to verify connectivity.

3. If connectivity succeeds:

   1. Document successful connectivity.
   2. Proceed to Step 2.

4. If connectivity fails:

   1. Recommend a temporary backup internet solution if appropriate.
   2. Document findings.
   3. Close the Service Order.

---

### Step 2: Identify the Workstation

1. Determine which workstation will be used for testing.

2. If necessary:

   1. Identify the workstation's network connection.
   2. Verify the network port currently in use.
   3. Document the connection details.
   4. Ensure the workstation can be restored to its original state after testing.

3. Proceed to Step 3.

---

### Step 3: Establish Remote Access

1. Initiate a screen-sharing session with the workstation if available.

---

### Step 4: Configure the Network Adapter

1. Open:

   1. **View Network Connections**
   2. **Ethernet Adapter Properties**
   3. **Internet Protocol Version 4 (IPv4)**

2. Document the current configuration:

   1. IP Address
   2. Subnet Mask
   3. Default Gateway
   4. Preferred DNS Server
   5. Alternate DNS Server

3. Update the adapter using the ISP-provided static IP information.

4. Configure DNS servers as appropriate for the environment.

5. Save the changes.

---

### Step 5: Connect the Workstation Directly to the ISP Device

1. Determine whether the ISP device is:

   1. An Optical Network Terminal (ONT)
   2. A modem or router with a single Ethernet port
   3. A modem or router with multiple available Ethernet ports

2. Connect the workstation directly to the ISP equipment using the appropriate method.

> ⚠️ **Warning:** This process may temporarily interrupt network connectivity for the site.

---

### Step 6: Test Internet Access

1. Have the caller browse to:

   https://speedtest.net

2. If the test is successful:

   1. Record:

      1. Download Speed
      2. Upload Speed
   2. Proceed to Step 7.

3. If the test is unsuccessful:

   1. Record:

      1. Exact error message
      2. Relevant troubleshooting observations
   2. Proceed to Step 7.

---

### Step 7: Restore Original Adapter Configuration

1. Return the network adapter settings to the values documented in Step 4.

2. Save the changes.

---

### Step 8: Restore Network Connections

1. If any network connections were disconnected during testing:

   1. Reconnect the workstation to its original network connection.
   2. Reconnect the secondary WAN connection if applicable.
   3. Verify that network services have recovered.

---

### Step 9: Verify Business-Critical Applications

1. Confirm connectivity to business-critical applications and services.

2. Document the results.

3. If connectivity issues remain:

   1. Record the current public IP address.
   2. Escalate according to established procedures.

---

### Step 10: Escalation

1. If the issue remains unresolved:

   1. Document all troubleshooting performed.
   2. Include relevant test results and observations.
   3. Assign the Service Order according to established escalation procedures.
