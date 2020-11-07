---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: BF80D456-DAB1-4B51-B50F-A75C2C66A472
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvmnetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmVMNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmVMNetworkInterface.md
ms.openlocfilehash: a7e84ee56e09e2008d76ccd9177d320be7ada96a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93673169"
---
# <span data-ttu-id="eab6e-101">Add-AzureRmVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="eab6e-101">Add-AzureRmVMNetworkInterface</span></span>

## <span data-ttu-id="eab6e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="eab6e-102">SYNOPSIS</span></span>
<span data-ttu-id="eab6e-103">Hálózati felületet ad hozzá egy virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="eab6e-103">Adds a network interface to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eab6e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="eab6e-104">SYNTAX</span></span>

### <span data-ttu-id="eab6e-105">GetNicFromNicId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="eab6e-105">GetNicFromNicId (Default)</span></span>
```
Add-AzureRmVMNetworkInterface [-VM] <PSVirtualMachine> [-Id] <String> [-Primary]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eab6e-106">GetNicFromNicObject</span><span class="sxs-lookup"><span data-stu-id="eab6e-106">GetNicFromNicObject</span></span>
```
Add-AzureRmVMNetworkInterface [-VM] <PSVirtualMachine>
 [-NetworkInterface] <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.INetworkInterfaceReference]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eab6e-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="eab6e-107">DESCRIPTION</span></span>
<span data-ttu-id="eab6e-108">A **Add-AzureRmVMNetworkInterface** parancsmag hálózati felületet ad hozzá egy virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="eab6e-108">The **Add-AzureRmVMNetworkInterface** cmdlet adds a network interface to a virtual machine.</span></span>
<span data-ttu-id="eab6e-109">Hozzáadhat egy felületet a virtuális gép létrehozásakor, vagy hozzáadhat egyet egy meglévő virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="eab6e-109">You can add an interface when you create a virtual machine or add one to an existing virtual machine.</span></span>

## <span data-ttu-id="eab6e-110">Példák</span><span class="sxs-lookup"><span data-stu-id="eab6e-110">EXAMPLES</span></span>

### <span data-ttu-id="eab6e-111">1. példa: hálózati felület felvétele új virtuális gépre</span><span class="sxs-lookup"><span data-stu-id="eab6e-111">Example 1: Add a network interface to a new virtual machine</span></span>
```
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> Add-AzureRmVMNetworkInterface -VM $VirtualMachine -Id "/subscriptions/46fc8ea4-2de6-4179-8ab1-365da4121af4/resourceGroups/contoso/providers/Microsoft.Network/networkInterfaces/sshNIC"
```

<span data-ttu-id="eab6e-112">Az első parancs létrehoz egy virtuálisgép-objektumot, majd a $VirtualMachine változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="eab6e-112">The first command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="eab6e-113">A parancs nevet és méretet rendel a virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="eab6e-113">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="eab6e-114">A második parancs hozzáadja a hálózati felületet a $VirtualMachineban tárolt virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="eab6e-114">The second command adds a network interface to the virtual machine stored in $VirtualMachine.</span></span>

### <span data-ttu-id="eab6e-115">2. példa: hálózati felület felvétele meglévő virtuális géphez</span><span class="sxs-lookup"><span data-stu-id="eab6e-115">Example 2: Add a network interface to an existing virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> Add-AzureRmVMNetworkInterface -VM $VirtualMachine -Id "/subscriptions/46fc8ea4-2de6-4179-8ab1-365da4121af4/resourceGroups/contoso/providers/Microsoft.Network/networkInterfaces/sshNIC"
PS C:\> Update-AzureRmVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="eab6e-116">Az első parancs a **Get-AzureRmVM** parancsmag használatával kapja meg a VirtualMachine07 nevű virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="eab6e-116">The first command gets the virtual machine named VirtualMachine07 by using the **Get-AzureRmVM** cmdlet.</span></span>
<span data-ttu-id="eab6e-117">A parancs a virtuális gépet a $VirtualMachine változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="eab6e-117">The command stores the virtual machine in the $VirtualMachine variable.</span></span>
<span data-ttu-id="eab6e-118">A második parancs hozzáadja a hálózati felületet a $VirtualMachineban tárolt virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="eab6e-118">The second command adds a network interface to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="eab6e-119">A végleges parancs frissíti a $VirtualMachineban tárolt virtuális gép állapotát a ResourceGroup11-ban.</span><span class="sxs-lookup"><span data-stu-id="eab6e-119">The final command updates the state of the virtual machine stored in $VirtualMachine in ResourceGroup11.</span></span>

## <span data-ttu-id="eab6e-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="eab6e-120">PARAMETERS</span></span>

### <span data-ttu-id="eab6e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eab6e-121">-DefaultProfile</span></span>
<span data-ttu-id="eab6e-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="eab6e-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eab6e-123">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="eab6e-123">-Id</span></span>
<span data-ttu-id="eab6e-124">A virtuális géphez hozzáadni kívánt hálózati interfész AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="eab6e-124">Specifies the ID of a network interface to add to a virtual machine.</span></span>
<span data-ttu-id="eab6e-125">A [Get-AzureRmNetworkInterface](/powershell/module/azurerm.network/get-azurermnetworkinterface) parancsmaggal hálózati felületet lehet beolvasni.</span><span class="sxs-lookup"><span data-stu-id="eab6e-125">You can use the [Get-AzureRmNetworkInterface](/powershell/module/azurerm.network/get-azurermnetworkinterface) cmdlet to obtain a network interface.</span></span>

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

### <span data-ttu-id="eab6e-126">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="eab6e-126">-NetworkInterface</span></span>
<span data-ttu-id="eab6e-127">A hálózati felületet adja meg.</span><span class="sxs-lookup"><span data-stu-id="eab6e-127">Specifies the network interface.</span></span>

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

### <span data-ttu-id="eab6e-128">-Elsődleges</span><span class="sxs-lookup"><span data-stu-id="eab6e-128">-Primary</span></span>
<span data-ttu-id="eab6e-129">Jelzi, hogy ez a parancsmag hozzáadja a hálózati felületet az elsődleges felülethez.</span><span class="sxs-lookup"><span data-stu-id="eab6e-129">Indicates that this cmdlet adds the network interface as the primary interface.</span></span>

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

### <span data-ttu-id="eab6e-130">-VM</span><span class="sxs-lookup"><span data-stu-id="eab6e-130">-VM</span></span>
<span data-ttu-id="eab6e-131">Annak a helyi virtuális gép-objektumnak a megadása, amelyhez hálózati felületet szeretne adni.</span><span class="sxs-lookup"><span data-stu-id="eab6e-131">Specifies a local virtual machine object to which to add a network interface.</span></span>
<span data-ttu-id="eab6e-132">Virtuális gép létrehozásához használja a **New-AzureRmVMConfig** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="eab6e-132">To create a virtual machine, use the **New-AzureRmVMConfig** cmdlet.</span></span>
<span data-ttu-id="eab6e-133">Ha egy meglévő virtuális gépet szeretne beolvasni, használja a **Get-AzureRmVM** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="eab6e-133">To obtain an existing virtual machine, use the **Get-AzureRmVM** cmdlet.</span></span>

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

### <span data-ttu-id="eab6e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eab6e-134">CommonParameters</span></span>
<span data-ttu-id="eab6e-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="eab6e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eab6e-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eab6e-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eab6e-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="eab6e-137">INPUTS</span></span>

### <span data-ttu-id="eab6e-138">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="eab6e-138">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="eab6e-139">System. String</span><span class="sxs-lookup"><span data-stu-id="eab6e-139">System.String</span></span>

### <span data-ttu-id="eab6e-140">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Management. internal. Network. Common. INetworkInterfaceReference, Microsoft. Azure. Common. Network, Version = 1.0.0.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="eab6e-140">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Internal.Network.Common.INetworkInterfaceReference, Microsoft.Azure.Commands.Common.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="eab6e-141">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="eab6e-141">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="eab6e-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="eab6e-142">OUTPUTS</span></span>

### <span data-ttu-id="eab6e-143">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="eab6e-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="eab6e-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="eab6e-144">NOTES</span></span>

## <span data-ttu-id="eab6e-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="eab6e-145">RELATED LINKS</span></span>

[<span data-ttu-id="eab6e-146">Új – AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="eab6e-146">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)

[<span data-ttu-id="eab6e-147">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="eab6e-147">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="eab6e-148">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="eab6e-148">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)
