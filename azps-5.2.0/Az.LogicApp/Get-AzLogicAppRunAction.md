---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 2EA28B90-4BAE-45DF-BD2E-60C74F53FB7B
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azlogicapprunaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppRunAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppRunAction.md
ms.openlocfilehash: c382b4bb9a02150beaa6880fd88d8f7b376b7c34
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98356177"
---
# <span data-ttu-id="e38ab-101">Get-AzLogicAppRunAction</span><span class="sxs-lookup"><span data-stu-id="e38ab-101">Get-AzLogicAppRunAction</span></span>

## <span data-ttu-id="e38ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e38ab-102">SYNOPSIS</span></span>
<span data-ttu-id="e38ab-103">Egy logikai appból futtat egy műveletet.</span><span class="sxs-lookup"><span data-stu-id="e38ab-103">Gets an action from a logic app run.</span></span>

## <span data-ttu-id="e38ab-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e38ab-104">SYNTAX</span></span>

```
Get-AzLogicAppRunAction -ResourceGroupName <String> -Name <String> -RunName <String> [-ActionName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e38ab-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e38ab-105">DESCRIPTION</span></span>
<span data-ttu-id="e38ab-106">A **Get-Az LogicAppRunAction parancsmag** egy logikai app futtatásával kapja meg a műveletet.</span><span class="sxs-lookup"><span data-stu-id="e38ab-106">The **Get-AzLogicAppRunAction** cmdlet gets an action from a logic app run.</span></span>
<span data-ttu-id="e38ab-107">Ez a parancsmag **egy WorkflowRunAction objektumot ad** vissza.</span><span class="sxs-lookup"><span data-stu-id="e38ab-107">This cmdlet returns a **WorkflowRunAction** objects.</span></span>
<span data-ttu-id="e38ab-108">Adja meg a logikai alkalmazást, az erőforráscsoportot, és futtassa.</span><span class="sxs-lookup"><span data-stu-id="e38ab-108">Specify the logic app, resource group, and run.</span></span>
<span data-ttu-id="e38ab-109">Ez a modul támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="e38ab-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="e38ab-110">Ha dinamikus paramétert használ, írja be a parancsba.</span><span class="sxs-lookup"><span data-stu-id="e38ab-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="e38ab-111">A dinamikus paraméterek nevének felfedezéséhez írjon be egy kötőjelet (-) a parancsmag neve után, majd a Tab billentyű többszöri lenyomása után lépkedhet a rendelkezésre álló paraméterek között.</span><span class="sxs-lookup"><span data-stu-id="e38ab-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="e38ab-112">Ha kihagy egy kötelező sablonparamétert, a parancsmag rákérdez az értékre.</span><span class="sxs-lookup"><span data-stu-id="e38ab-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="e38ab-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e38ab-113">EXAMPLES</span></span>

### <span data-ttu-id="e38ab-114">1. példa: Művelet lekérte egy logic app futtatásával</span><span class="sxs-lookup"><span data-stu-id="e38ab-114">Example 1: Get an action from a Logic App run</span></span>
```powershell
PS C:\>Get-AzLogicAppActionRun -ResourceGroupName "ResourceGroup11" -Name "LogicApp05" -RunName "LogicAppRun56" -ActionName "LogicAppAction01"
Code        : NotFound
EndTime     : 1/13/2016 2:42:56 PM
Error       : 
InputsLink  : Microsoft.Azure.Management.Logic.Models.ContentLink
Name        : LogicAppAction01
OutputsLink : Microsoft.Azure.Management.Logic.Models.ContentLink
StartTime   : 1/13/2016 2:42:55 PM
Status      : Failed
TrackingId  : 
Type        :
```

<span data-ttu-id="e38ab-115">Ez a parancs egy adott Logic App-műveletet kap a LogicApp05 nevű logikai appból a LogicAppRun56 nevű futtatáshoz.</span><span class="sxs-lookup"><span data-stu-id="e38ab-115">This command gets a specific Logic App action from the logic app named LogicApp05 for the run named LogicAppRun56.</span></span>

### <span data-ttu-id="e38ab-116">2. példa: Az összes művelet lekérte a Logic App futtatását</span><span class="sxs-lookup"><span data-stu-id="e38ab-116">Example 2: Get all the actions from a Logic App run</span></span>
```powershell
PS C:\>Get-AzLogicAppActionRun -ResourceGroupName "ResourceGroup11" -Name "LogicApp05" -RunName "LogicAppRun56"
Code        : NotFound
EndTime     : 1/13/2016 2:42:56 PM
Error       : 
InputsLink  : Microsoft.Azure.Management.Logic.Models.ContentLink
Name        : LogicAppAction1
OutputsLink : Microsoft.Azure.Management.Logic.Models.ContentLink
StartTime   : 1/13/2016 2:42:55 PM
Status      : Failed
TrackingId  : 
Type        :
```

<span data-ttu-id="e38ab-117">Ez a parancs a LogicApp05 nevű logikai alkalmazás LogicAppRun56 nevű futtatott műveletét beveszi.</span><span class="sxs-lookup"><span data-stu-id="e38ab-117">This command gets all Logic App actions from a run named LogicAppRun56 of a logic app named LogicApp05.</span></span>

### <span data-ttu-id="e38ab-118">3. példa</span><span class="sxs-lookup"><span data-stu-id="e38ab-118">Example 3</span></span>

<span data-ttu-id="e38ab-119">Ez a parancs a LogicApp05 nevű logikai alkalmazás LogicAppRun56 nevű futtatott műveletét beveszi.</span><span class="sxs-lookup"><span data-stu-id="e38ab-119">This command gets all Logic App actions from a run named LogicAppRun56 of a logic app named LogicApp05.</span></span> <span data-ttu-id="e38ab-120">(automatikusan generált)</span><span class="sxs-lookup"><span data-stu-id="e38ab-120">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Get-AzLogicAppRunAction -Name 'IntegrationAccount31' -ResourceGroupName MyResourceGroup -RunName '08587489104702792076'
```

## <span data-ttu-id="e38ab-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e38ab-121">PARAMETERS</span></span>

### <span data-ttu-id="e38ab-122">-ActionName</span><span class="sxs-lookup"><span data-stu-id="e38ab-122">-ActionName</span></span>
<span data-ttu-id="e38ab-123">Egy logikai appban futtatott művelet nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e38ab-123">Specifies the name of an action in a logic app run.</span></span>
<span data-ttu-id="e38ab-124">Ez a parancsmag a paraméter által megadott műveletet kapja meg.</span><span class="sxs-lookup"><span data-stu-id="e38ab-124">This cmdlet gets the action that this parameter specifies.</span></span>

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

### <span data-ttu-id="e38ab-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e38ab-125">-DefaultProfile</span></span>
<span data-ttu-id="e38ab-126">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="e38ab-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e38ab-127">-Name</span><span class="sxs-lookup"><span data-stu-id="e38ab-127">-Name</span></span>
<span data-ttu-id="e38ab-128">Annak a logikai alkalmazásnak a nevét adja meg, amelyhez a parancsmag műveletet kap.</span><span class="sxs-lookup"><span data-stu-id="e38ab-128">Specifies the name of a logic app for which this cmdlet gets an action.</span></span>

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

### <span data-ttu-id="e38ab-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e38ab-129">-ResourceGroupName</span></span>
<span data-ttu-id="e38ab-130">Annak az erőforráscsoportnak a nevét adja meg, amelyben a parancsmag műveletet kap.</span><span class="sxs-lookup"><span data-stu-id="e38ab-130">Specifies the name of a resource group in which this cmdlet gets an action.</span></span>

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

### <span data-ttu-id="e38ab-131">-RunName</span><span class="sxs-lookup"><span data-stu-id="e38ab-131">-RunName</span></span>
<span data-ttu-id="e38ab-132">Logikai alkalmazás futtatásának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e38ab-132">Specifies the name of a run of a logic app.</span></span>
<span data-ttu-id="e38ab-133">Ez a parancsmag egy műveletet kap a paraméter által megadott futtatáshoz.</span><span class="sxs-lookup"><span data-stu-id="e38ab-133">This cmdlet gets an action for the run that this parameter specifies.</span></span>

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

### <span data-ttu-id="e38ab-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e38ab-134">CommonParameters</span></span>
<span data-ttu-id="e38ab-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e38ab-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e38ab-136">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e38ab-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e38ab-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e38ab-137">INPUTS</span></span>

### <span data-ttu-id="e38ab-138">System.String</span><span class="sxs-lookup"><span data-stu-id="e38ab-138">System.String</span></span>

## <span data-ttu-id="e38ab-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e38ab-139">OUTPUTS</span></span>

### <span data-ttu-id="e38ab-140">Microsoft.Azure.Management.Logic.Models.WorkflowRunAction</span><span class="sxs-lookup"><span data-stu-id="e38ab-140">Microsoft.Azure.Management.Logic.Models.WorkflowRunAction</span></span>

## <span data-ttu-id="e38ab-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e38ab-141">NOTES</span></span>

## <span data-ttu-id="e38ab-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e38ab-142">RELATED LINKS</span></span>

[<span data-ttu-id="e38ab-143">Get-AzRunAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="e38ab-143">Get-AzLogicAppRunHistory</span></span>](./Get-AzLogicAppRunHistory.md)

[<span data-ttu-id="e38ab-144">Stop-AzRunAppRun</span><span class="sxs-lookup"><span data-stu-id="e38ab-144">Stop-AzLogicAppRun</span></span>](./Stop-AzLogicAppRun.md)


