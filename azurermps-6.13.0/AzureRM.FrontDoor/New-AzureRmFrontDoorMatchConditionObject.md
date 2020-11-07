---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoormatchconditionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorMatchConditionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorMatchConditionObject.md
ms.openlocfilehash: 70ab8b592c550280f424f9c0a4bfced877942edc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672929"
---
# <span data-ttu-id="560e5-101">New-AzureRmFrontDoorMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="560e5-101">New-AzureRmFrontDoorMatchConditionObject</span></span>

## <span data-ttu-id="560e5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="560e5-102">SYNOPSIS</span></span>
<span data-ttu-id="560e5-103">MatchCondition objektum létrehozása a WAF házirendek létrehozásához</span><span class="sxs-lookup"><span data-stu-id="560e5-103">Create MatchCondition Object for WAF policy creation</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="560e5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="560e5-104">SYNTAX</span></span>

```
New-AzureRmFrontDoorMatchConditionObject -MatchVariable <PSMatchVariable>
 -OperatorProperty <PSOperatorProperty> -MatchValue <String[]> [-Selector <String>]
 [-NegateCondition <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="560e5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="560e5-105">DESCRIPTION</span></span>
<span data-ttu-id="560e5-106">MatchCondition objektum létrehozása a WAF házirendek létrehozásához</span><span class="sxs-lookup"><span data-stu-id="560e5-106">Create MatchCondition Object for WAF policy creation</span></span>

## <span data-ttu-id="560e5-107">Példák</span><span class="sxs-lookup"><span data-stu-id="560e5-107">EXAMPLES</span></span>

### <span data-ttu-id="560e5-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="560e5-108">Example 1</span></span>
```powershell
PS C:\> New-AzureRmFrontDoorMatchConditionObject -MatchVariable RequestHeader -OperatorProperty Contains -Selector "UserAgent" -MatchValue "Windows"


MatchVariable    : RequestHeader
OperatorProperty : Contains
MatchValue       : {Windows}
Selector         : UserAgent
NegateCondition  : False
```

<span data-ttu-id="560e5-109">MatchCondition objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="560e5-109">Create a MatchCondition object</span></span>

## <span data-ttu-id="560e5-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="560e5-110">PARAMETERS</span></span>

### <span data-ttu-id="560e5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="560e5-111">-DefaultProfile</span></span>
<span data-ttu-id="560e5-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="560e5-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="560e5-113">-MatchValue</span><span class="sxs-lookup"><span data-stu-id="560e5-113">-MatchValue</span></span>
<span data-ttu-id="560e5-114">Az érték egyeztetése</span><span class="sxs-lookup"><span data-stu-id="560e5-114">Match value.</span></span>

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

### <span data-ttu-id="560e5-115">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="560e5-115">-MatchVariable</span></span>
<span data-ttu-id="560e5-116">Egyezés változó</span><span class="sxs-lookup"><span data-stu-id="560e5-116">Match Variable.</span></span>
<span data-ttu-id="560e5-117">A lehetséges értékek a következők: "RemoteAddr", "RequestMethod"; "QueryString"; "PostArgs"; "RequestUri"; "RequestHeader"; "RequestBody"</span><span class="sxs-lookup"><span data-stu-id="560e5-117">Possible values include: 'RemoteAddr', 'RequestMethod', 'QueryString', 'PostArgs','RequestUri', 'RequestHeader', 'RequestBody'</span></span>

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

### <span data-ttu-id="560e5-118">-NegateCondition</span><span class="sxs-lookup"><span data-stu-id="560e5-118">-NegateCondition</span></span>
<span data-ttu-id="560e5-119">Ez a cikk azt ismerteti, hogy a hiba nem azonos-e, vagy nem az alapértelmezett érték hamis</span><span class="sxs-lookup"><span data-stu-id="560e5-119">Describes if this is negate condition or not Default value is false</span></span>

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

### <span data-ttu-id="560e5-120">-OperatorProperty</span><span class="sxs-lookup"><span data-stu-id="560e5-120">-OperatorProperty</span></span>
<span data-ttu-id="560e5-121">A megfelelő operátort ismerteti.</span><span class="sxs-lookup"><span data-stu-id="560e5-121">Describes operator to be matched.</span></span>
<span data-ttu-id="560e5-122">Lehetséges értékek: "any", "IPMatch", "GeoMatch", "egyenlő", "tartalmaz", "LessThan", "GreaterThan"; "LessThanOrEqual"; "GreaterThanOrEqual"; "BeginsWith"; "EndsWith" "</span><span class="sxs-lookup"><span data-stu-id="560e5-122">Possible values include: 'Any', 'IPMatch', 'GeoMatch', 'Equal', 'Contains', 'LessThan', 'GreaterThan', 'LessThanOrEqual', 'GreaterThanOrEqual', 'BeginsWith', 'EndsWith''</span></span>

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

### <span data-ttu-id="560e5-123">-Választó</span><span class="sxs-lookup"><span data-stu-id="560e5-123">-Selector</span></span>
<span data-ttu-id="560e5-124">A kijelölő neve a RequestHeader-ban vagy a RequestBody egyeztetve</span><span class="sxs-lookup"><span data-stu-id="560e5-124">Name of selector in RequestHeader or RequestBody to be matched</span></span>

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

### <span data-ttu-id="560e5-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="560e5-125">CommonParameters</span></span>
<span data-ttu-id="560e5-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="560e5-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="560e5-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="560e5-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="560e5-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="560e5-128">INPUTS</span></span>

### <span data-ttu-id="560e5-129">Nincs</span><span class="sxs-lookup"><span data-stu-id="560e5-129">None</span></span>

## <span data-ttu-id="560e5-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="560e5-130">OUTPUTS</span></span>

### <span data-ttu-id="560e5-131">Microsoft. Azure. Command. FrontDoor. models. PSMatchCondition</span><span class="sxs-lookup"><span data-stu-id="560e5-131">Microsoft.Azure.Commands.FrontDoor.Models.PSMatchCondition</span></span>

## <span data-ttu-id="560e5-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="560e5-132">NOTES</span></span>

## <span data-ttu-id="560e5-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="560e5-133">RELATED LINKS</span></span>

[<span data-ttu-id="560e5-134">Új – AzureRmFrontDoorCustomRuleObject</span><span class="sxs-lookup"><span data-stu-id="560e5-134">New-AzureRmFrontDoorCustomRuleObject</span></span>](./New-AzureRmFrontDoorCustomRuleObject.md)
