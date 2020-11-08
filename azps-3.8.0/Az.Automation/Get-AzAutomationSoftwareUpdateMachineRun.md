---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationsoftwareupdatemachinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSoftwareUpdateMachineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSoftwareUpdateMachineRun.md
ms.openlocfilehash: 19c0321b1c915519b7c3617b52810da18e534521
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94015068"
---
# <span data-ttu-id="ef8a8-101">Get-AzAutomationSoftwareUpdateMachineRun</span><span class="sxs-lookup"><span data-stu-id="ef8a8-101">Get-AzAutomationSoftwareUpdateMachineRun</span></span>

## <span data-ttu-id="ef8a8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ef8a8-102">SYNOPSIS</span></span>
<span data-ttu-id="ef8a8-103">Lefuttatja az Azure automatizálási szoftverfrissítési konfigurációjának listáját.</span><span class="sxs-lookup"><span data-stu-id="ef8a8-103">Gets a list of azure automation software update configuration machine runs.</span></span>

## <span data-ttu-id="ef8a8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ef8a8-104">SYNTAX</span></span>

### <span data-ttu-id="ef8a8-105">ByAll (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ef8a8-105">ByAll (Default)</span></span>
```
Get-AzAutomationSoftwareUpdateMachineRun [-Status <SoftwareUpdateMachineRunStatus>] [-TargetComputer <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ef8a8-106">ById</span><span class="sxs-lookup"><span data-stu-id="ef8a8-106">ById</span></span>
```
Get-AzAutomationSoftwareUpdateMachineRun -Id <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ef8a8-107">BySucrId</span><span class="sxs-lookup"><span data-stu-id="ef8a8-107">BySucrId</span></span>
```
Get-AzAutomationSoftwareUpdateMachineRun [-SoftwareUpdateRunId <Guid>]
 [-Status <SoftwareUpdateMachineRunStatus>] [-TargetComputer <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ef8a8-108">BySucr</span><span class="sxs-lookup"><span data-stu-id="ef8a8-108">BySucr</span></span>
```
Get-AzAutomationSoftwareUpdateMachineRun [-SoftwareUpdateRun <SoftwareUpdateRun>]
 [-Status <SoftwareUpdateMachineRunStatus>] [-TargetComputer <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ef8a8-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="ef8a8-109">DESCRIPTION</span></span>
<span data-ttu-id="ef8a8-110">Ez a parancsmag a számítógép futási listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="ef8a8-110">This cmdlet returns a list of machine runs.</span></span> <span data-ttu-id="ef8a8-111">Minden szoftverfrissítési Futtatás elindítja a számítógép futását a szoftverfrissítési beállítások mindegyikéhez.</span><span class="sxs-lookup"><span data-stu-id="ef8a8-111">Each software update run will trigger a machine run for each of the software update configuration target machine.</span></span> <span data-ttu-id="ef8a8-112">Ha egy adott gépet szeretne futtatni, adja át az azonosító paramétert.</span><span class="sxs-lookup"><span data-stu-id="ef8a8-112">To get a specific machine run, pass the Id parameter.</span></span> <span data-ttu-id="ef8a8-113">Felsorolhatja az összes gépet, az összes futót egy adott számítógépen, a megfelelő paraméterek elküldésével minden futó meghatározott állapotú.</span><span class="sxs-lookup"><span data-stu-id="ef8a8-113">You can list all the machine runs, all runs for a specific computer, all runs with specific status by passing the corresponding parameters.</span></span>

## <span data-ttu-id="ef8a8-114">Példák</span><span class="sxs-lookup"><span data-stu-id="ef8a8-114">EXAMPLES</span></span>

### <span data-ttu-id="ef8a8-115">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ef8a8-115">Example 1</span></span>
<span data-ttu-id="ef8a8-116">Az alábbi példa visszaadja a megadott Azure Virtual Machine minden sikertelen futását.</span><span class="sxs-lookup"><span data-stu-id="ef8a8-116">This example returns all failed machine runs for the specified azure virtual machine.</span></span>


```powershell
PS C:\> $targetComputer = "/subscriptions/22e2445a-0984-4fa5-86a4-0280d76c4b2c/resourceGroups/compute/providers/Microsoft.Compute/virtualMachines/myvm"
PS C:\> Get-AzAutomationSoftwareUpdateMachineRun -ResourceGroupName "mygroup" `
                                                      -AutomationAccountName "myaccount" `
                                                      -TargetComputer $targetComputer `
                                                      -Status Failed

MachineRunId          : 0033d6d6-828d-4712-adab-293cc4fc8809
TargetComputer        : /subscriptions/22e2445a-0984-4fa5-86a4-0280d76c4b2c/resourceGroups/compute/providers/Microsoft.Compute/virtualMachines/myvm
TargetComputerType    : AzureVirtualMachines
SoftwareUpdateRunId   : 46568d26-0182-49b2-8bfd-af3455780397
OperatingSystem       : Windows
Status                : Failed
ResourceGroupName     : mygroup
AutomationAccountName : myaccount
Name                  : 0033d6d6-828d-4712-adab-293cc4fc8809
CreationTime          : 5/17/2018 2:06:44 AM +00:00
LastModifiedTime      : 5/17/2018 2:08:49 AM +00:00
```

## <span data-ttu-id="ef8a8-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ef8a8-117">PARAMETERS</span></span>

### <span data-ttu-id="ef8a8-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ef8a8-118">-AutomationAccountName</span></span>
<span data-ttu-id="ef8a8-119">Az automatizálási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="ef8a8-119">The automation account name.</span></span>

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

### <span data-ttu-id="ef8a8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef8a8-120">-DefaultProfile</span></span>
<span data-ttu-id="ef8a8-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ef8a8-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ef8a8-122">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="ef8a8-122">-Id</span></span>
<span data-ttu-id="ef8a8-123">Futtatja a szoftverfrissítési számítógép azonosítóját.</span><span class="sxs-lookup"><span data-stu-id="ef8a8-123">Id of the software update machine run.</span></span>

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

### <span data-ttu-id="ef8a8-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef8a8-124">-ResourceGroupName</span></span>
<span data-ttu-id="ef8a8-125">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="ef8a8-125">The resource group name.</span></span>

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

### <span data-ttu-id="ef8a8-126">-SoftwareUpdateRun</span><span class="sxs-lookup"><span data-stu-id="ef8a8-126">-SoftwareUpdateRun</span></span>
<span data-ttu-id="ef8a8-127">A szoftverfrissítés fut.</span><span class="sxs-lookup"><span data-stu-id="ef8a8-127">The software update run.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateRun
Parameter Sets: BySucr
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef8a8-128">-SoftwareUpdateRunId</span><span class="sxs-lookup"><span data-stu-id="ef8a8-128">-SoftwareUpdateRunId</span></span>
<span data-ttu-id="ef8a8-129">A szoftverfrissítési szolgáltatás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="ef8a8-129">Id of the software update run.</span></span>

```yaml
Type: System.Guid
Parameter Sets: BySucrId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef8a8-130">-Állapot</span><span class="sxs-lookup"><span data-stu-id="ef8a8-130">-Status</span></span>
<span data-ttu-id="ef8a8-131">A gép állapota</span><span class="sxs-lookup"><span data-stu-id="ef8a8-131">Status of the machine run.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateMachineRunStatus]
Parameter Sets: ByAll, BySucrId, BySucr
Aliases:
Accepted values: NotStarted, InProgress, Succeeded, Failed, MaintenanceWindowExceeded, FailedToStart

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef8a8-132">-TargetComputer</span><span class="sxs-lookup"><span data-stu-id="ef8a8-132">-TargetComputer</span></span>
<span data-ttu-id="ef8a8-133">a számítógépen futó célszámítógép.</span><span class="sxs-lookup"><span data-stu-id="ef8a8-133">target computer for the machine run.</span></span>
<span data-ttu-id="ef8a8-134">Lehet nem az a számítógép neve vagy Azure VM erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="ef8a8-134">Can be either a non-az computer name or an azure VM resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAll, BySucrId, BySucr
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef8a8-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef8a8-135">CommonParameters</span></span>
<span data-ttu-id="ef8a8-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ef8a8-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef8a8-137">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef8a8-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef8a8-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ef8a8-138">INPUTS</span></span>

### <span data-ttu-id="ef8a8-139">System. GUID</span><span class="sxs-lookup"><span data-stu-id="ef8a8-139">System.Guid</span></span>

### <span data-ttu-id="ef8a8-140">Microsoft. Azure. Command. Automation. Model. UpdateManagement. SoftwareUpdateRun</span><span class="sxs-lookup"><span data-stu-id="ef8a8-140">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateRun</span></span>

### <span data-ttu-id="ef8a8-141">System. nulla ' 1 [[Microsoft. Azure. commands. Automation. Model. UpdateManagement. SoftwareUpdateMachineRunStatus, Microsoft. Azure. PowerShell. parancsmagok. Automation, Version = 1.0.0.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="ef8a8-141">System.Nullable\`1[[Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateMachineRunStatus, Microsoft.Azure.PowerShell.Cmdlets.Automation, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="ef8a8-142">System. String</span><span class="sxs-lookup"><span data-stu-id="ef8a8-142">System.String</span></span>

## <span data-ttu-id="ef8a8-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ef8a8-143">OUTPUTS</span></span>

### <span data-ttu-id="ef8a8-144">Microsoft. Azure. Command. Automation. Model. UpdateManagement. SoftwareUpdateMachineRun</span><span class="sxs-lookup"><span data-stu-id="ef8a8-144">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateMachineRun</span></span>

## <span data-ttu-id="ef8a8-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ef8a8-145">NOTES</span></span>

## <span data-ttu-id="ef8a8-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ef8a8-146">RELATED LINKS</span></span>
