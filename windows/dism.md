# Dism
## Dism enable the feature
    dism /online /enable-feature /featurename:IIS-ASPNET45 /all
    dism /online /enable-feature:WCF-HTTP-Activation45 /all
    dism /online /enable-feature:WCF-TCP-Activation45 /all
    dism /online /enable-feature:WCF-Pipe-Activation45 /all
    dism /online /enable-feature:WCF-MSMQ-Activation45 /all
    dism /online /enable-feature:WCF-TCP-PortSharing45 /all
