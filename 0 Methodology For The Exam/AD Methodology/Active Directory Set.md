We start with a set of credentials as it's an assumed breach scenario. Now what do we do?

> 1: Start by logging into the machine using the provided external IP address via RDP.

> 2: Once logged in, escalate privileges to SYSTEM.

> 3: After gaining SYSTEM, use Mimikatz to dump hashes and extract any credentials, and set up tunneling.

Once you have a set of credentials or a hash:

1. Attempt Kerberoasting and AS-REP roasting.
    
2. Attempt pass-the-hash using Netexec (make sure to try different protocols).
    
3. Login with PsExec if you have SMB access on a compromised machine.

Think outside the box and keep your approach simple. Remember that this is an entry-level pentesting exam so there is not going to be anything crazy on here.
