Start by running an nmap scan for each machine in a separate terminal tab or session. There are 4 interfaces by default in Kali, so use interface 1 for the AD set and interfaces 2–4 for each standalone machine.

After you have a list of the open ports for each machine, go through them one by one and make notes of what you try so you don't end up repeating the same enumeration steps later and wasting time.

Our goal here is to rule out any ports that are unlikely to be useful before we dive deep into enumeration.

For unknown or unusual ports, search the port number on Google and you will most likely find information about it on SpeedGuide. Do a quick check and move on if nothing stands out.

**IMPORTANT:** If HTTP or SSH is running on a non-standard port, it is likely that the port will play some kind of role as the entry point to the machine or become relevant after finding an exploit.