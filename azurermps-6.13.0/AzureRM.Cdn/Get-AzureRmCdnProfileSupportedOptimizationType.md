---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/get-azurermcdnprofilesupportedoptimizationtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnProfileSupportedOptimizationType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnProfileSupportedOptimizationType.md
ms.openlocfilehash: e6434b2b5b07cad811f245d72e1d6bd34da63bb4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501191"
---
# <span data-ttu-id="fa045-101">Get-AzureRmCdnProfileSupportedOptimizationType</span><span class="sxs-lookup"><span data-stu-id="fa045-101">Get-AzureRmCdnProfileSupportedOptimizationType</span></span>

## <span data-ttu-id="fa045-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fa045-102">SYNOPSIS</span></span>
<span data-ttu-id="fa045-103">A támogatott optimalizálási típusokat kapja egy CDN-profilban.</span><span class="sxs-lookup"><span data-stu-id="fa045-103">Gets the supported optimization types for a CDN profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fa045-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fa045-104">SYNTAX</span></span>

### <span data-ttu-id="fa045-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fa045-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzureRmCdnProfileSupportedOptimizationType -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fa045-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fa045-106">ByObjectParameterSet</span></span>
```
Get-AzureRmCdnProfileSupportedOptimizationType -CdnProfile <PSProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fa045-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="fa045-107">DESCRIPTION</span></span>
<span data-ttu-id="fa045-108">A **Get-AzureRmCdnProfileSupportedOptimizationType** parancsmag az aktuális profil támogatott optimalizálási típusait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="fa045-108">The **Get-AzureRmCdnProfileSupportedOptimizationType** cmdlet gets the supported optimization types for the current profile.</span></span> <span data-ttu-id="fa045-109">A felhasználók létrehozhatnak egy olyan végpontot, amely egy optimalizálási típust használ a felsorolt értékekkel.</span><span class="sxs-lookup"><span data-stu-id="fa045-109">A user can create an endpoint with an optimization type from the listed values.</span></span>

## <span data-ttu-id="fa045-110">Példák</span><span class="sxs-lookup"><span data-stu-id="fa045-110">EXAMPLES</span></span>

### <span data-ttu-id="fa045-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="fa045-111">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmCdnProfileSupportedOptimizationType -ProfileName $profileName -ResourceGroupName $resourceGroupName
OptimizationType: GeneralWebDelivery
OptimizationType: DynamicSiteAcceleration
```

<span data-ttu-id="fa045-112">Beszerezhet egy CDN-profil támogatott optimalizálási típusait.</span><span class="sxs-lookup"><span data-stu-id="fa045-112">Get the supported optimization types for a CDN profile.</span></span>

## <span data-ttu-id="fa045-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fa045-113">PARAMETERS</span></span>

### <span data-ttu-id="fa045-114">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="fa045-114">-CdnProfile</span></span>
<span data-ttu-id="fa045-115">Az Azure CDN-profil objektuma.</span><span class="sxs-lookup"><span data-stu-id="fa045-115">The Azure CDN profile object.</span></span>

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

### <span data-ttu-id="fa045-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa045-116">-DefaultProfile</span></span>
<span data-ttu-id="fa045-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fa045-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa045-118">-Fájlnév</span><span class="sxs-lookup"><span data-stu-id="fa045-118">-ProfileName</span></span>
<span data-ttu-id="fa045-119">A profil neve.</span><span class="sxs-lookup"><span data-stu-id="fa045-119">The name of the profile.</span></span>

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

### <span data-ttu-id="fa045-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa045-120">-ResourceGroupName</span></span>
<span data-ttu-id="fa045-121">Az az erőforráscsoport, amelyhez a profil tartozik.</span><span class="sxs-lookup"><span data-stu-id="fa045-121">The resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="fa045-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa045-122">CommonParameters</span></span>
<span data-ttu-id="fa045-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fa045-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa045-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa045-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa045-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fa045-125">INPUTS</span></span>

### <span data-ttu-id="fa045-126">Microsoft. Azure. Command. CDN. models. profil. PSProfile</span><span class="sxs-lookup"><span data-stu-id="fa045-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>
<span data-ttu-id="fa045-127">Paraméterek: CdnProfile (ByValue)</span><span class="sxs-lookup"><span data-stu-id="fa045-127">Parameters: CdnProfile (ByValue)</span></span>

## <span data-ttu-id="fa045-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fa045-128">OUTPUTS</span></span>

### <span data-ttu-id="fa045-129">Microsoft. Azure. Command. CDN. models. profil. PSOptimizationType</span><span class="sxs-lookup"><span data-stu-id="fa045-129">Microsoft.Azure.Commands.Cdn.Models.Profile.PSOptimizationType</span></span>

## <span data-ttu-id="fa045-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fa045-130">NOTES</span></span>

## <span data-ttu-id="fa045-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fa045-131">RELATED LINKS</span></span>
