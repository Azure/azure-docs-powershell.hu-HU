---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B2D9FF7B-EA3B-4853-814C-00FC4E328957
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Start-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Start-AzureRMAutomationRunbook.md
ms.openlocfilehash: c84410a38cb803eab9dbe4866c7a9426c9c3a21d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493868"
---
# <span data-ttu-id="6853a-101">Start-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="6853a-101">Start-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="6853a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6853a-102">SYNOPSIS</span></span>
<span data-ttu-id="6853a-103">Elindít egy runbook-feladatot.</span><span class="sxs-lookup"><span data-stu-id="6853a-103">Starts a runbook job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6853a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6853a-104">SYNTAX</span></span>

### <span data-ttu-id="6853a-105">ByAsynchronousReturnJob (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6853a-105">ByAsynchronousReturnJob (Default)</span></span>
```
Start-AzureRmAutomationRunbook [-Name] <String> [-Parameters <IDictionary>] [-RunOn <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6853a-106">BySynchronousReturnJobOutput</span><span class="sxs-lookup"><span data-stu-id="6853a-106">BySynchronousReturnJobOutput</span></span>
```
Start-AzureRmAutomationRunbook [-Name] <String> [-Parameters <IDictionary>] [-RunOn <String>] [-Wait]
 [-MaxWaitSeconds <Int32>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6853a-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="6853a-107">DESCRIPTION</span></span>
<span data-ttu-id="6853a-108">A **Start-AzureRmAutomationRunbook** parancsmag az Azure automatizálási runbook feladatát indítja el.</span><span class="sxs-lookup"><span data-stu-id="6853a-108">The **Start-AzureRmAutomationRunbook** cmdlet starts an Azure Automation runbook job.</span></span>
<span data-ttu-id="6853a-109">Adja meg a runbook AZONOSÍTÓját vagy nevét.</span><span class="sxs-lookup"><span data-stu-id="6853a-109">Specify the ID or name of a runbook.</span></span>

## <span data-ttu-id="6853a-110">Példák</span><span class="sxs-lookup"><span data-stu-id="6853a-110">EXAMPLES</span></span>

### <span data-ttu-id="6853a-111">1. példa: runbook-feladat indítása</span><span class="sxs-lookup"><span data-stu-id="6853a-111">Example 1: Start a runbook job</span></span>
```
PS C:\>Start-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="6853a-112">Ez a parancs runbook-feladatot indít az Contoso17 nevű Azure Automation fiók Runbk01 nevű runbook.</span><span class="sxs-lookup"><span data-stu-id="6853a-112">This command starts a runbook job for the runbook named Runbk01 in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="6853a-113">2. példa: runbook feladat indítása és várakozás az eredményre</span><span class="sxs-lookup"><span data-stu-id="6853a-113">Example 2: Start a runbook job and wait for results</span></span>
```
Start-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01" -MaxWaitSeconds 1000 -Wait
```

<span data-ttu-id="6853a-114">Ez a parancs runbook-feladatot indít az Contoso17 nevű Azure Automation fiók Runbk01 nevű runbook.</span><span class="sxs-lookup"><span data-stu-id="6853a-114">This command starts a runbook job for the runbook named Runbk01 in the Azure Automation account named Contoso17.</span></span>
<span data-ttu-id="6853a-115">Ez a parancs a _várakozási_ paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="6853a-115">This command specifies the _Wait_ parameter.</span></span>
<span data-ttu-id="6853a-116">Így a feladat befejezését követően eredményül ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="6853a-116">Therefore, it returns results after the job is completed.</span></span>
<span data-ttu-id="6853a-117">A parancsmag az eredményhez legfeljebb 1000 másodpercet vár.</span><span class="sxs-lookup"><span data-stu-id="6853a-117">The cmdlet waits up to 1000 seconds for the results.</span></span>

## <span data-ttu-id="6853a-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6853a-118">PARAMETERS</span></span>

### <span data-ttu-id="6853a-119">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="6853a-119">-AutomationAccountName</span></span>
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

### <span data-ttu-id="6853a-120">-MaxWaitSeconds</span><span class="sxs-lookup"><span data-stu-id="6853a-120">-MaxWaitSeconds</span></span>
<span data-ttu-id="6853a-121">Azt adja meg, hogy hány másodpercig tart a parancsmag, mielőtt felhagyják a feladatot.</span><span class="sxs-lookup"><span data-stu-id="6853a-121">Specifies the number of seconds this cmdlet waits for a job to finish before it abandons the job.</span></span>
<span data-ttu-id="6853a-122">Az alapértelmezett érték a 10800, vagy három óra.</span><span class="sxs-lookup"><span data-stu-id="6853a-122">The default value is 10800, or three hours.</span></span>

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

### <span data-ttu-id="6853a-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6853a-123">-Name</span></span>
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

### <span data-ttu-id="6853a-124">-Paraméterek</span><span class="sxs-lookup"><span data-stu-id="6853a-124">-Parameters</span></span>
```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6853a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6853a-125">-ResourceGroupName</span></span>
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

### <span data-ttu-id="6853a-126">-RunOn</span><span class="sxs-lookup"><span data-stu-id="6853a-126">-RunOn</span></span>
<span data-ttu-id="6853a-127">Annak megadása, hogy melyik hibrid munkacsoportot szeretné futtatni a runbook.</span><span class="sxs-lookup"><span data-stu-id="6853a-127">Specifies which Hybrid Worker Group on which to run the runbook.</span></span>

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

### <span data-ttu-id="6853a-128">– Várjon</span><span class="sxs-lookup"><span data-stu-id="6853a-128">-Wait</span></span>
<span data-ttu-id="6853a-129">Jelzi, hogy ez a parancsmag várja a feladatok befejezését, felfüggesztését vagy sikertelenségét, majd visszaadja az Azure PowerShell-vezérlőt.</span><span class="sxs-lookup"><span data-stu-id="6853a-129">Indicates that this cmdlet waits for job to complete, suspend, or fail, and then returns control to Azure PowerShell.</span></span>

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

### <span data-ttu-id="6853a-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6853a-130">-DefaultProfile</span></span>
<span data-ttu-id="6853a-131">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6853a-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6853a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6853a-132">CommonParameters</span></span>
<span data-ttu-id="6853a-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6853a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6853a-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6853a-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6853a-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6853a-135">INPUTS</span></span>

## <span data-ttu-id="6853a-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6853a-136">OUTPUTS</span></span>

### <span data-ttu-id="6853a-137">Microsoft. Azure. Command. Automation. Model. job</span><span class="sxs-lookup"><span data-stu-id="6853a-137">Microsoft.Azure.Commands.Automation.Model.Job</span></span>
<span data-ttu-id="6853a-138">Ez a parancsmag akkor ad eredményül egy **Projektfeladat** -objektumot, ha a _várakozási_ paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="6853a-138">This cmdlet returns a **Job** object, unless you specify the _Wait_ parameter.</span></span>

<span data-ttu-id="6853a-139">Ha nem adja meg a _várakozást_ **, az Azure** PowerShell azonnal visszaadja a munkaobjektumot.</span><span class="sxs-lookup"><span data-stu-id="6853a-139">If you do not specify _Wait_ , Azure PowerShell returns a **Job** object immediately.</span></span>
<span data-ttu-id="6853a-140">Ha a _várakozást_ adja meg, az Azure PowerShell végrehajtja a feladatot, majd az eredményt adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="6853a-140">If you specify _Wait_ , Azure PowerShell completes the job, and then returns the result.</span></span>
<span data-ttu-id="6853a-141">Az eredmény nem a **projekt** objektum.</span><span class="sxs-lookup"><span data-stu-id="6853a-141">The result is not a **Job** object.</span></span>

## <span data-ttu-id="6853a-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6853a-142">NOTES</span></span>

## <span data-ttu-id="6853a-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6853a-143">RELATED LINKS</span></span>

[<span data-ttu-id="6853a-144">Exportálás – AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="6853a-144">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="6853a-145">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="6853a-145">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="6853a-146">Importálás – AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="6853a-146">Import-AzureRmAutomationRunbook</span></span>](./Import-AzureRMAutomationRunbook.md)

[<span data-ttu-id="6853a-147">Új – AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="6853a-147">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="6853a-148">Új – AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="6853a-148">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="6853a-149">Közzététel – AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="6853a-149">Publish-AzureRmAutomationRunbook</span></span>](./Publish-AzureRMAutomationRunbook.md)

[<span data-ttu-id="6853a-150">Remove-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="6853a-150">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="6853a-151">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="6853a-151">Set-AzureRmAutomationRunbook</span></span>](./Set-AzureRMAutomationRunbook.md)
