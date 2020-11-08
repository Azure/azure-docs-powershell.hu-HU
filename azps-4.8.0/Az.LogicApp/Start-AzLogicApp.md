---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 50C359FC-D98C-4C2C-87EE-BE9A25C3EDC6
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/start-azlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Start-AzLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Start-AzLogicApp.md
ms.openlocfilehash: e93efdaf8ec55c3b7c8fb0793a24e062553545ff
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184466"
---
# <span data-ttu-id="e23f1-101">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="e23f1-101">Start-AzLogicApp</span></span>

## <span data-ttu-id="e23f1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e23f1-102">SYNOPSIS</span></span>
<span data-ttu-id="e23f1-103">Egy logikai alkalmazást futtat egy erőforráscsoportben.</span><span class="sxs-lookup"><span data-stu-id="e23f1-103">Runs a logic app in a resource group.</span></span>

## <span data-ttu-id="e23f1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e23f1-104">SYNTAX</span></span>

```
Start-AzLogicApp -ResourceGroupName <String> -Name <String> [-Parameters <Object>] -TriggerName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e23f1-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e23f1-105">DESCRIPTION</span></span>
<span data-ttu-id="e23f1-106">A **Start-AzLogicApp** parancsmag a Logic apps funkció segítségével futtatja a logikai alkalmazást.</span><span class="sxs-lookup"><span data-stu-id="e23f1-106">The **Start-AzLogicApp** cmdlet runs a logic app by using the Logic Apps feature.</span></span>
<span data-ttu-id="e23f1-107">Adjon meg egy nevet, erőforráscsoportot és triggert.</span><span class="sxs-lookup"><span data-stu-id="e23f1-107">Specify a name, resource group, and trigger.</span></span>
<span data-ttu-id="e23f1-108">Ez a modul támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="e23f1-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="e23f1-109">Ha dinamikus paramétert szeretne használni, írja be azt a parancsba.</span><span class="sxs-lookup"><span data-stu-id="e23f1-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="e23f1-110">A dinamikus paraméterek nevének feltárásához írjon be egy kötőjelet (-) a parancsmag neve után, majd nyomja le többször a TAB billentyűt a rendelkezésre álló paraméterek közötti váltáshoz.</span><span class="sxs-lookup"><span data-stu-id="e23f1-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="e23f1-111">Ha kihagyja a szükséges sablon paramétert, a parancsmag kéri az érték megadását.</span><span class="sxs-lookup"><span data-stu-id="e23f1-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="e23f1-112">Példák</span><span class="sxs-lookup"><span data-stu-id="e23f1-112">EXAMPLES</span></span>

### <span data-ttu-id="e23f1-113">Példa 1: logikai alkalmazás futtatása</span><span class="sxs-lookup"><span data-stu-id="e23f1-113">Example 1: Run a logic app</span></span>
```
PS C:\>Start-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03" -TriggerName "Trigger22"
```

<span data-ttu-id="e23f1-114">Ez a parancs futtatja a Logic alkalmazást a ResourceGroup11 nevű erőforráscsoport-csoportban.</span><span class="sxs-lookup"><span data-stu-id="e23f1-114">This command runs the logic app in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="e23f1-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e23f1-115">PARAMETERS</span></span>

### <span data-ttu-id="e23f1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e23f1-116">-DefaultProfile</span></span>
<span data-ttu-id="e23f1-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="e23f1-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e23f1-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e23f1-118">-Name</span></span>
<span data-ttu-id="e23f1-119">Annak a logikai alkalmazásnak a nevét adja meg, amelyre a parancsmag indul.</span><span class="sxs-lookup"><span data-stu-id="e23f1-119">Specifies the name of the logic app that this cmdlet starts.</span></span>

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

### <span data-ttu-id="e23f1-120">-Paraméterek</span><span class="sxs-lookup"><span data-stu-id="e23f1-120">-Parameters</span></span>
<span data-ttu-id="e23f1-121">A Logic app Parameters Collection objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="e23f1-121">Specifies a parameters collection object of the logic app.</span></span>
<span data-ttu-id="e23f1-122">Adjon meg egy kivonatoló táblázatot, szótárt \<string\> vagy szótárat \<string, WorkflowParameter\> .</span><span class="sxs-lookup"><span data-stu-id="e23f1-122">Specify a hash table, Dictionary\<string\>, or Dictionary\<string, WorkflowParameter\>.</span></span>

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

### <span data-ttu-id="e23f1-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e23f1-123">-ResourceGroupName</span></span>
<span data-ttu-id="e23f1-124">Annak a logikai alkalmazást tartalmazó erőforráscsoportnak a neve, amely a parancsmag kezdetét tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="e23f1-124">Specifies the name of the resource group that contains the logic app that this cmdlet starts.</span></span>

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

### <span data-ttu-id="e23f1-125">-TriggerName</span><span class="sxs-lookup"><span data-stu-id="e23f1-125">-TriggerName</span></span>
<span data-ttu-id="e23f1-126">Annak a logikai alkalmazásnak az indítóját adja meg, amelyre a parancsmag elindul.</span><span class="sxs-lookup"><span data-stu-id="e23f1-126">Specifies the name of the trigger of the logic app that this cmdlet starts.</span></span>

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

### <span data-ttu-id="e23f1-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e23f1-127">-Confirm</span></span>
<span data-ttu-id="e23f1-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e23f1-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e23f1-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e23f1-129">-WhatIf</span></span>
<span data-ttu-id="e23f1-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e23f1-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e23f1-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e23f1-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e23f1-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e23f1-132">CommonParameters</span></span>
<span data-ttu-id="e23f1-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e23f1-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e23f1-134">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e23f1-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e23f1-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e23f1-135">INPUTS</span></span>

### <span data-ttu-id="e23f1-136">System. String</span><span class="sxs-lookup"><span data-stu-id="e23f1-136">System.String</span></span>

## <span data-ttu-id="e23f1-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e23f1-137">OUTPUTS</span></span>

### <span data-ttu-id="e23f1-138">System. Void</span><span class="sxs-lookup"><span data-stu-id="e23f1-138">System.Void</span></span>

## <span data-ttu-id="e23f1-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e23f1-139">NOTES</span></span>

## <span data-ttu-id="e23f1-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e23f1-140">RELATED LINKS</span></span>

[<span data-ttu-id="e23f1-141">Get-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="e23f1-141">Get-AzLogicApp</span></span>](./Get-AzLogicApp.md)

[<span data-ttu-id="e23f1-142">Get-AzLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="e23f1-142">Get-AzLogicAppRunHistory</span></span>](./Get-AzLogicAppRunHistory.md)

[<span data-ttu-id="e23f1-143">Új – AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="e23f1-143">New-AzLogicApp</span></span>](./New-AzLogicApp.md)

[<span data-ttu-id="e23f1-144">Remove-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="e23f1-144">Remove-AzLogicApp</span></span>](./Remove-AzLogicApp.md)

[<span data-ttu-id="e23f1-145">Set-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="e23f1-145">Set-AzLogicApp</span></span>](./Set-AzLogicApp.md)

[<span data-ttu-id="e23f1-146">Stop-AzLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="e23f1-146">Stop-AzLogicAppRun</span></span>](./Stop-AzLogicAppRun.md)


