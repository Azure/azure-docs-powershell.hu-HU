---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: D704BAC0-D89E-4F15-ACF8-FA2C1F0D1B8F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscCompilationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscCompilationJob.md
ms.openlocfilehash: 59263dab3037e050229bab2a69c43559c2c1827b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500956"
---
# <span data-ttu-id="7ca03-101">Get-AzureRmAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="7ca03-101">Get-AzureRmAutomationDscCompilationJob</span></span>

## <span data-ttu-id="7ca03-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7ca03-102">SYNOPSIS</span></span>
<span data-ttu-id="7ca03-103">A DSC fordítási feladatokat automatizálja az automatizálásban.</span><span class="sxs-lookup"><span data-stu-id="7ca03-103">Gets DSC compilation jobs in Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7ca03-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7ca03-104">SYNTAX</span></span>

### <span data-ttu-id="7ca03-105">ByAll (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7ca03-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationDscCompilationJob [-Status <String>] [-StartTime <DateTimeOffset>]
 [-EndTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7ca03-106">ByJobId</span><span class="sxs-lookup"><span data-stu-id="7ca03-106">ByJobId</span></span>
```
Get-AzureRmAutomationDscCompilationJob -Id <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7ca03-107">ByConfigurationName</span><span class="sxs-lookup"><span data-stu-id="7ca03-107">ByConfigurationName</span></span>
```
Get-AzureRmAutomationDscCompilationJob -ConfigurationName <String> [-Status <String>]
 [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7ca03-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="7ca03-108">DESCRIPTION</span></span>
<span data-ttu-id="7ca03-109">A **Get-AzureRmAutomationDscCompilationJob** parancsmag az Azure automatizálási lehetőségeinek megfelelő állami konfigurációs (DSC) fordítási feladatokat kap.</span><span class="sxs-lookup"><span data-stu-id="7ca03-109">The **Get-AzureRmAutomationDscCompilationJob** cmdlet gets APS Desired State Configuration (DSC) compilation jobs in Azure Automation.</span></span>

## <span data-ttu-id="7ca03-110">Példák</span><span class="sxs-lookup"><span data-stu-id="7ca03-110">EXAMPLES</span></span>

### <span data-ttu-id="7ca03-111">Példa 1: az összes DSC fordítási feladat beszerzése</span><span class="sxs-lookup"><span data-stu-id="7ca03-111">Example 1: Get all DSC compilation jobs</span></span>
```
PS C:\>Get-AzureRmAutomationDscCompilationJob -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="7ca03-112">Ez a parancs a Contoso17 nevű automatizálási fiókban minden fordítási feladatot kap.</span><span class="sxs-lookup"><span data-stu-id="7ca03-112">This command gets all compilation jobs in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="7ca03-113">2. példa: a DSC fordítási feladatok beszerzése egy konfigurációhoz</span><span class="sxs-lookup"><span data-stu-id="7ca03-113">Example 2: Get DSC compilation jobs for a configuration</span></span>
```
PS C:\>Get-AzureRmAutomationDscCompilationJob -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ConfigurationName "ContosoConfiguration"
```

<span data-ttu-id="7ca03-114">Ez a parancs a ContosoConfiguration nevű DSC-konfiguráció minden fordítási feladatát a Contoso17 nevű automatizálási fiókban kapja meg.</span><span class="sxs-lookup"><span data-stu-id="7ca03-114">This command gets all compilation jobs for the DSC configuration named ContosoConfiguration in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="7ca03-115">3. példa: speciális DSC-összeállítási feladat beszerzése</span><span class="sxs-lookup"><span data-stu-id="7ca03-115">Example 3: Get a specific DSC compilation job</span></span>
```
PS C:\>Get-AzureRmAutomationDscCompilationJob -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Id c0a1718e-d8be-4fa3-91b6-82e1d3a36298
```

<span data-ttu-id="7ca03-116">Ez a parancs a Contoso17 nevű automatizálási fiókban megadott AZONOSÍTÓJÚ fordítási feladatot kapja.</span><span class="sxs-lookup"><span data-stu-id="7ca03-116">This command gets the compilation job with the specified ID in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="7ca03-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7ca03-117">PARAMETERS</span></span>

### <span data-ttu-id="7ca03-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="7ca03-118">-AutomationAccountName</span></span>
<span data-ttu-id="7ca03-119">Megadja annak az automatizálási fióknak a nevét, amely a parancsmag által kapott DSC-összeállítási feladatokat tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="7ca03-119">Specifies the name of the Automation account that contains DSC compilation jobs that this cmdlet gets.</span></span>

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

### <span data-ttu-id="7ca03-120">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="7ca03-120">-ConfigurationName</span></span>
<span data-ttu-id="7ca03-121">Annak a DSC-konfigurációnak a neve, amelyhez ez a parancsmag befordítási feladatokat kap.</span><span class="sxs-lookup"><span data-stu-id="7ca03-121">Specifies the name of the DSC configuration for which this cmdlet gets compilation jobs.</span></span>

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

### <span data-ttu-id="7ca03-122">-A befejezési időpont</span><span class="sxs-lookup"><span data-stu-id="7ca03-122">-EndTime</span></span>
<span data-ttu-id="7ca03-123">A befejezési időpontot adja meg.</span><span class="sxs-lookup"><span data-stu-id="7ca03-123">Specifies an end time.</span></span>
<span data-ttu-id="7ca03-124">Ez a parancsmag azokat a fordítási feladatokat kapja meg, amelyek a paraméter által megadott időpontig kezdődtek.</span><span class="sxs-lookup"><span data-stu-id="7ca03-124">This cmdlet gets compilations jobs that started up to the time that this parameter specifies.</span></span>

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

### <span data-ttu-id="7ca03-125">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="7ca03-125">-Id</span></span>
<span data-ttu-id="7ca03-126">Annak a DSC-összeállítási munkának az egyedi AZONOSÍTÓját adja meg, amelyre a parancsmag bekerül.</span><span class="sxs-lookup"><span data-stu-id="7ca03-126">Specifies the unique ID of the DSC compilation job that this cmdlet gets.</span></span>

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

### <span data-ttu-id="7ca03-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ca03-127">-ResourceGroupName</span></span>
<span data-ttu-id="7ca03-128">Annak a csoportnak a nevét adja meg, amelyben a parancsmag a DSC összeállítási feladatokat kapja.</span><span class="sxs-lookup"><span data-stu-id="7ca03-128">Specifies the name of a resource group in which this cmdlet gets DSC compilation jobs.</span></span>

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

### <span data-ttu-id="7ca03-129">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="7ca03-129">-StartTime</span></span>
<span data-ttu-id="7ca03-130">Megadja a kezdés időpontját.</span><span class="sxs-lookup"><span data-stu-id="7ca03-130">Specifies a start time.</span></span>
<span data-ttu-id="7ca03-131">Ez a parancsmag olyan feladatokat kap, amelyek a paraméter által megadott időpontnál vagy azt követően kezdődnek.</span><span class="sxs-lookup"><span data-stu-id="7ca03-131">This cmdlet gets jobs that start at or after the time that this parameter specifies.</span></span>

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

### <span data-ttu-id="7ca03-132">-Állapot</span><span class="sxs-lookup"><span data-stu-id="7ca03-132">-Status</span></span>
<span data-ttu-id="7ca03-133">A parancsmag által kapott feladatok állapotát adja meg.</span><span class="sxs-lookup"><span data-stu-id="7ca03-133">Specifies the status of jobs that this cmdlet gets.</span></span>
<span data-ttu-id="7ca03-134">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="7ca03-134">Valid values are:</span></span> 

- <span data-ttu-id="7ca03-135">Kész</span><span class="sxs-lookup"><span data-stu-id="7ca03-135">Completed</span></span> 
- <span data-ttu-id="7ca03-136">Sikertelen</span><span class="sxs-lookup"><span data-stu-id="7ca03-136">Failed</span></span> 
- <span data-ttu-id="7ca03-137">Várólistán töltött</span><span class="sxs-lookup"><span data-stu-id="7ca03-137">Queued</span></span> 
- <span data-ttu-id="7ca03-138">Kezdve</span><span class="sxs-lookup"><span data-stu-id="7ca03-138">Starting</span></span> 
- <span data-ttu-id="7ca03-139">Újrakezd</span><span class="sxs-lookup"><span data-stu-id="7ca03-139">Resuming</span></span> 
- <span data-ttu-id="7ca03-140">Fut</span><span class="sxs-lookup"><span data-stu-id="7ca03-140">Running</span></span> 
- <span data-ttu-id="7ca03-141">Megállt</span><span class="sxs-lookup"><span data-stu-id="7ca03-141">Stopped</span></span> 
- <span data-ttu-id="7ca03-142">Megállás</span><span class="sxs-lookup"><span data-stu-id="7ca03-142">Stopping</span></span> 
- <span data-ttu-id="7ca03-143">Felfüggesztve</span><span class="sxs-lookup"><span data-stu-id="7ca03-143">Suspended</span></span> 
- <span data-ttu-id="7ca03-144">Indokolva kéri</span><span class="sxs-lookup"><span data-stu-id="7ca03-144">Suspending</span></span> 
- <span data-ttu-id="7ca03-145">Aktiválása</span><span class="sxs-lookup"><span data-stu-id="7ca03-145">Activating</span></span>
- <span data-ttu-id="7ca03-146">Új</span><span class="sxs-lookup"><span data-stu-id="7ca03-146">New</span></span>

```yaml
Type: System.String
Parameter Sets: ByAll, ByConfigurationName
Aliases: 
Accepted values: Completed, Failed, Queued, Starting, Resuming, Running, Stopped, Stopping, Suspended, Suspending, Activating

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ca03-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ca03-147">-DefaultProfile</span></span>
<span data-ttu-id="7ca03-148">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7ca03-148">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7ca03-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ca03-149">CommonParameters</span></span>
<span data-ttu-id="7ca03-150">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7ca03-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ca03-151">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ca03-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ca03-152">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7ca03-152">INPUTS</span></span>

## <span data-ttu-id="7ca03-153">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7ca03-153">OUTPUTS</span></span>

### <span data-ttu-id="7ca03-154">Microsoft. Azure. Command. Automation. Model. CompilationJob</span><span class="sxs-lookup"><span data-stu-id="7ca03-154">Microsoft.Azure.Commands.Automation.Model.CompilationJob</span></span>

## <span data-ttu-id="7ca03-155">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7ca03-155">NOTES</span></span>

## <span data-ttu-id="7ca03-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7ca03-156">RELATED LINKS</span></span>

[<span data-ttu-id="7ca03-157">Get-AzureRmAutomationDscCompilationJobOutput</span><span class="sxs-lookup"><span data-stu-id="7ca03-157">Get-AzureRmAutomationDscCompilationJobOutput</span></span>](./Get-AzureRmAutomationDscCompilationJobOutput.md)

[<span data-ttu-id="7ca03-158">Start-AzureRmAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="7ca03-158">Start-AzureRmAutomationDscCompilationJob</span></span>](./Start-AzureRmAutomationDscCompilationJob.md)


