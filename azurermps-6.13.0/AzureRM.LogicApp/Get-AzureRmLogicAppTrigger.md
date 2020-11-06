---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 5307F1F1-E84C-4949-A557-99EF0012C3DF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/get-azurermlogicapptrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicAppTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicAppTrigger.md
ms.openlocfilehash: 6066a08774be9f5e3fa67a07b0d868947384f518
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503619"
---
# <span data-ttu-id="7ec16-101">Get-AzureRmLogicAppTrigger</span><span class="sxs-lookup"><span data-stu-id="7ec16-101">Get-AzureRmLogicAppTrigger</span></span>

## <span data-ttu-id="7ec16-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7ec16-102">SYNOPSIS</span></span>
<span data-ttu-id="7ec16-103">Megnyeri a logikai alkalmazások eseményindítóit.</span><span class="sxs-lookup"><span data-stu-id="7ec16-103">Gets the triggers of a logic app.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7ec16-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7ec16-104">SYNTAX</span></span>

```
Get-AzureRmLogicAppTrigger -ResourceGroupName <String> -Name <String> [-TriggerName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7ec16-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7ec16-105">DESCRIPTION</span></span>
<span data-ttu-id="7ec16-106">A **Get-AzureRmLogicAppTrigger** parancsmag egy logikai alkalmazásból kapja meg az eseményindítókat.</span><span class="sxs-lookup"><span data-stu-id="7ec16-106">The **Get-AzureRmLogicAppTrigger** cmdlet gets triggers from a logic app.</span></span>
<span data-ttu-id="7ec16-107">Ez a parancsmag egy **WorkflowTrigger** objektumot ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="7ec16-107">This cmdlet returns a **WorkflowTrigger** object.</span></span>
<span data-ttu-id="7ec16-108">Adja meg a munkafolyamatot, az erőforráscsoportot és a triggert.</span><span class="sxs-lookup"><span data-stu-id="7ec16-108">Specify the workflow, resource group, and trigger.</span></span>
<span data-ttu-id="7ec16-109">Ez a modul támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="7ec16-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="7ec16-110">Ha dinamikus paramétert szeretne használni, írja be azt a parancsba.</span><span class="sxs-lookup"><span data-stu-id="7ec16-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="7ec16-111">A dinamikus paraméterek nevének feltárásához írjon be egy kötőjelet (-) a parancsmag neve után, majd nyomja le többször a TAB billentyűt a rendelkezésre álló paraméterek közötti váltáshoz.</span><span class="sxs-lookup"><span data-stu-id="7ec16-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="7ec16-112">Ha kihagyja a szükséges sablon paramétert, a parancsmag kéri az érték megadását.</span><span class="sxs-lookup"><span data-stu-id="7ec16-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="7ec16-113">Példák</span><span class="sxs-lookup"><span data-stu-id="7ec16-113">EXAMPLES</span></span>

### <span data-ttu-id="7ec16-114">Példa 1: logikai alkalmazás kiváltójának beszerzése</span><span class="sxs-lookup"><span data-stu-id="7ec16-114">Example 1: Get a trigger of a logic app</span></span>
```
PS C:\>Get-AzureRmLogicAppTrigger -ResourceGroupName "ResourceGroup11" -Name "LogicApp05" -TriggerName "Trigger01"
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

<span data-ttu-id="7ec16-115">Ez a parancs a Trigger01 nevű triggert kapja meg a LogicApp05 nevű logikai alkalmazásból.</span><span class="sxs-lookup"><span data-stu-id="7ec16-115">This command gets the trigger named Trigger01 from the logic app named LogicApp05.</span></span>

### <span data-ttu-id="7ec16-116">2. példa: egy logikai app minden eseményindítójának beolvasása</span><span class="sxs-lookup"><span data-stu-id="7ec16-116">Example 2: Get all triggers of a logic app</span></span>
```
PS C:\>Get-AzureRmLogicAppTrigger -ResourceGroupName "ResourceGroup11" -Name "LogicApp07"
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

<span data-ttu-id="7ec16-117">Ez a parancs a LogicApp07 nevű logikai app eseményindítóját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="7ec16-117">This command gets the triggers of the logic app named LogicApp07.</span></span>

## <span data-ttu-id="7ec16-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7ec16-118">PARAMETERS</span></span>

### <span data-ttu-id="7ec16-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ec16-119">-DefaultProfile</span></span>
<span data-ttu-id="7ec16-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="7ec16-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7ec16-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7ec16-121">-Name</span></span>
<span data-ttu-id="7ec16-122">Annak a logikai alkalmazásnak a neve, amelyből a parancsmag az indítót kapja.</span><span class="sxs-lookup"><span data-stu-id="7ec16-122">Specifies the name of the logic app from which this cmdlet gets a trigger.</span></span>

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

### <span data-ttu-id="7ec16-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ec16-123">-ResourceGroupName</span></span>
<span data-ttu-id="7ec16-124">Annak a csoportnak a nevét adja meg, amelyben a parancsmag az indítót kapja.</span><span class="sxs-lookup"><span data-stu-id="7ec16-124">Specifies the name of a resource group in which this cmdlet gets a trigger.</span></span>

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

### <span data-ttu-id="7ec16-125">-TriggerName</span><span class="sxs-lookup"><span data-stu-id="7ec16-125">-TriggerName</span></span>
<span data-ttu-id="7ec16-126">Itt adhatja meg annak az triggernek a nevét, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="7ec16-126">Specifies the name of the trigger that this cmdlet gets.</span></span>

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

### <span data-ttu-id="7ec16-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ec16-127">CommonParameters</span></span>
<span data-ttu-id="7ec16-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7ec16-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ec16-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ec16-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ec16-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7ec16-130">INPUTS</span></span>

### <span data-ttu-id="7ec16-131">System. String</span><span class="sxs-lookup"><span data-stu-id="7ec16-131">System.String</span></span>

## <span data-ttu-id="7ec16-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7ec16-132">OUTPUTS</span></span>

### <span data-ttu-id="7ec16-133">Microsoft. Azure. Management. Logic. models. WorkflowTrigger</span><span class="sxs-lookup"><span data-stu-id="7ec16-133">Microsoft.Azure.Management.Logic.Models.WorkflowTrigger</span></span>

## <span data-ttu-id="7ec16-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7ec16-134">NOTES</span></span>

## <span data-ttu-id="7ec16-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7ec16-135">RELATED LINKS</span></span>

[<span data-ttu-id="7ec16-136">Get-AzureRmLogicAppTriggerHistory</span><span class="sxs-lookup"><span data-stu-id="7ec16-136">Get-AzureRmLogicAppTriggerHistory</span></span>](./Get-AzureRmLogicAppTriggerHistory.md)

[<span data-ttu-id="7ec16-137">Start-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="7ec16-137">Start-AzureRmLogicApp</span></span>](./Start-AzureRmLogicApp.md)


