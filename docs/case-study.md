# Home SOC Lab Case Study

## Project Summary

Built a home SOC lab using Wazuh to monitor a Linux endpoint, simulate attacker behavior from Kali Linux, detect SSH brute-force activity, and apply firewall defenses using UFW.

## Problem

Organizations need visibility into endpoint activity and the ability to detect suspicious login behavior such as brute-force attacks.

## Solution

A Wazuh SIEM environment was configured to collect logs from a Linux endpoint. Kali Linux was used to simulate attack traffic with Nmap and Hydra. Wazuh alerts were reviewed through Discover/Threat Hunting, and UFW firewall controls were applied to reduce attack effectiveness.

## Outcome

The lab successfully demonstrated a basic SOC workflow: attack simulation, log collection, threat detection, analysis, and mitigation.
