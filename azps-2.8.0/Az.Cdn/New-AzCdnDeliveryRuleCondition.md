---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdndeliveryrulecondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleCondition.md
ms.openlocfilehash: 830b561a3d46e23f083d77dcac627b28f7dbb94e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667582"
---
# <span data-ttu-id="ae7c5-101">New-AzCdnDeliveryRuleCondition</span><span class="sxs-lookup"><span data-stu-id="ae7c5-101">New-AzCdnDeliveryRuleCondition</span></span>

## <span data-ttu-id="ae7c5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ae7c5-102">SYNOPSIS</span></span>
<span data-ttu-id="ae7c5-103">Kézbesítési szabály feltételét hozza létre.</span><span class="sxs-lookup"><span data-stu-id="ae7c5-103">Creates a delivery rule condition.</span></span>

## <span data-ttu-id="ae7c5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ae7c5-104">SYNTAX</span></span>

```
New-AzCdnDeliveryRuleCondition -MatchVariable <String> -Operator <String> -MatchValue <String[]>
 [-Transform <String>] [-NegateCondition] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ae7c5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ae7c5-105">DESCRIPTION</span></span>
<span data-ttu-id="ae7c5-106">A **New-AzCdnDeliveryRule** parancsmag szállítási szabályt hoz létre a CDN-végpontok létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="ae7c5-106">The **New-AzCdnDeliveryRule** cmdlet creates a delivery rule for CDN endpoint creation.</span></span>

## <span data-ttu-id="ae7c5-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ae7c5-107">EXAMPLES</span></span>

### <span data-ttu-id="ae7c5-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ae7c5-108">Example 1</span></span>
```powershell
PS C:\> New-AzCdnDeliveryRuleCondition -MatchVariable UrlPath -Operator Equal -MatchValue "abc"

MatchVariable   : UrlPath
Operator        : Equal
Selector        :
MatchValue      : {abc}
NegateCondition : False
Transfroms      :
```

<span data-ttu-id="ae7c5-109">Egyszerű feltételt hozhat létre.</span><span class="sxs-lookup"><span data-stu-id="ae7c5-109">Create a simple condition.</span></span>

## <span data-ttu-id="ae7c5-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ae7c5-110">PARAMETERS</span></span>

### <span data-ttu-id="ae7c5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae7c5-111">-DefaultProfile</span></span>
<span data-ttu-id="ae7c5-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ae7c5-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae7c5-113">-MatchValue</span><span class="sxs-lookup"><span data-stu-id="ae7c5-113">-MatchValue</span></span>
<span data-ttu-id="ae7c5-114">A lehetséges egyezési értékek listája.</span><span class="sxs-lookup"><span data-stu-id="ae7c5-114">List of possible match values.</span></span>

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

### <span data-ttu-id="ae7c5-115">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="ae7c5-115">-MatchVariable</span></span>
<span data-ttu-id="ae7c5-116">A feltétel változójának egyeztetése.</span><span class="sxs-lookup"><span data-stu-id="ae7c5-116">Match variable of the condition.</span></span>

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

### <span data-ttu-id="ae7c5-117">-NegateCondition</span><span class="sxs-lookup"><span data-stu-id="ae7c5-117">-NegateCondition</span></span>
<span data-ttu-id="ae7c5-118">Ez a cikk azt ismerteti, hogy a feltétel eredményét nem kell-e áthidalni.</span><span class="sxs-lookup"><span data-stu-id="ae7c5-118">Describes if the result of this condition should be negated.</span></span>

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

### <span data-ttu-id="ae7c5-119">-Operátor</span><span class="sxs-lookup"><span data-stu-id="ae7c5-119">-Operator</span></span>
<span data-ttu-id="ae7c5-120">A megfelelő operátor ismertetése</span><span class="sxs-lookup"><span data-stu-id="ae7c5-120">Describes operator to be matched</span></span>

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

### <span data-ttu-id="ae7c5-121">-Transform</span><span class="sxs-lookup"><span data-stu-id="ae7c5-121">-Transform</span></span>
<span data-ttu-id="ae7c5-122">Átalakítás alkalmazása a megfeleltetés előtt.</span><span class="sxs-lookup"><span data-stu-id="ae7c5-122">Transform to apply before matching.</span></span>
<span data-ttu-id="ae7c5-123">A lehetséges értékek kis-és nagybetűk</span><span class="sxs-lookup"><span data-stu-id="ae7c5-123">Possible values are Lowercase and Uppercase</span></span>

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

### <span data-ttu-id="ae7c5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae7c5-124">CommonParameters</span></span>
<span data-ttu-id="ae7c5-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ae7c5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae7c5-126">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ae7c5-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae7c5-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ae7c5-127">INPUTS</span></span>

### <span data-ttu-id="ae7c5-128">Nincs</span><span class="sxs-lookup"><span data-stu-id="ae7c5-128">None</span></span>

## <span data-ttu-id="ae7c5-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ae7c5-129">OUTPUTS</span></span>

### <span data-ttu-id="ae7c5-130">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleCondition</span><span class="sxs-lookup"><span data-stu-id="ae7c5-130">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleCondition</span></span>

## <span data-ttu-id="ae7c5-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ae7c5-131">NOTES</span></span>

## <span data-ttu-id="ae7c5-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ae7c5-132">RELATED LINKS</span></span>
