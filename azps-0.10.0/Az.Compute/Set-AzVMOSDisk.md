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
# Set-AzVMOSDisk

## Áttekintés
Beállítja az operációs rendszer lemezének tulajdonságait egy virtuális gépen.

## SZINTAXISA

### DefaultParamSet (alapértelmezett)
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-SourceImageUri] <String>] [[-CreateOption] <DiskCreateOptionTypes>]
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <StorageAccountTypes>]
 [-WriteAccelerator] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### WindowsParamSet
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-SourceImageUri] <String>] [[-CreateOption] <DiskCreateOptionTypes>] [-Windows]
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <StorageAccountTypes>]
 [-WriteAccelerator] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### WindowsDiskEncryptionParameterSet
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-SourceImageUri] <String>] [[-CreateOption] <DiskCreateOptionTypes>] [-Windows]
 [-DiskEncryptionKeyUrl] <String> [-DiskEncryptionKeyVaultId] <String> [[-KeyEncryptionKeyUrl] <String>]
 [[-KeyEncryptionKeyVaultId] <String>] [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>]
 [-StorageAccountType <StorageAccountTypes>] [-WriteAccelerator] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### LinuxParamSet
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-SourceImageUri] <String>] [[-CreateOption] <DiskCreateOptionTypes>] [-Linux]
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <StorageAccountTypes>]
 [-WriteAccelerator] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### LinuxDiskEncryptionParameterSet
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-SourceImageUri] <String>] [[-CreateOption] <DiskCreateOptionTypes>] [-Linux]
 [-DiskEncryptionKeyUrl] <String> [-DiskEncryptionKeyVaultId] <String> [[-KeyEncryptionKeyUrl] <String>]
 [[-KeyEncryptionKeyVaultId] <String>] [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>]
 [-StorageAccountType <StorageAccountTypes>] [-WriteAccelerator] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Leírás
A **set-AzVMOSDisk** parancsmag egy virtuális gépen az operációs rendszer lemezének tulajdonságait állítja be.

## Példák

### Példa 1: tulajdonságok beállítása virtuális gépen a platform képe
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet13" 
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> Set-AzVMOSDisk -VM $VirtualMachine -Name "OsDisk12" -VhdUri "os.vhd" -Caching ReadWrite
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Linux -ComputerName "MainComputer" -Credential (Get-Credential) 
PS C:\> $VirtualMachine = Set-AzVMSourceImage -VM $VirtualMachine -PublisherName "Canonical" -Offer "UbuntuServer" -Skus "15.10" -Version "latest" -Caching ReadWrite
PS C:\> $VirtualMachine = Set-AzVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -VhdUri "https://mystorageaccount.blob.core.windows.net/disks/" -CreateOption FromImage
PS C:> New-AzVM -VM $VirtualMachine -ResouceGroupName "ResourceGroup11"
```

Az első parancs beolvassa a AvailablitySet13 nevű ResourceGroup11 nevű erőforráscsoport elérhetőségi készletét, majd a $AvailabilitySet változóban tárolja az objektumot.
A második parancs létrehoz egy Virtual Machine-objektumot, majd a $VirtualMachine változóban tárolja.
A parancs nevet és méretet rendel a virtuális géphez.
A virtuális gép a $AvailabilitySetban tárolt elérhetőségi készlethez tartozik.
A végleges parancs az $VirtualMachine virtuális gép tulajdonságait állítja be.

### 2. példa: a tulajdonságok megadása egy virtuális gépen általános felhasználó képe
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet13" 
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1"
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Linux -ComputerName "MainComputer" -Credential (Get-Credential)
PS C:\> $VirtualMachine = Set-AzVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -SourceImageUri "https://mystorageaccount.blob.core.windows.net/vhds/myOSImage.vhd" -VhdUri "https://mystorageaccount.blob.core.windows.net/disks/" -CreateOption fromImage -Linux
PS C:> New-AzVM -VM $VirtualMachine -ResouceGroupName "ResourceGroup11"
```

Az első parancs a ResourceGroup11 nevű erőforráscsoport "AvailablitySet13" nevű adatkészletét kapja meg, és az adott objektumot a $AvailabilitySet változóban tárolja.
A második parancs létrehozza a virtuális gép objektumát, és a $VirtualMachine változóban tárolja.
A parancs nevet és méretet rendel a virtuális géphez.
A virtuális gép a $AvailabilitySetban tárolt elérhetőségi készlethez tartozik.
A végleges parancs az $VirtualMachine virtuális gép tulajdonságait állítja be.

### 3. példa: a tulajdonságok megadása egy virtuális gépen speciális felhasználói képből
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet13" 
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1"
PS C:\> $VirtualMachine = Set-AzVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -VhdUri "https://mystorageaccount.blob.core.windows.net/disks/" -CreateOption Attach -Linux
PS C:> New-AzVM -VM $VirtualMachine -ResouceGroupName "ResourceGroup11"
```

Az első parancs a ResourceGroup11 nevű erőforráscsoport "AvailablitySet13" nevű adatkészletét kapja meg, és az adott objektumot a $AvailabilitySet változóban tárolja.
A második parancs létrehozza a virtuális gép objektumát, és a $VirtualMachine változóban tárolja.
A parancs nevet és méretet rendel a virtuális géphez.
A virtuális gép a $AvailabilitySetban tárolt elérhetőségi készlethez tartozik.
A végleges parancs az $VirtualMachine virtuális gép tulajdonságait állítja be.

### 4. példa: a lemezvezérlő-titkosítási beállítások beállítása a virtuális gép operációs rendszerének merevlemezén
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1"
PS C:> $VirtualMachine = Set-AzVMOSDisk -VM $VirtualMachine -Name "OsDisk12" -VhdUri "os.vhd" -Caching ReadWrite -Windows -CreateOption "Attach" -DiskEncryptionKeyUrl "https://mytestvault.vault.azure.net/secrets/Test1/514ceb769c984379a7e0230bddaaaaaa" -DiskEncryptionKeyVaultId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myresourcegroup/providers/Microsoft.KeyVault/vaults/mytestvault"
PS C:> New-AzVM -VM $VirtualMachine -ResouceGroupName " ResourceGroup11"
```

Ebben a példában a virtuális gép operációs rendszerének merevlemezén a lemez titkosítási beállításait adhatja meg.

## PARAMÉTEREK

### -Gyorsítótárazás
Az operációs rendszer lemezének gyorsítótárazási módját adja meg.
Az érvényes értékek a következők: 

- ReadOnly
- ReadWrite

Az alapértelmezett érték a ReadWrite.
A gyorsítótárazási érték módosításakor a virtuális gép újraindul.

Ez a beállítás hatással van a lemez teljesítményére.

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

### -CreateOption
Itt adhatja meg, hogy a parancsmag létrehoz-e egy lemezt a virtuális gépen egy platformról vagy egy felhasználóról, vagy egy meglévő lemezt csatol a fájlhoz.
Az érvényes értékek a következők: 

- Csatolja.
Ezt a lehetőséget választva virtuális gépet hozhat létre egy speciális merevlemezről.
Ha ezt a beállítást adja meg, ne adja meg a *SourceImageUri* paramétert.
Ehelyett használja az Set-AzVMSourceImage parancsmagot.
A azure2 platformot az operációs rendszernek a VHD-on használt típusának megadásához a *Windows* vagy a *Linux* paraméterekkel is el kell végeznie.
A *VhdUri* paraméter elég ahhoz, hogy a azure2 platform a csatolni kívánt lemez helyét adja meg. 
- FromImage.
Ezt a lehetőséget választva virtuális gépet hozhat létre platformról származó képből vagy általános felhasználói képből.
Általános felhasználói képek esetén a **set-AzVMSourceImage** parancsmag használata helyett meg kell adnia a *SourceImageUri* paramétert, illetve a *Windows* vagy a *Linux* paramétert is, amellyel az Azure platformot elmondhatja az operációs rendszer VHD-lemezének helye és típusa.
Platform képe esetén a *VhdUri* paraméter elegendő. 
- Üres.

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

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

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

### -DiskEncryptionKeyUrl
A merevlemez titkosítási kulcsának helyét adja meg.

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

### -DiskEncryptionKeyVaultId
A lemez titkosítási kulcsát tartalmazó kulcsfájl erőforrás-AZONOSÍTÓját adja meg.

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

### -DiskSizeInGB
Az operációs rendszer lemezének méretét adja meg GB-ban.

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

### -KeyEncryptionKeyUrl
A kulcs-titkosítási kulcs helyét adja meg.

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

### -KeyEncryptionKeyVaultId
A kulcs titkosítási kulcsát tartalmazó kulcsfájl erőforrás-AZONOSÍTÓját adja meg.

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

### -Linux
Azt jelzi, hogy az operációs rendszer a felhasználói képen a Linux.
Adja meg ezt a paramétert a felhasználó képalapú virtuálisgép-bevezetéséhez.

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

### -ManagedDiskId
A felügyelt lemezek AZONOSÍTÓját adja meg.

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

### -Name (név)
Az operációs rendszer lemezének nevét adja meg.

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

### -SourceImageUri
A felhasználó képpontjának virtuális merevlemez-AZONOSÍTÓját adja meg.

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

### -StorageAccountType
A felügyelt lemez tárterület-típusát adja meg.

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

### -VhdUri
A virtuális merevlemez (VHD) egységes erőforrás-azonosítóját adja meg.

Képalapú virtuális gép esetén ez a paraméter azt a VHD-fájlt adja meg, amelyet a platform képe vagy a felhasználó képének megadásakor hozhat létre.
Az a hely, ahonnan a bináris nagy objektum (BLOB) másolódik a virtuális gép indításához.

A virtuális gép rendszerindítási forgatókönyve esetén ez a paraméter azt a VHD-fájlt adja meg, amelyet a virtuális gép közvetlenül használ a kezdéshez.

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

### -VM
Annak a helyi virtuális gépnek az objektumát adja meg, amelybe be szeretné állítani az operációs rendszer lemezének tulajdonságait.
A virtuálisgép-objektum beolvasásához használja az Get-AzVM parancsmagot.

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

### -Windows
Azt jelzi, hogy a felhasználó Windows rendszerű operációs rendszere.

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

### -WriteAccelerator
Megadja, hogy az operációs rendszer merevlemezén engedélyezni vagy tiltani kell-e a WriteAccelerator.

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

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### PSVirtualMachine
A ' VM ' paraméter elfogadja a "PSVirtualMachine" típusú értéket a csővezetékről

## KIMENETEK

### Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachine

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzVM](./Get-AzVM.md)

[Get-AzAvailabilitySet](./Get-AzAvailabilitySet.md)

[Új – AzVMConfig](./New-AzVMConfig.md)


