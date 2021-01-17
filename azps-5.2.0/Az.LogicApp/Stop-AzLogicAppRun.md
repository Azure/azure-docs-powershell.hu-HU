---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 3308F901-4C9F-424D-8BEB-877A6038B246
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/stop-azlogicapprun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Stop-AzLogicAppRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Stop-AzLogicAppRun.md
ms.openlocfilehash: 9a437d3b8e1803865aedf7e46d0bf879cfcdeab8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98343565"
---
# <span data-ttu-id="fc130-101">Stop-AzLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="fc130-101">Stop-AzLogicAppRun</span></span>

## <span data-ttu-id="fc130-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc130-102">SYNOPSIS</span></span>
<span data-ttu-id="fc130-103">Megszakítja egy logikai alkalmazás futtatását.</span><span class="sxs-lookup"><span data-stu-id="fc130-103">Cancels a run of a logic app.</span></span>

## <span data-ttu-id="fc130-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="fc130-104">SYNTAX</span></span>

```
Stop-AzLogicAppRun -ResourceGroupName <String> -Name <String> -RunName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc130-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="fc130-105">DESCRIPTION</span></span>
<span data-ttu-id="fc130-106">A **Stop-AzRunRun parancsmag** megszakítja egy logikai alkalmazás futtatását.</span><span class="sxs-lookup"><span data-stu-id="fc130-106">The **Stop-AzLogicAppRun** cmdlet cancels a run of a logic app.</span></span>
<span data-ttu-id="fc130-107">Adja meg a logikai alkalmazást, az erőforráscsoportot, és futtassa.</span><span class="sxs-lookup"><span data-stu-id="fc130-107">Specify the logic app, resource group, and run.</span></span>
<span data-ttu-id="fc130-108">Ez a modul támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="fc130-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="fc130-109">Ha dinamikus paramétert használ, írja be a parancsba.</span><span class="sxs-lookup"><span data-stu-id="fc130-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="fc130-110">A dinamikus paraméterek nevének felfedezéséhez írjon be egy kötőjelet (-) a parancsmag neve után, majd a Tab billentyű többszöri lenyomása után lépkedhet a rendelkezésre álló paraméterek között.</span><span class="sxs-lookup"><span data-stu-id="fc130-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="fc130-111">Ha kihagy egy kötelező sablonparamétert, a parancsmag rákérdez az értékre.</span><span class="sxs-lookup"><span data-stu-id="fc130-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="fc130-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="fc130-112">EXAMPLES</span></span>

### <span data-ttu-id="fc130-113">1. példa: Logikai alkalmazás futtatásának megszakítása</span><span class="sxs-lookup"><span data-stu-id="fc130-113">Example 1: Cancel a run of a logic app</span></span>
```
PS C:\>Stop-AzLogicAppRun -ResourceGroupName "ResourceGroup11" -Name "LogicApp03" -RunName "08587489104702792076" -Force
```

<span data-ttu-id="fc130-114">Ez a parancs megszakítja a LogicApp03 nevű logikai alkalmazás futtatását.</span><span class="sxs-lookup"><span data-stu-id="fc130-114">This command cancels a run of the logic app named LogicApp03.</span></span>

## <span data-ttu-id="fc130-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fc130-115">PARAMETERS</span></span>

### <span data-ttu-id="fc130-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc130-116">-DefaultProfile</span></span>
<span data-ttu-id="fc130-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="fc130-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fc130-118">-Force</span><span class="sxs-lookup"><span data-stu-id="fc130-118">-Force</span></span>
<span data-ttu-id="fc130-119">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="fc130-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="fc130-120">-Name</span><span class="sxs-lookup"><span data-stu-id="fc130-120">-Name</span></span>
<span data-ttu-id="fc130-121">Annak a logikai alkalmazásnak a nevét adja meg, amelynek a parancsmagja megszakít egy futtatást.</span><span class="sxs-lookup"><span data-stu-id="fc130-121">Specifies the name of a logic app for which this cmdlet cancels a run.</span></span>

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

### <span data-ttu-id="fc130-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc130-122">-ResourceGroupName</span></span>
<span data-ttu-id="fc130-123">Annak az erőforráscsoportnak a nevét adja meg, amelyben a parancsmag megszakítja a futtatásokat.</span><span class="sxs-lookup"><span data-stu-id="fc130-123">Specifies the name for a resource group in which this cmdlet cancels a run.</span></span>

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

### <span data-ttu-id="fc130-124">-RunName</span><span class="sxs-lookup"><span data-stu-id="fc130-124">-RunName</span></span>
<span data-ttu-id="fc130-125">A parancsmag által megszakított logikai app nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fc130-125">Specifies the name of a logic app run that this cmdlet cancels.</span></span>

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

### <span data-ttu-id="fc130-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fc130-126">-Confirm</span></span>
<span data-ttu-id="fc130-127">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="fc130-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc130-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc130-128">-WhatIf</span></span>
<span data-ttu-id="fc130-129">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="fc130-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc130-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fc130-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc130-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc130-131">CommonParameters</span></span>
<span data-ttu-id="fc130-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc130-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc130-133">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc130-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc130-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fc130-134">INPUTS</span></span>

### <span data-ttu-id="fc130-135">System.String</span><span class="sxs-lookup"><span data-stu-id="fc130-135">System.String</span></span>

## <span data-ttu-id="fc130-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fc130-136">OUTPUTS</span></span>

### <span data-ttu-id="fc130-137">System.Void</span><span class="sxs-lookup"><span data-stu-id="fc130-137">System.Void</span></span>

## <span data-ttu-id="fc130-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="fc130-138">NOTES</span></span>

## <span data-ttu-id="fc130-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fc130-139">RELATED LINKS</span></span>

[<span data-ttu-id="fc130-140">Start-AzApp</span><span class="sxs-lookup"><span data-stu-id="fc130-140">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)


