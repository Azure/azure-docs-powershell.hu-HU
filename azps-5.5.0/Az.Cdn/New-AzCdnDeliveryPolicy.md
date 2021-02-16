---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdndeliverypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryPolicy.md
ms.openlocfilehash: a00e8d11868ae487357f1105d2bc2ae3934a9db9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100145114"
---
# <span data-ttu-id="79e13-101">New-AzCdnDeliveryPolicy</span><span class="sxs-lookup"><span data-stu-id="79e13-101">New-AzCdnDeliveryPolicy</span></span>

## <span data-ttu-id="79e13-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79e13-102">SYNOPSIS</span></span>
<span data-ttu-id="79e13-103">Kézbesítési házirendet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="79e13-103">Creates a delivery policy.</span></span>

## <span data-ttu-id="79e13-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="79e13-104">SYNTAX</span></span>

```
New-AzCdnDeliveryPolicy [-Description <String>] -Rule <PSDeliveryRule[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="79e13-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="79e13-105">DESCRIPTION</span></span>
<span data-ttu-id="79e13-106">A **New-AzCdnDeliveryPolicy parancsmag** kézbesítési házirendet hoz létre a CDN-végpontok létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="79e13-106">The **New-AzCdnDeliveryPolicy** cmdlet creates a delivery policy for CDN endpoint creation.</span></span>

## <span data-ttu-id="79e13-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="79e13-107">EXAMPLES</span></span>

### <span data-ttu-id="79e13-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="79e13-108">Example 1</span></span>
```powershell
PS C:\> New-AzCdnDeliveryPolicy -Description "Sample Policy" -Rule $rule

Description   Rules
-----------   -----
Sample Policy {rule1}
```

<span data-ttu-id="79e13-109">Minta kézbesítési házirend létrehozása</span><span class="sxs-lookup"><span data-stu-id="79e13-109">Create a sample delivery policy</span></span>

## <span data-ttu-id="79e13-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="79e13-110">PARAMETERS</span></span>

### <span data-ttu-id="79e13-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79e13-111">-DefaultProfile</span></span>
<span data-ttu-id="79e13-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="79e13-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="79e13-113">-Leírás</span><span class="sxs-lookup"><span data-stu-id="79e13-113">-Description</span></span>
<span data-ttu-id="79e13-114">A házirend leírása</span><span class="sxs-lookup"><span data-stu-id="79e13-114">Description of the policy</span></span>

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

### <span data-ttu-id="79e13-115">-Rule</span><span class="sxs-lookup"><span data-stu-id="79e13-115">-Rule</span></span>
<span data-ttu-id="79e13-116">A kézbesítésiszabályok listája.</span><span class="sxs-lookup"><span data-stu-id="79e13-116">A list of deliveryRules.</span></span>

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

### <span data-ttu-id="79e13-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79e13-117">CommonParameters</span></span>
<span data-ttu-id="79e13-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79e13-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79e13-119">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="79e13-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79e13-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="79e13-120">INPUTS</span></span>

### <span data-ttu-id="79e13-121">Nincs</span><span class="sxs-lookup"><span data-stu-id="79e13-121">None</span></span>

## <span data-ttu-id="79e13-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="79e13-122">OUTPUTS</span></span>

### <span data-ttu-id="79e13-123">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryPolicy</span><span class="sxs-lookup"><span data-stu-id="79e13-123">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryPolicy</span></span>

## <span data-ttu-id="79e13-124">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="79e13-124">NOTES</span></span>

## <span data-ttu-id="79e13-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="79e13-125">RELATED LINKS</span></span>
