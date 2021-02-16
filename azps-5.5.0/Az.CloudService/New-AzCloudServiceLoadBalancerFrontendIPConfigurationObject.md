---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.CloudService/new-AzCloudServiceLoadBalancerFrontendIPConfigurationObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject.md
ms.openlocfilehash: cdd983e2ede5cd06c3b9b00805b337eac5b73a9b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100162355"
---
# <span data-ttu-id="b8ae3-101">New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="b8ae3-101">New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject</span></span>

## <span data-ttu-id="b8ae3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8ae3-102">SYNOPSIS</span></span>
<span data-ttu-id="b8ae3-103">Create a in-memory object for LoadBalancerFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="b8ae3-103">Create a in-memory object for LoadBalancerFrontendIPConfiguration</span></span>

## <span data-ttu-id="b8ae3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b8ae3-104">SYNTAX</span></span>

```
New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject [-Name <String>] [-PublicIPAddressId <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="b8ae3-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b8ae3-105">DESCRIPTION</span></span>
<span data-ttu-id="b8ae3-106">Create a in-memory object for LoadBalancerFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="b8ae3-106">Create a in-memory object for LoadBalancerFrontendIPConfiguration</span></span>

## <span data-ttu-id="b8ae3-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b8ae3-107">EXAMPLES</span></span>

### <span data-ttu-id="b8ae3-108">1. példa: Terheléselosztási frontend IP konfigurációs objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="b8ae3-108">Example 1: Create load balancer frontend IP configuration object</span></span>
```powershell
PS C:\> $publicIP = Get-AzPublicIpAddress -ResourceGroupName 'ContosoOrg' -Name 'ContosoPublicIP'
PS C:\> $feIpConfig = New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject -Name 'ContosoFe' -PublicIPAddressId $publicIp.Id
PS C:\> $loadBalancerConfig = New-AzCloudServiceLoadBalancerConfigurationObject -Name 'ContosoLB' -FrontendIPConfiguration $feIpConfig
```

<span data-ttu-id="b8ae3-109">Ez a parancs a terheléselosztási frontend IP konfigurációs objektumot hozza létre, amely egy felhőszolgáltatás létrehozására vagy frissítésére használható.</span><span class="sxs-lookup"><span data-stu-id="b8ae3-109">This command creates load balancer frontend IP configuration object which is used for creating or updating a cloud service.</span></span>
<span data-ttu-id="b8ae3-110">További részletekért lásd: New-AzCloudService.</span><span class="sxs-lookup"><span data-stu-id="b8ae3-110">For more details see New-AzCloudService.</span></span>

## <span data-ttu-id="b8ae3-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b8ae3-111">PARAMETERS</span></span>

### <span data-ttu-id="b8ae3-112">-Name</span><span class="sxs-lookup"><span data-stu-id="b8ae3-112">-Name</span></span>
<span data-ttu-id="b8ae3-113">A FrontendIpConfigration neve.</span><span class="sxs-lookup"><span data-stu-id="b8ae3-113">Name of FrontendIpConfigration.</span></span>

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

### <span data-ttu-id="b8ae3-114">-PublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="b8ae3-114">-PublicIPAddressId</span></span>
<span data-ttu-id="b8ae3-115">Erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="b8ae3-115">Resource Id.</span></span>

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

### <span data-ttu-id="b8ae3-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8ae3-116">CommonParameters</span></span>
<span data-ttu-id="b8ae3-117">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8ae3-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8ae3-118">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b8ae3-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8ae3-119">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b8ae3-119">INPUTS</span></span>

## <span data-ttu-id="b8ae3-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b8ae3-120">OUTPUTS</span></span>

### <span data-ttu-id="b8ae3-121">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.LoadBalancerFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="b8ae3-121">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.LoadBalancerFrontendIPConfiguration</span></span>

## <span data-ttu-id="b8ae3-122">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b8ae3-122">NOTES</span></span>

<span data-ttu-id="b8ae3-123">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="b8ae3-123">ALIASES</span></span>

## <span data-ttu-id="b8ae3-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b8ae3-124">RELATED LINKS</span></span>

