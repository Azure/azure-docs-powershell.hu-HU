---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoormatchconditionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorMatchConditionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorMatchConditionObject.md
ms.openlocfilehash: ed711160bf761fe7b28f02a94d1ab4ffa6fdb59f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836137"
---
# <span data-ttu-id="62e6f-101">New-AzFrontDoorMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="62e6f-101">New-AzFrontDoorMatchConditionObject</span></span>

## <span data-ttu-id="62e6f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="62e6f-102">SYNOPSIS</span></span>
<span data-ttu-id="62e6f-103">MatchCondition objektum létrehozása a WAF házirendek létrehozásához</span><span class="sxs-lookup"><span data-stu-id="62e6f-103">Create MatchCondition Object for WAF policy creation</span></span>

## <span data-ttu-id="62e6f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="62e6f-104">SYNTAX</span></span>

```
New-AzFrontDoorMatchConditionObject -MatchVariable <PSMatchVariable> -OperatorProperty <PSOperatorProperty>
 [-MatchValue <String[]>] [-Selector <String>] [-NegateCondition <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="62e6f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="62e6f-105">DESCRIPTION</span></span>
<span data-ttu-id="62e6f-106">MatchCondition objektum létrehozása a WAF házirendek létrehozásához</span><span class="sxs-lookup"><span data-stu-id="62e6f-106">Create MatchCondition Object for WAF policy creation</span></span>

## <span data-ttu-id="62e6f-107">Példák</span><span class="sxs-lookup"><span data-stu-id="62e6f-107">EXAMPLES</span></span>

### <span data-ttu-id="62e6f-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="62e6f-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorMatchConditionObject -MatchVariable RequestHeader -OperatorProperty Contains -Selector "User-Agent" -MatchValue "Windows"


MatchVariable OperatorProperty MatchValue Selector   NegateCondition
------------- ---------------- ---------- --------   ---------------
RequestHeader         Contains {Windows}  User-Agent           False
```

<span data-ttu-id="62e6f-109">MatchCondition objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="62e6f-109">Create a MatchCondition object</span></span>

## <span data-ttu-id="62e6f-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="62e6f-110">PARAMETERS</span></span>

### <span data-ttu-id="62e6f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62e6f-111">-DefaultProfile</span></span>
<span data-ttu-id="62e6f-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="62e6f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62e6f-113">-MatchValue</span><span class="sxs-lookup"><span data-stu-id="62e6f-113">-MatchValue</span></span>
<span data-ttu-id="62e6f-114">Az érték egyeztetése</span><span class="sxs-lookup"><span data-stu-id="62e6f-114">Match value.</span></span>

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

### <span data-ttu-id="62e6f-115">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="62e6f-115">-MatchVariable</span></span>
<span data-ttu-id="62e6f-116">Egyezés változó</span><span class="sxs-lookup"><span data-stu-id="62e6f-116">Match Variable.</span></span>
<span data-ttu-id="62e6f-117">A lehetséges értékek a következők: "RemoteAddr", "RequestMethod"; "QueryString"; "PostArgs"; "RequestUri"; "RequestHeader"; "RequestBody"</span><span class="sxs-lookup"><span data-stu-id="62e6f-117">Possible values include: 'RemoteAddr', 'RequestMethod', 'QueryString', 'PostArgs','RequestUri', 'RequestHeader', 'RequestBody'</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSMatchVariable
Parameter Sets: (All)
Aliases:
Accepted values: RemoteAddr, RequestMethod, QueryString, PostArgs, RequestUri, RequestHeader, RequestBody

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62e6f-118">-NegateCondition</span><span class="sxs-lookup"><span data-stu-id="62e6f-118">-NegateCondition</span></span>
<span data-ttu-id="62e6f-119">Ez a cikk azt ismerteti, hogy a hiba nem azonos-e, vagy nem az alapértelmezett érték hamis</span><span class="sxs-lookup"><span data-stu-id="62e6f-119">Describes if this is negate condition or not Default value is false</span></span>

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

### <span data-ttu-id="62e6f-120">-OperatorProperty</span><span class="sxs-lookup"><span data-stu-id="62e6f-120">-OperatorProperty</span></span>
<span data-ttu-id="62e6f-121">A megfelelő operátort ismerteti.</span><span class="sxs-lookup"><span data-stu-id="62e6f-121">Describes operator to be matched.</span></span>
<span data-ttu-id="62e6f-122">Lehetséges értékek: "any", "IPMatch", "GeoMatch", "egyenlő", "tartalmaz", "LessThan", "GreaterThan"; "LessThanOrEqual"; "GreaterThanOrEqual"; "BeginsWith"; "EndsWith" "</span><span class="sxs-lookup"><span data-stu-id="62e6f-122">Possible values include: 'Any', 'IPMatch', 'GeoMatch', 'Equal', 'Contains', 'LessThan', 'GreaterThan', 'LessThanOrEqual', 'GreaterThanOrEqual', 'BeginsWith', 'EndsWith''</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSOperatorProperty
Parameter Sets: (All)
Aliases:
Accepted values: Any, IPMatch, GeoMatch, Equal, Contains, LessThan, GreaterThan, LessThanOrEqual, GreaterThanOrEqual, BeginsWith, EndsWith

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62e6f-123">-Választó</span><span class="sxs-lookup"><span data-stu-id="62e6f-123">-Selector</span></span>
<span data-ttu-id="62e6f-124">A kijelölő neve a RequestHeader-ban vagy a RequestBody egyeztetve</span><span class="sxs-lookup"><span data-stu-id="62e6f-124">Name of selector in RequestHeader or RequestBody to be matched</span></span>

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

### <span data-ttu-id="62e6f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62e6f-125">CommonParameters</span></span>
<span data-ttu-id="62e6f-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="62e6f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62e6f-127">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="62e6f-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62e6f-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="62e6f-128">INPUTS</span></span>

### <span data-ttu-id="62e6f-129">Nincs</span><span class="sxs-lookup"><span data-stu-id="62e6f-129">None</span></span>

## <span data-ttu-id="62e6f-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="62e6f-130">OUTPUTS</span></span>

### <span data-ttu-id="62e6f-131">Microsoft. Azure. Command. FrontDoor. models. PSMatchCondition</span><span class="sxs-lookup"><span data-stu-id="62e6f-131">Microsoft.Azure.Commands.FrontDoor.Models.PSMatchCondition</span></span>

## <span data-ttu-id="62e6f-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="62e6f-132">NOTES</span></span>

## <span data-ttu-id="62e6f-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="62e6f-133">RELATED LINKS</span></span>

[<span data-ttu-id="62e6f-134">Új – AzFrontDoorCustomRuleObject</span><span class="sxs-lookup"><span data-stu-id="62e6f-134">New-AzFrontDoorCustomRuleObject</span></span>](./New-AzFrontDoorCustomRuleObject.md)
