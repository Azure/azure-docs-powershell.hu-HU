---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 1BECAC91-BB43-46EB-B2C9-C965C6FBC831
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVMConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVMConfig.md
ms.openlocfilehash: 4b128346d77e090e5b0699ace8f03eaa9a4786a1
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844470"
---
# <span data-ttu-id="6cc7c-101">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="6cc7c-101">New-AzVMConfig</span></span>

## <span data-ttu-id="6cc7c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6cc7c-102">SYNOPSIS</span></span>
<span data-ttu-id="6cc7c-103">Konfigurálható virtuálisgép-objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="6cc7c-103">Creates a configurable virtual machine object.</span></span>

## <span data-ttu-id="6cc7c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6cc7c-104">SYNTAX</span></span>

### <span data-ttu-id="6cc7c-105">DefaultParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6cc7c-105">DefaultParameterSet (Default)</span></span>
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>]
 [[-LicenseType] <String>] [-Zone <String[]>] [-Tags <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6cc7c-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="6cc7c-106">ExplicitIdentityParameterSet</span></span>
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>]
 [[-LicenseType] <String>] [-IdentityType] <ResourceIdentityType> [-IdentityId <String[]>] [-Zone <String[]>]
 [-Tags <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6cc7c-107">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="6cc7c-107">AssignIdentityParameterSet</span></span>
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>]
 [[-LicenseType] <String>] [-AssignIdentity] [-Zone <String[]>] [-Tags <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6cc7c-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="6cc7c-108">DESCRIPTION</span></span>
<span data-ttu-id="6cc7c-109">A **New-AzVMConfig** parancsmag létrehoz egy konfigurálható helyi virtuálisgép-objektumot az Azure-hoz.</span><span class="sxs-lookup"><span data-stu-id="6cc7c-109">The **New-AzVMConfig** cmdlet creates a configurable local virtual machine object for Azure.</span></span>
<span data-ttu-id="6cc7c-110">Az egyéb parancsmagok segítségével konfigurálhatók a virtuálisgép-objektumok, például a set-AzVMOperatingSystem, a set-AzVMSourceImage, a Add-AzVMNetworkInterface és a set-AzVMOSDisk.</span><span class="sxs-lookup"><span data-stu-id="6cc7c-110">Other cmdlets can be used to configure a virtual machine object, such as Set-AzVMOperatingSystem, Set-AzVMSourceImage, Add-AzVMNetworkInterface, and Set-AzVMOSDisk.</span></span>

## <span data-ttu-id="6cc7c-111">Példák</span><span class="sxs-lookup"><span data-stu-id="6cc7c-111">EXAMPLES</span></span>

### <span data-ttu-id="6cc7c-112">Példa 1: virtuális gép objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="6cc7c-112">Example 1: Create a virtual machine object</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
```

<span data-ttu-id="6cc7c-113">Az első parancs beolvassa a AvailablitySet03 nevű ResourceGroup11 nevű erőforráscsoport elérhetőségi készletét, majd a $AvailabilitySet változóban tárolja az objektumot.</span><span class="sxs-lookup"><span data-stu-id="6cc7c-113">The first command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>

<span data-ttu-id="6cc7c-114">A második parancs létrehoz egy Virtual Machine-objektumot, majd a $VirtualMachine változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="6cc7c-114">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="6cc7c-115">A parancs nevet és méretet rendel a virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="6cc7c-115">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="6cc7c-116">A virtuális gép a $AvailabilitySetban tárolt elérhetőségi készlethez tartozik.</span><span class="sxs-lookup"><span data-stu-id="6cc7c-116">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

## <span data-ttu-id="6cc7c-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6cc7c-117">PARAMETERS</span></span>

### <span data-ttu-id="6cc7c-118">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="6cc7c-118">-AssignIdentity</span></span>
<span data-ttu-id="6cc7c-119">Adja meg a virtuális gép rendszerhez rendelt identitását.</span><span class="sxs-lookup"><span data-stu-id="6cc7c-119">Specify the system assigned identity for the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AssignIdentityParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cc7c-120">-AvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="6cc7c-120">-AvailabilitySetId</span></span>
<span data-ttu-id="6cc7c-121">A rendelkezésre álló készlet AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="6cc7c-121">Specifies the ID of an availability set.</span></span>
<span data-ttu-id="6cc7c-122">Az elérhetőségi készlet objektum beolvasásához használja az Get-AzAvailabilitySet parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="6cc7c-122">To obtain an availability set object, use the Get-AzAvailabilitySet cmdlet.</span></span>
<span data-ttu-id="6cc7c-123">Az elérhetőségi készlet objektum egy azonosító tulajdonságot tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="6cc7c-123">The availability set object contains an ID property.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cc7c-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cc7c-124">-DefaultProfile</span></span>
<span data-ttu-id="6cc7c-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6cc7c-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6cc7c-126">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="6cc7c-126">-IdentityId</span></span>
<span data-ttu-id="6cc7c-127">A virtuálisgép-készlethez társított felhasználói identitások listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="6cc7c-127">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="6cc7c-128">A felhasználói identitás hivatkozásai az űrlapon az "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}" típusú erőforrás-azonosítók lesznek.</span><span class="sxs-lookup"><span data-stu-id="6cc7c-128">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

```yaml
Type: String[]
Parameter Sets: ExplicitIdentityParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cc7c-129">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="6cc7c-129">-IdentityType</span></span>
<span data-ttu-id="6cc7c-130">A virtuális gép identitása, ha be van állítva.</span><span class="sxs-lookup"><span data-stu-id="6cc7c-130">The identity of the virtual machine, if configured.</span></span>

```yaml
Type: ResourceIdentityType
Parameter Sets: ExplicitIdentityParameterSet
Aliases: 
Accepted values: SystemAssigned, UserAssigned, SystemAssignedUserAssigned, None

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cc7c-131">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="6cc7c-131">-LicenseType</span></span>
<span data-ttu-id="6cc7c-132">A licenc típusa, amely a saját licenc-forgatókönyv készítéséhez szükséges.</span><span class="sxs-lookup"><span data-stu-id="6cc7c-132">The license type, which is for bringing your own license scenario.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cc7c-133">-Címkék</span><span class="sxs-lookup"><span data-stu-id="6cc7c-133">-Tags</span></span>
<span data-ttu-id="6cc7c-134">Az erőforráshoz társított címkék.</span><span class="sxs-lookup"><span data-stu-id="6cc7c-134">The tags attached to the resource.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cc7c-135">-VMName</span><span class="sxs-lookup"><span data-stu-id="6cc7c-135">-VMName</span></span>
<span data-ttu-id="6cc7c-136">A virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6cc7c-136">Specifies a name for the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cc7c-137">-VMSize</span><span class="sxs-lookup"><span data-stu-id="6cc7c-137">-VMSize</span></span>
<span data-ttu-id="6cc7c-138">A virtuális gép méretét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6cc7c-138">Specifies the size for the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cc7c-139">-Zone (zóna)</span><span class="sxs-lookup"><span data-stu-id="6cc7c-139">-Zone</span></span>
<span data-ttu-id="6cc7c-140">A virtuális gép zóna listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="6cc7c-140">Specifies the zone list for the virtual machine.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cc7c-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cc7c-141">CommonParameters</span></span>
<span data-ttu-id="6cc7c-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6cc7c-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cc7c-143">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6cc7c-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cc7c-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6cc7c-144">INPUTS</span></span>

### <span data-ttu-id="6cc7c-145">Nincs</span><span class="sxs-lookup"><span data-stu-id="6cc7c-145">None</span></span>
<span data-ttu-id="6cc7c-146">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="6cc7c-146">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6cc7c-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6cc7c-147">OUTPUTS</span></span>

### <span data-ttu-id="6cc7c-148">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="6cc7c-148">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="6cc7c-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6cc7c-149">NOTES</span></span>

## <span data-ttu-id="6cc7c-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6cc7c-150">RELATED LINKS</span></span>

[<span data-ttu-id="6cc7c-151">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="6cc7c-151">Update-AzVM</span></span>](./Update-AzVM.md)

[<span data-ttu-id="6cc7c-152">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="6cc7c-152">Set-AzVMOperatingSystem</span></span>](./Set-AzVMOperatingSystem.md)

[<span data-ttu-id="6cc7c-153">Set-AzVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="6cc7c-153">Set-AzVMSourceImage</span></span>](./Set-AzVMSourceImage.md)

[<span data-ttu-id="6cc7c-154">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="6cc7c-154">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)


