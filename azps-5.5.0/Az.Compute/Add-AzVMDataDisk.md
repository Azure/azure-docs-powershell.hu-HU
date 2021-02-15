---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 169E6694-82CD-4FCB-AB3D-E8A74001B8DB
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMDataDisk.md
ms.openlocfilehash: 29233b0bdce273205acffcb87dbf3a8adb1d4a52
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100166602"
---
# Add-AzVMDataDisk

## SYNOPSIS
Adatlemezt ad hozzá egy virtuális géphez.

## SZINTAXIS

### VmNormalDiskParameterSetName (alapértelmezett)
```
Add-AzVMDataDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-Lun] <Int32> [-CreateOption] <String> [[-SourceImageUri] <String>]
 [-DiskEncryptionSetId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### VmManagedDiskParameterSetName
```
Add-AzVMDataDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-Lun] <Int32> [-CreateOption] <String> [[-ManagedDiskId] <String>]
 [[-StorageAccountType] <String>] [-DiskEncryptionSetId <String>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## LEÍRÁS
Az **Add-AzVMDataDisk** parancsmag hozzáad egy adatlemezt egy virtuális géphez.
Adatlemezt hozzáadhat virtuális gép létrehozásakor, vagy hozzáadhat egy adatlemezt egy meglévő virtuális géphez.

## PÉLDÁK

### 1. példa: Adatlemezek hozzáadása új virtuális géphez
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataDiskVhdUri01 = "https://contoso.blob.core.windows.net/test/data1.vhd"
PS C:\> $DataDiskVhdUri02 = "https://contoso.blob.core.windows.net/test/data2.vhd"
PS C:\> $DataDiskVhdUri03 = "https://contoso.blob.core.windows.net/test/data3.vhd"
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name 'DataDisk1' -Caching 'ReadOnly' -DiskSizeInGB 10 -Lun 0 -VhdUri $DataDiskVhdUri01 -CreateOption Empty
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name 'DataDisk2' -Caching 'ReadOnly' -DiskSizeInGB 11 -Lun 1 -VhdUri $DataDiskVhdUri02 -CreateOption Empty
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name 'DataDisk3' -Caching 'ReadOnly' -DiskSizeInGB 12 -Lun 2 -VhdUri $DataDiskVhdUri03 -CreateOption Empty
```

Az első parancs létrehoz egy virtuális gépi objektumot, majd tárolja azt a $VirtualMachine változóban.
A parancs nevet és méretet rendel a virtuális géphez.
A következő három parancs három adatlemez elérési útját rendeli hozzá a $DataDiskVhdUri 01, $DataDiskVhdUri 02 és $DataDiskVhdUri 03 változókhoz.
Ez a módszer csak az alábbi parancsok olvashatóságát közelíti meg.
Az utolsó három parancs egy-egy adatlemezt ad hozzá a $VirtualMachine.
A parancs megadja a lemez nevét és helyét, valamint a lemez egyéb tulajdonságait.
Az egyes lemezeket a $DataDiskVhdUri 01, a $DataDiskVhdUri 02 és a $DataDiskVhdUri 03 tárolja.

### 2. példa: Adatlemez hozzáadása meglévő virtuális géphez
```
PS C:\> $VirtualMachine = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> Add-AzVMDataDisk -VM $VirtualMachine -Name "disk1" -VhdUri "https://contoso.blob.core.windows.net/vhds/diskstandard03.vhd" -LUN 0 -Caching ReadOnly -DiskSizeinGB 1 -CreateOption Empty
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

Az első parancs a VirtualMachine07 nevű virtuális gépet kapja meg [a Get-AzVM parancsmag](./Get-AzVM.md) használatával.
A parancs a virtuális gépet a $VirtualMachine tárolja.
A második parancs hozzáad egy adatlemezt a $VirtualMachine.
Az utolsó parancs frissíti a ResourceGroup11-ben $VirtualMachine virtuális gép állapotát.

### 3. példa: Adatlemez hozzáadása egy új virtuális géphez egy általánosított felhasználói képből
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataImageUri = "https://contoso.blob.core.windows.net/system/Microsoft.Compute/Images/captured/dataimage.vhd"
PS C:\> $DataDiskUri = "https://contoso.blob.core.windows.net/test/datadisk.vhd"
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name "disk1" -SourceImageUri $DataImageUri -VhdUri $DataDiskUri -Lun 0 -DiskSizeinGB 10 -CreateOption FromImage
```

Az első parancs létrehoz egy virtuális gépi objektumot, és azt a $VirtualMachine tárolja.
A parancs nevet és méretet rendel a virtuális géphez.
A következő két parancs az adatkép és az adatlemezek elérési útját rendeli a $DataImageUri és $DataDiskUri változókhoz.
Ez a módszer az alábbi parancsok olvashatóságának javítására használható.
Az utolsó parancsok hozzáadnak egy adatlemezt a $VirtualMachine.
A parancs megadja a lemez nevét és helyét, valamint a lemez egyéb tulajdonságait.

### 4. példa: Adatlemezek hozzáadása új virtuális géphez egy speciális felhasználói képből
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataDiskUri = "https://contoso.blob.core.windows.net/test/datadisk.vhd"
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name "dd1" -VhdUri $DataDiskUri -Lun 0 -DiskSizeinGB 10 -CreateOption Attach
```

Az első parancs létrehoz egy virtuális gépi objektumot, és azt a $VirtualMachine tárolja.
A parancs nevet és méretet rendel a virtuális géphez.
A következő parancsok az adatlemez elérési útját rendelik a $DataDiskUri változóhoz.
Ez a módszer az alábbi parancsok olvashatóságának javítására használható.
Az utolsó parancs egy adatlemezt ad hozzá a $VirtualMachine.
A parancs megadja a lemez nevét és helyét, valamint a lemez egyéb tulajdonságait.

## PARAMETERS

### -Gyorsítótárazás
A lemez gyorsítótárazása.
A paraméter elfogadható értékei a következőek:
- ReadOnly
- ReadWrite
- Nincs az alapértelmezett érték a Beolvasott érték.
Ha módosítja ezt az értéket, a virtuális gép újraindul.
Ez a beállítás befolyásolja a lemez konzisztenciáját és teljesítményét.

```yaml
Type: Microsoft.Azure.Management.Compute.Models.CachingTypes
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CreateOption
Azt adja meg, hogy a parancsmag létrehoz-e egy lemezt a virtuális gépben egy platformról vagy egy felhasználói képről, létrehoz-e egy üres lemezt, vagy csatol-e egy meglévő lemezt.
A paraméter elfogadható értékei a következőek:
- Csatolás 2010.
Akkor válassza ezt a lehetőséget, ha egy speciális lemezről hoz létre virtuális gépet.
Ha ezt a beállítást adja meg, ne adja meg a *SourceImageUri paramétert.*
A *VhdUri* szükséges ahhoz, hogy az Azure platformnak meg tudja mondani a virtuális merevlemez (VHD) helyét, hogy adatlemezként csatolja a virtuális géphez.
- Üres.
Ezt megadásával üres adatlemezt hozhat létre.
- FromImage.
Akkor válassza ezt a lehetőséget, ha általánosított képből vagy lemezről hoz létre virtuális gépet.
Ha megadja ezt a beállítást, a *SourceImageUri* paramétert is meg kell adnia ahhoz, hogy az Azure-platformnak meg tudja határozni a VHD adatlemezként csatolható helyét.
A *VhdUri* paraméter a virtuális gép által használt adatlemez helyét határozza meg.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Egy virtuális géphez csatolni kívánt üres lemez gigabájtban megadott mérete.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Lun
Egy adatlemez logikai egységszámát (LUN) adja meg.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ManagedDiskId
Egy felügyelt lemez azonosítóját adja meg.

```yaml
Type: System.String
Parameter Sets: VmManagedDiskParameterSetName
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
A hozzáadni szükséges adatlemez nevét adja meg.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SourceImageUri
Annak a lemeznek az URI-ját adja meg, amelyhez a parancsmag csatolja.

```yaml
Type: System.String
Parameter Sets: VmNormalDiskParameterSetName
Aliases: SourceImage

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageAccountType
A felügyelt lemez tárfióktípusát adja meg.

```yaml
Type: System.String
Parameter Sets: VmManagedDiskParameterSetName
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VhdUri
Megadja a virtuális merevlemez-fájl (VHD) egységes erőforrás-azonosítóját (URI), amely platformkép vagy felhasználói kép használata esetén hozható létre.
Ez a parancsmag a kép bináris nagy objektumát (blobját) másolja erre a helyre.
Ez az a hely, ahol elindítja a virtuális gépet.

```yaml
Type: System.String
Parameter Sets: VmNormalDiskParameterSetName
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VM
Azt a helyi virtuális gépobjektumot adja meg, amelyhez adatlemezt szeretne hozzáadni.
A **Get-AzVM parancsmag** használatával virtuális gépi objektumot szerezhet be.
A **New-AzVMConfig** parancsmaggal virtuális gépi objektumot hozhat létre.

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -WriteAccelerator
Azt adja meg, hogy a WriteAccelerator engedélyezve vagy letiltva legyen-e felügyelt adatlemezen.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: VmManagedDiskParameterSetName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine

### System.String

### Microsoft.Azure.Management.Compute.Models.CachingTypes

### System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]

## KIMENETEK

### Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine

### Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Remove-AzVMDataDisk](./Remove-AzVMDataDisk.md)

[Get-AzVM](./Get-AzVM.md)

[New-AzVMConfig](./New-AzVMConfig.md)
