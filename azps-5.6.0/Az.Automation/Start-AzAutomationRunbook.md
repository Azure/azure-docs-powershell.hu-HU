---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B2D9FF7B-EA3B-4853-814C-00FC4E328957
online version: https://docs.microsoft.com/powershell/module/az.automation/start-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationRunbook.md
ms.openlocfilehash: 00eb652bc9779554f1c860edd503fc752c7ccaa0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921457"
---
# <span data-ttu-id="275ec-101">Start-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="275ec-101">Start-AzAutomationRunbook</span></span>

## <span data-ttu-id="275ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="275ec-102">SYNOPSIS</span></span>
<span data-ttu-id="275ec-103">Futtatásnapló-feladatot kezd.</span><span class="sxs-lookup"><span data-stu-id="275ec-103">Starts a runbook job.</span></span>

## <span data-ttu-id="275ec-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="275ec-104">SYNTAX</span></span>

### <span data-ttu-id="275ec-105">ByAsynchronousReturnSync (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="275ec-105">ByAsynchronousReturnJob (Default)</span></span>
```
Start-AzAutomationRunbook [-Name] <String> [-Parameters <IDictionary>] [-RunOn <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="275ec-106">BySynchronousReturnSyncOutput</span><span class="sxs-lookup"><span data-stu-id="275ec-106">BySynchronousReturnJobOutput</span></span>
```
Start-AzAutomationRunbook [-Name] <String> [-Parameters <IDictionary>] [-RunOn <String>] [-Wait]
 [-MaxWaitSeconds <Int32>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="275ec-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="275ec-107">DESCRIPTION</span></span>
<span data-ttu-id="275ec-108">A **Start-AzAutomationRunbook parancsmag** elindít egy Azure Automation-runbook-feladatot.</span><span class="sxs-lookup"><span data-stu-id="275ec-108">The **Start-AzAutomationRunbook** cmdlet starts an Azure Automation runbook job.</span></span>
<span data-ttu-id="275ec-109">Adja meg a runbook azonosítóját vagy nevét.</span><span class="sxs-lookup"><span data-stu-id="275ec-109">Specify the ID or name of a runbook.</span></span>

## <span data-ttu-id="275ec-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="275ec-110">EXAMPLES</span></span>

### <span data-ttu-id="275ec-111">1. példa: Runbook-feladat kezdése</span><span class="sxs-lookup"><span data-stu-id="275ec-111">Example 1: Start a runbook job</span></span>
```
PS C:\>Start-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="275ec-112">Ez a parancs elindítja a Contoso17 nevű Azure Automation-fiók Runbk01 nevű runbookját.</span><span class="sxs-lookup"><span data-stu-id="275ec-112">This command starts a runbook job for the runbook named Runbk01 in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="275ec-113">2. példa: A Python 2 runbook feladatának kezdése paraméterekkel</span><span class="sxs-lookup"><span data-stu-id="275ec-113">Example 2: Start a Python 2 runbook job with parameters</span></span>
```
PS C:\>Start-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "RunbkPy01" -ResourceGroupName "ResourceGroup01" -Parameters @{"Key1"="ValueForPosition1";"Key2"="ValueForPosition2"}
```

<span data-ttu-id="275ec-114">Ez a parancs elindít egy RunbkPy01 nevű runbookot a Contoso17 nevű Azure Automation-fiókban a "ValueForPosition1" első elhelyezési paraméterként és a másodikhoz az "ValueForPosition2" nevű RunbkPy01 nevű runbookon.</span><span class="sxs-lookup"><span data-stu-id="275ec-114">This command starts a runbook job for the Python 2 runbook named RunbkPy01 in the Azure Automation account named Contoso17 with "ValueForPosition1" as the first positional parameter and "ValueForPosition2" for the second one.</span></span>

### <span data-ttu-id="275ec-115">3. példa: Runbook-feladat kezdése és az eredmények várakozása</span><span class="sxs-lookup"><span data-stu-id="275ec-115">Example 3: Start a runbook job and wait for results</span></span>
```
Start-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01" -MaxWaitSeconds 1000 -Wait
```

<span data-ttu-id="275ec-116">Ez a parancs elindítja a Contoso17 nevű Azure Automation-fiók Runbk01 nevű runbookját.</span><span class="sxs-lookup"><span data-stu-id="275ec-116">This command starts a runbook job for the runbook named Runbk01 in the Azure Automation account named Contoso17.</span></span>
<span data-ttu-id="275ec-117">Ez a parancs a _Várakozás paramétert adja_ meg.</span><span class="sxs-lookup"><span data-stu-id="275ec-117">This command specifies the _Wait_ parameter.</span></span>
<span data-ttu-id="275ec-118">Ezért a feladat befejezése után visszaadja az eredményeket.</span><span class="sxs-lookup"><span data-stu-id="275ec-118">Therefore, it returns results after the job is completed.</span></span>
<span data-ttu-id="275ec-119">A parancsmag legfeljebb 1000 másodpercet vár az eredményekre.</span><span class="sxs-lookup"><span data-stu-id="275ec-119">The cmdlet waits up to 1000 seconds for the results.</span></span>

## <span data-ttu-id="275ec-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="275ec-120">PARAMETERS</span></span>

### <span data-ttu-id="275ec-121">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="275ec-121">-AutomationAccountName</span></span>
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

### <span data-ttu-id="275ec-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="275ec-122">-DefaultProfile</span></span>
<span data-ttu-id="275ec-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="275ec-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="275ec-124">-MaxWaitSeconds</span><span class="sxs-lookup"><span data-stu-id="275ec-124">-MaxWaitSeconds</span></span>
<span data-ttu-id="275ec-125">Azt adja meg, hogy ez a parancsmag hány másodpercig vár egy feladat befejezésére, mielőtt lemondja a feladatot.</span><span class="sxs-lookup"><span data-stu-id="275ec-125">Specifies the number of seconds this cmdlet waits for a job to finish before it abandons the job.</span></span>
<span data-ttu-id="275ec-126">Az alapértelmezett érték 10800 vagy három óra.</span><span class="sxs-lookup"><span data-stu-id="275ec-126">The default value is 10800, or three hours.</span></span>

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

### <span data-ttu-id="275ec-127">-Name</span><span class="sxs-lookup"><span data-stu-id="275ec-127">-Name</span></span>
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

### <span data-ttu-id="275ec-128">-Parameters</span><span class="sxs-lookup"><span data-stu-id="275ec-128">-Parameters</span></span>
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

### <span data-ttu-id="275ec-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="275ec-129">-ResourceGroupName</span></span>
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

### <span data-ttu-id="275ec-130">-RunOn</span><span class="sxs-lookup"><span data-stu-id="275ec-130">-RunOn</span></span>
<span data-ttu-id="275ec-131">Meghatározza, hogy melyik hibrid dolgozócsoporton futtassa a runbookot.</span><span class="sxs-lookup"><span data-stu-id="275ec-131">Specifies which Hybrid Worker Group on which to run the runbook.</span></span>

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

### <span data-ttu-id="275ec-132">-Wait</span><span class="sxs-lookup"><span data-stu-id="275ec-132">-Wait</span></span>
<span data-ttu-id="275ec-133">Azt jelzi, hogy ez a parancsmag megvárja a feladat befejezését, felfüggesztését vagy sikertelen befejezését, majd visszaadja az irányítást az Azure PowerShellnek.</span><span class="sxs-lookup"><span data-stu-id="275ec-133">Indicates that this cmdlet waits for job to complete, suspend, or fail, and then returns control to Azure PowerShell.</span></span>

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

### <span data-ttu-id="275ec-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="275ec-134">CommonParameters</span></span>
<span data-ttu-id="275ec-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="275ec-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="275ec-136">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="275ec-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="275ec-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="275ec-137">INPUTS</span></span>

### <span data-ttu-id="275ec-138">System.String</span><span class="sxs-lookup"><span data-stu-id="275ec-138">System.String</span></span>

## <span data-ttu-id="275ec-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="275ec-139">OUTPUTS</span></span>

### <span data-ttu-id="275ec-140">Microsoft.Azure.Commands.Automation.Model.Job</span><span class="sxs-lookup"><span data-stu-id="275ec-140">Microsoft.Azure.Commands.Automation.Model.Job</span></span>

### <span data-ttu-id="275ec-141">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="275ec-141">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="275ec-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="275ec-142">NOTES</span></span>

## <span data-ttu-id="275ec-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="275ec-143">RELATED LINKS</span></span>

[<span data-ttu-id="275ec-144">Export-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="275ec-144">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="275ec-145">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="275ec-145">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="275ec-146">Import-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="275ec-146">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="275ec-147">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="275ec-147">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="275ec-148">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="275ec-148">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="275ec-149">Publish-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="275ec-149">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="275ec-150">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="275ec-150">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="275ec-151">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="275ec-151">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)
