---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: FC6BC096-DBC4-48DA-A366-B87EB18A0496
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmss.md
ms.openlocfilehash: 881908cf85ff4f22fb76b7222a2c09d40a1e9e32
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836772"
---
# <span data-ttu-id="0844b-101">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="0844b-101">Get-AzVmss</span></span>

## <span data-ttu-id="0844b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0844b-102">SYNOPSIS</span></span>
<span data-ttu-id="0844b-103">Beolvassa a VMSS tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="0844b-103">Gets the properties of a VMSS.</span></span>

## <span data-ttu-id="0844b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0844b-104">SYNTAX</span></span>

### <span data-ttu-id="0844b-105">DefaultParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0844b-105">DefaultParameter (Default)</span></span>
```
Get-AzVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0844b-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="0844b-106">FriendMethod</span></span>
```
Get-AzVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [-InstanceView]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0844b-107">OSUpgradeHistoryMethodParameter</span><span class="sxs-lookup"><span data-stu-id="0844b-107">OSUpgradeHistoryMethodParameter</span></span>
```
Get-AzVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [-OSUpgradeHistory]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0844b-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="0844b-108">DESCRIPTION</span></span>
<span data-ttu-id="0844b-109">A **Get-AzVmss** parancsmag a virtuálisgép-készlet (VMSS) modell-és példány nézetét kapja.</span><span class="sxs-lookup"><span data-stu-id="0844b-109">The **Get-AzVmss** cmdlet gets the model and instance view of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="0844b-110">A modell nézet a virtuális gép méretarányának a felhasználó által megadott tulajdonságait adja meg.</span><span class="sxs-lookup"><span data-stu-id="0844b-110">The model view is the user specified properties of the virtual machine scale set.</span></span>
<span data-ttu-id="0844b-111">A példány nézet a virtuális gép méretarányának a példány szintjének állapota.</span><span class="sxs-lookup"><span data-stu-id="0844b-111">The instance view is the instance level status of the virtual machine scale set.</span></span>
<span data-ttu-id="0844b-112">Adja meg a *InstanceView* paramétert úgy, hogy csak a virtuálisgép-készlet példány nézetét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="0844b-112">Specify the *InstanceView* parameter to get only the instance view of a virtual machine scale set.</span></span>

## <span data-ttu-id="0844b-113">Példák</span><span class="sxs-lookup"><span data-stu-id="0844b-113">EXAMPLES</span></span>

### <span data-ttu-id="0844b-114">Példa 1: VMSS tulajdonságainak beolvasása</span><span class="sxs-lookup"><span data-stu-id="0844b-114">Example 1: Get the properties of a VMSS</span></span>
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

<span data-ttu-id="0844b-115">Ez a parancs beolvassa a Group001 nevű erőforráscsoport VMSS001 tartozó VMSS tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="0844b-115">This command gets the properties of the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>
<span data-ttu-id="0844b-116">Mivel a parancs nem adja meg a *InstanceView* kapcsoló paramétert, a parancsmag a virtuális gép méretarányának modell nézetét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="0844b-116">Since the command does not specify the *InstanceView* switch parameter, the cmdlet gets the model view of the virtual machine scale set.</span></span>

### <span data-ttu-id="0844b-117">2. példa: egy erőforráscsoport minden Vmss beolvasása</span><span class="sxs-lookup"><span data-stu-id="0844b-117">Example 2: Get all Vmss in a resource group</span></span>
```
PS C:\> Get-AzVmss -ResourceGroupName "Group001"

ResourceGroupName                               Name       Location             Sku Capacity ProvisioningState
-----------------                               ----       --------             --- -------- -----------------
Group001                                       VMSS001      eastus Standard_DS1_v2        2         Succeeded
Group001                                       VMSS002      eastus     Standard_A1        2         Succeeded
```

<span data-ttu-id="0844b-118">Az összes Vmss beolvasása az erőforráscsoport "Group001" csoportjában</span><span class="sxs-lookup"><span data-stu-id="0844b-118">Get all Vmss in resource group "Group001"</span></span>

### <span data-ttu-id="0844b-119">3. példa: az előfizetésben szereplő összes Vmss beszerzése</span><span class="sxs-lookup"><span data-stu-id="0844b-119">Example 3: Get all Vmss in a subscription</span></span>
```
PS C:\> Get-AzVmss

ResourceGroupName                               Name       Location             Sku Capacity ProvisioningState
-----------------                               ----       --------             --- -------- -----------------
Group001                                       VMSS001      eastus Standard_DS1_v2        2         Succeeded
Group001                                       VMSS002      eastus     Standard_A1        2         Succeeded
Group002                                       VMSS003      eastus     Standard_A1        1         Succeeded
Group002                                       VMSS004      eastus Standard_DS1_v2        2         Succeeded
```

<span data-ttu-id="0844b-120">Az összes Vmss beszerzése az előfizetésbe.</span><span class="sxs-lookup"><span data-stu-id="0844b-120">Get all Vmss in subscription.</span></span>

### <span data-ttu-id="0844b-121">Példa 4: az összes Vmss beolvasása szűrés használatával</span><span class="sxs-lookup"><span data-stu-id="0844b-121">Example 4: Get all Vmss using filtering</span></span>
```
PS C:\> Get-AzVmss -Name VMSS00*

ResourceGroupName                               Name       Location             Sku Capacity ProvisioningState
-----------------                               ----       --------             --- -------- -----------------
Group001                                       VMSS001      eastus Standard_DS1_v2        2         Succeeded
Group001                                       VMSS002      eastus     Standard_A1        2         Succeeded
Group002                                       VMSS003      eastus     Standard_A1        1         Succeeded
Group002                                       VMSS004      eastus Standard_DS1_v2        2         Succeeded
```

<span data-ttu-id="0844b-122">A "VMSS00" kezdetű előfizetés összes Vmss beszerzése.</span><span class="sxs-lookup"><span data-stu-id="0844b-122">Get all Vmss in subscription that start with "VMSS00".</span></span>

## <span data-ttu-id="0844b-123">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0844b-123">PARAMETERS</span></span>

### <span data-ttu-id="0844b-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0844b-124">-DefaultProfile</span></span>
<span data-ttu-id="0844b-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0844b-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0844b-126">-InstanceView</span><span class="sxs-lookup"><span data-stu-id="0844b-126">-InstanceView</span></span>
<span data-ttu-id="0844b-127">Azt jelzi, hogy ez a parancsmag csak a virtuálisgép-készlet példányának nézetét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="0844b-127">Indicates that this cmdlet gets only the instance view of the virtual machine scale set.</span></span>

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

### <span data-ttu-id="0844b-128">-OSUpgradeHistory</span><span class="sxs-lookup"><span data-stu-id="0844b-128">-OSUpgradeHistory</span></span>
<span data-ttu-id="0844b-129">Azt jelzi, hogy ez a parancsmag a virtuális gép méretarányát tároló operációs rendszer frissítési előzményeit jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="0844b-129">Indicates that this cmdlet lists the os upgrade history of the virtual machine scale set.</span></span>

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

### <span data-ttu-id="0844b-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0844b-130">-ResourceGroupName</span></span>
<span data-ttu-id="0844b-131">A VMSS erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0844b-131">Specifies the name of the Resource Group of the VMSS.</span></span>

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

### <span data-ttu-id="0844b-132">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="0844b-132">-VMScaleSetName</span></span>
<span data-ttu-id="0844b-133">Faj: a VMSS neve.</span><span class="sxs-lookup"><span data-stu-id="0844b-133">Species the name of the VMSS.</span></span>

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

### <span data-ttu-id="0844b-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0844b-134">CommonParameters</span></span>
<span data-ttu-id="0844b-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0844b-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0844b-136">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="0844b-136">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0844b-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0844b-137">INPUTS</span></span>

### <span data-ttu-id="0844b-138">System. String</span><span class="sxs-lookup"><span data-stu-id="0844b-138">System.String</span></span>

## <span data-ttu-id="0844b-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0844b-139">OUTPUTS</span></span>

### <span data-ttu-id="0844b-140">Microsoft. Azure. commands. számítási. Automation. models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="0844b-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="0844b-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0844b-141">NOTES</span></span>

## <span data-ttu-id="0844b-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0844b-142">RELATED LINKS</span></span>

[<span data-ttu-id="0844b-143">Új – AzVmss</span><span class="sxs-lookup"><span data-stu-id="0844b-143">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="0844b-144">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="0844b-144">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="0844b-145">Újraindítás – AzVmss</span><span class="sxs-lookup"><span data-stu-id="0844b-145">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="0844b-146">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="0844b-146">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="0844b-147">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="0844b-147">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="0844b-148">Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="0844b-148">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="0844b-149">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="0844b-149">Update-AzVmss</span></span>](./Update-AzVmss.md)


