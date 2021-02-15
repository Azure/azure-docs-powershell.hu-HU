---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.CloudService/new-AzCloudServiceLoadBalancerConfigurationObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceLoadBalancerConfigurationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceLoadBalancerConfigurationObject.md
ms.openlocfilehash: 6afabb94ae006cec122d7e89997be17c20e85b05
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100166659"
---
# <span data-ttu-id="790b9-101">New-AzCloudServiceLoadBalancerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="790b9-101">New-AzCloudServiceLoadBalancerConfigurationObject</span></span>

## <span data-ttu-id="790b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="790b9-102">SYNOPSIS</span></span>
<span data-ttu-id="790b9-103">Create a in-memory object for LoadBalancerConfiguration</span><span class="sxs-lookup"><span data-stu-id="790b9-103">Create a in-memory object for LoadBalancerConfiguration</span></span>

## <span data-ttu-id="790b9-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="790b9-104">SYNTAX</span></span>

```
New-AzCloudServiceLoadBalancerConfigurationObject
 [-FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>] [-Name <String>] [<CommonParameters>]
```

## <span data-ttu-id="790b9-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="790b9-105">DESCRIPTION</span></span>
<span data-ttu-id="790b9-106">Create a in-memory object for LoadBalancerConfiguration</span><span class="sxs-lookup"><span data-stu-id="790b9-106">Create a in-memory object for LoadBalancerConfiguration</span></span>

## <span data-ttu-id="790b9-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="790b9-107">EXAMPLES</span></span>

### <span data-ttu-id="790b9-108">1. példa: Terheléselosztási konfigurációs objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="790b9-108">Example 1: Create load balancer configuration object</span></span>
```powershell
PS C:\> $publicIP = Get-AzPublicIpAddress -ResourceGroupName 'ContosoOrg' -Name 'ContosoPublicIP'
PS C:\> $feIpConfig = New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject -Name 'ContosoFe' -PublicIPAddressId $publicIP.Id
PS C:\> $loadBalancerConfig = New-AzCloudServiceLoadBalancerConfigurationObject -Name 'ContosoLB' -FrontendIPConfiguration $feIpConfig
```

<span data-ttu-id="790b9-109">Ez a parancs egy terheléselosztási konfigurációs objektumot hoz létre, amely egy felhőszolgáltatás létrehozására vagy frissítésére használható.</span><span class="sxs-lookup"><span data-stu-id="790b9-109">This command creates load balancer configuration object which is used for creating or updating a cloud service.</span></span>
<span data-ttu-id="790b9-110">További részletekért lásd: New-AzCloudService.</span><span class="sxs-lookup"><span data-stu-id="790b9-110">For more details see New-AzCloudService.</span></span>

## <span data-ttu-id="790b9-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="790b9-111">PARAMETERS</span></span>

### <span data-ttu-id="790b9-112">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="790b9-112">-FrontendIPConfiguration</span></span>
<span data-ttu-id="790b9-113">FrontendIPConfiguration.</span><span class="sxs-lookup"><span data-stu-id="790b9-113">FrontendIPConfiguration.</span></span>
<span data-ttu-id="790b9-114">Ennek létrehozásáról a NOTES (JEGYZETEK) szakasz tartalmaz frontenDIPCONFIGURATION tulajdonságokat, és hozzon létre egy kivonattáblát.</span><span class="sxs-lookup"><span data-stu-id="790b9-114">To construct, see NOTES section for FRONTENDIPCONFIGURATION properties and create a hash table.</span></span>

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

### <span data-ttu-id="790b9-115">-Name</span><span class="sxs-lookup"><span data-stu-id="790b9-115">-Name</span></span>
<span data-ttu-id="790b9-116">A LoadBalancerConfiguration neve.</span><span class="sxs-lookup"><span data-stu-id="790b9-116">Name of LoadBalancerConfiguration.</span></span>

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

### <span data-ttu-id="790b9-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="790b9-117">CommonParameters</span></span>
<span data-ttu-id="790b9-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="790b9-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="790b9-119">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="790b9-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="790b9-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="790b9-120">INPUTS</span></span>

## <span data-ttu-id="790b9-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="790b9-121">OUTPUTS</span></span>

### <span data-ttu-id="790b9-122">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.LoadBalancerConfiguration</span><span class="sxs-lookup"><span data-stu-id="790b9-122">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.LoadBalancerConfiguration</span></span>

## <span data-ttu-id="790b9-123">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="790b9-123">NOTES</span></span>

<span data-ttu-id="790b9-124">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="790b9-124">ALIASES</span></span>

<span data-ttu-id="790b9-125">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="790b9-125">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="790b9-126">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="790b9-126">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="790b9-127">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="790b9-127">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="790b9-128">FRONTENDIPCONFIGURATION <ILoadBalancerFrontendIPConfiguration[]>: FrontendIPConfiguration.</span><span class="sxs-lookup"><span data-stu-id="790b9-128">FRONTENDIPCONFIGURATION <ILoadBalancerFrontendIPConfiguration[]>: FrontendIPConfiguration.</span></span>
  - <span data-ttu-id="790b9-129">`[Name <String>]`:</span><span class="sxs-lookup"><span data-stu-id="790b9-129">`[Name <String>]`:</span></span> 
  - <span data-ttu-id="790b9-130">`[PrivateIPAddress <String>]`: A felhőszolgáltatás által hivatkozott privát IP-cím.</span><span class="sxs-lookup"><span data-stu-id="790b9-130">`[PrivateIPAddress <String>]`: The private IP address referenced by the cloud service.</span></span>
  - <span data-ttu-id="790b9-131">`[PublicIPAddressId <String>]`: Erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="790b9-131">`[PublicIPAddressId <String>]`: Resource Id</span></span>
  - <span data-ttu-id="790b9-132">`[SubnetId <String>]`: Erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="790b9-132">`[SubnetId <String>]`: Resource Id</span></span>

## <span data-ttu-id="790b9-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="790b9-133">RELATED LINKS</span></span>

