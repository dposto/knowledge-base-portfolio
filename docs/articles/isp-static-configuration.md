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

* The site is operating on a backup internet connection
* The site is connected through a secondary WAN interface
* The site is completely offline
* Connectivity issues suggest a static IP configuration problem

---

## Solution

### Pre-Step 1: Set Priority

* Set the Service Order priority to **Priority 1**.

---

### Pre-Step 2: Verify Eligibility

This procedure should only be used when:

* The site is already operating on a backup internet connection, or
* The site is completely offline.

> **Note:** In many environments, a secondary WAN interface is configured using DHCP and can be used for temporary connectivity testing.

---

### Pre-Step 3: Verify ISP Static IP Information

Ask the caller:

> *Do you have the site's static IP information from the ISP?*

Record the following information:

* Static IP Address
* Subnet Mask
* Default Gateway

#### If the caller does not have the information

Inform the caller:

> *You'll need to contact your ISP and request your static IP address, subnet mask, and default gateway information.*

* Document the interaction.
* Close the Service Order.

---

### Step 1: Verify Secondary WAN Connectivity

Confirm:

* The ISP modem or router is connected to the secondary WAN interface.
* The secondary WAN connection is active.

Have the caller perform an internet search to verify connectivity.

#### If connectivity succeeds

* Document successful connectivity.
* Proceed to Step 2.

#### If connectivity fails

* Recommend a temporary backup internet solution if appropriate.
* Document findings.
* Close the Service Order.

---

### Step 2: Identify the Workstation

Determine which workstation will be used for testing.

If necessary:

1. Identify the workstation's network connection.
2. Verify the network port currently in use.
3. Document the connection details.
4. Ensure the workstation can be restored to its original state after testing.

Proceed to Step 3.

---

### Step 3: Establish Remote Access

Initiate a screen-sharing session with the workstation if available.

---

### Step 4: Configure the Network Adapter

Open:

* **View Network Connections**
* **Ethernet Adapter Properties**
* **Internet Protocol Version 4 (IPv4)**

Document the current configuration:

* IP Address
* Subnet Mask
* Default Gateway
* Preferred DNS Server
* Alternate DNS Server

Update the adapter using the ISP-provided static IP information.

Configure DNS servers as appropriate for the environment.

Save the changes.

---

### Step 5: Connect the Workstation Directly to the ISP Device

Determine whether the ISP device is:

* An Optical Network Terminal (ONT)
* A modem or router with a single Ethernet port
* A modem or router with multiple available Ethernet ports

Connect the workstation directly to the ISP equipment using the appropriate method.

> ⚠️ **Warning:** This process may temporarily interrupt network connectivity for the site.

---

### Step 6: Test Internet Access

Have the caller browse to:

https://speedtest.net

#### If successful

Record:

* Download Speed
* Upload Speed

Proceed to Step 7.

#### If unsuccessful

Record:

* Exact error message
* Relevant troubleshooting observations

Proceed to Step 7.

---

### Step 7: Restore Original Adapter Configuration

Return the network adapter settings to the values documented in Step 4.

Save the changes.

---

### Step 8: Restore Network Connections

If any network connections were disconnected during testing:

1. Reconnect the workstation to its original network connection.
2. Reconnect the secondary WAN connection if applicable.
3. Verify that network services have recovered.

---

### Step 9: Verify Business-Critical Applications

Confirm connectivity to business-critical applications and services.

Document the results.

#### If connectivity issues remain

* Record the current public IP address.
* Escalate according to established procedures.

---

### Step 10: Escalation

If the issue remains unresolved:

1. Document all troubleshooting performed.
2. Include relevant test results and observations.
3. Assign the Service Order to the appropriate resolver group according to escalation procedures.
