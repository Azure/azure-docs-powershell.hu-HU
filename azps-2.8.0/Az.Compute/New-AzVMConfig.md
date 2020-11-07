---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 1BECAC91-BB43-46EB-B2C9-C965C6FBC831
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMConfig.md
ms.openlocfilehash: 5dda2e33496e3391d55e7be20348fef681bc22b9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667356"
---
# <span data-ttu-id="e1318-101">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="e1318-101">New-AzVMConfig</span></span>

## <span data-ttu-id="e1318-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e1318-102">SYNOPSIS</span></span>
<span data-ttu-id="e1318-103">Konfigurálható virtuálisgép-objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="e1318-103">Creates a configurable virtual machine object.</span></span>

## <span data-ttu-id="e1318-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e1318-104">SYNTAX</span></span>

### <span data-ttu-id="e1318-105">DefaultParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e1318-105">DefaultParameterSet (Default)</span></span>
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>] [[-LicenseType] <String>]
 [-Zone <String[]>] [-ProximityPlacementGroupId <String>] [-HostId <String>] [-VmssId <String>]
 [-MaxPrice <Double>] [-EvictionPolicy <String>] [-Priority <String>] [-Tags <Hashtable>] [-EnableUltraSSD]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e1318-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="e1318-106">ExplicitIdentityParameterSet</span></span>
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>] [[-LicenseType] <String>]
 [-IdentityType] <ResourceIdentityType> [-IdentityId <String[]>] [-Zone <String[]>]
 [-ProximityPlacementGroupId <String>] [-HostId <String>] [-VmssId <String>] [-MaxPrice <Double>]
 [-EvictionPolicy <String>] [-Priority <String>] [-Tags <Hashtable>] [-EnableUltraSSD]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e1318-107">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="e1318-107">AssignIdentityParameterSet</span></span>
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>] [[-LicenseType] <String>]
 [-AssignIdentity] [-Zone <String[]>] [-ProximityPlacementGroupId <String>] [-HostId <String>]
 [-VmssId <String>] [-MaxPrice <Double>] [-EvictionPolicy <String>] [-Priority <String>] [-Tags <Hashtable>]
 [-EnableUltraSSD] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e1318-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="e1318-108">DESCRIPTION</span></span>
<span data-ttu-id="e1318-109">A **New-AzVMConfig** parancsmag létrehoz egy konfigurálható helyi virtuálisgép-objektumot az Azure-hoz.</span><span class="sxs-lookup"><span data-stu-id="e1318-109">The **New-AzVMConfig** cmdlet creates a configurable local virtual machine object for Azure.</span></span>
<span data-ttu-id="e1318-110">Az egyéb parancsmagok segítségével konfigurálhatók a virtuálisgép-objektumok, például a set-AzVMOperatingSystem, a set-AzVMSourceImage, a Add-AzVMNetworkInterface és a set-AzVMOSDisk.</span><span class="sxs-lookup"><span data-stu-id="e1318-110">Other cmdlets can be used to configure a virtual machine object, such as Set-AzVMOperatingSystem, Set-AzVMSourceImage, Add-AzVMNetworkInterface, and Set-AzVMOSDisk.</span></span>

## <span data-ttu-id="e1318-111">Példák</span><span class="sxs-lookup"><span data-stu-id="e1318-111">EXAMPLES</span></span>

### <span data-ttu-id="e1318-112">Példa 1: virtuális gép objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="e1318-112">Example 1: Create a virtual machine object</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
```

<span data-ttu-id="e1318-113">Az első parancs beolvassa a AvailabilitySet03 nevű ResourceGroup11 nevű erőforráscsoport elérhetőségi készletét, majd a $AvailabilitySet változóban tárolja az objektumot.</span><span class="sxs-lookup"><span data-stu-id="e1318-113">The first command gets the availability set named AvailabilitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="e1318-114">A második parancs létrehoz egy Virtual Machine-objektumot, majd a $VirtualMachine változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="e1318-114">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="e1318-115">A parancs nevet és méretet rendel a virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="e1318-115">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="e1318-116">A virtuális gép a $AvailabilitySetban tárolt elérhetőségi készlethez tartozik.</span><span class="sxs-lookup"><span data-stu-id="e1318-116">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

## <span data-ttu-id="e1318-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e1318-117">PARAMETERS</span></span>

### <span data-ttu-id="e1318-118">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="e1318-118">-AssignIdentity</span></span>
<span data-ttu-id="e1318-119">Adja meg a virtuális gép rendszerhez rendelt identitását.</span><span class="sxs-lookup"><span data-stu-id="e1318-119">Specify the system assigned identity for the virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AssignIdentityParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1318-120">-AvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="e1318-120">-AvailabilitySetId</span></span>
<span data-ttu-id="e1318-121">A rendelkezésre álló készlet AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="e1318-121">Specifies the ID of an availability set.</span></span>
<span data-ttu-id="e1318-122">Az elérhetőségi készlet objektum beolvasásához használja az Get-AzAvailabilitySet parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="e1318-122">To obtain an availability set object, use the Get-AzAvailabilitySet cmdlet.</span></span>
<span data-ttu-id="e1318-123">Az elérhetőségi készlet objektum egy azonosító tulajdonságot tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="e1318-123">The availability set object contains an ID property.</span></span>

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

### <span data-ttu-id="e1318-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1318-124">-DefaultProfile</span></span>
<span data-ttu-id="e1318-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e1318-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e1318-126">-EnableUltraSSD</span><span class="sxs-lookup"><span data-stu-id="e1318-126">-EnableUltraSSD</span></span>
<span data-ttu-id="e1318-127">Lehetővé teszi, hogy egy vagy több felügyelt adatlemez legyen a VM-UltraSSD_LRS tárterület-fiók típusával.</span><span class="sxs-lookup"><span data-stu-id="e1318-127">Enables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the VM.</span></span>
<span data-ttu-id="e1318-128">A felügyelt lemezek tároló fiók típusú UltraSSD_LRS csak akkor adhatók hozzá a virtuális géphez, ha a tulajdonság engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="e1318-128">Managed disks with storage account type UltraSSD_LRS can be added to a virtual machine only if this property is enabled.</span></span>


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

### <span data-ttu-id="e1318-129">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="e1318-129">-EvictionPolicy</span></span>
<span data-ttu-id="e1318-130">Az alacsony prioritású virtuális gép kilakoltatási irányelve.</span><span class="sxs-lookup"><span data-stu-id="e1318-130">The eviction policy for the low priority virtual machine.</span></span>  <span data-ttu-id="e1318-131">Csak a támogatott érték "deallokációja".</span><span class="sxs-lookup"><span data-stu-id="e1318-131">Only supported value is 'Deallocate'.</span></span>

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

### <span data-ttu-id="e1318-132">-Állomásazonosító</span><span class="sxs-lookup"><span data-stu-id="e1318-132">-HostId</span></span>
<span data-ttu-id="e1318-133">Az állomás azonosítója</span><span class="sxs-lookup"><span data-stu-id="e1318-133">The Id of Host</span></span>

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

### <span data-ttu-id="e1318-134">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="e1318-134">-IdentityId</span></span>
<span data-ttu-id="e1318-135">A virtuálisgép-készlethez társított felhasználói identitások listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="e1318-135">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="e1318-136">A felhasználói identitás hivatkozásai az űrlapon az "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}" típusú erőforrás-azonosítók lesznek.</span><span class="sxs-lookup"><span data-stu-id="e1318-136">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="e1318-137">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="e1318-137">-IdentityType</span></span>
<span data-ttu-id="e1318-138">A virtuális gép identitása, ha be van állítva.</span><span class="sxs-lookup"><span data-stu-id="e1318-138">The identity of the virtual machine, if configured.</span></span>

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

### <span data-ttu-id="e1318-139">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="e1318-139">-LicenseType</span></span>
<span data-ttu-id="e1318-140">A licenc típusa, amely a saját licenc-forgatókönyv készítéséhez szükséges.</span><span class="sxs-lookup"><span data-stu-id="e1318-140">The license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="e1318-141">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="e1318-141">-MaxPrice</span></span>
<span data-ttu-id="e1318-142">Itt adhatja meg, hogy az alacsony prioritású VM/VMSS milyen maximális árat fizessen.</span><span class="sxs-lookup"><span data-stu-id="e1318-142">Specifies the maximum price you are willing to pay for a low priority VM/VMSS.</span></span> <span data-ttu-id="e1318-143">Ez az ár amerikai dollárban van.</span><span class="sxs-lookup"><span data-stu-id="e1318-143">This price is in US Dollars.</span></span> <span data-ttu-id="e1318-144">Ezt az árat a program összehasonlítja a VM-méret jelenlegi alacsony prioritási árával.</span><span class="sxs-lookup"><span data-stu-id="e1318-144">This price will be compared with the current low priority price for the VM size.</span></span> <span data-ttu-id="e1318-145">Az árakat az alacsony prioritású VM/VMSS létrehozásának/frissítésének időpontjában is összehasonlították, és a művelet csak akkor fog sikerülni, ha a maxPrice nagyobb, mint a jelenlegi alacsony prioritású ár.</span><span class="sxs-lookup"><span data-stu-id="e1318-145">Also, the prices are compared at the time of create/update of low priority VM/VMSS and the operation will only succeed if the maxPrice is greater than the current low priority price.</span></span> <span data-ttu-id="e1318-146">A maxPrice a VM/VMSS létrehozása után is az alacsony prioritású VM/VMSS eltávolítására használható, ha a jelenlegi alacsony prioritású ár túllépi a maxPrice.</span><span class="sxs-lookup"><span data-stu-id="e1318-146">The maxPrice will also be used for evicting a low priority VM/VMSS if the current low priority price goes beyond the maxPrice after creation of VM/VMSS.</span></span> <span data-ttu-id="e1318-147">Lehetséges értékek: bármely nullánál nagyobb decimális érték.</span><span class="sxs-lookup"><span data-stu-id="e1318-147">Possible values are: any decimal value greater than zero.</span></span> <span data-ttu-id="e1318-148">Példa: 0,01538.</span><span class="sxs-lookup"><span data-stu-id="e1318-148">Example: 0.01538.</span></span>  <span data-ttu-id="e1318-149">-1 – azt jelzi, hogy az alacsony prioritású VM/VMSS nem szabad az árak miatt kizárni.</span><span class="sxs-lookup"><span data-stu-id="e1318-149">-1 indicates that the low priority VM/VMSS should not be evicted for price reasons.</span></span> <span data-ttu-id="e1318-150">Az alapértelmezett Max ár is-1, ha az nem az Ön által megadott.</span><span class="sxs-lookup"><span data-stu-id="e1318-150">Also, the default max price is -1 if it is not provided by you.</span></span>

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

### <span data-ttu-id="e1318-151">– Prioritás</span><span class="sxs-lookup"><span data-stu-id="e1318-151">-Priority</span></span>
<span data-ttu-id="e1318-152">A virtuális gép prioritása.</span><span class="sxs-lookup"><span data-stu-id="e1318-152">The priority for the virtual machine.</span></span>  <span data-ttu-id="e1318-153">Csak a támogatott értékek "normál" és "alacsony".</span><span class="sxs-lookup"><span data-stu-id="e1318-153">Only supported values are 'Regular' and 'Low'.</span></span>

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

### <span data-ttu-id="e1318-154">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="e1318-154">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="e1318-155">A ProximityPlacementGroup azonosítója</span><span class="sxs-lookup"><span data-stu-id="e1318-155">The Id of ProximityPlacementGroup</span></span>

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

### <span data-ttu-id="e1318-156">-Címkék</span><span class="sxs-lookup"><span data-stu-id="e1318-156">-Tags</span></span>
<span data-ttu-id="e1318-157">Az erőforráshoz társított címkék.</span><span class="sxs-lookup"><span data-stu-id="e1318-157">The tags attached to the resource.</span></span>

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

### <span data-ttu-id="e1318-158">-VMName</span><span class="sxs-lookup"><span data-stu-id="e1318-158">-VMName</span></span>
<span data-ttu-id="e1318-159">A virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e1318-159">Specifies a name for the virtual machine.</span></span>

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

### <span data-ttu-id="e1318-160">-VMSize</span><span class="sxs-lookup"><span data-stu-id="e1318-160">-VMSize</span></span>
<span data-ttu-id="e1318-161">A virtuális gép méretét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e1318-161">Specifies the size for the virtual machine.</span></span>

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

### <span data-ttu-id="e1318-162">-VmssId</span><span class="sxs-lookup"><span data-stu-id="e1318-162">-VmssId</span></span>
<span data-ttu-id="e1318-163">A virtuális gép méretarányának azonosítója</span><span class="sxs-lookup"><span data-stu-id="e1318-163">The Id of virtual machine scale set</span></span>

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

### <span data-ttu-id="e1318-164">-Zone (zóna)</span><span class="sxs-lookup"><span data-stu-id="e1318-164">-Zone</span></span>
<span data-ttu-id="e1318-165">A virtuális gép elérhetőségi zóna listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="e1318-165">Specifies the availability zone list for the virtual machine.</span></span> <span data-ttu-id="e1318-166">A megengedett értékek a régió képességeitől függenek.</span><span class="sxs-lookup"><span data-stu-id="e1318-166">The allowed values depend on the capabilities of the region.</span></span> <span data-ttu-id="e1318-167">A megengedett értékek általában 1, 2, 3.</span><span class="sxs-lookup"><span data-stu-id="e1318-167">Allowed values will normally be 1,2,3.</span></span>

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

### <span data-ttu-id="e1318-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1318-168">CommonParameters</span></span>
<span data-ttu-id="e1318-169">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e1318-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1318-170">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e1318-170">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1318-171">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e1318-171">INPUTS</span></span>

### <span data-ttu-id="e1318-172">System. String</span><span class="sxs-lookup"><span data-stu-id="e1318-172">System.String</span></span>

### <span data-ttu-id="e1318-173">System. string []</span><span class="sxs-lookup"><span data-stu-id="e1318-173">System.String[]</span></span>

### <span data-ttu-id="e1318-174">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="e1318-174">System.Collections.Hashtable</span></span>

### <span data-ttu-id="e1318-175">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="e1318-175">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e1318-176">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e1318-176">OUTPUTS</span></span>

### <span data-ttu-id="e1318-177">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="e1318-177">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="e1318-178">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e1318-178">NOTES</span></span>

## <span data-ttu-id="e1318-179">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e1318-179">RELATED LINKS</span></span>

[<span data-ttu-id="e1318-180">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="e1318-180">Update-AzVM</span></span>](./Update-AzVM.md)

[<span data-ttu-id="e1318-181">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="e1318-181">Set-AzVMOperatingSystem</span></span>](./Set-AzVMOperatingSystem.md)

[<span data-ttu-id="e1318-182">Set-AzVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="e1318-182">Set-AzVMSourceImage</span></span>](./Set-AzVMSourceImage.md)

[<span data-ttu-id="e1318-183">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="e1318-183">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)


