---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/New-AzIotSecuritySolutionRecommendationConfigurationObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzIotSecuritySolutionRecommendationConfigurationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzIotSecuritySolutionRecommendationConfigurationObject.md
ms.openlocfilehash: 448b72ce068c29e357db69abb45420157c3c1bf0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186194"
---
# <span data-ttu-id="48ba9-101">New-AzIotSecuritySolutionRecommendationConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="48ba9-101">New-AzIotSecuritySolutionRecommendationConfigurationObject</span></span>

## <span data-ttu-id="48ba9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="48ba9-102">SYNOPSIS</span></span>
<span data-ttu-id="48ba9-103">Új ajánlási konfiguráció létrehozása a IOT biztonsági megoldásához</span><span class="sxs-lookup"><span data-stu-id="48ba9-103">Create new recommendation configuration for iot security solution</span></span>

## <span data-ttu-id="48ba9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="48ba9-104">SYNTAX</span></span>

```
New-AzIotSecuritySolutionRecommendationConfigurationObject -RecommendationType <String> -Enabled <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="48ba9-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="48ba9-105">DESCRIPTION</span></span>
<span data-ttu-id="48ba9-106">A AzIotSecuritySolutionRecommendationConfigurationObject létrehoz egy új ajánlási konfigurációs objektumot a IOT biztonsági megoldásához.</span><span class="sxs-lookup"><span data-stu-id="48ba9-106">The AzIotSecuritySolutionRecommendationConfigurationObject creates a new recommendation configuration object for iot security solution.</span></span>
<span data-ttu-id="48ba9-107">Így az ajánlás állapota úgy van konfigurálva, hogy be van-e kapcsolva vagy le van tiltva.</span><span class="sxs-lookup"><span data-stu-id="48ba9-107">This way the status of a recommendation is configured, whether it is enabled or disabled.</span></span>

## <span data-ttu-id="48ba9-108">Példák</span><span class="sxs-lookup"><span data-stu-id="48ba9-108">EXAMPLES</span></span>

### <span data-ttu-id="48ba9-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="48ba9-109">Example 1</span></span>
```powershell
PS C:\> New-AzIotSecuritySolutionRecommendationConfigurationObject -RecommendationType "IoT_ACRAuthentication" -Enabled $false

RecommendationType: "IoT_ACRAuthentication"
Name: "Service prinicpal not used with ACR repository"
Status: "Disabled"
```

<span data-ttu-id="48ba9-110">Új ajánlási konfiguráció létrehozása az "IoT_ACRAuthentication" vagy a letiltási beállítás típusához</span><span class="sxs-lookup"><span data-stu-id="48ba9-110">Create new recommendation configuration for recommendation type "IoT_ACRAuthentication" with status set to disable</span></span>

## <span data-ttu-id="48ba9-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="48ba9-111">PARAMETERS</span></span>

### <span data-ttu-id="48ba9-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48ba9-112">-DefaultProfile</span></span>
<span data-ttu-id="48ba9-113">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="48ba9-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="48ba9-114">-Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="48ba9-114">-Enabled</span></span>
<span data-ttu-id="48ba9-115">Állapot.</span><span class="sxs-lookup"><span data-stu-id="48ba9-115">Status .</span></span>

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

### <span data-ttu-id="48ba9-116">-RecommendationType</span><span class="sxs-lookup"><span data-stu-id="48ba9-116">-RecommendationType</span></span>
<span data-ttu-id="48ba9-117">Javaslat típusa</span><span class="sxs-lookup"><span data-stu-id="48ba9-117">Recommendation type.</span></span>

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

### <span data-ttu-id="48ba9-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48ba9-118">CommonParameters</span></span>
<span data-ttu-id="48ba9-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="48ba9-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48ba9-120">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="48ba9-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48ba9-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="48ba9-121">INPUTS</span></span>

### <span data-ttu-id="48ba9-122">Nincs</span><span class="sxs-lookup"><span data-stu-id="48ba9-122">None</span></span>

## <span data-ttu-id="48ba9-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="48ba9-123">OUTPUTS</span></span>

### <span data-ttu-id="48ba9-124">Microsoft. Azure. commands. Security. models. IotSecuritySolutions. PSRecommendationConfiguration</span><span class="sxs-lookup"><span data-stu-id="48ba9-124">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSRecommendationConfiguration</span></span>

## <span data-ttu-id="48ba9-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="48ba9-125">NOTES</span></span>

## <span data-ttu-id="48ba9-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="48ba9-126">RELATED LINKS</span></span>
