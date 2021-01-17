---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: C1F6BBF9-0DB5-46FD-B8A8-9029B0AB6166
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azlogicapptriggerhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppTriggerHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppTriggerHistory.md
ms.openlocfilehash: d20d6ba980b424109e33fd4380eec9be4f7728ee
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98386174"
---
# <span data-ttu-id="93fa1-101">Get-AzLogicAppTriggerHistory</span><span class="sxs-lookup"><span data-stu-id="93fa1-101">Get-AzLogicAppTriggerHistory</span></span>

## <span data-ttu-id="93fa1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="93fa1-102">SYNOPSIS</span></span>
<span data-ttu-id="93fa1-103">Logikai appban lejátsa az eseményindítók előzményeit.</span><span class="sxs-lookup"><span data-stu-id="93fa1-103">Gets the history of triggers in a logic app.</span></span>

## <span data-ttu-id="93fa1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="93fa1-104">SYNTAX</span></span>

```
Get-AzLogicAppTriggerHistory -ResourceGroupName <String> -Name <String> -TriggerName <String>
 [-HistoryName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="93fa1-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="93fa1-105">DESCRIPTION</span></span>
<span data-ttu-id="93fa1-106">A **Get-Az LogicAppTriggerHistory** parancsmag az eseményindítók előzményeit a Logic Apps funkció logikai appjában kapja meg.</span><span class="sxs-lookup"><span data-stu-id="93fa1-106">The **Get-AzLogicAppTriggerHistory** cmdlet gets the history of triggers in a logic app in the Logic Apps feature.</span></span>
<span data-ttu-id="93fa1-107">Ez a parancsmag **egy WorkflowTriggerHistory objektumot** ad vissza.</span><span class="sxs-lookup"><span data-stu-id="93fa1-107">This cmdlet returns a **WorkflowTriggerHistory** object.</span></span>
<span data-ttu-id="93fa1-108">Adja meg a logikai alkalmazást, az erőforráscsoportot és az eseményindítót.</span><span class="sxs-lookup"><span data-stu-id="93fa1-108">Specify the logic app, resource group, and trigger.</span></span>
<span data-ttu-id="93fa1-109">Ez a modul támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="93fa1-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="93fa1-110">Ha dinamikus paramétert használ, írja be a parancsba.</span><span class="sxs-lookup"><span data-stu-id="93fa1-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="93fa1-111">A dinamikus paraméterek nevének felfedezéséhez írjon be egy kötőjelet (-) a parancsmag neve után, majd a Tab billentyű többszöri lenyomása után lépkedhet a rendelkezésre álló paraméterek között.</span><span class="sxs-lookup"><span data-stu-id="93fa1-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="93fa1-112">Ha kihagy egy kötelező sablonparamétert, a parancsmag rákérdez az értékre.</span><span class="sxs-lookup"><span data-stu-id="93fa1-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="93fa1-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="93fa1-113">EXAMPLES</span></span>

### <span data-ttu-id="93fa1-114">1. példa: Logikai alkalmazás eseményindító előzményeinek lekérte</span><span class="sxs-lookup"><span data-stu-id="93fa1-114">Example 1: Get a trigger history of a logic app</span></span>
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

<span data-ttu-id="93fa1-115">Ez a parancs egy adott logic app eseményindító előzményeit kapja a LogicApp03 nevű logikai appban.</span><span class="sxs-lookup"><span data-stu-id="93fa1-115">This command gets a specific logic app trigger history for a trigger in the logic app named LogicApp03.</span></span>

### <span data-ttu-id="93fa1-116">2. példa: Logikai alkalmazás eseményindító-történetének lekérte</span><span class="sxs-lookup"><span data-stu-id="93fa1-116">Example 2: Get trigger histories of a logic app</span></span>
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

<span data-ttu-id="93fa1-117">Ez a parancs lekérte a LogicApp07 nevű logikai alkalmazás egyik eseményindítójának munkafolyamat-eseményindítóját.</span><span class="sxs-lookup"><span data-stu-id="93fa1-117">This command gets the workflow trigger histories for a trigger in the logic app named LogicApp07.</span></span>

## <span data-ttu-id="93fa1-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="93fa1-118">PARAMETERS</span></span>

### <span data-ttu-id="93fa1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93fa1-119">-DefaultProfile</span></span>
<span data-ttu-id="93fa1-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="93fa1-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="93fa1-121">-HistoryName</span><span class="sxs-lookup"><span data-stu-id="93fa1-121">-HistoryName</span></span>
<span data-ttu-id="93fa1-122">A parancsmag által lekért előzmények neve.</span><span class="sxs-lookup"><span data-stu-id="93fa1-122">Specifies the name of the history that this cmdlet gets.</span></span>

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

### <span data-ttu-id="93fa1-123">-Name</span><span class="sxs-lookup"><span data-stu-id="93fa1-123">-Name</span></span>
<span data-ttu-id="93fa1-124">Annak a logikai alkalmazásnak a nevét adja meg, amelyhez ez a parancsmag eseményindító előzményeket kap.</span><span class="sxs-lookup"><span data-stu-id="93fa1-124">Specifies the name of the logic app for which this cmdlet gets trigger history.</span></span>

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

### <span data-ttu-id="93fa1-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93fa1-125">-ResourceGroupName</span></span>
<span data-ttu-id="93fa1-126">Annak az erőforráscsoportnak a nevét adja meg, amelyben a parancsmag előzményt kap.</span><span class="sxs-lookup"><span data-stu-id="93fa1-126">Specifies the name of the resource group in which this cmdlet gets history.</span></span>

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

### <span data-ttu-id="93fa1-127">-TriggerName</span><span class="sxs-lookup"><span data-stu-id="93fa1-127">-TriggerName</span></span>
<span data-ttu-id="93fa1-128">Annak az eseményindítónak a nevét adja meg, amelyhez a parancsmag előzményt kap.</span><span class="sxs-lookup"><span data-stu-id="93fa1-128">Specifies the name of the trigger for which this cmdlet gets history.</span></span>

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

### <span data-ttu-id="93fa1-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93fa1-129">CommonParameters</span></span>
<span data-ttu-id="93fa1-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93fa1-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93fa1-131">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93fa1-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93fa1-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="93fa1-132">INPUTS</span></span>

### <span data-ttu-id="93fa1-133">System.String</span><span class="sxs-lookup"><span data-stu-id="93fa1-133">System.String</span></span>

## <span data-ttu-id="93fa1-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="93fa1-134">OUTPUTS</span></span>

### <span data-ttu-id="93fa1-135">Microsoft.Azure.Management.Logic.Models.WorkflowTriggerHistory</span><span class="sxs-lookup"><span data-stu-id="93fa1-135">Microsoft.Azure.Management.Logic.Models.WorkflowTriggerHistory</span></span>

## <span data-ttu-id="93fa1-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="93fa1-136">NOTES</span></span>

## <span data-ttu-id="93fa1-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="93fa1-137">RELATED LINKS</span></span>

[<span data-ttu-id="93fa1-138">Get-AzRunAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="93fa1-138">Get-AzLogicAppRunHistory</span></span>](./Get-AzLogicAppRunHistory.md)

[<span data-ttu-id="93fa1-139">Get-AzAppTrigger</span><span class="sxs-lookup"><span data-stu-id="93fa1-139">Get-AzLogicAppTrigger</span></span>](./Get-AzLogicAppTrigger.md)

[<span data-ttu-id="93fa1-140">Start-AzApp</span><span class="sxs-lookup"><span data-stu-id="93fa1-140">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)


