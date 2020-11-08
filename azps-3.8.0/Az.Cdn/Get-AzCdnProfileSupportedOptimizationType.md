---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnprofilesupportedoptimizationtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileSupportedOptimizationType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileSupportedOptimizationType.md
ms.openlocfilehash: db6520ae16d114fdcad85daf3e0742589fa0fbbe
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94002940"
---
# <span data-ttu-id="7f454-101">Get-AzCdnProfileSupportedOptimizationType</span><span class="sxs-lookup"><span data-stu-id="7f454-101">Get-AzCdnProfileSupportedOptimizationType</span></span>

## <span data-ttu-id="7f454-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7f454-102">SYNOPSIS</span></span>
<span data-ttu-id="7f454-103">A támogatott optimalizálási típusokat kapja egy CDN-profilban.</span><span class="sxs-lookup"><span data-stu-id="7f454-103">Gets the supported optimization types for a CDN profile.</span></span>

## <span data-ttu-id="7f454-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7f454-104">SYNTAX</span></span>

### <span data-ttu-id="7f454-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7f454-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnProfileSupportedOptimizationType -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7f454-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7f454-106">ByObjectParameterSet</span></span>
```
Get-AzCdnProfileSupportedOptimizationType -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7f454-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="7f454-107">DESCRIPTION</span></span>
<span data-ttu-id="7f454-108">A **Get-AzCdnProfileSupportedOptimizationType** parancsmag az aktuális profil támogatott optimalizálási típusait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="7f454-108">The **Get-AzCdnProfileSupportedOptimizationType** cmdlet gets the supported optimization types for the current profile.</span></span> <span data-ttu-id="7f454-109">A felhasználók létrehozhatnak egy olyan végpontot, amely egy optimalizálási típust használ a felsorolt értékekkel.</span><span class="sxs-lookup"><span data-stu-id="7f454-109">A user can create an endpoint with an optimization type from the listed values.</span></span>

## <span data-ttu-id="7f454-110">Példák</span><span class="sxs-lookup"><span data-stu-id="7f454-110">EXAMPLES</span></span>

### <span data-ttu-id="7f454-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="7f454-111">Example 1</span></span>
```powershell
PS C:\> Get-AzCdnProfileSupportedOptimizationType -ProfileName $profileName -ResourceGroupName $resourceGroupName
OptimizationType: GeneralWebDelivery
OptimizationType: DynamicSiteAcceleration
```

<span data-ttu-id="7f454-112">Beszerezhet egy CDN-profil támogatott optimalizálási típusait.</span><span class="sxs-lookup"><span data-stu-id="7f454-112">Get the supported optimization types for a CDN profile.</span></span>

## <span data-ttu-id="7f454-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7f454-113">PARAMETERS</span></span>

### <span data-ttu-id="7f454-114">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="7f454-114">-CdnProfile</span></span>
<span data-ttu-id="7f454-115">Az Azure CDN-profil objektuma.</span><span class="sxs-lookup"><span data-stu-id="7f454-115">The Azure CDN profile object.</span></span>

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

### <span data-ttu-id="7f454-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f454-116">-DefaultProfile</span></span>
<span data-ttu-id="7f454-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7f454-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7f454-118">-Fájlnév</span><span class="sxs-lookup"><span data-stu-id="7f454-118">-ProfileName</span></span>
<span data-ttu-id="7f454-119">A profil neve.</span><span class="sxs-lookup"><span data-stu-id="7f454-119">The name of the profile.</span></span>

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

### <span data-ttu-id="7f454-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f454-120">-ResourceGroupName</span></span>
<span data-ttu-id="7f454-121">Az az erőforráscsoport, amelyhez a profil tartozik.</span><span class="sxs-lookup"><span data-stu-id="7f454-121">The resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="7f454-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f454-122">CommonParameters</span></span>
<span data-ttu-id="7f454-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7f454-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f454-124">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="7f454-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f454-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7f454-125">INPUTS</span></span>

### <span data-ttu-id="7f454-126">Microsoft. Azure. Command. CDN. models. profil. PSProfile</span><span class="sxs-lookup"><span data-stu-id="7f454-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="7f454-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7f454-127">OUTPUTS</span></span>

### <span data-ttu-id="7f454-128">Microsoft. Azure. Command. CDN. models. profil. PSOptimizationType</span><span class="sxs-lookup"><span data-stu-id="7f454-128">Microsoft.Azure.Commands.Cdn.Models.Profile.PSOptimizationType</span></span>

## <span data-ttu-id="7f454-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7f454-129">NOTES</span></span>

## <span data-ttu-id="7f454-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7f454-130">RELATED LINKS</span></span>
