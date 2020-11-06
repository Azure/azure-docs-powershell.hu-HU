---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 8F7AF1B8-D769-452C-92CF-4486C3EB894D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMOSDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMOSDisk.md
ms.openlocfilehash: dfcd408e3afa7988b06a1e020d76844c48d990b8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493176"
---
# <span data-ttu-id="02de7-101">Set-AzureRmVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="02de7-101">Set-AzureRmVMOSDisk</span></span>

## <span data-ttu-id="02de7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="02de7-102">SYNOPSIS</span></span>
<span data-ttu-id="02de7-103">Beállítja az operációs rendszer lemezének tulajdonságait egy virtuális gépen.</span><span class="sxs-lookup"><span data-stu-id="02de7-103">Sets the operating system disk properties on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="02de7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="02de7-104">SYNTAX</span></span>

### <span data-ttu-id="02de7-105">DefaultParamSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="02de7-105">DefaultParamSet (Default)</span></span>
```
Set-AzureRmVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-SourceImageUri] <String>] [-CreateOption] <DiskCreateOptionTypes>
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <StorageAccountTypes>]
 [<CommonParameters>]
```

### <span data-ttu-id="02de7-106">WindowsParamSet</span><span class="sxs-lookup"><span data-stu-id="02de7-106">WindowsParamSet</span></span>
```
Set-AzureRmVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-SourceImageUri] <String>] [-CreateOption] <DiskCreateOptionTypes> [-Windows]
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <StorageAccountTypes>]
 [<CommonParameters>]
```

### <span data-ttu-id="02de7-107">WindowsDiskEncryptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="02de7-107">WindowsDiskEncryptionParameterSet</span></span>
```
Set-AzureRmVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-SourceImageUri] <String>] [-CreateOption] <DiskCreateOptionTypes> [-Windows]
 [-DiskEncryptionKeyUrl] <String> [-DiskEncryptionKeyVaultId] <String> [[-KeyEncryptionKeyUrl] <String>]
 [[-KeyEncryptionKeyVaultId] <String>] [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>]
 [-StorageAccountType <StorageAccountTypes>] [<CommonParameters>]
```

### <span data-ttu-id="02de7-108">LinuxParamSet</span><span class="sxs-lookup"><span data-stu-id="02de7-108">LinuxParamSet</span></span>
```
Set-AzureRmVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-SourceImageUri] <String>] [-CreateOption] <DiskCreateOptionTypes> [-Linux]
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <StorageAccountTypes>]
 [<CommonParameters>]
```

### <span data-ttu-id="02de7-109">LinuxDiskEncryptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="02de7-109">LinuxDiskEncryptionParameterSet</span></span>
```
Set-AzureRmVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-SourceImageUri] <String>] [-CreateOption] <DiskCreateOptionTypes> [-Linux]
 [-DiskEncryptionKeyUrl] <String> [-DiskEncryptionKeyVaultId] <String> [[-KeyEncryptionKeyUrl] <String>]
 [[-KeyEncryptionKeyVaultId] <String>] [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>]
 [-StorageAccountType <StorageAccountTypes>] [<CommonParameters>]
```

## <span data-ttu-id="02de7-110">Leírás</span><span class="sxs-lookup"><span data-stu-id="02de7-110">DESCRIPTION</span></span>
<span data-ttu-id="02de7-111">A **set-AzureRmVMOSDisk** parancsmag egy virtuális gépen az operációs rendszer lemezének tulajdonságait állítja be.</span><span class="sxs-lookup"><span data-stu-id="02de7-111">The **Set-AzureRmVMOSDisk** cmdlet sets the operating system disk properties on a virtual machine.</span></span>

## <span data-ttu-id="02de7-112">Példák</span><span class="sxs-lookup"><span data-stu-id="02de7-112">EXAMPLES</span></span>

### <span data-ttu-id="02de7-113">Példa 1: tulajdonságok beállítása virtuális gépen a platform képe</span><span class="sxs-lookup"><span data-stu-id="02de7-113">Example 1: Set properties on a virtual machine from platform image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet13" 
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> Set-AzureRmVMOSDisk -VM $VirtualMachine -Name "OsDisk12" -VhdUri "os.vhd" -Caching ReadWrite
PS C:\> $VirtualMachine = Set-AzureRmVMOperatingSystem -VM $VirtualMachine -Linux -ComputerName "MainComputer" -Credential (Get-Credential) 
PS C:\> $VirtualMachine = Set-AzureRmVMSourceImage -VM $VirtualMachine -PublisherName "Canonical" -Offer "UbuntuServer" -Skus "15.10" -Version "latest" -Caching ReadWrite
PS C:\> $VirtualMachine = Set-AzureRmVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -VhdUri "https://mystorageaccount.blob.core.windows.net/disks/" -CreateOption FromImage
PS C:> New-AzureRmVM -VM $VirtualMachine -ResouceGroupName "ResourceGroup11"
```

<span data-ttu-id="02de7-114">Az első parancs beolvassa a AvailablitySet13 nevű ResourceGroup11 nevű erőforráscsoport elérhetőségi készletét, majd a $AvailabilitySet változóban tárolja az objektumot.</span><span class="sxs-lookup"><span data-stu-id="02de7-114">The first command gets the availability set named AvailablitySet13 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="02de7-115">A második parancs létrehoz egy Virtual Machine-objektumot, majd a $VirtualMachine változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="02de7-115">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="02de7-116">A parancs nevet és méretet rendel a virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="02de7-116">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="02de7-117">A virtuális gép a $AvailabilitySetban tárolt elérhetőségi készlethez tartozik.</span><span class="sxs-lookup"><span data-stu-id="02de7-117">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="02de7-118">A végleges parancs az $VirtualMachine virtuális gép tulajdonságait állítja be.</span><span class="sxs-lookup"><span data-stu-id="02de7-118">The final command sets the properties on the virtual machine in $VirtualMachine.</span></span>

### <span data-ttu-id="02de7-119">2. példa: a tulajdonságok megadása egy virtuális gépen általános felhasználó képe</span><span class="sxs-lookup"><span data-stu-id="02de7-119">Example 2: Sets properties on a virtual machine from generalized user image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet13" 
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1"
PS C:\> $VirtualMachine = Set-AzureRmVMOperatingSystem -VM $VirtualMachine -Linux -ComputerName "MainComputer" -Credential (Get-Credential)
PS C:\> $VirtualMachine = Set-AzureRmVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -SourceImageUri "https://mystorageaccount.blob.core.windows.net/vhds/myOSImage.vhd" -VhdUri "https://mystorageaccount.blob.core.windows.net/disks/" -CreateOption fromImage -Linux
PS C:> New-AzureRmVM -VM $VirtualMachine -ResouceGroupName "ResourceGroup11"
```

<span data-ttu-id="02de7-120">Az első parancs a ResourceGroup11 nevű erőforráscsoport "AvailablitySet13" nevű adatkészletét kapja meg, és az adott objektumot a $AvailabilitySet változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="02de7-120">The first command gets the availability set named AvailablitySet13 in the resource group named ResourceGroup11 and stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="02de7-121">A második parancs létrehozza a virtuális gép objektumát, és a $VirtualMachine változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="02de7-121">The second command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="02de7-122">A parancs nevet és méretet rendel a virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="02de7-122">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="02de7-123">A virtuális gép a $AvailabilitySetban tárolt elérhetőségi készlethez tartozik.</span><span class="sxs-lookup"><span data-stu-id="02de7-123">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="02de7-124">A végleges parancs az $VirtualMachine virtuális gép tulajdonságait állítja be.</span><span class="sxs-lookup"><span data-stu-id="02de7-124">The final command sets the properties on the virtual machine in $VirtualMachine.</span></span>

### <span data-ttu-id="02de7-125">3. példa: a tulajdonságok megadása egy virtuális gépen speciális felhasználói képből</span><span class="sxs-lookup"><span data-stu-id="02de7-125">Example 3: Sets properties on a virtual machine from specialized user image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet13" 
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1"
PS C:\> $VirtualMachine = Set-AzureRmVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -VhdUri "https://mystorageaccount.blob.core.windows.net/disks/" -CreateOption Attach -Linux
PS C:> New-AzureRmVM -VM $VirtualMachine -ResouceGroupName "ResourceGroup11"
```

<span data-ttu-id="02de7-126">Az első parancs a ResourceGroup11 nevű erőforráscsoport "AvailablitySet13" nevű adatkészletét kapja meg, és az adott objektumot a $AvailabilitySet változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="02de7-126">The first command gets the availability set named AvailablitySet13 in the resource group named ResourceGroup11 and stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="02de7-127">A második parancs létrehozza a virtuális gép objektumát, és a $VirtualMachine változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="02de7-127">The second command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="02de7-128">A parancs nevet és méretet rendel a virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="02de7-128">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="02de7-129">A virtuális gép a $AvailabilitySetban tárolt elérhetőségi készlethez tartozik.</span><span class="sxs-lookup"><span data-stu-id="02de7-129">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="02de7-130">A végleges parancs az $VirtualMachine virtuális gép tulajdonságait állítja be.</span><span class="sxs-lookup"><span data-stu-id="02de7-130">The final command sets the properties on the virtual machine in $VirtualMachine.</span></span>

### <span data-ttu-id="02de7-131">4. példa: a lemezvezérlő-titkosítási beállítások beállítása a virtuális gép operációs rendszerének merevlemezén</span><span class="sxs-lookup"><span data-stu-id="02de7-131">Example 4: Set the disk encryption settings on a virtual machine operating system disk</span></span>
```
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1"
PS C:> $VirtualMachine = Set-AzureRmVMOSDisk -VM $VirtualMachine -Name "OsDisk12" -VhdUri "os.vhd" -Caching ReadWrite -Windows -CreateOption "Attach" -DiskEncryptionKeyUrl "https://mytestvault.vault.azure.net/secrets/Test1/514ceb769c984379a7e0230bddaaaaaa" -DiskEncryptionKeyVaultId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myresourcegroup/providers/Microsoft.KeyVault/vaults/mytestvault"
PS C:> New-AzureRmVM -VM $VirtualMachine -ResouceGroupName " ResourceGroup11"
```

<span data-ttu-id="02de7-132">Ebben a példában a virtuális gép operációs rendszerének merevlemezén a lemez titkosítási beállításait adhatja meg.</span><span class="sxs-lookup"><span data-stu-id="02de7-132">This example sets the disk encryption settings on a virtual machine operating system disk.</span></span>

## <span data-ttu-id="02de7-133">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="02de7-133">PARAMETERS</span></span>

### <span data-ttu-id="02de7-134">-Gyorsítótárazás</span><span class="sxs-lookup"><span data-stu-id="02de7-134">-Caching</span></span>
<span data-ttu-id="02de7-135">Az operációs rendszer lemezének gyorsítótárazási módját adja meg.</span><span class="sxs-lookup"><span data-stu-id="02de7-135">Specifies the caching mode of the operating system disk.</span></span>
<span data-ttu-id="02de7-136">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="02de7-136">Valid values are:</span></span> 

- <span data-ttu-id="02de7-137">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="02de7-137">ReadOnly</span></span>
- <span data-ttu-id="02de7-138">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="02de7-138">ReadWrite</span></span>

<span data-ttu-id="02de7-139">Az alapértelmezett érték a ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="02de7-139">The default value is ReadWrite.</span></span>
<span data-ttu-id="02de7-140">A gyorsítótárazási érték módosításakor a virtuális gép újraindul.</span><span class="sxs-lookup"><span data-stu-id="02de7-140">Changing the caching value causes the virtual machine to restart.</span></span>

<span data-ttu-id="02de7-141">Ez a beállítás hatással van a lemez teljesítményére.</span><span class="sxs-lookup"><span data-stu-id="02de7-141">This setting affects the performance of the disk.</span></span>

```yaml
Type: CachingTypes
Parameter Sets: (All)
Aliases: 
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02de7-142">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="02de7-142">-CreateOption</span></span>
<span data-ttu-id="02de7-143">Itt adhatja meg, hogy a parancsmag létrehoz-e egy lemezt a virtuális gépen egy platformról vagy egy felhasználóról, vagy egy meglévő lemezt csatol a fájlhoz.</span><span class="sxs-lookup"><span data-stu-id="02de7-143">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, or attaches an existing disk.</span></span>
<span data-ttu-id="02de7-144">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="02de7-144">Valid values are:</span></span> 

- <span data-ttu-id="02de7-145">Csatolja.</span><span class="sxs-lookup"><span data-stu-id="02de7-145">Attach.</span></span>
<span data-ttu-id="02de7-146">Ezt a lehetőséget választva virtuális gépet hozhat létre egy speciális merevlemezről.</span><span class="sxs-lookup"><span data-stu-id="02de7-146">Specify this option to create a virtual machine from a specialized disk.</span></span>
<span data-ttu-id="02de7-147">Ha ezt a beállítást adja meg, ne adja meg a *SourceImageUri* paramétert.</span><span class="sxs-lookup"><span data-stu-id="02de7-147">When you specify this option, do not specify the *SourceImageUri* parameter.</span></span>
<span data-ttu-id="02de7-148">Ehelyett használja az Set-AzureRmVMSourceImage parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="02de7-148">Instead, use the Set-AzureRmVMSourceImage cmdlet.</span></span>
<span data-ttu-id="02de7-149">A azure2 platformot az operációs rendszernek a VHD-on használt típusának megadásához a *Windows* vagy a *Linux* paraméterekkel is el kell végeznie.</span><span class="sxs-lookup"><span data-stu-id="02de7-149">You must also use the use the *Windows* or *Linux* parameters to tell the azure2 platform the type of the operating system on the VHD.</span></span>
<span data-ttu-id="02de7-150">A *VhdUri* paraméter elég ahhoz, hogy a azure2 platform a csatolni kívánt lemez helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="02de7-150">The *VhdUri* parameter is enough to tell the azure2 platform the location of the disk to attach.</span></span> 
- <span data-ttu-id="02de7-151">FromImage.</span><span class="sxs-lookup"><span data-stu-id="02de7-151">FromImage.</span></span>
<span data-ttu-id="02de7-152">Ezt a lehetőséget választva virtuális gépet hozhat létre platformról származó képből vagy általános felhasználói képből.</span><span class="sxs-lookup"><span data-stu-id="02de7-152">Specify this option to create a virtual machine from a platform image or a generalized user image.</span></span>
<span data-ttu-id="02de7-153">Általános felhasználói képek esetén a **set-AzureRmVMSourceImage** parancsmag használata helyett meg kell adnia a *SourceImageUri* paramétert, illetve a *Windows* vagy a *Linux* paramétert is, amellyel az Azure platformot elmondhatja az operációs rendszer VHD-lemezének helye és típusa.</span><span class="sxs-lookup"><span data-stu-id="02de7-153">In the case of a generalized user image, you also need to specify the *SourceImageUri* parameter and either the *Windows* or *Linux* parameters to tell the Azure platform the location and type of the operating system disk VHD instead of using the **Set-AzureRmVMSourceImage** cmdlet.</span></span>
<span data-ttu-id="02de7-154">Platform képe esetén a *VhdUri* paraméter elegendő.</span><span class="sxs-lookup"><span data-stu-id="02de7-154">In the case of a platform image, the *VhdUri* parameter is sufficient.</span></span> 
- <span data-ttu-id="02de7-155">Üres.</span><span class="sxs-lookup"><span data-stu-id="02de7-155">Empty.</span></span>

```yaml
Type: DiskCreateOptionTypes
Parameter Sets: (All)
Aliases: 
Accepted values: FromImage, Empty, Attach

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02de7-156">-DiskEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="02de7-156">-DiskEncryptionKeyUrl</span></span>
<span data-ttu-id="02de7-157">A merevlemez titkosítási kulcsának helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="02de7-157">Specifies the location of the disk encryption key.</span></span>

```yaml
Type: String
Parameter Sets: WindowsDiskEncryptionParameterSet, LinuxDiskEncryptionParameterSet
Aliases: 

Required: True
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02de7-158">-DiskEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="02de7-158">-DiskEncryptionKeyVaultId</span></span>
<span data-ttu-id="02de7-159">A lemez titkosítási kulcsát tartalmazó kulcsfájl erőforrás-AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="02de7-159">Specifies the resource ID of the Key Vault containing the disk encryption key.</span></span>

```yaml
Type: String
Parameter Sets: WindowsDiskEncryptionParameterSet, LinuxDiskEncryptionParameterSet
Aliases: 

Required: True
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02de7-160">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="02de7-160">-DiskSizeInGB</span></span>
<span data-ttu-id="02de7-161">Az operációs rendszer lemezének méretét adja meg GB-ban.</span><span class="sxs-lookup"><span data-stu-id="02de7-161">Specifies the size, in GB, of the operating system disk.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02de7-162">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="02de7-162">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="02de7-163">A kulcs-titkosítási kulcs helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="02de7-163">Specifies the location of the key encryption key.</span></span>

```yaml
Type: String
Parameter Sets: WindowsDiskEncryptionParameterSet, LinuxDiskEncryptionParameterSet
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02de7-164">-KeyEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="02de7-164">-KeyEncryptionKeyVaultId</span></span>
<span data-ttu-id="02de7-165">A kulcs titkosítási kulcsát tartalmazó kulcsfájl erőforrás-AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="02de7-165">Specifies the resource ID of the Key Vault containing the key encryption key.</span></span>

```yaml
Type: String
Parameter Sets: WindowsDiskEncryptionParameterSet, LinuxDiskEncryptionParameterSet
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02de7-166">-Linux</span><span class="sxs-lookup"><span data-stu-id="02de7-166">-Linux</span></span>
<span data-ttu-id="02de7-167">Azt jelzi, hogy az operációs rendszer a felhasználói képen a Linux.</span><span class="sxs-lookup"><span data-stu-id="02de7-167">Indicates that the operating system on the user image is Linux.</span></span>
<span data-ttu-id="02de7-168">Adja meg ezt a paramétert a felhasználó képalapú virtuálisgép-bevezetéséhez.</span><span class="sxs-lookup"><span data-stu-id="02de7-168">Specify this parameter for user image based virtual machine deployment.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: LinuxParamSet, LinuxDiskEncryptionParameterSet
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02de7-169">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="02de7-169">-ManagedDiskId</span></span>
<span data-ttu-id="02de7-170">A felügyelt lemezek AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="02de7-170">Specifies the ID of a managed disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02de7-171">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="02de7-171">-Name</span></span>
<span data-ttu-id="02de7-172">Az operációs rendszer lemezének nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="02de7-172">Specifies the name of the operating system disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: OSDiskName, DiskName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02de7-173">-SourceImageUri</span><span class="sxs-lookup"><span data-stu-id="02de7-173">-SourceImageUri</span></span>
<span data-ttu-id="02de7-174">A felhasználó képpontjának virtuális merevlemez-AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="02de7-174">Specifies the URI of the VHD for user image scenarios.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SourceImage

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02de7-175">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="02de7-175">-StorageAccountType</span></span>
<span data-ttu-id="02de7-176">A felügyelt lemez tárterület-típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="02de7-176">Specifies the storage account type of managed disk.</span></span>

```yaml
Type: StorageAccountTypes
Parameter Sets: (All)
Aliases: 
Accepted values: StandardLRS, PremiumLRS

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02de7-177">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="02de7-177">-VhdUri</span></span>
<span data-ttu-id="02de7-178">A virtuális merevlemez (VHD) egységes erőforrás-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="02de7-178">Specifies the Uniform Resource Identifier (URI) of a virtual hard disk (VHD).</span></span>

<span data-ttu-id="02de7-179">Képalapú virtuális gép esetén ez a paraméter azt a VHD-fájlt adja meg, amelyet a platform képe vagy a felhasználó képének megadásakor hozhat létre.</span><span class="sxs-lookup"><span data-stu-id="02de7-179">For an image based virtual machine, this parameter specifies the VHD file to create when a platform image or user image is specified.</span></span>
<span data-ttu-id="02de7-180">Az a hely, ahonnan a bináris nagy objektum (BLOB) másolódik a virtuális gép indításához.</span><span class="sxs-lookup"><span data-stu-id="02de7-180">This is the location from which the image binary large object (BLOB) is copied to start the virtual machine.</span></span>

<span data-ttu-id="02de7-181">A virtuális gép rendszerindítási forgatókönyve esetén ez a paraméter azt a VHD-fájlt adja meg, amelyet a virtuális gép közvetlenül használ a kezdéshez.</span><span class="sxs-lookup"><span data-stu-id="02de7-181">For a disk based virtual machine boot scenario, this parameter specifies the VHD file that the virtual machine uses directly for starting up.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: OSDiskVhdUri, DiskVhdUri

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02de7-182">-VM</span><span class="sxs-lookup"><span data-stu-id="02de7-182">-VM</span></span>
<span data-ttu-id="02de7-183">Annak a helyi virtuális gépnek az objektumát adja meg, amelybe be szeretné állítani az operációs rendszer lemezének tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="02de7-183">Specifies the local virtual machine object on which to set operating system disk properties.</span></span>
<span data-ttu-id="02de7-184">A virtuálisgép-objektum beolvasásához használja az Get-AzureRmVM parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="02de7-184">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

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

### <span data-ttu-id="02de7-185">-Windows</span><span class="sxs-lookup"><span data-stu-id="02de7-185">-Windows</span></span>
<span data-ttu-id="02de7-186">Azt jelzi, hogy a felhasználó Windows rendszerű operációs rendszere.</span><span class="sxs-lookup"><span data-stu-id="02de7-186">Indicates that the operating system on the user image is Windows.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: WindowsParamSet, WindowsDiskEncryptionParameterSet
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02de7-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02de7-187">CommonParameters</span></span>
<span data-ttu-id="02de7-188">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="02de7-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02de7-189">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02de7-189">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02de7-190">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="02de7-190">INPUTS</span></span>

### <span data-ttu-id="02de7-191">Nincs</span><span class="sxs-lookup"><span data-stu-id="02de7-191">None</span></span>
<span data-ttu-id="02de7-192">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="02de7-192">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="02de7-193">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="02de7-193">OUTPUTS</span></span>

## <span data-ttu-id="02de7-194">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="02de7-194">NOTES</span></span>

## <span data-ttu-id="02de7-195">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="02de7-195">RELATED LINKS</span></span>

[<span data-ttu-id="02de7-196">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="02de7-196">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="02de7-197">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="02de7-197">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)

[<span data-ttu-id="02de7-198">Új – AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="02de7-198">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)


