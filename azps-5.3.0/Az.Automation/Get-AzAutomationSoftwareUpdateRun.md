---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationsoftwareupdaterun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSoftwareUpdateRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSoftwareUpdateRun.md
ms.openlocfilehash: d93820d12a2f61714c58341f835bef8cba832b84
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98478669"
---
# <span data-ttu-id="e6780-101">Get-AzAutomationSoftwareUpdateRun</span><span class="sxs-lookup"><span data-stu-id="e6780-101">Get-AzAutomationSoftwareUpdateRun</span></span>

## <span data-ttu-id="e6780-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e6780-102">SYNOPSIS</span></span>
<span data-ttu-id="e6780-103">Lejátsa az Azure Automation szoftverfrissítések listáját.</span><span class="sxs-lookup"><span data-stu-id="e6780-103">Gets a list of azure automation software update runs.</span></span>

## <span data-ttu-id="e6780-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e6780-104">SYNTAX</span></span>

### <span data-ttu-id="e6780-105">ByAll (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e6780-105">ByAll (Default)</span></span>
```
Get-AzAutomationSoftwareUpdateRun [-OperatingSystem <OperatingSystemType>] [-Status <SoftwareUpdateRunStatus>]
 [-StartTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e6780-106">ById</span><span class="sxs-lookup"><span data-stu-id="e6780-106">ById</span></span>
```
Get-AzAutomationSoftwareUpdateRun -Id <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e6780-107">BySucName</span><span class="sxs-lookup"><span data-stu-id="e6780-107">BySucName</span></span>
```
Get-AzAutomationSoftwareUpdateRun [-SoftwareUpdateConfigurationName <String>]
 [-OperatingSystem <OperatingSystemType>] [-Status <SoftwareUpdateRunStatus>] [-StartTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e6780-108">BySuc</span><span class="sxs-lookup"><span data-stu-id="e6780-108">BySuc</span></span>
```
Get-AzAutomationSoftwareUpdateRun [-SoftwareUpdateConfiguration <SoftwareUpdateConfiguration>]
 [-OperatingSystem <OperatingSystemType>] [-Status <SoftwareUpdateRunStatus>] [-StartTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e6780-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e6780-109">DESCRIPTION</span></span>
<span data-ttu-id="e6780-110">A Get-AzAutomationSoftwareUpdateRun parancsmag visszaadja a futtatott szoftverfrissítések listáját.</span><span class="sxs-lookup"><span data-stu-id="e6780-110">The Get-AzAutomationSoftwareUpdateRun cmdlet returns a list of software update runs.</span></span> <span data-ttu-id="e6780-111">Mivel egy szoftverfrissítési konfigurációhoz társított ütemezés tartozik, többször is elindítható.</span><span class="sxs-lookup"><span data-stu-id="e6780-111">Since a software update configuration has an associated schedule, it can be triggered multiple times.</span></span> <span data-ttu-id="e6780-112">Minden alkalommal, amikor egy ütemezés aktiválódik, frissítési futtatás jön létre.</span><span class="sxs-lookup"><span data-stu-id="e6780-112">Each time a schedule is triggered will result in an update run created.</span></span> <span data-ttu-id="e6780-113">A frissítési futtatás az összes gépi futtatás eredményének összesítése.</span><span class="sxs-lookup"><span data-stu-id="e6780-113">Update run is an aggregate of the result of all machine runs.</span></span> <span data-ttu-id="e6780-114">Futtathat adott szoftverfrissítés-konfigurációt a SoftwareUpdateConfigurationName paraméterrel.</span><span class="sxs-lookup"><span data-stu-id="e6780-114">You can get runs for specific software update configuration by passing the SoftwareUpdateConfigurationName parameter.</span></span> <span data-ttu-id="e6780-115">Egy adott futtatáshoz át kell adni a név paramétert.</span><span class="sxs-lookup"><span data-stu-id="e6780-115">To get a specific runs, you need to pass the name parameter.</span></span> <span data-ttu-id="e6780-116">A listában adott állapottal is futtathat, adott operációs rendszert célozhat meg, illetve a megfelelő paraméterrel meghatározott idő után is elindíthatja a futtatásokat.</span><span class="sxs-lookup"><span data-stu-id="e6780-116">You can also list runs with specific status, runs targeting specific operating system, or runs started after specific time by passing the appropriate parameter.</span></span>

## <span data-ttu-id="e6780-117">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e6780-117">EXAMPLES</span></span>

### <span data-ttu-id="e6780-118">1. példa</span><span class="sxs-lookup"><span data-stu-id="e6780-118">Example 1</span></span>
<span data-ttu-id="e6780-119">Ez a példa felsorolja az összes frissítést, amelyet egy adott szoftverfrissítési konfiguráció indít el.</span><span class="sxs-lookup"><span data-stu-id="e6780-119">This example list all update runs triggered by a specific software update configuration.</span></span>

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

## <span data-ttu-id="e6780-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e6780-120">PARAMETERS</span></span>

### <span data-ttu-id="e6780-121">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="e6780-121">-AutomationAccountName</span></span>
<span data-ttu-id="e6780-122">Az automatizálási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="e6780-122">The automation account name.</span></span>

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

### <span data-ttu-id="e6780-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6780-123">-DefaultProfile</span></span>
<span data-ttu-id="e6780-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e6780-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6780-125">-Id</span><span class="sxs-lookup"><span data-stu-id="e6780-125">-Id</span></span>
<span data-ttu-id="e6780-126">A szoftverfrissítéskonfiguráció azonosítója.</span><span class="sxs-lookup"><span data-stu-id="e6780-126">Id of the software update configuration run.</span></span>

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

### <span data-ttu-id="e6780-127">-OperatingSystem</span><span class="sxs-lookup"><span data-stu-id="e6780-127">-OperatingSystem</span></span>
<span data-ttu-id="e6780-128">A futtatás operációs rendszere.</span><span class="sxs-lookup"><span data-stu-id="e6780-128">The operating system of the run.</span></span>

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

### <span data-ttu-id="e6780-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6780-129">-ResourceGroupName</span></span>
<span data-ttu-id="e6780-130">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e6780-130">The resource group name.</span></span>

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

### <span data-ttu-id="e6780-131">-SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="e6780-131">-SoftwareUpdateConfiguration</span></span>
<span data-ttu-id="e6780-132">A futtatást a szoftverfrissítéskonfiguráció indította el.</span><span class="sxs-lookup"><span data-stu-id="e6780-132">The software update configuration triggered the run.</span></span>

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

### <span data-ttu-id="e6780-133">-SoftwareUpdateConfigurationName</span><span class="sxs-lookup"><span data-stu-id="e6780-133">-SoftwareUpdateConfigurationName</span></span>
<span data-ttu-id="e6780-134">A futtatást indító szoftverfrissítés-konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="e6780-134">Name of the software update configuration triggered the run.</span></span>

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

### <span data-ttu-id="e6780-135">-StartTime</span><span class="sxs-lookup"><span data-stu-id="e6780-135">-StartTime</span></span>
<span data-ttu-id="e6780-136">A futtatás minimális kezdési ideje.</span><span class="sxs-lookup"><span data-stu-id="e6780-136">Minimum start time of the run.</span></span>

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

### <span data-ttu-id="e6780-137">-Állapot</span><span class="sxs-lookup"><span data-stu-id="e6780-137">-Status</span></span>
<span data-ttu-id="e6780-138">A futtatás állapota.</span><span class="sxs-lookup"><span data-stu-id="e6780-138">Status of the run.</span></span>

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

### <span data-ttu-id="e6780-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6780-139">CommonParameters</span></span>
<span data-ttu-id="e6780-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6780-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6780-141">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6780-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6780-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e6780-142">INPUTS</span></span>

### <span data-ttu-id="e6780-143">System.Guid</span><span class="sxs-lookup"><span data-stu-id="e6780-143">System.Guid</span></span>

### <span data-ttu-id="e6780-144">System.String</span><span class="sxs-lookup"><span data-stu-id="e6780-144">System.String</span></span>

### <span data-ttu-id="e6780-145">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="e6780-145">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span></span>

### <span data-ttu-id="e6780-146">System.Nullable'1[[Microsoft.Azure.Commands.Automation.Model.UpdateManagement.OperatingSystemType, Microsoft.Azure.PowerShell.Cmdlets.Automation, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="e6780-146">System.Nullable\`1[[Microsoft.Azure.Commands.Automation.Model.UpdateManagement.OperatingSystemType, Microsoft.Azure.PowerShell.Cmdlets.Automation, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="e6780-147">System.Nullable'1[[Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateRunStatus, Microsoft.Azure.PowerShell.Cmdlets.Automation, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="e6780-147">System.Nullable\`1[[Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateRunStatus, Microsoft.Azure.PowerShell.Cmdlets.Automation, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="e6780-148">System.DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="e6780-148">System.DateTimeOffset</span></span>

## <span data-ttu-id="e6780-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e6780-149">OUTPUTS</span></span>

### <span data-ttu-id="e6780-150">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateRun</span><span class="sxs-lookup"><span data-stu-id="e6780-150">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateRun</span></span>

## <span data-ttu-id="e6780-151">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e6780-151">NOTES</span></span>

## <span data-ttu-id="e6780-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e6780-152">RELATED LINKS</span></span>
