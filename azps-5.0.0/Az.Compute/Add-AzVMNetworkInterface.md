---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: BF80D456-DAB1-4B51-B50F-A75C2C66A472
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmnetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMNetworkInterface.md
ms.openlocfilehash: 3c0a88d53ea1d2c6b77e08ab29a7def3ae9ee445
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195227"
---
# <span data-ttu-id="5d2e5-101">Add-AzVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="5d2e5-101">Add-AzVMNetworkInterface</span></span>

## <span data-ttu-id="5d2e5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5d2e5-102">SYNOPSIS</span></span>
<span data-ttu-id="5d2e5-103">Hálózati felületet ad hozzá egy virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="5d2e5-103">Adds a network interface to a virtual machine.</span></span>

## <span data-ttu-id="5d2e5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5d2e5-104">SYNTAX</span></span>

### <span data-ttu-id="5d2e5-105">GetNicFromNicId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5d2e5-105">GetNicFromNicId (Default)</span></span>
```
Add-AzVMNetworkInterface [-VM] <PSVirtualMachine> [-Id] <String> [-Primary]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5d2e5-106">GetNicFromNicObject</span><span class="sxs-lookup"><span data-stu-id="5d2e5-106">GetNicFromNicObject</span></span>
```
Add-AzVMNetworkInterface [-VM] <PSVirtualMachine>
 [-NetworkInterface] <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.INetworkInterfaceReference]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5d2e5-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="5d2e5-107">DESCRIPTION</span></span>
<span data-ttu-id="5d2e5-108">A **Add-AzVMNetworkInterface** parancsmag hálózati felületet ad hozzá egy virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="5d2e5-108">The **Add-AzVMNetworkInterface** cmdlet adds a network interface to a virtual machine.</span></span>
<span data-ttu-id="5d2e5-109">Hozzáadhat egy felületet a virtuális gép létrehozásakor, vagy hozzáadhat egyet egy meglévő virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="5d2e5-109">You can add an interface when you create a virtual machine or add one to an existing virtual machine.</span></span>

## <span data-ttu-id="5d2e5-110">Példák</span><span class="sxs-lookup"><span data-stu-id="5d2e5-110">EXAMPLES</span></span>

### <span data-ttu-id="5d2e5-111">1. példa: hálózati felület felvétele új virtuális gépre</span><span class="sxs-lookup"><span data-stu-id="5d2e5-111">Example 1: Add a network interface to a new virtual machine</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> Add-AzVMNetworkInterface -VM $VirtualMachine -Id "/subscriptions/46fc8ea4-2de6-4179-8ab1-365da4121af4/resourceGroups/contoso/providers/Microsoft.Network/networkInterfaces/sshNIC"
```

<span data-ttu-id="5d2e5-112">Az első parancs létrehoz egy virtuálisgép-objektumot, majd a $VirtualMachine változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="5d2e5-112">The first command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="5d2e5-113">A parancs nevet és méretet rendel a virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="5d2e5-113">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="5d2e5-114">A második parancs hozzáadja a hálózati felületet a $VirtualMachineban tárolt virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="5d2e5-114">The second command adds a network interface to the virtual machine stored in $VirtualMachine.</span></span>

### <span data-ttu-id="5d2e5-115">2. példa: hálózati felület felvétele meglévő virtuális géphez</span><span class="sxs-lookup"><span data-stu-id="5d2e5-115">Example 2: Add a network interface to an existing virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> Add-AzVMNetworkInterface -VM $VirtualMachine -Id "/subscriptions/46fc8ea4-2de6-4179-8ab1-365da4121af4/resourceGroups/contoso/providers/Microsoft.Network/networkInterfaces/sshNIC"
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="5d2e5-116">Az első parancs a **Get-AzVM** parancsmag használatával kapja meg a VirtualMachine07 nevű virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="5d2e5-116">The first command gets the virtual machine named VirtualMachine07 by using the **Get-AzVM** cmdlet.</span></span>
<span data-ttu-id="5d2e5-117">A parancs a virtuális gépet a $VirtualMachine változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="5d2e5-117">The command stores the virtual machine in the $VirtualMachine variable.</span></span>
<span data-ttu-id="5d2e5-118">A második parancs hozzáadja a hálózati felületet a $VirtualMachineban tárolt virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="5d2e5-118">The second command adds a network interface to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="5d2e5-119">A végleges parancs frissíti a $VirtualMachineban tárolt virtuális gép állapotát a ResourceGroup11-ban.</span><span class="sxs-lookup"><span data-stu-id="5d2e5-119">The final command updates the state of the virtual machine stored in $VirtualMachine in ResourceGroup11.</span></span>

## <span data-ttu-id="5d2e5-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5d2e5-120">PARAMETERS</span></span>

### <span data-ttu-id="5d2e5-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d2e5-121">-DefaultProfile</span></span>
<span data-ttu-id="5d2e5-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5d2e5-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5d2e5-123">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="5d2e5-123">-Id</span></span>
<span data-ttu-id="5d2e5-124">A virtuális géphez hozzáadni kívánt hálózati interfész AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="5d2e5-124">Specifies the ID of a network interface to add to a virtual machine.</span></span>
<span data-ttu-id="5d2e5-125">A [Get-AzNetworkInterface](/powershell/module/az.network/get-aznetworkinterface) parancsmaggal hálózati felületet lehet beolvasni.</span><span class="sxs-lookup"><span data-stu-id="5d2e5-125">You can use the [Get-AzNetworkInterface](/powershell/module/az.network/get-aznetworkinterface) cmdlet to obtain a network interface.</span></span>

```yaml
Type: System.String
Parameter Sets: GetNicFromNicId
Aliases: NicId, NetworkInterfaceId

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d2e5-126">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="5d2e5-126">-NetworkInterface</span></span>
<span data-ttu-id="5d2e5-127">A hálózati felületet adja meg.</span><span class="sxs-lookup"><span data-stu-id="5d2e5-127">Specifies the network interface.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.INetworkInterfaceReference]
Parameter Sets: GetNicFromNicObject
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5d2e5-128">-Elsődleges</span><span class="sxs-lookup"><span data-stu-id="5d2e5-128">-Primary</span></span>
<span data-ttu-id="5d2e5-129">Jelzi, hogy ez a parancsmag hozzáadja a hálózati felületet az elsődleges felülethez.</span><span class="sxs-lookup"><span data-stu-id="5d2e5-129">Indicates that this cmdlet adds the network interface as the primary interface.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetNicFromNicId
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d2e5-130">-VM</span><span class="sxs-lookup"><span data-stu-id="5d2e5-130">-VM</span></span>
<span data-ttu-id="5d2e5-131">Annak a helyi virtuális gép-objektumnak a megadása, amelyhez hálózati felületet szeretne adni.</span><span class="sxs-lookup"><span data-stu-id="5d2e5-131">Specifies a local virtual machine object to which to add a network interface.</span></span>
<span data-ttu-id="5d2e5-132">Virtuális gép létrehozásához használja a **New-AzVMConfig** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="5d2e5-132">To create a virtual machine, use the **New-AzVMConfig** cmdlet.</span></span>
<span data-ttu-id="5d2e5-133">Ha egy meglévő virtuális gépet szeretne beolvasni, használja a **Get-AzVM** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="5d2e5-133">To obtain an existing virtual machine, use the **Get-AzVM** cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5d2e5-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d2e5-134">CommonParameters</span></span>
<span data-ttu-id="5d2e5-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5d2e5-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d2e5-136">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="5d2e5-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d2e5-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5d2e5-137">INPUTS</span></span>

### <span data-ttu-id="5d2e5-138">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="5d2e5-138">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="5d2e5-139">System. String</span><span class="sxs-lookup"><span data-stu-id="5d2e5-139">System.String</span></span>

### <span data-ttu-id="5d2e5-140">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Management. internal. Network. Common. INetworkInterfaceReference, Microsoft. Azure. PowerShell. clients. Network, Version = 1.0.0.0, Culture = semleges, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="5d2e5-140">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Internal.Network.Common.INetworkInterfaceReference, Microsoft.Azure.PowerShell.Clients.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="5d2e5-141">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="5d2e5-141">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="5d2e5-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5d2e5-142">OUTPUTS</span></span>

### <span data-ttu-id="5d2e5-143">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="5d2e5-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="5d2e5-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5d2e5-144">NOTES</span></span>

## <span data-ttu-id="5d2e5-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5d2e5-145">RELATED LINKS</span></span>

[<span data-ttu-id="5d2e5-146">Új – AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="5d2e5-146">New-AzVMConfig</span></span>](./New-AzVMConfig.md)

[<span data-ttu-id="5d2e5-147">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="5d2e5-147">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="5d2e5-148">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="5d2e5-148">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)
