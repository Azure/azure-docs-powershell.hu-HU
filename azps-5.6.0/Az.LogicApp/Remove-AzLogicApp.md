---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 39D1576D-7042-4A62-AB41-0B5131C150D5
online version: https://docs.microsoft.com/powershell/module/az.logicapp/remove-azlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzLogicApp.md
ms.openlocfilehash: f9feca370a2672b14252691711810f5de241aa78
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925537"
---
# <span data-ttu-id="518d1-101">Remove-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="518d1-101">Remove-AzLogicApp</span></span>

## <span data-ttu-id="518d1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="518d1-102">SYNOPSIS</span></span>
<span data-ttu-id="518d1-103">Eltávolít egy logikai alkalmazást egy erőforráscsoportból.</span><span class="sxs-lookup"><span data-stu-id="518d1-103">Removes a logic app from a resource group.</span></span>

## <span data-ttu-id="518d1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="518d1-104">SYNTAX</span></span>

```
Remove-AzLogicApp -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="518d1-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="518d1-105">DESCRIPTION</span></span>
<span data-ttu-id="518d1-106">A **Remove-Az LogicApp** parancsmag a Logic Apps funkcióval eltávolítja a logikai alkalmazásokat egy erőforráscsoportból.</span><span class="sxs-lookup"><span data-stu-id="518d1-106">The **Remove-AzLogicApp** cmdlet removes a logic app from a resource group by using the Logic Apps feature.</span></span>
<span data-ttu-id="518d1-107">Adja meg a logikai alkalmazást és az erőforráscsoportot.</span><span class="sxs-lookup"><span data-stu-id="518d1-107">Specify the logic app and resource group.</span></span>
<span data-ttu-id="518d1-108">Ez a modul támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="518d1-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="518d1-109">Ha dinamikus paramétert használ, írja be a parancsba.</span><span class="sxs-lookup"><span data-stu-id="518d1-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="518d1-110">A dinamikus paraméterek nevének felfedezéséhez írjon be egy kötőjelet (-) a parancsmag neve után, majd a Tab billentyű többszöri lenyomása után lépkedhet a rendelkezésre álló paraméterek között.</span><span class="sxs-lookup"><span data-stu-id="518d1-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="518d1-111">Ha kihagy egy kötelező sablonparamétert, a parancsmag rákérdez az értékre.</span><span class="sxs-lookup"><span data-stu-id="518d1-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="518d1-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="518d1-112">EXAMPLES</span></span>

### <span data-ttu-id="518d1-113">1. példa: Logikai alkalmazás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="518d1-113">Example 1: Remove a logic app</span></span>
```
PS C:\>Remove-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03" -Force
```

<span data-ttu-id="518d1-114">Ez a parancs eltávolít egy logikai alkalmazást egy erőforráscsoportból.</span><span class="sxs-lookup"><span data-stu-id="518d1-114">This command removes a logic app from a resource group.</span></span>
<span data-ttu-id="518d1-115">A parancs tartalmazza az *Kényszerítés* paramétert, amely megakadályozza, hogy a parancs megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="518d1-115">The command includes the *Force* parameter, which prevents the command from prompting you for confirmation.</span></span>

## <span data-ttu-id="518d1-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="518d1-116">PARAMETERS</span></span>

### <span data-ttu-id="518d1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="518d1-117">-DefaultProfile</span></span>
<span data-ttu-id="518d1-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="518d1-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="518d1-119">-Force</span><span class="sxs-lookup"><span data-stu-id="518d1-119">-Force</span></span>
<span data-ttu-id="518d1-120">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="518d1-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="518d1-121">-Name</span><span class="sxs-lookup"><span data-stu-id="518d1-121">-Name</span></span>
<span data-ttu-id="518d1-122">Annak a logikai alkalmazásnak a nevét adja meg, amelyről a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="518d1-122">Specifies the name of the logic app that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="518d1-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="518d1-123">-ResourceGroupName</span></span>
<span data-ttu-id="518d1-124">Annak az erőforráscsoportnak a nevét adja meg, amely a parancsmag által eltávolított logikai appot tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="518d1-124">Specifies the name of the resource group that contains the logic app that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="518d1-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="518d1-125">-Confirm</span></span>
<span data-ttu-id="518d1-126">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="518d1-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="518d1-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="518d1-127">-WhatIf</span></span>
<span data-ttu-id="518d1-128">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="518d1-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="518d1-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="518d1-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="518d1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="518d1-130">CommonParameters</span></span>
<span data-ttu-id="518d1-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="518d1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="518d1-132">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="518d1-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="518d1-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="518d1-133">INPUTS</span></span>

### <span data-ttu-id="518d1-134">System.String</span><span class="sxs-lookup"><span data-stu-id="518d1-134">System.String</span></span>

## <span data-ttu-id="518d1-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="518d1-135">OUTPUTS</span></span>

### <span data-ttu-id="518d1-136">System.Void</span><span class="sxs-lookup"><span data-stu-id="518d1-136">System.Void</span></span>

## <span data-ttu-id="518d1-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="518d1-137">NOTES</span></span>

## <span data-ttu-id="518d1-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="518d1-138">RELATED LINKS</span></span>

[<span data-ttu-id="518d1-139">Get-AzApp</span><span class="sxs-lookup"><span data-stu-id="518d1-139">Get-AzLogicApp</span></span>](./Get-AzLogicApp.md)

[<span data-ttu-id="518d1-140">New-AzApp</span><span class="sxs-lookup"><span data-stu-id="518d1-140">New-AzLogicApp</span></span>](./New-AzLogicApp.md)

[<span data-ttu-id="518d1-141">Set-AzApp</span><span class="sxs-lookup"><span data-stu-id="518d1-141">Set-AzLogicApp</span></span>](./Set-AzLogicApp.md)

[<span data-ttu-id="518d1-142">Start-AzApp</span><span class="sxs-lookup"><span data-stu-id="518d1-142">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)


