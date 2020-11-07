---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 1BECAC91-BB43-46EB-B2C9-C965C6FBC831
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMConfig.md
ms.openlocfilehash: 4fd4c3a903910068933a46d3343e8dc990565b8b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671306"
---
# <span data-ttu-id="401b9-101">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="401b9-101">New-AzVMConfig</span></span>

## <span data-ttu-id="401b9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="401b9-102">SYNOPSIS</span></span>
<span data-ttu-id="401b9-103">Konfigurálható virtuálisgép-objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="401b9-103">Creates a configurable virtual machine object.</span></span>

## <span data-ttu-id="401b9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="401b9-104">SYNTAX</span></span>

### <span data-ttu-id="401b9-105">DefaultParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="401b9-105">DefaultParameterSet (Default)</span></span>
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>] [[-LicenseType] <String>]
 [-Zone <String[]>] [-Tags <Hashtable>] [-EnableUltraSSD] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="401b9-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="401b9-106">ExplicitIdentityParameterSet</span></span>
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>] [[-LicenseType] <String>]
 [-IdentityType] <ResourceIdentityType> [-IdentityId <String[]>] [-Zone <String[]>] [-Tags <Hashtable>]
 [-EnableUltraSSD] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="401b9-107">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="401b9-107">AssignIdentityParameterSet</span></span>
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>] [[-LicenseType] <String>]
 [-AssignIdentity] [-Zone <String[]>] [-Tags <Hashtable>] [-EnableUltraSSD]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="401b9-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="401b9-108">DESCRIPTION</span></span>
<span data-ttu-id="401b9-109">A **New-AzVMConfig** parancsmag létrehoz egy konfigurálható helyi virtuálisgép-objektumot az Azure-hoz.</span><span class="sxs-lookup"><span data-stu-id="401b9-109">The **New-AzVMConfig** cmdlet creates a configurable local virtual machine object for Azure.</span></span>
<span data-ttu-id="401b9-110">Az egyéb parancsmagok segítségével konfigurálhatók a virtuálisgép-objektumok, például a set-AzVMOperatingSystem, a set-AzVMSourceImage, a Add-AzVMNetworkInterface és a set-AzVMOSDisk.</span><span class="sxs-lookup"><span data-stu-id="401b9-110">Other cmdlets can be used to configure a virtual machine object, such as Set-AzVMOperatingSystem, Set-AzVMSourceImage, Add-AzVMNetworkInterface, and Set-AzVMOSDisk.</span></span>

## <span data-ttu-id="401b9-111">Példák</span><span class="sxs-lookup"><span data-stu-id="401b9-111">EXAMPLES</span></span>

### <span data-ttu-id="401b9-112">Példa 1: virtuális gép objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="401b9-112">Example 1: Create a virtual machine object</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
```

<span data-ttu-id="401b9-113">Az első parancs beolvassa a AvailablitySet03 nevű ResourceGroup11 nevű erőforráscsoport elérhetőségi készletét, majd a $AvailabilitySet változóban tárolja az objektumot.</span><span class="sxs-lookup"><span data-stu-id="401b9-113">The first command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="401b9-114">A második parancs létrehoz egy Virtual Machine-objektumot, majd a $VirtualMachine változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="401b9-114">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="401b9-115">A parancs nevet és méretet rendel a virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="401b9-115">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="401b9-116">A virtuális gép a $AvailabilitySetban tárolt elérhetőségi készlethez tartozik.</span><span class="sxs-lookup"><span data-stu-id="401b9-116">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

## <span data-ttu-id="401b9-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="401b9-117">PARAMETERS</span></span>

### <span data-ttu-id="401b9-118">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="401b9-118">-AssignIdentity</span></span>
<span data-ttu-id="401b9-119">Adja meg a virtuális gép rendszerhez rendelt identitását.</span><span class="sxs-lookup"><span data-stu-id="401b9-119">Specify the system assigned identity for the virtual machine.</span></span>

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

### <span data-ttu-id="401b9-120">-AvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="401b9-120">-AvailabilitySetId</span></span>
<span data-ttu-id="401b9-121">A rendelkezésre álló készlet AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="401b9-121">Specifies the ID of an availability set.</span></span>
<span data-ttu-id="401b9-122">Az elérhetőségi készlet objektum beolvasásához használja az Get-AzAvailabilitySet parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="401b9-122">To obtain an availability set object, use the Get-AzAvailabilitySet cmdlet.</span></span>
<span data-ttu-id="401b9-123">Az elérhetőségi készlet objektum egy azonosító tulajdonságot tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="401b9-123">The availability set object contains an ID property.</span></span>

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

### <span data-ttu-id="401b9-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="401b9-124">-DefaultProfile</span></span>
<span data-ttu-id="401b9-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="401b9-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="401b9-126">-EnableUltraSSD</span><span class="sxs-lookup"><span data-stu-id="401b9-126">-EnableUltraSSD</span></span>
<span data-ttu-id="401b9-127">Lehetővé teszi, hogy egy vagy több felügyelt adatlemez legyen a VM-UltraSSD_LRS tárterület-fiók típusával.</span><span class="sxs-lookup"><span data-stu-id="401b9-127">Enables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the VM.</span></span>
<span data-ttu-id="401b9-128">A felügyelt lemezek tároló fiók típusú UltraSSD_LRS csak akkor adhatók hozzá a virtuális géphez, ha a tulajdonság engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="401b9-128">Managed disks with storage account type UltraSSD_LRS can be added to a virtual machine only if this property is enabled.</span></span>


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

### <span data-ttu-id="401b9-129">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="401b9-129">-IdentityId</span></span>
<span data-ttu-id="401b9-130">A virtuálisgép-készlethez társított felhasználói identitások listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="401b9-130">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="401b9-131">A felhasználói identitás hivatkozásai az űrlapon az "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}" típusú erőforrás-azonosítók lesznek.</span><span class="sxs-lookup"><span data-stu-id="401b9-131">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="401b9-132">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="401b9-132">-IdentityType</span></span>
<span data-ttu-id="401b9-133">A virtuális gép identitása, ha be van állítva.</span><span class="sxs-lookup"><span data-stu-id="401b9-133">The identity of the virtual machine, if configured.</span></span>

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

### <span data-ttu-id="401b9-134">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="401b9-134">-LicenseType</span></span>
<span data-ttu-id="401b9-135">A licenc típusa, amely a saját licenc-forgatókönyv készítéséhez szükséges.</span><span class="sxs-lookup"><span data-stu-id="401b9-135">The license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="401b9-136">-Címkék</span><span class="sxs-lookup"><span data-stu-id="401b9-136">-Tags</span></span>
<span data-ttu-id="401b9-137">Az erőforráshoz társított címkék.</span><span class="sxs-lookup"><span data-stu-id="401b9-137">The tags attached to the resource.</span></span>

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

### <span data-ttu-id="401b9-138">-VMName</span><span class="sxs-lookup"><span data-stu-id="401b9-138">-VMName</span></span>
<span data-ttu-id="401b9-139">A virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="401b9-139">Specifies a name for the virtual machine.</span></span>

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

### <span data-ttu-id="401b9-140">-VMSize</span><span class="sxs-lookup"><span data-stu-id="401b9-140">-VMSize</span></span>
<span data-ttu-id="401b9-141">A virtuális gép méretét adja meg.</span><span class="sxs-lookup"><span data-stu-id="401b9-141">Specifies the size for the virtual machine.</span></span>

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

### <span data-ttu-id="401b9-142">-Zone (zóna)</span><span class="sxs-lookup"><span data-stu-id="401b9-142">-Zone</span></span>
<span data-ttu-id="401b9-143">A virtuális gép elérhetőségi zóna listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="401b9-143">Specifies the availability zone list for the virtual machine.</span></span> <span data-ttu-id="401b9-144">A megengedett értékek a régió képességeitől függenek.</span><span class="sxs-lookup"><span data-stu-id="401b9-144">The allowed values depend on the capabilities of the region.</span></span> <span data-ttu-id="401b9-145">A megengedett értékek általában 1, 2, 3.</span><span class="sxs-lookup"><span data-stu-id="401b9-145">Allowed values will normally be 1,2,3.</span></span>

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

### <span data-ttu-id="401b9-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="401b9-146">CommonParameters</span></span>
<span data-ttu-id="401b9-147">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="401b9-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="401b9-148">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="401b9-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="401b9-149">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="401b9-149">INPUTS</span></span>

### <span data-ttu-id="401b9-150">System. String</span><span class="sxs-lookup"><span data-stu-id="401b9-150">System.String</span></span>

### <span data-ttu-id="401b9-151">System. string []</span><span class="sxs-lookup"><span data-stu-id="401b9-151">System.String[]</span></span>

### <span data-ttu-id="401b9-152">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="401b9-152">System.Collections.Hashtable</span></span>

### <span data-ttu-id="401b9-153">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="401b9-153">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="401b9-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="401b9-154">OUTPUTS</span></span>

### <span data-ttu-id="401b9-155">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="401b9-155">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="401b9-156">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="401b9-156">NOTES</span></span>

## <span data-ttu-id="401b9-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="401b9-157">RELATED LINKS</span></span>

[<span data-ttu-id="401b9-158">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="401b9-158">Update-AzVM</span></span>](./Update-AzVM.md)

[<span data-ttu-id="401b9-159">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="401b9-159">Set-AzVMOperatingSystem</span></span>](./Set-AzVMOperatingSystem.md)

[<span data-ttu-id="401b9-160">Set-AzVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="401b9-160">Set-AzVMSourceImage</span></span>](./Set-AzVMSourceImage.md)

[<span data-ttu-id="401b9-161">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="401b9-161">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)


