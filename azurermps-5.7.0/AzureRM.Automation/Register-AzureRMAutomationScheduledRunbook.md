---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: F79AFF9A-CEDA-4E57-B5DB-9D0A7CDA6D27
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/register-azurermautomationscheduledrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Register-AzureRMAutomationScheduledRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Register-AzureRMAutomationScheduledRunbook.md
ms.openlocfilehash: ec89359453af2dd997aed6359914ac499a6a3f7e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493285"
---
# <span data-ttu-id="f2f2a-101">Register-AzureRmAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="f2f2a-101">Register-AzureRmAutomationScheduledRunbook</span></span>

## <span data-ttu-id="f2f2a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f2f2a-102">SYNOPSIS</span></span>
<span data-ttu-id="f2f2a-103">Runbook társít egy ütemtervhez.</span><span class="sxs-lookup"><span data-stu-id="f2f2a-103">Associates a runbook to a schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f2f2a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f2f2a-104">SYNTAX</span></span>

### <span data-ttu-id="f2f2a-105">ByRunbookName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f2f2a-105">ByRunbookName (Default)</span></span>
```
Register-AzureRmAutomationScheduledRunbook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f2f2a-106">ByRunbookNameAndScheduleName</span><span class="sxs-lookup"><span data-stu-id="f2f2a-106">ByRunbookNameAndScheduleName</span></span>
```
Register-AzureRmAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String>
 [-Parameters <IDictionary>] [-RunOn <String>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f2f2a-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="f2f2a-107">DESCRIPTION</span></span>
<span data-ttu-id="f2f2a-108">A **Register-AzureRmAutomationScheduledRunbook** parancsmag az Azure automatizálási runbook egy ütemtervhez társítja.</span><span class="sxs-lookup"><span data-stu-id="f2f2a-108">The **Register-AzureRmAutomationScheduledRunbook** cmdlet associates an Azure Automation runbook to a schedule.</span></span>
<span data-ttu-id="f2f2a-109">A runbook a *ScheduleName* paraméterrel megadott ütemezés alapján kezdődik.</span><span class="sxs-lookup"><span data-stu-id="f2f2a-109">The runbook starts based on the schedule you specify using the *ScheduleName* parameter.</span></span>

## <span data-ttu-id="f2f2a-110">Példák</span><span class="sxs-lookup"><span data-stu-id="f2f2a-110">EXAMPLES</span></span>

### <span data-ttu-id="f2f2a-111">1. példa: runbook társítása ütemtervvel</span><span class="sxs-lookup"><span data-stu-id="f2f2a-111">Example 1: Associate a runbook with a schedule</span></span>
```
PS C:\>Register-AzureRmAutomationScheduledRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ScheduleName "Sched01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="f2f2a-112">Ez a parancs a Runbk01 nevű runbook társítja a Contoso17 nevű Azure automatizálási fiók Sched01 nevű munkabeosztásával.</span><span class="sxs-lookup"><span data-stu-id="f2f2a-112">This command associates the runbook named Runbk01 with the schedule named Sched01 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="f2f2a-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f2f2a-113">PARAMETERS</span></span>

### <span data-ttu-id="f2f2a-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f2f2a-114">-AutomationAccountName</span></span>
<span data-ttu-id="f2f2a-115">A parancsmag működését biztosító runbook automatizálási fiókját adja meg.</span><span class="sxs-lookup"><span data-stu-id="f2f2a-115">Specifies an Automation account for the runbook on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="f2f2a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2f2a-116">-DefaultProfile</span></span>
<span data-ttu-id="f2f2a-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="f2f2a-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f2f2a-118">-Paraméterek</span><span class="sxs-lookup"><span data-stu-id="f2f2a-118">-Parameters</span></span>
<span data-ttu-id="f2f2a-119">A kulcs/érték párokat tartalmazó hash-táblázatot adja meg.</span><span class="sxs-lookup"><span data-stu-id="f2f2a-119">Specifies a hash table of key/value pairs.</span></span>
<span data-ttu-id="f2f2a-120">A kulcsok a runbook.</span><span class="sxs-lookup"><span data-stu-id="f2f2a-120">The keys are runbook parameter names.</span></span>
<span data-ttu-id="f2f2a-121">Az értékek a runbook.</span><span class="sxs-lookup"><span data-stu-id="f2f2a-121">The values are runbook parameter values.</span></span>
<span data-ttu-id="f2f2a-122">Ha a runbook a kapcsolódó ütemtervre válaszol, ezek a paraméterek a runbook kerülnek.</span><span class="sxs-lookup"><span data-stu-id="f2f2a-122">When the runbook starts in response to the associated schedule, these parameters are passed to the runbook.</span></span>

```yaml
Type: IDictionary
Parameter Sets: ByRunbookNameAndScheduleName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2f2a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2f2a-123">-ResourceGroupName</span></span>
<span data-ttu-id="f2f2a-124">Az ütemezett runbook tartozó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f2f2a-124">Specifies the name of a resource group for the scheduled runbook.</span></span>

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

### <span data-ttu-id="f2f2a-125">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="f2f2a-125">-RunbookName</span></span>
<span data-ttu-id="f2f2a-126">Annak a runbook a nevét adja meg, amely a parancsmagnak az ütemtervhez van társítva.</span><span class="sxs-lookup"><span data-stu-id="f2f2a-126">Specifies the name of the runbook that this cmdlet associates to a schedule.</span></span>

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

### <span data-ttu-id="f2f2a-127">-RunOn</span><span class="sxs-lookup"><span data-stu-id="f2f2a-127">-RunOn</span></span>
<span data-ttu-id="f2f2a-128">A hibrid runbook dolgozó csoport neve.</span><span class="sxs-lookup"><span data-stu-id="f2f2a-128">The name of the hybrid runbook worker group.</span></span>

```yaml
Type: String
Parameter Sets: ByRunbookNameAndScheduleName
Aliases: HybridWorker

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2f2a-129">-ScheduleName</span><span class="sxs-lookup"><span data-stu-id="f2f2a-129">-ScheduleName</span></span>
<span data-ttu-id="f2f2a-130">Annak az ütemezésnek a nevét adja meg, amelyre a parancsmag társít egy runbook.</span><span class="sxs-lookup"><span data-stu-id="f2f2a-130">Specifies the name of the schedule to which this cmdlet associates a runbook.</span></span>

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

### <span data-ttu-id="f2f2a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2f2a-131">CommonParameters</span></span>
<span data-ttu-id="f2f2a-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f2f2a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2f2a-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2f2a-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2f2a-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f2f2a-134">INPUTS</span></span>

### <span data-ttu-id="f2f2a-135">Nincs</span><span class="sxs-lookup"><span data-stu-id="f2f2a-135">None</span></span>
<span data-ttu-id="f2f2a-136">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="f2f2a-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f2f2a-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f2f2a-137">OUTPUTS</span></span>

### <span data-ttu-id="f2f2a-138">Microsoft. Azure. Command. Automation. Model. JobSchedule</span><span class="sxs-lookup"><span data-stu-id="f2f2a-138">Microsoft.Azure.Commands.Automation.Model.JobSchedule</span></span>

## <span data-ttu-id="f2f2a-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f2f2a-139">NOTES</span></span>

## <span data-ttu-id="f2f2a-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f2f2a-140">RELATED LINKS</span></span>

[<span data-ttu-id="f2f2a-141">Get-AzureRmAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="f2f2a-141">Get-AzureRmAutomationScheduledRunbook</span></span>](./Get-AzureRMAutomationScheduledRunbook.md)

[<span data-ttu-id="f2f2a-142">Regisztráció törlése – AzureRmAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="f2f2a-142">Unregister-AzureRmAutomationScheduledRunbook</span></span>](./Unregister-AzureRMAutomationScheduledRunbook.md)


