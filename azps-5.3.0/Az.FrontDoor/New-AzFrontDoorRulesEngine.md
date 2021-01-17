---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorrulesengine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngine.md
ms.openlocfilehash: 9f01a17bfe9e3e499e2bac2953f1cccc2af56c41
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469781"
---
# <span data-ttu-id="0db98-101">New-AzFrontDoorRulesEngine</span><span class="sxs-lookup"><span data-stu-id="0db98-101">New-AzFrontDoorRulesEngine</span></span>

## <span data-ttu-id="0db98-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0db98-102">SYNOPSIS</span></span>
<span data-ttu-id="0db98-103">Hozzon létre egy új szabálymotor-konfigurációt egy adott előtéri ajtóhoz.</span><span class="sxs-lookup"><span data-stu-id="0db98-103">Create a new rules engine configuration for a specified front door.</span></span> 

## <span data-ttu-id="0db98-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0db98-104">SYNTAX</span></span>

```
New-AzFrontDoorRulesEngine -ResourceGroupName <String> -FrontDoorName <String> -Name <String>
 [-Rule <PSRulesEngineRule[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0db98-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0db98-105">DESCRIPTION</span></span>
<span data-ttu-id="0db98-106">Hozzon létre egy új szabálymotor-konfigurációt egy adott előtéri ajtóhoz.</span><span class="sxs-lookup"><span data-stu-id="0db98-106">Create a new rules engine configuration for a specified front door.</span></span> 

<span data-ttu-id="0db98-107">A "New-AzFrontDoorRulesEngineRule" parancsmag használatával szabálymotorszabályokat építve adja át a parancsmag "-Rules" paraméterét.</span><span class="sxs-lookup"><span data-stu-id="0db98-107">Use cmdlet "New-AzFrontDoorRulesEngineRule" to construct rules engine rules to pass into the "-Rules" parameter of this cmdlet.</span></span>

## <span data-ttu-id="0db98-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0db98-108">EXAMPLES</span></span>

### <span data-ttu-id="0db98-109">1. példa</span><span class="sxs-lookup"><span data-stu-id="0db98-109">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name myRulesEngine -Rule $rulesEngineRule1

Name          RulesEngineRules
----          ----------------
myRulesEngine {rules1}
```

<span data-ttu-id="0db98-110">Hozzon létre egy új szabálymotor-konfigurációt a megadott előtér-ajtóhoz.</span><span class="sxs-lookup"><span data-stu-id="0db98-110">Create a new rules engine configuration for specified front door.</span></span>

## <span data-ttu-id="0db98-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0db98-111">PARAMETERS</span></span>

### <span data-ttu-id="0db98-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0db98-112">-DefaultProfile</span></span>
<span data-ttu-id="0db98-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0db98-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0db98-114">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="0db98-114">-FrontDoorName</span></span>
<span data-ttu-id="0db98-115">Front Door name.</span><span class="sxs-lookup"><span data-stu-id="0db98-115">Front Door name.</span></span>

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

### <span data-ttu-id="0db98-116">-Name</span><span class="sxs-lookup"><span data-stu-id="0db98-116">-Name</span></span>
<span data-ttu-id="0db98-117">A szabálymotor neve.</span><span class="sxs-lookup"><span data-stu-id="0db98-117">Rules engine name.</span></span>

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

### <span data-ttu-id="0db98-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0db98-118">-ResourceGroupName</span></span>
<span data-ttu-id="0db98-119">Az erőforráscsoport neve, amelybe a front door nevet fogja létrehozni.</span><span class="sxs-lookup"><span data-stu-id="0db98-119">The resource group name that the Front Door will be created in.</span></span>

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

### <span data-ttu-id="0db98-120">-Rule</span><span class="sxs-lookup"><span data-stu-id="0db98-120">-Rule</span></span>
<span data-ttu-id="0db98-121">Egy adott szabálymotor-konfigurációt definiáló szabályok listája.</span><span class="sxs-lookup"><span data-stu-id="0db98-121">A list of rules that define a particular Rules Engine Configuration.</span></span>

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

### <span data-ttu-id="0db98-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0db98-122">-Confirm</span></span>
<span data-ttu-id="0db98-123">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="0db98-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0db98-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0db98-124">-WhatIf</span></span>
<span data-ttu-id="0db98-125">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="0db98-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0db98-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0db98-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0db98-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0db98-127">CommonParameters</span></span>
<span data-ttu-id="0db98-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0db98-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0db98-129">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0db98-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0db98-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0db98-130">INPUTS</span></span>

### <span data-ttu-id="0db98-131">Nincs</span><span class="sxs-lookup"><span data-stu-id="0db98-131">None</span></span>

## <span data-ttu-id="0db98-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0db98-132">OUTPUTS</span></span>

### <span data-ttu-id="0db98-133">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span><span class="sxs-lookup"><span data-stu-id="0db98-133">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span></span>

## <span data-ttu-id="0db98-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0db98-134">NOTES</span></span>

## <span data-ttu-id="0db98-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0db98-135">RELATED LINKS</span></span>
