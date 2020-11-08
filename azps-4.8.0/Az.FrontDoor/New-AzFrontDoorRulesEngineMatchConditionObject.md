---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorrulesenginematchconditionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngineMatchConditionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngineMatchConditionObject.md
ms.openlocfilehash: 991d3233dd484025e699bba455b7d43e86f586e7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94017759"
---
# <span data-ttu-id="11d6d-101">New-AzFrontDoorRulesEngineMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="11d6d-101">New-AzFrontDoorRulesEngineMatchConditionObject</span></span>

## <span data-ttu-id="11d6d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="11d6d-102">SYNOPSIS</span></span>
<span data-ttu-id="11d6d-103">PSRulesEngineMatchCondition objektum létrehozása szabály-végrehajtó szabály létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="11d6d-103">Create a PSRulesEngineMatchCondition object for creating a rules engine rule.</span></span>

## <span data-ttu-id="11d6d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="11d6d-104">SYNTAX</span></span>

```
New-AzFrontDoorRulesEngineMatchConditionObject -MatchVariable <PSRulesEngineMatchVariable>
 -MatchValue <String[]> [-Selector <String>] [-Operator <PSRulesEngineOperator>] [-NegateCondition <Boolean>]
 [-Transform <PSTransform[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="11d6d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="11d6d-105">DESCRIPTION</span></span>
<span data-ttu-id="11d6d-106">PSRulesEngineMatchCondition objektum létrehozása szabály-végrehajtó szabály létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="11d6d-106">Create a PSRulesEngineMatchCondition object for creating a rules engine rule.</span></span>

## <span data-ttu-id="11d6d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="11d6d-107">EXAMPLES</span></span>

### <span data-ttu-id="11d6d-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="11d6d-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorRulesEngineMatchConditionObject -MatchVariable RequestHeader -Operator Equal -MatchValue allowoverride -Transform "LowerCase", "UpperCase"-Selector Rules-Engine-Route-Forward -NegateCondition $false

RulesEngineMatchVariable : RequestHeader
RulesEngineMatchValue    : {allowoverride}
Selector                 : Rules-Engine-Route-Forward
RulesEngineOperator      : Equal
NegateCondition          : False
Transform                : {Lowercase, Uppercase}
```

<span data-ttu-id="11d6d-109">Remekül új PSRulesEngineMatchCondition objektumot.</span><span class="sxs-lookup"><span data-stu-id="11d6d-109">Greate a new PSRulesEngineMatchCondition object.</span></span>

## <span data-ttu-id="11d6d-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="11d6d-110">PARAMETERS</span></span>

### <span data-ttu-id="11d6d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11d6d-111">-DefaultProfile</span></span>
<span data-ttu-id="11d6d-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="11d6d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11d6d-113">-MatchValue</span><span class="sxs-lookup"><span data-stu-id="11d6d-113">-MatchValue</span></span>
<span data-ttu-id="11d6d-114">A megfelelő értékek egyeztetése.</span><span class="sxs-lookup"><span data-stu-id="11d6d-114">Match values to match against.</span></span>
<span data-ttu-id="11d6d-115">Az operátor minden ide-vagy szemantikai értékre érvényes lesz.</span><span class="sxs-lookup"><span data-stu-id="11d6d-115">The operator will apply to each value in here with OR semantics.</span></span>
<span data-ttu-id="11d6d-116">Ha bármelyikük egyezik azzal a változóval, amely a megadott operátorral egyezik, akkor ez az egyeztetési feltétel egyezésnek számít.</span><span class="sxs-lookup"><span data-stu-id="11d6d-116">If any of them match the variable with the given operator this match condition is considered a match.</span></span>

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

### <span data-ttu-id="11d6d-117">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="11d6d-117">-MatchVariable</span></span>
<span data-ttu-id="11d6d-118">Egyezés változó</span><span class="sxs-lookup"><span data-stu-id="11d6d-118">Match Variable.</span></span>
<span data-ttu-id="11d6d-119">Lehetséges értékek IsMobile, RemoteAddr, RequestMethod, QueryString, PostArg, RequestUri, RequestPath, RequestFileName, RequestfilenameExtension, RequestHeader, RequestBody, RequestScheme,,</span><span class="sxs-lookup"><span data-stu-id="11d6d-119">Possible values are IsMobile, RemoteAddr, RequestMethod, QueryString, PostArg, RequestUri, RequestPath, RequestFileName, RequestfilenameExtension, RequestHeader, RequestBody, RequestScheme</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineMatchVariable
Parameter Sets: (All)
Aliases:
Accepted values: IsMobile, RemoteAddr, RequestMethod, QueryString, PostArgs, RequestUri, RequestPath, RequestFilename, RequestFilenameExtension, RequestHeader, RequestBody, RequestScheme

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11d6d-120">-NegateCondition</span><span class="sxs-lookup"><span data-stu-id="11d6d-120">-NegateCondition</span></span>
<span data-ttu-id="11d6d-121">Ez a cikk azt ismerteti, hogy a feltétel nincs-e megtagadva</span><span class="sxs-lookup"><span data-stu-id="11d6d-121">Describes if this is negate condition or not</span></span>

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

### <span data-ttu-id="11d6d-122">-Operátor</span><span class="sxs-lookup"><span data-stu-id="11d6d-122">-Operator</span></span>
<span data-ttu-id="11d6d-123">Ez a cikk bemutatja, hogy az operátor a hol. van feltétellel érvényes.</span><span class="sxs-lookup"><span data-stu-id="11d6d-123">Describes operator to apply to the match condition.</span></span>
<span data-ttu-id="11d6d-124">Lehetséges értékek: any, IPMatch, GeoMatch, egyenlő, tartalmaz, LessThan, GreaterThan, LessThanOrEqual, GreaterThanOrEqual, BeginsWith, EndsWith.</span><span class="sxs-lookup"><span data-stu-id="11d6d-124">Possible values are Any, IPMatch, GeoMatch, Equal, Contains, LessThan, GreaterThan, LessThanOrEqual, GreaterThanOrEqual, BeginsWith, EndsWith.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineOperator
Parameter Sets: (All)
Aliases:
Accepted values: Any, IPMatch, GeoMatch, Equal, Contains, LessThan, GreaterThan, LessThanOrEqual, GreaterThanOrEqual, BeginsWith, EndsWith

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11d6d-125">-Választó</span><span class="sxs-lookup"><span data-stu-id="11d6d-125">-Selector</span></span>
<span data-ttu-id="11d6d-126">A kijelölő neve a RequestHeader-ban vagy a RequestBody egyeztetve</span><span class="sxs-lookup"><span data-stu-id="11d6d-126">Name of selector in RequestHeader or RequestBody to be matched</span></span>

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

### <span data-ttu-id="11d6d-127">-Transform</span><span class="sxs-lookup"><span data-stu-id="11d6d-127">-Transform</span></span>
<span data-ttu-id="11d6d-128">Annak listája, hogy milyen átalakításokat alkalmaz a program a megfeleltetés előtt.</span><span class="sxs-lookup"><span data-stu-id="11d6d-128">List of what transforms are applied before matching.</span></span> <span data-ttu-id="11d6d-129">A lehetséges egyéni átalakítási értékek kisbetűsek, nagybetűs, kivágás, UrlDecode, UrlEncode és RemoveNulls.</span><span class="sxs-lookup"><span data-stu-id="11d6d-129">Possible individual transform values are Lowercase, Uppercase, Trim, UrlDecode, UrlEncode, RemoveNulls.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSTransform[]
Parameter Sets: (All)
Aliases:
Accepted values: Lowercase, Uppercase, Trim, UrlDecode, UrlEncode, RemoveNulls

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11d6d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11d6d-130">CommonParameters</span></span>
<span data-ttu-id="11d6d-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="11d6d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11d6d-132">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="11d6d-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11d6d-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="11d6d-133">INPUTS</span></span>

### <span data-ttu-id="11d6d-134">Nincs</span><span class="sxs-lookup"><span data-stu-id="11d6d-134">None</span></span>

## <span data-ttu-id="11d6d-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="11d6d-135">OUTPUTS</span></span>

### <span data-ttu-id="11d6d-136">Microsoft. Azure. Command. FrontDoor. models. PSRulesEngineMatchCondition</span><span class="sxs-lookup"><span data-stu-id="11d6d-136">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineMatchCondition</span></span>

## <span data-ttu-id="11d6d-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="11d6d-137">NOTES</span></span>

## <span data-ttu-id="11d6d-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="11d6d-138">RELATED LINKS</span></span>
