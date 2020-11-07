---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5AECCBD7-1FDE-4217-9F59-36328062E669
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkSecurityGroup.md
ms.openlocfilehash: 46106379160ee593748a95489c2641d43114d863
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670537"
---
# <span data-ttu-id="d6036-101">Get-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="d6036-101">Get-AzNetworkSecurityGroup</span></span>

## <span data-ttu-id="d6036-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d6036-102">SYNOPSIS</span></span>
<span data-ttu-id="d6036-103">Hálózati biztonsági csoportba kerül.</span><span class="sxs-lookup"><span data-stu-id="d6036-103">Gets a network security group.</span></span>

## <span data-ttu-id="d6036-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d6036-104">SYNTAX</span></span>

### <span data-ttu-id="d6036-105">Nincs kibontva</span><span class="sxs-lookup"><span data-stu-id="d6036-105">NoExpand</span></span>
```
Get-AzNetworkSecurityGroup [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d6036-106">Bővíteni</span><span class="sxs-lookup"><span data-stu-id="d6036-106">Expand</span></span>
```
Get-AzNetworkSecurityGroup -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d6036-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="d6036-107">DESCRIPTION</span></span>
<span data-ttu-id="d6036-108">A **Get-AzNetworkSecurityGroup** parancsmag Azure hálózati biztonsági csoportot kap.</span><span class="sxs-lookup"><span data-stu-id="d6036-108">The **Get-AzNetworkSecurityGroup** cmdlet gets an Azure network security group.</span></span>

## <span data-ttu-id="d6036-109">Példák</span><span class="sxs-lookup"><span data-stu-id="d6036-109">EXAMPLES</span></span>

### <span data-ttu-id="d6036-110">1: meglévő hálózati biztonsági csoport beolvasása</span><span class="sxs-lookup"><span data-stu-id="d6036-110">1: Retrieve an existing network security group</span></span>
```
Get-AzNetworkSecurityGroup -Name nsg1 -ResourceGroupName "rg1"

Name                        : nsg1
ResourceGroupName           : rg1
Location                    : eastus
Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/provider
                              s/Microsoft.Network/networkInterfaces/nsg1
Etag                        : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid                : 00000000-0000-0000-0000-000000000000
ProvisioningState           : Succeeded
Tags                        :
VirtualMachine              : null
IpConfigurations            : [
                                {
                                  "Name": "ipconfig1",
                                  "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                  "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1
                              /providers/Microsoft.Network/networkInterfaces/nsg1/ipConfigurations/ipcon
                              fig1",
                                  "PrivateIpAddress": "x.x.x.x",
                                  "PrivateIpAllocationMethod": "Dynamic",
                                  "Subnet": {
                                    "Delegations": [],
                                    "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1
                              /providers/Microsoft.Network/virtualNetworks/vnetcrptestps2673/subnets/subnetcrptestp
                              s2673",
                                    "ServiceAssociationLinks": []
                                  },
                                  "PublicIpAddress": {
                                    "IpTags": [],
                                    "Zones": [],
                                    "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1
                              /providers/Microsoft.Network/publicIPAddresses/pubipcrptestps2673"
                                  },
                                  "ProvisioningState": "Succeeded",
                                  "PrivateIpAddressVersion": "IPv4",
                                  "LoadBalancerBackendAddressPools": [],
                                  "LoadBalancerInboundNatRules": [],
                                  "Primary": true,
                                  "ApplicationGatewayBackendAddressPools": [],
                                  "ApplicationSecurityGroups": []
                                }
                              ]
DnsSettings                 : {
                                "DnsServers": [],
                                "AppliedDnsServers": [],
                                "InternalDomainNameSuffix": "xxxxxxxxxxxxxxx.xx.internal.cloudapp.net"
                              }
EnableIPForwarding          : False
EnableAcceleratedNetworking : False
NetworkSecurityGroup        : null
Primary                     :
MacAddress                  :
```

<span data-ttu-id="d6036-111">Ez a parancs a "nsg1" erőforráscsoport "rg1" erőforráscsoporthoz tartozó Azure Network biztonsági csoportjának tartalmát jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="d6036-111">This command returns contents of Azure network security group "nsg1" in resource group "rg1"</span></span>

### <span data-ttu-id="d6036-112">2: a meglévő hálózati biztonsági csoportok listázása szűréssel</span><span class="sxs-lookup"><span data-stu-id="d6036-112">2: List existing network security groups using filtering</span></span>
```
Get-AzNetworkSecurityGroup -Name nsg*

Name                        : nsg1
ResourceGroupName           : rg1
Location                    : eastus
Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/provider
                              s/Microsoft.Network/networkInterfaces/nsg1
Etag                        : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid                : 00000000-0000-0000-0000-000000000000
ProvisioningState           : Succeeded
Tags                        :
VirtualMachine              : null
IpConfigurations            : [
                                {
                                  "Name": "ipconfig1",
                                  "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                  "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1
                              /providers/Microsoft.Network/networkInterfaces/nsg1/ipConfigurations/ipcon
                              fig1",
                                  "PrivateIpAddress": "x.x.x.x",
                                  "PrivateIpAllocationMethod": "Dynamic",
                                  "Subnet": {
                                    "Delegations": [],
                                    "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1
                              /providers/Microsoft.Network/virtualNetworks/vnetcrptestps2673/subnets/subnetcrptestp
                              s2673",
                                    "ServiceAssociationLinks": []
                                  },
                                  "PublicIpAddress": {
                                    "IpTags": [],
                                    "Zones": [],
                                    "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1
                              /providers/Microsoft.Network/publicIPAddresses/pubipcrptestps2673"
                                  },
                                  "ProvisioningState": "Succeeded",
                                  "PrivateIpAddressVersion": "IPv4",
                                  "LoadBalancerBackendAddressPools": [],
                                  "LoadBalancerInboundNatRules": [],
                                  "Primary": true,
                                  "ApplicationGatewayBackendAddressPools": [],
                                  "ApplicationSecurityGroups": []
                                }
                              ]
DnsSettings                 : {
                                "DnsServers": [],
                                "AppliedDnsServers": [],
                                "InternalDomainNameSuffix": "xxxxxxxxxxxxxxx.xx.internal.cloudapp.net"
                              }
EnableIPForwarding          : False
EnableAcceleratedNetworking : False
NetworkSecurityGroup        : null
Primary                     :
MacAddress                  :
```

<span data-ttu-id="d6036-113">Ez a parancs a "NSG" kezdetű Azure hálózati biztonsági csoportok tartalmát ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="d6036-113">This command returns contents of Azure network security groups that start with "nsg"</span></span>

## <span data-ttu-id="d6036-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d6036-114">PARAMETERS</span></span>

### <span data-ttu-id="d6036-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6036-115">-DefaultProfile</span></span>
<span data-ttu-id="d6036-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d6036-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6036-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="d6036-117">-ExpandResource</span></span>
```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6036-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d6036-118">-Name</span></span>
<span data-ttu-id="d6036-119">Annak a hálózati biztonsági csoportnak a neve, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="d6036-119">Specifies the name of the network security group that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="d6036-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6036-120">-ResourceGroupName</span></span>
<span data-ttu-id="d6036-121">Annak az erőforráscsoport-csoportnak a neve, amelyhez a hálózat biztonsági csoportja tartozik.</span><span class="sxs-lookup"><span data-stu-id="d6036-121">Specifies the name of the resource group that the network security group belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="d6036-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6036-122">CommonParameters</span></span>
<span data-ttu-id="d6036-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d6036-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6036-124">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d6036-124">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6036-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d6036-125">INPUTS</span></span>

### <span data-ttu-id="d6036-126">System. String</span><span class="sxs-lookup"><span data-stu-id="d6036-126">System.String</span></span>

## <span data-ttu-id="d6036-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d6036-127">OUTPUTS</span></span>

### <span data-ttu-id="d6036-128">Microsoft. Azure. commands. Network. models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="d6036-128">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="d6036-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d6036-129">NOTES</span></span>

## <span data-ttu-id="d6036-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d6036-130">RELATED LINKS</span></span>

[<span data-ttu-id="d6036-131">Új – AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="d6036-131">New-AzNetworkSecurityGroup</span></span>](./New-AzNetworkSecurityGroup.md)

[<span data-ttu-id="d6036-132">Remove-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="d6036-132">Remove-AzNetworkSecurityGroup</span></span>](./Remove-AzNetworkSecurityGroup.md)

[<span data-ttu-id="d6036-133">Set-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="d6036-133">Set-AzNetworkSecurityGroup</span></span>](./Set-AzNetworkSecurityGroup.md)


