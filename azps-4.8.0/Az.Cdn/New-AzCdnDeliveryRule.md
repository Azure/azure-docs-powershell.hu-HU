---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdndeliveryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRule.md
ms.openlocfilehash: df04d3f3dd19c62c37ffbb82cbd57e50c3d73c15
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94017888"
---
# <span data-ttu-id="fb91a-101">New-AzCdnDeliveryRule</span><span class="sxs-lookup"><span data-stu-id="fb91a-101">New-AzCdnDeliveryRule</span></span>

## <span data-ttu-id="fb91a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fb91a-102">SYNOPSIS</span></span>
<span data-ttu-id="fb91a-103">Kézbesítési szabály létrehozása</span><span class="sxs-lookup"><span data-stu-id="fb91a-103">Creates a delivery rule.</span></span>

## <span data-ttu-id="fb91a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fb91a-104">SYNTAX</span></span>

```
New-AzCdnDeliveryRule [-Name <String>] -Order <Int32> [-Condition <PSDeliveryRuleCondition[]>]
 -Action <PSDeliveryRuleAction[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fb91a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="fb91a-105">DESCRIPTION</span></span>
<span data-ttu-id="fb91a-106">A **New-AzCdnDeliveryRule** parancsmag szállítási szabályt hoz létre a CDN-végpontok létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="fb91a-106">The **New-AzCdnDeliveryRule** cmdlet creates a delivery rule for CDN endpoint creation.</span></span>

## <span data-ttu-id="fb91a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="fb91a-107">EXAMPLES</span></span>

### <span data-ttu-id="fb91a-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="fb91a-108">Example 1</span></span>
```powershell
PS C:\> New-AzCdnDeliveryRule -Name "rule1" -Order 1 -Condition $cond1 -Action $action1

Name  Order Actions           Conditions
----  ----- -------           ----------
rule1     1 {Accept-Encoding} {Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleCondition}
```

<span data-ttu-id="fb91a-109">Egyszerű szabály létrehozása</span><span class="sxs-lookup"><span data-stu-id="fb91a-109">Create a simple rule.</span></span>

## <span data-ttu-id="fb91a-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fb91a-110">PARAMETERS</span></span>

### <span data-ttu-id="fb91a-111">-Műveletek</span><span class="sxs-lookup"><span data-stu-id="fb91a-111">-Action</span></span>
<span data-ttu-id="fb91a-112">Azoknak a műveleteknek a listája, amelyeket egy szabály minden feltételei teljesülése esetén végre kell hajtani.</span><span class="sxs-lookup"><span data-stu-id="fb91a-112">A list of actions that are executed when all the conditions of a rule are satisfied.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleAction[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb91a-113">-Feltétel</span><span class="sxs-lookup"><span data-stu-id="fb91a-113">-Condition</span></span>
<span data-ttu-id="fb91a-114">Azoknak a feltételeknek a listáját, amelyeknek a végrehajtandó műveletek esetében meg kell egyezniük.</span><span class="sxs-lookup"><span data-stu-id="fb91a-114">A list of conditions that must be matched for the actions to be executed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleCondition[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb91a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb91a-115">-DefaultProfile</span></span>
<span data-ttu-id="fb91a-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fb91a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb91a-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="fb91a-117">-Name</span></span>
<span data-ttu-id="fb91a-118">A szabály neve</span><span class="sxs-lookup"><span data-stu-id="fb91a-118">Name of the rule</span></span>

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

### <span data-ttu-id="fb91a-119">-Order (rendelés)</span><span class="sxs-lookup"><span data-stu-id="fb91a-119">-Order</span></span>
<span data-ttu-id="fb91a-120">A szabály sorrendje</span><span class="sxs-lookup"><span data-stu-id="fb91a-120">Order of the rule</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb91a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb91a-121">CommonParameters</span></span>
<span data-ttu-id="fb91a-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fb91a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb91a-123">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="fb91a-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb91a-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fb91a-124">INPUTS</span></span>

### <span data-ttu-id="fb91a-125">Nincs</span><span class="sxs-lookup"><span data-stu-id="fb91a-125">None</span></span>

## <span data-ttu-id="fb91a-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fb91a-126">OUTPUTS</span></span>

### <span data-ttu-id="fb91a-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRule</span><span class="sxs-lookup"><span data-stu-id="fb91a-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRule</span></span>

## <span data-ttu-id="fb91a-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fb91a-128">NOTES</span></span>

## <span data-ttu-id="fb91a-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fb91a-129">RELATED LINKS</span></span>
