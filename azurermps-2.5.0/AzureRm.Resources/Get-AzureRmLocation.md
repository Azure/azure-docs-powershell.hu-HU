---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: DC870E11-2129-4906-8357-D9BC1CF2E08E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermlocation
schema: 2.0.0
ms.openlocfilehash: c5d9d2131ff144f04794d2cf283aaf51ed1450e9
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849534"
---
# <span data-ttu-id="542fa-101">Get-AzureRmLocation</span><span class="sxs-lookup"><span data-stu-id="542fa-101">Get-AzureRmLocation</span></span>

## <span data-ttu-id="542fa-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="542fa-102">SYNOPSIS</span></span>
<span data-ttu-id="542fa-103">Minden hely és a támogatott erőforrás-szolgáltatók beolvasása minden helyhez.</span><span class="sxs-lookup"><span data-stu-id="542fa-103">Gets all locations and the supported resource providers for each location.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="542fa-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="542fa-104">SYNTAX</span></span>

```
Get-AzureRmLocation [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="542fa-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="542fa-105">DESCRIPTION</span></span>
<span data-ttu-id="542fa-106">A **Get-AzureRmLocation** parancsmag minden helyhez megkapja a minden helyet és a támogatott erőforrás-szolgáltatókat.</span><span class="sxs-lookup"><span data-stu-id="542fa-106">The **Get-AzureRmLocation** cmdlet gets all locations and the supported resource providers for each location.</span></span>

## <span data-ttu-id="542fa-107">Példák</span><span class="sxs-lookup"><span data-stu-id="542fa-107">EXAMPLES</span></span>

### <span data-ttu-id="542fa-108">1. példa: a minden hely és a támogatott erőforrás-szolgáltatók beolvasása</span><span class="sxs-lookup"><span data-stu-id="542fa-108">Example 1: Get all locations and the supported resource providers</span></span>
```
PS C:\>Get-AzureRmLocation
```

<span data-ttu-id="542fa-109">Ez a parancs minden helyet és a támogatott erőforrás-szolgáltatókat beolvassa az egyes helyekhez.</span><span class="sxs-lookup"><span data-stu-id="542fa-109">This command gets all locations and the supported resource providers for each location.</span></span>

## <span data-ttu-id="542fa-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="542fa-110">PARAMETERS</span></span>

### <span data-ttu-id="542fa-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="542fa-111">-ApiVersion</span></span>
<span data-ttu-id="542fa-112">Az erőforrás-szolgáltató által támogatott API-verziót adja meg.</span><span class="sxs-lookup"><span data-stu-id="542fa-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="542fa-113">Az alapértelmezett verziótól eltérő verziót is megadhat.</span><span class="sxs-lookup"><span data-stu-id="542fa-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="542fa-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="542fa-114">-DefaultProfile</span></span>
<span data-ttu-id="542fa-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="542fa-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="542fa-116">-Pre</span><span class="sxs-lookup"><span data-stu-id="542fa-116">-Pre</span></span>
<span data-ttu-id="542fa-117">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="542fa-117">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="542fa-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="542fa-118">CommonParameters</span></span>
<span data-ttu-id="542fa-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="542fa-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="542fa-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="542fa-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="542fa-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="542fa-121">INPUTS</span></span>

## <span data-ttu-id="542fa-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="542fa-122">OUTPUTS</span></span>

## <span data-ttu-id="542fa-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="542fa-123">NOTES</span></span>

## <span data-ttu-id="542fa-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="542fa-124">RELATED LINKS</span></span>
