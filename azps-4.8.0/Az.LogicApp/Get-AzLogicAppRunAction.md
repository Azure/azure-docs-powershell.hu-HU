---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 2EA28B90-4BAE-45DF-BD2E-60C74F53FB7B
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azlogicapprunaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppRunAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppRunAction.md
ms.openlocfilehash: c382b4bb9a02150beaa6880fd88d8f7b376b7c34
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181832"
---
# <span data-ttu-id="14180-101">Get-AzLogicAppRunAction</span><span class="sxs-lookup"><span data-stu-id="14180-101">Get-AzLogicAppRunAction</span></span>

## <span data-ttu-id="14180-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="14180-102">SYNOPSIS</span></span>
<span data-ttu-id="14180-103">Egy logikai app futásának műveletét kapja.</span><span class="sxs-lookup"><span data-stu-id="14180-103">Gets an action from a logic app run.</span></span>

## <span data-ttu-id="14180-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="14180-104">SYNTAX</span></span>

```
Get-AzLogicAppRunAction -ResourceGroupName <String> -Name <String> -RunName <String> [-ActionName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="14180-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="14180-105">DESCRIPTION</span></span>
<span data-ttu-id="14180-106">A **Get-AzLogicAppRunAction** parancsmag egy logikai app futtatását követően kapja meg a műveletsort.</span><span class="sxs-lookup"><span data-stu-id="14180-106">The **Get-AzLogicAppRunAction** cmdlet gets an action from a logic app run.</span></span>
<span data-ttu-id="14180-107">Ez a parancsmag **WorkflowRunAction** -objektumokat ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="14180-107">This cmdlet returns a **WorkflowRunAction** objects.</span></span>
<span data-ttu-id="14180-108">Adja meg a logikai alkalmazást, az erőforrás csoportot és a futtatást.</span><span class="sxs-lookup"><span data-stu-id="14180-108">Specify the logic app, resource group, and run.</span></span>
<span data-ttu-id="14180-109">Ez a modul támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="14180-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="14180-110">Ha dinamikus paramétert szeretne használni, írja be azt a parancsba.</span><span class="sxs-lookup"><span data-stu-id="14180-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="14180-111">A dinamikus paraméterek nevének feltárásához írjon be egy kötőjelet (-) a parancsmag neve után, majd nyomja le többször a TAB billentyűt a rendelkezésre álló paraméterek közötti váltáshoz.</span><span class="sxs-lookup"><span data-stu-id="14180-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="14180-112">Ha kihagyja a szükséges sablon paramétert, a parancsmag kéri az érték megadását.</span><span class="sxs-lookup"><span data-stu-id="14180-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="14180-113">Példák</span><span class="sxs-lookup"><span data-stu-id="14180-113">EXAMPLES</span></span>

### <span data-ttu-id="14180-114">Példa 1: művelet beszerzése logikai alkalmazásból</span><span class="sxs-lookup"><span data-stu-id="14180-114">Example 1: Get an action from a Logic App run</span></span>
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

<span data-ttu-id="14180-115">Ez a parancs a LogicApp05 nevű LogicAppRun56 nevű logikai app konkrét logikával kapcsolatos műveletét kapja.</span><span class="sxs-lookup"><span data-stu-id="14180-115">This command gets a specific Logic App action from the logic app named LogicApp05 for the run named LogicAppRun56.</span></span>

### <span data-ttu-id="14180-116">2. példa: a logikai alkalmazások által futtatott összes művelet beolvasása</span><span class="sxs-lookup"><span data-stu-id="14180-116">Example 2: Get all the actions from a Logic App run</span></span>
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

<span data-ttu-id="14180-117">Ez a parancs a LogicApp05 nevű logikai app Run nevű LogicAppRun56 minden logikai app-műveletet beolvassa.</span><span class="sxs-lookup"><span data-stu-id="14180-117">This command gets all Logic App actions from a run named LogicAppRun56 of a logic app named LogicApp05.</span></span>

### <span data-ttu-id="14180-118">3. példa</span><span class="sxs-lookup"><span data-stu-id="14180-118">Example 3</span></span>

<span data-ttu-id="14180-119">Ez a parancs a LogicApp05 nevű logikai app Run nevű LogicAppRun56 minden logikai app-műveletet beolvassa.</span><span class="sxs-lookup"><span data-stu-id="14180-119">This command gets all Logic App actions from a run named LogicAppRun56 of a logic app named LogicApp05.</span></span> <span data-ttu-id="14180-120">autogenerated</span><span class="sxs-lookup"><span data-stu-id="14180-120">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Get-AzLogicAppRunAction -Name 'IntegrationAccount31' -ResourceGroupName MyResourceGroup -RunName '08587489104702792076'
```

## <span data-ttu-id="14180-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="14180-121">PARAMETERS</span></span>

### <span data-ttu-id="14180-122">-ActionName</span><span class="sxs-lookup"><span data-stu-id="14180-122">-ActionName</span></span>
<span data-ttu-id="14180-123">Egy logikai alkalmazásban futtatott művelet nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="14180-123">Specifies the name of an action in a logic app run.</span></span>
<span data-ttu-id="14180-124">Ez a parancsmag a paraméter által megadott műveleteket kapja meg.</span><span class="sxs-lookup"><span data-stu-id="14180-124">This cmdlet gets the action that this parameter specifies.</span></span>

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

### <span data-ttu-id="14180-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14180-125">-DefaultProfile</span></span>
<span data-ttu-id="14180-126">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="14180-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="14180-127">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="14180-127">-Name</span></span>
<span data-ttu-id="14180-128">Annak a logikai alkalmazásnak a nevét adja meg, amelyhez ez a parancsmag a műveleteket kapja.</span><span class="sxs-lookup"><span data-stu-id="14180-128">Specifies the name of a logic app for which this cmdlet gets an action.</span></span>

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

### <span data-ttu-id="14180-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14180-129">-ResourceGroupName</span></span>
<span data-ttu-id="14180-130">Annak a csoportnak a nevét adja meg, amelyben ez a parancsmag egy művelethez jut.</span><span class="sxs-lookup"><span data-stu-id="14180-130">Specifies the name of a resource group in which this cmdlet gets an action.</span></span>

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

### <span data-ttu-id="14180-131">-RunName</span><span class="sxs-lookup"><span data-stu-id="14180-131">-RunName</span></span>
<span data-ttu-id="14180-132">A logikai alkalmazás futtatásának a nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="14180-132">Specifies the name of a run of a logic app.</span></span>
<span data-ttu-id="14180-133">Ez a parancsmag a paraméter által megadott futtatási műveletre ad lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="14180-133">This cmdlet gets an action for the run that this parameter specifies.</span></span>

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

### <span data-ttu-id="14180-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14180-134">CommonParameters</span></span>
<span data-ttu-id="14180-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="14180-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14180-136">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14180-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14180-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="14180-137">INPUTS</span></span>

### <span data-ttu-id="14180-138">System. String</span><span class="sxs-lookup"><span data-stu-id="14180-138">System.String</span></span>

## <span data-ttu-id="14180-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="14180-139">OUTPUTS</span></span>

### <span data-ttu-id="14180-140">Microsoft. Azure. Management. Logic. models. WorkflowRunAction</span><span class="sxs-lookup"><span data-stu-id="14180-140">Microsoft.Azure.Management.Logic.Models.WorkflowRunAction</span></span>

## <span data-ttu-id="14180-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="14180-141">NOTES</span></span>

## <span data-ttu-id="14180-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="14180-142">RELATED LINKS</span></span>

[<span data-ttu-id="14180-143">Get-AzLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="14180-143">Get-AzLogicAppRunHistory</span></span>](./Get-AzLogicAppRunHistory.md)

[<span data-ttu-id="14180-144">Stop-AzLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="14180-144">Stop-AzLogicAppRun</span></span>](./Stop-AzLogicAppRun.md)


