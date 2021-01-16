---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: FC6BC096-DBC4-48DA-A366-B87EB18A0496
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmss.md
ms.openlocfilehash: 7985a979f9bbb89d6594416575e3fa00640784b5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98322500"
---
# <span data-ttu-id="ae318-101">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="ae318-101">Get-AzVmss</span></span>

## <span data-ttu-id="ae318-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae318-102">SYNOPSIS</span></span>
<span data-ttu-id="ae318-103">A VMSS tulajdonságainak lekérte.</span><span class="sxs-lookup"><span data-stu-id="ae318-103">Gets the properties of a VMSS.</span></span>

## <span data-ttu-id="ae318-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ae318-104">SYNTAX</span></span>

### <span data-ttu-id="ae318-105">DefaultParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ae318-105">DefaultParameter (Default)</span></span>
```
Get-AzVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ae318-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="ae318-106">FriendMethod</span></span>
```
Get-AzVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [-InstanceView]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ae318-107">OSUpgradeHistoryMethodParameter</span><span class="sxs-lookup"><span data-stu-id="ae318-107">OSUpgradeHistoryMethodParameter</span></span>
```
Get-AzVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [-OSUpgradeHistory]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ae318-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ae318-108">DESCRIPTION</span></span>
<span data-ttu-id="ae318-109">A **Get-AzVmss** parancsmag egy virtuális gép méretarány-készletének (VMSS) modell- és példánynézetét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="ae318-109">The **Get-AzVmss** cmdlet gets the model and instance view of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="ae318-110">A modellnézet a virtuális gép méretaránykészletének felhasználó által megadott tulajdonságai.</span><span class="sxs-lookup"><span data-stu-id="ae318-110">The model view is the user specified properties of the virtual machine scale set.</span></span>
<span data-ttu-id="ae318-111">A példánynézet a virtuális gép méretaránykészletének példányszintű állapota.</span><span class="sxs-lookup"><span data-stu-id="ae318-111">The instance view is the instance level status of the virtual machine scale set.</span></span>
<span data-ttu-id="ae318-112">Adja meg *a InstanceView* paramétert, hogy csak egy virtuális gép méretaránykészletének példánynézetét szerezze be.</span><span class="sxs-lookup"><span data-stu-id="ae318-112">Specify the *InstanceView* parameter to get only the instance view of a virtual machine scale set.</span></span>

## <span data-ttu-id="ae318-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ae318-113">EXAMPLES</span></span>

### <span data-ttu-id="ae318-114">1. példa: VMSS-tulajdonságok lekérte</span><span class="sxs-lookup"><span data-stu-id="ae318-114">Example 1: Get the properties of a VMSS</span></span>
```
PS C:\> Get-AzVmss -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"

ResourceGroupName                           : Group001
Sku                                         :
  Name                                      : Standard_DS1_v2
  Tier                                      : Standard
  Capacity                                  : 2
UpgradePolicy                               :
  Mode                                      : Manual
VirtualMachineProfile                       :
  OsProfile                                 :
    ComputerNamePrefix                      : test
    AdminUsername                           : contoso
    WindowsConfiguration                    :
      ProvisionVMAgent                      : True
      EnableAutomaticUpdates                : True
  StorageProfile                            :
    ImageReference                          :
      Publisher                             : MicrosoftWindowsServer
      Offer                                 : WindowsServer
      Sku                                   : 2016-Datacenter
      Version                               : latest
    OsDisk                                  :
      Caching                               : None
      CreateOption                          : FromImage
      ManagedDisk                           :
        StorageAccountType                  : Premium_LRS
  NetworkProfile                            :
    NetworkInterfaceConfigurations[0]       :
      Name                                  : Group001
      Primary                               : True
      EnableAcceleratedNetworking           : False
      NetworkSecurityGroup                  :
        Id                                  : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/Group001
/providers/Microsoft.Network/networkSecurityGroups/Group001
      DnsSettings                           :
      IpConfigurations[0]                   :
        Name                                : Group001
        Subnet                              :
          Id                                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/group001
/providers/Microsoft.Network/virtualNetworks/Group001/subnets/Group001
        PrivateIPAddressVersion             : IPv4
        LoadBalancerBackendAddressPools[0]  :
          Id                                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/group001
/providers/Microsoft.Network/loadBalancers/Group001/backendAddressPools/Group001
        LoadBalancerInboundNatPools[0]      :
          Id                                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/group001
/providers/Microsoft.Network/loadBalancers/Group001/inboundNatPools/Group001
        LoadBalancerInboundNatPools[1]      :
          Id                                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/group001
/providers/Microsoft.Network/loadBalancers/Group001/inboundNatPools/Group001
      EnableIPForwarding                    : False
ProvisioningState                           : Succeeded
Overprovision                               : True
UniqueId                                    : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SinglePlacementGroup                        : False
Id                                          : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/Group001/
providers/Microsoft.Compute/virtualMachineScaleSets/VMSS001
Name                                        : VMSS001
Type                                        : Microsoft.Compute/virtualMachineScaleSets
Location                                    : eastus
Tags                                        : {}
```

<span data-ttu-id="ae318-115">Ez a parancs a VMSS001 nevű VMSSS tulajdonságát kapja meg, amely a Group0001 nevű erőforráscsoporthoz tartozik.</span><span class="sxs-lookup"><span data-stu-id="ae318-115">This command gets the properties of the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>
<span data-ttu-id="ae318-116">Mivel a parancs nem adja meg a *InstanceView* kapcsoló paramétert, a parancsmag megkapja a virtuális gép méretaránykészletének modellnézetét.</span><span class="sxs-lookup"><span data-stu-id="ae318-116">Since the command does not specify the *InstanceView* switch parameter, the cmdlet gets the model view of the virtual machine scale set.</span></span>

### <span data-ttu-id="ae318-117">2. példa: Erőforráscsoport összes vmsének be szereznie</span><span class="sxs-lookup"><span data-stu-id="ae318-117">Example 2: Get all Vmss in a resource group</span></span>
```
PS C:\> Get-AzVmss -ResourceGroupName "Group001"

ResourceGroupName                               Name       Location             Sku Capacity ProvisioningState
-----------------                               ----       --------             --- -------- -----------------
Group001                                       VMSS001      eastus Standard_DS1_v2        2         Succeeded
Group001                                       VMSS002      eastus     Standard_A1        2         Succeeded
```

<span data-ttu-id="ae318-118">A "Group001" erőforráscsoport összes vmsének lekérte</span><span class="sxs-lookup"><span data-stu-id="ae318-118">Get all Vmss in resource group "Group001"</span></span>

### <span data-ttu-id="ae318-119">3. példa: Az előfizetésben található összes vm lekérte</span><span class="sxs-lookup"><span data-stu-id="ae318-119">Example 3: Get all Vmss in a subscription</span></span>
```
PS C:\> Get-AzVmss

ResourceGroupName                               Name       Location             Sku Capacity ProvisioningState
-----------------                               ----       --------             --- -------- -----------------
Group001                                       VMSS001      eastus Standard_DS1_v2        2         Succeeded
Group001                                       VMSS002      eastus     Standard_A1        2         Succeeded
Group002                                       VMSS003      eastus     Standard_A1        1         Succeeded
Group002                                       VMSS004      eastus Standard_DS1_v2        2         Succeeded
```

<span data-ttu-id="ae318-120">Szerezze be az előfizetésben található összes Vms-et.</span><span class="sxs-lookup"><span data-stu-id="ae318-120">Get all Vmss in subscription.</span></span>

### <span data-ttu-id="ae318-121">4. példa: Az összes vms lekérte szűrés használatával</span><span class="sxs-lookup"><span data-stu-id="ae318-121">Example 4: Get all Vmss using filtering</span></span>
```
PS C:\> Get-AzVmss -Name VMSS00*

ResourceGroupName                               Name       Location             Sku Capacity ProvisioningState
-----------------                               ----       --------             --- -------- -----------------
Group001                                       VMSS001      eastus Standard_DS1_v2        2         Succeeded
Group001                                       VMSS002      eastus     Standard_A1        2         Succeeded
Group002                                       VMSS003      eastus     Standard_A1        1         Succeeded
Group002                                       VMSS004      eastus Standard_DS1_v2        2         Succeeded
```

<span data-ttu-id="ae318-122">Szerezze be az előfizetésben a "VMSS00" kezdettől induló összes vmst.</span><span class="sxs-lookup"><span data-stu-id="ae318-122">Get all Vmss in subscription that start with "VMSS00".</span></span>

## <span data-ttu-id="ae318-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ae318-123">PARAMETERS</span></span>

### <span data-ttu-id="ae318-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae318-124">-DefaultProfile</span></span>
<span data-ttu-id="ae318-125">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ae318-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ae318-126">-InstanceView</span><span class="sxs-lookup"><span data-stu-id="ae318-126">-InstanceView</span></span>
<span data-ttu-id="ae318-127">Azt jelzi, hogy ez a parancsmag csak a virtuális gép méretaránykészletének példánynézetét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="ae318-127">Indicates that this cmdlet gets only the instance view of the virtual machine scale set.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FriendMethod
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae318-128">-OSUpgradeHistory</span><span class="sxs-lookup"><span data-stu-id="ae318-128">-OSUpgradeHistory</span></span>
<span data-ttu-id="ae318-129">Azt jelzi, hogy ez a parancsmag felsorolja a virtuális gép méretkészletének os frissítési előzményeit.</span><span class="sxs-lookup"><span data-stu-id="ae318-129">Indicates that this cmdlet lists the os upgrade history of the virtual machine scale set.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: OSUpgradeHistoryMethodParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae318-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae318-130">-ResourceGroupName</span></span>
<span data-ttu-id="ae318-131">A VMSS erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ae318-131">Specifies the name of the Resource Group of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="ae318-132">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="ae318-132">-VMScaleSetName</span></span>
<span data-ttu-id="ae318-133">A VMSS nevének fakása.</span><span class="sxs-lookup"><span data-stu-id="ae318-133">Species the name of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="ae318-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae318-134">CommonParameters</span></span>
<span data-ttu-id="ae318-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae318-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae318-136">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ae318-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae318-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ae318-137">INPUTS</span></span>

### <span data-ttu-id="ae318-138">System.String</span><span class="sxs-lookup"><span data-stu-id="ae318-138">System.String</span></span>

## <span data-ttu-id="ae318-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ae318-139">OUTPUTS</span></span>

### <span data-ttu-id="ae318-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="ae318-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="ae318-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ae318-141">NOTES</span></span>

## <span data-ttu-id="ae318-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ae318-142">RELATED LINKS</span></span>

[<span data-ttu-id="ae318-143">Új-AzVms</span><span class="sxs-lookup"><span data-stu-id="ae318-143">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="ae318-144">Remove-AzVms</span><span class="sxs-lookup"><span data-stu-id="ae318-144">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="ae318-145">Restart-AzVms</span><span class="sxs-lookup"><span data-stu-id="ae318-145">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="ae318-146">Set-AzVms</span><span class="sxs-lookup"><span data-stu-id="ae318-146">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="ae318-147">Start-AzVms</span><span class="sxs-lookup"><span data-stu-id="ae318-147">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="ae318-148">Stop-AzVms</span><span class="sxs-lookup"><span data-stu-id="ae318-148">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="ae318-149">Update-AzVms</span><span class="sxs-lookup"><span data-stu-id="ae318-149">Update-AzVmss</span></span>](./Update-AzVmss.md)


