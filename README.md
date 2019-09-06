# RawCopy
Can copy any files from a Windows operating system even system locked one.

### Credits
This was based on the DirectCopy v2.0 - by Napalm @ NetCore2k

The DirectCopy function invokes a Device Control Code tog et the cluster information about a file.
We then loop through each resulting extent and copy each cluster to a new file. If the file has no
clusters assigned to it the data is stored in the MFT. This means the file data itself is in the
MFT since it would be a waste to allocate an entire cluster of sectors for lets say just 5 bytes.