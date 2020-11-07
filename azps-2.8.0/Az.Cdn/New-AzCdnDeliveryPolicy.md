---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdndeliverypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryPolicy.md
ms.openlocfilehash: 9dcb9720c194fbad4e82607f50132c9bbc5415c4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667590"
---
# <span data-ttu-id="7c783-101">New-AzCdnDeliveryPolicy</span><span class="sxs-lookup"><span data-stu-id="7c783-101">New-AzCdnDeliveryPolicy</span></span>

## <span data-ttu-id="7c783-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7c783-102">SYNOPSIS</span></span>
<span data-ttu-id="7c783-103">Kézbesítési házirendet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="7c783-103">Creates a delivery policy.</span></span>

## <span data-ttu-id="7c783-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7c783-104">SYNTAX</span></span>

```
New-AzCdnDeliveryPolicy [-Description <String>] -Rule <PSDeliveryRule[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7c783-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7c783-105">DESCRIPTION</span></span>
<span data-ttu-id="7c783-106">A **New-AzCdnDeliveryPolicy** parancsmag kézbesítési házirendet hoz létre a CDN-végpontok létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="7c783-106">The **New-AzCdnDeliveryPolicy** cmdlet creates a delivery policy for CDN endpoint creation.</span></span>

## <span data-ttu-id="7c783-107">Példák</span><span class="sxs-lookup"><span data-stu-id="7c783-107">EXAMPLES</span></span>

### <span data-ttu-id="7c783-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="7c783-108">Example 1</span></span>
```powershell
PS C:\> New-AzCdnDeliveryPolicy -Description "Sample Policy" -Rule $rule

Description   Rules
-----------   -----
Sample Policy {rule1}
```

<span data-ttu-id="7c783-109">Minta kézbesítési házirend létrehozása</span><span class="sxs-lookup"><span data-stu-id="7c783-109">Create a sample delivery policy</span></span>

## <span data-ttu-id="7c783-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7c783-110">PARAMETERS</span></span>

### <span data-ttu-id="7c783-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c783-111">-DefaultProfile</span></span>
<span data-ttu-id="7c783-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7c783-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c783-113">-Leírás</span><span class="sxs-lookup"><span data-stu-id="7c783-113">-Description</span></span>
<span data-ttu-id="7c783-114">A házirend leírása</span><span class="sxs-lookup"><span data-stu-id="7c783-114">Description of the policy</span></span>

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

### <span data-ttu-id="7c783-115">-Szabály</span><span class="sxs-lookup"><span data-stu-id="7c783-115">-Rule</span></span>
<span data-ttu-id="7c783-116">A deliveryRules listája.</span><span class="sxs-lookup"><span data-stu-id="7c783-116">A list of deliveryRules.</span></span>

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

### <span data-ttu-id="7c783-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c783-117">CommonParameters</span></span>
<span data-ttu-id="7c783-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7c783-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c783-119">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="7c783-119">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c783-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7c783-120">INPUTS</span></span>

### <span data-ttu-id="7c783-121">Nincs</span><span class="sxs-lookup"><span data-stu-id="7c783-121">None</span></span>

## <span data-ttu-id="7c783-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7c783-122">OUTPUTS</span></span>

### <span data-ttu-id="7c783-123">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryPolicy</span><span class="sxs-lookup"><span data-stu-id="7c783-123">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryPolicy</span></span>

## <span data-ttu-id="7c783-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7c783-124">NOTES</span></span>

## <span data-ttu-id="7c783-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7c783-125">RELATED LINKS</span></span>
