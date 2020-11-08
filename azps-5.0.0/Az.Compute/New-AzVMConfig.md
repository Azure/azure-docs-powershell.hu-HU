---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 1BECAC91-BB43-46EB-B2C9-C965C6FBC831
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMConfig.md
ms.openlocfilehash: 8c20a6be76f77a74082090d1386054a23b9b9ea0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194116"
---
# <span data-ttu-id="31f26-101">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="31f26-101">New-AzVMConfig</span></span>

## <span data-ttu-id="31f26-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="31f26-102">SYNOPSIS</span></span>
<span data-ttu-id="31f26-103">Konfigurálható virtuálisgép-objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="31f26-103">Creates a configurable virtual machine object.</span></span>

## <span data-ttu-id="31f26-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="31f26-104">SYNTAX</span></span>

### <span data-ttu-id="31f26-105">DefaultParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="31f26-105">DefaultParameterSet (Default)</span></span>
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>] [[-LicenseType] <String>]
 [-Zone <String[]>] [-ProximityPlacementGroupId <String>] [-HostId <String>] [-VmssId <String>]
 [-MaxPrice <Double>] [-EvictionPolicy <String>] [-Priority <String>] [-Tags <Hashtable>] [-EnableUltraSSD] 
 [-EncryptionAtHost] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="31f26-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="31f26-106">ExplicitIdentityParameterSet</span></span>
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>] [[-LicenseType] <String>]
 [-IdentityType] <ResourceIdentityType> [-IdentityId <String[]>] [-Zone <String[]>]
 [-ProximityPlacementGroupId <String>] [-HostId <String>] [-VmssId <String>] [-MaxPrice <Double>]
 [-EvictionPolicy <String>] [-Priority <String>] [-Tags <Hashtable>] [-EnableUltraSSD]
 [-EncryptionAtHost] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="31f26-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="31f26-107">DESCRIPTION</span></span>
<span data-ttu-id="31f26-108">A **New-AzVMConfig** parancsmag létrehoz egy konfigurálható helyi virtuálisgép-objektumot az Azure-hoz.</span><span class="sxs-lookup"><span data-stu-id="31f26-108">The **New-AzVMConfig** cmdlet creates a configurable local virtual machine object for Azure.</span></span>
<span data-ttu-id="31f26-109">Az egyéb parancsmagok segítségével konfigurálhatók a virtuálisgép-objektumok, például a set-AzVMOperatingSystem, a set-AzVMSourceImage, a Add-AzVMNetworkInterface és a set-AzVMOSDisk.</span><span class="sxs-lookup"><span data-stu-id="31f26-109">Other cmdlets can be used to configure a virtual machine object, such as Set-AzVMOperatingSystem, Set-AzVMSourceImage, Add-AzVMNetworkInterface, and Set-AzVMOSDisk.</span></span>

## <span data-ttu-id="31f26-110">Példák</span><span class="sxs-lookup"><span data-stu-id="31f26-110">EXAMPLES</span></span>

### <span data-ttu-id="31f26-111">Példa 1: virtuális gép objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="31f26-111">Example 1: Create a virtual machine object</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
```

<span data-ttu-id="31f26-112">Az első parancs beolvassa a AvailabilitySet03 nevű ResourceGroup11 nevű erőforráscsoport elérhetőségi készletét, majd a $AvailabilitySet változóban tárolja az objektumot.</span><span class="sxs-lookup"><span data-stu-id="31f26-112">The first command gets the availability set named AvailabilitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="31f26-113">A második parancs létrehoz egy Virtual Machine-objektumot, majd a $VirtualMachine változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="31f26-113">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="31f26-114">A parancs nevet és méretet rendel a virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="31f26-114">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="31f26-115">A virtuális gép a $AvailabilitySetban tárolt elérhetőségi készlethez tartozik.</span><span class="sxs-lookup"><span data-stu-id="31f26-115">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

## <span data-ttu-id="31f26-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="31f26-116">PARAMETERS</span></span>

### <span data-ttu-id="31f26-117">-AvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="31f26-117">-AvailabilitySetId</span></span>
<span data-ttu-id="31f26-118">A rendelkezésre álló készlet AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="31f26-118">Specifies the ID of an availability set.</span></span>
<span data-ttu-id="31f26-119">Az elérhetőségi készlet objektum beolvasásához használja az Get-AzAvailabilitySet parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="31f26-119">To obtain an availability set object, use the Get-AzAvailabilitySet cmdlet.</span></span>
<span data-ttu-id="31f26-120">Az elérhetőségi készlet objektum egy azonosító tulajdonságot tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="31f26-120">The availability set object contains an ID property.</span></span> <br>
<span data-ttu-id="31f26-121">Az elérhetőségi halmazban meghatározott virtuális gépek a különböző csomópontokra vannak kiosztva a teljes elérhetőség érdekében.</span><span class="sxs-lookup"><span data-stu-id="31f26-121">Virtual machines specified in the same availability set are allocated to different nodes to maximize availability.</span></span> <br>
<span data-ttu-id="31f26-122">Az elérhetőségi készletekről a [virtuális gépek elérhetőségének kezelése](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-manage-availability?toc=%2fazure%2fvirtual-machines%2fwindows%2ftoc.json)című témakörben olvashat bővebben.</span><span class="sxs-lookup"><span data-stu-id="31f26-122">For more information about availability sets, see [Manage the availability of virtual machines](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-manage-availability?toc=%2fazure%2fvirtual-machines%2fwindows%2ftoc.json).</span></span> <br>
<span data-ttu-id="31f26-123">Az Azure tervezett karbantartásáról további információt a [virtuális gépek tervezett karbantartása az Azure-ban](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-planned-maintenance?toc=%2fazure%2fvirtual-machines%2fwindows%2ftoc.json) című témakörben találhat.</span><span class="sxs-lookup"><span data-stu-id="31f26-123">For more information on Azure planned maintenance, see [Planned maintenance for virtual machines in Azure](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-planned-maintenance?toc=%2fazure%2fvirtual-machines%2fwindows%2ftoc.json)</span></span> <br>
<span data-ttu-id="31f26-124">A VM jelenleg csak a létrehozási időpontban vehető fel az elérhetőségi készletbe.</span><span class="sxs-lookup"><span data-stu-id="31f26-124">Currently, a VM can only be added to availability set at creation time.</span></span> <span data-ttu-id="31f26-125">Az elérhetőségi készlet, amelyhez a virtuális gépet felveszik, ugyanabba a csoportba tartozó erőforrás legyen, mint az elérhetőségi készlet erőforrás.</span><span class="sxs-lookup"><span data-stu-id="31f26-125">The availability set to which the VM is being added should be under the same resource group as the availability set resource.</span></span> <span data-ttu-id="31f26-126">Egy meglévő VM nem vehető fel az elérhetőségi halmazba.</span><span class="sxs-lookup"><span data-stu-id="31f26-126">An existing VM cannot be added to an availability set.</span></span> <br>
<span data-ttu-id="31f26-127">Ez a tulajdonság nem létezhet a nem null tulajdonságokkal együtt. virtualMachineScaleSet hivatkozás.</span><span class="sxs-lookup"><span data-stu-id="31f26-127">This property cannot exist along with a non-null properties.virtualMachineScaleSet reference.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31f26-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31f26-128">-DefaultProfile</span></span>
<span data-ttu-id="31f26-129">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="31f26-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="31f26-130">-EnableUltraSSD</span><span class="sxs-lookup"><span data-stu-id="31f26-130">-EnableUltraSSD</span></span>
<span data-ttu-id="31f26-131">Lehetővé teszi, hogy egy vagy több felügyelt adatlemez legyen a VM-UltraSSD_LRS tárterület-fiók típusával.</span><span class="sxs-lookup"><span data-stu-id="31f26-131">Enables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the VM.</span></span>
<span data-ttu-id="31f26-132">A felügyelt lemezek tároló fiók típusú UltraSSD_LRS csak akkor adhatók hozzá a virtuális géphez, ha a tulajdonság engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="31f26-132">Managed disks with storage account type UltraSSD_LRS can be added to a virtual machine only if this property is enabled.</span></span>


```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31f26-133">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="31f26-133">-EvictionPolicy</span></span>
<span data-ttu-id="31f26-134">Az Azure spot Virtual Machine kilakoltatási házirendje.</span><span class="sxs-lookup"><span data-stu-id="31f26-134">The eviction policy for the Azure Spot virtual machine.</span></span>  <span data-ttu-id="31f26-135">A támogatott értékek "kifoglalás" és "Törlés".</span><span class="sxs-lookup"><span data-stu-id="31f26-135">Supported values are 'Deallocate' and 'Delete'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31f26-136">-Állomásazonosító</span><span class="sxs-lookup"><span data-stu-id="31f26-136">-HostId</span></span>
<span data-ttu-id="31f26-137">Az állomás azonosítója</span><span class="sxs-lookup"><span data-stu-id="31f26-137">The Id of Host</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31f26-138">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="31f26-138">-IdentityId</span></span>
<span data-ttu-id="31f26-139">A virtuálisgép-készlethez társított felhasználói identitások listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="31f26-139">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="31f26-140">A felhasználói identitás hivatkozásai az űrlapon az "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}" típusú erőforrás-azonosítók lesznek.</span><span class="sxs-lookup"><span data-stu-id="31f26-140">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

```yaml
Type: System.String[]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31f26-141">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="31f26-141">-IdentityType</span></span>
<span data-ttu-id="31f26-142">A virtuális gép identitása, ha be van állítva.</span><span class="sxs-lookup"><span data-stu-id="31f26-142">The identity of the virtual machine, if configured.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:
Accepted values: SystemAssigned, UserAssigned, SystemAssignedUserAssigned, None

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31f26-143">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="31f26-143">-LicenseType</span></span>
<span data-ttu-id="31f26-144">A licenc típusa, amely a saját licenc-forgatókönyv készítéséhez szükséges.</span><span class="sxs-lookup"><span data-stu-id="31f26-144">The license type, which is for bringing your own license scenario.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31f26-145">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="31f26-145">-MaxPrice</span></span>
<span data-ttu-id="31f26-146">Itt adhatja meg, hogy az alacsony prioritású VM/VMSS milyen maximális árat fizessen.</span><span class="sxs-lookup"><span data-stu-id="31f26-146">Specifies the maximum price you are willing to pay for a low priority VM/VMSS.</span></span> <span data-ttu-id="31f26-147">Ez az ár amerikai dollárban van.</span><span class="sxs-lookup"><span data-stu-id="31f26-147">This price is in US Dollars.</span></span> <span data-ttu-id="31f26-148">Ezt az árat a program összehasonlítja a VM-méret jelenlegi alacsony prioritási árával.</span><span class="sxs-lookup"><span data-stu-id="31f26-148">This price will be compared with the current low priority price for the VM size.</span></span> <span data-ttu-id="31f26-149">Az árakat az alacsony prioritású VM/VMSS létrehozásának/frissítésének időpontjában is összehasonlították, és a művelet csak akkor fog sikerülni, ha a maxPrice nagyobb, mint a jelenlegi alacsony prioritású ár.</span><span class="sxs-lookup"><span data-stu-id="31f26-149">Also, the prices are compared at the time of create/update of low priority VM/VMSS and the operation will only succeed if the maxPrice is greater than the current low priority price.</span></span> <span data-ttu-id="31f26-150">A maxPrice a VM/VMSS létrehozása után is az alacsony prioritású VM/VMSS eltávolítására használható, ha a jelenlegi alacsony prioritású ár túllépi a maxPrice.</span><span class="sxs-lookup"><span data-stu-id="31f26-150">The maxPrice will also be used for evicting a low priority VM/VMSS if the current low priority price goes beyond the maxPrice after creation of VM/VMSS.</span></span> <span data-ttu-id="31f26-151">Lehetséges értékek: bármely nullánál nagyobb decimális érték.</span><span class="sxs-lookup"><span data-stu-id="31f26-151">Possible values are: any decimal value greater than zero.</span></span> <span data-ttu-id="31f26-152">Példa: 0,01538.</span><span class="sxs-lookup"><span data-stu-id="31f26-152">Example: 0.01538.</span></span>  <span data-ttu-id="31f26-153">-1 – azt jelzi, hogy az alacsony prioritású VM/VMSS nem szabad az árak miatt kizárni.</span><span class="sxs-lookup"><span data-stu-id="31f26-153">-1 indicates that the low priority VM/VMSS should not be evicted for price reasons.</span></span> <span data-ttu-id="31f26-154">Az alapértelmezett Max ár is-1, ha az nem az Ön által megadott.</span><span class="sxs-lookup"><span data-stu-id="31f26-154">Also, the default max price is -1 if it is not provided by you.</span></span>

```yaml
Type: System.Double
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31f26-155">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="31f26-155">-EncryptionAtHost</span></span>
<span data-ttu-id="31f26-156">A EncryptionAtHost tulajdonságot a felhasználó használhatja fel a virtuális gép vagy a virtuálisgép-készlet adatkészlet-titkosításának engedélyezéséhez vagy letiltásához.</span><span class="sxs-lookup"><span data-stu-id="31f26-156">EncryptionAtHost property can be used by user in the request to enable or disable the Host Encryption for the virtual machine or virtual machine scale set.</span></span> <span data-ttu-id="31f26-157">Ezzel engedélyezi az összes lemez titkosítását, például az erőforrás/Temp diskt az állomáson.</span><span class="sxs-lookup"><span data-stu-id="31f26-157">This will enable the encryption for all the disks including Resource/Temp disk at host itself.</span></span> <span data-ttu-id="31f26-158">Alapértelmezés: az állomáson a titkosítás le lesz tiltva, kivéve ha a tulajdonság értéke igaz az erőforrás esetében.</span><span class="sxs-lookup"><span data-stu-id="31f26-158">Default: The Encryption at host will be disabled unless this property is set to true for the resource.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31f26-159">– Prioritás</span><span class="sxs-lookup"><span data-stu-id="31f26-159">-Priority</span></span>
<span data-ttu-id="31f26-160">A virtuális gép prioritása.</span><span class="sxs-lookup"><span data-stu-id="31f26-160">The priority for the virtual machine.</span></span>  <span data-ttu-id="31f26-161">Csak a támogatott értékek "normál", "spot" és "Low".</span><span class="sxs-lookup"><span data-stu-id="31f26-161">Only supported values are 'Regular', 'Spot' and 'Low'.</span></span>
<span data-ttu-id="31f26-162">"Normál": a normál virtuális gép.</span><span class="sxs-lookup"><span data-stu-id="31f26-162">'Regular' is for regular virtual machine.</span></span>
<span data-ttu-id="31f26-163">A "spot" a direkt virtuális gép.</span><span class="sxs-lookup"><span data-stu-id="31f26-163">'Spot' is for spot virtual machine.</span></span>
<span data-ttu-id="31f26-164">Az "alacsony" a direkt virtuális gép is, de a helyére "spot" lép.</span><span class="sxs-lookup"><span data-stu-id="31f26-164">'Low' is also for spot virtual machine but is replaced by 'Spot'.</span></span> <span data-ttu-id="31f26-165">Kérjük, hogy az "alacsony" helyett a "spot" értéket használja.</span><span class="sxs-lookup"><span data-stu-id="31f26-165">Please use 'Spot' instead of 'Low'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31f26-166">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="31f26-166">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="31f26-167">Az ezzel a virtuális géppel használható közelségi hely csoport erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="31f26-167">The resource id of the Proximity Placement Group to use with this virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31f26-168">-Címkék</span><span class="sxs-lookup"><span data-stu-id="31f26-168">-Tags</span></span>
<span data-ttu-id="31f26-169">Az erőforráshoz társított címkék.</span><span class="sxs-lookup"><span data-stu-id="31f26-169">The tags attached to the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31f26-170">-VMName</span><span class="sxs-lookup"><span data-stu-id="31f26-170">-VMName</span></span>
<span data-ttu-id="31f26-171">A virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="31f26-171">Specifies a name for the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31f26-172">-VMSize</span><span class="sxs-lookup"><span data-stu-id="31f26-172">-VMSize</span></span>
<span data-ttu-id="31f26-173">A virtuális gép méretét adja meg.</span><span class="sxs-lookup"><span data-stu-id="31f26-173">Specifies the size for the virtual machine.</span></span>

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

### <span data-ttu-id="31f26-174">-VmssId</span><span class="sxs-lookup"><span data-stu-id="31f26-174">-VmssId</span></span>
<span data-ttu-id="31f26-175">A virtuális gép méretarányának azonosítója</span><span class="sxs-lookup"><span data-stu-id="31f26-175">The Id of virtual machine scale set</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31f26-176">-Zone (zóna)</span><span class="sxs-lookup"><span data-stu-id="31f26-176">-Zone</span></span>
<span data-ttu-id="31f26-177">A virtuális gép elérhetőségi zóna listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="31f26-177">Specifies the availability zone list for the virtual machine.</span></span> <span data-ttu-id="31f26-178">A megengedett értékek a régió képességeitől függenek.</span><span class="sxs-lookup"><span data-stu-id="31f26-178">The allowed values depend on the capabilities of the region.</span></span> <span data-ttu-id="31f26-179">A megengedett értékek általában 1, 2, 3.</span><span class="sxs-lookup"><span data-stu-id="31f26-179">Allowed values will normally be 1,2,3.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31f26-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31f26-180">CommonParameters</span></span>
<span data-ttu-id="31f26-181">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="31f26-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31f26-182">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="31f26-182">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31f26-183">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="31f26-183">INPUTS</span></span>

### <span data-ttu-id="31f26-184">System. String</span><span class="sxs-lookup"><span data-stu-id="31f26-184">System.String</span></span>

### <span data-ttu-id="31f26-185">System. string []</span><span class="sxs-lookup"><span data-stu-id="31f26-185">System.String[]</span></span>

### <span data-ttu-id="31f26-186">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="31f26-186">System.Collections.Hashtable</span></span>

### <span data-ttu-id="31f26-187">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="31f26-187">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="31f26-188">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="31f26-188">OUTPUTS</span></span>

### <span data-ttu-id="31f26-189">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="31f26-189">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="31f26-190">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="31f26-190">NOTES</span></span>

## <span data-ttu-id="31f26-191">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="31f26-191">RELATED LINKS</span></span>

[<span data-ttu-id="31f26-192">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="31f26-192">Update-AzVM</span></span>](./Update-AzVM.md)

[<span data-ttu-id="31f26-193">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="31f26-193">Set-AzVMOperatingSystem</span></span>](./Set-AzVMOperatingSystem.md)

[<span data-ttu-id="31f26-194">Set-AzVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="31f26-194">Set-AzVMSourceImage</span></span>](./Set-AzVMSourceImage.md)

[<span data-ttu-id="31f26-195">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="31f26-195">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)


