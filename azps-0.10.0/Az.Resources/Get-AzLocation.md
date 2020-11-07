---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: DC870E11-2129-4906-8357-D9BC1CF2E08E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azlocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzLocation.md
ms.openlocfilehash: 4aedbb502780a08d0ce5556af84a445ab44552f5
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843454"
---
# <span data-ttu-id="e30bd-101">Get-AzLocation</span><span class="sxs-lookup"><span data-stu-id="e30bd-101">Get-AzLocation</span></span>

## <span data-ttu-id="e30bd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e30bd-102">SYNOPSIS</span></span>
<span data-ttu-id="e30bd-103">Minden hely és a támogatott erőforrás-szolgáltatók beolvasása minden helyhez.</span><span class="sxs-lookup"><span data-stu-id="e30bd-103">Gets all locations and the supported resource providers for each location.</span></span>

## <span data-ttu-id="e30bd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e30bd-104">SYNTAX</span></span>

```
Get-AzLocation [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e30bd-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e30bd-105">DESCRIPTION</span></span>
<span data-ttu-id="e30bd-106">A **Get-AzLocation** parancsmag minden helyhez megkapja a minden helyet és a támogatott erőforrás-szolgáltatókat.</span><span class="sxs-lookup"><span data-stu-id="e30bd-106">The **Get-AzLocation** cmdlet gets all locations and the supported resource providers for each location.</span></span>

## <span data-ttu-id="e30bd-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e30bd-107">EXAMPLES</span></span>

### <span data-ttu-id="e30bd-108">1. példa: a minden hely és a támogatott erőforrás-szolgáltatók beolvasása</span><span class="sxs-lookup"><span data-stu-id="e30bd-108">Example 1: Get all locations and the supported resource providers</span></span>
```
PS C:\>Get-AzLocation
```

<span data-ttu-id="e30bd-109">Ez a parancs minden helyet és a támogatott erőforrás-szolgáltatókat beolvassa az egyes helyekhez.</span><span class="sxs-lookup"><span data-stu-id="e30bd-109">This command gets all locations and the supported resource providers for each location.</span></span>

## <span data-ttu-id="e30bd-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e30bd-110">PARAMETERS</span></span>

### <span data-ttu-id="e30bd-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="e30bd-111">-ApiVersion</span></span>
<span data-ttu-id="e30bd-112">Az erőforrás-szolgáltató által támogatott API-verziót adja meg.</span><span class="sxs-lookup"><span data-stu-id="e30bd-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="e30bd-113">Az alapértelmezett verziótól eltérő verziót is megadhat.</span><span class="sxs-lookup"><span data-stu-id="e30bd-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="e30bd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e30bd-114">-DefaultProfile</span></span>
<span data-ttu-id="e30bd-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="e30bd-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e30bd-116">-Pre</span><span class="sxs-lookup"><span data-stu-id="e30bd-116">-Pre</span></span>
<span data-ttu-id="e30bd-117">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="e30bd-117">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="e30bd-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e30bd-118">CommonParameters</span></span>
<span data-ttu-id="e30bd-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e30bd-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e30bd-120">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e30bd-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e30bd-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e30bd-121">INPUTS</span></span>

## <span data-ttu-id="e30bd-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e30bd-122">OUTPUTS</span></span>

## <span data-ttu-id="e30bd-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e30bd-123">NOTES</span></span>

## <span data-ttu-id="e30bd-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e30bd-124">RELATED LINKS</span></span>
