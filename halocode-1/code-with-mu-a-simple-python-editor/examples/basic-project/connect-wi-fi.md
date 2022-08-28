# Connect Wi-Fi

Connect HaloCode to the internet.

![](<../../../../.gitbook/assets/0 (1).png>)

**Toggle on Upload mode**

![](<../../../../.gitbook/assets/1 (9).gif>)

**Connect Wi-Fi**

1\. Add an Events block when HaloCode starts up and a Wi-Fi block connect to Wi-Fi() password(). Input the network name and password of the nearby Wi-Fi.

![](<../../../../.gitbook/assets/2 (8).gif>)

2\. We want to know when HaloCode is successfully connected to the internet. Add a Control block wait (), a Wi-Fi block Wi-Fi connected?, and a Lighting block show (). Light up 6 LEDs in color green.

![](<../../../../.gitbook/assets/3 (10).gif>)
