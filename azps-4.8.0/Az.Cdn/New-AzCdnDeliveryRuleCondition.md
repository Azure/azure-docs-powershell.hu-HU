---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdndeliveryrulecondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleCondition.md
ms.openlocfilehash: 7d7d15fdbaac3de1a212c13fb35dee134dde5381
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181773"
---
# <span data-ttu-id="d6aeb-101">New-AzCdnDeliveryRuleCondition</span><span class="sxs-lookup"><span data-stu-id="d6aeb-101">New-AzCdnDeliveryRuleCondition</span></span>

## <span data-ttu-id="d6aeb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d6aeb-102">SYNOPSIS</span></span>
<span data-ttu-id="d6aeb-103">Kézbesítési szabály feltételét hozza létre.</span><span class="sxs-lookup"><span data-stu-id="d6aeb-103">Creates a delivery rule condition.</span></span>

## <span data-ttu-id="d6aeb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d6aeb-104">SYNTAX</span></span>

```
New-AzCdnDeliveryRuleCondition -MatchVariable <String> -Operator <String> [-Selector <String>]
 -MatchValue <String[]> [-Transform <String>] [-NegateCondition] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d6aeb-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d6aeb-105">DESCRIPTION</span></span>
<span data-ttu-id="d6aeb-106">A **New-AzCdnDeliveryRule** parancsmag szállítási szabályt hoz létre a CDN-végpontok létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="d6aeb-106">The **New-AzCdnDeliveryRule** cmdlet creates a delivery rule for CDN endpoint creation.</span></span>

## <span data-ttu-id="d6aeb-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d6aeb-107">EXAMPLES</span></span>

### <span data-ttu-id="d6aeb-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d6aeb-108">Example 1</span></span>
```powershell
PS C:\> New-AzCdnDeliveryRuleCondition -MatchVariable UrlPath -Operator Equal -MatchValue "abc"

MatchVariable   : UrlPath
Operator        : Equal
Selector        :
MatchValue      : {abc}
NegateCondition : False
Transfroms      :
```

<span data-ttu-id="d6aeb-109">Egyszerű feltételt hozhat létre.</span><span class="sxs-lookup"><span data-stu-id="d6aeb-109">Create a simple condition.</span></span>

## <span data-ttu-id="d6aeb-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d6aeb-110">PARAMETERS</span></span>

### <span data-ttu-id="d6aeb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6aeb-111">-DefaultProfile</span></span>
<span data-ttu-id="d6aeb-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d6aeb-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6aeb-113">-MatchValue</span><span class="sxs-lookup"><span data-stu-id="d6aeb-113">-MatchValue</span></span>
<span data-ttu-id="d6aeb-114">A lehetséges egyezési értékek listája.</span><span class="sxs-lookup"><span data-stu-id="d6aeb-114">List of possible match values.</span></span>

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

### <span data-ttu-id="d6aeb-115">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="d6aeb-115">-MatchVariable</span></span>
<span data-ttu-id="d6aeb-116">A feltétel változójának egyeztetése.</span><span class="sxs-lookup"><span data-stu-id="d6aeb-116">Match variable of the condition.</span></span>

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

### <span data-ttu-id="d6aeb-117">-NegateCondition</span><span class="sxs-lookup"><span data-stu-id="d6aeb-117">-NegateCondition</span></span>
<span data-ttu-id="d6aeb-118">Ez a cikk azt ismerteti, hogy a feltétel eredményét nem kell-e áthidalni.</span><span class="sxs-lookup"><span data-stu-id="d6aeb-118">Describes if the result of this condition should be negated.</span></span>

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

### <span data-ttu-id="d6aeb-119">-Operátor</span><span class="sxs-lookup"><span data-stu-id="d6aeb-119">-Operator</span></span>
<span data-ttu-id="d6aeb-120">A megfelelő operátor ismertetése</span><span class="sxs-lookup"><span data-stu-id="d6aeb-120">Describes operator to be matched</span></span>

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

### <span data-ttu-id="d6aeb-121">-Választó</span><span class="sxs-lookup"><span data-stu-id="d6aeb-121">-Selector</span></span>
<span data-ttu-id="d6aeb-122">Az egyeztetni kívánt választó neve</span><span class="sxs-lookup"><span data-stu-id="d6aeb-122">Name of Selector to be matched</span></span>

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

### <span data-ttu-id="d6aeb-123">-Transform</span><span class="sxs-lookup"><span data-stu-id="d6aeb-123">-Transform</span></span>
<span data-ttu-id="d6aeb-124">Átalakítás alkalmazása a megfeleltetés előtt.</span><span class="sxs-lookup"><span data-stu-id="d6aeb-124">Transform to apply before matching.</span></span>
<span data-ttu-id="d6aeb-125">A lehetséges értékek kis-és nagybetűk</span><span class="sxs-lookup"><span data-stu-id="d6aeb-125">Possible values are Lowercase and Uppercase</span></span>

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

### <span data-ttu-id="d6aeb-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6aeb-126">CommonParameters</span></span>
<span data-ttu-id="d6aeb-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d6aeb-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6aeb-128">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d6aeb-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6aeb-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d6aeb-129">INPUTS</span></span>

### <span data-ttu-id="d6aeb-130">Nincs</span><span class="sxs-lookup"><span data-stu-id="d6aeb-130">None</span></span>

## <span data-ttu-id="d6aeb-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d6aeb-131">OUTPUTS</span></span>

### <span data-ttu-id="d6aeb-132">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleCondition</span><span class="sxs-lookup"><span data-stu-id="d6aeb-132">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleCondition</span></span>

## <span data-ttu-id="d6aeb-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d6aeb-133">NOTES</span></span>

## <span data-ttu-id="d6aeb-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d6aeb-134">RELATED LINKS</span></span>
