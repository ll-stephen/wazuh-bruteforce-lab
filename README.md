This project demonstrates configuring a Wazuh manager and agent to detect SSH brute-force activity in a small lab network. 

## Lab Topology

- Wazuh Manager: Kali Linux VM
- Victim: Ubuntu VM (PP-Victim) with Wazuh agent installed
- Attacker: Kali/Parrot/etc. performing SSH brute force attempts

## Wazuh Configuration Summary

- Wazuh manager installed and running on Kali.
- Wazuh agent install on PP-Victim and enrolled with the manager.
- Authentication logs from PP-Victim forwarded to manager.
- Built-in Wazuh rules trigger a Level 10 alerts for multiple failed SSH logins in a shot period. 

## Evidence

See:
- 'evidence/Level10_brute_force_evidence.txt'

  Parsed Wazuh alert showing:
  - Rule ID and **Level 10**
  - Agent 'PP-Victim (192.168.56.111)'
  - Brute-force attempts against 'brutetgt'
  - Corresponding log snippet.

-'screenshots/'

  - Wazuh manager status
  - Agent list
  - Alerts view and Level 10 alert evidence

## Notes

 - Sensitivite data (keys, tokens, real passwords) are excluded.
 - Rotated logs and bulky raw files are not committed to keep repo lean. 

