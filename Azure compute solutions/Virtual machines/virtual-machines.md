Resource that gives us the flexibility of virtualization without having to buy and maintain the physical hardware that runs it.

# Design considerations and extensions

![image](https://user-images.githubusercontent.com/12272451/200029328-bc786df9-61c5-4b8a-b4b3-6998b58c33c5.png)

The best way to determine the appropiate VM size is to consider the type of workload your VM needs to run. The following table helps with that.

![image](https://user-images.githubusercontent.com/12272451/200029632-caa71cc9-8609-4779-b31a-615b28df8bfb.png)

Virtual machines have the following availability options:

![image](https://user-images.githubusercontent.com/12272451/200030264-082f393d-c71e-47bb-a675-b934dfb15e49.png)

In regards to Availability sets we should take in account:

![image](https://user-images.githubusercontent.com/12272451/200030536-1fece38a-23f8-459c-9bcd-990a61aef4e7.png)

# Create Virtual Machine

**Az cli**
```
az vm create --resource-group 'MyResourceGroup' --name 'MyVM' --image 'OpenLogic:CentOS:7.5:7.5.20180815' --admin-username 'username' --admin-password 'Password123!' --location 'frn00006'
```


**Powershell**
```
New-AzVm `
    -ResourceGroupName 'myResourceGroup' `
    -Name 'myVM' `
    -Location 'East US' `
    -VirtualNetworkName 'myVnet' `
    -SubnetName 'mySubnet' `
    -SecurityGroupName 'myNetworkSecurityGroup' `
    -PublicIpAddressName 'myPublicIpAddress' `
    -OpenPorts 80,3389
 ```
