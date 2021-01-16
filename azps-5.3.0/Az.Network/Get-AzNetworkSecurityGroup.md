---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5AECCBD7-1FDE-4217-9F59-36328062E669
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkSecurityGroup.md
ms.openlocfilehash: ee140a968741269b8bebebeb7b179f8ad74e35c8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98379972"
---
# <span data-ttu-id="c0aee-101">Get-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="c0aee-101">Get-AzNetworkSecurityGroup</span></span>

## <span data-ttu-id="c0aee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0aee-102">SYNOPSIS</span></span>
<span data-ttu-id="c0aee-103">Hálózati biztonsági csoportot kap.</span><span class="sxs-lookup"><span data-stu-id="c0aee-103">Gets a network security group.</span></span>

## <span data-ttu-id="c0aee-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c0aee-104">SYNTAX</span></span>

### <span data-ttu-id="c0aee-105">NoExpand</span><span class="sxs-lookup"><span data-stu-id="c0aee-105">NoExpand</span></span>
```
Get-AzNetworkSecurityGroup [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c0aee-106">Kibontás</span><span class="sxs-lookup"><span data-stu-id="c0aee-106">Expand</span></span>
```
Get-AzNetworkSecurityGroup -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c0aee-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c0aee-107">DESCRIPTION</span></span>
<span data-ttu-id="c0aee-108">A **Get-AzNetworkSecurityGroup** parancsmag egy Azure-hálózati biztonsági csoportot kap.</span><span class="sxs-lookup"><span data-stu-id="c0aee-108">The **Get-AzNetworkSecurityGroup** cmdlet gets an Azure network security group.</span></span>

## <span data-ttu-id="c0aee-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c0aee-109">EXAMPLES</span></span>

### <span data-ttu-id="c0aee-110">1. példa: Meglévő hálózatbiztonsági csoport lekérése</span><span class="sxs-lookup"><span data-stu-id="c0aee-110">Example 1: Retrieve an existing network security group</span></span>
```powershell
Get-AzNetworkSecurityGroup -Name nsg1 -ResourceGroupName "rg1"

Name                        : nsg1
ResourceGroupName           : rg1
Location                    : eastus
Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/provider
                              s/Microsoft.Network/networkSecurityGroups/nsg1
Etag                        : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid                : 00000000-0000-0000-0000-000000000000
ProvisioningState           : Succeeded
Tags                        :
SecurityRules               : []
DefaultSecurityRules        : [
                                {
                                  "Name": "AllowVnetInBound",
                                  "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                  "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/provide
                              rs/Microsoft.Network/networkSecurityGroups/nsg1/defaultSecurityRules/AllowVnetInBound",
                                  "Description": "Allow inbound traffic from all VMs in VNET",
                                  "Protocol": "*",
                                  "SourcePortRange": [
                                    "*"
                                  ],
                                  "DestinationPortRange": [
                                    "*"
                                  ],
                                  "SourceAddressPrefix": [
                                    "VirtualNetwork"
                                  ],
                                  "DestinationAddressPrefix": [
                                    "VirtualNetwork"
                                  ],
                                  "Access": "Allow",
                                  "Priority": 65000,
                                  "Direction": "Inbound",
                                  "ProvisioningState": "Succeeded",
                                  "SourceApplicationSecurityGroups": [],
                                  "DestinationApplicationSecurityGroups": []
                                },
                                {
                                  "Name": "AllowAzureLoadBalancerInBound",
                                  "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                  "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/provide
                              rs/Microsoft.Network/networkSecurityGroups/nsg1/defaultSecurityRules/AllowAzureLoadBalancerInBou
                              nd",
                                  "Description": "Allow inbound traffic from azure load balancer",
                                  "Protocol": "*",
                                  "SourcePortRange": [
                                    "*"
                                  ],
                                  "DestinationPortRange": [
                                    "*"
                                  ],
                                  "SourceAddressPrefix": [
                                    "AzureLoadBalancer"
                                  ],
                                  "DestinationAddressPrefix": [
                                    "*"
                                  ],
                                  "Access": "Allow",
                                  "Priority": 65001,
                                  "Direction": "Inbound",
                                  "ProvisioningState": "Succeeded",
                                  "SourceApplicationSecurityGroups": [],
                                  "DestinationApplicationSecurityGroups": []
                                },
                                {
                                  "Name": "DenyAllInBound",
                                  "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                  "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/provide
                              rs/Microsoft.Network/networkSecurityGroups/nsg1/defaultSecurityRules/DenyAllInBound",
                                  "Description": "Deny all inbound traffic",
                                  "Protocol": "*",
                                  "SourcePortRange": [
                                    "*"
                                  ],
                                  "DestinationPortRange": [
                                    "*"
                                  ],
                                  "SourceAddressPrefix": [
                                    "*"
                                  ],
                                  "DestinationAddressPrefix": [
                                    "*"
                                  ],
                                  "Access": "Deny",
                                  "Priority": 65500,
                                  "Direction": "Inbound",
                                  "ProvisioningState": "Succeeded",
                                  "SourceApplicationSecurityGroups": [],
                                  "DestinationApplicationSecurityGroups": []
                                },
                                {
                                  "Name": "AllowVnetOutBound",
                                  "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                  "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/provide
                              rs/Microsoft.Network/networkSecurityGroups/nsg1/defaultSecurityRules/AllowVnetOutBound",
                                  "Description": "Allow outbound traffic from all VMs to all VMs in VNET",
                                  "Protocol": "*",
                                  "SourcePortRange": [
                                    "*"
                                  ],
                                  "DestinationPortRange": [
                                    "*"
                                  ],
                                  "SourceAddressPrefix": [
                                    "VirtualNetwork"
                                  ],
                                  "DestinationAddressPrefix": [
                                    "VirtualNetwork"
                                  ],
                                  "Access": "Allow",
                                  "Priority": 65000,
                                  "Direction": "Outbound",
                                  "ProvisioningState": "Succeeded",
                                  "SourceApplicationSecurityGroups": [],
                                  "DestinationApplicationSecurityGroups": []
                                },
                                {
                                  "Name": "AllowInternetOutBound",
                                  "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                  "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/provide
                              rs/Microsoft.Network/networkSecurityGroups/nsg1/defaultSecurityRules/AllowInternetOutBound",
                                  "Description": "Allow outbound traffic from all VMs to Internet",
                                  "Protocol": "*",
                                  "SourcePortRange": [
                                    "*"
                                  ],
                                  "DestinationPortRange": [
                                    "*"
                                  ],
                                  "SourceAddressPrefix": [
                                    "*"
                                  ],
                                  "DestinationAddressPrefix": [
                                    "Internet"
                                  ],
                                  "Access": "Allow",
                                  "Priority": 65001,
                                  "Direction": "Outbound",
                                  "ProvisioningState": "Succeeded",
                                  "SourceApplicationSecurityGroups": [],
                                  "DestinationApplicationSecurityGroups": []
                                },
                                {
                                  "Name": "DenyAllOutBound",
                                  "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                  "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/provide
                              rs/Microsoft.Network/networkSecurityGroups/nsg1/defaultSecurityRules/DenyAllOutBound",
                                  "Description": "Deny all outbound traffic",
                                  "Protocol": "*",
                                  "SourcePortRange": [
                                    "*"
                                  ],
                                  "DestinationPortRange": [
                                    "*"
                                  ],
                                  "SourceAddressPrefix": [
                                    "*"
                                  ],
                                  "DestinationAddressPrefix": [
                                    "*"
                                  ],
                                  "Access": "Deny",
                                  "Priority": 65500,
                                  "Direction": "Outbound",
                                  "ProvisioningState": "Succeeded",
                                  "SourceApplicationSecurityGroups": [],
                                  "DestinationApplicationSecurityGroups": []
                                }
                              ]
NetworkInterfaces           : []
Subnets                     : []
```

<span data-ttu-id="c0aee-111">Ez a parancs az "rg1" erőforráscsoportban visszaadja az "nsg1" Azure-hálózat biztonsági csoportjának tartalmát.</span><span class="sxs-lookup"><span data-stu-id="c0aee-111">This command returns contents of Azure network security group "nsg1" in resource group "rg1"</span></span>

### <span data-ttu-id="c0aee-112">2. példa: Meglévő hálózatbiztonsági csoportok felsorolása szűrés használatával</span><span class="sxs-lookup"><span data-stu-id="c0aee-112">Example 2: List existing network security groups using filtering</span></span>
```powershell
Get-AzNetworkSecurityGroup -Name nsg*

Name                        : nsg1
ResourceGroupName           : rg1
Location                    : eastus
Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/provider
                              s/Microsoft.Network/networkSecurityGroups/nsg1
Etag                        : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid                : 00000000-0000-0000-0000-000000000000
ProvisioningState           : Succeeded
Tags                        :
SecurityRules               : []
DefaultSecurityRules        : [
                                {
                                  "Name": "AllowVnetInBound",
                                  "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                  "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/provide
                              rs/Microsoft.Network/networkSecurityGroups/nsg1/defaultSecurityRules/AllowVnetInBound",
                                  "Description": "Allow inbound traffic from all VMs in VNET",
                                  "Protocol": "*",
                                  "SourcePortRange": [
                                    "*"
                                  ],
                                  "DestinationPortRange": [
                                    "*"
                                  ],
                                  "SourceAddressPrefix": [
                                    "VirtualNetwork"
                                  ],
                                  "DestinationAddressPrefix": [
                                    "VirtualNetwork"
                                  ],
                                  "Access": "Allow",
                                  "Priority": 65000,
                                  "Direction": "Inbound",
                                  "ProvisioningState": "Succeeded",
                                  "SourceApplicationSecurityGroups": [],
                                  "DestinationApplicationSecurityGroups": []
                                },
                                {
                                  "Name": "AllowAzureLoadBalancerInBound",
                                  "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                  "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/provide
                              rs/Microsoft.Network/networkSecurityGroups/nsg1/defaultSecurityRules/AllowAzureLoadBalancerInBou
                              nd",
                                  "Description": "Allow inbound traffic from azure load balancer",
                                  "Protocol": "*",
                                  "SourcePortRange": [
                                    "*"
                                  ],
                                  "DestinationPortRange": [
                                    "*"
                                  ],
                                  "SourceAddressPrefix": [
                                    "AzureLoadBalancer"
                                  ],
                                  "DestinationAddressPrefix": [
                                    "*"
                                  ],
                                  "Access": "Allow",
                                  "Priority": 65001,
                                  "Direction": "Inbound",
                                  "ProvisioningState": "Succeeded",
                                  "SourceApplicationSecurityGroups": [],
                                  "DestinationApplicationSecurityGroups": []
                                },
                                {
                                  "Name": "DenyAllInBound",
                                  "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                  "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/provide
                              rs/Microsoft.Network/networkSecurityGroups/nsg1/defaultSecurityRules/DenyAllInBound",
                                  "Description": "Deny all inbound traffic",
                                  "Protocol": "*",
                                  "SourcePortRange": [
                                    "*"
                                  ],
                                  "DestinationPortRange": [
                                    "*"
                                  ],
                                  "SourceAddressPrefix": [
                                    "*"
                                  ],
                                  "DestinationAddressPrefix": [
                                    "*"
                                  ],
                                  "Access": "Deny",
                                  "Priority": 65500,
                                  "Direction": "Inbound",
                                  "ProvisioningState": "Succeeded",
                                  "SourceApplicationSecurityGroups": [],
                                  "DestinationApplicationSecurityGroups": []
                                },
                                {
                                  "Name": "AllowVnetOutBound",
                                  "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                  "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/provide
                              rs/Microsoft.Network/networkSecurityGroups/nsg1/defaultSecurityRules/AllowVnetOutBound",
                                  "Description": "Allow outbound traffic from all VMs to all VMs in VNET",
                                  "Protocol": "*",
                                  "SourcePortRange": [
                                    "*"
                                  ],
                                  "DestinationPortRange": [
                                    "*"
                                  ],
                                  "SourceAddressPrefix": [
                                    "VirtualNetwork"
                                  ],
                                  "DestinationAddressPrefix": [
                                    "VirtualNetwork"
                                  ],
                                  "Access": "Allow",
                                  "Priority": 65000,
                                  "Direction": "Outbound",
                                  "ProvisioningState": "Succeeded",
                                  "SourceApplicationSecurityGroups": [],
                                  "DestinationApplicationSecurityGroups": []
                                },
                                {
                                  "Name": "AllowInternetOutBound",
                                  "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                  "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/provide
                              rs/Microsoft.Network/networkSecurityGroups/nsg1/defaultSecurityRules/AllowInternetOutBound",
                                  "Description": "Allow outbound traffic from all VMs to Internet",
                                  "Protocol": "*",
                                  "SourcePortRange": [
                                    "*"
                                  ],
                                  "DestinationPortRange": [
                                    "*"
                                  ],
                                  "SourceAddressPrefix": [
                                    "*"
                                  ],
                                  "DestinationAddressPrefix": [
                                    "Internet"
                                  ],
                                  "Access": "Allow",
                                  "Priority": 65001,
                                  "Direction": "Outbound",
                                  "ProvisioningState": "Succeeded",
                                  "SourceApplicationSecurityGroups": [],
                                  "DestinationApplicationSecurityGroups": []
                                },
                                {
                                  "Name": "DenyAllOutBound",
                                  "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                  "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/provide
                              rs/Microsoft.Network/networkSecurityGroups/nsg1/defaultSecurityRules/DenyAllOutBound",
                                  "Description": "Deny all outbound traffic",
                                  "Protocol": "*",
                                  "SourcePortRange": [
                                    "*"
                                  ],
                                  "DestinationPortRange": [
                                    "*"
                                  ],
                                  "SourceAddressPrefix": [
                                    "*"
                                  ],
                                  "DestinationAddressPrefix": [
                                    "*"
                                  ],
                                  "Access": "Deny",
                                  "Priority": 65500,
                                  "Direction": "Outbound",
                                  "ProvisioningState": "Succeeded",
                                  "SourceApplicationSecurityGroups": [],
                                  "DestinationApplicationSecurityGroups": []
                                }
                              ]
NetworkInterfaces           : []
Subnets                     : []
```

<span data-ttu-id="c0aee-113">Ez a parancs az "nsg" kezdetekkel kezdődik Azure-hálózatbiztonsági csoportok tartalmát adja vissza.</span><span class="sxs-lookup"><span data-stu-id="c0aee-113">This command returns contents of Azure network security groups that start with "nsg"</span></span>

## <span data-ttu-id="c0aee-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c0aee-114">PARAMETERS</span></span>

### <span data-ttu-id="c0aee-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0aee-115">-DefaultProfile</span></span>
<span data-ttu-id="c0aee-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c0aee-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c0aee-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="c0aee-117">-ExpandResource</span></span>
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

### <span data-ttu-id="c0aee-118">-Name</span><span class="sxs-lookup"><span data-stu-id="c0aee-118">-Name</span></span>
<span data-ttu-id="c0aee-119">Annak a hálózati biztonsági csoportnak a neve, amelybe ez a parancsmag kerül.</span><span class="sxs-lookup"><span data-stu-id="c0aee-119">Specifies the name of the network security group that this cmdlet gets.</span></span>

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

### <span data-ttu-id="c0aee-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0aee-120">-ResourceGroupName</span></span>
<span data-ttu-id="c0aee-121">Annak az erőforráscsoportnak a nevét adja meg, amelyhez a hálózati biztonsági csoport tartozik.</span><span class="sxs-lookup"><span data-stu-id="c0aee-121">Specifies the name of the resource group that the network security group belongs to.</span></span>

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

### <span data-ttu-id="c0aee-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0aee-122">CommonParameters</span></span>
<span data-ttu-id="c0aee-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0aee-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0aee-124">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c0aee-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0aee-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c0aee-125">INPUTS</span></span>

### <span data-ttu-id="c0aee-126">System.String</span><span class="sxs-lookup"><span data-stu-id="c0aee-126">System.String</span></span>

## <span data-ttu-id="c0aee-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c0aee-127">OUTPUTS</span></span>

### <span data-ttu-id="c0aee-128">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="c0aee-128">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="c0aee-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c0aee-129">NOTES</span></span>

## <span data-ttu-id="c0aee-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c0aee-130">RELATED LINKS</span></span>

[<span data-ttu-id="c0aee-131">New-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="c0aee-131">New-AzNetworkSecurityGroup</span></span>](./New-AzNetworkSecurityGroup.md)

[<span data-ttu-id="c0aee-132">Remove-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="c0aee-132">Remove-AzNetworkSecurityGroup</span></span>](./Remove-AzNetworkSecurityGroup.md)

[<span data-ttu-id="c0aee-133">Set-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="c0aee-133">Set-AzNetworkSecurityGroup</span></span>](./Set-AzNetworkSecurityGroup.md)


