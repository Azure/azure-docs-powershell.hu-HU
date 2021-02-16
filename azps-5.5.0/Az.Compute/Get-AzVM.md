---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 6250EC11-79CF-428B-A72F-9BD72C1751F0
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVM.md
ms.openlocfilehash: f1103e8fc7ed9646aa6b91bc0336e331f7ada990
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100148947"
---
# <span data-ttu-id="9687b-101">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="9687b-101">Get-AzVM</span></span>

## <span data-ttu-id="9687b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9687b-102">SYNOPSIS</span></span>
<span data-ttu-id="9687b-103">Egy virtuális gép tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="9687b-103">Gets the properties of a virtual machine.</span></span>

## <span data-ttu-id="9687b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9687b-104">SYNTAX</span></span>

### <span data-ttu-id="9687b-105">DefaultParamSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9687b-105">DefaultParamSet (Default)</span></span>
```
Get-AzVM [[-ResourceGroupName] <String>] [[-Name] <String>] [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9687b-106">GetVirtualMachineInResourceGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="9687b-106">GetVirtualMachineInResourceGroupParamSet</span></span>
```
Get-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Status] [-DisplayHint <DisplayHintType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9687b-107">ListLocationVirtualMachinesParamSet</span><span class="sxs-lookup"><span data-stu-id="9687b-107">ListLocationVirtualMachinesParamSet</span></span>
```
Get-AzVM -Location <String> [-Status] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9687b-108">ListNextLinkVirtualMachinesParamSet</span><span class="sxs-lookup"><span data-stu-id="9687b-108">ListNextLinkVirtualMachinesParamSet</span></span>
```
Get-AzVM [-Status] [-NextLink] <Uri> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9687b-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9687b-109">DESCRIPTION</span></span>
<span data-ttu-id="9687b-110">A **Get-AzVM parancsmag** egy Azure virtuális gép modellnézetét vagy példánynézetét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="9687b-110">The **Get-AzVM** cmdlet gets the model view or the instance view of an Azure virtual machine.</span></span>
<span data-ttu-id="9687b-111">A modellnézet a virtuális gép felhasználó által megadott tulajdonságai.</span><span class="sxs-lookup"><span data-stu-id="9687b-111">The model view is the user specified properties of the virtual machine.</span></span>
<span data-ttu-id="9687b-112">A példánynézet a virtuális gép példányszintű állapota.</span><span class="sxs-lookup"><span data-stu-id="9687b-112">The instance view is the instance level status of the virtual machine.</span></span>
<span data-ttu-id="9687b-113">Adja meg *az Állapot* paramétert, hogy egy virtuális gép példánynézetét használja az alapértelmezett modellnézet helyett.</span><span class="sxs-lookup"><span data-stu-id="9687b-113">Specify the *Status* parameter to get the instance view of a virtual machine instead of the model view which is the default.</span></span>

## <span data-ttu-id="9687b-114">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9687b-114">EXAMPLES</span></span>

### <span data-ttu-id="9687b-115">1. példa: Modell- és példánynézet-tulajdonságok lekérte</span><span class="sxs-lookup"><span data-stu-id="9687b-115">Example 1: Get model and instance view properties</span></span>
```
PS C:\> Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"

ResourceGroupName        : ResourceGroup11
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup11/providers/M
icrosoft.Compute/virtualMachines/VirtualMachine07
VmId                     : 00000000-0000-0000-0000-000000000000
Name                     : VirtualMachine07
Type                     : Microsoft.Compute/virtualMachines
Location                 : eastus
Tags                     : {"creationSource":"acs-VirtualMachine07"}
AvailabilitySetReference : {Id}
DiagnosticsProfile       : {BootDiagnostics}
Extensions               : {linuxdiagnostic, waitforleader}
HardwareProfile          : {VmSize}
NetworkProfile           : {NetworkInterfaces}
OSProfile                : {ComputerName, AdminUsername, LinuxConfiguration, Secrets}
ProvisioningState        : Succeeded
StorageProfile           : {ImageReference, OsDisk, DataDisks}
```

<span data-ttu-id="9687b-116">Ez a parancs a VirtualMachine07 nevű virtuális gép modellnézet- és példánynézet-tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="9687b-116">This command gets the model view and instance view properties of the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="9687b-117">2. példa: Példánynézet tulajdonságainak lekérte</span><span class="sxs-lookup"><span data-stu-id="9687b-117">Example 2: Get instance view properties</span></span>
```
PS C:\> Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Status

ResourceGroupName       : ResourceGroup11
Name                    : VirtualMachine07
Disks[0]                :
  Name                  : VirtualMachine07-osdisk
  Statuses[0]           :
    Code                : ProvisioningState/succeeded
    Level               : Info
    DisplayStatus       : Provisioning succeeded
    Time                : 3/1/2019 12:59:30 AM
Extensions[0]           :
  Name                  : linuxdiagnostic
  Type                  : Microsoft.OSTCExtensions.LinuxDiagnostic
  TypeHandlerVersion    : 2.3.9029
  Statuses[0]           :
    Code                : ProvisioningState/succeeded
    Level               : Info
    DisplayStatus       : Provisioning succeeded
    Message             : Invalid config settings given: Empty storageAccountName. Install will proceed, but enable
can't proceed, in which case it's still considered a success as it's an external error.
Extensions[1]           :
  Name                  : waitforleader
  Type                  : Microsoft.OSTCExtensions.CustomScriptForLinux
  TypeHandlerVersion    : 1.5.4
  Statuses[0]           :
    Code                : ProvisioningState/succeeded
    Level               : Info
    DisplayStatus       : Provisioning succeeded
    Message             : Command is finished.
---stdout---
waiting for leader.mesos
waiting for leader.mesos
waiting for leader.mesos
waiting for leader.mesos
waiting for leader.mesos
waiting for leader.mesos
PING leader.mesos (xxx.xx.x.x) 56(84) bytes of data.
64 bytes from xxx.xx.x.x: icmp_seq=1 ttl=64 time=0.022 ms

--- leader.mesos ping statistics ---
1 packets transmitted, 1 received, 0% packet loss, time 0ms
rtt min/avg/max/mdev = 0.022/0.022/0.022/0.000 ms
leader.mesos up

---errout---
ping: unknown host leader.mesos
ping: unknown host leader.mesos
ping: unknown host leader.mesos
ping: unknown host leader.mesos
ping: unknown host leader.mesos
ping: unknown host leader.mesos


PlatformFaultDomain     : 0
PlatformUpdateDomain    : 0
VMAgent                 :
  VmAgentVersion        : 2.2.37
  ExtensionHandlers[0]  :
    Type                : Microsoft.OSTCExtensions.LinuxDiagnostic
    TypeHandlerVersion  : 2.3.9029
    Status              :
      Code              : ProvisioningState/succeeded
      Level             : Info
      DisplayStatus     : Ready
      Message           : Plugin enabled
  ExtensionHandlers[1]  :
    Type                : Microsoft.OSTCExtensions.CustomScriptForLinux
    TypeHandlerVersion  : 1.5.4
    Status              :
      Code              : ProvisioningState/succeeded
      Level             : Info
      DisplayStatus     : Ready
      Message           : Plugin enabled
  Statuses[0]           :
    Code                : ProvisioningState/succeeded
    Level               : Info
    DisplayStatus       : Ready
    Message             : Guest Agent is running
    Time                : 3/1/2019 2:04:12 AM
Statuses[0]             :
  Code                  : ProvisioningState/succeeded
  Level                 : Info
  DisplayStatus         : Provisioning succeeded
  Time                  : 3/1/2019 1:01:57 AM
Statuses[1]             :
  Code                  : PowerState/running
  Level                 : Info
  DisplayStatus         : VM running
```

<span data-ttu-id="9687b-118">Ez a parancs a VirtualMachine07 nevű virtuális gép tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="9687b-118">This command gets properties of the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="9687b-119">Ez a parancs az Állapot *paramétert adja* meg.</span><span class="sxs-lookup"><span data-stu-id="9687b-119">This command specifies the *Status* parameter.</span></span>
<span data-ttu-id="9687b-120">Ezért a parancs csak a példánynézet tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="9687b-120">Therefore, the command gets only the instance view properties.</span></span>

### <span data-ttu-id="9687b-121">3. példa: Az erőforráscsoport összes virtuális gépének tulajdonságainak lekérte</span><span class="sxs-lookup"><span data-stu-id="9687b-121">Example 3: Get properties for all virtual machines in a resource group</span></span>
```
PS C:\> Get-AzVM -ResourceGroupName "ResourceGroup11"

ResourceGroupName    Name       Location          VmSize  OsType            NIC
-----------------    ----       --------          ------  ------            ---
ResourceGroup11     test1         eastus Standard_DS1_v2 Windows          test1
ResourceGroup11     test2         westus Standard_DS1_v2 Windows          test2
ResourceGroup11     test3         eastus Standard_DS1_v2 Windows          test3
```

<span data-ttu-id="9687b-122">Ez a parancs az Erőforráscsoport11 nevű erőforráscsoport összes virtuális gépének tulajdonságait beveszi.</span><span class="sxs-lookup"><span data-stu-id="9687b-122">This command gets properties for all the virtual machines in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="9687b-123">4. példa: Az előfizetés összes virtuális gépének lekérte</span><span class="sxs-lookup"><span data-stu-id="9687b-123">Example 4: Get all virtual machines in your subscription</span></span>
```
PS C:\> Get-AzVM

ResourceGroupName    Name       Location          VmSize  OsType            NIC
-----------------    ----       --------          ------  ------            ---
TEST1               test1         eastus Standard_DS1_v2 Windows          test1
TEST1               test2         westus Standard_DS1_v2 Windows          test2
TEST1               test3         eastus Standard_DS1_v2 Windows          test3
TEST2               test4         westus Standard_DS1_v2 Windows          test4
TEST2               test5         eastus Standard_DS1_v2 Windows          test5
```

<span data-ttu-id="9687b-124">Ez a parancs az előfizetés összes virtuális gépét megkapja.</span><span class="sxs-lookup"><span data-stu-id="9687b-124">This command gets all the virtual machines in your subscription.</span></span>

### <span data-ttu-id="9687b-125">5. példa: Az összes virtuális gép lekérte a helyet.</span><span class="sxs-lookup"><span data-stu-id="9687b-125">Example 5: Get all virtual machines in the location.</span></span>
```
PS C:\> Get-AzVM -Location "westus"

ResourceGroupName    Name       Location          VmSize  OsType            NIC
-----------------    ----       --------          ------  ------            ---
TEST1               test2         westus Standard_DS1_v2 Windows          test2
TEST2               test4         westus Standard_DS1_v2 Windows          test4
```

<span data-ttu-id="9687b-126">Ez a parancs a nyugat-amerikai régió összes virtuális gépét beveszi.</span><span class="sxs-lookup"><span data-stu-id="9687b-126">This command gets all the virtual machines in West US region.</span></span>

### <span data-ttu-id="9687b-127">6. példa: Az összes virtuális gép behozása szűrés használatával</span><span class="sxs-lookup"><span data-stu-id="9687b-127">Example 6: Get all virtual machines using filtering</span></span>
```
PS C:\> Get-AzVM -Name test*

ResourceGroupName    Name       Location          VmSize  OsType            NIC
-----------------    ----       --------          ------  ------            ---
TEST1               test1         eastus Standard_DS1_v2 Windows          test1
TEST1               test2         westus Standard_DS1_v2 Windows          test2
TEST1               test3         eastus Standard_DS1_v2 Windows          test3
TEST2               test4         westus Standard_DS1_v2 Windows          test4
TEST2               test5         eastus Standard_DS1_v2 Windows          test5
```

<span data-ttu-id="9687b-128">Ez a parancs az előfizetés összes olyan virtuális gépét lekérte, amelyek a "teszt" kezdetével kezdődnek.</span><span class="sxs-lookup"><span data-stu-id="9687b-128">This command gets all the virtual machines in your subscription that start with "test".</span></span>

## <span data-ttu-id="9687b-129">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9687b-129">PARAMETERS</span></span>

### <span data-ttu-id="9687b-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9687b-130">-DefaultProfile</span></span>
<span data-ttu-id="9687b-131">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9687b-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9687b-132">-DisplayHint</span><span class="sxs-lookup"><span data-stu-id="9687b-132">-DisplayHint</span></span>
<span data-ttu-id="9687b-133">Meghatározza, hogyan jelenik meg a virtuális gépi objektum.</span><span class="sxs-lookup"><span data-stu-id="9687b-133">Determines how the virtual machine object is displayed.</span></span>
<span data-ttu-id="9687b-134">Érvényes értékek: -- Kompakt: csak a legfelső szintű tulajdonságokat jeleníti meg – Kibontás: az összes tulajdonság megjelenítése minden szinten</span><span class="sxs-lookup"><span data-stu-id="9687b-134">Valid values are: -- Compact: displays only top level properties -- Expand: displays all properties in all levels</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.DisplayHintType
Parameter Sets: GetVirtualMachineInResourceGroupParamSet
Aliases:
Accepted values: Compact, Expand

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9687b-135">-Location</span><span class="sxs-lookup"><span data-stu-id="9687b-135">-Location</span></span>
<span data-ttu-id="9687b-136">Megadja a virtuális gépek listába sorolni helyét.</span><span class="sxs-lookup"><span data-stu-id="9687b-136">Specifies a location for the virtual machines to list.</span></span>

```yaml
Type: System.String
Parameter Sets: ListLocationVirtualMachinesParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9687b-137">-Name</span><span class="sxs-lookup"><span data-stu-id="9687b-137">-Name</span></span>
<span data-ttu-id="9687b-138">A lekért virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9687b-138">Specifies the name of the virtual machine to get.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParamSet
Aliases: ResourceName, VMName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: GetVirtualMachineInResourceGroupParamSet
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="9687b-139">-NextLink</span><span class="sxs-lookup"><span data-stu-id="9687b-139">-NextLink</span></span>
<span data-ttu-id="9687b-140">A következő hivatkozást adja meg.</span><span class="sxs-lookup"><span data-stu-id="9687b-140">Specifies the next link.</span></span>

```yaml
Type: System.Uri
Parameter Sets: ListNextLinkVirtualMachinesParamSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9687b-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9687b-141">-ResourceGroupName</span></span>
<span data-ttu-id="9687b-142">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9687b-142">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParamSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: GetVirtualMachineInResourceGroupParamSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="9687b-143">-Állapot</span><span class="sxs-lookup"><span data-stu-id="9687b-143">-Status</span></span>
<span data-ttu-id="9687b-144">Azt jelzi, hogy ez a parancsmag csak a virtuális gép példánynézetét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="9687b-144">Indicates that this cmdlet gets only the instance view of the virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9687b-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9687b-145">CommonParameters</span></span>
<span data-ttu-id="9687b-146">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9687b-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9687b-147">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9687b-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9687b-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9687b-148">INPUTS</span></span>

### <span data-ttu-id="9687b-149">System.String</span><span class="sxs-lookup"><span data-stu-id="9687b-149">System.String</span></span>

### <span data-ttu-id="9687b-150">System.Uri</span><span class="sxs-lookup"><span data-stu-id="9687b-150">System.Uri</span></span>

### <span data-ttu-id="9687b-151">Microsoft.Azure.Commands.Compute.Models.DisplayHintType</span><span class="sxs-lookup"><span data-stu-id="9687b-151">Microsoft.Azure.Commands.Compute.Models.DisplayHintType</span></span>

## <span data-ttu-id="9687b-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9687b-152">OUTPUTS</span></span>

### <span data-ttu-id="9687b-153">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="9687b-153">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="9687b-154">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineInstanceView</span><span class="sxs-lookup"><span data-stu-id="9687b-154">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineInstanceView</span></span>

## <span data-ttu-id="9687b-155">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9687b-155">NOTES</span></span>

## <span data-ttu-id="9687b-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9687b-156">RELATED LINKS</span></span>

[<span data-ttu-id="9687b-157">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="9687b-157">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="9687b-158">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="9687b-158">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="9687b-159">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="9687b-159">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="9687b-160">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="9687b-160">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="9687b-161">Stop-AzVM</span><span class="sxs-lookup"><span data-stu-id="9687b-161">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="9687b-162">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="9687b-162">Update-AzVM</span></span>](./Update-AzVM.md)


