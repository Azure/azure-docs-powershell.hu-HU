---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: C1F6BBF9-0DB5-46FD-B8A8-9029B0AB6166
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicAppTriggerHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicAppTriggerHistory.md
ms.openlocfilehash: 23ccef6dedf1a0be0f7d7cf1b565c936e76a0309
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679430"
---
# <span data-ttu-id="81ed4-101">Get-AzureRmLogicAppTriggerHistory</span><span class="sxs-lookup"><span data-stu-id="81ed4-101">Get-AzureRmLogicAppTriggerHistory</span></span>

## <span data-ttu-id="81ed4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="81ed4-102">SYNOPSIS</span></span>
<span data-ttu-id="81ed4-103">Egy logikai alkalmazásban kapja meg az eseményindítók előzményeit.</span><span class="sxs-lookup"><span data-stu-id="81ed4-103">Gets the history of triggers in a logic app.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="81ed4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="81ed4-104">SYNTAX</span></span>

```
Get-AzureRmLogicAppTriggerHistory -ResourceGroupName <String> -Name <String> -TriggerName <String>
 [-HistoryName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="81ed4-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="81ed4-105">DESCRIPTION</span></span>
<span data-ttu-id="81ed4-106">A **Get-AzureRmLogicAppTriggerHistory** parancsmag az eseményindítók előzményeit a logikai alkalmazások funkcióban egy logikai alkalmazásban kapja meg.</span><span class="sxs-lookup"><span data-stu-id="81ed4-106">The **Get-AzureRmLogicAppTriggerHistory** cmdlet gets the history of triggers in a logic app in the Logic Apps feature.</span></span>
<span data-ttu-id="81ed4-107">Ez a parancsmag egy **WorkflowTriggerHistory** objektumot ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="81ed4-107">This cmdlet returns a **WorkflowTriggerHistory** object.</span></span>
<span data-ttu-id="81ed4-108">Adja meg a logikai alkalmazást, az erőforráscsoportot és az triggert.</span><span class="sxs-lookup"><span data-stu-id="81ed4-108">Specify the logic app, resource group, and trigger.</span></span>

<span data-ttu-id="81ed4-109">Ez a modul támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="81ed4-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="81ed4-110">Ha dinamikus paramétert szeretne használni, írja be azt a parancsba.</span><span class="sxs-lookup"><span data-stu-id="81ed4-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="81ed4-111">A dinamikus paraméterek nevének feltárásához írjon be egy kötőjelet (-) a parancsmag neve után, majd nyomja le többször a TAB billentyűt a rendelkezésre álló paraméterek közötti váltáshoz.</span><span class="sxs-lookup"><span data-stu-id="81ed4-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="81ed4-112">Ha kihagyja a szükséges sablon paramétert, a parancsmag kéri az érték megadását.</span><span class="sxs-lookup"><span data-stu-id="81ed4-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="81ed4-113">Példák</span><span class="sxs-lookup"><span data-stu-id="81ed4-113">EXAMPLES</span></span>

### <span data-ttu-id="81ed4-114">Példa 1: egy logikai app trigger-előzményeinek beszerzése</span><span class="sxs-lookup"><span data-stu-id="81ed4-114">Example 1: Get a trigger history of a logic app</span></span>
```
PS C:\>Get-AzureRmLogicAppTriggerHistory -ResourceGroupName "Resourcegroup11" -Name "LogicApp03" -TriggerName "Trigger01" -HistoryName "08587489107387695768"
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

<span data-ttu-id="81ed4-115">Ez a parancs a LogicApp03 nevű logikai alkalmazásban meghatározott logikai alkalmazási előzményeket hoz létre a triggerekhez.</span><span class="sxs-lookup"><span data-stu-id="81ed4-115">This command gets a specific logic app trigger history for a trigger in the logic app named LogicApp03.</span></span>

### <span data-ttu-id="81ed4-116">2. példa: egy logikai app indító előzményeinek beszerzése</span><span class="sxs-lookup"><span data-stu-id="81ed4-116">Example 2: Get trigger histories of a logic app</span></span>
```
PS C:\>Get-AzureRmLogicAppTriggerHistory -ResourceGroupName "ResourceGroup11" -Name "LogicApp07" -TriggerName "Trigger01"
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

<span data-ttu-id="81ed4-117">Ez a parancs a LogicApp07 nevű logikai app trigger-előzményeit kapja.</span><span class="sxs-lookup"><span data-stu-id="81ed4-117">This command gets the workflow trigger histories for a trigger in the logic app named LogicApp07.</span></span>

## <span data-ttu-id="81ed4-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="81ed4-118">PARAMETERS</span></span>

### <span data-ttu-id="81ed4-119">-HistoryName</span><span class="sxs-lookup"><span data-stu-id="81ed4-119">-HistoryName</span></span>
<span data-ttu-id="81ed4-120">Itt adhatja meg annak az előzményeinek a nevét, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="81ed4-120">Specifies the name of the history that this cmdlet gets.</span></span>

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

### <span data-ttu-id="81ed4-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="81ed4-121">-Name</span></span>
<span data-ttu-id="81ed4-122">Annak a logikai alkalmazásnak a nevét adja meg, amelyhez ez a parancsmag a trigger-előzményeket kapja.</span><span class="sxs-lookup"><span data-stu-id="81ed4-122">Specifies the name of the logic app for which this cmdlet gets trigger history.</span></span>

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

### <span data-ttu-id="81ed4-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81ed4-123">-ResourceGroupName</span></span>
<span data-ttu-id="81ed4-124">Annak az erőforrás csoportnak a nevét adja meg, amelyben a parancsmag előzményeit kapja.</span><span class="sxs-lookup"><span data-stu-id="81ed4-124">Specifies the name of the resource group in which this cmdlet gets history.</span></span>

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

### <span data-ttu-id="81ed4-125">-TriggerName</span><span class="sxs-lookup"><span data-stu-id="81ed4-125">-TriggerName</span></span>
<span data-ttu-id="81ed4-126">Annak az indítónak a neve, amelyhez ez a parancsmag az előzményeket kapja.</span><span class="sxs-lookup"><span data-stu-id="81ed4-126">Specifies the name of the trigger for which this cmdlet gets history.</span></span>

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

### <span data-ttu-id="81ed4-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81ed4-127">-DefaultProfile</span></span>
<span data-ttu-id="81ed4-128">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="81ed4-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81ed4-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81ed4-129">CommonParameters</span></span>
<span data-ttu-id="81ed4-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="81ed4-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81ed4-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81ed4-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81ed4-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="81ed4-132">INPUTS</span></span>

## <span data-ttu-id="81ed4-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="81ed4-133">OUTPUTS</span></span>

### <span data-ttu-id="81ed4-134">Microsoft. Azure. Management. Logic. models. WorkflowTriggerHistory</span><span class="sxs-lookup"><span data-stu-id="81ed4-134">Microsoft.Azure.Management.Logic.Models.WorkflowTriggerHistory</span></span>

## <span data-ttu-id="81ed4-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="81ed4-135">NOTES</span></span>

## <span data-ttu-id="81ed4-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="81ed4-136">RELATED LINKS</span></span>

[<span data-ttu-id="81ed4-137">Get-AzureRmLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="81ed4-137">Get-AzureRmLogicAppRunHistory</span></span>](./Get-AzureRmLogicAppRunHistory.md)

[<span data-ttu-id="81ed4-138">Get-AzureRmLogicAppTrigger</span><span class="sxs-lookup"><span data-stu-id="81ed4-138">Get-AzureRmLogicAppTrigger</span></span>](./Get-AzureRmLogicAppTrigger.md)

[<span data-ttu-id="81ed4-139">Start-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="81ed4-139">Start-AzureRmLogicApp</span></span>](./Start-AzureRmLogicApp.md)


