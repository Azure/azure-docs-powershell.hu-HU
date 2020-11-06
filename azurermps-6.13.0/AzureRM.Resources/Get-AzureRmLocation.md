---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: DC870E11-2129-4906-8357-D9BC1CF2E08E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermlocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmLocation.md
ms.openlocfilehash: 6052a621b43cd0b51170e9a502a38df46d38e17d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495707"
---
# <span data-ttu-id="1f656-101">Get-AzureRmLocation</span><span class="sxs-lookup"><span data-stu-id="1f656-101">Get-AzureRmLocation</span></span>

## <span data-ttu-id="1f656-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1f656-102">SYNOPSIS</span></span>
<span data-ttu-id="1f656-103">Minden hely és a támogatott erőforrás-szolgáltatók beolvasása minden helyhez.</span><span class="sxs-lookup"><span data-stu-id="1f656-103">Gets all locations and the supported resource providers for each location.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1f656-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1f656-104">SYNTAX</span></span>

```
Get-AzureRmLocation [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1f656-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="1f656-105">DESCRIPTION</span></span>
<span data-ttu-id="1f656-106">A **Get-AzureRmLocation** parancsmag minden helyhez megkapja a minden helyet és a támogatott erőforrás-szolgáltatókat.</span><span class="sxs-lookup"><span data-stu-id="1f656-106">The **Get-AzureRmLocation** cmdlet gets all locations and the supported resource providers for each location.</span></span>

## <span data-ttu-id="1f656-107">Példák</span><span class="sxs-lookup"><span data-stu-id="1f656-107">EXAMPLES</span></span>

### <span data-ttu-id="1f656-108">1. példa: a minden hely és a támogatott erőforrás-szolgáltatók beolvasása</span><span class="sxs-lookup"><span data-stu-id="1f656-108">Example 1: Get all locations and the supported resource providers</span></span>
```
PS C:\>Get-AzureRmLocation
```

<span data-ttu-id="1f656-109">Ez a parancs minden helyet és a támogatott erőforrás-szolgáltatókat beolvassa az egyes helyekhez.</span><span class="sxs-lookup"><span data-stu-id="1f656-109">This command gets all locations and the supported resource providers for each location.</span></span>

## <span data-ttu-id="1f656-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1f656-110">PARAMETERS</span></span>

### <span data-ttu-id="1f656-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="1f656-111">-ApiVersion</span></span>
<span data-ttu-id="1f656-112">Az erőforrás-szolgáltató által támogatott API-verziót adja meg.</span><span class="sxs-lookup"><span data-stu-id="1f656-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="1f656-113">Az alapértelmezett verziótól eltérő verziót is megadhat.</span><span class="sxs-lookup"><span data-stu-id="1f656-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="1f656-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f656-114">-DefaultProfile</span></span>
<span data-ttu-id="1f656-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="1f656-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1f656-116">-Pre</span><span class="sxs-lookup"><span data-stu-id="1f656-116">-Pre</span></span>
<span data-ttu-id="1f656-117">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="1f656-117">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f656-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f656-118">CommonParameters</span></span>
<span data-ttu-id="1f656-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1f656-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f656-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f656-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f656-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1f656-121">INPUTS</span></span>

## <span data-ttu-id="1f656-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1f656-122">OUTPUTS</span></span>

## <span data-ttu-id="1f656-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1f656-123">NOTES</span></span>

## <span data-ttu-id="1f656-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1f656-124">RELATED LINKS</span></span>
