---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: C7C193CF-4E3A-4275-8289-946C99B1C553
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Unregister-AzureRMAutomationScheduledRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Unregister-AzureRMAutomationScheduledRunbook.md
ms.openlocfilehash: aa970f71be1e80f9eb5fcc1b4ec24cf0ce7f0e9f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503268"
---
# <span data-ttu-id="5e2ca-101">Unregister-AzureRmAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="5e2ca-101">Unregister-AzureRmAutomationScheduledRunbook</span></span>

## <span data-ttu-id="5e2ca-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5e2ca-102">SYNOPSIS</span></span>
<span data-ttu-id="5e2ca-103">Egy runbook és egy ütemterv közötti társítás eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="5e2ca-103">Removes an association between a runbook and a schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5e2ca-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5e2ca-104">SYNTAX</span></span>

### <span data-ttu-id="5e2ca-105">ByJobScheduleId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5e2ca-105">ByJobScheduleId (Default)</span></span>
```
Unregister-AzureRmAutomationScheduledRunbook -JobScheduleId <Guid> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5e2ca-106">ByRunbookNameAndScheduleName</span><span class="sxs-lookup"><span data-stu-id="5e2ca-106">ByRunbookNameAndScheduleName</span></span>
```
Unregister-AzureRmAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String> [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e2ca-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="5e2ca-107">DESCRIPTION</span></span>
<span data-ttu-id="5e2ca-108">A **unregister-AzureRmAutomationScheduledRunbook** parancsmag eltávolítja az Azure automatizálási runbook és az ütemterv közötti társítást.</span><span class="sxs-lookup"><span data-stu-id="5e2ca-108">The **Unregister-AzureRmAutomationScheduledRunbook** cmdlet removes the association between an Azure Automation runbook and a schedule.</span></span>
<span data-ttu-id="5e2ca-109">Az ütemezés már nem indítja el a runbook.</span><span class="sxs-lookup"><span data-stu-id="5e2ca-109">The schedule no longer starts the runbook.</span></span>

## <span data-ttu-id="5e2ca-110">Példák</span><span class="sxs-lookup"><span data-stu-id="5e2ca-110">EXAMPLES</span></span>

### <span data-ttu-id="5e2ca-111">1. példa: a runbook és az ütemterv közötti társítás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="5e2ca-111">Example 1: Remove the association between a runbook and a schedule</span></span>
```
PS C:\>Unregister-AzureRmAutomationScheduledRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01" -ScheduleName "Runbk01Sched"
```

<span data-ttu-id="5e2ca-112">Ez a parancs eltávolítja a Runbk01 nevű runbook társítását és a Runbk01Sched nevű ütemtervet.</span><span class="sxs-lookup"><span data-stu-id="5e2ca-112">This command removes the association between the runbook named Runbk01 and the schedule named Runbk01Sched.</span></span>

## <span data-ttu-id="5e2ca-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5e2ca-113">PARAMETERS</span></span>

### <span data-ttu-id="5e2ca-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="5e2ca-114">-AutomationAccountName</span></span>
<span data-ttu-id="5e2ca-115">A parancsmag működését biztosító runbook automatizálási fiókját adja meg.</span><span class="sxs-lookup"><span data-stu-id="5e2ca-115">Specifies an Automation account for the runbook on which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e2ca-116">-Force</span><span class="sxs-lookup"><span data-stu-id="5e2ca-116">-Force</span></span>
<span data-ttu-id="5e2ca-117">ps_force</span><span class="sxs-lookup"><span data-stu-id="5e2ca-117">ps_force</span></span>

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

### <span data-ttu-id="5e2ca-118">-JobScheduleId</span><span class="sxs-lookup"><span data-stu-id="5e2ca-118">-JobScheduleId</span></span>
<span data-ttu-id="5e2ca-119">Az ütemezett runbook AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="5e2ca-119">Specifies the ID of a scheduled runbook.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: ByJobScheduleId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e2ca-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e2ca-120">-ResourceGroupName</span></span>
<span data-ttu-id="5e2ca-121">Az ütemezett runbook tartozó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5e2ca-121">Specifies the name of a resource group for the scheduled runbook.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e2ca-122">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="5e2ca-122">-RunbookName</span></span>
<span data-ttu-id="5e2ca-123">Annak a runbook a nevét adja meg, amelynek a parancsmagja nem egy ütemtervből áll.</span><span class="sxs-lookup"><span data-stu-id="5e2ca-123">Specifies the name of the runbook that this cmdlet dissociates from a schedule.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRunbookNameAndScheduleName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e2ca-124">-ScheduleName</span><span class="sxs-lookup"><span data-stu-id="5e2ca-124">-ScheduleName</span></span>
<span data-ttu-id="5e2ca-125">Annak az ütemezésnek a neve, amelyből a parancsmag egy runbook.</span><span class="sxs-lookup"><span data-stu-id="5e2ca-125">Specifies the name of the schedule from which this cmdlet dissociates a runbook.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRunbookNameAndScheduleName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e2ca-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5e2ca-126">-Confirm</span></span>
<span data-ttu-id="5e2ca-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5e2ca-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e2ca-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e2ca-128">-WhatIf</span></span>
<span data-ttu-id="5e2ca-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5e2ca-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e2ca-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5e2ca-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e2ca-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e2ca-131">-DefaultProfile</span></span>
<span data-ttu-id="5e2ca-132">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5e2ca-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5e2ca-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e2ca-133">CommonParameters</span></span>
<span data-ttu-id="5e2ca-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5e2ca-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e2ca-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e2ca-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e2ca-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5e2ca-136">INPUTS</span></span>

## <span data-ttu-id="5e2ca-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5e2ca-137">OUTPUTS</span></span>

## <span data-ttu-id="5e2ca-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5e2ca-138">NOTES</span></span>

## <span data-ttu-id="5e2ca-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5e2ca-139">RELATED LINKS</span></span>

[<span data-ttu-id="5e2ca-140">Get-AzureRmAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="5e2ca-140">Get-AzureRmAutomationScheduledRunbook</span></span>](./Get-AzureRMAutomationScheduledRunbook.md)

[<span data-ttu-id="5e2ca-141">Register-AzureRmAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="5e2ca-141">Register-AzureRmAutomationScheduledRunbook</span></span>](./Register-AzureRMAutomationScheduledRunbook.md)


