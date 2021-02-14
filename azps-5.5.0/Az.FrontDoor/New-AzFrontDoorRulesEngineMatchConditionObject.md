---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorrulesenginematchconditionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngineMatchConditionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngineMatchConditionObject.md
ms.openlocfilehash: 991d3233dd484025e699bba455b7d43e86f586e7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100167522"
---
# <span data-ttu-id="3df65-101">New-AzFrontDoorRulesEngineMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="3df65-101">New-AzFrontDoorRulesEngineMatchConditionObject</span></span>

## <span data-ttu-id="3df65-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3df65-102">SYNOPSIS</span></span>
<span data-ttu-id="3df65-103">Hozzon létre egy PSRulesEngineMatchCondition objektumot szabálymotor-szabály létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="3df65-103">Create a PSRulesEngineMatchCondition object for creating a rules engine rule.</span></span>

## <span data-ttu-id="3df65-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="3df65-104">SYNTAX</span></span>

```
New-AzFrontDoorRulesEngineMatchConditionObject -MatchVariable <PSRulesEngineMatchVariable>
 -MatchValue <String[]> [-Selector <String>] [-Operator <PSRulesEngineOperator>] [-NegateCondition <Boolean>]
 [-Transform <PSTransform[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3df65-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="3df65-105">DESCRIPTION</span></span>
<span data-ttu-id="3df65-106">Hozzon létre egy PSRulesEngineMatchCondition objektumot szabálymotor-szabály létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="3df65-106">Create a PSRulesEngineMatchCondition object for creating a rules engine rule.</span></span>

## <span data-ttu-id="3df65-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="3df65-107">EXAMPLES</span></span>

### <span data-ttu-id="3df65-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="3df65-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorRulesEngineMatchConditionObject -MatchVariable RequestHeader -Operator Equal -MatchValue allowoverride -Transform "LowerCase", "UpperCase"-Selector Rules-Engine-Route-Forward -NegateCondition $false

RulesEngineMatchVariable : RequestHeader
RulesEngineMatchValue    : {allowoverride}
Selector                 : Rules-Engine-Route-Forward
RulesEngineOperator      : Equal
NegateCondition          : False
Transform                : {Lowercase, Uppercase}
```

<span data-ttu-id="3df65-109">Greate a new PSRulesEngineMatchCondition object.</span><span class="sxs-lookup"><span data-stu-id="3df65-109">Greate a new PSRulesEngineMatchCondition object.</span></span>

## <span data-ttu-id="3df65-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3df65-110">PARAMETERS</span></span>

### <span data-ttu-id="3df65-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3df65-111">-DefaultProfile</span></span>
<span data-ttu-id="3df65-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3df65-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3df65-113">-MatchValue</span><span class="sxs-lookup"><span data-stu-id="3df65-113">-MatchValue</span></span>
<span data-ttu-id="3df65-114">Egyezést ad meg az egyező értékeknek.</span><span class="sxs-lookup"><span data-stu-id="3df65-114">Match values to match against.</span></span>
<span data-ttu-id="3df65-115">Az operátor az OR szemantikai operátorral megadott értékeket fogja alkalmazni.</span><span class="sxs-lookup"><span data-stu-id="3df65-115">The operator will apply to each value in here with OR semantics.</span></span>
<span data-ttu-id="3df65-116">Ha bármelyikük megfelel a megadott operátorral megadott változónak, a feltétel egyezésnek minősül.</span><span class="sxs-lookup"><span data-stu-id="3df65-116">If any of them match the variable with the given operator this match condition is considered a match.</span></span>

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

### <span data-ttu-id="3df65-117">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="3df65-117">-MatchVariable</span></span>
<span data-ttu-id="3df65-118">Változó egyeztetése</span><span class="sxs-lookup"><span data-stu-id="3df65-118">Match Variable.</span></span>
<span data-ttu-id="3df65-119">Lehetséges értékek: IsMobile, RemoteAddr, RequestMethod, QueryString, PostArg, RequestUri, RequestPath, RequestFileName, RequestfilenameExtension, RequestHeader, RequestFile, RequestScheme</span><span class="sxs-lookup"><span data-stu-id="3df65-119">Possible values are IsMobile, RemoteAddr, RequestMethod, QueryString, PostArg, RequestUri, RequestPath, RequestFileName, RequestfilenameExtension, RequestHeader, RequestBody, RequestScheme</span></span>

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

### <span data-ttu-id="3df65-120">-NegateCondition</span><span class="sxs-lookup"><span data-stu-id="3df65-120">-NegateCondition</span></span>
<span data-ttu-id="3df65-121">Azt ismerteti, hogy ez nem egy feltétel-e</span><span class="sxs-lookup"><span data-stu-id="3df65-121">Describes if this is negate condition or not</span></span>

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

### <span data-ttu-id="3df65-122">-Operátor</span><span class="sxs-lookup"><span data-stu-id="3df65-122">-Operator</span></span>
<span data-ttu-id="3df65-123">Az egyezés feltételre alkalmazandó operátort ismerteti.</span><span class="sxs-lookup"><span data-stu-id="3df65-123">Describes operator to apply to the match condition.</span></span>
<span data-ttu-id="3df65-124">Lehetséges értékek: Any, IPMatch, GeoMatch, Equal, Contains, LessThan, GreaterThan, LessThanOrEqual, GreaterThanOrEqual, BeginsWith, EndsWith.</span><span class="sxs-lookup"><span data-stu-id="3df65-124">Possible values are Any, IPMatch, GeoMatch, Equal, Contains, LessThan, GreaterThan, LessThanOrEqual, GreaterThanOrEqual, BeginsWith, EndsWith.</span></span>

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

### <span data-ttu-id="3df65-125">-Választó</span><span class="sxs-lookup"><span data-stu-id="3df65-125">-Selector</span></span>
<span data-ttu-id="3df65-126">A választó neve a RequestHeaderben vagy a RequestGépben, hogy egyeztethető legyen</span><span class="sxs-lookup"><span data-stu-id="3df65-126">Name of selector in RequestHeader or RequestBody to be matched</span></span>

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

### <span data-ttu-id="3df65-127">-Átalakítás</span><span class="sxs-lookup"><span data-stu-id="3df65-127">-Transform</span></span>
<span data-ttu-id="3df65-128">Az egyezés előtt alkalmazott átalakítások listája.</span><span class="sxs-lookup"><span data-stu-id="3df65-128">List of what transforms are applied before matching.</span></span> <span data-ttu-id="3df65-129">Az egyes transzformációk lehetséges értékei: Kisbetűk, Nagybetűk, Trim, UrlDecode, UrlEncode, RemoveNulls.</span><span class="sxs-lookup"><span data-stu-id="3df65-129">Possible individual transform values are Lowercase, Uppercase, Trim, UrlDecode, UrlEncode, RemoveNulls.</span></span>

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

### <span data-ttu-id="3df65-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3df65-130">CommonParameters</span></span>
<span data-ttu-id="3df65-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3df65-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3df65-132">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3df65-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3df65-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3df65-133">INPUTS</span></span>

### <span data-ttu-id="3df65-134">Nincs</span><span class="sxs-lookup"><span data-stu-id="3df65-134">None</span></span>

## <span data-ttu-id="3df65-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3df65-135">OUTPUTS</span></span>

### <span data-ttu-id="3df65-136">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineMatchCondition</span><span class="sxs-lookup"><span data-stu-id="3df65-136">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineMatchCondition</span></span>

## <span data-ttu-id="3df65-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="3df65-137">NOTES</span></span>

## <span data-ttu-id="3df65-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3df65-138">RELATED LINKS</span></span>
