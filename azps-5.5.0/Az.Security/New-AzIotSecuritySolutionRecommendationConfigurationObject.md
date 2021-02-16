---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/New-AzIotSecuritySolutionRecommendationConfigurationObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzIotSecuritySolutionRecommendationConfigurationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzIotSecuritySolutionRecommendationConfigurationObject.md
ms.openlocfilehash: 448b72ce068c29e357db69abb45420157c3c1bf0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100169026"
---
# <span data-ttu-id="c0c92-101">New-AzIotSecuritySolutionRecommendationConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="c0c92-101">New-AzIotSecuritySolutionRecommendationConfigurationObject</span></span>

## <span data-ttu-id="c0c92-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0c92-102">SYNOPSIS</span></span>
<span data-ttu-id="c0c92-103">Új ajánlott konfiguráció létrehozása iot biztonsági megoldáshoz</span><span class="sxs-lookup"><span data-stu-id="c0c92-103">Create new recommendation configuration for iot security solution</span></span>

## <span data-ttu-id="c0c92-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c0c92-104">SYNTAX</span></span>

```
New-AzIotSecuritySolutionRecommendationConfigurationObject -RecommendationType <String> -Enabled <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c0c92-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c0c92-105">DESCRIPTION</span></span>
<span data-ttu-id="c0c92-106">AzIotSecuritySolutionRecommendationConfigurationObject létrehoz egy új ajánlási konfigurációs objektumot az iot biztonsági megoldáshoz.</span><span class="sxs-lookup"><span data-stu-id="c0c92-106">The AzIotSecuritySolutionRecommendationConfigurationObject creates a new recommendation configuration object for iot security solution.</span></span>
<span data-ttu-id="c0c92-107">Ily módon a javaslat állapota konfigurálva van, akár engedélyezve van, akár le van tiltva.</span><span class="sxs-lookup"><span data-stu-id="c0c92-107">This way the status of a recommendation is configured, whether it is enabled or disabled.</span></span>

## <span data-ttu-id="c0c92-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c0c92-108">EXAMPLES</span></span>

### <span data-ttu-id="c0c92-109">1. példa</span><span class="sxs-lookup"><span data-stu-id="c0c92-109">Example 1</span></span>
```powershell
PS C:\> New-AzIotSecuritySolutionRecommendationConfigurationObject -RecommendationType "IoT_ACRAuthentication" -Enabled $false

RecommendationType: "IoT_ACRAuthentication"
Name: "Service prinicpal not used with ACR repository"
Status: "Disabled"
```

<span data-ttu-id="c0c92-110">Új ajánlási konfiguráció létrehozása "IoT_ACRAuthentication" típushoz letiltható állapot beállítással</span><span class="sxs-lookup"><span data-stu-id="c0c92-110">Create new recommendation configuration for recommendation type "IoT_ACRAuthentication" with status set to disable</span></span>

## <span data-ttu-id="c0c92-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c0c92-111">PARAMETERS</span></span>

### <span data-ttu-id="c0c92-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0c92-112">-DefaultProfile</span></span>
<span data-ttu-id="c0c92-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c0c92-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0c92-114">-Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="c0c92-114">-Enabled</span></span>
<span data-ttu-id="c0c92-115">Állapot.</span><span class="sxs-lookup"><span data-stu-id="c0c92-115">Status .</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0c92-116">-RecommendationType</span><span class="sxs-lookup"><span data-stu-id="c0c92-116">-RecommendationType</span></span>
<span data-ttu-id="c0c92-117">Javaslat típusa.</span><span class="sxs-lookup"><span data-stu-id="c0c92-117">Recommendation type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0c92-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0c92-118">CommonParameters</span></span>
<span data-ttu-id="c0c92-119">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0c92-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0c92-120">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c0c92-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0c92-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c0c92-121">INPUTS</span></span>

### <span data-ttu-id="c0c92-122">Nincs</span><span class="sxs-lookup"><span data-stu-id="c0c92-122">None</span></span>

## <span data-ttu-id="c0c92-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c0c92-123">OUTPUTS</span></span>

### <span data-ttu-id="c0c92-124">Microsoft.Azure.Commands.Security.Models.iotSecuritySolutions.PSRecommendationConfiguration</span><span class="sxs-lookup"><span data-stu-id="c0c92-124">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSRecommendationConfiguration</span></span>

## <span data-ttu-id="c0c92-125">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c0c92-125">NOTES</span></span>

## <span data-ttu-id="c0c92-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c0c92-126">RELATED LINKS</span></span>
