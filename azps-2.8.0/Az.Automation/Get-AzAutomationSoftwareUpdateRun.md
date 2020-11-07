---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationsoftwareupdaterun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSoftwareUpdateRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSoftwareUpdateRun.md
ms.openlocfilehash: c866a1e4a703938e5ef860af3760b4bbb082fc3d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667823"
---
# <span data-ttu-id="85b9b-101">Get-AzAutomationSoftwareUpdateRun</span><span class="sxs-lookup"><span data-stu-id="85b9b-101">Get-AzAutomationSoftwareUpdateRun</span></span>

## <span data-ttu-id="85b9b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="85b9b-102">SYNOPSIS</span></span>
<span data-ttu-id="85b9b-103">Lefuttatja az Azure automatizálási szoftverfrissítés listáját.</span><span class="sxs-lookup"><span data-stu-id="85b9b-103">Gets a list of azure automation software update runs.</span></span>

## <span data-ttu-id="85b9b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="85b9b-104">SYNTAX</span></span>

### <span data-ttu-id="85b9b-105">ByAll (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="85b9b-105">ByAll (Default)</span></span>
```
Get-AzAutomationSoftwareUpdateRun [-OperatingSystem <OperatingSystemType>] [-Status <SoftwareUpdateRunStatus>]
 [-StartTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="85b9b-106">ById</span><span class="sxs-lookup"><span data-stu-id="85b9b-106">ById</span></span>
```
Get-AzAutomationSoftwareUpdateRun -Id <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="85b9b-107">BySucName</span><span class="sxs-lookup"><span data-stu-id="85b9b-107">BySucName</span></span>
```
Get-AzAutomationSoftwareUpdateRun [-SoftwareUpdateConfigurationName <String>]
 [-OperatingSystem <OperatingSystemType>] [-Status <SoftwareUpdateRunStatus>] [-StartTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="85b9b-108">BySuc</span><span class="sxs-lookup"><span data-stu-id="85b9b-108">BySuc</span></span>
```
Get-AzAutomationSoftwareUpdateRun [-SoftwareUpdateConfiguration <SoftwareUpdateConfiguration>]
 [-OperatingSystem <OperatingSystemType>] [-Status <SoftwareUpdateRunStatus>] [-StartTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="85b9b-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="85b9b-109">DESCRIPTION</span></span>
<span data-ttu-id="85b9b-110">A Get-AzAutomationSoftwareUpdateRun parancsmag a szoftverfrissítési frissítések listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="85b9b-110">The Get-AzAutomationSoftwareUpdateRun cmdlet returns a list of software update runs.</span></span> <span data-ttu-id="85b9b-111">Mivel a szoftverfrissítési konfigurációhoz társítva van egy ütemezés, több alkalommal is elindítható.</span><span class="sxs-lookup"><span data-stu-id="85b9b-111">Since a software update configuration has an associated schedule, it can be triggered multiple times.</span></span> <span data-ttu-id="85b9b-112">Minden alkalommal, amikor egy ütemtervet kezdeményez, a program a frissítés futását eredményezi.</span><span class="sxs-lookup"><span data-stu-id="85b9b-112">Each time a schedule is triggered will result in an update run created.</span></span> <span data-ttu-id="85b9b-113">A frissítés futtatása a számítógép minden futási eredményének összessége.</span><span class="sxs-lookup"><span data-stu-id="85b9b-113">Update run is an aggregate of the result of all machine runs.</span></span> <span data-ttu-id="85b9b-114">Az SoftwareUpdateConfigurationName paraméter átadásával az adott szoftverfrissítés-konfigurációban futtatható.</span><span class="sxs-lookup"><span data-stu-id="85b9b-114">You can get runs for specific software update configuration by passing the SoftwareUpdateConfigurationName parameter.</span></span> <span data-ttu-id="85b9b-115">Ha meghatározott futási időpontot szeretne kapni, át kell adni a name paramétert.</span><span class="sxs-lookup"><span data-stu-id="85b9b-115">To get a specific runs, you need to pass the name parameter.</span></span> <span data-ttu-id="85b9b-116">Azt is megteheti, hogy a lista adott állapotú, az adott operációs rendszert célozza, vagy ha adott idő után futtatja az indítást, a megfelelő paramétert átadva.</span><span class="sxs-lookup"><span data-stu-id="85b9b-116">You can also list runs with specific status, runs targeting specific operating system, or runs started after specific time by passing the appropriate parameter.</span></span>

## <span data-ttu-id="85b9b-117">Példák</span><span class="sxs-lookup"><span data-stu-id="85b9b-117">EXAMPLES</span></span>

### <span data-ttu-id="85b9b-118">Példa 1</span><span class="sxs-lookup"><span data-stu-id="85b9b-118">Example 1</span></span>
<span data-ttu-id="85b9b-119">Ez a példa felsorolja az összes frissítést, amelyet egy bizonyos szoftverfrissítés-konfiguráció indít elő.</span><span class="sxs-lookup"><span data-stu-id="85b9b-119">This example list all update runs triggered by a specific software update configuration.</span></span>

```powershell
PS C:\> Get-AzAutomationSoftwareUpdateRun -ResourceGroupName "mygroup" `
                                               -AutomationAccountName "myaccount" `
                                               -SoftwareUpdateConfigurationName "MyUpdateConfiguration"

RunId                           : ec9ce57f-da18-44be-b33b-651a0f93cb52
SoftwareUpdateConfigurationName : MyUpdateConfiguration
ConfiguredDuration              : 02:00:00
OperatingSystem                 : Windows
StartTime                       : 5/22/2018 11:37:42 PM +00:00
EndTime                         : 5/22/2018 11:38:31 PM +00:00
ComputerCount                   : 2
FailedCount                     : 0
ResourceGroupName               : mygroup
AutomationAccountName           : myaccount
Name                            : ec9ce57f-da18-44be-b33b-651a0f93cb52
CreationTime                    : 5/22/2018 11:37:42 PM +00:00
LastModifiedTime                : 5/22/2018 11:38:54 PM +00:00
Description                     :

RunId                           : ac9396c7-a837-43d4-be97-fbfe46c80baa
SoftwareUpdateConfigurationName : MyUpdateConfiguration
ConfiguredDuration              : 02:00:00
OperatingSystem                 : Windows
StartTime                       : 5/22/2018 10:00:47 PM +00:00
EndTime                         : 5/22/2018 10:02:20 PM +00:00
ComputerCount                   : 2
FailedCount                     : 0
ResourceGroupName               : mygroup
AutomationAccountName           : myaccount
Name                            : ac9396c7-a837-43d4-be97-fbfe46c80baa
CreationTime                    : 5/22/2018 10:00:47 PM +00:00
LastModifiedTime                : 5/22/2018 10:02:58 PM +00:00
```

## <span data-ttu-id="85b9b-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="85b9b-120">PARAMETERS</span></span>

### <span data-ttu-id="85b9b-121">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="85b9b-121">-AutomationAccountName</span></span>
<span data-ttu-id="85b9b-122">Az automatizálási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="85b9b-122">The automation account name.</span></span>

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

### <span data-ttu-id="85b9b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85b9b-123">-DefaultProfile</span></span>
<span data-ttu-id="85b9b-124">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="85b9b-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="85b9b-125">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="85b9b-125">-Id</span></span>
<span data-ttu-id="85b9b-126">A szoftverfrissítési konfiguráció azonosítója.</span><span class="sxs-lookup"><span data-stu-id="85b9b-126">Id of the software update configuration run.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85b9b-127">-OperatingSystem tulajdonság</span><span class="sxs-lookup"><span data-stu-id="85b9b-127">-OperatingSystem</span></span>
<span data-ttu-id="85b9b-128">A Futtatás operációs rendszere.</span><span class="sxs-lookup"><span data-stu-id="85b9b-128">The operating system of the run.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Automation.Model.UpdateManagement.OperatingSystemType]
Parameter Sets: ByAll, BySucName, BySuc
Aliases:
Accepted values: Windows, Linux

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85b9b-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85b9b-129">-ResourceGroupName</span></span>
<span data-ttu-id="85b9b-130">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="85b9b-130">The resource group name.</span></span>

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

### <span data-ttu-id="85b9b-131">-SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="85b9b-131">-SoftwareUpdateConfiguration</span></span>
<span data-ttu-id="85b9b-132">A szoftverfrissítés-konfiguráció kezdeményezte a futtatást.</span><span class="sxs-lookup"><span data-stu-id="85b9b-132">The software update configuration triggered the run.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration
Parameter Sets: BySuc
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85b9b-133">-SoftwareUpdateConfigurationName</span><span class="sxs-lookup"><span data-stu-id="85b9b-133">-SoftwareUpdateConfigurationName</span></span>
<span data-ttu-id="85b9b-134">A szoftverfrissítés-konfiguráció neve a futtatást kezdeményezte.</span><span class="sxs-lookup"><span data-stu-id="85b9b-134">Name of the software update configuration triggered the run.</span></span>

```yaml
Type: System.String
Parameter Sets: BySucName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85b9b-135">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="85b9b-135">-StartTime</span></span>
<span data-ttu-id="85b9b-136">A Futtatás minimális kezdési ideje.</span><span class="sxs-lookup"><span data-stu-id="85b9b-136">Minimum start time of the run.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: ByAll, BySucName, BySuc
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85b9b-137">-Állapot</span><span class="sxs-lookup"><span data-stu-id="85b9b-137">-Status</span></span>
<span data-ttu-id="85b9b-138">A Futtatás állapota</span><span class="sxs-lookup"><span data-stu-id="85b9b-138">Status of the run.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateRunStatus]
Parameter Sets: ByAll, BySucName, BySuc
Aliases:
Accepted values: NotStarted, InProgress, Succeeded, Failed, MaintenanceWindowExceeded

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85b9b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85b9b-139">CommonParameters</span></span>
<span data-ttu-id="85b9b-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="85b9b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85b9b-141">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85b9b-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85b9b-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="85b9b-142">INPUTS</span></span>

### <span data-ttu-id="85b9b-143">System. GUID</span><span class="sxs-lookup"><span data-stu-id="85b9b-143">System.Guid</span></span>

### <span data-ttu-id="85b9b-144">System. String</span><span class="sxs-lookup"><span data-stu-id="85b9b-144">System.String</span></span>

### <span data-ttu-id="85b9b-145">Microsoft. Azure. Command. Automation. Model. UpdateManagement. SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="85b9b-145">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span></span>

### <span data-ttu-id="85b9b-146">System. nulla ' 1 [[Microsoft. Azure. commands. Automation. Model. UpdateManagement. OperatingSystemType, Microsoft. Azure. PowerShell. parancsmagok. Automation, Version = 1.0.0.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="85b9b-146">System.Nullable\`1[[Microsoft.Azure.Commands.Automation.Model.UpdateManagement.OperatingSystemType, Microsoft.Azure.PowerShell.Cmdlets.Automation, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="85b9b-147">System. nulla ' 1 [[Microsoft. Azure. commands. Automation. Model. UpdateManagement. SoftwareUpdateRunStatus, Microsoft. Azure. PowerShell. parancsmagok. Automation, Version = 1.0.0.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="85b9b-147">System.Nullable\`1[[Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateRunStatus, Microsoft.Azure.PowerShell.Cmdlets.Automation, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="85b9b-148">System. DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="85b9b-148">System.DateTimeOffset</span></span>

## <span data-ttu-id="85b9b-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="85b9b-149">OUTPUTS</span></span>

### <span data-ttu-id="85b9b-150">Microsoft. Azure. Command. Automation. Model. UpdateManagement. SoftwareUpdateRun</span><span class="sxs-lookup"><span data-stu-id="85b9b-150">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateRun</span></span>

## <span data-ttu-id="85b9b-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="85b9b-151">NOTES</span></span>

## <span data-ttu-id="85b9b-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="85b9b-152">RELATED LINKS</span></span>
