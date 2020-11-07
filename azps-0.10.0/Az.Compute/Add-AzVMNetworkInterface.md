---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: BF80D456-DAB1-4B51-B50F-A75C2C66A472
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmnetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVMNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVMNetworkInterface.md
ms.openlocfilehash: aaf1162cdeeb007a680a3e9de325cbd10fadef94
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844745"
---
# <span data-ttu-id="67a3d-101">Add-AzVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="67a3d-101">Add-AzVMNetworkInterface</span></span>

## <span data-ttu-id="67a3d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="67a3d-102">SYNOPSIS</span></span>
<span data-ttu-id="67a3d-103">Hálózati felületet ad hozzá egy virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="67a3d-103">Adds a network interface to a virtual machine.</span></span>

## <span data-ttu-id="67a3d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="67a3d-104">SYNTAX</span></span>

### <span data-ttu-id="67a3d-105">GetNicFromNicId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="67a3d-105">GetNicFromNicId (Default)</span></span>
```
Add-AzVMNetworkInterface [-VM] <PSVirtualMachine> [-Id] <String> [-Primary]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="67a3d-106">GetNicFromNicObject</span><span class="sxs-lookup"><span data-stu-id="67a3d-106">GetNicFromNicObject</span></span>
```
Add-AzVMNetworkInterface [-VM] <PSVirtualMachine>
 [-NetworkInterface] <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.INetworkInterfaceReference]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="67a3d-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="67a3d-107">DESCRIPTION</span></span>
<span data-ttu-id="67a3d-108">A **Add-AzVMNetworkInterface** parancsmag hálózati felületet ad hozzá egy virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="67a3d-108">The **Add-AzVMNetworkInterface** cmdlet adds a network interface to a virtual machine.</span></span>
<span data-ttu-id="67a3d-109">Hozzáadhat egy felületet a virtuális gép létrehozásakor, vagy hozzáadhat egyet egy meglévő virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="67a3d-109">You can add an interface when you create a virtual machine or add one to an existing virtual machine.</span></span>

## <span data-ttu-id="67a3d-110">Példák</span><span class="sxs-lookup"><span data-stu-id="67a3d-110">EXAMPLES</span></span>

### <span data-ttu-id="67a3d-111">1. példa: hálózati felület felvétele új virtuális gépre</span><span class="sxs-lookup"><span data-stu-id="67a3d-111">Example 1: Add a network interface to a new virtual machine</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> Add-AzVMNetworkInterface -VM $VirtualMachine -Id "/subscriptions/46fc8ea4-2de6-4179-8ab1-365da4121af4/resourceGroups/contoso/providers/Microsoft.Network/networkInterfaces/sshNIC"
```

<span data-ttu-id="67a3d-112">Az első parancs létrehoz egy virtuálisgép-objektumot, majd a $VirtualMachine változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="67a3d-112">The first command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="67a3d-113">A parancs nevet és méretet rendel a virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="67a3d-113">The command assigns a name and size to the virtual machine.</span></span>

<span data-ttu-id="67a3d-114">A második parancs hozzáadja a hálózati felületet a $VirtualMachineban tárolt virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="67a3d-114">The second command adds a network interface to the virtual machine stored in $VirtualMachine.</span></span>

### <span data-ttu-id="67a3d-115">2. példa: hálózati felület felvétele meglévő virtuális géphez</span><span class="sxs-lookup"><span data-stu-id="67a3d-115">Example 2: Add a network interface to an existing virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> Add-AzVMNetworkInterface -VM $VirtualMachine -Id "/subscriptions/46fc8ea4-2de6-4179-8ab1-365da4121af4/resourceGroups/contoso/providers/Microsoft.Network/networkInterfaces/sshNIC"
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="67a3d-116">Az első parancs a **Get-AzVM** parancsmag használatával kapja meg a VirtualMachine07 nevű virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="67a3d-116">The first command gets the virtual machine named VirtualMachine07 by using the **Get-AzVM** cmdlet.</span></span>
<span data-ttu-id="67a3d-117">A parancs a virtuális gépet a $VirtualMachine változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="67a3d-117">The command stores the virtual machine in the $VirtualMachine variable.</span></span>

<span data-ttu-id="67a3d-118">A második parancs hozzáadja a hálózati felületet a $VirtualMachineban tárolt virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="67a3d-118">The second command adds a network interface to the virtual machine stored in $VirtualMachine.</span></span>

<span data-ttu-id="67a3d-119">A végleges parancs frissíti a $VirtualMachineban tárolt virtuális gép állapotát a ResourceGroup11-ban.</span><span class="sxs-lookup"><span data-stu-id="67a3d-119">The final command updates the state of the virtual machine stored in $VirtualMachine in ResourceGroup11.</span></span>

## <span data-ttu-id="67a3d-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="67a3d-120">PARAMETERS</span></span>

### <span data-ttu-id="67a3d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67a3d-121">-DefaultProfile</span></span>
<span data-ttu-id="67a3d-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="67a3d-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67a3d-123">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="67a3d-123">-Id</span></span>
<span data-ttu-id="67a3d-124">A virtuális géphez hozzáadni kívánt hálózati interfész AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="67a3d-124">Specifies the ID of a network interface to add to a virtual machine.</span></span>
<span data-ttu-id="67a3d-125">A [Get-AzNetworkInterface](/powershell/module/azurerm.network/get-aznetworkinterface) parancsmaggal hálózati felületet lehet beolvasni.</span><span class="sxs-lookup"><span data-stu-id="67a3d-125">You can use the [Get-AzNetworkInterface](/powershell/module/azurerm.network/get-aznetworkinterface) cmdlet to obtain a network interface.</span></span>

```yaml
Type: String
Parameter Sets: GetNicFromNicId
Aliases: NicId, NetworkInterfaceId

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67a3d-126">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="67a3d-126">-NetworkInterface</span></span>
<span data-ttu-id="67a3d-127">A hálózati felületet adja meg.</span><span class="sxs-lookup"><span data-stu-id="67a3d-127">Specifies the network interface.</span></span>

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

### <span data-ttu-id="67a3d-128">-Elsődleges</span><span class="sxs-lookup"><span data-stu-id="67a3d-128">-Primary</span></span>
<span data-ttu-id="67a3d-129">Jelzi, hogy ez a parancsmag hozzáadja a hálózati felületet az elsődleges felülethez.</span><span class="sxs-lookup"><span data-stu-id="67a3d-129">Indicates that this cmdlet adds the network interface as the primary interface.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: GetNicFromNicId
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67a3d-130">-VM</span><span class="sxs-lookup"><span data-stu-id="67a3d-130">-VM</span></span>
<span data-ttu-id="67a3d-131">Annak a helyi virtuális gép-objektumnak a megadása, amelyhez hálózati felületet szeretne adni.</span><span class="sxs-lookup"><span data-stu-id="67a3d-131">Specifies a local virtual machine object to which to add a network interface.</span></span>
<span data-ttu-id="67a3d-132">Virtuális gép létrehozásához használja a **New-AzVMConfig** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="67a3d-132">To create a virtual machine, use the **New-AzVMConfig** cmdlet.</span></span>
<span data-ttu-id="67a3d-133">Ha egy meglévő virtuális gépet szeretne beolvasni, használja a **Get-AzVM** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="67a3d-133">To obtain an existing virtual machine, use the **Get-AzVM** cmdlet.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="67a3d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67a3d-134">CommonParameters</span></span>
<span data-ttu-id="67a3d-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="67a3d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67a3d-136">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67a3d-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67a3d-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="67a3d-137">INPUTS</span></span>

### <span data-ttu-id="67a3d-138">System. Collections. Generic. list ' 1 [Microsoft. Azure. commands. Network. models. PSNetworkInterface]</span><span class="sxs-lookup"><span data-stu-id="67a3d-138">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.Network.Models.PSNetworkInterface]</span></span>
<span data-ttu-id="67a3d-139">A ' NetworkInterface ' paraméter a ' System. Collections. Generic. list ' 1 [Microsoft. Azure. commands. Network. models. PSNetworkInterface] ' típus értékét veszi fel a csővezetékről.</span><span class="sxs-lookup"><span data-stu-id="67a3d-139">Parameter 'NetworkInterface' accepts value of type 'System.Collections.Generic.List\`1[Microsoft.Azure.Commands.Network.Models.PSNetworkInterface]' from the pipeline</span></span>

### <span data-ttu-id="67a3d-140">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="67a3d-140">PSVirtualMachine</span></span>
<span data-ttu-id="67a3d-141">A ' VM ' paraméter elfogadja a "PSVirtualMachine" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="67a3d-141">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="67a3d-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="67a3d-142">OUTPUTS</span></span>

### <span data-ttu-id="67a3d-143">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="67a3d-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="67a3d-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="67a3d-144">NOTES</span></span>

## <span data-ttu-id="67a3d-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="67a3d-145">RELATED LINKS</span></span>

[<span data-ttu-id="67a3d-146">Új – AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="67a3d-146">New-AzVMConfig</span></span>](./New-AzVMConfig.md)

[<span data-ttu-id="67a3d-147">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="67a3d-147">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="67a3d-148">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="67a3d-148">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)
