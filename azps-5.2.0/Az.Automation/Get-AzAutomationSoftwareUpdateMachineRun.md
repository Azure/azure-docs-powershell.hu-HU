---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationsoftwareupdatemachinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSoftwareUpdateMachineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSoftwareUpdateMachineRun.md
ms.openlocfilehash: 19c0321b1c915519b7c3617b52810da18e534521
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98373714"
---
# <span data-ttu-id="c0ba6-101">Get-AzAutomationSoftwareUpdateMachineRun</span><span class="sxs-lookup"><span data-stu-id="c0ba6-101">Get-AzAutomationSoftwareUpdateMachineRun</span></span>

## <span data-ttu-id="c0ba6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0ba6-102">SYNOPSIS</span></span>
<span data-ttu-id="c0ba6-103">Lejátsa az Azure Automation szoftverfrissítés-konfigurációs számítógépének listáját.</span><span class="sxs-lookup"><span data-stu-id="c0ba6-103">Gets a list of azure automation software update configuration machine runs.</span></span>

## <span data-ttu-id="c0ba6-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c0ba6-104">SYNTAX</span></span>

### <span data-ttu-id="c0ba6-105">ByAll (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c0ba6-105">ByAll (Default)</span></span>
```
Get-AzAutomationSoftwareUpdateMachineRun [-Status <SoftwareUpdateMachineRunStatus>] [-TargetComputer <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c0ba6-106">ById</span><span class="sxs-lookup"><span data-stu-id="c0ba6-106">ById</span></span>
```
Get-AzAutomationSoftwareUpdateMachineRun -Id <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c0ba6-107">BySucrId</span><span class="sxs-lookup"><span data-stu-id="c0ba6-107">BySucrId</span></span>
```
Get-AzAutomationSoftwareUpdateMachineRun [-SoftwareUpdateRunId <Guid>]
 [-Status <SoftwareUpdateMachineRunStatus>] [-TargetComputer <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c0ba6-108">BySucr</span><span class="sxs-lookup"><span data-stu-id="c0ba6-108">BySucr</span></span>
```
Get-AzAutomationSoftwareUpdateMachineRun [-SoftwareUpdateRun <SoftwareUpdateRun>]
 [-Status <SoftwareUpdateMachineRunStatus>] [-TargetComputer <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c0ba6-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c0ba6-109">DESCRIPTION</span></span>
<span data-ttu-id="c0ba6-110">Ez a parancsmag a gép által futtatott gépek listáját adja vissza.</span><span class="sxs-lookup"><span data-stu-id="c0ba6-110">This cmdlet returns a list of machine runs.</span></span> <span data-ttu-id="c0ba6-111">Minden szoftverfrissítés futtatása elindít egy gép futtatását minden egyes szoftverfrissítéskonfigurációs célgéphez.</span><span class="sxs-lookup"><span data-stu-id="c0ba6-111">Each software update run will trigger a machine run for each of the software update configuration target machine.</span></span> <span data-ttu-id="c0ba6-112">Egy adott gép futtatásához adja át az Azonosító paramétert.</span><span class="sxs-lookup"><span data-stu-id="c0ba6-112">To get a specific machine run, pass the Id parameter.</span></span> <span data-ttu-id="c0ba6-113">Felsorolhatja az összes futtatott gépet, és mindegyiket egy adott számítógépen futtatja, és mindegyik adott állapottal fut a megfelelő paraméterek átadásával.</span><span class="sxs-lookup"><span data-stu-id="c0ba6-113">You can list all the machine runs, all runs for a specific computer, all runs with specific status by passing the corresponding parameters.</span></span>

## <span data-ttu-id="c0ba6-114">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c0ba6-114">EXAMPLES</span></span>

### <span data-ttu-id="c0ba6-115">1. példa</span><span class="sxs-lookup"><span data-stu-id="c0ba6-115">Example 1</span></span>
<span data-ttu-id="c0ba6-116">Ez a példa visszaadja a megadott azure virtuális gép összes sikertelen gépének futását.</span><span class="sxs-lookup"><span data-stu-id="c0ba6-116">This example returns all failed machine runs for the specified azure virtual machine.</span></span>


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

## <span data-ttu-id="c0ba6-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c0ba6-117">PARAMETERS</span></span>

### <span data-ttu-id="c0ba6-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="c0ba6-118">-AutomationAccountName</span></span>
<span data-ttu-id="c0ba6-119">Az automatizálási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="c0ba6-119">The automation account name.</span></span>

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

### <span data-ttu-id="c0ba6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0ba6-120">-DefaultProfile</span></span>
<span data-ttu-id="c0ba6-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c0ba6-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0ba6-122">-Id</span><span class="sxs-lookup"><span data-stu-id="c0ba6-122">-Id</span></span>
<span data-ttu-id="c0ba6-123">A futtatott szoftverfrissítési számítógép azonosítója.</span><span class="sxs-lookup"><span data-stu-id="c0ba6-123">Id of the software update machine run.</span></span>

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

### <span data-ttu-id="c0ba6-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0ba6-124">-ResourceGroupName</span></span>
<span data-ttu-id="c0ba6-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="c0ba6-125">The resource group name.</span></span>

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

### <span data-ttu-id="c0ba6-126">-SoftwareUpdateRun</span><span class="sxs-lookup"><span data-stu-id="c0ba6-126">-SoftwareUpdateRun</span></span>
<span data-ttu-id="c0ba6-127">Fut a szoftverfrissítés.</span><span class="sxs-lookup"><span data-stu-id="c0ba6-127">The software update run.</span></span>

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

### <span data-ttu-id="c0ba6-128">-SoftwareUpdateRunId</span><span class="sxs-lookup"><span data-stu-id="c0ba6-128">-SoftwareUpdateRunId</span></span>
<span data-ttu-id="c0ba6-129">A futtatott szoftverfrissítés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="c0ba6-129">Id of the software update run.</span></span>

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

### <span data-ttu-id="c0ba6-130">-Állapot</span><span class="sxs-lookup"><span data-stu-id="c0ba6-130">-Status</span></span>
<span data-ttu-id="c0ba6-131">A gép futtatásának állapota.</span><span class="sxs-lookup"><span data-stu-id="c0ba6-131">Status of the machine run.</span></span>

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

### <span data-ttu-id="c0ba6-132">-TargetComputer</span><span class="sxs-lookup"><span data-stu-id="c0ba6-132">-TargetComputer</span></span>
<span data-ttu-id="c0ba6-133">célgépet a gép futtatásához.</span><span class="sxs-lookup"><span data-stu-id="c0ba6-133">target computer for the machine run.</span></span>
<span data-ttu-id="c0ba6-134">Lehet egy nem az az-számítógép neve vagy egy Azure VM-erőforrásazonosító.</span><span class="sxs-lookup"><span data-stu-id="c0ba6-134">Can be either a non-az computer name or an azure VM resource id.</span></span>

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

### <span data-ttu-id="c0ba6-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0ba6-135">CommonParameters</span></span>
<span data-ttu-id="c0ba6-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0ba6-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0ba6-137">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0ba6-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0ba6-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c0ba6-138">INPUTS</span></span>

### <span data-ttu-id="c0ba6-139">System.Guid</span><span class="sxs-lookup"><span data-stu-id="c0ba6-139">System.Guid</span></span>

### <span data-ttu-id="c0ba6-140">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateRun</span><span class="sxs-lookup"><span data-stu-id="c0ba6-140">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateRun</span></span>

### <span data-ttu-id="c0ba6-141">System.Nullable'1[[Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateMachineRunStatus, Microsoft.Azure.PowerShell.Cmdlets.Automation, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="c0ba6-141">System.Nullable\`1[[Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateMachineRunStatus, Microsoft.Azure.PowerShell.Cmdlets.Automation, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="c0ba6-142">System.String</span><span class="sxs-lookup"><span data-stu-id="c0ba6-142">System.String</span></span>

## <span data-ttu-id="c0ba6-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c0ba6-143">OUTPUTS</span></span>

### <span data-ttu-id="c0ba6-144">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateMachineRun</span><span class="sxs-lookup"><span data-stu-id="c0ba6-144">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateMachineRun</span></span>

## <span data-ttu-id="c0ba6-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c0ba6-145">NOTES</span></span>

## <span data-ttu-id="c0ba6-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c0ba6-146">RELATED LINKS</span></span>
