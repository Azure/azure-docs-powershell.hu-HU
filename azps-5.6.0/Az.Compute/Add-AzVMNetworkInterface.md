---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: BF80D456-DAB1-4B51-B50F-A75C2C66A472
online version: https://docs.microsoft.com/powershell/module/az.compute/add-azvmnetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMNetworkInterface.md
ms.openlocfilehash: efe587cf01fa2adf16e4b6beaaa319312f3c9fa5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101927401"
---
# <span data-ttu-id="94095-101">Add-AzVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="94095-101">Add-AzVMNetworkInterface</span></span>

## <span data-ttu-id="94095-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94095-102">SYNOPSIS</span></span>
<span data-ttu-id="94095-103">Hálózati felületet ad hozzá egy virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="94095-103">Adds a network interface to a virtual machine.</span></span>

## <span data-ttu-id="94095-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="94095-104">SYNTAX</span></span>

### <span data-ttu-id="94095-105">GetNicFromNicId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="94095-105">GetNicFromNicId (Default)</span></span>
```
Add-AzVMNetworkInterface [-VM] <PSVirtualMachine> [-Id] <String> [-Primary]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94095-106">GetNicFromNicObject</span><span class="sxs-lookup"><span data-stu-id="94095-106">GetNicFromNicObject</span></span>
```
Add-AzVMNetworkInterface [-VM] <PSVirtualMachine>
 [-NetworkInterface] <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.INetworkInterfaceReference]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="94095-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="94095-107">DESCRIPTION</span></span>
<span data-ttu-id="94095-108">Az **Add-AzVMNetworkInterface** parancsmag hálózati felületet ad egy virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="94095-108">The **Add-AzVMNetworkInterface** cmdlet adds a network interface to a virtual machine.</span></span>
<span data-ttu-id="94095-109">Felületet akkor adhat hozzá, amikor létrehoz egy virtuális gépet, vagy hozzáad egyet egy meglévő virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="94095-109">You can add an interface when you create a virtual machine or add one to an existing virtual machine.</span></span>

## <span data-ttu-id="94095-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="94095-110">EXAMPLES</span></span>

### <span data-ttu-id="94095-111">1. példa: Hálózati felület hozzáadása új virtuális géphez</span><span class="sxs-lookup"><span data-stu-id="94095-111">Example 1: Add a network interface to a new virtual machine</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> Add-AzVMNetworkInterface -VM $VirtualMachine -Id "/subscriptions/46fc8ea4-2de6-4179-8ab1-365da4121af4/resourceGroups/contoso/providers/Microsoft.Network/networkInterfaces/sshNIC"
```

<span data-ttu-id="94095-112">Az első parancs létrehoz egy virtuális gépi objektumot, majd tárolja azt a $VirtualMachine változóban.</span><span class="sxs-lookup"><span data-stu-id="94095-112">The first command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="94095-113">A parancs nevet és méretet rendel a virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="94095-113">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="94095-114">A második parancs hozzáad egy hálózati felületet a $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="94095-114">The second command adds a network interface to the virtual machine stored in $VirtualMachine.</span></span>

### <span data-ttu-id="94095-115">2. példa: Hálózati felület hozzáadása meglévő virtuális géphez</span><span class="sxs-lookup"><span data-stu-id="94095-115">Example 2: Add a network interface to an existing virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> Add-AzVMNetworkInterface -VM $VirtualMachine -Id "/subscriptions/46fc8ea4-2de6-4179-8ab1-365da4121af4/resourceGroups/contoso/providers/Microsoft.Network/networkInterfaces/sshNIC"
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="94095-116">Az első parancs a VirtualMachine07 nevű virtuális gépet kapja meg **a Get-AzVM parancsmag** használatával.</span><span class="sxs-lookup"><span data-stu-id="94095-116">The first command gets the virtual machine named VirtualMachine07 by using the **Get-AzVM** cmdlet.</span></span>
<span data-ttu-id="94095-117">A parancs a virtuális gépet a $VirtualMachine tárolja.</span><span class="sxs-lookup"><span data-stu-id="94095-117">The command stores the virtual machine in the $VirtualMachine variable.</span></span>
<span data-ttu-id="94095-118">A második parancs hozzáad egy hálózati felületet a $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="94095-118">The second command adds a network interface to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="94095-119">Az utolsó parancs frissíti a ResourceGroup11-ben $VirtualMachine virtuális gép állapotát.</span><span class="sxs-lookup"><span data-stu-id="94095-119">The final command updates the state of the virtual machine stored in $VirtualMachine in ResourceGroup11.</span></span>

## <span data-ttu-id="94095-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="94095-120">PARAMETERS</span></span>

### <span data-ttu-id="94095-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94095-121">-DefaultProfile</span></span>
<span data-ttu-id="94095-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="94095-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="94095-123">-Id</span><span class="sxs-lookup"><span data-stu-id="94095-123">-Id</span></span>
<span data-ttu-id="94095-124">Egy virtuális géphez hozzáadható hálózati felület azonosítója.</span><span class="sxs-lookup"><span data-stu-id="94095-124">Specifies the ID of a network interface to add to a virtual machine.</span></span>
<span data-ttu-id="94095-125">A [Get-AzNetworkInterface](/powershell/module/az.network/get-aznetworkinterface) parancsmag használatával hálózati felületet szerezhet be.</span><span class="sxs-lookup"><span data-stu-id="94095-125">You can use the [Get-AzNetworkInterface](/powershell/module/az.network/get-aznetworkinterface) cmdlet to obtain a network interface.</span></span>

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

### <span data-ttu-id="94095-126">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="94095-126">-NetworkInterface</span></span>
<span data-ttu-id="94095-127">A hálózati felületet határozza meg.</span><span class="sxs-lookup"><span data-stu-id="94095-127">Specifies the network interface.</span></span>

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

### <span data-ttu-id="94095-128">-Primary</span><span class="sxs-lookup"><span data-stu-id="94095-128">-Primary</span></span>
<span data-ttu-id="94095-129">Azt jelzi, hogy ez a parancsmag hozzáadja a hálózati felületet elsődleges felületként.</span><span class="sxs-lookup"><span data-stu-id="94095-129">Indicates that this cmdlet adds the network interface as the primary interface.</span></span>

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

### <span data-ttu-id="94095-130">-VM</span><span class="sxs-lookup"><span data-stu-id="94095-130">-VM</span></span>
<span data-ttu-id="94095-131">Megadja azt a helyi virtuális gépobjektumot, amelyhez hálózati felületet szeretne hozzáadni.</span><span class="sxs-lookup"><span data-stu-id="94095-131">Specifies a local virtual machine object to which to add a network interface.</span></span>
<span data-ttu-id="94095-132">Virtuális gép létrehozásához használja a **New-AzVMConfig** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="94095-132">To create a virtual machine, use the **New-AzVMConfig** cmdlet.</span></span>
<span data-ttu-id="94095-133">Meglévő virtuális gép beszerzéséhez használja a **Get-AzVM** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="94095-133">To obtain an existing virtual machine, use the **Get-AzVM** cmdlet.</span></span>

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

### <span data-ttu-id="94095-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94095-134">CommonParameters</span></span>
<span data-ttu-id="94095-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94095-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94095-136">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="94095-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94095-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="94095-137">INPUTS</span></span>

### <span data-ttu-id="94095-138">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="94095-138">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="94095-139">System.String</span><span class="sxs-lookup"><span data-stu-id="94095-139">System.String</span></span>

### <span data-ttu-id="94095-140">System.Collections.Generic.List'1[[Microsoft.Azure.Management.Internal.Network.Common.INetworkInterfaceReference, Microsoft.Azure.PowerShell.Clients.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="94095-140">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Internal.Network.Common.INetworkInterfaceReference, Microsoft.Azure.PowerShell.Clients.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="94095-141">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="94095-141">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="94095-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="94095-142">OUTPUTS</span></span>

### <span data-ttu-id="94095-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="94095-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="94095-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="94095-144">NOTES</span></span>

## <span data-ttu-id="94095-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="94095-145">RELATED LINKS</span></span>

[<span data-ttu-id="94095-146">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="94095-146">New-AzVMConfig</span></span>](./New-AzVMConfig.md)

[<span data-ttu-id="94095-147">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="94095-147">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="94095-148">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="94095-148">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)
