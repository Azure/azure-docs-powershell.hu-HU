---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdndeliveryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRule.md
ms.openlocfilehash: df04d3f3dd19c62c37ffbb82cbd57e50c3d73c15
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014908"
---
# <span data-ttu-id="ef986-101">New-AzCdnDeliveryRule</span><span class="sxs-lookup"><span data-stu-id="ef986-101">New-AzCdnDeliveryRule</span></span>

## <span data-ttu-id="ef986-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ef986-102">SYNOPSIS</span></span>
<span data-ttu-id="ef986-103">Kézbesítési szabály létrehozása</span><span class="sxs-lookup"><span data-stu-id="ef986-103">Creates a delivery rule.</span></span>

## <span data-ttu-id="ef986-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ef986-104">SYNTAX</span></span>

```
New-AzCdnDeliveryRule [-Name <String>] -Order <Int32> [-Condition <PSDeliveryRuleCondition[]>]
 -Action <PSDeliveryRuleAction[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ef986-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ef986-105">DESCRIPTION</span></span>
<span data-ttu-id="ef986-106">A **New-AzCdnDeliveryRule** parancsmag szállítási szabályt hoz létre a CDN-végpontok létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="ef986-106">The **New-AzCdnDeliveryRule** cmdlet creates a delivery rule for CDN endpoint creation.</span></span>

## <span data-ttu-id="ef986-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ef986-107">EXAMPLES</span></span>

### <span data-ttu-id="ef986-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ef986-108">Example 1</span></span>
```powershell
PS C:\> New-AzCdnDeliveryRule -Name "rule1" -Order 1 -Condition $cond1 -Action $action1

Name  Order Actions           Conditions
----  ----- -------           ----------
rule1     1 {Accept-Encoding} {Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleCondition}
```

<span data-ttu-id="ef986-109">Egyszerű szabály létrehozása</span><span class="sxs-lookup"><span data-stu-id="ef986-109">Create a simple rule.</span></span>

## <span data-ttu-id="ef986-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ef986-110">PARAMETERS</span></span>

### <span data-ttu-id="ef986-111">-Műveletek</span><span class="sxs-lookup"><span data-stu-id="ef986-111">-Action</span></span>
<span data-ttu-id="ef986-112">Azoknak a műveleteknek a listája, amelyeket egy szabály minden feltételei teljesülése esetén végre kell hajtani.</span><span class="sxs-lookup"><span data-stu-id="ef986-112">A list of actions that are executed when all the conditions of a rule are satisfied.</span></span>

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

### <span data-ttu-id="ef986-113">-Feltétel</span><span class="sxs-lookup"><span data-stu-id="ef986-113">-Condition</span></span>
<span data-ttu-id="ef986-114">Azoknak a feltételeknek a listáját, amelyeknek a végrehajtandó műveletek esetében meg kell egyezniük.</span><span class="sxs-lookup"><span data-stu-id="ef986-114">A list of conditions that must be matched for the actions to be executed.</span></span>

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

### <span data-ttu-id="ef986-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef986-115">-DefaultProfile</span></span>
<span data-ttu-id="ef986-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ef986-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ef986-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ef986-117">-Name</span></span>
<span data-ttu-id="ef986-118">A szabály neve</span><span class="sxs-lookup"><span data-stu-id="ef986-118">Name of the rule</span></span>

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

### <span data-ttu-id="ef986-119">-Order (rendelés)</span><span class="sxs-lookup"><span data-stu-id="ef986-119">-Order</span></span>
<span data-ttu-id="ef986-120">A szabály sorrendje</span><span class="sxs-lookup"><span data-stu-id="ef986-120">Order of the rule</span></span>

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

### <span data-ttu-id="ef986-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef986-121">CommonParameters</span></span>
<span data-ttu-id="ef986-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ef986-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef986-123">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ef986-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef986-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ef986-124">INPUTS</span></span>

### <span data-ttu-id="ef986-125">Nincs</span><span class="sxs-lookup"><span data-stu-id="ef986-125">None</span></span>

## <span data-ttu-id="ef986-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ef986-126">OUTPUTS</span></span>

### <span data-ttu-id="ef986-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRule</span><span class="sxs-lookup"><span data-stu-id="ef986-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRule</span></span>

## <span data-ttu-id="ef986-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ef986-128">NOTES</span></span>

## <span data-ttu-id="ef986-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ef986-129">RELATED LINKS</span></span>
