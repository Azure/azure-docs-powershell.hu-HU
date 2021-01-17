---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationsoftwareupdateconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationSoftwareUpdateConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationSoftwareUpdateConfiguration.md
ms.openlocfilehash: d54acf3ad4e47c173b8ec4ef2fd37145c6dbf198
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98478597"
---
# <span data-ttu-id="8fe24-101">New-AzAutomationSoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="8fe24-101">New-AzAutomationSoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="8fe24-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8fe24-102">SYNOPSIS</span></span>
<span data-ttu-id="8fe24-103">Ütemezett Azure Automatizálási szoftverfrissítés-konfigurációt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="8fe24-103">Creates a scheduled azure automation software update configuration.</span></span>

## <span data-ttu-id="8fe24-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8fe24-104">SYNTAX</span></span>

### <span data-ttu-id="8fe24-105">Windows (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8fe24-105">Windows (Default)</span></span>
```
New-AzAutomationSoftwareUpdateConfiguration -Schedule <Schedule> [-Windows] [-RebootOnly]
 [-AzureVMResourceId <String[]>] [-PreTaskRunbookName <String>] [-PostTaskRunbookName <String>]
 [-PreTaskRunbookParameter <Hashtable>] [-PostTaskRunbookParameter <Hashtable>] [-NonAzureComputer <String[]>]
 [-AzureQuery <AzureQueryProperties[]>] [-NonAzureQuery <NonAzureQueryProperties[]>] [-Duration <TimeSpan>]
 [-RebootSetting <RebootSetting>] [-IncludedUpdateClassification <WindowsUpdateClasses[]>]
 [-ExcludedKbNumber <String[]>] [-IncludedKbNumber <String[]>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8fe24-106">Linux</span><span class="sxs-lookup"><span data-stu-id="8fe24-106">Linux</span></span>
```
New-AzAutomationSoftwareUpdateConfiguration -Schedule <Schedule> [-Linux] [-RebootOnly]
 [-AzureVMResourceId <String[]>] [-PreTaskRunbookName <String>] [-PostTaskRunbookName <String>]
 [-PreTaskRunbookParameter <Hashtable>] [-PostTaskRunbookParameter <Hashtable>] [-NonAzureComputer <String[]>]
 [-AzureQuery <AzureQueryProperties[]>] [-NonAzureQuery <NonAzureQueryProperties[]>] [-Duration <TimeSpan>]
 [-RebootSetting <RebootSetting>] [-IncludedPackageClassification <LinuxPackageClasses[]>]
 [-ExcludedPackageNameMask <String[]>] [-IncludedPackageNameMask <String[]>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8fe24-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8fe24-107">DESCRIPTION</span></span>
<span data-ttu-id="8fe24-108">Olyan szoftverfrissítés-konfigurációt hoz létre, amely ütemezve fut a számítógépek listájának frissítéséhez.</span><span class="sxs-lookup"><span data-stu-id="8fe24-108">Creates a software update configuration that runs on a schedule to update a list of computers.</span></span> <span data-ttu-id="8fe24-109">A számítógépek azure virtuális gépeket vagy nem az ügyfélszámítógépeket is tartalmaznak.</span><span class="sxs-lookup"><span data-stu-id="8fe24-109">Computers include both azure virtual machines or non-az computers.</span></span>

## <span data-ttu-id="8fe24-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8fe24-110">EXAMPLES</span></span>

### <span data-ttu-id="8fe24-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="8fe24-111">Example 1</span></span>
<span data-ttu-id="8fe24-112">Szoftverfrissítéskonfigurációt hoz létre, hogy a kritikus frissítéseket két Windows Azure virtuális gépre telepítse minden szombat 9.09-kor.</span><span class="sxs-lookup"><span data-stu-id="8fe24-112">Creates a software update configuration to install critical updates on two Windows azure virtual machines once every Saturday 9PM.</span></span> <span data-ttu-id="8fe24-113">Ebben a példában a frissítés időtartama 2 órára van állítva.</span><span class="sxs-lookup"><span data-stu-id="8fe24-113">Update duration is set to 2 hours in this example.</span></span>

```powershell
PS C:\> $startTime = [DateTimeOffset]"2018-09-13T21:00"
PS C:\> $targetMachines = @( `
    "/subscriptions/22e2445a-0984-4fa5-86a4-0280d76c4b2c/resourceGroups/compute/providers/Microsoft.Compute/virtualMachines/vm-w-01", `
    "/subscriptions/22e2445a-0984-4fa5-86a4-0280d76c4b2c/resourceGroups/compute/providers/Microsoft.Compute/virtualMachines/vm-w-02"
    )
PS C:\> $duration = New-TimeSpan -Hours 2
PS C:\> $schedule = New-AzAutomationSchedule -ResourceGroupName "mygroup" `
                                                  -AutomationAccountName "myaccount" `
                                                  -Name MyWeeklySchedule `
                                                  -StartTime $startTime `
                                                  -DaysOfWeek Saturday `
                                                  -WeekInterval 1 `
                                                  -ForUpdateConfiguration

New-AzAutomationSoftwareUpdateConfiguration -ResourceGroupName "mygroup" `
                                                 -AutomationAccountName "myaccount" `
                                                 -Schedule $schedule `
                                                 -Windows `
                                                 -AzureVMResourceId $targetMachines `
                                                 -IncludedUpdateClassification Critical `
                                                 -Duration $duration

UpdateConfiguration   : Microsoft.Azure.Commands.Automation.Model.UpdateManagement.UpdateConfiguration
ScheduleConfiguration : Microsoft.Azure.Commands.Automation.Model.Schedule
ProvisioningState     : Provisioning
ErrorInfo             :
ResourceGroupName     : mygroup
AutomationAccountName : myaccount
Name                  : MyWeeklySchedule
CreationTime          : 9/14/2018 3:53:27 AM +00:00
LastModifiedTime      : 9/14/2018 3:53:27 AM +00:00
Description           :
```

## <span data-ttu-id="8fe24-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8fe24-114">PARAMETERS</span></span>

### <span data-ttu-id="8fe24-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="8fe24-115">-AutomationAccountName</span></span>
<span data-ttu-id="8fe24-116">Az automatizálási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="8fe24-116">The automation account name.</span></span>

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

### <span data-ttu-id="8fe24-117">-AzureQuery</span><span class="sxs-lookup"><span data-stu-id="8fe24-117">-AzureQuery</span></span>
<span data-ttu-id="8fe24-118">Dinamikus csoport azure-lekérdezése.</span><span class="sxs-lookup"><span data-stu-id="8fe24-118">Dynamic group azure query.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.UpdateManagement.AzureQueryProperties[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fe24-119">-AzureVMResourceId</span><span class="sxs-lookup"><span data-stu-id="8fe24-119">-AzureVMResourceId</span></span>
<span data-ttu-id="8fe24-120">Azure virtuális gépek erőforrás-azonosítói.</span><span class="sxs-lookup"><span data-stu-id="8fe24-120">Resource Ids for azure virtual machines.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fe24-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fe24-121">-DefaultProfile</span></span>
<span data-ttu-id="8fe24-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8fe24-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fe24-123">-Időtartam</span><span class="sxs-lookup"><span data-stu-id="8fe24-123">-Duration</span></span>
<span data-ttu-id="8fe24-124">A frissítés maximális időtartama.</span><span class="sxs-lookup"><span data-stu-id="8fe24-124">Maximum duration for the update.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fe24-125">-ExcludedKbNumber</span><span class="sxs-lookup"><span data-stu-id="8fe24-125">-ExcludedKbNumber</span></span>
<span data-ttu-id="8fe24-126">A kihagyott frissítések KB-száma.</span><span class="sxs-lookup"><span data-stu-id="8fe24-126">KB numbers of excluded updates.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Windows
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fe24-127">-ExcludedPackageNameMask</span><span class="sxs-lookup"><span data-stu-id="8fe24-127">-ExcludedPackageNameMask</span></span>
<span data-ttu-id="8fe24-128">Kizárt Linux-csomagmaszkok.</span><span class="sxs-lookup"><span data-stu-id="8fe24-128">Excluded Linux package masks.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Linux
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fe24-129">-IncludedKbNumber</span><span class="sxs-lookup"><span data-stu-id="8fe24-129">-IncludedKbNumber</span></span>
<span data-ttu-id="8fe24-130">KB-os számú frissítés.</span><span class="sxs-lookup"><span data-stu-id="8fe24-130">KB numbers of included updates.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Windows
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fe24-131">-IncludedPackageClassification</span><span class="sxs-lookup"><span data-stu-id="8fe24-131">-IncludedPackageClassification</span></span>
<span data-ttu-id="8fe24-132">Linux-csomagbesorolások.</span><span class="sxs-lookup"><span data-stu-id="8fe24-132">Included Linux package classifications.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.UpdateManagement.LinuxPackageClasses[]
Parameter Sets: Linux
Aliases:
Accepted values: Unclassified, Critical, Security, Other

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fe24-133">-IncludedPackageNameMask</span><span class="sxs-lookup"><span data-stu-id="8fe24-133">-IncludedPackageNameMask</span></span>
<span data-ttu-id="8fe24-134">Tartalmazott Linux-csomagmaszkokat.</span><span class="sxs-lookup"><span data-stu-id="8fe24-134">Included Linux package masks.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Linux
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fe24-135">-IncludedUpdateClassification</span><span class="sxs-lookup"><span data-stu-id="8fe24-135">-IncludedUpdateClassification</span></span>
<span data-ttu-id="8fe24-136">Tartalmazza a Windows Update besorolásokat.</span><span class="sxs-lookup"><span data-stu-id="8fe24-136">Included Windows Update classifications.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.UpdateManagement.WindowsUpdateClasses[]
Parameter Sets: Windows
Aliases:
Accepted values: Unclassified, Critical, Security, UpdateRollup, FeaturePack, ServicePack, Definition, Tools, Updates

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fe24-137">-Linux</span><span class="sxs-lookup"><span data-stu-id="8fe24-137">-Linux</span></span>
<span data-ttu-id="8fe24-138">Azt jelzi, hogy a Linux operációs rendszer gépeit megcélzott szoftverfrissítés-konfiguráció.</span><span class="sxs-lookup"><span data-stu-id="8fe24-138">Indicates that the software update configuration targeting Linux operating system machines.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Linux
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fe24-139">-NonAzureComputer</span><span class="sxs-lookup"><span data-stu-id="8fe24-139">-NonAzureComputer</span></span>
<span data-ttu-id="8fe24-140">Nem az az-s számítógépek nevei.</span><span class="sxs-lookup"><span data-stu-id="8fe24-140">Non-Az computer names.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fe24-141">-NonAzureQuery</span><span class="sxs-lookup"><span data-stu-id="8fe24-141">-NonAzureQuery</span></span>
<span data-ttu-id="8fe24-142">Dinamikus csoport, nem Azure-lekérdezés.</span><span class="sxs-lookup"><span data-stu-id="8fe24-142">Dynamic group non Azure query.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.UpdateManagement.NonAzureQueryProperties[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fe24-143">-PostTaskRunbookName</span><span class="sxs-lookup"><span data-stu-id="8fe24-143">-PostTaskRunbookName</span></span>
<span data-ttu-id="8fe24-144">Feladat bejegyzése</span><span class="sxs-lookup"><span data-stu-id="8fe24-144">Post task.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fe24-145">-PostTaskRunbookParameter</span><span class="sxs-lookup"><span data-stu-id="8fe24-145">-PostTaskRunbookParameter</span></span>
<span data-ttu-id="8fe24-146">Feladat paraméterének megadása</span><span class="sxs-lookup"><span data-stu-id="8fe24-146">Post task parameter.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fe24-147">-PreTaskRunbookName</span><span class="sxs-lookup"><span data-stu-id="8fe24-147">-PreTaskRunbookName</span></span>
<span data-ttu-id="8fe24-148">Pre task.</span><span class="sxs-lookup"><span data-stu-id="8fe24-148">Pre task.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fe24-149">-PreTaskRunbookParameter</span><span class="sxs-lookup"><span data-stu-id="8fe24-149">-PreTaskRunbookParameter</span></span>
<span data-ttu-id="8fe24-150">Pre task parameter.</span><span class="sxs-lookup"><span data-stu-id="8fe24-150">Pre task parameter.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fe24-151">-RebootOnly</span><span class="sxs-lookup"><span data-stu-id="8fe24-151">-RebootOnly</span></span>
<span data-ttu-id="8fe24-152">Azt jelzi, hogy a szoftverfrissítések konfigurációja csak a gépeket indítja újra.</span><span class="sxs-lookup"><span data-stu-id="8fe24-152">Indicates that the software update configuration will Only Reboot the machines.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fe24-153">-RebootSetting</span><span class="sxs-lookup"><span data-stu-id="8fe24-153">-RebootSetting</span></span>
<span data-ttu-id="8fe24-154">Indítsa újra a beállítást.</span><span class="sxs-lookup"><span data-stu-id="8fe24-154">Reboot Setting.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.UpdateManagement.RebootSetting
Parameter Sets: (All)
Aliases:
Accepted values: IfRequired, Never, Always, RebootOnly

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fe24-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8fe24-155">-ResourceGroupName</span></span>
<span data-ttu-id="8fe24-156">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="8fe24-156">The resource group name.</span></span>

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

### <span data-ttu-id="8fe24-157">-Schedule</span><span class="sxs-lookup"><span data-stu-id="8fe24-157">-Schedule</span></span>
<span data-ttu-id="8fe24-158">Szoftverfrissítés-konfigurációhoz használt objektum ütemezése.</span><span class="sxs-lookup"><span data-stu-id="8fe24-158">Schedule object used for software update configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.Schedule
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fe24-159">-Windows</span><span class="sxs-lookup"><span data-stu-id="8fe24-159">-Windows</span></span>
<span data-ttu-id="8fe24-160">Azt jelzi, hogy a windows operációs rendszer gépeit megcélzott szoftverfrissítés-konfiguráció.</span><span class="sxs-lookup"><span data-stu-id="8fe24-160">Indicates that the software update configuration targeting windows operating system machines.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fe24-161">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8fe24-161">-Confirm</span></span>
<span data-ttu-id="8fe24-162">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="8fe24-162">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fe24-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8fe24-163">-WhatIf</span></span>
<span data-ttu-id="8fe24-164">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="8fe24-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8fe24-165">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8fe24-165">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fe24-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fe24-166">CommonParameters</span></span>
<span data-ttu-id="8fe24-167">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8fe24-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fe24-168">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8fe24-168">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fe24-169">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8fe24-169">INPUTS</span></span>

### <span data-ttu-id="8fe24-170">Microsoft.Azure.Commands.Automation.Model.Schedule</span><span class="sxs-lookup"><span data-stu-id="8fe24-170">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

### <span data-ttu-id="8fe24-171">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="8fe24-171">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="8fe24-172">System.String[]</span><span class="sxs-lookup"><span data-stu-id="8fe24-172">System.String[]</span></span>

### <span data-ttu-id="8fe24-173">System.TimeSpan</span><span class="sxs-lookup"><span data-stu-id="8fe24-173">System.TimeSpan</span></span>

### <span data-ttu-id="8fe24-174">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.WindowsUpdateClasses[]</span><span class="sxs-lookup"><span data-stu-id="8fe24-174">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.WindowsUpdateClasses[]</span></span>

### <span data-ttu-id="8fe24-175">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.LinuxPackageClasses[]</span><span class="sxs-lookup"><span data-stu-id="8fe24-175">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.LinuxPackageClasses[]</span></span>

### <span data-ttu-id="8fe24-176">System.String</span><span class="sxs-lookup"><span data-stu-id="8fe24-176">System.String</span></span>

## <span data-ttu-id="8fe24-177">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8fe24-177">OUTPUTS</span></span>

### <span data-ttu-id="8fe24-178">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="8fe24-178">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="8fe24-179">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8fe24-179">NOTES</span></span>

## <span data-ttu-id="8fe24-180">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8fe24-180">RELATED LINKS</span></span>
