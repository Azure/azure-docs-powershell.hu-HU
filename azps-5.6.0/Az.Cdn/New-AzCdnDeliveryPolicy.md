---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/powershell/module/az.cdn/new-azcdndeliverypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryPolicy.md
ms.openlocfilehash: 01cadd267a98cab239b7a83357d308d8dd2d32bd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001845"
---
# <span data-ttu-id="f4d67-101">New-AzCdnDeliveryPolicy</span><span class="sxs-lookup"><span data-stu-id="f4d67-101">New-AzCdnDeliveryPolicy</span></span>

## <span data-ttu-id="f4d67-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4d67-102">SYNOPSIS</span></span>
<span data-ttu-id="f4d67-103">Kézbesítési házirendet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="f4d67-103">Creates a delivery policy.</span></span>

## <span data-ttu-id="f4d67-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f4d67-104">SYNTAX</span></span>

```
New-AzCdnDeliveryPolicy [-Description <String>] -Rule <PSDeliveryRule[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f4d67-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f4d67-105">DESCRIPTION</span></span>
<span data-ttu-id="f4d67-106">A **New-AzCdnDeliveryPolicy parancsmag** kézbesítési házirendet hoz létre a CDN-végpontok létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="f4d67-106">The **New-AzCdnDeliveryPolicy** cmdlet creates a delivery policy for CDN endpoint creation.</span></span>

## <span data-ttu-id="f4d67-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f4d67-107">EXAMPLES</span></span>

### <span data-ttu-id="f4d67-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="f4d67-108">Example 1</span></span>
```powershell
PS C:\> New-AzCdnDeliveryPolicy -Description "Sample Policy" -Rule $rule

Description   Rules
-----------   -----
Sample Policy {rule1}
```

<span data-ttu-id="f4d67-109">Minta kézbesítési házirend létrehozása</span><span class="sxs-lookup"><span data-stu-id="f4d67-109">Create a sample delivery policy</span></span>

## <span data-ttu-id="f4d67-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f4d67-110">PARAMETERS</span></span>

### <span data-ttu-id="f4d67-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4d67-111">-DefaultProfile</span></span>
<span data-ttu-id="f4d67-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f4d67-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4d67-113">-Leírás</span><span class="sxs-lookup"><span data-stu-id="f4d67-113">-Description</span></span>
<span data-ttu-id="f4d67-114">A házirend leírása</span><span class="sxs-lookup"><span data-stu-id="f4d67-114">Description of the policy</span></span>

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

### <span data-ttu-id="f4d67-115">-Rule</span><span class="sxs-lookup"><span data-stu-id="f4d67-115">-Rule</span></span>
<span data-ttu-id="f4d67-116">A kézbesítésiszabályok listája.</span><span class="sxs-lookup"><span data-stu-id="f4d67-116">A list of deliveryRules.</span></span>

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

### <span data-ttu-id="f4d67-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4d67-117">CommonParameters</span></span>
<span data-ttu-id="f4d67-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4d67-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4d67-119">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f4d67-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4d67-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f4d67-120">INPUTS</span></span>

### <span data-ttu-id="f4d67-121">Nincs</span><span class="sxs-lookup"><span data-stu-id="f4d67-121">None</span></span>

## <span data-ttu-id="f4d67-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f4d67-122">OUTPUTS</span></span>

### <span data-ttu-id="f4d67-123">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryPolicy</span><span class="sxs-lookup"><span data-stu-id="f4d67-123">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryPolicy</span></span>

## <span data-ttu-id="f4d67-124">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f4d67-124">NOTES</span></span>

## <span data-ttu-id="f4d67-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f4d67-125">RELATED LINKS</span></span>
