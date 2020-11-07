---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: F79AFF9A-CEDA-4E57-B5DB-9D0A7CDA6D27
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/register-azurermautomationscheduledrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Register-AzureRMAutomationScheduledRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Register-AzureRMAutomationScheduledRunbook.md
ms.openlocfilehash: deb6611fedbb1f88b9668b4750e096056ea8b1b7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672807"
---
# <span data-ttu-id="900bb-101">Register-AzureRmAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="900bb-101">Register-AzureRmAutomationScheduledRunbook</span></span>

## <span data-ttu-id="900bb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="900bb-102">SYNOPSIS</span></span>
<span data-ttu-id="900bb-103">Runbook társít egy ütemtervhez.</span><span class="sxs-lookup"><span data-stu-id="900bb-103">Associates a runbook to a schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="900bb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="900bb-104">SYNTAX</span></span>

### <span data-ttu-id="900bb-105">ByRunbookName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="900bb-105">ByRunbookName (Default)</span></span>
```
Register-AzureRmAutomationScheduledRunbook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="900bb-106">ByRunbookNameAndScheduleName</span><span class="sxs-lookup"><span data-stu-id="900bb-106">ByRunbookNameAndScheduleName</span></span>
```
Register-AzureRmAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String>
 [-Parameters <IDictionary>] [-RunOn <String>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="900bb-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="900bb-107">DESCRIPTION</span></span>
<span data-ttu-id="900bb-108">A **Register-AzureRmAutomationScheduledRunbook** parancsmag az Azure automatizálási runbook egy ütemtervhez társítja.</span><span class="sxs-lookup"><span data-stu-id="900bb-108">The **Register-AzureRmAutomationScheduledRunbook** cmdlet associates an Azure Automation runbook to a schedule.</span></span>
<span data-ttu-id="900bb-109">A runbook a *ScheduleName* paraméterrel megadott ütemezés alapján kezdődik.</span><span class="sxs-lookup"><span data-stu-id="900bb-109">The runbook starts based on the schedule you specify using the *ScheduleName* parameter.</span></span>

## <span data-ttu-id="900bb-110">Példák</span><span class="sxs-lookup"><span data-stu-id="900bb-110">EXAMPLES</span></span>

### <span data-ttu-id="900bb-111">1. példa: runbook társítása ütemtervvel</span><span class="sxs-lookup"><span data-stu-id="900bb-111">Example 1: Associate a runbook with a schedule</span></span>
```
PS C:\>Register-AzureRmAutomationScheduledRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ScheduleName "Sched01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="900bb-112">Ez a parancs a Runbk01 nevű runbook társítja a Contoso17 nevű Azure automatizálási fiók Sched01 nevű munkabeosztásával.</span><span class="sxs-lookup"><span data-stu-id="900bb-112">This command associates the runbook named Runbk01 with the schedule named Sched01 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="900bb-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="900bb-113">PARAMETERS</span></span>

### <span data-ttu-id="900bb-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="900bb-114">-AutomationAccountName</span></span>
<span data-ttu-id="900bb-115">A parancsmag működését biztosító runbook automatizálási fiókját adja meg.</span><span class="sxs-lookup"><span data-stu-id="900bb-115">Specifies an Automation account for the runbook on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="900bb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="900bb-116">-DefaultProfile</span></span>
<span data-ttu-id="900bb-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="900bb-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="900bb-118">-Paraméterek</span><span class="sxs-lookup"><span data-stu-id="900bb-118">-Parameters</span></span>
<span data-ttu-id="900bb-119">A kulcs/érték párokat tartalmazó hash-táblázatot adja meg.</span><span class="sxs-lookup"><span data-stu-id="900bb-119">Specifies a hash table of key/value pairs.</span></span>
<span data-ttu-id="900bb-120">A kulcsok a runbook.</span><span class="sxs-lookup"><span data-stu-id="900bb-120">The keys are runbook parameter names.</span></span>
<span data-ttu-id="900bb-121">Az értékek a runbook.</span><span class="sxs-lookup"><span data-stu-id="900bb-121">The values are runbook parameter values.</span></span>
<span data-ttu-id="900bb-122">Ha a runbook a kapcsolódó ütemtervre válaszol, ezek a paraméterek a runbook kerülnek.</span><span class="sxs-lookup"><span data-stu-id="900bb-122">When the runbook starts in response to the associated schedule, these parameters are passed to the runbook.</span></span>

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

### <span data-ttu-id="900bb-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="900bb-123">-ResourceGroupName</span></span>
<span data-ttu-id="900bb-124">Az ütemezett runbook tartozó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="900bb-124">Specifies the name of a resource group for the scheduled runbook.</span></span>

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

### <span data-ttu-id="900bb-125">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="900bb-125">-RunbookName</span></span>
<span data-ttu-id="900bb-126">Annak a runbook a nevét adja meg, amely a parancsmagnak az ütemtervhez van társítva.</span><span class="sxs-lookup"><span data-stu-id="900bb-126">Specifies the name of the runbook that this cmdlet associates to a schedule.</span></span>

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

### <span data-ttu-id="900bb-127">-RunOn</span><span class="sxs-lookup"><span data-stu-id="900bb-127">-RunOn</span></span>
<span data-ttu-id="900bb-128">A hibrid runbook dolgozó csoport neve.</span><span class="sxs-lookup"><span data-stu-id="900bb-128">The name of the hybrid runbook worker group.</span></span>

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

### <span data-ttu-id="900bb-129">-ScheduleName</span><span class="sxs-lookup"><span data-stu-id="900bb-129">-ScheduleName</span></span>
<span data-ttu-id="900bb-130">Annak az ütemezésnek a nevét adja meg, amelyre a parancsmag társít egy runbook.</span><span class="sxs-lookup"><span data-stu-id="900bb-130">Specifies the name of the schedule to which this cmdlet associates a runbook.</span></span>

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

### <span data-ttu-id="900bb-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="900bb-131">CommonParameters</span></span>
<span data-ttu-id="900bb-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="900bb-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="900bb-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="900bb-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="900bb-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="900bb-134">INPUTS</span></span>

### <span data-ttu-id="900bb-135">System. String</span><span class="sxs-lookup"><span data-stu-id="900bb-135">System.String</span></span>

## <span data-ttu-id="900bb-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="900bb-136">OUTPUTS</span></span>

### <span data-ttu-id="900bb-137">Microsoft. Azure. Command. Automation. Model. JobSchedule</span><span class="sxs-lookup"><span data-stu-id="900bb-137">Microsoft.Azure.Commands.Automation.Model.JobSchedule</span></span>

## <span data-ttu-id="900bb-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="900bb-138">NOTES</span></span>

## <span data-ttu-id="900bb-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="900bb-139">RELATED LINKS</span></span>

[<span data-ttu-id="900bb-140">Get-AzureRmAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="900bb-140">Get-AzureRmAutomationScheduledRunbook</span></span>](./Get-AzureRMAutomationScheduledRunbook.md)

[<span data-ttu-id="900bb-141">Regisztráció törlése – AzureRmAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="900bb-141">Unregister-AzureRmAutomationScheduledRunbook</span></span>](./Unregister-AzureRMAutomationScheduledRunbook.md)


