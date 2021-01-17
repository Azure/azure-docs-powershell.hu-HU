---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafmatchconditionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafMatchConditionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafMatchConditionObject.md
ms.openlocfilehash: 0340cbf8c71b0ab117f1ff967ec7c3bb3e32b8f9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98332273"
---
# <span data-ttu-id="f81fc-101">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="f81fc-101">New-AzFrontDoorWafMatchConditionObject</span></span>

## <span data-ttu-id="f81fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f81fc-102">SYNOPSIS</span></span>
<span data-ttu-id="f81fc-103">MatchCondition objektum létrehozása a WAF-házirendek létrehozásához</span><span class="sxs-lookup"><span data-stu-id="f81fc-103">Create MatchCondition Object for WAF policy creation</span></span>

## <span data-ttu-id="f81fc-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f81fc-104">SYNTAX</span></span>

```
New-AzFrontDoorWafMatchConditionObject -MatchVariable <String> -OperatorProperty <String>
 [-MatchValue <String[]>] [-Selector <String>] [-NegateCondition <Boolean>] [-Transform <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f81fc-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f81fc-105">DESCRIPTION</span></span>
<span data-ttu-id="f81fc-106">MatchCondition objektum létrehozása a WAF-házirendek létrehozásához</span><span class="sxs-lookup"><span data-stu-id="f81fc-106">Create MatchCondition Object for WAF policy creation</span></span>

## <span data-ttu-id="f81fc-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f81fc-107">EXAMPLES</span></span>

### <span data-ttu-id="f81fc-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="f81fc-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorWafMatchConditionObject -MatchVariable RequestHeader -OperatorProperty Contains -Selector "User-Agent" -MatchValue "Windows"


MatchVariable OperatorProperty MatchValue Selector   NegateCondition Transform
------------- ---------------- ---------- --------   --------------- ---------
RequestHeader Contains         {Windows}  User-Agent           False
```

### <span data-ttu-id="f81fc-109">2. példa</span><span class="sxs-lookup"><span data-stu-id="f81fc-109">Example 2</span></span>
```powershell
PS C:\> New-AzFrontDoorWafMatchConditionObject -MatchVariable RequestHeader -OperatorProperty Contains -Selector "User-Agent" -MatchValue "WINDOWS" -Transform Uppercase


MatchVariable OperatorProperty MatchValue Selector   NegateCondition Transform
------------- ---------------- ---------- --------   --------------- ---------
RequestHeader Contains         {WINDOWS}  User-Agent           False {Uppercase}
```

<span data-ttu-id="f81fc-110">MatchCondition objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="f81fc-110">Create a MatchCondition object</span></span>

## <span data-ttu-id="f81fc-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f81fc-111">PARAMETERS</span></span>

### <span data-ttu-id="f81fc-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f81fc-112">-DefaultProfile</span></span>
<span data-ttu-id="f81fc-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f81fc-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f81fc-114">-MatchValue</span><span class="sxs-lookup"><span data-stu-id="f81fc-114">-MatchValue</span></span>
<span data-ttu-id="f81fc-115">Érték egyeztetése</span><span class="sxs-lookup"><span data-stu-id="f81fc-115">Match value.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f81fc-116">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="f81fc-116">-MatchVariable</span></span>
<span data-ttu-id="f81fc-117">Változó egyeztetése</span><span class="sxs-lookup"><span data-stu-id="f81fc-117">Match Variable.</span></span>
<span data-ttu-id="f81fc-118">Lehetséges értékek: 'RemoteAddr', 'RequestMethod', 'QueryString', 'PostArgs','RequestUri', 'RequestHeader', 'Request SocketAddr', 'SocketAddr'</span><span class="sxs-lookup"><span data-stu-id="f81fc-118">Possible values include: 'RemoteAddr', 'RequestMethod', 'QueryString', 'PostArgs','RequestUri', 'RequestHeader', 'RequestBody', 'SocketAddr'</span></span>

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

### <span data-ttu-id="f81fc-119">-NegateCondition</span><span class="sxs-lookup"><span data-stu-id="f81fc-119">-NegateCondition</span></span>
<span data-ttu-id="f81fc-120">Azt ismerteti, hogy ez egy nem engedélyezett feltétel vagy nem az alapértelmezett érték hamis-e</span><span class="sxs-lookup"><span data-stu-id="f81fc-120">Describes if this is negate condition or not Default value is false</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f81fc-121">-OperatorProperty</span><span class="sxs-lookup"><span data-stu-id="f81fc-121">-OperatorProperty</span></span>
<span data-ttu-id="f81fc-122">Az egyező operátort ismerteti.</span><span class="sxs-lookup"><span data-stu-id="f81fc-122">Describes operator to be matched.</span></span>
<span data-ttu-id="f81fc-123">Lehetséges értékek: 'Any', 'IPMatch', 'GeoMatch', 'Equal', 'Contains', 'LessThan', 'GreaterThan', 'LessThanOrEqual', 'GreaterThanOrEqual', 'BeginsWith', 'EndsWith', 'RegEx'</span><span class="sxs-lookup"><span data-stu-id="f81fc-123">Possible values include: 'Any', 'IPMatch', 'GeoMatch', 'Equal', 'Contains', 'LessThan', 'GreaterThan', 'LessThanOrEqual', 'GreaterThanOrEqual', 'BeginsWith', 'EndsWith', 'RegEx'</span></span>

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

### <span data-ttu-id="f81fc-124">-Választó</span><span class="sxs-lookup"><span data-stu-id="f81fc-124">-Selector</span></span>
<span data-ttu-id="f81fc-125">A választó neve a RequestHeaderben vagy a RequestGépben, hogy egyeztethető legyen</span><span class="sxs-lookup"><span data-stu-id="f81fc-125">Name of selector in RequestHeader or RequestBody to be matched</span></span>

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

### <span data-ttu-id="f81fc-126">-Átalakítás</span><span class="sxs-lookup"><span data-stu-id="f81fc-126">-Transform</span></span>
<span data-ttu-id="f81fc-127">Átalakítható.</span><span class="sxs-lookup"><span data-stu-id="f81fc-127">Transforms to apply.</span></span> <span data-ttu-id="f81fc-128">Lehetséges értékek: "Kisbetűk", "Nagybetűk", "Trim", "UrlDecode", "UrlEncode", "RemoveNulls".</span><span class="sxs-lookup"><span data-stu-id="f81fc-128">Possible values include: 'Lowercase', 'Uppercase', 'Trim', 'UrlDecode', 'UrlEncode', 'RemoveNulls'.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f81fc-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f81fc-129">CommonParameters</span></span>
<span data-ttu-id="f81fc-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f81fc-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f81fc-131">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f81fc-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f81fc-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f81fc-132">INPUTS</span></span>

### <span data-ttu-id="f81fc-133">Nincs</span><span class="sxs-lookup"><span data-stu-id="f81fc-133">None</span></span>

## <span data-ttu-id="f81fc-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f81fc-134">OUTPUTS</span></span>

### <span data-ttu-id="f81fc-135">Microsoft.Azure.Commands.FrontDoor.Models.PSMatchCondition</span><span class="sxs-lookup"><span data-stu-id="f81fc-135">Microsoft.Azure.Commands.FrontDoor.Models.PSMatchCondition</span></span>

## <span data-ttu-id="f81fc-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f81fc-136">NOTES</span></span>

## <span data-ttu-id="f81fc-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f81fc-137">RELATED LINKS</span></span>

[<span data-ttu-id="f81fc-138">New-AzFrontDoorWafCustomRuleObject</span><span class="sxs-lookup"><span data-stu-id="f81fc-138">New-AzFrontDoorWafCustomRuleObject</span></span>](./New-AzFrontDoorWafCustomRuleObject.md)
