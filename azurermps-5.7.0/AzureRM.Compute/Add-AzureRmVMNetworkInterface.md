---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: BF80D456-DAB1-4B51-B50F-A75C2C66A472
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVMNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVMNetworkInterface.md
ms.openlocfilehash: 11d2f8226e2cabba5fb431054a0e6c822e33af6e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495462"
---
# <span data-ttu-id="70981-101">Add-AzureRmVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="70981-101">Add-AzureRmVMNetworkInterface</span></span>

## <span data-ttu-id="70981-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="70981-102">SYNOPSIS</span></span>
<span data-ttu-id="70981-103">Hálózati felületet ad hozzá egy virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="70981-103">Adds a network interface to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="70981-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="70981-104">SYNTAX</span></span>

### <span data-ttu-id="70981-105">GetNicFromNicId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="70981-105">GetNicFromNicId (Default)</span></span>
```
Add-AzureRmVMNetworkInterface [-VM] <PSVirtualMachine> [-Id] <String> [-Primary] [<CommonParameters>]
```

### <span data-ttu-id="70981-106">GetNicFromNicObject</span><span class="sxs-lookup"><span data-stu-id="70981-106">GetNicFromNicObject</span></span>
```
Add-AzureRmVMNetworkInterface [-VM] <PSVirtualMachine>
 [-NetworkInterface] <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkInterface]>
 [<CommonParameters>]
```

## <span data-ttu-id="70981-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="70981-107">DESCRIPTION</span></span>
<span data-ttu-id="70981-108">A **Add-AzureRmVMNetworkInterface** parancsmag hálózati felületet ad hozzá egy virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="70981-108">The **Add-AzureRmVMNetworkInterface** cmdlet adds a network interface to a virtual machine.</span></span>
<span data-ttu-id="70981-109">Hozzáadhat egy felületet a virtuális gép létrehozásakor, vagy hozzáadhat egyet egy meglévő virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="70981-109">You can add an interface when you create a virtual machine or add one to an existing virtual machine.</span></span>

## <span data-ttu-id="70981-110">Példák</span><span class="sxs-lookup"><span data-stu-id="70981-110">EXAMPLES</span></span>

### <span data-ttu-id="70981-111">1. példa: hálózati felület felvétele új virtuális gépre</span><span class="sxs-lookup"><span data-stu-id="70981-111">Example 1: Add a network interface to a new virtual machine</span></span>
```
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" 
PS C:\> Add-AzureRmVMNetworkInterface -VM $VirtualMachine -Id "/subscriptions/46fc8ea4-2de6-4179-8ab1-365da4121af4/resourceGroups/contoso/providers/Microsoft.Network/networkInterfaces/sshNIC"
```

<span data-ttu-id="70981-112">Az első parancs létrehoz egy virtuálisgép-objektumot, majd a $VirtualMachine változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="70981-112">The first command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="70981-113">A parancs nevet és méretet rendel a virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="70981-113">The command assigns a name and size to the virtual machine.</span></span>

<span data-ttu-id="70981-114">A második parancs hozzáadja a hálózati felületet a $VirtualMachineban tárolt virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="70981-114">The second command adds a network interface to the virtual machine stored in $VirtualMachine.</span></span>

### <span data-ttu-id="70981-115">2. példa: hálózati felület felvétele meglévő virtuális géphez</span><span class="sxs-lookup"><span data-stu-id="70981-115">Example 2: Add a network interface to an existing virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> Add-AzureRmVMNetworkInterface -VM $VirtualMachine -Id "/subscriptions/46fc8ea4-2de6-4179-8ab1-365da4121af4/resourceGroups/contoso/providers/Microsoft.Network/networkInterfaces/sshNIC"
PS C:\> Update-AzureRmVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="70981-116">Az első parancs a **Get-AzureRmVM** parancsmag használatával kapja meg a VirtualMachine07 nevű virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="70981-116">The first command gets the virtual machine named VirtualMachine07 by using the **Get-AzureRmVM** cmdlet.</span></span>
<span data-ttu-id="70981-117">A parancs a virtuális gépet a $VirtualMachine változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="70981-117">The command stores the virtual machine in the $VirtualMachine variable.</span></span>

<span data-ttu-id="70981-118">A második parancs hozzáadja a hálózati felületet a $VirtualMachineban tárolt virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="70981-118">The second command adds a network interface to the virtual machine stored in $VirtualMachine.</span></span>

<span data-ttu-id="70981-119">A végleges parancs frissíti a $VirtualMachineban tárolt virtuális gép állapotát a ResourceGroup11-ban.</span><span class="sxs-lookup"><span data-stu-id="70981-119">The final command updates the state of the virtual machine stored in $VirtualMachine in ResourceGroup11.</span></span>

## <span data-ttu-id="70981-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="70981-120">PARAMETERS</span></span>

### <span data-ttu-id="70981-121">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="70981-121">-Id</span></span>
<span data-ttu-id="70981-122">A virtuális géphez hozzáadni kívánt hálózati interfész AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="70981-122">Specifies the ID of a network interface to add to a virtual machine.</span></span>
<span data-ttu-id="70981-123">A [Get-AzureRmNetworkInterface](/powershell/module/azurerm.network/get-azurermnetworkinterface) parancsmaggal hálózati felületet lehet beolvasni.</span><span class="sxs-lookup"><span data-stu-id="70981-123">You can use the [Get-AzureRmNetworkInterface](/powershell/module/azurerm.network/get-azurermnetworkinterface) cmdlet to obtain a network interface.</span></span>

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

### <span data-ttu-id="70981-124">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="70981-124">-NetworkInterface</span></span>
<span data-ttu-id="70981-125">A hálózati felületet adja meg.</span><span class="sxs-lookup"><span data-stu-id="70981-125">Specifies the network interface.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkInterface]
Parameter Sets: GetNicFromNicObject
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="70981-126">-Elsődleges</span><span class="sxs-lookup"><span data-stu-id="70981-126">-Primary</span></span>
<span data-ttu-id="70981-127">Jelzi, hogy ez a parancsmag hozzáadja a hálózati felületet az elsődleges felülethez.</span><span class="sxs-lookup"><span data-stu-id="70981-127">Indicates that this cmdlet adds the network interface as the primary interface.</span></span>

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

### <span data-ttu-id="70981-128">-VM</span><span class="sxs-lookup"><span data-stu-id="70981-128">-VM</span></span>
<span data-ttu-id="70981-129">Annak a helyi virtuális gép-objektumnak a megadása, amelyhez hálózati felületet szeretne adni.</span><span class="sxs-lookup"><span data-stu-id="70981-129">Specifies a local virtual machine object to which to add a network interface.</span></span>
<span data-ttu-id="70981-130">Virtuális gép létrehozásához használja a **New-AzureRmVMConfig** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="70981-130">To create a virtual machine, use the **New-AzureRmVMConfig** cmdlet.</span></span>
<span data-ttu-id="70981-131">Ha egy meglévő virtuális gépet szeretne beolvasni, használja a **Get-AzureRmVM** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="70981-131">To obtain an existing virtual machine, use the **Get-AzureRmVM** cmdlet.</span></span>

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

### <span data-ttu-id="70981-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70981-132">CommonParameters</span></span>
<span data-ttu-id="70981-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="70981-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70981-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70981-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70981-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="70981-135">INPUTS</span></span>

### <span data-ttu-id="70981-136">Nincs</span><span class="sxs-lookup"><span data-stu-id="70981-136">None</span></span>
<span data-ttu-id="70981-137">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="70981-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="70981-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="70981-138">OUTPUTS</span></span>

## <span data-ttu-id="70981-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="70981-139">NOTES</span></span>

## <span data-ttu-id="70981-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="70981-140">RELATED LINKS</span></span>

[<span data-ttu-id="70981-141">Új – AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="70981-141">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)

[<span data-ttu-id="70981-142">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="70981-142">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="70981-143">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="70981-143">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)
