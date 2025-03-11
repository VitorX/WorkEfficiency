# Sort-Object(sort)
## Sort the msedge process with creationdate descending order
    gcim win32_process |where -Property processname -eq "msedge.exe" |select -Property creationdate |sort -Property creationdate -Descending
    
# Get-WmiObject(gwmi)
## List Edge Process and show the command line
    gwmi win32_process |where -Property processname -eq "msedge.exe" |select -Property commandline,processid|fl

# Get-CimInstance(gcim)
## List Edge Process and show the command line
    gcim win32_process |where -Property processname -eq "msedge.exe" |select -Property commandline,processid|fl
## List Namespace or root
    gcim -Namespace root -ClassName __namespace
# Get-CimClass(gcls)
## List Class of namespace
    gcls

## List Class of namespace root
    gcls -Namespace root

## List Class of namespace root
    gcls -Namespace root

# Get-Process(ps)
## Show first process
    $process=ps;$process[0]


# Get-Member(gm)
## List the member of process
The below commands show the process information, but has different members
    ps |gm |grep -i --color=always id
    gwmi win32_process|gm |grep -i --color=always id

# New-SelfSignedCertificate
## Generate the selfsigned certificate for test purpose
After run the following command, we also need to export the certificate and install the certificate to the "Trusted Root Certification Authorities"

    New-SelfSignedCertificate -Type Custom -Subject "CN=cookiedemo" -dnsname "cookiedemo","testsite","testsite1" -KeyUsage DigitalSignature -KeyAlgorithm RSA -KeyLength 2048 -CertStoreLocation "Cert:\localmachine\My" -FriendlyName "cookiedemo"
