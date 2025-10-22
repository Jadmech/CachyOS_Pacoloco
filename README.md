The following files are configured to allow CachyOS systems to point to a pacoloco server on your local network. Once configured on the server and the client, the systems will use the pacoloco server for all CachyOS and Arch Linux repositories.

Note: If you are using the v4 instruction sets for CPUs such as Intel Skylake (2015+) or newer server processors, Intel Core Rocket Lake, Ice Lake, Tiger Lake, and AMD Zen 4 or newer, you'll need to add the v4 to the .yaml file as well.

Setup is as follows:

SERVER:

Create a local pacoloco server.

I used a Docker image from https://github.com/anatol/pacoloco/pkgs/container/pacoloco.

Follow the instructions for setup as provided.

Once the server is up and running, copy the pacoloco.yaml provided into the pacolocal home directory (backing up or overwriting the current file). Config should work as configured. Workes as of 21-Oct-2025.



CLIENTS:

For each client, you'll have to adjust each of the following files (examples are provided - I usually rename the originals - just in case):

* cachyos-mirrorlist

* cachyos-v3-mirrorlist
  
* cachyos-v4-mirrorlist

* mirrorlist

You'll need to update the IP address in each file to point to your server.

Good Luck!

Reach out if I can help.
