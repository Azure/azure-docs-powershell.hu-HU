---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafmatchconditionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafMatchConditionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafMatchConditionObject.md
ms.openlocfilehash: 0340cbf8c71b0ab117f1ff967ec7c3bb3e32b8f9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845289"
---
# <span data-ttu-id="fc559-101">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="fc559-101">New-AzFrontDoorWafMatchConditionObject</span></span>

## <span data-ttu-id="fc559-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fc559-102">SYNOPSIS</span></span>
<span data-ttu-id="fc559-103">MatchCondition objektum létrehozása a WAF házirendek létrehozásához</span><span class="sxs-lookup"><span data-stu-id="fc559-103">Create MatchCondition Object for WAF policy creation</span></span>

## <span data-ttu-id="fc559-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fc559-104">SYNTAX</span></span>

```
New-AzFrontDoorWafMatchConditionObject -MatchVariable <String> -OperatorProperty <String>
 [-MatchValue <String[]>] [-Selector <String>] [-NegateCondition <Boolean>] [-Transform <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fc559-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="fc559-105">DESCRIPTION</span></span>
<span data-ttu-id="fc559-106">MatchCondition objektum létrehozása a WAF házirendek létrehozásához</span><span class="sxs-lookup"><span data-stu-id="fc559-106">Create MatchCondition Object for WAF policy creation</span></span>

## <span data-ttu-id="fc559-107">Példák</span><span class="sxs-lookup"><span data-stu-id="fc559-107">EXAMPLES</span></span>

### <span data-ttu-id="fc559-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="fc559-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorWafMatchConditionObject -MatchVariable RequestHeader -OperatorProperty Contains -Selector "User-Agent" -MatchValue "Windows"


MatchVariable OperatorProperty MatchValue Selector   NegateCondition Transform
------------- ---------------- ---------- --------   --------------- ---------
RequestHeader Contains         {Windows}  User-Agent           False
```

### <span data-ttu-id="fc559-109">2. példa</span><span class="sxs-lookup"><span data-stu-id="fc559-109">Example 2</span></span>
```powershell
PS C:\> New-AzFrontDoorWafMatchConditionObject -MatchVariable RequestHeader -OperatorProperty Contains -Selector "User-Agent" -MatchValue "WINDOWS" -Transform Uppercase


MatchVariable OperatorProperty MatchValue Selector   NegateCondition Transform
------------- ---------------- ---------- --------   --------------- ---------
RequestHeader Contains         {WINDOWS}  User-Agent           False {Uppercase}
```

<span data-ttu-id="fc559-110">MatchCondition objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="fc559-110">Create a MatchCondition object</span></span>

## <span data-ttu-id="fc559-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fc559-111">PARAMETERS</span></span>

### <span data-ttu-id="fc559-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc559-112">-DefaultProfile</span></span>
<span data-ttu-id="fc559-113">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fc559-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fc559-114">-MatchValue</span><span class="sxs-lookup"><span data-stu-id="fc559-114">-MatchValue</span></span>
<span data-ttu-id="fc559-115">Az érték egyeztetése</span><span class="sxs-lookup"><span data-stu-id="fc559-115">Match value.</span></span>

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

### <span data-ttu-id="fc559-116">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="fc559-116">-MatchVariable</span></span>
<span data-ttu-id="fc559-117">Egyezés változó</span><span class="sxs-lookup"><span data-stu-id="fc559-117">Match Variable.</span></span>
<span data-ttu-id="fc559-118">A lehetséges értékek a következők: "RemoteAddr", "RequestMethod"; "QueryString"; "PostArgs"; "RequestUri"; "RequestHeader"; "RequestBody"; "SocketAddr"</span><span class="sxs-lookup"><span data-stu-id="fc559-118">Possible values include: 'RemoteAddr', 'RequestMethod', 'QueryString', 'PostArgs','RequestUri', 'RequestHeader', 'RequestBody', 'SocketAddr'</span></span>

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

### <span data-ttu-id="fc559-119">-NegateCondition</span><span class="sxs-lookup"><span data-stu-id="fc559-119">-NegateCondition</span></span>
<span data-ttu-id="fc559-120">Ez a cikk azt ismerteti, hogy a hiba nem azonos-e, vagy nem az alapértelmezett érték hamis</span><span class="sxs-lookup"><span data-stu-id="fc559-120">Describes if this is negate condition or not Default value is false</span></span>

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

### <span data-ttu-id="fc559-121">-OperatorProperty</span><span class="sxs-lookup"><span data-stu-id="fc559-121">-OperatorProperty</span></span>
<span data-ttu-id="fc559-122">A megfelelő operátort ismerteti.</span><span class="sxs-lookup"><span data-stu-id="fc559-122">Describes operator to be matched.</span></span>
<span data-ttu-id="fc559-123">Lehetséges értékek: "any", "IPMatch", "GeoMatch", "egyenlő", "benne", "LessThan", "GreaterThan"; "LessThanOrEqual"; "GreaterThanOrEqual"; "BeginsWith"; "EndsWith"</span><span class="sxs-lookup"><span data-stu-id="fc559-123">Possible values include: 'Any', 'IPMatch', 'GeoMatch', 'Equal', 'Contains', 'LessThan', 'GreaterThan', 'LessThanOrEqual', 'GreaterThanOrEqual', 'BeginsWith', 'EndsWith', 'RegEx'</span></span>

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

### <span data-ttu-id="fc559-124">-Választó</span><span class="sxs-lookup"><span data-stu-id="fc559-124">-Selector</span></span>
<span data-ttu-id="fc559-125">A kijelölő neve a RequestHeader-ban vagy a RequestBody egyeztetve</span><span class="sxs-lookup"><span data-stu-id="fc559-125">Name of selector in RequestHeader or RequestBody to be matched</span></span>

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

### <span data-ttu-id="fc559-126">-Transform</span><span class="sxs-lookup"><span data-stu-id="fc559-126">-Transform</span></span>
<span data-ttu-id="fc559-127">Átalakítja az alkalmazásra.</span><span class="sxs-lookup"><span data-stu-id="fc559-127">Transforms to apply.</span></span> <span data-ttu-id="fc559-128">A lehetséges értékek a következők: "kisbetűs", "nagybetűs", "Trim", "UrlDecode", "UrlEncode", "RemoveNulls".</span><span class="sxs-lookup"><span data-stu-id="fc559-128">Possible values include: 'Lowercase', 'Uppercase', 'Trim', 'UrlDecode', 'UrlEncode', 'RemoveNulls'.</span></span>

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

### <span data-ttu-id="fc559-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc559-129">CommonParameters</span></span>
<span data-ttu-id="fc559-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fc559-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc559-131">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="fc559-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc559-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fc559-132">INPUTS</span></span>

### <span data-ttu-id="fc559-133">Nincs</span><span class="sxs-lookup"><span data-stu-id="fc559-133">None</span></span>

## <span data-ttu-id="fc559-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fc559-134">OUTPUTS</span></span>

### <span data-ttu-id="fc559-135">Microsoft. Azure. Command. FrontDoor. models. PSMatchCondition</span><span class="sxs-lookup"><span data-stu-id="fc559-135">Microsoft.Azure.Commands.FrontDoor.Models.PSMatchCondition</span></span>

## <span data-ttu-id="fc559-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fc559-136">NOTES</span></span>

## <span data-ttu-id="fc559-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fc559-137">RELATED LINKS</span></span>

[<span data-ttu-id="fc559-138">Új – AzFrontDoorWafCustomRuleObject</span><span class="sxs-lookup"><span data-stu-id="fc559-138">New-AzFrontDoorWafCustomRuleObject</span></span>](./New-AzFrontDoorWafCustomRuleObject.md)
