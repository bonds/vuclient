Script for polling CPU load, GPU load, memory load, and root disk % full. 
Sends the results to [VU-Server](https://github.com/SasaKaranovic/VU-Server). 
For use with VU Dials, the nix package. Set the CPUDIAL, GPUDIAL, MEMDIAL, and DSKDIAL 
environment variables to their respective dial UIDs and then run the script. It will
loop every second or so, updating the dials. Assumes the API key for VU-Server is
at /run/vuserver/key, which is the case for the matching nix packaging of
VU-Server.

Only works on Linux because it assumes /proc exists and linux packages like
radeontop are available.
