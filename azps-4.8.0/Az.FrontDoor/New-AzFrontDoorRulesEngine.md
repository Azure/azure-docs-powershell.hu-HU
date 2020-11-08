---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorrulesengine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngine.md
ms.openlocfilehash: 9f01a17bfe9e3e499e2bac2953f1cccc2af56c41
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94017761"
---
# <span data-ttu-id="8f2cd-101">New-AzFrontDoorRulesEngine</span><span class="sxs-lookup"><span data-stu-id="8f2cd-101">New-AzFrontDoorRulesEngine</span></span>

## <span data-ttu-id="8f2cd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8f2cd-102">SYNOPSIS</span></span>
<span data-ttu-id="8f2cd-103">Új szabályok motor-konfigurációjának létrehozása adott bejárati ajtóhoz.</span><span class="sxs-lookup"><span data-stu-id="8f2cd-103">Create a new rules engine configuration for a specified front door.</span></span> 

## <span data-ttu-id="8f2cd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8f2cd-104">SYNTAX</span></span>

```
New-AzFrontDoorRulesEngine -ResourceGroupName <String> -FrontDoorName <String> -Name <String>
 [-Rule <PSRulesEngineRule[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8f2cd-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8f2cd-105">DESCRIPTION</span></span>
<span data-ttu-id="8f2cd-106">Új szabályok motor-konfigurációjának létrehozása adott bejárati ajtóhoz.</span><span class="sxs-lookup"><span data-stu-id="8f2cd-106">Create a new rules engine configuration for a specified front door.</span></span> 

<span data-ttu-id="8f2cd-107">A "New-AzFrontDoorRulesEngineRule" parancsmaggal létrehozhatja a szabályok motorjának szabályait, hogy átmenjenek a parancsmag "-Rules" paraméterére.</span><span class="sxs-lookup"><span data-stu-id="8f2cd-107">Use cmdlet "New-AzFrontDoorRulesEngineRule" to construct rules engine rules to pass into the "-Rules" parameter of this cmdlet.</span></span>

## <span data-ttu-id="8f2cd-108">Példák</span><span class="sxs-lookup"><span data-stu-id="8f2cd-108">EXAMPLES</span></span>

### <span data-ttu-id="8f2cd-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="8f2cd-109">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name myRulesEngine -Rule $rulesEngineRule1

Name          RulesEngineRules
----          ----------------
myRulesEngine {rules1}
```

<span data-ttu-id="8f2cd-110">Új szabály-végrehajtó konfiguráció létrehozása a megadott bejárati ajtóhoz.</span><span class="sxs-lookup"><span data-stu-id="8f2cd-110">Create a new rules engine configuration for specified front door.</span></span>

## <span data-ttu-id="8f2cd-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8f2cd-111">PARAMETERS</span></span>

### <span data-ttu-id="8f2cd-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f2cd-112">-DefaultProfile</span></span>
<span data-ttu-id="8f2cd-113">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8f2cd-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8f2cd-114">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="8f2cd-114">-FrontDoorName</span></span>
<span data-ttu-id="8f2cd-115">A bejárati ajtó neve.</span><span class="sxs-lookup"><span data-stu-id="8f2cd-115">Front Door name.</span></span>

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

### <span data-ttu-id="8f2cd-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8f2cd-116">-Name</span></span>
<span data-ttu-id="8f2cd-117">A szabályok motorjának neve</span><span class="sxs-lookup"><span data-stu-id="8f2cd-117">Rules engine name.</span></span>

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

### <span data-ttu-id="8f2cd-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f2cd-118">-ResourceGroupName</span></span>
<span data-ttu-id="8f2cd-119">Az erőforráscsoport neve, amelybe az első ajtó jön létre.</span><span class="sxs-lookup"><span data-stu-id="8f2cd-119">The resource group name that the Front Door will be created in.</span></span>

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

### <span data-ttu-id="8f2cd-120">-Szabály</span><span class="sxs-lookup"><span data-stu-id="8f2cd-120">-Rule</span></span>
<span data-ttu-id="8f2cd-121">Az egyes szabályok motor-konfigurációját meghatározó szabályok listája.</span><span class="sxs-lookup"><span data-stu-id="8f2cd-121">A list of rules that define a particular Rules Engine Configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f2cd-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8f2cd-122">-Confirm</span></span>
<span data-ttu-id="8f2cd-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8f2cd-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f2cd-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f2cd-124">-WhatIf</span></span>
<span data-ttu-id="8f2cd-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8f2cd-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8f2cd-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8f2cd-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f2cd-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f2cd-127">CommonParameters</span></span>
<span data-ttu-id="8f2cd-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8f2cd-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f2cd-129">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="8f2cd-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f2cd-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8f2cd-130">INPUTS</span></span>

### <span data-ttu-id="8f2cd-131">Nincs</span><span class="sxs-lookup"><span data-stu-id="8f2cd-131">None</span></span>

## <span data-ttu-id="8f2cd-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8f2cd-132">OUTPUTS</span></span>

### <span data-ttu-id="8f2cd-133">Microsoft. Azure. Command. FrontDoor. models. PSRulesEngine</span><span class="sxs-lookup"><span data-stu-id="8f2cd-133">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span></span>

## <span data-ttu-id="8f2cd-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8f2cd-134">NOTES</span></span>

## <span data-ttu-id="8f2cd-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8f2cd-135">RELATED LINKS</span></span>
