---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B2D9FF7B-EA3B-4853-814C-00FC4E328957
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/start-azurermautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Start-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Start-AzureRMAutomationRunbook.md
ms.openlocfilehash: c3c59c8c4f503b090a77a93014f50dd7e2ce01dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494575"
---
# <span data-ttu-id="47c87-101">Start-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="47c87-101">Start-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="47c87-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="47c87-102">SYNOPSIS</span></span>
<span data-ttu-id="47c87-103">Elindít egy runbook-feladatot.</span><span class="sxs-lookup"><span data-stu-id="47c87-103">Starts a runbook job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="47c87-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="47c87-104">SYNTAX</span></span>

### <span data-ttu-id="47c87-105">ByAsynchronousReturnJob (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="47c87-105">ByAsynchronousReturnJob (Default)</span></span>
```
Start-AzureRmAutomationRunbook [-Name] <String> [-Parameters <IDictionary>] [-RunOn <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="47c87-106">BySynchronousReturnJobOutput</span><span class="sxs-lookup"><span data-stu-id="47c87-106">BySynchronousReturnJobOutput</span></span>
```
Start-AzureRmAutomationRunbook [-Name] <String> [-Parameters <IDictionary>] [-RunOn <String>] [-Wait]
 [-MaxWaitSeconds <Int32>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="47c87-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="47c87-107">DESCRIPTION</span></span>
<span data-ttu-id="47c87-108">A **Start-AzureRmAutomationRunbook** parancsmag az Azure automatizálási runbook feladatát indítja el.</span><span class="sxs-lookup"><span data-stu-id="47c87-108">The **Start-AzureRmAutomationRunbook** cmdlet starts an Azure Automation runbook job.</span></span>
<span data-ttu-id="47c87-109">Adja meg a runbook AZONOSÍTÓját vagy nevét.</span><span class="sxs-lookup"><span data-stu-id="47c87-109">Specify the ID or name of a runbook.</span></span>

## <span data-ttu-id="47c87-110">Példák</span><span class="sxs-lookup"><span data-stu-id="47c87-110">EXAMPLES</span></span>

### <span data-ttu-id="47c87-111">1. példa: runbook-feladat indítása</span><span class="sxs-lookup"><span data-stu-id="47c87-111">Example 1: Start a runbook job</span></span>
```
PS C:\>Start-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="47c87-112">Ez a parancs runbook-feladatot indít az Contoso17 nevű Azure Automation fiók Runbk01 nevű runbook.</span><span class="sxs-lookup"><span data-stu-id="47c87-112">This command starts a runbook job for the runbook named Runbk01 in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="47c87-113">2. példa: runbook feladat indítása és várakozás az eredményre</span><span class="sxs-lookup"><span data-stu-id="47c87-113">Example 2: Start a runbook job and wait for results</span></span>
```
Start-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01" -MaxWaitSeconds 1000 -Wait
```

<span data-ttu-id="47c87-114">Ez a parancs runbook-feladatot indít az Contoso17 nevű Azure Automation fiók Runbk01 nevű runbook.</span><span class="sxs-lookup"><span data-stu-id="47c87-114">This command starts a runbook job for the runbook named Runbk01 in the Azure Automation account named Contoso17.</span></span>
<span data-ttu-id="47c87-115">Ez a parancs a _várakozási_ paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="47c87-115">This command specifies the _Wait_ parameter.</span></span>
<span data-ttu-id="47c87-116">Így a feladat befejezését követően eredményül ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="47c87-116">Therefore, it returns results after the job is completed.</span></span>
<span data-ttu-id="47c87-117">A parancsmag az eredményhez legfeljebb 1000 másodpercet vár.</span><span class="sxs-lookup"><span data-stu-id="47c87-117">The cmdlet waits up to 1000 seconds for the results.</span></span>

## <span data-ttu-id="47c87-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="47c87-118">PARAMETERS</span></span>

### <span data-ttu-id="47c87-119">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="47c87-119">-AutomationAccountName</span></span>
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

### <span data-ttu-id="47c87-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47c87-120">-DefaultProfile</span></span>
<span data-ttu-id="47c87-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="47c87-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="47c87-122">-MaxWaitSeconds</span><span class="sxs-lookup"><span data-stu-id="47c87-122">-MaxWaitSeconds</span></span>
<span data-ttu-id="47c87-123">Azt adja meg, hogy hány másodpercig tart a parancsmag, mielőtt felhagyják a feladatot.</span><span class="sxs-lookup"><span data-stu-id="47c87-123">Specifies the number of seconds this cmdlet waits for a job to finish before it abandons the job.</span></span>
<span data-ttu-id="47c87-124">Az alapértelmezett érték a 10800, vagy három óra.</span><span class="sxs-lookup"><span data-stu-id="47c87-124">The default value is 10800, or three hours.</span></span>

```yaml
Type: Int32
Parameter Sets: BySynchronousReturnJobOutput
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47c87-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="47c87-125">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: RunbookName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47c87-126">-Paraméterek</span><span class="sxs-lookup"><span data-stu-id="47c87-126">-Parameters</span></span>
```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47c87-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47c87-127">-ResourceGroupName</span></span>
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

### <span data-ttu-id="47c87-128">-RunOn</span><span class="sxs-lookup"><span data-stu-id="47c87-128">-RunOn</span></span>
<span data-ttu-id="47c87-129">Annak megadása, hogy melyik hibrid munkacsoportot szeretné futtatni a runbook.</span><span class="sxs-lookup"><span data-stu-id="47c87-129">Specifies which Hybrid Worker Group on which to run the runbook.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: HybridWorker

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47c87-130">– Várjon</span><span class="sxs-lookup"><span data-stu-id="47c87-130">-Wait</span></span>
<span data-ttu-id="47c87-131">Jelzi, hogy ez a parancsmag várja a feladatok befejezését, felfüggesztését vagy sikertelenségét, majd visszaadja az Azure PowerShell-vezérlőt.</span><span class="sxs-lookup"><span data-stu-id="47c87-131">Indicates that this cmdlet waits for job to complete, suspend, or fail, and then returns control to Azure PowerShell.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: BySynchronousReturnJobOutput
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47c87-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47c87-132">CommonParameters</span></span>
<span data-ttu-id="47c87-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="47c87-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47c87-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47c87-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47c87-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="47c87-135">INPUTS</span></span>

### <span data-ttu-id="47c87-136">Nincs</span><span class="sxs-lookup"><span data-stu-id="47c87-136">None</span></span>
<span data-ttu-id="47c87-137">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="47c87-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="47c87-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="47c87-138">OUTPUTS</span></span>

### <span data-ttu-id="47c87-139">Microsoft. Azure. Command. Automation. Model. job</span><span class="sxs-lookup"><span data-stu-id="47c87-139">Microsoft.Azure.Commands.Automation.Model.Job</span></span>
<span data-ttu-id="47c87-140">Ez a parancsmag akkor ad eredményül egy **Projektfeladat** -objektumot, ha a _várakozási_ paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="47c87-140">This cmdlet returns a **Job** object, unless you specify the _Wait_ parameter.</span></span>

<span data-ttu-id="47c87-141">Ha nem adja meg a _várakozást_ **, az Azure** PowerShell azonnal visszaadja a munkaobjektumot.</span><span class="sxs-lookup"><span data-stu-id="47c87-141">If you do not specify _Wait_ , Azure PowerShell returns a **Job** object immediately.</span></span>
<span data-ttu-id="47c87-142">Ha a _várakozást_ adja meg, az Azure PowerShell végrehajtja a feladatot, majd az eredményt adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="47c87-142">If you specify _Wait_ , Azure PowerShell completes the job, and then returns the result.</span></span>
<span data-ttu-id="47c87-143">Az eredmény nem a **projekt** objektum.</span><span class="sxs-lookup"><span data-stu-id="47c87-143">The result is not a **Job** object.</span></span>

## <span data-ttu-id="47c87-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="47c87-144">NOTES</span></span>

## <span data-ttu-id="47c87-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="47c87-145">RELATED LINKS</span></span>

[<span data-ttu-id="47c87-146">Exportálás – AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="47c87-146">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="47c87-147">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="47c87-147">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="47c87-148">Importálás – AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="47c87-148">Import-AzureRmAutomationRunbook</span></span>](./Import-AzureRMAutomationRunbook.md)

[<span data-ttu-id="47c87-149">Új – AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="47c87-149">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="47c87-150">Új – AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="47c87-150">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="47c87-151">Közzététel – AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="47c87-151">Publish-AzureRmAutomationRunbook</span></span>](./Publish-AzureRMAutomationRunbook.md)

[<span data-ttu-id="47c87-152">Remove-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="47c87-152">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="47c87-153">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="47c87-153">Set-AzureRmAutomationRunbook</span></span>](./Set-AzureRMAutomationRunbook.md)
