---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdndeliveryrulecondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleCondition.md
ms.openlocfilehash: 7d7d15fdbaac3de1a212c13fb35dee134dde5381
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98358650"
---
# <span data-ttu-id="666e3-101">New-AzCdnDeliveryRuleCondition</span><span class="sxs-lookup"><span data-stu-id="666e3-101">New-AzCdnDeliveryRuleCondition</span></span>

## <span data-ttu-id="666e3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="666e3-102">SYNOPSIS</span></span>
<span data-ttu-id="666e3-103">Kézbesítési szabály feltételét hozza létre.</span><span class="sxs-lookup"><span data-stu-id="666e3-103">Creates a delivery rule condition.</span></span>

## <span data-ttu-id="666e3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="666e3-104">SYNTAX</span></span>

```
New-AzCdnDeliveryRuleCondition -MatchVariable <String> -Operator <String> [-Selector <String>]
 -MatchValue <String[]> [-Transform <String>] [-NegateCondition] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="666e3-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="666e3-105">DESCRIPTION</span></span>
<span data-ttu-id="666e3-106">A **New-AzCdnDeliveryRule** parancsmag létrehoz egy kézbesítési szabályt a CDN-végpontok létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="666e3-106">The **New-AzCdnDeliveryRule** cmdlet creates a delivery rule for CDN endpoint creation.</span></span>

## <span data-ttu-id="666e3-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="666e3-107">EXAMPLES</span></span>

### <span data-ttu-id="666e3-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="666e3-108">Example 1</span></span>
```powershell
PS C:\> New-AzCdnDeliveryRuleCondition -MatchVariable UrlPath -Operator Equal -MatchValue "abc"

MatchVariable   : UrlPath
Operator        : Equal
Selector        :
MatchValue      : {abc}
NegateCondition : False
Transfroms      :
```

<span data-ttu-id="666e3-109">Hozzon létre egy egyszerű feltételt.</span><span class="sxs-lookup"><span data-stu-id="666e3-109">Create a simple condition.</span></span>

## <span data-ttu-id="666e3-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="666e3-110">PARAMETERS</span></span>

### <span data-ttu-id="666e3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="666e3-111">-DefaultProfile</span></span>
<span data-ttu-id="666e3-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="666e3-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="666e3-113">-MatchValue</span><span class="sxs-lookup"><span data-stu-id="666e3-113">-MatchValue</span></span>
<span data-ttu-id="666e3-114">Az egyezések lehetséges értékeinek listája.</span><span class="sxs-lookup"><span data-stu-id="666e3-114">List of possible match values.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="666e3-115">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="666e3-115">-MatchVariable</span></span>
<span data-ttu-id="666e3-116">A feltétel változója.</span><span class="sxs-lookup"><span data-stu-id="666e3-116">Match variable of the condition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="666e3-117">-NegateCondition</span><span class="sxs-lookup"><span data-stu-id="666e3-117">-NegateCondition</span></span>
<span data-ttu-id="666e3-118">Azt ismerteti, hogy a feltétel eredményét negatáltként kell-e eredményül írni.</span><span class="sxs-lookup"><span data-stu-id="666e3-118">Describes if the result of this condition should be negated.</span></span>

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

### <span data-ttu-id="666e3-119">-Operátor</span><span class="sxs-lookup"><span data-stu-id="666e3-119">-Operator</span></span>
<span data-ttu-id="666e3-120">Az egyező operátort írja le.</span><span class="sxs-lookup"><span data-stu-id="666e3-120">Describes operator to be matched</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="666e3-121">-Választó</span><span class="sxs-lookup"><span data-stu-id="666e3-121">-Selector</span></span>
<span data-ttu-id="666e3-122">Az egyezni kívánt választó neve</span><span class="sxs-lookup"><span data-stu-id="666e3-122">Name of Selector to be matched</span></span>

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

### <span data-ttu-id="666e3-123">-Átalakítás</span><span class="sxs-lookup"><span data-stu-id="666e3-123">-Transform</span></span>
<span data-ttu-id="666e3-124">Átalakítás az alkalmazáshoz az egyezés előtt.</span><span class="sxs-lookup"><span data-stu-id="666e3-124">Transform to apply before matching.</span></span>
<span data-ttu-id="666e3-125">Lehetséges értékek: Kis- és Nagybetűk</span><span class="sxs-lookup"><span data-stu-id="666e3-125">Possible values are Lowercase and Uppercase</span></span>

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

### <span data-ttu-id="666e3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="666e3-126">CommonParameters</span></span>
<span data-ttu-id="666e3-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="666e3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="666e3-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="666e3-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="666e3-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="666e3-129">INPUTS</span></span>

### <span data-ttu-id="666e3-130">Nincs</span><span class="sxs-lookup"><span data-stu-id="666e3-130">None</span></span>

## <span data-ttu-id="666e3-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="666e3-131">OUTPUTS</span></span>

### <span data-ttu-id="666e3-132">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDRuleCondition</span><span class="sxs-lookup"><span data-stu-id="666e3-132">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleCondition</span></span>

## <span data-ttu-id="666e3-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="666e3-133">NOTES</span></span>

## <span data-ttu-id="666e3-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="666e3-134">RELATED LINKS</span></span>
