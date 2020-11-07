---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: C1F6BBF9-0DB5-46FD-B8A8-9029B0AB6166
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azlogicapptriggerhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppTriggerHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppTriggerHistory.md
ms.openlocfilehash: f9283ce587baebb4050bda6d901cf0cf9eab9f81
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666063"
---
# <span data-ttu-id="35177-101">Get-AzLogicAppTriggerHistory</span><span class="sxs-lookup"><span data-stu-id="35177-101">Get-AzLogicAppTriggerHistory</span></span>

## <span data-ttu-id="35177-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="35177-102">SYNOPSIS</span></span>
<span data-ttu-id="35177-103">Egy logikai alkalmazásban kapja meg az eseményindítók előzményeit.</span><span class="sxs-lookup"><span data-stu-id="35177-103">Gets the history of triggers in a logic app.</span></span>

## <span data-ttu-id="35177-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="35177-104">SYNTAX</span></span>

```
Get-AzLogicAppTriggerHistory -ResourceGroupName <String> -Name <String> -TriggerName <String>
 [-HistoryName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="35177-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="35177-105">DESCRIPTION</span></span>
<span data-ttu-id="35177-106">A **Get-AzLogicAppTriggerHistory** parancsmag az eseményindítók előzményeit a logikai alkalmazások funkcióban egy logikai alkalmazásban kapja meg.</span><span class="sxs-lookup"><span data-stu-id="35177-106">The **Get-AzLogicAppTriggerHistory** cmdlet gets the history of triggers in a logic app in the Logic Apps feature.</span></span>
<span data-ttu-id="35177-107">Ez a parancsmag egy **WorkflowTriggerHistory** objektumot ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="35177-107">This cmdlet returns a **WorkflowTriggerHistory** object.</span></span>
<span data-ttu-id="35177-108">Adja meg a logikai alkalmazást, az erőforráscsoportot és az triggert.</span><span class="sxs-lookup"><span data-stu-id="35177-108">Specify the logic app, resource group, and trigger.</span></span>
<span data-ttu-id="35177-109">Ez a modul támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="35177-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="35177-110">Ha dinamikus paramétert szeretne használni, írja be azt a parancsba.</span><span class="sxs-lookup"><span data-stu-id="35177-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="35177-111">A dinamikus paraméterek nevének feltárásához írjon be egy kötőjelet (-) a parancsmag neve után, majd nyomja le többször a TAB billentyűt a rendelkezésre álló paraméterek közötti váltáshoz.</span><span class="sxs-lookup"><span data-stu-id="35177-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="35177-112">Ha kihagyja a szükséges sablon paramétert, a parancsmag kéri az érték megadását.</span><span class="sxs-lookup"><span data-stu-id="35177-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="35177-113">Példák</span><span class="sxs-lookup"><span data-stu-id="35177-113">EXAMPLES</span></span>

### <span data-ttu-id="35177-114">Példa 1: egy logikai app trigger-előzményeinek beszerzése</span><span class="sxs-lookup"><span data-stu-id="35177-114">Example 1: Get a trigger history of a logic app</span></span>
```
PS C:\>Get-AzLogicAppTriggerHistory -ResourceGroupName "Resourcegroup11" -Name "LogicApp03" -TriggerName "Trigger01" -HistoryName "08587489107387695768"
Code        : BadRequest
EndTime     : 1/13/2016 2:42:26 PM
Error       : {code, message}
Fired       : False
InputsLink  : https://flowprodcu02by01.blob.core.windows.net/flow3ea9ffd11c684c9f9f258b1a6ea5cb6020160113t000000zcontent/A7392_d1e831de68ac4ef89d19a40f05e663
              cb_httpTrigger:5Finputs:2Ejson?sv=2014-02-14&sr=b&sig=&se=2016-01-14T16%3A15%3A16Z&sp=r
Name        : 08587489107387695768
OutputsLink : 
Run         : 
StartTime   : 1/13/2016 2:42:26 PM
Status      : Failed
TrackingId  : f88a499b-f80f-4a28-9bbf-c4cc0d129700
Type        : Microsoft.Logic/workflows/triggers/histories
```

<span data-ttu-id="35177-115">Ez a parancs a LogicApp03 nevű logikai alkalmazásban meghatározott logikai alkalmazási előzményeket hoz létre a triggerekhez.</span><span class="sxs-lookup"><span data-stu-id="35177-115">This command gets a specific logic app trigger history for a trigger in the logic app named LogicApp03.</span></span>

### <span data-ttu-id="35177-116">2. példa: egy logikai app indító előzményeinek beszerzése</span><span class="sxs-lookup"><span data-stu-id="35177-116">Example 2: Get trigger histories of a logic app</span></span>
```
PS C:\>Get-AzLogicAppTriggerHistory -ResourceGroupName "ResourceGroup11" -Name "LogicApp07" -TriggerName "Trigger01"
Code        : BadRequest
EndTime     : 1/13/2016 2:43:33 PM
Error       : {code, message}
Fired       : False
InputsLink  : https://flowprodcu02by01.blob.core.windows.net/flow3ea9ffd11c684c9f9f258b1a6ea5cb6020160113t000000zcontent/CAB46_60e2ad0f0e1947e8b5798716914c5d
              b6_httpTrigger:5Finputs:2Ejson?sv=2014-02-14&sr=b&sig=&se=2016-01-14T16%3A18%3A27Z&sp=r
Name        : 08587489106716457817
OutputsLink : 
Run         : 
StartTime   : 1/13/2016 2:43:33 PM
Status      : Failed
TrackingId  : c91a63f1-48b4-4eae-91eb-8f6dbfa9fe06
Type        : Microsoft.Logic/workflows/triggers/histories

Code        : BadRequest
EndTime     : 1/13/2016 2:42:26 PM
Error       : {code, message}
Fired       : False
InputsLink  : https://flowprodcu02by01.blob.core.windows.net/flow3ea9ffd11c684c9f9f258b1a6ea5cb6020160113t000000zcontent/A7392_d1e831de68ac4ef89d19a40f05e663
              cb_httpTrigger:5Finputs:2Ejson?sv=2014-02-14&sr=b&sig=&se=2016-01-14T16%3A18%3A27Z&sp=r
Name        : 08587489107387695768
OutputsLink : 
Run         : 
StartTime   : 1/13/2016 2:42:26 PM
Status      : Failed
TrackingId  : f88a499b-f80f-4a28-9bbf-c4cc0d129700
Type        : Microsoft.Logic/workflows/triggers/histories
```

<span data-ttu-id="35177-117">Ez a parancs a LogicApp07 nevű logikai app trigger-előzményeit kapja.</span><span class="sxs-lookup"><span data-stu-id="35177-117">This command gets the workflow trigger histories for a trigger in the logic app named LogicApp07.</span></span>

## <span data-ttu-id="35177-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="35177-118">PARAMETERS</span></span>

### <span data-ttu-id="35177-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35177-119">-DefaultProfile</span></span>
<span data-ttu-id="35177-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="35177-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="35177-121">-HistoryName</span><span class="sxs-lookup"><span data-stu-id="35177-121">-HistoryName</span></span>
<span data-ttu-id="35177-122">Itt adhatja meg annak az előzményeinek a nevét, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="35177-122">Specifies the name of the history that this cmdlet gets.</span></span>

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

### <span data-ttu-id="35177-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="35177-123">-Name</span></span>
<span data-ttu-id="35177-124">Annak a logikai alkalmazásnak a nevét adja meg, amelyhez ez a parancsmag a trigger-előzményeket kapja.</span><span class="sxs-lookup"><span data-stu-id="35177-124">Specifies the name of the logic app for which this cmdlet gets trigger history.</span></span>

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

### <span data-ttu-id="35177-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35177-125">-ResourceGroupName</span></span>
<span data-ttu-id="35177-126">Annak az erőforrás csoportnak a nevét adja meg, amelyben a parancsmag előzményeit kapja.</span><span class="sxs-lookup"><span data-stu-id="35177-126">Specifies the name of the resource group in which this cmdlet gets history.</span></span>

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

### <span data-ttu-id="35177-127">-TriggerName</span><span class="sxs-lookup"><span data-stu-id="35177-127">-TriggerName</span></span>
<span data-ttu-id="35177-128">Annak az indítónak a neve, amelyhez ez a parancsmag az előzményeket kapja.</span><span class="sxs-lookup"><span data-stu-id="35177-128">Specifies the name of the trigger for which this cmdlet gets history.</span></span>

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

### <span data-ttu-id="35177-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35177-129">CommonParameters</span></span>
<span data-ttu-id="35177-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="35177-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35177-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35177-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35177-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="35177-132">INPUTS</span></span>

### <span data-ttu-id="35177-133">System. String</span><span class="sxs-lookup"><span data-stu-id="35177-133">System.String</span></span>

## <span data-ttu-id="35177-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="35177-134">OUTPUTS</span></span>

### <span data-ttu-id="35177-135">Microsoft. Azure. Management. Logic. models. WorkflowTriggerHistory</span><span class="sxs-lookup"><span data-stu-id="35177-135">Microsoft.Azure.Management.Logic.Models.WorkflowTriggerHistory</span></span>

## <span data-ttu-id="35177-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="35177-136">NOTES</span></span>

## <span data-ttu-id="35177-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="35177-137">RELATED LINKS</span></span>

[<span data-ttu-id="35177-138">Get-AzLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="35177-138">Get-AzLogicAppRunHistory</span></span>](./Get-AzLogicAppRunHistory.md)

[<span data-ttu-id="35177-139">Get-AzLogicAppTrigger</span><span class="sxs-lookup"><span data-stu-id="35177-139">Get-AzLogicAppTrigger</span></span>](./Get-AzLogicAppTrigger.md)

[<span data-ttu-id="35177-140">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="35177-140">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)


