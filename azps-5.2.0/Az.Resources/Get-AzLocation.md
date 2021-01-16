---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: DC870E11-2129-4906-8357-D9BC1CF2E08E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azlocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzLocation.md
ms.openlocfilehash: f14da4760f70c8e4ba95136b81a884f830f4f44a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98325327"
---
# <span data-ttu-id="0c7c6-101">Get-AzLocation</span><span class="sxs-lookup"><span data-stu-id="0c7c6-101">Get-AzLocation</span></span>

## <span data-ttu-id="0c7c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c7c6-102">SYNOPSIS</span></span>
<span data-ttu-id="0c7c6-103">Lekérte az összes helyet és a támogatott erőforrás-szolgáltatókat az egyes helyekhez.</span><span class="sxs-lookup"><span data-stu-id="0c7c6-103">Gets all locations and the supported resource providers for each location.</span></span>

## <span data-ttu-id="0c7c6-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0c7c6-104">SYNTAX</span></span>

```
Get-AzLocation [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0c7c6-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0c7c6-105">DESCRIPTION</span></span>
<span data-ttu-id="0c7c6-106">A **Get-AzLocation** parancsmag minden helyet és a támogatott erőforrás-szolgáltatókat minden helyhez megkapja.</span><span class="sxs-lookup"><span data-stu-id="0c7c6-106">The **Get-AzLocation** cmdlet gets all locations and the supported resource providers for each location.</span></span>

## <span data-ttu-id="0c7c6-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0c7c6-107">EXAMPLES</span></span>

### <span data-ttu-id="0c7c6-108">1. példa: Az összes hely és a támogatott erőforrás-szolgáltatók lekérte</span><span class="sxs-lookup"><span data-stu-id="0c7c6-108">Example 1: Get all locations and the supported resource providers</span></span>
```
PS C:\>Get-AzLocation
```

<span data-ttu-id="0c7c6-109">Ez a parancs az összes helyet és a támogatott erőforrás-szolgáltatókat beveszi az egyes helyekhez.</span><span class="sxs-lookup"><span data-stu-id="0c7c6-109">This command gets all locations and the supported resource providers for each location.</span></span>

## <span data-ttu-id="0c7c6-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0c7c6-110">PARAMETERS</span></span>

### <span data-ttu-id="0c7c6-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="0c7c6-111">-ApiVersion</span></span>
<span data-ttu-id="0c7c6-112">Az erőforrásszolgáltató által támogatott API-verziót adja meg.</span><span class="sxs-lookup"><span data-stu-id="0c7c6-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="0c7c6-113">Az alapértelmezett verziótól eltérő verziót is megadhat.</span><span class="sxs-lookup"><span data-stu-id="0c7c6-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="0c7c6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c7c6-114">-DefaultProfile</span></span>
<span data-ttu-id="0c7c6-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="0c7c6-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0c7c6-116">-Pre</span><span class="sxs-lookup"><span data-stu-id="0c7c6-116">-Pre</span></span>
<span data-ttu-id="0c7c6-117">Azt jelzi, hogy ez a parancsmag figyelembe veszi a megjelenés előtt ható API-verziókat, amikor automatikusan meghatározza, hogy melyik verziót kell használni.</span><span class="sxs-lookup"><span data-stu-id="0c7c6-117">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="0c7c6-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c7c6-118">CommonParameters</span></span>
<span data-ttu-id="0c7c6-119">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c7c6-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c7c6-120">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0c7c6-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c7c6-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0c7c6-121">INPUTS</span></span>

### <span data-ttu-id="0c7c6-122">Nincs</span><span class="sxs-lookup"><span data-stu-id="0c7c6-122">None</span></span>

## <span data-ttu-id="0c7c6-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0c7c6-123">OUTPUTS</span></span>

### <span data-ttu-id="0c7c6-124">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProviderLocation</span><span class="sxs-lookup"><span data-stu-id="0c7c6-124">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProviderLocation</span></span>

## <span data-ttu-id="0c7c6-125">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0c7c6-125">NOTES</span></span>

## <span data-ttu-id="0c7c6-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0c7c6-126">RELATED LINKS</span></span>
