---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.CloudService/new-AzCloudServiceLoadBalancerConfigurationObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceLoadBalancerConfigurationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceLoadBalancerConfigurationObject.md
ms.openlocfilehash: 5d3acb8c03ceae44024ed8c6c52a8ee962c9861c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101935834"
---
# <span data-ttu-id="33781-101">New-AzCloudServiceLoadBalancerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="33781-101">New-AzCloudServiceLoadBalancerConfigurationObject</span></span>

## <span data-ttu-id="33781-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="33781-102">SYNOPSIS</span></span>
<span data-ttu-id="33781-103">Create a in-memory object for LoadBalancerConfiguration</span><span class="sxs-lookup"><span data-stu-id="33781-103">Create a in-memory object for LoadBalancerConfiguration</span></span>

## <span data-ttu-id="33781-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="33781-104">SYNTAX</span></span>

```
New-AzCloudServiceLoadBalancerConfigurationObject
 [-FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>] [-Name <String>] [<CommonParameters>]
```

## <span data-ttu-id="33781-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="33781-105">DESCRIPTION</span></span>
<span data-ttu-id="33781-106">Create a in-memory object for LoadBalancerConfiguration</span><span class="sxs-lookup"><span data-stu-id="33781-106">Create a in-memory object for LoadBalancerConfiguration</span></span>

## <span data-ttu-id="33781-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="33781-107">EXAMPLES</span></span>

### <span data-ttu-id="33781-108">1. példa: Terheléselosztási konfigurációs objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="33781-108">Example 1: Create load balancer configuration object</span></span>
```powershell
PS C:\> $publicIP = Get-AzPublicIpAddress -ResourceGroupName 'ContosoOrg' -Name 'ContosoPublicIP'
PS C:\> $feIpConfig = New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject -Name 'ContosoFe' -PublicIPAddressId $publicIP.Id
PS C:\> $loadBalancerConfig = New-AzCloudServiceLoadBalancerConfigurationObject -Name 'ContosoLB' -FrontendIPConfiguration $feIpConfig
```

<span data-ttu-id="33781-109">Ez a parancs egy terheléselosztási konfigurációs objektumot hoz létre, amely egy felhőszolgáltatás létrehozására vagy frissítésére használható.</span><span class="sxs-lookup"><span data-stu-id="33781-109">This command creates load balancer configuration object which is used for creating or updating a cloud service.</span></span>
<span data-ttu-id="33781-110">További részletekért lásd: New-AzCloudService.</span><span class="sxs-lookup"><span data-stu-id="33781-110">For more details see New-AzCloudService.</span></span>

## <span data-ttu-id="33781-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="33781-111">PARAMETERS</span></span>

### <span data-ttu-id="33781-112">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="33781-112">-FrontendIPConfiguration</span></span>
<span data-ttu-id="33781-113">FrontendIPConfiguration.</span><span class="sxs-lookup"><span data-stu-id="33781-113">FrontendIPConfiguration.</span></span>
<span data-ttu-id="33781-114">Ennek létrehozásáról a FRONTENDIPCONFIGURATION tulajdonságokat és a kivonattáblát a NOTES (JEGYZETEK) című szakaszban láthatja.</span><span class="sxs-lookup"><span data-stu-id="33781-114">To construct, see NOTES section for FRONTENDIPCONFIGURATION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ILoadBalancerFrontendIPConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33781-115">-Name</span><span class="sxs-lookup"><span data-stu-id="33781-115">-Name</span></span>
<span data-ttu-id="33781-116">A LoadBalancerConfiguration neve.</span><span class="sxs-lookup"><span data-stu-id="33781-116">Name of LoadBalancerConfiguration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33781-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33781-117">CommonParameters</span></span>
<span data-ttu-id="33781-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33781-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33781-119">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="33781-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33781-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="33781-120">INPUTS</span></span>

## <span data-ttu-id="33781-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="33781-121">OUTPUTS</span></span>

### <span data-ttu-id="33781-122">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.LoadBalancerConfiguration</span><span class="sxs-lookup"><span data-stu-id="33781-122">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.LoadBalancerConfiguration</span></span>

## <span data-ttu-id="33781-123">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="33781-123">NOTES</span></span>

<span data-ttu-id="33781-124">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="33781-124">ALIASES</span></span>

<span data-ttu-id="33781-125">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="33781-125">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="33781-126">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="33781-126">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="33781-127">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="33781-127">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="33781-128">FRONTENDIPCONFIGURATION <ILoadBalancerFrontendIPConfiguration[]>: FrontendIPConfiguration.</span><span class="sxs-lookup"><span data-stu-id="33781-128">FRONTENDIPCONFIGURATION <ILoadBalancerFrontendIPConfiguration[]>: FrontendIPConfiguration.</span></span>
  - <span data-ttu-id="33781-129">`[Name <String>]`:</span><span class="sxs-lookup"><span data-stu-id="33781-129">`[Name <String>]`:</span></span> 
  - <span data-ttu-id="33781-130">`[PrivateIPAddress <String>]`: A felhőszolgáltatás által hivatkozott privát IP-cím.</span><span class="sxs-lookup"><span data-stu-id="33781-130">`[PrivateIPAddress <String>]`: The private IP address referenced by the cloud service.</span></span>
  - <span data-ttu-id="33781-131">`[PublicIPAddressId <String>]`: Erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="33781-131">`[PublicIPAddressId <String>]`: Resource Id</span></span>
  - <span data-ttu-id="33781-132">`[SubnetId <String>]`: Erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="33781-132">`[SubnetId <String>]`: Resource Id</span></span>

## <span data-ttu-id="33781-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="33781-133">RELATED LINKS</span></span>

