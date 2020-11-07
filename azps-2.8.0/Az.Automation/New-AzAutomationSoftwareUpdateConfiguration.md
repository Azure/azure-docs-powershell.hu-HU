---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationsoftwareupdateconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationSoftwareUpdateConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationSoftwareUpdateConfiguration.md
ms.openlocfilehash: f441df5be99764f9582939d4c4d5d422ea88c97f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667795"
---
# <span data-ttu-id="9fc77-101">New-AzAutomationSoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="9fc77-101">New-AzAutomationSoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="9fc77-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9fc77-102">SYNOPSIS</span></span>
<span data-ttu-id="9fc77-103">Ütemezett Azure automatizálási szoftverfrissítési konfigurációt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="9fc77-103">Creates a scheduled azure automation software update configuration.</span></span>

## <span data-ttu-id="9fc77-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9fc77-104">SYNTAX</span></span>

### <span data-ttu-id="9fc77-105">Windows (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9fc77-105">Windows (Default)</span></span>
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

### <span data-ttu-id="9fc77-106">Linux</span><span class="sxs-lookup"><span data-stu-id="9fc77-106">Linux</span></span>
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

## <span data-ttu-id="9fc77-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="9fc77-107">DESCRIPTION</span></span>
<span data-ttu-id="9fc77-108">Egy, az ütemterven futó szoftverfrissítési konfigurációt hoz létre a számítógépek listájának frissítéséhez.</span><span class="sxs-lookup"><span data-stu-id="9fc77-108">Creates a software update configuration that runs on a schedule to update a list of computers.</span></span> <span data-ttu-id="9fc77-109">A számítógépeken az Azure virtuális gépek vagy a nem a számítógépek is szerepelnek.</span><span class="sxs-lookup"><span data-stu-id="9fc77-109">Computers include both azure virtual machines or non-az computers.</span></span>

## <span data-ttu-id="9fc77-110">Példák</span><span class="sxs-lookup"><span data-stu-id="9fc77-110">EXAMPLES</span></span>

### <span data-ttu-id="9fc77-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="9fc77-111">Example 1</span></span>
<span data-ttu-id="9fc77-112">Szoftverfrissítési konfigurációt hoz létre a fontos frissítések két Windows Azure virtuális gépen való telepítéséhez 9 – 9 minden szombaton.</span><span class="sxs-lookup"><span data-stu-id="9fc77-112">Creates a software update configuration to install critical updates on two Windows azure virtual machines once every Saturday 9PM.</span></span> <span data-ttu-id="9fc77-113">A frissítés időtartama 2 óra értékre van állítva ebben a példában.</span><span class="sxs-lookup"><span data-stu-id="9fc77-113">Update duration is set to 2 hours in this example.</span></span>

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
                                                 -AzVMResourceId $targetMachines `
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

## <span data-ttu-id="9fc77-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9fc77-114">PARAMETERS</span></span>

### <span data-ttu-id="9fc77-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="9fc77-115">-AutomationAccountName</span></span>
<span data-ttu-id="9fc77-116">Az automatizálási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="9fc77-116">The automation account name.</span></span>

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

### <span data-ttu-id="9fc77-117">-AzureQuery</span><span class="sxs-lookup"><span data-stu-id="9fc77-117">-AzureQuery</span></span>
<span data-ttu-id="9fc77-118">Dinamikus csoport Azure-lekérdezése.</span><span class="sxs-lookup"><span data-stu-id="9fc77-118">Dynamic group azure query.</span></span>

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

### <span data-ttu-id="9fc77-119">-AzureVMResourceId</span><span class="sxs-lookup"><span data-stu-id="9fc77-119">-AzureVMResourceId</span></span>
<span data-ttu-id="9fc77-120">Az Azure Virtual Machines erőforrás-azonosítói.</span><span class="sxs-lookup"><span data-stu-id="9fc77-120">Resource Ids for azure virtual machines.</span></span>

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

### <span data-ttu-id="9fc77-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fc77-121">-DefaultProfile</span></span>
<span data-ttu-id="9fc77-122">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9fc77-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9fc77-123">-Időtartam</span><span class="sxs-lookup"><span data-stu-id="9fc77-123">-Duration</span></span>
<span data-ttu-id="9fc77-124">A frissítés maximális időtartama.</span><span class="sxs-lookup"><span data-stu-id="9fc77-124">Maximum duration for the update.</span></span>

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

### <span data-ttu-id="9fc77-125">-ExcludedKbNumber</span><span class="sxs-lookup"><span data-stu-id="9fc77-125">-ExcludedKbNumber</span></span>
<span data-ttu-id="9fc77-126">A kizárt frissítések KB-száma.</span><span class="sxs-lookup"><span data-stu-id="9fc77-126">KB numbers of excluded updates.</span></span>

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

### <span data-ttu-id="9fc77-127">-ExcludedPackageNameMask</span><span class="sxs-lookup"><span data-stu-id="9fc77-127">-ExcludedPackageNameMask</span></span>
<span data-ttu-id="9fc77-128">Kizárt Linux-csomagok maszkja.</span><span class="sxs-lookup"><span data-stu-id="9fc77-128">Excluded Linux package masks.</span></span>

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

### <span data-ttu-id="9fc77-129">-IncludedKbNumber</span><span class="sxs-lookup"><span data-stu-id="9fc77-129">-IncludedKbNumber</span></span>
<span data-ttu-id="9fc77-130">A mellékelt frissítések KB.</span><span class="sxs-lookup"><span data-stu-id="9fc77-130">KB numbers of included updates.</span></span>

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

### <span data-ttu-id="9fc77-131">-IncludedPackageClassification</span><span class="sxs-lookup"><span data-stu-id="9fc77-131">-IncludedPackageClassification</span></span>
<span data-ttu-id="9fc77-132">A Linux csomag besorolásai.</span><span class="sxs-lookup"><span data-stu-id="9fc77-132">Included Linux package classifications.</span></span>

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

### <span data-ttu-id="9fc77-133">-IncludedPackageNameMask</span><span class="sxs-lookup"><span data-stu-id="9fc77-133">-IncludedPackageNameMask</span></span>
<span data-ttu-id="9fc77-134">A Linux-csomagok maszkja is.</span><span class="sxs-lookup"><span data-stu-id="9fc77-134">Included Linux package masks.</span></span>

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

### <span data-ttu-id="9fc77-135">-IncludedUpdateClassification</span><span class="sxs-lookup"><span data-stu-id="9fc77-135">-IncludedUpdateClassification</span></span>
<span data-ttu-id="9fc77-136">Belefoglalta a Windows Update besorolását.</span><span class="sxs-lookup"><span data-stu-id="9fc77-136">Included Windows Update classifications.</span></span>

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

### <span data-ttu-id="9fc77-137">-Linux</span><span class="sxs-lookup"><span data-stu-id="9fc77-137">-Linux</span></span>
<span data-ttu-id="9fc77-138">Azt jelzi, hogy a szoftverfrissítési konfiguráció a Linux operációs rendszerek számítógépeit célozza meg.</span><span class="sxs-lookup"><span data-stu-id="9fc77-138">Indicates that the software update configuration targeting Linux operating system machines.</span></span>

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

### <span data-ttu-id="9fc77-139">-NonAzureComputer</span><span class="sxs-lookup"><span data-stu-id="9fc77-139">-NonAzureComputer</span></span>
<span data-ttu-id="9fc77-140">Nem az a számítógép neve.</span><span class="sxs-lookup"><span data-stu-id="9fc77-140">Non-Az computer names.</span></span>

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

### <span data-ttu-id="9fc77-141">-NonAzureQuery</span><span class="sxs-lookup"><span data-stu-id="9fc77-141">-NonAzureQuery</span></span>
<span data-ttu-id="9fc77-142">Dinamikus csoport nem Azure-lekérdezés.</span><span class="sxs-lookup"><span data-stu-id="9fc77-142">Dynamic group non Azure query.</span></span>

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

### <span data-ttu-id="9fc77-143">-PostTaskRunbookName</span><span class="sxs-lookup"><span data-stu-id="9fc77-143">-PostTaskRunbookName</span></span>
<span data-ttu-id="9fc77-144">Tevékenység közzététele</span><span class="sxs-lookup"><span data-stu-id="9fc77-144">Post task.</span></span>

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

### <span data-ttu-id="9fc77-145">-PostTaskRunbookParameter</span><span class="sxs-lookup"><span data-stu-id="9fc77-145">-PostTaskRunbookParameter</span></span>
<span data-ttu-id="9fc77-146">Tevékenység utáni paraméter</span><span class="sxs-lookup"><span data-stu-id="9fc77-146">Post task parameter.</span></span>

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

### <span data-ttu-id="9fc77-147">-PreTaskRunbookName</span><span class="sxs-lookup"><span data-stu-id="9fc77-147">-PreTaskRunbookName</span></span>
<span data-ttu-id="9fc77-148">Tevékenység előfeltétele</span><span class="sxs-lookup"><span data-stu-id="9fc77-148">Pre task.</span></span>

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

### <span data-ttu-id="9fc77-149">-PreTaskRunbookParameter</span><span class="sxs-lookup"><span data-stu-id="9fc77-149">-PreTaskRunbookParameter</span></span>
<span data-ttu-id="9fc77-150">A tevékenység előtti paraméter</span><span class="sxs-lookup"><span data-stu-id="9fc77-150">Pre task parameter.</span></span>

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

### <span data-ttu-id="9fc77-151">-RebootOnly</span><span class="sxs-lookup"><span data-stu-id="9fc77-151">-RebootOnly</span></span>
<span data-ttu-id="9fc77-152">Azt jelzi, hogy a szoftverfrissítési konfiguráció csak újraindítja a számítógépeket.</span><span class="sxs-lookup"><span data-stu-id="9fc77-152">Indicates that the software update configuration will Only Reboot the machines.</span></span>

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

### <span data-ttu-id="9fc77-153">-RebootSetting</span><span class="sxs-lookup"><span data-stu-id="9fc77-153">-RebootSetting</span></span>
<span data-ttu-id="9fc77-154">Újraindítás beállítás</span><span class="sxs-lookup"><span data-stu-id="9fc77-154">Reboot Setting.</span></span>

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

### <span data-ttu-id="9fc77-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9fc77-155">-ResourceGroupName</span></span>
<span data-ttu-id="9fc77-156">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="9fc77-156">The resource group name.</span></span>

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

### <span data-ttu-id="9fc77-157">– Ütemezés</span><span class="sxs-lookup"><span data-stu-id="9fc77-157">-Schedule</span></span>
<span data-ttu-id="9fc77-158">A szoftverfrissítési konfigurációhoz használt objektum ütemezése.</span><span class="sxs-lookup"><span data-stu-id="9fc77-158">Schedule object used for software update configuration.</span></span>

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

### <span data-ttu-id="9fc77-159">-Windows</span><span class="sxs-lookup"><span data-stu-id="9fc77-159">-Windows</span></span>
<span data-ttu-id="9fc77-160">Azt jelzi, hogy a szoftverfrissítési konfiguráció a Windows operációs rendszerek számítógépeit célozza meg.</span><span class="sxs-lookup"><span data-stu-id="9fc77-160">Indicates that the software update configuration targeting windows operating system machines.</span></span>

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

### <span data-ttu-id="9fc77-161">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9fc77-161">-Confirm</span></span>
<span data-ttu-id="9fc77-162">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9fc77-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9fc77-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9fc77-163">-WhatIf</span></span>
<span data-ttu-id="9fc77-164">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9fc77-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9fc77-165">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9fc77-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9fc77-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fc77-166">CommonParameters</span></span>
<span data-ttu-id="9fc77-167">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9fc77-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fc77-168">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9fc77-168">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fc77-169">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9fc77-169">INPUTS</span></span>

### <span data-ttu-id="9fc77-170">Microsoft. Azure. Command. Automation. Model. Schedule</span><span class="sxs-lookup"><span data-stu-id="9fc77-170">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

### <span data-ttu-id="9fc77-171">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="9fc77-171">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="9fc77-172">System. string []</span><span class="sxs-lookup"><span data-stu-id="9fc77-172">System.String[]</span></span>

### <span data-ttu-id="9fc77-173">System. időszak</span><span class="sxs-lookup"><span data-stu-id="9fc77-173">System.TimeSpan</span></span>

### <span data-ttu-id="9fc77-174">Microsoft. Azure. Command. Automation. Model. UpdateManagement. WindowsUpdateClasses []</span><span class="sxs-lookup"><span data-stu-id="9fc77-174">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.WindowsUpdateClasses[]</span></span>

### <span data-ttu-id="9fc77-175">Microsoft. Azure. Command. Automation. Model. UpdateManagement. LinuxPackageClasses []</span><span class="sxs-lookup"><span data-stu-id="9fc77-175">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.LinuxPackageClasses[]</span></span>

### <span data-ttu-id="9fc77-176">System. String</span><span class="sxs-lookup"><span data-stu-id="9fc77-176">System.String</span></span>

## <span data-ttu-id="9fc77-177">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9fc77-177">OUTPUTS</span></span>

### <span data-ttu-id="9fc77-178">Microsoft. Azure. Command. Automation. Model. UpdateManagement. SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="9fc77-178">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="9fc77-179">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9fc77-179">NOTES</span></span>

## <span data-ttu-id="9fc77-180">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9fc77-180">RELATED LINKS</span></span>
