---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 50C359FC-D98C-4C2C-87EE-BE9A25C3EDC6
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/start-azlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Start-AzLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Start-AzLogicApp.md
ms.openlocfilehash: e93efdaf8ec55c3b7c8fb0793a24e062553545ff
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98368338"
---
# <span data-ttu-id="0db9e-101">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="0db9e-101">Start-AzLogicApp</span></span>

## <span data-ttu-id="0db9e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0db9e-102">SYNOPSIS</span></span>
<span data-ttu-id="0db9e-103">Logikai alkalmazást futtat egy erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="0db9e-103">Runs a logic app in a resource group.</span></span>

## <span data-ttu-id="0db9e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0db9e-104">SYNTAX</span></span>

```
Start-AzLogicApp -ResourceGroupName <String> -Name <String> [-Parameters <Object>] -TriggerName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0db9e-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0db9e-105">DESCRIPTION</span></span>
<span data-ttu-id="0db9e-106">A **Start-Az LogicApp** parancsmag logikai appot futtat a Logic Apps funkcióval.</span><span class="sxs-lookup"><span data-stu-id="0db9e-106">The **Start-AzLogicApp** cmdlet runs a logic app by using the Logic Apps feature.</span></span>
<span data-ttu-id="0db9e-107">Adjon meg egy nevet, erőforráscsoportot és eseményindítót.</span><span class="sxs-lookup"><span data-stu-id="0db9e-107">Specify a name, resource group, and trigger.</span></span>
<span data-ttu-id="0db9e-108">Ez a modul támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="0db9e-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="0db9e-109">Ha dinamikus paramétert használ, írja be a parancsba.</span><span class="sxs-lookup"><span data-stu-id="0db9e-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="0db9e-110">A dinamikus paraméterek nevének felfedezéséhez írjon be egy kötőjelet (-) a parancsmag neve után, majd a Tab billentyű többszöri lenyomása után lépkedhet a rendelkezésre álló paraméterek között.</span><span class="sxs-lookup"><span data-stu-id="0db9e-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="0db9e-111">Ha kihagy egy kötelező sablonparamétert, a parancsmag rákérdez az értékre.</span><span class="sxs-lookup"><span data-stu-id="0db9e-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="0db9e-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0db9e-112">EXAMPLES</span></span>

### <span data-ttu-id="0db9e-113">1. példa: Logikai alkalmazás futtatása</span><span class="sxs-lookup"><span data-stu-id="0db9e-113">Example 1: Run a logic app</span></span>
```
PS C:\>Start-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03" -TriggerName "Trigger22"
```

<span data-ttu-id="0db9e-114">Ez a parancs a logic appot az ResourceGroup11 nevű erőforráscsoportban futtatja.</span><span class="sxs-lookup"><span data-stu-id="0db9e-114">This command runs the logic app in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="0db9e-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0db9e-115">PARAMETERS</span></span>

### <span data-ttu-id="0db9e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0db9e-116">-DefaultProfile</span></span>
<span data-ttu-id="0db9e-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="0db9e-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0db9e-118">-Name</span><span class="sxs-lookup"><span data-stu-id="0db9e-118">-Name</span></span>
<span data-ttu-id="0db9e-119">Annak a logikai alkalmazásnak a nevét adja meg, amelytől a parancsmag elindul.</span><span class="sxs-lookup"><span data-stu-id="0db9e-119">Specifies the name of the logic app that this cmdlet starts.</span></span>

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

### <span data-ttu-id="0db9e-120">-Parameters</span><span class="sxs-lookup"><span data-stu-id="0db9e-120">-Parameters</span></span>
<span data-ttu-id="0db9e-121">A logikai alkalmazás paramétergyűjtemény-objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="0db9e-121">Specifies a parameters collection object of the logic app.</span></span>
<span data-ttu-id="0db9e-122">Adjon meg egy kivonattáblát, szótárat \<string\> vagy \<string, WorkflowParameter\> szótárat.</span><span class="sxs-lookup"><span data-stu-id="0db9e-122">Specify a hash table, Dictionary\<string\>, or Dictionary\<string, WorkflowParameter\>.</span></span>

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

### <span data-ttu-id="0db9e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0db9e-123">-ResourceGroupName</span></span>
<span data-ttu-id="0db9e-124">Annak az erőforráscsoportnak a nevét adja meg, amely a parancsmag által elindított logikai appot tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="0db9e-124">Specifies the name of the resource group that contains the logic app that this cmdlet starts.</span></span>

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

### <span data-ttu-id="0db9e-125">-TriggerName</span><span class="sxs-lookup"><span data-stu-id="0db9e-125">-TriggerName</span></span>
<span data-ttu-id="0db9e-126">A parancsmag által elindított logikai alkalmazás eseményindítójának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0db9e-126">Specifies the name of the trigger of the logic app that this cmdlet starts.</span></span>

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

### <span data-ttu-id="0db9e-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0db9e-127">-Confirm</span></span>
<span data-ttu-id="0db9e-128">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="0db9e-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0db9e-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0db9e-129">-WhatIf</span></span>
<span data-ttu-id="0db9e-130">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="0db9e-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0db9e-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0db9e-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0db9e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0db9e-132">CommonParameters</span></span>
<span data-ttu-id="0db9e-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0db9e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0db9e-134">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0db9e-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0db9e-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0db9e-135">INPUTS</span></span>

### <span data-ttu-id="0db9e-136">System.String</span><span class="sxs-lookup"><span data-stu-id="0db9e-136">System.String</span></span>

## <span data-ttu-id="0db9e-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0db9e-137">OUTPUTS</span></span>

### <span data-ttu-id="0db9e-138">System.Void</span><span class="sxs-lookup"><span data-stu-id="0db9e-138">System.Void</span></span>

## <span data-ttu-id="0db9e-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0db9e-139">NOTES</span></span>

## <span data-ttu-id="0db9e-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0db9e-140">RELATED LINKS</span></span>

[<span data-ttu-id="0db9e-141">Get-AzApp</span><span class="sxs-lookup"><span data-stu-id="0db9e-141">Get-AzLogicApp</span></span>](./Get-AzLogicApp.md)

[<span data-ttu-id="0db9e-142">Get-AzRunAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="0db9e-142">Get-AzLogicAppRunHistory</span></span>](./Get-AzLogicAppRunHistory.md)

[<span data-ttu-id="0db9e-143">New-AzApp</span><span class="sxs-lookup"><span data-stu-id="0db9e-143">New-AzLogicApp</span></span>](./New-AzLogicApp.md)

[<span data-ttu-id="0db9e-144">Remove-AzApp</span><span class="sxs-lookup"><span data-stu-id="0db9e-144">Remove-AzLogicApp</span></span>](./Remove-AzLogicApp.md)

[<span data-ttu-id="0db9e-145">Set-AzApp</span><span class="sxs-lookup"><span data-stu-id="0db9e-145">Set-AzLogicApp</span></span>](./Set-AzLogicApp.md)

[<span data-ttu-id="0db9e-146">Stop-AzRunAppRun</span><span class="sxs-lookup"><span data-stu-id="0db9e-146">Stop-AzLogicAppRun</span></span>](./Stop-AzLogicAppRun.md)


