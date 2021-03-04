---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/powershell/module/az.cdn/get-azcdnprofilesupportedoptimizationtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileSupportedOptimizationType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileSupportedOptimizationType.md
ms.openlocfilehash: f26e1bd19b9856df7bf68de6c8afddefb3ee64a0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937153"
---
# <span data-ttu-id="1f7e0-101">Get-AzCdnProfileSupportedOptimizationType</span><span class="sxs-lookup"><span data-stu-id="1f7e0-101">Get-AzCdnProfileSupportedOptimizationType</span></span>

## <span data-ttu-id="1f7e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f7e0-102">SYNOPSIS</span></span>
<span data-ttu-id="1f7e0-103">Egy CDN-profil támogatott optimalizálási típusait kapja.</span><span class="sxs-lookup"><span data-stu-id="1f7e0-103">Gets the supported optimization types for a CDN profile.</span></span>

## <span data-ttu-id="1f7e0-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="1f7e0-104">SYNTAX</span></span>

### <span data-ttu-id="1f7e0-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1f7e0-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnProfileSupportedOptimizationType -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1f7e0-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1f7e0-106">ByObjectParameterSet</span></span>
```
Get-AzCdnProfileSupportedOptimizationType -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1f7e0-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="1f7e0-107">DESCRIPTION</span></span>
<span data-ttu-id="1f7e0-108">A **Get-AzCdnProfileSupportedOptimizationType** parancsmag megkapja az aktuális profil támogatott optimalizálási típusait.</span><span class="sxs-lookup"><span data-stu-id="1f7e0-108">The **Get-AzCdnProfileSupportedOptimizationType** cmdlet gets the supported optimization types for the current profile.</span></span> <span data-ttu-id="1f7e0-109">A felhasználók létrehozhatnak egy optimalizálási típust használó végpontot a listában szereplő értékekből.</span><span class="sxs-lookup"><span data-stu-id="1f7e0-109">A user can create an endpoint with an optimization type from the listed values.</span></span>

## <span data-ttu-id="1f7e0-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="1f7e0-110">EXAMPLES</span></span>

### <span data-ttu-id="1f7e0-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="1f7e0-111">Example 1</span></span>
```powershell
PS C:\> Get-AzCdnProfileSupportedOptimizationType -ProfileName $profileName -ResourceGroupName $resourceGroupName
OptimizationType: GeneralWebDelivery
OptimizationType: DynamicSiteAcceleration
```

<span data-ttu-id="1f7e0-112">A CDN-profil támogatott optimalizálási típusainak lekérte.</span><span class="sxs-lookup"><span data-stu-id="1f7e0-112">Get the supported optimization types for a CDN profile.</span></span>

## <span data-ttu-id="1f7e0-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1f7e0-113">PARAMETERS</span></span>

### <span data-ttu-id="1f7e0-114">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="1f7e0-114">-CdnProfile</span></span>
<span data-ttu-id="1f7e0-115">Az Azure CDN-profilobjektum.</span><span class="sxs-lookup"><span data-stu-id="1f7e0-115">The Azure CDN profile object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1f7e0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f7e0-116">-DefaultProfile</span></span>
<span data-ttu-id="1f7e0-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1f7e0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f7e0-118">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="1f7e0-118">-ProfileName</span></span>
<span data-ttu-id="1f7e0-119">A profil neve.</span><span class="sxs-lookup"><span data-stu-id="1f7e0-119">The name of the profile.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f7e0-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f7e0-120">-ResourceGroupName</span></span>
<span data-ttu-id="1f7e0-121">Az az erőforráscsoport, amelyhez a profil tartozik.</span><span class="sxs-lookup"><span data-stu-id="1f7e0-121">The resource group to which the profile belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f7e0-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f7e0-122">CommonParameters</span></span>
<span data-ttu-id="1f7e0-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f7e0-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f7e0-124">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1f7e0-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f7e0-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1f7e0-125">INPUTS</span></span>

### <span data-ttu-id="1f7e0-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span><span class="sxs-lookup"><span data-stu-id="1f7e0-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="1f7e0-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1f7e0-127">OUTPUTS</span></span>

### <span data-ttu-id="1f7e0-128">Microsoft.Azure.Commands.Cdn.Models.Profile.PSOptimizationType</span><span class="sxs-lookup"><span data-stu-id="1f7e0-128">Microsoft.Azure.Commands.Cdn.Models.Profile.PSOptimizationType</span></span>

## <span data-ttu-id="1f7e0-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="1f7e0-129">NOTES</span></span>

## <span data-ttu-id="1f7e0-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1f7e0-130">RELATED LINKS</span></span>
