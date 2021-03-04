---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateLinkService.md
ms.openlocfilehash: 8b2e8902257566256ed41c38c90c31cb430d12d1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919697"
---
# <span data-ttu-id="4ce51-101">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="4ce51-101">Get-AzPrivateLinkService</span></span>

## <span data-ttu-id="4ce51-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ce51-102">SYNOPSIS</span></span>
<span data-ttu-id="4ce51-103">Privát hivatkozásszolgáltatást kap</span><span class="sxs-lookup"><span data-stu-id="4ce51-103">Gets private link service</span></span>

## <span data-ttu-id="4ce51-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="4ce51-104">SYNTAX</span></span>

### <span data-ttu-id="4ce51-105">NoExpand (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4ce51-105">NoExpand (Default)</span></span>
```
Get-AzPrivateLinkService [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4ce51-106">Kibontás</span><span class="sxs-lookup"><span data-stu-id="4ce51-106">Expand</span></span>
```
Get-AzPrivateLinkService -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4ce51-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="4ce51-107">DESCRIPTION</span></span>
<span data-ttu-id="4ce51-108">A **Get-AzPrivateLinkService** parancsmag egy vagy több privát hivatkozásszolgáltatást kap.</span><span class="sxs-lookup"><span data-stu-id="4ce51-108">The **Get-AzPrivateLinkService** cmdlet gets one or more private link services.</span></span>

## <span data-ttu-id="4ce51-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="4ce51-109">EXAMPLES</span></span>

### <span data-ttu-id="4ce51-110">Példa</span><span class="sxs-lookup"><span data-stu-id="4ce51-110">Example</span></span>
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

<span data-ttu-id="4ce51-111">Ez a parancsmag egy privát hivatkozásszolgáltatást kap az erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="4ce51-111">This commandlet gets a private link service in the resource group.</span></span>

## <span data-ttu-id="4ce51-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4ce51-112">PARAMETERS</span></span>

### <span data-ttu-id="4ce51-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ce51-113">-DefaultProfile</span></span>
<span data-ttu-id="4ce51-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4ce51-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ce51-115">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="4ce51-115">-ExpandResource</span></span>
<span data-ttu-id="4ce51-116">A kibontani szükséges erőforrás-hivatkozás.</span><span class="sxs-lookup"><span data-stu-id="4ce51-116">The resource reference to be expanded.</span></span>

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

### <span data-ttu-id="4ce51-117">-Name</span><span class="sxs-lookup"><span data-stu-id="4ce51-117">-Name</span></span>
<span data-ttu-id="4ce51-118">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="4ce51-118">The resource name.</span></span>

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

### <span data-ttu-id="4ce51-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ce51-119">-ResourceGroupName</span></span>
<span data-ttu-id="4ce51-120">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="4ce51-120">The resource group name.</span></span>

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

### <span data-ttu-id="4ce51-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ce51-121">CommonParameters</span></span>
<span data-ttu-id="4ce51-122">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ce51-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ce51-123">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4ce51-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ce51-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4ce51-124">INPUTS</span></span>

### <span data-ttu-id="4ce51-125">System.String</span><span class="sxs-lookup"><span data-stu-id="4ce51-125">System.String</span></span>

## <span data-ttu-id="4ce51-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4ce51-126">OUTPUTS</span></span>

### <span data-ttu-id="4ce51-127">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="4ce51-127">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="4ce51-128">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="4ce51-128">NOTES</span></span>

## <span data-ttu-id="4ce51-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4ce51-129">RELATED LINKS</span></span>
