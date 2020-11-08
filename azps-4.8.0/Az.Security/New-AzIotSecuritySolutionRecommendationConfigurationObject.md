---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/New-AzIotSecuritySolutionRecommendationConfigurationObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzIotSecuritySolutionRecommendationConfigurationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzIotSecuritySolutionRecommendationConfigurationObject.md
ms.openlocfilehash: 448b72ce068c29e357db69abb45420157c3c1bf0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183982"
---
# <span data-ttu-id="1cce3-101">New-AzIotSecuritySolutionRecommendationConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="1cce3-101">New-AzIotSecuritySolutionRecommendationConfigurationObject</span></span>

## <span data-ttu-id="1cce3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1cce3-102">SYNOPSIS</span></span>
<span data-ttu-id="1cce3-103">Új ajánlási konfiguráció létrehozása a IOT biztonsági megoldásához</span><span class="sxs-lookup"><span data-stu-id="1cce3-103">Create new recommendation configuration for iot security solution</span></span>

## <span data-ttu-id="1cce3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1cce3-104">SYNTAX</span></span>

```
New-AzIotSecuritySolutionRecommendationConfigurationObject -RecommendationType <String> -Enabled <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1cce3-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="1cce3-105">DESCRIPTION</span></span>
<span data-ttu-id="1cce3-106">A AzIotSecuritySolutionRecommendationConfigurationObject létrehoz egy új ajánlási konfigurációs objektumot a IOT biztonsági megoldásához.</span><span class="sxs-lookup"><span data-stu-id="1cce3-106">The AzIotSecuritySolutionRecommendationConfigurationObject creates a new recommendation configuration object for iot security solution.</span></span>
<span data-ttu-id="1cce3-107">Így az ajánlás állapota úgy van konfigurálva, hogy be van-e kapcsolva vagy le van tiltva.</span><span class="sxs-lookup"><span data-stu-id="1cce3-107">This way the status of a recommendation is configured, whether it is enabled or disabled.</span></span>

## <span data-ttu-id="1cce3-108">Példák</span><span class="sxs-lookup"><span data-stu-id="1cce3-108">EXAMPLES</span></span>

### <span data-ttu-id="1cce3-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="1cce3-109">Example 1</span></span>
```powershell
PS C:\> New-AzIotSecuritySolutionRecommendationConfigurationObject -RecommendationType "IoT_ACRAuthentication" -Enabled $false

RecommendationType: "IoT_ACRAuthentication"
Name: "Service prinicpal not used with ACR repository"
Status: "Disabled"
```

<span data-ttu-id="1cce3-110">Új ajánlási konfiguráció létrehozása az "IoT_ACRAuthentication" vagy a letiltási beállítás típusához</span><span class="sxs-lookup"><span data-stu-id="1cce3-110">Create new recommendation configuration for recommendation type "IoT_ACRAuthentication" with status set to disable</span></span>

## <span data-ttu-id="1cce3-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1cce3-111">PARAMETERS</span></span>

### <span data-ttu-id="1cce3-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1cce3-112">-DefaultProfile</span></span>
<span data-ttu-id="1cce3-113">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1cce3-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1cce3-114">-Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="1cce3-114">-Enabled</span></span>
<span data-ttu-id="1cce3-115">Állapot.</span><span class="sxs-lookup"><span data-stu-id="1cce3-115">Status .</span></span>

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

### <span data-ttu-id="1cce3-116">-RecommendationType</span><span class="sxs-lookup"><span data-stu-id="1cce3-116">-RecommendationType</span></span>
<span data-ttu-id="1cce3-117">Javaslat típusa</span><span class="sxs-lookup"><span data-stu-id="1cce3-117">Recommendation type.</span></span>

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

### <span data-ttu-id="1cce3-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1cce3-118">CommonParameters</span></span>
<span data-ttu-id="1cce3-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1cce3-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1cce3-120">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="1cce3-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1cce3-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1cce3-121">INPUTS</span></span>

### <span data-ttu-id="1cce3-122">Nincs</span><span class="sxs-lookup"><span data-stu-id="1cce3-122">None</span></span>

## <span data-ttu-id="1cce3-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1cce3-123">OUTPUTS</span></span>

### <span data-ttu-id="1cce3-124">Microsoft. Azure. commands. Security. models. IotSecuritySolutions. PSRecommendationConfiguration</span><span class="sxs-lookup"><span data-stu-id="1cce3-124">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSRecommendationConfiguration</span></span>

## <span data-ttu-id="1cce3-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1cce3-125">NOTES</span></span>

## <span data-ttu-id="1cce3-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1cce3-126">RELATED LINKS</span></span>
