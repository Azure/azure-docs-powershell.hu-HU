---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 8F7AF1B8-D769-452C-92CF-4486C3EB894D
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmosdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOSDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOSDisk.md
ms.openlocfilehash: 07d71e8fa7cd5c19cfc6f4aab8d27e5c5758b41c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101942697"
---
# Set-AzVMOSDisk

## SYNOPSIS
Beállítja az operációs rendszer lemeztulajdonságokat egy virtuális gépen.

## SZINTAXIS

### DefaultParamSet (alapértelmezett)
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-SourceImageUri] <String>] [[-CreateOption] <String>] [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>]
 [-StorageAccountType <String>] [-DiskEncryptionSetId <String>] [-WriteAccelerator] [-DiffDiskSetting <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### WindowsParamSet
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-SourceImageUri] <String>] [[-CreateOption] <String>] [-Windows] [-DiskSizeInGB <Int32>]
 [-ManagedDiskId <String>] [-StorageAccountType <String>] [-DiskEncryptionSetId <String>] [-WriteAccelerator]
 [-DiffDiskSetting <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### WindowsDiskEncryptionParameterSet
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-SourceImageUri] <String>] [[-CreateOption] <String>] [-Windows] [-DiskEncryptionKeyUrl] <String>
 [-DiskEncryptionKeyVaultId] <String> [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>]
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <String>]
 [-DiskEncryptionSetId <String>] [-WriteAccelerator] [-DiffDiskSetting <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### LinuxParamSet
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-SourceImageUri] <String>] [[-CreateOption] <String>] [-Linux] [-DiskSizeInGB <Int32>]
 [-ManagedDiskId <String>] [-StorageAccountType <String>] [-DiskEncryptionSetId <String>] [-WriteAccelerator]
 [-DiffDiskSetting <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### LinuxDiskEncryptionParameterSet
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-SourceImageUri] <String>] [[-CreateOption] <String>] [-Linux] [-DiskEncryptionKeyUrl] <String>
 [-DiskEncryptionKeyVaultId] <String> [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>]
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <String>]
 [-DiskEncryptionSetId <String>] [-WriteAccelerator] [-DiffDiskSetting <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## LEÍRÁS
A **Set-AzVMOSDisk** parancsmag beállítja az operációs rendszer lemeztulajdonságokat egy virtuális gépen.

## PÉLDÁK

### 1. példa: Tulajdonságok beállítása virtuális gépen platformképről
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet13" 
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> Set-AzVMOSDisk -VM $VirtualMachine -Name "OsDisk12" -VhdUri "os.vhd" -Caching ReadWrite
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Linux -ComputerName "MainComputer" -Credential (Get-Credential) 
PS C:\> $VirtualMachine = Set-AzVMSourceImage -VM $VirtualMachine -PublisherName "Canonical" -Offer "UbuntuServer" -Skus "15.10" -Version "latest" -Caching ReadWrite
PS C:\> $VirtualMachine = Set-AzVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -VhdUri "https://mystorageaccount.blob.core.windows.net/disks/" -CreateOption FromImage
PS C:> New-AzVM -VM $VirtualMachine -ResouceGroupName "ResourceGroup11"
```

Az első parancs az Erőforráscsoport11 erőforráscsoportBan az AvailabilitySet13 nevű elérhetőségi halmazt kapja, majd az objektumot a $AvailabilitySet tárolja.
A második parancs létrehoz egy virtuális gépobjektumot, majd a $VirtualMachine tárolja.
A parancs nevet és méretet rendel a virtuális géphez.
A virtuális gép a 2016-ban tárolt rendelkezésre állási $AvailabilitySet.
Az utolsó parancs beállítja a tulajdonságokat a virtuális gépen a $VirtualMachine.

### 2. példa: Tulajdonságokat állít be egy virtuális gépen általános felhasználói képből
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet13" 
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1"
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Linux -ComputerName "MainComputer" -Credential (Get-Credential)
PS C:\> $VirtualMachine = Set-AzVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -SourceImageUri "https://mystorageaccount.blob.core.windows.net/vhds/myOSImage.vhd" -VhdUri "https://mystorageaccount.blob.core.windows.net/disks/" -CreateOption fromImage -Linux
PS C:> New-AzVM -VM $VirtualMachine -ResouceGroupName "ResourceGroup11"
```

Az első parancs az Erőforráscsoport11 nevű erőforráscsoportBan az AvailabilitySet13 nevű elérhetőségi halmazt kapja, és az objektumot a $AvailabilitySet tárolja.
A második parancs létrehoz egy virtuális gépi objektumot, és azt a $VirtualMachine tárolja.
A parancs nevet és méretet rendel a virtuális géphez.
A virtuális gép a 2016-ban tárolt rendelkezésre állási $AvailabilitySet.
Az utolsó parancs beállítja a tulajdonságokat a virtuális gépen a $VirtualMachine.

### 3. példa: Egy virtuális gép tulajdonságainak beállítása speciális felhasználói kép alapján
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet13" 
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1"
PS C:\> $VirtualMachine = Set-AzVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -VhdUri "https://mystorageaccount.blob.core.windows.net/disks/" -CreateOption Attach -Linux
PS C:> New-AzVM -VM $VirtualMachine -ResouceGroupName "ResourceGroup11"
```

Az első parancs az Erőforráscsoport11 nevű erőforráscsoportBan az AvailabilitySet13 nevű elérhetőségi halmazt kapja, és az objektumot a $AvailabilitySet tárolja.
A második parancs létrehoz egy virtuális gépi objektumot, és azt a $VirtualMachine tárolja.
A parancs nevet és méretet rendel a virtuális géphez.
A virtuális gép a 2016-ban tárolt rendelkezésre állási $AvailabilitySet.
Az utolsó parancs beállítja a tulajdonságokat a virtuális gépen a $VirtualMachine.

### 4. példa: A lemeztitkosítási beállítások megadása virtuális gép operációs rendszer lemezén
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1"
PS C:> $VirtualMachine = Set-AzVMOSDisk -VM $VirtualMachine -Name "OsDisk12" -VhdUri "os.vhd" -Caching ReadWrite -Windows -CreateOption "Attach" -DiskEncryptionKeyUrl "https://mytestvault.vault.azure.net/secrets/Test1/514ceb769c984379a7e0230bddaaaaaa" -DiskEncryptionKeyVaultId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myresourcegroup/providers/Microsoft.KeyVault/vaults/mytestvault"
PS C:> New-AzVM -VM $VirtualMachine -ResouceGroupName " ResourceGroup11"
```

Ebben a példában egy virtuális gép operációs rendszer lemezén adhatja meg a lemeztitkosítási beállításokat.

## PARAMETERS

### -Gyorsítótárazás
Az operációs rendszer lemezének gyorsítótárazása.
Érvényes értékek: 
- ReadOnly
- ReadWrite The default value is ReadWrite.
A gyorsítótárazás értékének módosítása esetén a virtuális gép újraindul.
Ez a beállítás befolyásolja a lemez teljesítményét.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.CachingTypes]
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
Azt adja meg, hogy ez a parancsmag egy platformról vagy egy felhasználói képről hoz-e létre egy lemezt a virtuális gépben, vagy egy meglévő lemezt csatol.
Érvényes értékek: 
- Csatolás 2010.
Akkor válassza ezt a lehetőséget, ha egy speciális lemezről hoz létre virtuális gépet.
Ha ezt a beállítást adja meg, ne adja meg a *SourceImageUri paramétert.*
Ehelyett használja a Set-AzVMSourceImage parancsmagot.
A *Windows* vagy *a Linux* paramétereit használva is meg kell mondania az Azure platformnak a VHD operációs rendszer típusát.
A *VhdUri* paraméter elég ahhoz, hogy meg tudja mondani az azure platformnak a csatolható lemez helyét. 
- FromImage.
Ezzel a beállítással virtuális gépet hozhat létre platformképből vagy általánosított felhasználói képből.
Általánosított felhasználói lemezkép esetén a *SourceImageUri* paramétert és a *Windows* vagy *Linux* paramétereket is meg kell adnia ahhoz, hogy az Azure platformon a **Set-AzVMSourceImage** parancsmag használata helyett meg tudja mondani az operációs rendszer merevlemezének helyét és típusát.
Platformkép esetén a *VhdUri* paraméter elegendő. 
- Üres.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.

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

### -DiffDiskSetting
Az operációs rendszer lemezének eltérő lemezbeállításai.

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

### -DiskEncryptionKeyUrl
A lemeztitkosítási kulcs helyét határozza meg.

```yaml
Type: System.String
Parameter Sets: WindowsDiskEncryptionParameterSet, LinuxDiskEncryptionParameterSet
Aliases:

Required: True
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DiskEncryptionKeyVaultId
A lemeztitkosítási kulcsot tartalmazó kulcstár erőforrásazonosítóját adja meg.

```yaml
Type: System.String
Parameter Sets: WindowsDiskEncryptionParameterSet, LinuxDiskEncryptionParameterSet
Aliases:

Required: True
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DiskEncryptionSetId
Az ügyfél által felügyelt lemeztitkosítási készlet erőforrás-azonosítóját adja meg.  Ez csak felügyelt lemezhez lehet megadni.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DiskSizeInGB
Az operációs rendszer lemezének mérete GB-ban.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyEncryptionKeyUrl
A kulcstitkosítási kulcs helyét határozza meg.

```yaml
Type: System.String
Parameter Sets: WindowsDiskEncryptionParameterSet, LinuxDiskEncryptionParameterSet
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyEncryptionKeyVaultId
A kulcstitkosítási kulcsot tartalmazó kulcstár erőforrás-azonosítója.

```yaml
Type: System.String
Parameter Sets: WindowsDiskEncryptionParameterSet, LinuxDiskEncryptionParameterSet
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Linux
Azt jelzi, hogy a felhasználó képének operációs rendszere Linux.
Adja meg ezt a paramétert a felhasználói képalapú virtuális gép központi telepítéséhez.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: LinuxParamSet, LinuxDiskEncryptionParameterSet
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ManagedDiskId
Egy felügyelt lemez azonosítóját adja meg.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Az operációs rendszer lemezének nevét adja meg.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: OSDiskName, DiskName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceImageUri
A VHD URI azonosítóját adja meg a felhasználói képek esetében.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SourceImage

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageAccountType
A felügyelt lemez tárfióktípusát adja meg.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VhdUri
Egy virtuális merevlemez (VHD) egységes erőforrás-azonosítóját (URI) adja meg.
Képalapú virtuális gép esetén ez a paraméter azt a VHD-fájlt adja meg, amely platformkép vagy felhasználói kép megadása esetén hozható létre.
Ez az a hely, amelyből a rendszer a bináris nagy objektumot (BLOB) a virtuális gép indításaként másolja.
Lemezalapú virtuális gép rendszerindítási forgatókönyve esetén ez a paraméter azt a VHD-fájlt adja meg, amely a virtuális gép által közvetlenül az indításhoz használható.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: OSDiskVhdUri, DiskVhdUri

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VM
Megadja azt a helyi virtuális gépobjektumot, amelyen meg kell állítani az operációs rendszer lemeztulajdonságát.
Virtuális gépi objektum beszerzéséhez használja a Get-AzVM parancsmagot.

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Windows
Azt jelzi, hogy a felhasználói képen a Windows operációs rendszer látható.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WindowsParamSet, WindowsDiskEncryptionParameterSet
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WriteAccelerator
Azt adja meg, hogy a WriteAccelerator engedélyezve vagy letiltva legyen-e az operációs rendszer lemezén.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine

### System.String

## KIMENETEK

### Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzVM](./Get-AzVM.md)

[Get-AzAvailabilitySet](./Get-AzAvailabilitySet.md)

[New-AzVMConfig](./New-AzVMConfig.md)


