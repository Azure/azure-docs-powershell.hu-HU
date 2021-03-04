---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 1BECAC91-BB43-46EB-B2C9-C965C6FBC831
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azvmconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMConfig.md
ms.openlocfilehash: 71aa555528ff1cdb5748c1a4ac62481ddd17c17c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938873"
---
# <span data-ttu-id="2bbfd-101">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="2bbfd-101">New-AzVMConfig</span></span>

## <span data-ttu-id="2bbfd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2bbfd-102">SYNOPSIS</span></span>
<span data-ttu-id="2bbfd-103">Konfigurálható virtuális gépobjektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="2bbfd-103">Creates a configurable virtual machine object.</span></span>

## <span data-ttu-id="2bbfd-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2bbfd-104">SYNTAX</span></span>

### <span data-ttu-id="2bbfd-105">DefaultParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2bbfd-105">DefaultParameterSet (Default)</span></span>
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>] [[-LicenseType] <String>]
 [-Zone <String[]>] [-ProximityPlacementGroupId <String>] [-HostId <String>] [-VmssId <String>]
 [-MaxPrice <Double>] [-EvictionPolicy <String>] [-Priority <String>] [-Tags <Hashtable>] [-EnableUltraSSD] 
 [-EncryptionAtHost] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2bbfd-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="2bbfd-106">ExplicitIdentityParameterSet</span></span>
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>] [[-LicenseType] <String>]
 [-IdentityType] <ResourceIdentityType> [-IdentityId <String[]>] [-Zone <String[]>]
 [-ProximityPlacementGroupId <String>] [-HostId <String>] [-VmssId <String>] [-MaxPrice <Double>]
 [-EvictionPolicy <String>] [-Priority <String>] [-Tags <Hashtable>] [-EnableUltraSSD]
 [-EncryptionAtHost] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2bbfd-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2bbfd-107">DESCRIPTION</span></span>
<span data-ttu-id="2bbfd-108">A **New-AzVMConfig** parancsmag létrehoz egy konfigurálható helyi virtuális gépobjektumot az Azure-hoz.</span><span class="sxs-lookup"><span data-stu-id="2bbfd-108">The **New-AzVMConfig** cmdlet creates a configurable local virtual machine object for Azure.</span></span>
<span data-ttu-id="2bbfd-109">A virtuális gépi objektumok (például Set-AzVMOperatingSystem, Set-AzVMSourceImage, Add-AzVMNetworkInterface és Set-AzVMOSDisk) konfigurálása más parancsmagokkal is használhatók.</span><span class="sxs-lookup"><span data-stu-id="2bbfd-109">Other cmdlets can be used to configure a virtual machine object, such as Set-AzVMOperatingSystem, Set-AzVMSourceImage, Add-AzVMNetworkInterface, and Set-AzVMOSDisk.</span></span>

## <span data-ttu-id="2bbfd-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2bbfd-110">EXAMPLES</span></span>

### <span data-ttu-id="2bbfd-111">1. példa: Virtuális gépi objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="2bbfd-111">Example 1: Create a virtual machine object</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
```

<span data-ttu-id="2bbfd-112">Az első parancs az Erőforráscsoport11 erőforráscsoportBan az AvailabilitySet03 nevű elérhetőségi halmazt kapja, majd az objektumot a $AvailabilitySet tárolja.</span><span class="sxs-lookup"><span data-stu-id="2bbfd-112">The first command gets the availability set named AvailabilitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="2bbfd-113">A második parancs létrehoz egy virtuális gépobjektumot, majd a $VirtualMachine tárolja.</span><span class="sxs-lookup"><span data-stu-id="2bbfd-113">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="2bbfd-114">A parancs nevet és méretet rendel a virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="2bbfd-114">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="2bbfd-115">A virtuális gép a 2016-ban tárolt rendelkezésre állási $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="2bbfd-115">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

## <span data-ttu-id="2bbfd-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2bbfd-116">PARAMETERS</span></span>

### <span data-ttu-id="2bbfd-117">-AvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="2bbfd-117">-AvailabilitySetId</span></span>
<span data-ttu-id="2bbfd-118">Egy rendelkezésre állási készlet azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="2bbfd-118">Specifies the ID of an availability set.</span></span>
<span data-ttu-id="2bbfd-119">Az elérhetőségi halmaz objektum beszerzéséhez használja a Get-AzAvailabilitySet parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="2bbfd-119">To obtain an availability set object, use the Get-AzAvailabilitySet cmdlet.</span></span>
<span data-ttu-id="2bbfd-120">Az elérhetőségi halmaz objektum egy ID tulajdonságot tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="2bbfd-120">The availability set object contains an ID property.</span></span> <br>
<span data-ttu-id="2bbfd-121">Az ugyanazon rendelkezésre állási halmazban megadott virtuális gépek a rendelkezésre állás maximalizálása érdekében különböző csomópontokra vannak kiosztva.</span><span class="sxs-lookup"><span data-stu-id="2bbfd-121">Virtual machines specified in the same availability set are allocated to different nodes to maximize availability.</span></span> <br>
<span data-ttu-id="2bbfd-122">Az elérhetőségi készletekről további információt a virtuális gépek elérhetőségének [kezelése.](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-manage-availability?toc=%2fazure%2fvirtual-machines%2fwindows%2ftoc.json)</span><span class="sxs-lookup"><span data-stu-id="2bbfd-122">For more information about availability sets, see [Manage the availability of virtual machines](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-manage-availability?toc=%2fazure%2fvirtual-machines%2fwindows%2ftoc.json).</span></span> <br>
<span data-ttu-id="2bbfd-123">Az Azure tervezett karbantartásával kapcsolatos további információkért lásd: Tervezett karbantartás [virtuális gépekhez az Azure-ban](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-planned-maintenance?toc=%2fazure%2fvirtual-machines%2fwindows%2ftoc.json)</span><span class="sxs-lookup"><span data-stu-id="2bbfd-123">For more information on Azure planned maintenance, see [Planned maintenance for virtual machines in Azure](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-planned-maintenance?toc=%2fazure%2fvirtual-machines%2fwindows%2ftoc.json)</span></span> <br>
<span data-ttu-id="2bbfd-124">Jelenleg egy virtuális gép csak a létrehozáskor megadott elérhetőségi beállításhoz vehető fel.</span><span class="sxs-lookup"><span data-stu-id="2bbfd-124">Currently, a VM can only be added to availability set at creation time.</span></span> <span data-ttu-id="2bbfd-125">Az elérhetőségi készletnek, amelyhez a VM-et hozzá kell adni, ugyanabban az erőforráscsoportban kell lennie, mint az elérhetőségi készlet erőforrásnak.</span><span class="sxs-lookup"><span data-stu-id="2bbfd-125">The availability set to which the VM is being added should be under the same resource group as the availability set resource.</span></span> <span data-ttu-id="2bbfd-126">Egy meglévő virtuális gép nem vehető fel egy rendelkezésre állási készletbe.</span><span class="sxs-lookup"><span data-stu-id="2bbfd-126">An existing VM cannot be added to an availability set.</span></span> <br>
<span data-ttu-id="2bbfd-127">Ez a tulajdonság nem létezhet nem null értékű properties.virtualMachineScaleSet hivatkozással együtt.</span><span class="sxs-lookup"><span data-stu-id="2bbfd-127">This property cannot exist along with a non-null properties.virtualMachineScaleSet reference.</span></span>

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

### <span data-ttu-id="2bbfd-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2bbfd-128">-DefaultProfile</span></span>
<span data-ttu-id="2bbfd-129">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2bbfd-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2bbfd-130">-EnableUltraSSD</span><span class="sxs-lookup"><span data-stu-id="2bbfd-130">-EnableUltraSSD</span></span>
<span data-ttu-id="2bbfd-131">Lehetővé teszi, hogy egy vagy több felügyelt adatlemezzel UltraSSD_LRS tárolófióktípussal a VM-en.</span><span class="sxs-lookup"><span data-stu-id="2bbfd-131">Enables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the VM.</span></span>
<span data-ttu-id="2bbfd-132">A tárfiók-típussal rendelkező felügyelt UltraSSD_LRS csak akkor lehet virtuális gépre hozzáadni, ha ez a tulajdonság engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="2bbfd-132">Managed disks with storage account type UltraSSD_LRS can be added to a virtual machine only if this property is enabled.</span></span>


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

### <span data-ttu-id="2bbfd-133">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="2bbfd-133">-EvictionPolicy</span></span>
<span data-ttu-id="2bbfd-134">Az Azure Spot virtuális gépre vonatkozó kilakoltatási házirend.</span><span class="sxs-lookup"><span data-stu-id="2bbfd-134">The eviction policy for the Azure Spot virtual machine.</span></span>  <span data-ttu-id="2bbfd-135">A támogatott értékek a "Deallocate" és a "Delete".</span><span class="sxs-lookup"><span data-stu-id="2bbfd-135">Supported values are 'Deallocate' and 'Delete'.</span></span>

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

### <span data-ttu-id="2bbfd-136">-HostId</span><span class="sxs-lookup"><span data-stu-id="2bbfd-136">-HostId</span></span>
<span data-ttu-id="2bbfd-137">A host azonosítója</span><span class="sxs-lookup"><span data-stu-id="2bbfd-137">The Id of Host</span></span>

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

### <span data-ttu-id="2bbfd-138">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="2bbfd-138">-IdentityId</span></span>
<span data-ttu-id="2bbfd-139">A virtuális gép méretkészletével társított felhasználói identitások listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="2bbfd-139">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="2bbfd-140">A felhasználói identitáshivatkozások ARM következő űrlapon található erőforrás-azonosítók lesznek: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span><span class="sxs-lookup"><span data-stu-id="2bbfd-140">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="2bbfd-141">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="2bbfd-141">-IdentityType</span></span>
<span data-ttu-id="2bbfd-142">A virtuális gép identitása, ha be van állítva.</span><span class="sxs-lookup"><span data-stu-id="2bbfd-142">The identity of the virtual machine, if configured.</span></span>

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

### <span data-ttu-id="2bbfd-143">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="2bbfd-143">-LicenseType</span></span>
<span data-ttu-id="2bbfd-144">Egy licenctípust ad meg, amely azt jelzi, hogy a virtuális gép lemezképe vagy lemeze a helyszínen lett licenccel.</span><span class="sxs-lookup"><span data-stu-id="2bbfd-144">Specifies a license type, which indicates that the image or disk for the virtual machine was licensed on-premises.</span></span>
<span data-ttu-id="2bbfd-145">A Windows Server lehetséges értékei:</span><span class="sxs-lookup"><span data-stu-id="2bbfd-145">Possible values for Windows Server are:</span></span>
- <span data-ttu-id="2bbfd-146">Windows_Client</span><span class="sxs-lookup"><span data-stu-id="2bbfd-146">Windows_Client</span></span>
- <span data-ttu-id="2bbfd-147">Windows_Server Linux Server operációs rendszer lehetséges értékei:</span><span class="sxs-lookup"><span data-stu-id="2bbfd-147">Windows_Server Possible values for Linux Server operating system are:</span></span> 
- <span data-ttu-id="2bbfd-148">RHEL_BYOS (RHEL)</span><span class="sxs-lookup"><span data-stu-id="2bbfd-148">RHEL_BYOS (for RHEL)</span></span> 
- <span data-ttu-id="2bbfd-149">SLES_BYOS (SUSE)</span><span class="sxs-lookup"><span data-stu-id="2bbfd-149">SLES_BYOS (for SUSE)</span></span> 

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

### <span data-ttu-id="2bbfd-150">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="2bbfd-150">-MaxPrice</span></span>
<span data-ttu-id="2bbfd-151">Megadja az alacsony prioritású VM/VMSS-ek maximális árát.</span><span class="sxs-lookup"><span data-stu-id="2bbfd-151">Specifies the maximum price you are willing to pay for a low priority VM/VMSS.</span></span> <span data-ttu-id="2bbfd-152">Ez az ár amerikai dollárban van meg.</span><span class="sxs-lookup"><span data-stu-id="2bbfd-152">This price is in US Dollars.</span></span> <span data-ttu-id="2bbfd-153">Ezt az árat összehasonlítjuk a VM-méret jelenlegi alacsony prioritású árával.</span><span class="sxs-lookup"><span data-stu-id="2bbfd-153">This price will be compared with the current low priority price for the VM size.</span></span> <span data-ttu-id="2bbfd-154">Ezenkívül az alacsony prioritású VM/VMSS létrehozása/frissítése során összehasonlítja az árakat, és a művelet csak akkor lesz sikeres, ha a maxPrice nagyobb, mint a jelenlegi alacsony prioritású ár.</span><span class="sxs-lookup"><span data-stu-id="2bbfd-154">Also, the prices are compared at the time of create/update of low priority VM/VMSS and the operation will only succeed if the maxPrice is greater than the current low priority price.</span></span> <span data-ttu-id="2bbfd-155">A maxPrice akkor is használatos az alacsony prioritású VM/VMSS kivoktatására, ha a jelenlegi alacsony prioritású ár meghaladja a VM/VMSS létrehozását követően a maxPrice értéken.</span><span class="sxs-lookup"><span data-stu-id="2bbfd-155">The maxPrice will also be used for evicting a low priority VM/VMSS if the current low priority price goes beyond the maxPrice after creation of VM/VMSS.</span></span> <span data-ttu-id="2bbfd-156">A lehetséges értékek a nullánál nagyobb decimális értékek.</span><span class="sxs-lookup"><span data-stu-id="2bbfd-156">Possible values are: any decimal value greater than zero.</span></span> <span data-ttu-id="2bbfd-157">Példa: 0,01538.</span><span class="sxs-lookup"><span data-stu-id="2bbfd-157">Example: 0.01538.</span></span>  <span data-ttu-id="2bbfd-158">-1 azt jelzi, hogy az alacsony prioritású VM/VMSS nem lesz kiváltva ár miatt.</span><span class="sxs-lookup"><span data-stu-id="2bbfd-158">-1 indicates that the low priority VM/VMSS should not be evicted for price reasons.</span></span> <span data-ttu-id="2bbfd-159">Az alapértelmezett maximális ár -1, ha nem Ön biztosítja.</span><span class="sxs-lookup"><span data-stu-id="2bbfd-159">Also, the default max price is -1 if it is not provided by you.</span></span>

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

### <span data-ttu-id="2bbfd-160">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="2bbfd-160">-EncryptionAtHost</span></span>
<span data-ttu-id="2bbfd-161">A EncryptionAtHost tulajdonságot a felhasználó használhatja a kérésben a gazdatitkosítás engedélyezéséhez vagy letiltásához a virtuális gép vagy virtuális gép méretarányának beállítására.</span><span class="sxs-lookup"><span data-stu-id="2bbfd-161">EncryptionAtHost property can be used by user in the request to enable or disable the Host Encryption for the virtual machine or virtual machine scale set.</span></span> <span data-ttu-id="2bbfd-162">Ez lehetővé teszi a titkosítást az összes lemezen, beleértve magában az erőforrás-/ideiglenes lemezen is.</span><span class="sxs-lookup"><span data-stu-id="2bbfd-162">This will enable the encryption for all the disks including Resource/Temp disk at host itself.</span></span> <span data-ttu-id="2bbfd-163">Alapértelmezett: A gazdaszámítógép titkosítása le lesz tiltva, hacsak ez a tulajdonság nincs igazra állítva az erőforráshoz.</span><span class="sxs-lookup"><span data-stu-id="2bbfd-163">Default: The Encryption at host will be disabled unless this property is set to true for the resource.</span></span>

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

### <span data-ttu-id="2bbfd-164">-Priority</span><span class="sxs-lookup"><span data-stu-id="2bbfd-164">-Priority</span></span>
<span data-ttu-id="2bbfd-165">A virtuális gép prioritása.</span><span class="sxs-lookup"><span data-stu-id="2bbfd-165">The priority for the virtual machine.</span></span>  <span data-ttu-id="2bbfd-166">Csak a "Regular", a "Spot" és a "Low" támogatott értékeket támogatja.</span><span class="sxs-lookup"><span data-stu-id="2bbfd-166">Only supported values are 'Regular', 'Spot' and 'Low'.</span></span>
<span data-ttu-id="2bbfd-167">A "Regular" normál virtuális géphez való.</span><span class="sxs-lookup"><span data-stu-id="2bbfd-167">'Regular' is for regular virtual machine.</span></span>
<span data-ttu-id="2bbfd-168">A "Spot" a direkt virtuális gépekhez való.</span><span class="sxs-lookup"><span data-stu-id="2bbfd-168">'Spot' is for spot virtual machine.</span></span>
<span data-ttu-id="2bbfd-169">A "Low" a direkt virtuális gépre is igaz, de a "Spot" (Direkt) szövegre cseréli.</span><span class="sxs-lookup"><span data-stu-id="2bbfd-169">'Low' is also for spot virtual machine but is replaced by 'Spot'.</span></span> <span data-ttu-id="2bbfd-170">A "Gyenge" helyett használja a "Spot" (Direkt) használhatja.</span><span class="sxs-lookup"><span data-stu-id="2bbfd-170">Please use 'Spot' instead of 'Low'.</span></span>

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

### <span data-ttu-id="2bbfd-171">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="2bbfd-171">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="2bbfd-172">Az ezzel a virtuális géppel használható Közelség elhelyezési csoport erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="2bbfd-172">The resource id of the Proximity Placement Group to use with this virtual machine.</span></span>

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

### <span data-ttu-id="2bbfd-173">-Címkék</span><span class="sxs-lookup"><span data-stu-id="2bbfd-173">-Tags</span></span>
<span data-ttu-id="2bbfd-174">Az erőforráshoz csatolt címkék.</span><span class="sxs-lookup"><span data-stu-id="2bbfd-174">The tags attached to the resource.</span></span>

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

### <span data-ttu-id="2bbfd-175">-VMName</span><span class="sxs-lookup"><span data-stu-id="2bbfd-175">-VMName</span></span>
<span data-ttu-id="2bbfd-176">Megadja a virtuális gép nevét.</span><span class="sxs-lookup"><span data-stu-id="2bbfd-176">Specifies a name for the virtual machine.</span></span>

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

### <span data-ttu-id="2bbfd-177">-VMSize</span><span class="sxs-lookup"><span data-stu-id="2bbfd-177">-VMSize</span></span>
<span data-ttu-id="2bbfd-178">A virtuális gép méretét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2bbfd-178">Specifies the size for the virtual machine.</span></span>

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

### <span data-ttu-id="2bbfd-179">-VmssId</span><span class="sxs-lookup"><span data-stu-id="2bbfd-179">-VmssId</span></span>
<span data-ttu-id="2bbfd-180">A virtuális gép méretaránykészletének azonosítója</span><span class="sxs-lookup"><span data-stu-id="2bbfd-180">The Id of virtual machine scale set</span></span>

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

### <span data-ttu-id="2bbfd-181">-Zone</span><span class="sxs-lookup"><span data-stu-id="2bbfd-181">-Zone</span></span>
<span data-ttu-id="2bbfd-182">A virtuális gép elérhetőségi zónalistát adja meg.</span><span class="sxs-lookup"><span data-stu-id="2bbfd-182">Specifies the availability zone list for the virtual machine.</span></span> <span data-ttu-id="2bbfd-183">Az engedélyezett értékek a régió képességeitől függnek.</span><span class="sxs-lookup"><span data-stu-id="2bbfd-183">The allowed values depend on the capabilities of the region.</span></span> <span data-ttu-id="2bbfd-184">Az engedélyezett értékek általában 1,2,3 lesznek.</span><span class="sxs-lookup"><span data-stu-id="2bbfd-184">Allowed values will normally be 1,2,3.</span></span>

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

### <span data-ttu-id="2bbfd-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bbfd-185">CommonParameters</span></span>
<span data-ttu-id="2bbfd-186">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2bbfd-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bbfd-187">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2bbfd-187">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bbfd-188">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2bbfd-188">INPUTS</span></span>

### <span data-ttu-id="2bbfd-189">System.String</span><span class="sxs-lookup"><span data-stu-id="2bbfd-189">System.String</span></span>

### <span data-ttu-id="2bbfd-190">System.String[]</span><span class="sxs-lookup"><span data-stu-id="2bbfd-190">System.String[]</span></span>

### <span data-ttu-id="2bbfd-191">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="2bbfd-191">System.Collections.Hashtable</span></span>

### <span data-ttu-id="2bbfd-192">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="2bbfd-192">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="2bbfd-193">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2bbfd-193">OUTPUTS</span></span>

### <span data-ttu-id="2bbfd-194">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="2bbfd-194">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="2bbfd-195">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2bbfd-195">NOTES</span></span>

## <span data-ttu-id="2bbfd-196">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2bbfd-196">RELATED LINKS</span></span>

[<span data-ttu-id="2bbfd-197">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="2bbfd-197">Update-AzVM</span></span>](./Update-AzVM.md)

[<span data-ttu-id="2bbfd-198">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="2bbfd-198">Set-AzVMOperatingSystem</span></span>](./Set-AzVMOperatingSystem.md)

[<span data-ttu-id="2bbfd-199">Set-AzVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="2bbfd-199">Set-AzVMSourceImage</span></span>](./Set-AzVMSourceImage.md)

[<span data-ttu-id="2bbfd-200">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="2bbfd-200">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)


