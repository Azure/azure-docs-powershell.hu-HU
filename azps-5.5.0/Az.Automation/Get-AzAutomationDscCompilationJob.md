---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: D704BAC0-D89E-4F15-ACF8-FA2C1F0D1B8F
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdsccompilationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscCompilationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscCompilationJob.md
ms.openlocfilehash: 5b2c8685596771cd7986d8cfa071808daa63435c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100149426"
---
# <span data-ttu-id="98a35-101">Get-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="98a35-101">Get-AzAutomationDscCompilationJob</span></span>

## <span data-ttu-id="98a35-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="98a35-102">SYNOPSIS</span></span>
<span data-ttu-id="98a35-103">DSC-fordítási feladatokat kap az automatizálásban.</span><span class="sxs-lookup"><span data-stu-id="98a35-103">Gets DSC compilation jobs in Automation.</span></span>

## <span data-ttu-id="98a35-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="98a35-104">SYNTAX</span></span>

### <span data-ttu-id="98a35-105">ByAll (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="98a35-105">ByAll (Default)</span></span>
```
Get-AzAutomationDscCompilationJob [-Status <String>] [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="98a35-106">ByJobId</span><span class="sxs-lookup"><span data-stu-id="98a35-106">ByJobId</span></span>
```
Get-AzAutomationDscCompilationJob -Id <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="98a35-107">ByConfigurationName</span><span class="sxs-lookup"><span data-stu-id="98a35-107">ByConfigurationName</span></span>
```
Get-AzAutomationDscCompilationJob -ConfigurationName <String> [-Status <String>] [-StartTime <DateTimeOffset>]
 [-EndTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="98a35-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="98a35-108">DESCRIPTION</span></span>
<span data-ttu-id="98a35-109">A **Get-AzAutomationDscCompilation Parancsmag** az APS kívánt államkonfigurációs (DSC) fordítási feladatokat kap az Azure Automationben.</span><span class="sxs-lookup"><span data-stu-id="98a35-109">The **Get-AzAutomationDscCompilationJob** cmdlet gets APS Desired State Configuration (DSC) compilation jobs in Azure Automation.</span></span>

## <span data-ttu-id="98a35-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="98a35-110">EXAMPLES</span></span>

### <span data-ttu-id="98a35-111">1. példa: Az összes DSC-fordítási feladat lekérte</span><span class="sxs-lookup"><span data-stu-id="98a35-111">Example 1: Get all DSC compilation jobs</span></span>
```
PS C:\>Get-AzAutomationDscCompilationJob -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="98a35-112">Ez a parancs a Contoso17 nevű automatizálási fiók összes fordítási feladatát beveszi.</span><span class="sxs-lookup"><span data-stu-id="98a35-112">This command gets all compilation jobs in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="98a35-113">2. példa: A DSC összeállítási feladatának lekért beállítása konfigurációhoz</span><span class="sxs-lookup"><span data-stu-id="98a35-113">Example 2: Get DSC compilation jobs for a configuration</span></span>
```
PS C:\>Get-AzAutomationDscCompilationJob -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ConfigurationName "ContosoConfiguration"
```

<span data-ttu-id="98a35-114">Ez a parancs a Contoso17 nevű automatizálási fiók ContosoConfiguration nevű DSC-konfigurációjának összes fordítási feladatát beállítja.</span><span class="sxs-lookup"><span data-stu-id="98a35-114">This command gets all compilation jobs for the DSC configuration named ContosoConfiguration in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="98a35-115">3. példa: Adott fordítási feladat lekérte a DSC-t</span><span class="sxs-lookup"><span data-stu-id="98a35-115">Example 3: Get a specific DSC compilation job</span></span>
```
PS C:\>Get-AzAutomationDscCompilationJob -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Id c0a1718e-d8be-4fa3-91b6-82e1d3a36298
```

<span data-ttu-id="98a35-116">Ez a parancs a Contoso17 nevű automatizálási fiókban megadott azonosítójú fordítási feladatot kapja meg.</span><span class="sxs-lookup"><span data-stu-id="98a35-116">This command gets the compilation job with the specified ID in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="98a35-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="98a35-117">PARAMETERS</span></span>

### <span data-ttu-id="98a35-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="98a35-118">-AutomationAccountName</span></span>
<span data-ttu-id="98a35-119">Annak az automatizálási fióknak a nevét adja meg, amely a parancsmag által lekért DSC-fordítási feladatokat tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="98a35-119">Specifies the name of the Automation account that contains DSC compilation jobs that this cmdlet gets.</span></span>

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

### <span data-ttu-id="98a35-120">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="98a35-120">-ConfigurationName</span></span>
<span data-ttu-id="98a35-121">Annak a DSC-konfigurációnak a nevét adja meg, amelyhez a parancsmag fordítási feladatokat kap.</span><span class="sxs-lookup"><span data-stu-id="98a35-121">Specifies the name of the DSC configuration for which this cmdlet gets compilation jobs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByConfigurationName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98a35-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98a35-122">-DefaultProfile</span></span>
<span data-ttu-id="98a35-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="98a35-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="98a35-124">-EndTime</span><span class="sxs-lookup"><span data-stu-id="98a35-124">-EndTime</span></span>
<span data-ttu-id="98a35-125">A záró időpont megadása.</span><span class="sxs-lookup"><span data-stu-id="98a35-125">Specifies an end time.</span></span>
<span data-ttu-id="98a35-126">Ez a parancsmag olyan összeállítási feladatokat ad vissza, amelyek a paraméter által megadott időpontig elkezdődöttek.</span><span class="sxs-lookup"><span data-stu-id="98a35-126">This cmdlet gets compilations jobs that started up to the time that this parameter specifies.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll, ByConfigurationName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98a35-127">-Id</span><span class="sxs-lookup"><span data-stu-id="98a35-127">-Id</span></span>
<span data-ttu-id="98a35-128">A parancsmag által lekért fordítási DSC-feladat egyedi azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="98a35-128">Specifies the unique ID of the DSC compilation job that this cmdlet gets.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ByJobId
Aliases: JobId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98a35-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98a35-129">-ResourceGroupName</span></span>
<span data-ttu-id="98a35-130">Annak az erőforráscsoportnak a nevét adja meg, amelyben ez a parancsmag DSC-fordítási feladatokat kap.</span><span class="sxs-lookup"><span data-stu-id="98a35-130">Specifies the name of a resource group in which this cmdlet gets DSC compilation jobs.</span></span>

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

### <span data-ttu-id="98a35-131">-StartTime</span><span class="sxs-lookup"><span data-stu-id="98a35-131">-StartTime</span></span>
<span data-ttu-id="98a35-132">Megadja a kezdési időt.</span><span class="sxs-lookup"><span data-stu-id="98a35-132">Specifies a start time.</span></span>
<span data-ttu-id="98a35-133">Ez a parancsmag olyan feladatokat kap, amelyek a paraméter megadásakor vagy után kezdődnek.</span><span class="sxs-lookup"><span data-stu-id="98a35-133">This cmdlet gets jobs that start at or after the time that this parameter specifies.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll, ByConfigurationName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98a35-134">-Állapot</span><span class="sxs-lookup"><span data-stu-id="98a35-134">-Status</span></span>
<span data-ttu-id="98a35-135">A parancsmag által lekért feladatok állapotát adja meg.</span><span class="sxs-lookup"><span data-stu-id="98a35-135">Specifies the status of jobs that this cmdlet gets.</span></span>
<span data-ttu-id="98a35-136">Érvényes értékek:</span><span class="sxs-lookup"><span data-stu-id="98a35-136">Valid values are:</span></span> 
- <span data-ttu-id="98a35-137">Befejezve</span><span class="sxs-lookup"><span data-stu-id="98a35-137">Completed</span></span> 
- <span data-ttu-id="98a35-138">Sikertelen</span><span class="sxs-lookup"><span data-stu-id="98a35-138">Failed</span></span> 
- <span data-ttu-id="98a35-139">Várólistán</span><span class="sxs-lookup"><span data-stu-id="98a35-139">Queued</span></span> 
- <span data-ttu-id="98a35-140">Indítás</span><span class="sxs-lookup"><span data-stu-id="98a35-140">Starting</span></span> 
- <span data-ttu-id="98a35-141">Visszaúszás</span><span class="sxs-lookup"><span data-stu-id="98a35-141">Resuming</span></span> 
- <span data-ttu-id="98a35-142">Fut</span><span class="sxs-lookup"><span data-stu-id="98a35-142">Running</span></span> 
- <span data-ttu-id="98a35-143">Leállítva</span><span class="sxs-lookup"><span data-stu-id="98a35-143">Stopped</span></span> 
- <span data-ttu-id="98a35-144">Leállítás</span><span class="sxs-lookup"><span data-stu-id="98a35-144">Stopping</span></span> 
- <span data-ttu-id="98a35-145">Felfüggesztve</span><span class="sxs-lookup"><span data-stu-id="98a35-145">Suspended</span></span> 
- <span data-ttu-id="98a35-146">Felfüggesztés</span><span class="sxs-lookup"><span data-stu-id="98a35-146">Suspending</span></span> 
- <span data-ttu-id="98a35-147">Aktiválás</span><span class="sxs-lookup"><span data-stu-id="98a35-147">Activating</span></span>
- <span data-ttu-id="98a35-148">Új</span><span class="sxs-lookup"><span data-stu-id="98a35-148">New</span></span>

```yaml
Type: System.String
Parameter Sets: ByAll, ByConfigurationName
Aliases:
Accepted values: Completed, Failed, Queued, Starting, Resuming, Running, Stopped, Stopping, Suspended, Suspending, Activating, New

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98a35-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98a35-149">CommonParameters</span></span>
<span data-ttu-id="98a35-150">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98a35-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98a35-151">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98a35-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98a35-152">INPUTS</span><span class="sxs-lookup"><span data-stu-id="98a35-152">INPUTS</span></span>

### <span data-ttu-id="98a35-153">System.Guid</span><span class="sxs-lookup"><span data-stu-id="98a35-153">System.Guid</span></span>

### <span data-ttu-id="98a35-154">System.String</span><span class="sxs-lookup"><span data-stu-id="98a35-154">System.String</span></span>

## <span data-ttu-id="98a35-155">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="98a35-155">OUTPUTS</span></span>

### <span data-ttu-id="98a35-156">Microsoft.Azure.Commands.Automation.Model.CompilationJob</span><span class="sxs-lookup"><span data-stu-id="98a35-156">Microsoft.Azure.Commands.Automation.Model.CompilationJob</span></span>

## <span data-ttu-id="98a35-157">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="98a35-157">NOTES</span></span>

## <span data-ttu-id="98a35-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="98a35-158">RELATED LINKS</span></span>

[<span data-ttu-id="98a35-159">Get-AzAutomationDscCompilationPut</span><span class="sxs-lookup"><span data-stu-id="98a35-159">Get-AzAutomationDscCompilationJobOutput</span></span>](./Get-AzAutomationDscCompilationJobOutput.md)

[<span data-ttu-id="98a35-160">Start-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="98a35-160">Start-AzAutomationDscCompilationJob</span></span>](./Start-AzAutomationDscCompilationJob.md)


