---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: C7C193CF-4E3A-4275-8289-946C99B1C553
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/unregister-azurermautomationscheduledrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Unregister-AzureRMAutomationScheduledRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Unregister-AzureRMAutomationScheduledRunbook.md
ms.openlocfilehash: a8e79dfcd505de6cb1a539f0b194f549835a95f3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501536"
---
# <span data-ttu-id="98a43-101">Unregister-AzureRmAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="98a43-101">Unregister-AzureRmAutomationScheduledRunbook</span></span>

## <span data-ttu-id="98a43-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="98a43-102">SYNOPSIS</span></span>
<span data-ttu-id="98a43-103">Egy runbook és egy ütemterv közötti társítás eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="98a43-103">Removes an association between a runbook and a schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="98a43-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="98a43-104">SYNTAX</span></span>

### <span data-ttu-id="98a43-105">ByJobScheduleId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="98a43-105">ByJobScheduleId (Default)</span></span>
```
Unregister-AzureRmAutomationScheduledRunbook -JobScheduleId <Guid> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="98a43-106">ByRunbookNameAndScheduleName</span><span class="sxs-lookup"><span data-stu-id="98a43-106">ByRunbookNameAndScheduleName</span></span>
```
Unregister-AzureRmAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String> [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="98a43-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="98a43-107">DESCRIPTION</span></span>
<span data-ttu-id="98a43-108">A **unregister-AzureRmAutomationScheduledRunbook** parancsmag eltávolítja az Azure automatizálási runbook és az ütemterv közötti társítást.</span><span class="sxs-lookup"><span data-stu-id="98a43-108">The **Unregister-AzureRmAutomationScheduledRunbook** cmdlet removes the association between an Azure Automation runbook and a schedule.</span></span>
<span data-ttu-id="98a43-109">Az ütemezés már nem indítja el a runbook.</span><span class="sxs-lookup"><span data-stu-id="98a43-109">The schedule no longer starts the runbook.</span></span>

## <span data-ttu-id="98a43-110">Példák</span><span class="sxs-lookup"><span data-stu-id="98a43-110">EXAMPLES</span></span>

### <span data-ttu-id="98a43-111">1. példa: a runbook és az ütemterv közötti társítás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="98a43-111">Example 1: Remove the association between a runbook and a schedule</span></span>
```
PS C:\>Unregister-AzureRmAutomationScheduledRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01" -ScheduleName "Runbk01Sched"
```

<span data-ttu-id="98a43-112">Ez a parancs eltávolítja a Runbk01 nevű runbook társítását és a Runbk01Sched nevű ütemtervet.</span><span class="sxs-lookup"><span data-stu-id="98a43-112">This command removes the association between the runbook named Runbk01 and the schedule named Runbk01Sched.</span></span>

## <span data-ttu-id="98a43-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="98a43-113">PARAMETERS</span></span>

### <span data-ttu-id="98a43-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="98a43-114">-AutomationAccountName</span></span>
<span data-ttu-id="98a43-115">A parancsmag működését biztosító runbook automatizálási fiókját adja meg.</span><span class="sxs-lookup"><span data-stu-id="98a43-115">Specifies an Automation account for the runbook on which this cmdlet operates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98a43-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98a43-116">-DefaultProfile</span></span>
<span data-ttu-id="98a43-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="98a43-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98a43-118">-Force</span><span class="sxs-lookup"><span data-stu-id="98a43-118">-Force</span></span>
<span data-ttu-id="98a43-119">ps_force</span><span class="sxs-lookup"><span data-stu-id="98a43-119">ps_force</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98a43-120">-JobScheduleId</span><span class="sxs-lookup"><span data-stu-id="98a43-120">-JobScheduleId</span></span>
<span data-ttu-id="98a43-121">Az ütemezett runbook AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="98a43-121">Specifies the ID of a scheduled runbook.</span></span>

```yaml
Type: Guid
Parameter Sets: ByJobScheduleId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98a43-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98a43-122">-ResourceGroupName</span></span>
<span data-ttu-id="98a43-123">Az ütemezett runbook tartozó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="98a43-123">Specifies the name of a resource group for the scheduled runbook.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98a43-124">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="98a43-124">-RunbookName</span></span>
<span data-ttu-id="98a43-125">Annak a runbook a nevét adja meg, amelynek a parancsmagja nem egy ütemtervből áll.</span><span class="sxs-lookup"><span data-stu-id="98a43-125">Specifies the name of the runbook that this cmdlet dissociates from a schedule.</span></span>

```yaml
Type: String
Parameter Sets: ByRunbookNameAndScheduleName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98a43-126">-ScheduleName</span><span class="sxs-lookup"><span data-stu-id="98a43-126">-ScheduleName</span></span>
<span data-ttu-id="98a43-127">Annak az ütemezésnek a neve, amelyből a parancsmag egy runbook.</span><span class="sxs-lookup"><span data-stu-id="98a43-127">Specifies the name of the schedule from which this cmdlet dissociates a runbook.</span></span>

```yaml
Type: String
Parameter Sets: ByRunbookNameAndScheduleName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98a43-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="98a43-128">-Confirm</span></span>
<span data-ttu-id="98a43-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="98a43-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98a43-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98a43-130">-WhatIf</span></span>
<span data-ttu-id="98a43-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="98a43-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="98a43-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="98a43-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98a43-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98a43-133">CommonParameters</span></span>
<span data-ttu-id="98a43-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="98a43-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98a43-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98a43-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98a43-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="98a43-136">INPUTS</span></span>

### <span data-ttu-id="98a43-137">Nincs</span><span class="sxs-lookup"><span data-stu-id="98a43-137">None</span></span>
<span data-ttu-id="98a43-138">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="98a43-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="98a43-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="98a43-139">OUTPUTS</span></span>

## <span data-ttu-id="98a43-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="98a43-140">NOTES</span></span>

## <span data-ttu-id="98a43-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="98a43-141">RELATED LINKS</span></span>

[<span data-ttu-id="98a43-142">Get-AzureRmAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="98a43-142">Get-AzureRmAutomationScheduledRunbook</span></span>](./Get-AzureRMAutomationScheduledRunbook.md)

[<span data-ttu-id="98a43-143">Register-AzureRmAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="98a43-143">Register-AzureRmAutomationScheduledRunbook</span></span>](./Register-AzureRMAutomationScheduledRunbook.md)


