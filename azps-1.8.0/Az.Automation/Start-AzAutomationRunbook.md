---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B2D9FF7B-EA3B-4853-814C-00FC4E328957
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/start-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationRunbook.md
ms.openlocfilehash: 2f9b5354731a64a5cb614e173aa45be5349197d5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671488"
---
# <span data-ttu-id="25c03-101">Start-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="25c03-101">Start-AzAutomationRunbook</span></span>

## <span data-ttu-id="25c03-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="25c03-102">SYNOPSIS</span></span>
<span data-ttu-id="25c03-103">Elindít egy runbook-feladatot.</span><span class="sxs-lookup"><span data-stu-id="25c03-103">Starts a runbook job.</span></span>

## <span data-ttu-id="25c03-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="25c03-104">SYNTAX</span></span>

### <span data-ttu-id="25c03-105">ByAsynchronousReturnJob (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="25c03-105">ByAsynchronousReturnJob (Default)</span></span>
```
Start-AzAutomationRunbook [-Name] <String> [-Parameters <IDictionary>] [-RunOn <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="25c03-106">BySynchronousReturnJobOutput</span><span class="sxs-lookup"><span data-stu-id="25c03-106">BySynchronousReturnJobOutput</span></span>
```
Start-AzAutomationRunbook [-Name] <String> [-Parameters <IDictionary>] [-RunOn <String>] [-Wait]
 [-MaxWaitSeconds <Int32>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="25c03-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="25c03-107">DESCRIPTION</span></span>
<span data-ttu-id="25c03-108">A **Start-AzAutomationRunbook** parancsmag az Azure automatizálási runbook feladatát indítja el.</span><span class="sxs-lookup"><span data-stu-id="25c03-108">The **Start-AzAutomationRunbook** cmdlet starts an Azure Automation runbook job.</span></span>
<span data-ttu-id="25c03-109">Adja meg a runbook AZONOSÍTÓját vagy nevét.</span><span class="sxs-lookup"><span data-stu-id="25c03-109">Specify the ID or name of a runbook.</span></span>

## <span data-ttu-id="25c03-110">Példák</span><span class="sxs-lookup"><span data-stu-id="25c03-110">EXAMPLES</span></span>

### <span data-ttu-id="25c03-111">1. példa: runbook-feladat indítása</span><span class="sxs-lookup"><span data-stu-id="25c03-111">Example 1: Start a runbook job</span></span>
```
PS C:\>Start-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="25c03-112">Ez a parancs runbook-feladatot indít az Contoso17 nevű Azure Automation fiók Runbk01 nevű runbook.</span><span class="sxs-lookup"><span data-stu-id="25c03-112">This command starts a runbook job for the runbook named Runbk01 in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="25c03-113">2. példa: a Python 2 runbook feladatát paraméterekkel indíthatja el.</span><span class="sxs-lookup"><span data-stu-id="25c03-113">Example 2: Start a Python 2 runbook job with parameters</span></span>
```
PS C:\>Start-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "RunbkPy01" -ResourceGroupName "ResourceGroup01" -Parameters @{"Key1"="ValueForPosition1";"Key2"="ValueForPosition2"}
```

<span data-ttu-id="25c03-114">Ez a parancs elindítja a runbook-feladatot a Python 2 runbook nevű RunbkPy01 nevű az Azure automatizálási fiókjában, a Contoso17 "ValueForPosition1" néven az első pozicionált paramétert, a másodikat pedig "ValueForPosition2".</span><span class="sxs-lookup"><span data-stu-id="25c03-114">This command starts a runbook job for the Python 2 runbook named RunbkPy01 in the Azure Automation account named Contoso17 with "ValueForPosition1" as the first positional parameter and "ValueForPosition2" for the second one.</span></span>

### <span data-ttu-id="25c03-115">3. példa: runbook feladat indítása és várakozás az eredményre</span><span class="sxs-lookup"><span data-stu-id="25c03-115">Example 3: Start a runbook job and wait for results</span></span>
```
Start-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01" -MaxWaitSeconds 1000 -Wait
```

<span data-ttu-id="25c03-116">Ez a parancs runbook-feladatot indít az Contoso17 nevű Azure Automation fiók Runbk01 nevű runbook.</span><span class="sxs-lookup"><span data-stu-id="25c03-116">This command starts a runbook job for the runbook named Runbk01 in the Azure Automation account named Contoso17.</span></span>
<span data-ttu-id="25c03-117">Ez a parancs a _várakozási_ paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="25c03-117">This command specifies the _Wait_ parameter.</span></span>
<span data-ttu-id="25c03-118">Így a feladat befejezését követően eredményül ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="25c03-118">Therefore, it returns results after the job is completed.</span></span>
<span data-ttu-id="25c03-119">A parancsmag az eredményhez legfeljebb 1000 másodpercet vár.</span><span class="sxs-lookup"><span data-stu-id="25c03-119">The cmdlet waits up to 1000 seconds for the results.</span></span>

## <span data-ttu-id="25c03-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="25c03-120">PARAMETERS</span></span>

### <span data-ttu-id="25c03-121">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="25c03-121">-AutomationAccountName</span></span>
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

### <span data-ttu-id="25c03-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25c03-122">-DefaultProfile</span></span>
<span data-ttu-id="25c03-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="25c03-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="25c03-124">-MaxWaitSeconds</span><span class="sxs-lookup"><span data-stu-id="25c03-124">-MaxWaitSeconds</span></span>
<span data-ttu-id="25c03-125">Azt adja meg, hogy hány másodpercig tart a parancsmag, mielőtt felhagyják a feladatot.</span><span class="sxs-lookup"><span data-stu-id="25c03-125">Specifies the number of seconds this cmdlet waits for a job to finish before it abandons the job.</span></span>
<span data-ttu-id="25c03-126">Az alapértelmezett érték a 10800, vagy három óra.</span><span class="sxs-lookup"><span data-stu-id="25c03-126">The default value is 10800, or three hours.</span></span>

```yaml
Type: System.Int32
Parameter Sets: BySynchronousReturnJobOutput
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25c03-127">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="25c03-127">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RunbookName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25c03-128">-Paraméterek</span><span class="sxs-lookup"><span data-stu-id="25c03-128">-Parameters</span></span>
```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases: JobParameters

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25c03-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25c03-129">-ResourceGroupName</span></span>
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

### <span data-ttu-id="25c03-130">-RunOn</span><span class="sxs-lookup"><span data-stu-id="25c03-130">-RunOn</span></span>
<span data-ttu-id="25c03-131">Annak megadása, hogy melyik hibrid munkacsoportot szeretné futtatni a runbook.</span><span class="sxs-lookup"><span data-stu-id="25c03-131">Specifies which Hybrid Worker Group on which to run the runbook.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HybridWorker

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25c03-132">– Várjon</span><span class="sxs-lookup"><span data-stu-id="25c03-132">-Wait</span></span>
<span data-ttu-id="25c03-133">Jelzi, hogy ez a parancsmag várja a feladatok befejezését, felfüggesztését vagy sikertelenségét, majd visszaadja az Azure PowerShell-vezérlőt.</span><span class="sxs-lookup"><span data-stu-id="25c03-133">Indicates that this cmdlet waits for job to complete, suspend, or fail, and then returns control to Azure PowerShell.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: BySynchronousReturnJobOutput
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25c03-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25c03-134">CommonParameters</span></span>
<span data-ttu-id="25c03-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="25c03-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25c03-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25c03-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25c03-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="25c03-137">INPUTS</span></span>

### <span data-ttu-id="25c03-138">System. String</span><span class="sxs-lookup"><span data-stu-id="25c03-138">System.String</span></span>

## <span data-ttu-id="25c03-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="25c03-139">OUTPUTS</span></span>

### <span data-ttu-id="25c03-140">Microsoft. Azure. Command. Automation. Model. job</span><span class="sxs-lookup"><span data-stu-id="25c03-140">Microsoft.Azure.Commands.Automation.Model.Job</span></span>

### <span data-ttu-id="25c03-141">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="25c03-141">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="25c03-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="25c03-142">NOTES</span></span>

## <span data-ttu-id="25c03-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="25c03-143">RELATED LINKS</span></span>

[<span data-ttu-id="25c03-144">Exportálás – AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="25c03-144">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="25c03-145">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="25c03-145">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="25c03-146">Importálás – AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="25c03-146">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="25c03-147">Új – AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="25c03-147">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="25c03-148">Új – AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="25c03-148">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="25c03-149">Közzététel – AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="25c03-149">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="25c03-150">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="25c03-150">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="25c03-151">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="25c03-151">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)
