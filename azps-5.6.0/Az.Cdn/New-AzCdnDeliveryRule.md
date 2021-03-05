---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/powershell/module/az.cdn/new-azcdndeliveryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRule.md
ms.openlocfilehash: a2143e0363d08a06ac72ee7c5207ef93f5c3a509
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001830"
---
# <span data-ttu-id="a1d06-101">New-AzCdnDeliveryRule</span><span class="sxs-lookup"><span data-stu-id="a1d06-101">New-AzCdnDeliveryRule</span></span>

## <span data-ttu-id="a1d06-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a1d06-102">SYNOPSIS</span></span>
<span data-ttu-id="a1d06-103">Kézbesítési szabályt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="a1d06-103">Creates a delivery rule.</span></span>

## <span data-ttu-id="a1d06-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a1d06-104">SYNTAX</span></span>

```
New-AzCdnDeliveryRule [-Name <String>] -Order <Int32> [-Condition <PSDeliveryRuleCondition[]>]
 -Action <PSDeliveryRuleAction[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a1d06-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a1d06-105">DESCRIPTION</span></span>
<span data-ttu-id="a1d06-106">A **New-AzCdnDeliveryRule** parancsmag létrehoz egy kézbesítési szabályt a CDN-végpontok létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="a1d06-106">The **New-AzCdnDeliveryRule** cmdlet creates a delivery rule for CDN endpoint creation.</span></span>

## <span data-ttu-id="a1d06-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a1d06-107">EXAMPLES</span></span>

### <span data-ttu-id="a1d06-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="a1d06-108">Example 1</span></span>
```powershell
PS C:\> New-AzCdnDeliveryRule -Name "rule1" -Order 1 -Condition $cond1 -Action $action1

Name  Order Actions           Conditions
----  ----- -------           ----------
rule1     1 {Accept-Encoding} {Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleCondition}
```

<span data-ttu-id="a1d06-109">Hozzon létre egy egyszerű szabályt.</span><span class="sxs-lookup"><span data-stu-id="a1d06-109">Create a simple rule.</span></span>

## <span data-ttu-id="a1d06-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a1d06-110">PARAMETERS</span></span>

### <span data-ttu-id="a1d06-111">-Művelet</span><span class="sxs-lookup"><span data-stu-id="a1d06-111">-Action</span></span>
<span data-ttu-id="a1d06-112">Olyan műveletek listája, amelyek akkor hajtva végre, ha egy szabály minden feltétele teljesül.</span><span class="sxs-lookup"><span data-stu-id="a1d06-112">A list of actions that are executed when all the conditions of a rule are satisfied.</span></span>

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

### <span data-ttu-id="a1d06-113">-Feltétel</span><span class="sxs-lookup"><span data-stu-id="a1d06-113">-Condition</span></span>
<span data-ttu-id="a1d06-114">A végrehajtandó műveletek feltételeinek listája.</span><span class="sxs-lookup"><span data-stu-id="a1d06-114">A list of conditions that must be matched for the actions to be executed.</span></span>

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

### <span data-ttu-id="a1d06-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1d06-115">-DefaultProfile</span></span>
<span data-ttu-id="a1d06-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a1d06-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a1d06-117">-Name</span><span class="sxs-lookup"><span data-stu-id="a1d06-117">-Name</span></span>
<span data-ttu-id="a1d06-118">A szabály neve</span><span class="sxs-lookup"><span data-stu-id="a1d06-118">Name of the rule</span></span>

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

### <span data-ttu-id="a1d06-119">-Order</span><span class="sxs-lookup"><span data-stu-id="a1d06-119">-Order</span></span>
<span data-ttu-id="a1d06-120">A szabály sorrendje</span><span class="sxs-lookup"><span data-stu-id="a1d06-120">Order of the rule</span></span>

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

### <span data-ttu-id="a1d06-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1d06-121">CommonParameters</span></span>
<span data-ttu-id="a1d06-122">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1d06-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1d06-123">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a1d06-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1d06-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a1d06-124">INPUTS</span></span>

### <span data-ttu-id="a1d06-125">Nincs</span><span class="sxs-lookup"><span data-stu-id="a1d06-125">None</span></span>

## <span data-ttu-id="a1d06-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a1d06-126">OUTPUTS</span></span>

### <span data-ttu-id="a1d06-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDEliveryRule</span><span class="sxs-lookup"><span data-stu-id="a1d06-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRule</span></span>

## <span data-ttu-id="a1d06-128">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a1d06-128">NOTES</span></span>

## <span data-ttu-id="a1d06-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a1d06-129">RELATED LINKS</span></span>
