---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/new-azurermautomationsoftwareupdateconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationSoftwareUpdateConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationSoftwareUpdateConfiguration.md
ms.openlocfilehash: f66d22e8ca07812ab76c482c29018f2a639d84f1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498499"
---
# <span data-ttu-id="86593-101">New-AzureRmAutomationSoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="86593-101">New-AzureRmAutomationSoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="86593-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="86593-102">SYNOPSIS</span></span>
<span data-ttu-id="86593-103">Ütemezett Azure automatizálási szoftverfrissítési konfigurációt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="86593-103">Creates a scheduled azure automation software update configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="86593-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="86593-104">SYNTAX</span></span>

### <span data-ttu-id="86593-105">Windows (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="86593-105">Windows (Default)</span></span>
```
New-AzureRmAutomationSoftwareUpdateConfiguration -Schedule <Schedule> [-Windows]
 [-AzureVMResourceId <String[]>] [-NonAzureComputer <String[]>] [-Duration <TimeSpan>]
 [-IncludedUpdateClassification <WindowsUpdateClasses[]>] [-ExcludedKbNumber <String[]>]
 [-IncludedKbNumber <String[]>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86593-106">Linux</span><span class="sxs-lookup"><span data-stu-id="86593-106">Linux</span></span>
```
New-AzureRmAutomationSoftwareUpdateConfiguration -Schedule <Schedule> [-Linux] [-AzureVMResourceId <String[]>]
 [-NonAzureComputer <String[]>] [-Duration <TimeSpan>] [-IncludedPackageClassification <LinuxPackageClasses[]>]
 [-ExcludedPackageNameMask <String[]>] [-IncludedPackageNameMask <String[]>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="86593-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="86593-107">DESCRIPTION</span></span>
<span data-ttu-id="86593-108">Egy, az ütemterven futó szoftverfrissítési konfigurációt hoz létre a számítógépek listájának frissítéséhez.</span><span class="sxs-lookup"><span data-stu-id="86593-108">Creates a software update configuration that runs on a schedule to update a list of computers.</span></span> <span data-ttu-id="86593-109">A számítógépeken Azure virtuális gépek és nem Azure rendszerű számítógépek is szerepelnek.</span><span class="sxs-lookup"><span data-stu-id="86593-109">Computers include both azure virtual machines or non-azure computers.</span></span>

## <span data-ttu-id="86593-110">Példák</span><span class="sxs-lookup"><span data-stu-id="86593-110">EXAMPLES</span></span>

### <span data-ttu-id="86593-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="86593-111">Example 1</span></span>
<span data-ttu-id="86593-112">Szoftverfrissítési konfigurációt hoz létre a fontos frissítések két Windows Azure virtuális gépen való telepítéséhez 9 – 9 minden szombaton.</span><span class="sxs-lookup"><span data-stu-id="86593-112">Creates a software update configuration to install critical updates on two Windows azure virtual machines once every Saturday 9PM.</span></span> <span data-ttu-id="86593-113">A frissítés időtartama 2 óra értékre van állítva ebben a példában.</span><span class="sxs-lookup"><span data-stu-id="86593-113">Update duration is set to 2 hours in this example.</span></span>

```powershell
PS C:\> $startTime = [DateTimeOffset]"2018-09-13T21:00"
PS C:\> $targetMachines = @( `
    "/subscriptions/22e2445a-0984-4fa5-86a4-0280d76c4b2c/resourceGroups/compute/providers/Microsoft.Compute/virtualMachines/vm-w-01", `
    "/subscriptions/22e2445a-0984-4fa5-86a4-0280d76c4b2c/resourceGroups/compute/providers/Microsoft.Compute/virtualMachines/vm-w-02"
    )
PS C:\> $duration = New-TimeSpan -Hours 2
PS C:\> $schedule = New-AzureRmAutomationSchedule -ResourceGroupName "mygroup" `
                                                  -AutomationAccountName "myaccount" `
                                                  -Name MyWeeklySchedule `
                                                  -StartTime $startTime `
                                                  -DaysOfWeek Saturday `
                                                  -WeekInterval 1 `
                                                  -ForUpdateConfiguration

New-AzureRmAutomationSoftwareUpdateConfiguration -ResourceGroupName "mygroup" `
                                                 -AutomationAccountName "myaccount" `
                                                 -Schedule $schedule `
                                                 -Windows `
                                                 -AzureVMResourceIds $targetMachines `
                                                 -IncludedUpdateClassifications Critical `
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

## <span data-ttu-id="86593-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="86593-114">PARAMETERS</span></span>

### <span data-ttu-id="86593-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="86593-115">-AutomationAccountName</span></span>
<span data-ttu-id="86593-116">Az automatizálási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="86593-116">The automation account name.</span></span>

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

### <span data-ttu-id="86593-117">-AzureVMResourceId</span><span class="sxs-lookup"><span data-stu-id="86593-117">-AzureVMResourceId</span></span>
<span data-ttu-id="86593-118">Az Azure Virtual Machines erőforrás-azonosítói.</span><span class="sxs-lookup"><span data-stu-id="86593-118">Resource Ids for azure virtual machines.</span></span>

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

### <span data-ttu-id="86593-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86593-119">-DefaultProfile</span></span>
<span data-ttu-id="86593-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="86593-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="86593-121">-Időtartam</span><span class="sxs-lookup"><span data-stu-id="86593-121">-Duration</span></span>
<span data-ttu-id="86593-122">A frissítés maximális időtartama.</span><span class="sxs-lookup"><span data-stu-id="86593-122">Maximum duration for the update.</span></span>

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

### <span data-ttu-id="86593-123">-ExcludedKbNumber</span><span class="sxs-lookup"><span data-stu-id="86593-123">-ExcludedKbNumber</span></span>
<span data-ttu-id="86593-124">A kizárt frissítések KB-száma.</span><span class="sxs-lookup"><span data-stu-id="86593-124">KB numbers of excluded updates.</span></span>

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

### <span data-ttu-id="86593-125">-ExcludedPackageNameMask</span><span class="sxs-lookup"><span data-stu-id="86593-125">-ExcludedPackageNameMask</span></span>
<span data-ttu-id="86593-126">Kizárt Linux-csomagok maszkja.</span><span class="sxs-lookup"><span data-stu-id="86593-126">Excluded Linux package masks.</span></span>

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

### <span data-ttu-id="86593-127">-IncludedKbNumber</span><span class="sxs-lookup"><span data-stu-id="86593-127">-IncludedKbNumber</span></span>
<span data-ttu-id="86593-128">A mellékelt frissítések KB.</span><span class="sxs-lookup"><span data-stu-id="86593-128">KB numbers of included updates.</span></span>

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

### <span data-ttu-id="86593-129">-IncludedPackageClassification</span><span class="sxs-lookup"><span data-stu-id="86593-129">-IncludedPackageClassification</span></span>
<span data-ttu-id="86593-130">A Linux csomag besorolásai.</span><span class="sxs-lookup"><span data-stu-id="86593-130">Included Linux package classifications.</span></span>

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

### <span data-ttu-id="86593-131">-IncludedPackageNameMask</span><span class="sxs-lookup"><span data-stu-id="86593-131">-IncludedPackageNameMask</span></span>
<span data-ttu-id="86593-132">A Linux-csomagok maszkja is.</span><span class="sxs-lookup"><span data-stu-id="86593-132">Included Linux package masks.</span></span>

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

### <span data-ttu-id="86593-133">-IncludedUpdateClassification</span><span class="sxs-lookup"><span data-stu-id="86593-133">-IncludedUpdateClassification</span></span>
<span data-ttu-id="86593-134">Belefoglalta a Windows Update besorolását.</span><span class="sxs-lookup"><span data-stu-id="86593-134">Included Windows Update classifications.</span></span>

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

### <span data-ttu-id="86593-135">-Linux</span><span class="sxs-lookup"><span data-stu-id="86593-135">-Linux</span></span>
<span data-ttu-id="86593-136">Azt jelzi, hogy a szoftverfrissítési konfiguráció a Linux operációs rendszerek számítógépeit célozza meg.</span><span class="sxs-lookup"><span data-stu-id="86593-136">Indicates that the software update configuration targeting Linux operating system machines.</span></span>

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

### <span data-ttu-id="86593-137">-NonAzureComputer</span><span class="sxs-lookup"><span data-stu-id="86593-137">-NonAzureComputer</span></span>
<span data-ttu-id="86593-138">Nem Azure rendszerű számítógépek nevei</span><span class="sxs-lookup"><span data-stu-id="86593-138">Non-Azure computer names.</span></span>

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

### <span data-ttu-id="86593-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86593-139">-ResourceGroupName</span></span>
<span data-ttu-id="86593-140">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="86593-140">The resource group name.</span></span>

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

### <span data-ttu-id="86593-141">– Ütemezés</span><span class="sxs-lookup"><span data-stu-id="86593-141">-Schedule</span></span>
<span data-ttu-id="86593-142">A szoftverfrissítési konfigurációhoz használt objektum ütemezése.</span><span class="sxs-lookup"><span data-stu-id="86593-142">Schedule object used for software update configuration.</span></span>

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

### <span data-ttu-id="86593-143">-Windows</span><span class="sxs-lookup"><span data-stu-id="86593-143">-Windows</span></span>
<span data-ttu-id="86593-144">Azt jelzi, hogy a szoftverfrissítési konfiguráció a Windows operációs rendszerek számítógépeit célozza meg.</span><span class="sxs-lookup"><span data-stu-id="86593-144">Indicates that the software update configuration targeting windows operating system machines.</span></span>

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

### <span data-ttu-id="86593-145">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="86593-145">-Confirm</span></span>
<span data-ttu-id="86593-146">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="86593-146">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86593-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86593-147">-WhatIf</span></span>
<span data-ttu-id="86593-148">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="86593-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="86593-149">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="86593-149">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86593-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86593-150">CommonParameters</span></span>
<span data-ttu-id="86593-151">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="86593-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86593-152">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86593-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86593-153">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="86593-153">INPUTS</span></span>

### <span data-ttu-id="86593-154">Microsoft. Azure. Command. Automation. Model. Schedule</span><span class="sxs-lookup"><span data-stu-id="86593-154">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

### <span data-ttu-id="86593-155">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="86593-155">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="86593-156">System. string []</span><span class="sxs-lookup"><span data-stu-id="86593-156">System.String[]</span></span>

### <span data-ttu-id="86593-157">System. időszak</span><span class="sxs-lookup"><span data-stu-id="86593-157">System.TimeSpan</span></span>

### <span data-ttu-id="86593-158">Microsoft. Azure. Command. Automation. Model. UpdateManagement. WindowsUpdateClasses []</span><span class="sxs-lookup"><span data-stu-id="86593-158">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.WindowsUpdateClasses[]</span></span>

### <span data-ttu-id="86593-159">Microsoft. Azure. Command. Automation. Model. UpdateManagement. LinuxPackageClasses []</span><span class="sxs-lookup"><span data-stu-id="86593-159">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.LinuxPackageClasses[]</span></span>

### <span data-ttu-id="86593-160">System. String</span><span class="sxs-lookup"><span data-stu-id="86593-160">System.String</span></span>

## <span data-ttu-id="86593-161">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="86593-161">OUTPUTS</span></span>

### <span data-ttu-id="86593-162">Microsoft. Azure. Command. Automation. Model. UpdateManagement. SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="86593-162">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="86593-163">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="86593-163">NOTES</span></span>

## <span data-ttu-id="86593-164">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="86593-164">RELATED LINKS</span></span>
