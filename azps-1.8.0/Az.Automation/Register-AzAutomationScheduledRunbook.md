---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: F79AFF9A-CEDA-4E57-B5DB-9D0A7CDA6D27
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/register-azautomationscheduledrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Register-AzAutomationScheduledRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Register-AzAutomationScheduledRunbook.md
ms.openlocfilehash: df6fc949fe1aa105a84ede2329c71feb4b27a449
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671546"
---
# <span data-ttu-id="90663-101">Register-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="90663-101">Register-AzAutomationScheduledRunbook</span></span>

## <span data-ttu-id="90663-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="90663-102">SYNOPSIS</span></span>
<span data-ttu-id="90663-103">Runbook társít egy ütemtervhez.</span><span class="sxs-lookup"><span data-stu-id="90663-103">Associates a runbook to a schedule.</span></span>

## <span data-ttu-id="90663-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="90663-104">SYNTAX</span></span>

### <span data-ttu-id="90663-105">ByRunbookName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="90663-105">ByRunbookName (Default)</span></span>
```
Register-AzAutomationScheduledRunbook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="90663-106">ByRunbookNameAndScheduleName</span><span class="sxs-lookup"><span data-stu-id="90663-106">ByRunbookNameAndScheduleName</span></span>
```
Register-AzAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String> [-Parameters <IDictionary>]
 [-RunOn <String>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="90663-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="90663-107">DESCRIPTION</span></span>
<span data-ttu-id="90663-108">A **Register-AzAutomationScheduledRunbook** parancsmag az Azure automatizálási runbook egy ütemtervhez társítja.</span><span class="sxs-lookup"><span data-stu-id="90663-108">The **Register-AzAutomationScheduledRunbook** cmdlet associates an Azure Automation runbook to a schedule.</span></span>
<span data-ttu-id="90663-109">A runbook a *ScheduleName* paraméterrel megadott ütemezés alapján kezdődik.</span><span class="sxs-lookup"><span data-stu-id="90663-109">The runbook starts based on the schedule you specify using the *ScheduleName* parameter.</span></span>

## <span data-ttu-id="90663-110">Példák</span><span class="sxs-lookup"><span data-stu-id="90663-110">EXAMPLES</span></span>

### <span data-ttu-id="90663-111">1. példa: runbook társítása ütemtervvel</span><span class="sxs-lookup"><span data-stu-id="90663-111">Example 1: Associate a runbook with a schedule</span></span>
```
PS C:\>Register-AzAutomationScheduledRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ScheduleName "Sched01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="90663-112">Ez a parancs a Runbk01 nevű runbook társítja a Contoso17 nevű Azure automatizálási fiók Sched01 nevű munkabeosztásával.</span><span class="sxs-lookup"><span data-stu-id="90663-112">This command associates the runbook named Runbk01 with the schedule named Sched01 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="90663-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="90663-113">PARAMETERS</span></span>

### <span data-ttu-id="90663-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="90663-114">-AutomationAccountName</span></span>
<span data-ttu-id="90663-115">A parancsmag működését biztosító runbook automatizálási fiókját adja meg.</span><span class="sxs-lookup"><span data-stu-id="90663-115">Specifies an Automation account for the runbook on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="90663-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90663-116">-DefaultProfile</span></span>
<span data-ttu-id="90663-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="90663-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="90663-118">-Paraméterek</span><span class="sxs-lookup"><span data-stu-id="90663-118">-Parameters</span></span>
<span data-ttu-id="90663-119">A kulcs/érték párokat tartalmazó hash-táblázatot adja meg.</span><span class="sxs-lookup"><span data-stu-id="90663-119">Specifies a hash table of key/value pairs.</span></span>
<span data-ttu-id="90663-120">A kulcsok a runbook.</span><span class="sxs-lookup"><span data-stu-id="90663-120">The keys are runbook parameter names.</span></span>
<span data-ttu-id="90663-121">Az értékek a runbook.</span><span class="sxs-lookup"><span data-stu-id="90663-121">The values are runbook parameter values.</span></span>
<span data-ttu-id="90663-122">Ha a runbook a kapcsolódó ütemtervre válaszol, ezek a paraméterek a runbook kerülnek.</span><span class="sxs-lookup"><span data-stu-id="90663-122">When the runbook starts in response to the associated schedule, these parameters are passed to the runbook.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: ByRunbookNameAndScheduleName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90663-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90663-123">-ResourceGroupName</span></span>
<span data-ttu-id="90663-124">Az ütemezett runbook tartozó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="90663-124">Specifies the name of a resource group for the scheduled runbook.</span></span>

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

### <span data-ttu-id="90663-125">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="90663-125">-RunbookName</span></span>
<span data-ttu-id="90663-126">Annak a runbook a nevét adja meg, amely a parancsmagnak az ütemtervhez van társítva.</span><span class="sxs-lookup"><span data-stu-id="90663-126">Specifies the name of the runbook that this cmdlet associates to a schedule.</span></span>

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

### <span data-ttu-id="90663-127">-RunOn</span><span class="sxs-lookup"><span data-stu-id="90663-127">-RunOn</span></span>
<span data-ttu-id="90663-128">A hibrid runbook dolgozó csoport neve.</span><span class="sxs-lookup"><span data-stu-id="90663-128">The name of the hybrid runbook worker group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRunbookNameAndScheduleName
Aliases: HybridWorker

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90663-129">-ScheduleName</span><span class="sxs-lookup"><span data-stu-id="90663-129">-ScheduleName</span></span>
<span data-ttu-id="90663-130">Annak az ütemezésnek a nevét adja meg, amelyre a parancsmag társít egy runbook.</span><span class="sxs-lookup"><span data-stu-id="90663-130">Specifies the name of the schedule to which this cmdlet associates a runbook.</span></span>

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

### <span data-ttu-id="90663-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90663-131">CommonParameters</span></span>
<span data-ttu-id="90663-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="90663-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90663-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90663-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90663-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="90663-134">INPUTS</span></span>

### <span data-ttu-id="90663-135">System. String</span><span class="sxs-lookup"><span data-stu-id="90663-135">System.String</span></span>

## <span data-ttu-id="90663-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="90663-136">OUTPUTS</span></span>

### <span data-ttu-id="90663-137">Microsoft. Azure. Command. Automation. Model. JobSchedule</span><span class="sxs-lookup"><span data-stu-id="90663-137">Microsoft.Azure.Commands.Automation.Model.JobSchedule</span></span>

## <span data-ttu-id="90663-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="90663-138">NOTES</span></span>

## <span data-ttu-id="90663-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="90663-139">RELATED LINKS</span></span>

[<span data-ttu-id="90663-140">Get-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="90663-140">Get-AzAutomationScheduledRunbook</span></span>](./Get-AzAutomationScheduledRunbook.md)

[<span data-ttu-id="90663-141">Regisztráció törlése – AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="90663-141">Unregister-AzAutomationScheduledRunbook</span></span>](./Unregister-AzAutomationScheduledRunbook.md)


