---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateLinkService.md
ms.openlocfilehash: fdbb023c6796a780bfe9e6474191185a58489c91
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302015"
---
# <span data-ttu-id="01438-101">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="01438-101">Get-AzPrivateLinkService</span></span>

## <span data-ttu-id="01438-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="01438-102">SYNOPSIS</span></span>
<span data-ttu-id="01438-103">Kapja a privát link szolgáltatást</span><span class="sxs-lookup"><span data-stu-id="01438-103">Gets private link service</span></span>

## <span data-ttu-id="01438-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="01438-104">SYNTAX</span></span>

### <span data-ttu-id="01438-105">Kibontott (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="01438-105">NoExpand (Default)</span></span>
```
Get-AzPrivateLinkService [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="01438-106">Bővíteni</span><span class="sxs-lookup"><span data-stu-id="01438-106">Expand</span></span>
```
Get-AzPrivateLinkService -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="01438-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="01438-107">DESCRIPTION</span></span>
<span data-ttu-id="01438-108">A **Get-AzPrivateLinkService** parancsmag egy vagy több privát kapcsolati szolgáltatást kap.</span><span class="sxs-lookup"><span data-stu-id="01438-108">The **Get-AzPrivateLinkService** cmdlet gets one or more private link services.</span></span>

## <span data-ttu-id="01438-109">Példák</span><span class="sxs-lookup"><span data-stu-id="01438-109">EXAMPLES</span></span>

### <span data-ttu-id="01438-110">Például</span><span class="sxs-lookup"><span data-stu-id="01438-110">Example</span></span>
```
Get-AzPrivateLinkService -Name MyPLS -ResourceGroupName TestResourceGroup

Name                                 : MyPLS
ResourceGroupName                    : TestResourceGroup
Id                                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/prov
                                       iders/Microsoft.Network/privateLinkServices/MyPLS
Location                             : eastus2euap
Type                                 : Microsoft.Network/privateLinkServices
Etag                                 : W/"00000000-0000-0000-0000-000000000000"
Tag                                  : {}
ProvisioningState                    : Succeeded
Visibility                           : 
AutoApproval                         : 
Alias                                :
LoadBalancerFrontendIpConfigurations : []
IpConfigurations                     : [
                                         {
                                           "PrivateIPAddress": "10.0.2.5",
                                           "PrivateIPAllocationMethod": "Static",
                                           "ProvisioningState": "Failed",
                                           "PrivateIPAddressVersion": "IPv4",
                                           "Name": "IP-Config",
                                           "Subnet": {
                                             "Delegations": [],
                                             "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/
                                       TestResourceGroup/providers/Microsoft.Network/virtualNetworks/myvnet/subnets/backendSubne
                                       t",
                                             "ServiceAssociationLinks": []
                                           }
                                         }
                                       ]
PrivateEndpointConnections           : []
NetworkInterfaces                    : [
                                         {
                                           "TapConfigurations": [],
                                           "HostedWorkloads": [],
                                           "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Network/networkInterfaces/mytestinterface"
                                         }
                                       ]
```

<span data-ttu-id="01438-111">Ez a parancsmagot az erőforráscsoport privát kapcsolat szolgáltatását kapja.</span><span class="sxs-lookup"><span data-stu-id="01438-111">This commandlet gets a private link service in the resource group.</span></span>

## <span data-ttu-id="01438-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="01438-112">PARAMETERS</span></span>

### <span data-ttu-id="01438-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01438-113">-DefaultProfile</span></span>
<span data-ttu-id="01438-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="01438-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01438-115">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="01438-115">-ExpandResource</span></span>
<span data-ttu-id="01438-116">A kibontani kívánt erőforrás-hivatkozás.</span><span class="sxs-lookup"><span data-stu-id="01438-116">The resource reference to be expanded.</span></span>

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

### <span data-ttu-id="01438-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="01438-117">-Name</span></span>
<span data-ttu-id="01438-118">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="01438-118">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01438-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01438-119">-ResourceGroupName</span></span>
<span data-ttu-id="01438-120">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="01438-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### <span data-ttu-id="01438-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01438-121">CommonParameters</span></span>
<span data-ttu-id="01438-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="01438-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01438-123">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="01438-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01438-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="01438-124">INPUTS</span></span>

### <span data-ttu-id="01438-125">System. String</span><span class="sxs-lookup"><span data-stu-id="01438-125">System.String</span></span>

## <span data-ttu-id="01438-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="01438-126">OUTPUTS</span></span>

### <span data-ttu-id="01438-127">Microsoft. Azure. commands. Network. models. PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="01438-127">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="01438-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="01438-128">NOTES</span></span>

## <span data-ttu-id="01438-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="01438-129">RELATED LINKS</span></span>
