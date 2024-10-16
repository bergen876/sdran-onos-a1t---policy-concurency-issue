# SDRAN ONOS A1T - Policy Concurrency Issue

## Overview
This repository demonstrates a Proof of Concept (PoC) Denial of Service (DoS) attack targeting the **ONOS A1 Termination (a1t)** module within the **SDRAN-in-a-box** deployment. The attack exploits a policy concurrency vulnerability by replaying multiple concurrent A1 policies, resulting in service termination and impacting the management of A1 policies within the **SD-RAN ORAN** deployment.

## Attack Description
The **ONOS A1 Termination** component in **SD-RAN ORAN** is vulnerable to a DoS attack through the continuous replay of concurrent HTTP-based policies. By exploiting this issue, attackers can disrupt the service, causing it to crash and rendering it unable to manage A1 policies effectively.

## Environment
- **SDRAN-in-a-Box Version**: v1.4.3
- **Installation Guide**: [SDRAN-in-a-Box Installation Guide](#) https://docs.sd-ran.org/master/sdran-in-a-box/docs/Installation_RANSim_RIMDEO_TS.html

## Attack Steps

### 1. Setup
- Download and set up the **SDRAN-in-a-Box** environment.

### 2. Identify A1T IP and Port
- After deployment, run `make test-rnib` to identify the IP and port of the **a1t** component.

### 3. Execute the Attack
- Use the provided `a1dos.py` script to send multiple concurrent requests to the **ONOS A1 Termination** component.
- Adjust the intensity of the attack by modifying the number of threads in the script.

### 4. Crash Verification
- Monitor the **a1t**

## PoC Video
- Watch the video showcasing the PoC running on a Vagrant VM with Ubuntu 20.04.
  
