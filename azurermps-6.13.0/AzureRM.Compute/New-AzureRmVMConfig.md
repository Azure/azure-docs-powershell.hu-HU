---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 1BECAC91-BB43-46EB-B2C9-C965C6FBC831
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvmconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVMConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVMConfig.md
ms.openlocfilehash: 6809088110944648781fc2264bd2c56f98cbee1a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499684"
---
# <span data-ttu-id="ab11b-101">New-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="ab11b-101">New-AzureRmVMConfig</span></span>

## <span data-ttu-id="ab11b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ab11b-102">SYNOPSIS</span></span>
<span data-ttu-id="ab11b-103">Konfigurálható virtuálisgép-objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="ab11b-103">Creates a configurable virtual machine object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ab11b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ab11b-104">SYNTAX</span></span>

### <span data-ttu-id="ab11b-105">DefaultParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ab11b-105">DefaultParameterSet (Default)</span></span>
```
New-AzureRmVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>]
 [[-LicenseType] <String>] [-Zone <String[]>] [-Tags <Hashtable>] [-EnableUltraSSD]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ab11b-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="ab11b-106">ExplicitIdentityParameterSet</span></span>
```
New-AzureRmVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>]
 [[-LicenseType] <String>] [-IdentityType] <ResourceIdentityType> [-IdentityId <String[]>] [-Zone <String[]>]
 [-Tags <Hashtable>] [-EnableUltraSSD] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ab11b-107">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="ab11b-107">AssignIdentityParameterSet</span></span>
```
New-AzureRmVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>]
 [[-LicenseType] <String>] [-AssignIdentity] [-Zone <String[]>] [-Tags <Hashtable>] [-EnableUltraSSD]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ab11b-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="ab11b-108">DESCRIPTION</span></span>
<span data-ttu-id="ab11b-109">A **New-AzureRmVMConfig** parancsmag létrehoz egy konfigurálható helyi virtuálisgép-objektumot az Azure-hoz.</span><span class="sxs-lookup"><span data-stu-id="ab11b-109">The **New-AzureRmVMConfig** cmdlet creates a configurable local virtual machine object for Azure.</span></span>
<span data-ttu-id="ab11b-110">Az egyéb parancsmagok segítségével konfigurálhatók a virtuálisgép-objektumok, például a set-AzureRmVMOperatingSystem, a set-AzureRmVMSourceImage, a Add-AzureRmVMNetworkInterface és a set-AzureRmVMOSDisk.</span><span class="sxs-lookup"><span data-stu-id="ab11b-110">Other cmdlets can be used to configure a virtual machine object, such as Set-AzureRmVMOperatingSystem, Set-AzureRmVMSourceImage, Add-AzureRmVMNetworkInterface, and Set-AzureRmVMOSDisk.</span></span>

## <span data-ttu-id="ab11b-111">Példák</span><span class="sxs-lookup"><span data-stu-id="ab11b-111">EXAMPLES</span></span>

### <span data-ttu-id="ab11b-112">Példa 1: virtuális gép objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="ab11b-112">Example 1: Create a virtual machine object</span></span>
```
PS C:\> $AvailabilitySet = Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
```

<span data-ttu-id="ab11b-113">Az első parancs beolvassa a AvailablitySet03 nevű ResourceGroup11 nevű erőforráscsoport elérhetőségi készletét, majd a $AvailabilitySet változóban tárolja az objektumot.</span><span class="sxs-lookup"><span data-stu-id="ab11b-113">The first command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="ab11b-114">A második parancs létrehoz egy Virtual Machine-objektumot, majd a $VirtualMachine változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="ab11b-114">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="ab11b-115">A parancs nevet és méretet rendel a virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="ab11b-115">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="ab11b-116">A virtuális gép a $AvailabilitySetban tárolt elérhetőségi készlethez tartozik.</span><span class="sxs-lookup"><span data-stu-id="ab11b-116">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

## <span data-ttu-id="ab11b-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ab11b-117">PARAMETERS</span></span>

### <span data-ttu-id="ab11b-118">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="ab11b-118">-AssignIdentity</span></span>
<span data-ttu-id="ab11b-119">Adja meg a virtuális gép rendszerhez rendelt identitását.</span><span class="sxs-lookup"><span data-stu-id="ab11b-119">Specify the system assigned identity for the virtual machine.</span></span>

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

### <span data-ttu-id="ab11b-120">-AvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="ab11b-120">-AvailabilitySetId</span></span>
<span data-ttu-id="ab11b-121">A rendelkezésre álló készlet AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="ab11b-121">Specifies the ID of an availability set.</span></span>
<span data-ttu-id="ab11b-122">Az elérhetőségi készlet objektum beolvasásához használja az Get-AzureRmAvailabilitySet parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="ab11b-122">To obtain an availability set object, use the Get-AzureRmAvailabilitySet cmdlet.</span></span>
<span data-ttu-id="ab11b-123">Az elérhetőségi készlet objektum egy azonosító tulajdonságot tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="ab11b-123">The availability set object contains an ID property.</span></span>

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

### <span data-ttu-id="ab11b-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab11b-124">-DefaultProfile</span></span>
<span data-ttu-id="ab11b-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ab11b-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ab11b-126">-EnableUltraSSD</span><span class="sxs-lookup"><span data-stu-id="ab11b-126">-EnableUltraSSD</span></span>
<span data-ttu-id="ab11b-127">Lehetővé teszi, hogy egy vagy több felügyelt adatlemez legyen a VM-UltraSSD_LRS tárterület-fiók típusával.</span><span class="sxs-lookup"><span data-stu-id="ab11b-127">Enables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the VM.</span></span>
<span data-ttu-id="ab11b-128">A felügyelt lemezek tároló fiók típusú UltraSSD_LRS csak akkor adhatók hozzá a virtuális géphez, ha a tulajdonság engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="ab11b-128">Managed disks with storage account type UltraSSD_LRS can be added to a virtual machine only if this property is enabled.</span></span>


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

### <span data-ttu-id="ab11b-129">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="ab11b-129">-IdentityId</span></span>
<span data-ttu-id="ab11b-130">A virtuálisgép-készlethez társított felhasználói identitások listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="ab11b-130">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="ab11b-131">A felhasználói identitás hivatkozásai az űrlapon az "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}" típusú erőforrás-azonosítók lesznek.</span><span class="sxs-lookup"><span data-stu-id="ab11b-131">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="ab11b-132">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="ab11b-132">-IdentityType</span></span>
<span data-ttu-id="ab11b-133">A virtuális gép identitása, ha be van állítva.</span><span class="sxs-lookup"><span data-stu-id="ab11b-133">The identity of the virtual machine, if configured.</span></span>

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

### <span data-ttu-id="ab11b-134">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="ab11b-134">-LicenseType</span></span>
<span data-ttu-id="ab11b-135">A licenc típusa, amely a saját licenc-forgatókönyv készítéséhez szükséges.</span><span class="sxs-lookup"><span data-stu-id="ab11b-135">The license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="ab11b-136">-Címkék</span><span class="sxs-lookup"><span data-stu-id="ab11b-136">-Tags</span></span>
<span data-ttu-id="ab11b-137">Az erőforráshoz társított címkék.</span><span class="sxs-lookup"><span data-stu-id="ab11b-137">The tags attached to the resource.</span></span>

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

### <span data-ttu-id="ab11b-138">-VMName</span><span class="sxs-lookup"><span data-stu-id="ab11b-138">-VMName</span></span>
<span data-ttu-id="ab11b-139">A virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ab11b-139">Specifies a name for the virtual machine.</span></span>

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

### <span data-ttu-id="ab11b-140">-VMSize</span><span class="sxs-lookup"><span data-stu-id="ab11b-140">-VMSize</span></span>
<span data-ttu-id="ab11b-141">A virtuális gép méretét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ab11b-141">Specifies the size for the virtual machine.</span></span>

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

### <span data-ttu-id="ab11b-142">-Zone (zóna)</span><span class="sxs-lookup"><span data-stu-id="ab11b-142">-Zone</span></span>
<span data-ttu-id="ab11b-143">A virtuális gép zóna listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="ab11b-143">Specifies the zone list for the virtual machine.</span></span>

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

### <span data-ttu-id="ab11b-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab11b-144">CommonParameters</span></span>
<span data-ttu-id="ab11b-145">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ab11b-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab11b-146">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab11b-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab11b-147">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ab11b-147">INPUTS</span></span>

### <span data-ttu-id="ab11b-148">System. String</span><span class="sxs-lookup"><span data-stu-id="ab11b-148">System.String</span></span>

### <span data-ttu-id="ab11b-149">System. string []</span><span class="sxs-lookup"><span data-stu-id="ab11b-149">System.String[]</span></span>

### <span data-ttu-id="ab11b-150">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="ab11b-150">System.Collections.Hashtable</span></span>

## <span data-ttu-id="ab11b-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ab11b-151">OUTPUTS</span></span>

### <span data-ttu-id="ab11b-152">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="ab11b-152">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="ab11b-153">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ab11b-153">NOTES</span></span>

## <span data-ttu-id="ab11b-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ab11b-154">RELATED LINKS</span></span>

[<span data-ttu-id="ab11b-155">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ab11b-155">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)

[<span data-ttu-id="ab11b-156">Set-AzureRmVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="ab11b-156">Set-AzureRmVMOperatingSystem</span></span>](./Set-AzureRmVMOperatingSystem.md)

[<span data-ttu-id="ab11b-157">Set-AzureRmVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="ab11b-157">Set-AzureRmVMSourceImage</span></span>](./Set-AzureRmVMSourceImage.md)

[<span data-ttu-id="ab11b-158">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="ab11b-158">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)


