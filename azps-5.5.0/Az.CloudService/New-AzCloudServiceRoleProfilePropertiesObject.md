---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.CloudService/new-AzCloudServiceRoleProfilePropertiesObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceRoleProfilePropertiesObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceRoleProfilePropertiesObject.md
ms.openlocfilehash: c9e41a6a4fa7a89db31304dc343da466e8632a74
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100149019"
---
# <span data-ttu-id="f61e0-101">New-AzCloudServiceRoleProfilePropertiesObject</span><span class="sxs-lookup"><span data-stu-id="f61e0-101">New-AzCloudServiceRoleProfilePropertiesObject</span></span>

## <span data-ttu-id="f61e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f61e0-102">SYNOPSIS</span></span>
<span data-ttu-id="f61e0-103">Create a in-memory object for CloudServiceRoleProfileProperties</span><span class="sxs-lookup"><span data-stu-id="f61e0-103">Create a in-memory object for CloudServiceRoleProfileProperties</span></span>

## <span data-ttu-id="f61e0-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f61e0-104">SYNTAX</span></span>

```
New-AzCloudServiceRoleProfilePropertiesObject [-Name <String>] [-SkuCapacity <Int64>] [-SkuName <String>]
 [-SkuTier <String>] [<CommonParameters>]
```

## <span data-ttu-id="f61e0-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f61e0-105">DESCRIPTION</span></span>
<span data-ttu-id="f61e0-106">Create a in-memory object for CloudServiceRoleProfileProperties</span><span class="sxs-lookup"><span data-stu-id="f61e0-106">Create a in-memory object for CloudServiceRoleProfileProperties</span></span>

## <span data-ttu-id="f61e0-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f61e0-107">EXAMPLES</span></span>

### <span data-ttu-id="f61e0-108">1. példa: Szerepkörprofil-tulajdonságobjektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="f61e0-108">Example 1: Create role profile properties object</span></span>
```powershell
$role = New-AzCloudServiceRoleProfilePropertiesObject -Name 'WebRole' -SkuName 'Standard_D1_v2' -SkuTier 'Standard' -SkuCapacity 2
```

<span data-ttu-id="f61e0-109">Ez a parancs létrehozza a szerepkörprofil-tulajdonságobjektumot, amely egy felhőszolgáltatás létrehozására vagy frissítésére használható.</span><span class="sxs-lookup"><span data-stu-id="f61e0-109">This command creates role profile properties object which is used for creating or updating a cloud service.</span></span>
<span data-ttu-id="f61e0-110">További részletekért lásd: New-AzCloudService.</span><span class="sxs-lookup"><span data-stu-id="f61e0-110">For more details see New-AzCloudService.</span></span>

## <span data-ttu-id="f61e0-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f61e0-111">PARAMETERS</span></span>

### <span data-ttu-id="f61e0-112">-Name</span><span class="sxs-lookup"><span data-stu-id="f61e0-112">-Name</span></span>
<span data-ttu-id="f61e0-113">A szerepkörprofil neve.</span><span class="sxs-lookup"><span data-stu-id="f61e0-113">Name of role profile.</span></span>

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

### <span data-ttu-id="f61e0-114">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="f61e0-114">-SkuCapacity</span></span>
<span data-ttu-id="f61e0-115">A felhőszolgáltatás szerepkör-példányainak számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="f61e0-115">Specifies the number of role instances in the cloud service.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f61e0-116">-SkuName</span><span class="sxs-lookup"><span data-stu-id="f61e0-116">-SkuName</span></span>
<span data-ttu-id="f61e0-117">A termékváltozat neve.</span><span class="sxs-lookup"><span data-stu-id="f61e0-117">The sku name.</span></span>

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

### <span data-ttu-id="f61e0-118">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="f61e0-118">-SkuTier</span></span>
<span data-ttu-id="f61e0-119">SkuTier.</span><span class="sxs-lookup"><span data-stu-id="f61e0-119">SkuTier.</span></span>

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

### <span data-ttu-id="f61e0-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f61e0-120">CommonParameters</span></span>
<span data-ttu-id="f61e0-121">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f61e0-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f61e0-122">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f61e0-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f61e0-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f61e0-123">INPUTS</span></span>

## <span data-ttu-id="f61e0-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f61e0-124">OUTPUTS</span></span>

### <span data-ttu-id="f61e0-125">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.CloudServiceRoleProfileProperties</span><span class="sxs-lookup"><span data-stu-id="f61e0-125">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.CloudServiceRoleProfileProperties</span></span>

## <span data-ttu-id="f61e0-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f61e0-126">NOTES</span></span>

<span data-ttu-id="f61e0-127">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="f61e0-127">ALIASES</span></span>

## <span data-ttu-id="f61e0-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f61e0-128">RELATED LINKS</span></span>

