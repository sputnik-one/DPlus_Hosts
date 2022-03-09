# DPlus_Hosts
updated hosts list to support currently unlisted repeaters

credit to original work by PA7LIM and MW0MWZ

to sync this with your device during pistar-update or nightly update jobs you will need to modify /usr/local/sbin/HostFilesUpdate.sh

change this line:
curl --fail -o ${DPlusHOSTS} -s http://www.pistar.uk/downloads/DPlus_Hosts.txt --user-agent "Pi-Star_${pistarCurVersion}"
to:
curl --fail -o ${DPlusHOSTS} -s https://raw.githubusercontent.com/sputnik-one/DPlus_Hosts/main/DPlus_Hosts.txt --user-agent "Pi-Star_${pistarCurVersion}"

Q: Will this break things?
A: Undoubtedly, but so far so good.  I'd backup HostFilesUpdate.sh just to be on the safe side.

Q: It says I can't save that file, the system is read only
A: That's more of a statement, but yeah, that's to prevent SD card corruption.  Cancel out, run 'rpi-rw' to set it read-write and try again.

Q: Why didn't you reach out to the people who maintain the official list and get that fixed instead?
A: I don't like bothering people and it was a good learning exercise.
