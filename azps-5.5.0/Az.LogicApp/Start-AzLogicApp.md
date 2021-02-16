---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 50C359FC-D98C-4C2C-87EE-BE9A25C3EDC6
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/start-azlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Start-AzLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Start-AzLogicApp.md
ms.openlocfilehash: e93efdaf8ec55c3b7c8fb0793a24e062553545ff
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100161418"
---
# <span data-ttu-id="d1154-101">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="d1154-101">Start-AzLogicApp</span></span>

## <span data-ttu-id="d1154-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d1154-102">SYNOPSIS</span></span>
<span data-ttu-id="d1154-103">Logikai alkalmazást futtat egy erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="d1154-103">Runs a logic app in a resource group.</span></span>

## <span data-ttu-id="d1154-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d1154-104">SYNTAX</span></span>

```
Start-AzLogicApp -ResourceGroupName <String> -Name <String> [-Parameters <Object>] -TriggerName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d1154-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d1154-105">DESCRIPTION</span></span>
<span data-ttu-id="d1154-106">A **Start-Az LogicApp** parancsmag logikai appot futtat a Logic Apps funkcióval.</span><span class="sxs-lookup"><span data-stu-id="d1154-106">The **Start-AzLogicApp** cmdlet runs a logic app by using the Logic Apps feature.</span></span>
<span data-ttu-id="d1154-107">Adjon meg egy nevet, erőforráscsoportot és eseményindítót.</span><span class="sxs-lookup"><span data-stu-id="d1154-107">Specify a name, resource group, and trigger.</span></span>
<span data-ttu-id="d1154-108">Ez a modul támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="d1154-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="d1154-109">Ha dinamikus paramétert használ, írja be a parancsba.</span><span class="sxs-lookup"><span data-stu-id="d1154-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="d1154-110">A dinamikus paraméterek nevének felfedezéséhez írjon be egy kötőjelet (-) a parancsmag neve után, majd a Tab billentyű többszöri lenyomása után lépkedhet a rendelkezésre álló paraméterek között.</span><span class="sxs-lookup"><span data-stu-id="d1154-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="d1154-111">Ha kihagy egy kötelező sablonparamétert, a parancsmag rákérdez az értékre.</span><span class="sxs-lookup"><span data-stu-id="d1154-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="d1154-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d1154-112">EXAMPLES</span></span>

### <span data-ttu-id="d1154-113">1. példa: Logikai alkalmazás futtatása</span><span class="sxs-lookup"><span data-stu-id="d1154-113">Example 1: Run a logic app</span></span>
```
PS C:\>Start-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03" -TriggerName "Trigger22"
```

<span data-ttu-id="d1154-114">Ez a parancs a logic appot az ResourceGroup11 nevű erőforráscsoportban futtatja.</span><span class="sxs-lookup"><span data-stu-id="d1154-114">This command runs the logic app in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="d1154-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d1154-115">PARAMETERS</span></span>

### <span data-ttu-id="d1154-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1154-116">-DefaultProfile</span></span>
<span data-ttu-id="d1154-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="d1154-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d1154-118">-Name</span><span class="sxs-lookup"><span data-stu-id="d1154-118">-Name</span></span>
<span data-ttu-id="d1154-119">A parancsmag által elindított logikai app nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d1154-119">Specifies the name of the logic app that this cmdlet starts.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1154-120">-Parameters</span><span class="sxs-lookup"><span data-stu-id="d1154-120">-Parameters</span></span>
<span data-ttu-id="d1154-121">A logikai alkalmazás paramétergyűjtemény-objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d1154-121">Specifies a parameters collection object of the logic app.</span></span>
<span data-ttu-id="d1154-122">Adjon meg egy kivonattáblát, szótárat \<string\> vagy \<string, WorkflowParameter\> szótárat.</span><span class="sxs-lookup"><span data-stu-id="d1154-122">Specify a hash table, Dictionary\<string\>, or Dictionary\<string, WorkflowParameter\>.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1154-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1154-123">-ResourceGroupName</span></span>
<span data-ttu-id="d1154-124">Annak az erőforráscsoportnak a nevét adja meg, amely a parancsmag által elindított logikai appot tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="d1154-124">Specifies the name of the resource group that contains the logic app that this cmdlet starts.</span></span>

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

### <span data-ttu-id="d1154-125">-TriggerName</span><span class="sxs-lookup"><span data-stu-id="d1154-125">-TriggerName</span></span>
<span data-ttu-id="d1154-126">A parancsmag által elindított logikai alkalmazás eseményindítójának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d1154-126">Specifies the name of the trigger of the logic app that this cmdlet starts.</span></span>

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

### <span data-ttu-id="d1154-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d1154-127">-Confirm</span></span>
<span data-ttu-id="d1154-128">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d1154-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1154-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1154-129">-WhatIf</span></span>
<span data-ttu-id="d1154-130">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="d1154-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1154-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d1154-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1154-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1154-132">CommonParameters</span></span>
<span data-ttu-id="d1154-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1154-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1154-134">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1154-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1154-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d1154-135">INPUTS</span></span>

### <span data-ttu-id="d1154-136">System.String</span><span class="sxs-lookup"><span data-stu-id="d1154-136">System.String</span></span>

## <span data-ttu-id="d1154-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d1154-137">OUTPUTS</span></span>

### <span data-ttu-id="d1154-138">System.Void</span><span class="sxs-lookup"><span data-stu-id="d1154-138">System.Void</span></span>

## <span data-ttu-id="d1154-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d1154-139">NOTES</span></span>

## <span data-ttu-id="d1154-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d1154-140">RELATED LINKS</span></span>

[<span data-ttu-id="d1154-141">Get-AzApp</span><span class="sxs-lookup"><span data-stu-id="d1154-141">Get-AzLogicApp</span></span>](./Get-AzLogicApp.md)

[<span data-ttu-id="d1154-142">Get-AzRunAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="d1154-142">Get-AzLogicAppRunHistory</span></span>](./Get-AzLogicAppRunHistory.md)

[<span data-ttu-id="d1154-143">New-AzApp</span><span class="sxs-lookup"><span data-stu-id="d1154-143">New-AzLogicApp</span></span>](./New-AzLogicApp.md)

[<span data-ttu-id="d1154-144">Remove-AzApp</span><span class="sxs-lookup"><span data-stu-id="d1154-144">Remove-AzLogicApp</span></span>](./Remove-AzLogicApp.md)

[<span data-ttu-id="d1154-145">Set-AzApp</span><span class="sxs-lookup"><span data-stu-id="d1154-145">Set-AzLogicApp</span></span>](./Set-AzLogicApp.md)

[<span data-ttu-id="d1154-146">Stop-AzRunAppRun</span><span class="sxs-lookup"><span data-stu-id="d1154-146">Stop-AzLogicAppRun</span></span>](./Stop-AzLogicAppRun.md)


