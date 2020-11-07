---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 8F7AF1B8-D769-452C-92CF-4486C3EB894D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmosdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMOSDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMOSDisk.md
ms.openlocfilehash: 378d0d33d6cc1ceb2eca4773d93f76afbf75cf4b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844206"
---
# <span data-ttu-id="cdaa8-101">Set-AzVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="cdaa8-101">Set-AzVMOSDisk</span></span>

## <span data-ttu-id="cdaa8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cdaa8-102">SYNOPSIS</span></span>
<span data-ttu-id="cdaa8-103">Beállítja az operációs rendszer lemezének tulajdonságait egy virtuális gépen.</span><span class="sxs-lookup"><span data-stu-id="cdaa8-103">Sets the operating system disk properties on a virtual machine.</span></span>

## <span data-ttu-id="cdaa8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cdaa8-104">SYNTAX</span></span>

### <span data-ttu-id="cdaa8-105">DefaultParamSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cdaa8-105">DefaultParamSet (Default)</span></span>
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-SourceImageUri] <String>] [[-CreateOption] <DiskCreateOptionTypes>]
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <StorageAccountTypes>]
 [-WriteAccelerator] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cdaa8-106">WindowsParamSet</span><span class="sxs-lookup"><span data-stu-id="cdaa8-106">WindowsParamSet</span></span>
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-SourceImageUri] <String>] [[-CreateOption] <DiskCreateOptionTypes>] [-Windows]
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <StorageAccountTypes>]
 [-WriteAccelerator] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cdaa8-107">WindowsDiskEncryptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="cdaa8-107">WindowsDiskEncryptionParameterSet</span></span>
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-SourceImageUri] <String>] [[-CreateOption] <DiskCreateOptionTypes>] [-Windows]
 [-DiskEncryptionKeyUrl] <String> [-DiskEncryptionKeyVaultId] <String> [[-KeyEncryptionKeyUrl] <String>]
 [[-KeyEncryptionKeyVaultId] <String>] [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>]
 [-StorageAccountType <StorageAccountTypes>] [-WriteAccelerator] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cdaa8-108">LinuxParamSet</span><span class="sxs-lookup"><span data-stu-id="cdaa8-108">LinuxParamSet</span></span>
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-SourceImageUri] <String>] [[-CreateOption] <DiskCreateOptionTypes>] [-Linux]
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <StorageAccountTypes>]
 [-WriteAccelerator] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cdaa8-109">LinuxDiskEncryptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="cdaa8-109">LinuxDiskEncryptionParameterSet</span></span>
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-SourceImageUri] <String>] [[-CreateOption] <DiskCreateOptionTypes>] [-Linux]
 [-DiskEncryptionKeyUrl] <String> [-DiskEncryptionKeyVaultId] <String> [[-KeyEncryptionKeyUrl] <String>]
 [[-KeyEncryptionKeyVaultId] <String>] [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>]
 [-StorageAccountType <StorageAccountTypes>] [-WriteAccelerator] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cdaa8-110">Leírás</span><span class="sxs-lookup"><span data-stu-id="cdaa8-110">DESCRIPTION</span></span>
<span data-ttu-id="cdaa8-111">A **set-AzVMOSDisk** parancsmag egy virtuális gépen az operációs rendszer lemezének tulajdonságait állítja be.</span><span class="sxs-lookup"><span data-stu-id="cdaa8-111">The **Set-AzVMOSDisk** cmdlet sets the operating system disk properties on a virtual machine.</span></span>

## <span data-ttu-id="cdaa8-112">Példák</span><span class="sxs-lookup"><span data-stu-id="cdaa8-112">EXAMPLES</span></span>

### <span data-ttu-id="cdaa8-113">Példa 1: tulajdonságok beállítása virtuális gépen a platform képe</span><span class="sxs-lookup"><span data-stu-id="cdaa8-113">Example 1: Set properties on a virtual machine from platform image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet13" 
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> Set-AzVMOSDisk -VM $VirtualMachine -Name "OsDisk12" -VhdUri "os.vhd" -Caching ReadWrite
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Linux -ComputerName "MainComputer" -Credential (Get-Credential) 
PS C:\> $VirtualMachine = Set-AzVMSourceImage -VM $VirtualMachine -PublisherName "Canonical" -Offer "UbuntuServer" -Skus "15.10" -Version "latest" -Caching ReadWrite
PS C:\> $VirtualMachine = Set-AzVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -VhdUri "https://mystorageaccount.blob.core.windows.net/disks/" -CreateOption FromImage
PS C:> New-AzVM -VM $VirtualMachine -ResouceGroupName "ResourceGroup11"
```

<span data-ttu-id="cdaa8-114">Az első parancs beolvassa a AvailablitySet13 nevű ResourceGroup11 nevű erőforráscsoport elérhetőségi készletét, majd a $AvailabilitySet változóban tárolja az objektumot.</span><span class="sxs-lookup"><span data-stu-id="cdaa8-114">The first command gets the availability set named AvailablitySet13 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="cdaa8-115">A második parancs létrehoz egy Virtual Machine-objektumot, majd a $VirtualMachine változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="cdaa8-115">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="cdaa8-116">A parancs nevet és méretet rendel a virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="cdaa8-116">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="cdaa8-117">A virtuális gép a $AvailabilitySetban tárolt elérhetőségi készlethez tartozik.</span><span class="sxs-lookup"><span data-stu-id="cdaa8-117">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="cdaa8-118">A végleges parancs az $VirtualMachine virtuális gép tulajdonságait állítja be.</span><span class="sxs-lookup"><span data-stu-id="cdaa8-118">The final command sets the properties on the virtual machine in $VirtualMachine.</span></span>

### <span data-ttu-id="cdaa8-119">2. példa: a tulajdonságok megadása egy virtuális gépen általános felhasználó képe</span><span class="sxs-lookup"><span data-stu-id="cdaa8-119">Example 2: Sets properties on a virtual machine from generalized user image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet13" 
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1"
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Linux -ComputerName "MainComputer" -Credential (Get-Credential)
PS C:\> $VirtualMachine = Set-AzVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -SourceImageUri "https://mystorageaccount.blob.core.windows.net/vhds/myOSImage.vhd" -VhdUri "https://mystorageaccount.blob.core.windows.net/disks/" -CreateOption fromImage -Linux
PS C:> New-AzVM -VM $VirtualMachine -ResouceGroupName "ResourceGroup11"
```

<span data-ttu-id="cdaa8-120">Az első parancs a ResourceGroup11 nevű erőforráscsoport "AvailablitySet13" nevű adatkészletét kapja meg, és az adott objektumot a $AvailabilitySet változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="cdaa8-120">The first command gets the availability set named AvailablitySet13 in the resource group named ResourceGroup11 and stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="cdaa8-121">A második parancs létrehozza a virtuális gép objektumát, és a $VirtualMachine változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="cdaa8-121">The second command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="cdaa8-122">A parancs nevet és méretet rendel a virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="cdaa8-122">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="cdaa8-123">A virtuális gép a $AvailabilitySetban tárolt elérhetőségi készlethez tartozik.</span><span class="sxs-lookup"><span data-stu-id="cdaa8-123">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="cdaa8-124">A végleges parancs az $VirtualMachine virtuális gép tulajdonságait állítja be.</span><span class="sxs-lookup"><span data-stu-id="cdaa8-124">The final command sets the properties on the virtual machine in $VirtualMachine.</span></span>

### <span data-ttu-id="cdaa8-125">3. példa: a tulajdonságok megadása egy virtuális gépen speciális felhasználói képből</span><span class="sxs-lookup"><span data-stu-id="cdaa8-125">Example 3: Sets properties on a virtual machine from specialized user image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet13" 
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1"
PS C:\> $VirtualMachine = Set-AzVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -VhdUri "https://mystorageaccount.blob.core.windows.net/disks/" -CreateOption Attach -Linux
PS C:> New-AzVM -VM $VirtualMachine -ResouceGroupName "ResourceGroup11"
```

<span data-ttu-id="cdaa8-126">Az első parancs a ResourceGroup11 nevű erőforráscsoport "AvailablitySet13" nevű adatkészletét kapja meg, és az adott objektumot a $AvailabilitySet változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="cdaa8-126">The first command gets the availability set named AvailablitySet13 in the resource group named ResourceGroup11 and stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="cdaa8-127">A második parancs létrehozza a virtuális gép objektumát, és a $VirtualMachine változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="cdaa8-127">The second command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="cdaa8-128">A parancs nevet és méretet rendel a virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="cdaa8-128">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="cdaa8-129">A virtuális gép a $AvailabilitySetban tárolt elérhetőségi készlethez tartozik.</span><span class="sxs-lookup"><span data-stu-id="cdaa8-129">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="cdaa8-130">A végleges parancs az $VirtualMachine virtuális gép tulajdonságait állítja be.</span><span class="sxs-lookup"><span data-stu-id="cdaa8-130">The final command sets the properties on the virtual machine in $VirtualMachine.</span></span>

### <span data-ttu-id="cdaa8-131">4. példa: a lemezvezérlő-titkosítási beállítások beállítása a virtuális gép operációs rendszerének merevlemezén</span><span class="sxs-lookup"><span data-stu-id="cdaa8-131">Example 4: Set the disk encryption settings on a virtual machine operating system disk</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1"
PS C:> $VirtualMachine = Set-AzVMOSDisk -VM $VirtualMachine -Name "OsDisk12" -VhdUri "os.vhd" -Caching ReadWrite -Windows -CreateOption "Attach" -DiskEncryptionKeyUrl "https://mytestvault.vault.azure.net/secrets/Test1/514ceb769c984379a7e0230bddaaaaaa" -DiskEncryptionKeyVaultId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myresourcegroup/providers/Microsoft.KeyVault/vaults/mytestvault"
PS C:> New-AzVM -VM $VirtualMachine -ResouceGroupName " ResourceGroup11"
```

<span data-ttu-id="cdaa8-132">Ebben a példában a virtuális gép operációs rendszerének merevlemezén a lemez titkosítási beállításait adhatja meg.</span><span class="sxs-lookup"><span data-stu-id="cdaa8-132">This example sets the disk encryption settings on a virtual machine operating system disk.</span></span>

## <span data-ttu-id="cdaa8-133">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cdaa8-133">PARAMETERS</span></span>

### <span data-ttu-id="cdaa8-134">-Gyorsítótárazás</span><span class="sxs-lookup"><span data-stu-id="cdaa8-134">-Caching</span></span>
<span data-ttu-id="cdaa8-135">Az operációs rendszer lemezének gyorsítótárazási módját adja meg.</span><span class="sxs-lookup"><span data-stu-id="cdaa8-135">Specifies the caching mode of the operating system disk.</span></span>
<span data-ttu-id="cdaa8-136">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="cdaa8-136">Valid values are:</span></span> 

- <span data-ttu-id="cdaa8-137">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="cdaa8-137">ReadOnly</span></span>
- <span data-ttu-id="cdaa8-138">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="cdaa8-138">ReadWrite</span></span>

<span data-ttu-id="cdaa8-139">Az alapértelmezett érték a ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="cdaa8-139">The default value is ReadWrite.</span></span>
<span data-ttu-id="cdaa8-140">A gyorsítótárazási érték módosításakor a virtuális gép újraindul.</span><span class="sxs-lookup"><span data-stu-id="cdaa8-140">Changing the caching value causes the virtual machine to restart.</span></span>

<span data-ttu-id="cdaa8-141">Ez a beállítás hatással van a lemez teljesítményére.</span><span class="sxs-lookup"><span data-stu-id="cdaa8-141">This setting affects the performance of the disk.</span></span>

```yaml
Type: CachingTypes
Parameter Sets: (All)
Aliases: 
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdaa8-142">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="cdaa8-142">-CreateOption</span></span>
<span data-ttu-id="cdaa8-143">Itt adhatja meg, hogy a parancsmag létrehoz-e egy lemezt a virtuális gépen egy platformról vagy egy felhasználóról, vagy egy meglévő lemezt csatol a fájlhoz.</span><span class="sxs-lookup"><span data-stu-id="cdaa8-143">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, or attaches an existing disk.</span></span>
<span data-ttu-id="cdaa8-144">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="cdaa8-144">Valid values are:</span></span> 

- <span data-ttu-id="cdaa8-145">Csatolja.</span><span class="sxs-lookup"><span data-stu-id="cdaa8-145">Attach.</span></span>
<span data-ttu-id="cdaa8-146">Ezt a lehetőséget választva virtuális gépet hozhat létre egy speciális merevlemezről.</span><span class="sxs-lookup"><span data-stu-id="cdaa8-146">Specify this option to create a virtual machine from a specialized disk.</span></span>
<span data-ttu-id="cdaa8-147">Ha ezt a beállítást adja meg, ne adja meg a *SourceImageUri* paramétert.</span><span class="sxs-lookup"><span data-stu-id="cdaa8-147">When you specify this option, do not specify the *SourceImageUri* parameter.</span></span>
<span data-ttu-id="cdaa8-148">Ehelyett használja az Set-AzVMSourceImage parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="cdaa8-148">Instead, use the Set-AzVMSourceImage cmdlet.</span></span>
<span data-ttu-id="cdaa8-149">A azure2 platformot az operációs rendszernek a VHD-on használt típusának megadásához a *Windows* vagy a *Linux* paraméterekkel is el kell végeznie.</span><span class="sxs-lookup"><span data-stu-id="cdaa8-149">You must also use the use the *Windows* or *Linux* parameters to tell the azure2 platform the type of the operating system on the VHD.</span></span>
<span data-ttu-id="cdaa8-150">A *VhdUri* paraméter elég ahhoz, hogy a azure2 platform a csatolni kívánt lemez helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cdaa8-150">The *VhdUri* parameter is enough to tell the azure2 platform the location of the disk to attach.</span></span> 
- <span data-ttu-id="cdaa8-151">FromImage.</span><span class="sxs-lookup"><span data-stu-id="cdaa8-151">FromImage.</span></span>
<span data-ttu-id="cdaa8-152">Ezt a lehetőséget választva virtuális gépet hozhat létre platformról származó képből vagy általános felhasználói képből.</span><span class="sxs-lookup"><span data-stu-id="cdaa8-152">Specify this option to create a virtual machine from a platform image or a generalized user image.</span></span>
<span data-ttu-id="cdaa8-153">Általános felhasználói képek esetén a **set-AzVMSourceImage** parancsmag használata helyett meg kell adnia a *SourceImageUri* paramétert, illetve a *Windows* vagy a *Linux* paramétert is, amellyel az Azure platformot elmondhatja az operációs rendszer VHD-lemezének helye és típusa.</span><span class="sxs-lookup"><span data-stu-id="cdaa8-153">In the case of a generalized user image, you also need to specify the *SourceImageUri* parameter and either the *Windows* or *Linux* parameters to tell the Azure platform the location and type of the operating system disk VHD instead of using the **Set-AzVMSourceImage** cmdlet.</span></span>
<span data-ttu-id="cdaa8-154">Platform képe esetén a *VhdUri* paraméter elegendő.</span><span class="sxs-lookup"><span data-stu-id="cdaa8-154">In the case of a platform image, the *VhdUri* parameter is sufficient.</span></span> 
- <span data-ttu-id="cdaa8-155">Üres.</span><span class="sxs-lookup"><span data-stu-id="cdaa8-155">Empty.</span></span>

```yaml
Type: DiskCreateOptionTypes
Parameter Sets: (All)
Aliases: 
Accepted values: FromImage, Empty, Attach

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdaa8-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdaa8-156">-DefaultProfile</span></span>
<span data-ttu-id="cdaa8-157">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cdaa8-157">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cdaa8-158">-DiskEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="cdaa8-158">-DiskEncryptionKeyUrl</span></span>
<span data-ttu-id="cdaa8-159">A merevlemez titkosítási kulcsának helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cdaa8-159">Specifies the location of the disk encryption key.</span></span>

```yaml
Type: String
Parameter Sets: WindowsDiskEncryptionParameterSet, LinuxDiskEncryptionParameterSet
Aliases: 

Required: True
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdaa8-160">-DiskEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="cdaa8-160">-DiskEncryptionKeyVaultId</span></span>
<span data-ttu-id="cdaa8-161">A lemez titkosítási kulcsát tartalmazó kulcsfájl erőforrás-AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="cdaa8-161">Specifies the resource ID of the Key Vault containing the disk encryption key.</span></span>

```yaml
Type: String
Parameter Sets: WindowsDiskEncryptionParameterSet, LinuxDiskEncryptionParameterSet
Aliases: 

Required: True
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdaa8-162">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="cdaa8-162">-DiskSizeInGB</span></span>
<span data-ttu-id="cdaa8-163">Az operációs rendszer lemezének méretét adja meg GB-ban.</span><span class="sxs-lookup"><span data-stu-id="cdaa8-163">Specifies the size, in GB, of the operating system disk.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdaa8-164">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="cdaa8-164">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="cdaa8-165">A kulcs-titkosítási kulcs helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cdaa8-165">Specifies the location of the key encryption key.</span></span>

```yaml
Type: String
Parameter Sets: WindowsDiskEncryptionParameterSet, LinuxDiskEncryptionParameterSet
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdaa8-166">-KeyEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="cdaa8-166">-KeyEncryptionKeyVaultId</span></span>
<span data-ttu-id="cdaa8-167">A kulcs titkosítási kulcsát tartalmazó kulcsfájl erőforrás-AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="cdaa8-167">Specifies the resource ID of the Key Vault containing the key encryption key.</span></span>

```yaml
Type: String
Parameter Sets: WindowsDiskEncryptionParameterSet, LinuxDiskEncryptionParameterSet
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdaa8-168">-Linux</span><span class="sxs-lookup"><span data-stu-id="cdaa8-168">-Linux</span></span>
<span data-ttu-id="cdaa8-169">Azt jelzi, hogy az operációs rendszer a felhasználói képen a Linux.</span><span class="sxs-lookup"><span data-stu-id="cdaa8-169">Indicates that the operating system on the user image is Linux.</span></span>
<span data-ttu-id="cdaa8-170">Adja meg ezt a paramétert a felhasználó képalapú virtuálisgép-bevezetéséhez.</span><span class="sxs-lookup"><span data-stu-id="cdaa8-170">Specify this parameter for user image based virtual machine deployment.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: LinuxParamSet, LinuxDiskEncryptionParameterSet
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdaa8-171">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="cdaa8-171">-ManagedDiskId</span></span>
<span data-ttu-id="cdaa8-172">A felügyelt lemezek AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="cdaa8-172">Specifies the ID of a managed disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdaa8-173">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="cdaa8-173">-Name</span></span>
<span data-ttu-id="cdaa8-174">Az operációs rendszer lemezének nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cdaa8-174">Specifies the name of the operating system disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: OSDiskName, DiskName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdaa8-175">-SourceImageUri</span><span class="sxs-lookup"><span data-stu-id="cdaa8-175">-SourceImageUri</span></span>
<span data-ttu-id="cdaa8-176">A felhasználó képpontjának virtuális merevlemez-AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="cdaa8-176">Specifies the URI of the VHD for user image scenarios.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SourceImage

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdaa8-177">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="cdaa8-177">-StorageAccountType</span></span>
<span data-ttu-id="cdaa8-178">A felügyelt lemez tárterület-típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="cdaa8-178">Specifies the storage account type of managed disk.</span></span>

```yaml
Type: StorageAccountTypes
Parameter Sets: (All)
Aliases: 
Accepted values: StandardLRS, PremiumLRS

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdaa8-179">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="cdaa8-179">-VhdUri</span></span>
<span data-ttu-id="cdaa8-180">A virtuális merevlemez (VHD) egységes erőforrás-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="cdaa8-180">Specifies the Uniform Resource Identifier (URI) of a virtual hard disk (VHD).</span></span>

<span data-ttu-id="cdaa8-181">Képalapú virtuális gép esetén ez a paraméter azt a VHD-fájlt adja meg, amelyet a platform képe vagy a felhasználó képének megadásakor hozhat létre.</span><span class="sxs-lookup"><span data-stu-id="cdaa8-181">For an image based virtual machine, this parameter specifies the VHD file to create when a platform image or user image is specified.</span></span>
<span data-ttu-id="cdaa8-182">Az a hely, ahonnan a bináris nagy objektum (BLOB) másolódik a virtuális gép indításához.</span><span class="sxs-lookup"><span data-stu-id="cdaa8-182">This is the location from which the image binary large object (BLOB) is copied to start the virtual machine.</span></span>

<span data-ttu-id="cdaa8-183">A virtuális gép rendszerindítási forgatókönyve esetén ez a paraméter azt a VHD-fájlt adja meg, amelyet a virtuális gép közvetlenül használ a kezdéshez.</span><span class="sxs-lookup"><span data-stu-id="cdaa8-183">For a disk based virtual machine boot scenario, this parameter specifies the VHD file that the virtual machine uses directly for starting up.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: OSDiskVhdUri, DiskVhdUri

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdaa8-184">-VM</span><span class="sxs-lookup"><span data-stu-id="cdaa8-184">-VM</span></span>
<span data-ttu-id="cdaa8-185">Annak a helyi virtuális gépnek az objektumát adja meg, amelybe be szeretné állítani az operációs rendszer lemezének tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="cdaa8-185">Specifies the local virtual machine object on which to set operating system disk properties.</span></span>
<span data-ttu-id="cdaa8-186">A virtuálisgép-objektum beolvasásához használja az Get-AzVM parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="cdaa8-186">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cdaa8-187">-Windows</span><span class="sxs-lookup"><span data-stu-id="cdaa8-187">-Windows</span></span>
<span data-ttu-id="cdaa8-188">Azt jelzi, hogy a felhasználó Windows rendszerű operációs rendszere.</span><span class="sxs-lookup"><span data-stu-id="cdaa8-188">Indicates that the operating system on the user image is Windows.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: WindowsParamSet, WindowsDiskEncryptionParameterSet
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdaa8-189">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="cdaa8-189">-WriteAccelerator</span></span>
<span data-ttu-id="cdaa8-190">Megadja, hogy az operációs rendszer merevlemezén engedélyezni vagy tiltani kell-e a WriteAccelerator.</span><span class="sxs-lookup"><span data-stu-id="cdaa8-190">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdaa8-191">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdaa8-191">CommonParameters</span></span>
<span data-ttu-id="cdaa8-192">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cdaa8-192">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdaa8-193">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cdaa8-193">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdaa8-194">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cdaa8-194">INPUTS</span></span>

### <span data-ttu-id="cdaa8-195">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="cdaa8-195">PSVirtualMachine</span></span>
<span data-ttu-id="cdaa8-196">A ' VM ' paraméter elfogadja a "PSVirtualMachine" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="cdaa8-196">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="cdaa8-197">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cdaa8-197">OUTPUTS</span></span>

### <span data-ttu-id="cdaa8-198">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="cdaa8-198">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="cdaa8-199">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cdaa8-199">NOTES</span></span>

## <span data-ttu-id="cdaa8-200">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cdaa8-200">RELATED LINKS</span></span>

[<span data-ttu-id="cdaa8-201">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="cdaa8-201">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="cdaa8-202">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="cdaa8-202">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)

[<span data-ttu-id="cdaa8-203">Új – AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="cdaa8-203">New-AzVMConfig</span></span>](./New-AzVMConfig.md)


