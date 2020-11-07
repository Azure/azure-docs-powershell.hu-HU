---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: DC870E11-2129-4906-8357-D9BC1CF2E08E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azlocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzLocation.md
ms.openlocfilehash: 17bc16b38bc967f9997b22d7dd86b056253d8a18
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838942"
---
# <span data-ttu-id="a10ab-101">Get-AzLocation</span><span class="sxs-lookup"><span data-stu-id="a10ab-101">Get-AzLocation</span></span>

## <span data-ttu-id="a10ab-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a10ab-102">SYNOPSIS</span></span>
<span data-ttu-id="a10ab-103">Minden hely és a támogatott erőforrás-szolgáltatók beolvasása minden helyhez.</span><span class="sxs-lookup"><span data-stu-id="a10ab-103">Gets all locations and the supported resource providers for each location.</span></span>

## <span data-ttu-id="a10ab-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a10ab-104">SYNTAX</span></span>

```
Get-AzLocation [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a10ab-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a10ab-105">DESCRIPTION</span></span>
<span data-ttu-id="a10ab-106">A **Get-AzLocation** parancsmag minden helyhez megkapja a minden helyet és a támogatott erőforrás-szolgáltatókat.</span><span class="sxs-lookup"><span data-stu-id="a10ab-106">The **Get-AzLocation** cmdlet gets all locations and the supported resource providers for each location.</span></span>

## <span data-ttu-id="a10ab-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a10ab-107">EXAMPLES</span></span>

### <span data-ttu-id="a10ab-108">1. példa: a minden hely és a támogatott erőforrás-szolgáltatók beolvasása</span><span class="sxs-lookup"><span data-stu-id="a10ab-108">Example 1: Get all locations and the supported resource providers</span></span>
```
PS C:\>Get-AzLocation
```

<span data-ttu-id="a10ab-109">Ez a parancs minden helyet és a támogatott erőforrás-szolgáltatókat beolvassa az egyes helyekhez.</span><span class="sxs-lookup"><span data-stu-id="a10ab-109">This command gets all locations and the supported resource providers for each location.</span></span>

## <span data-ttu-id="a10ab-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a10ab-110">PARAMETERS</span></span>

### <span data-ttu-id="a10ab-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="a10ab-111">-ApiVersion</span></span>
<span data-ttu-id="a10ab-112">Az erőforrás-szolgáltató által támogatott API-verziót adja meg.</span><span class="sxs-lookup"><span data-stu-id="a10ab-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="a10ab-113">Az alapértelmezett verziótól eltérő verziót is megadhat.</span><span class="sxs-lookup"><span data-stu-id="a10ab-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="a10ab-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a10ab-114">-DefaultProfile</span></span>
<span data-ttu-id="a10ab-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="a10ab-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a10ab-116">-Pre</span><span class="sxs-lookup"><span data-stu-id="a10ab-116">-Pre</span></span>
<span data-ttu-id="a10ab-117">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="a10ab-117">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="a10ab-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a10ab-118">CommonParameters</span></span>
<span data-ttu-id="a10ab-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a10ab-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a10ab-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a10ab-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a10ab-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a10ab-121">INPUTS</span></span>

### <span data-ttu-id="a10ab-122">Nincs</span><span class="sxs-lookup"><span data-stu-id="a10ab-122">None</span></span>

## <span data-ttu-id="a10ab-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a10ab-123">OUTPUTS</span></span>

### <span data-ttu-id="a10ab-124">Microsoft. Azure. Command. ResourceManager. Parancsmags. SdkModels. PSResourceProviderLocation</span><span class="sxs-lookup"><span data-stu-id="a10ab-124">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProviderLocation</span></span>

## <span data-ttu-id="a10ab-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a10ab-125">NOTES</span></span>

## <span data-ttu-id="a10ab-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a10ab-126">RELATED LINKS</span></span>
