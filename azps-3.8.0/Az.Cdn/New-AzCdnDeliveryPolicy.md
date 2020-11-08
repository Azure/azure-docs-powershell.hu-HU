---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdndeliverypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryPolicy.md
ms.openlocfilehash: a00e8d11868ae487357f1105d2bc2ae3934a9db9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014907"
---
# <span data-ttu-id="6ba59-101">New-AzCdnDeliveryPolicy</span><span class="sxs-lookup"><span data-stu-id="6ba59-101">New-AzCdnDeliveryPolicy</span></span>

## <span data-ttu-id="6ba59-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6ba59-102">SYNOPSIS</span></span>
<span data-ttu-id="6ba59-103">Kézbesítési házirendet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="6ba59-103">Creates a delivery policy.</span></span>

## <span data-ttu-id="6ba59-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6ba59-104">SYNTAX</span></span>

```
New-AzCdnDeliveryPolicy [-Description <String>] -Rule <PSDeliveryRule[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6ba59-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6ba59-105">DESCRIPTION</span></span>
<span data-ttu-id="6ba59-106">A **New-AzCdnDeliveryPolicy** parancsmag kézbesítési házirendet hoz létre a CDN-végpontok létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="6ba59-106">The **New-AzCdnDeliveryPolicy** cmdlet creates a delivery policy for CDN endpoint creation.</span></span>

## <span data-ttu-id="6ba59-107">Példák</span><span class="sxs-lookup"><span data-stu-id="6ba59-107">EXAMPLES</span></span>

### <span data-ttu-id="6ba59-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="6ba59-108">Example 1</span></span>
```powershell
PS C:\> New-AzCdnDeliveryPolicy -Description "Sample Policy" -Rule $rule

Description   Rules
-----------   -----
Sample Policy {rule1}
```

<span data-ttu-id="6ba59-109">Minta kézbesítési házirend létrehozása</span><span class="sxs-lookup"><span data-stu-id="6ba59-109">Create a sample delivery policy</span></span>

## <span data-ttu-id="6ba59-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6ba59-110">PARAMETERS</span></span>

### <span data-ttu-id="6ba59-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ba59-111">-DefaultProfile</span></span>
<span data-ttu-id="6ba59-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6ba59-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ba59-113">-Leírás</span><span class="sxs-lookup"><span data-stu-id="6ba59-113">-Description</span></span>
<span data-ttu-id="6ba59-114">A házirend leírása</span><span class="sxs-lookup"><span data-stu-id="6ba59-114">Description of the policy</span></span>

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

### <span data-ttu-id="6ba59-115">-Szabály</span><span class="sxs-lookup"><span data-stu-id="6ba59-115">-Rule</span></span>
<span data-ttu-id="6ba59-116">A deliveryRules listája.</span><span class="sxs-lookup"><span data-stu-id="6ba59-116">A list of deliveryRules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRule[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ba59-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ba59-117">CommonParameters</span></span>
<span data-ttu-id="6ba59-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6ba59-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ba59-119">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="6ba59-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ba59-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6ba59-120">INPUTS</span></span>

### <span data-ttu-id="6ba59-121">Nincs</span><span class="sxs-lookup"><span data-stu-id="6ba59-121">None</span></span>

## <span data-ttu-id="6ba59-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6ba59-122">OUTPUTS</span></span>

### <span data-ttu-id="6ba59-123">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryPolicy</span><span class="sxs-lookup"><span data-stu-id="6ba59-123">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryPolicy</span></span>

## <span data-ttu-id="6ba59-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6ba59-124">NOTES</span></span>

## <span data-ttu-id="6ba59-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6ba59-125">RELATED LINKS</span></span>
