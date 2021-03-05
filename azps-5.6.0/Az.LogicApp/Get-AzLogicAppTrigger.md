---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 5307F1F1-E84C-4949-A557-99EF0012C3DF
online version: https://docs.microsoft.com/powershell/module/az.logicapp/get-azlogicapptrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppTrigger.md
ms.openlocfilehash: 28a7cd76f03dd3b6d2fc79e5d0b8d4d963a7f55c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008933"
---
# <span data-ttu-id="f9cb9-101">Get-AzLogicAppTrigger</span><span class="sxs-lookup"><span data-stu-id="f9cb9-101">Get-AzLogicAppTrigger</span></span>

## <span data-ttu-id="f9cb9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f9cb9-102">SYNOPSIS</span></span>
<span data-ttu-id="f9cb9-103">Egy logikai alkalmazás eseményindítóit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="f9cb9-103">Gets the triggers of a logic app.</span></span>

## <span data-ttu-id="f9cb9-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f9cb9-104">SYNTAX</span></span>

```
Get-AzLogicAppTrigger -ResourceGroupName <String> -Name <String> [-TriggerName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f9cb9-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f9cb9-105">DESCRIPTION</span></span>
<span data-ttu-id="f9cb9-106">A **Get-Az LogicAppTrigger parancsmag** triggereket kap egy logikai alkalmazásból.</span><span class="sxs-lookup"><span data-stu-id="f9cb9-106">The **Get-AzLogicAppTrigger** cmdlet gets triggers from a logic app.</span></span>
<span data-ttu-id="f9cb9-107">Ez a parancsmag **egy WorkflowTrigger-objektumot** ad vissza.</span><span class="sxs-lookup"><span data-stu-id="f9cb9-107">This cmdlet returns a **WorkflowTrigger** object.</span></span>
<span data-ttu-id="f9cb9-108">Adja meg a munkafolyamatot, az erőforráscsoportot és az eseményindítót.</span><span class="sxs-lookup"><span data-stu-id="f9cb9-108">Specify the workflow, resource group, and trigger.</span></span>
<span data-ttu-id="f9cb9-109">Ez a modul támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="f9cb9-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="f9cb9-110">Ha dinamikus paramétert használ, írja be a parancsba.</span><span class="sxs-lookup"><span data-stu-id="f9cb9-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="f9cb9-111">A dinamikus paraméterek nevének felfedezéséhez írjon be egy kötőjelet (-) a parancsmag neve után, majd a Tab billentyű többszöri lenyomása után lépkedhet a rendelkezésre álló paraméterek között.</span><span class="sxs-lookup"><span data-stu-id="f9cb9-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="f9cb9-112">Ha kihagy egy kötelező sablonparamétert, a parancsmag rákérdez az értékre.</span><span class="sxs-lookup"><span data-stu-id="f9cb9-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="f9cb9-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f9cb9-113">EXAMPLES</span></span>

### <span data-ttu-id="f9cb9-114">1. példa: Logikai alkalmazás kiváltása</span><span class="sxs-lookup"><span data-stu-id="f9cb9-114">Example 1: Get a trigger of a logic app</span></span>
```
PS C:\>Get-AzLogicAppTrigger -ResourceGroupName "ResourceGroup11" -Name "LogicApp05" -TriggerName "Trigger01"
ChangedTime         : 1/14/2016 11:45:07 AM
CreatedTime         : 1/13/2016 2:42:26 PM
LastExecutionTime   : 1/14/2016 11:45:07 AM
Name                : Trigger01
NextExecutionTime   : 1/14/2016 12:45:07 PM
RecurrenceFrequency : Minute
RecurrenceInterval  : 60
Status              : Waiting
Type                : Microsoft.Logic/workflows/triggers
LogicAppName        : LogicApp05
LogicAppVersion     : 08587489107406290826
```

<span data-ttu-id="f9cb9-115">Ez a parancs a LogicApp05 nevű logikai appból kapja meg a Trigger01 nevű eseményindítót.</span><span class="sxs-lookup"><span data-stu-id="f9cb9-115">This command gets the trigger named Trigger01 from the logic app named LogicApp05.</span></span>

### <span data-ttu-id="f9cb9-116">2. példa: Logikai alkalmazás összes eseményindítójának lekérte</span><span class="sxs-lookup"><span data-stu-id="f9cb9-116">Example 2: Get all triggers of a logic app</span></span>
```
PS C:\>Get-AzLogicAppTrigger -ResourceGroupName "ResourceGroup11" -Name "LogicApp07"
ChangedTime         : 1/14/2016 11:45:07 AM
CreatedTime         : 1/13/2016 2:42:26 PM
LastExecutionTime   : 1/14/2016 11:45:07 AM
Name                : Trigger02
NextExecutionTime   : 1/14/2016 12:45:07 PM
RecurrenceFrequency : Minute
RecurrenceInterval  : 60
Status              : Waiting
Type                : Microsoft.Logic/workflows/triggers
LogicAppName        : LogicApp07
LogicAppVersion     : 08587489107406290826
```

<span data-ttu-id="f9cb9-117">Ez a parancs a LogicApp07 nevű logikai alkalmazás indítóit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="f9cb9-117">This command gets the triggers of the logic app named LogicApp07.</span></span>

## <span data-ttu-id="f9cb9-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f9cb9-118">PARAMETERS</span></span>

### <span data-ttu-id="f9cb9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9cb9-119">-DefaultProfile</span></span>
<span data-ttu-id="f9cb9-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="f9cb9-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f9cb9-121">-Name</span><span class="sxs-lookup"><span data-stu-id="f9cb9-121">-Name</span></span>
<span data-ttu-id="f9cb9-122">Annak a logikai alkalmazásnak a nevét adja meg, amelyből a parancsmag elindítja az eseményindítót.</span><span class="sxs-lookup"><span data-stu-id="f9cb9-122">Specifies the name of the logic app from which this cmdlet gets a trigger.</span></span>

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

### <span data-ttu-id="f9cb9-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9cb9-123">-ResourceGroupName</span></span>
<span data-ttu-id="f9cb9-124">Annak az erőforráscsoportnak a nevét adja meg, amelyben a parancsmag eseményindítót kap.</span><span class="sxs-lookup"><span data-stu-id="f9cb9-124">Specifies the name of a resource group in which this cmdlet gets a trigger.</span></span>

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

### <span data-ttu-id="f9cb9-125">-TriggerName</span><span class="sxs-lookup"><span data-stu-id="f9cb9-125">-TriggerName</span></span>
<span data-ttu-id="f9cb9-126">A parancsmag által lekért eseményindító neve.</span><span class="sxs-lookup"><span data-stu-id="f9cb9-126">Specifies the name of the trigger that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9cb9-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9cb9-127">CommonParameters</span></span>
<span data-ttu-id="f9cb9-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9cb9-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9cb9-129">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9cb9-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9cb9-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f9cb9-130">INPUTS</span></span>

### <span data-ttu-id="f9cb9-131">System.String</span><span class="sxs-lookup"><span data-stu-id="f9cb9-131">System.String</span></span>

## <span data-ttu-id="f9cb9-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f9cb9-132">OUTPUTS</span></span>

### <span data-ttu-id="f9cb9-133">Microsoft.Azure.Management.Logic.Models.WorkflowTrigger</span><span class="sxs-lookup"><span data-stu-id="f9cb9-133">Microsoft.Azure.Management.Logic.Models.WorkflowTrigger</span></span>

## <span data-ttu-id="f9cb9-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f9cb9-134">NOTES</span></span>

## <span data-ttu-id="f9cb9-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f9cb9-135">RELATED LINKS</span></span>

[<span data-ttu-id="f9cb9-136">Get-AzAppTriggerHistory</span><span class="sxs-lookup"><span data-stu-id="f9cb9-136">Get-AzLogicAppTriggerHistory</span></span>](./Get-AzLogicAppTriggerHistory.md)

[<span data-ttu-id="f9cb9-137">Start-AzApp</span><span class="sxs-lookup"><span data-stu-id="f9cb9-137">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)


