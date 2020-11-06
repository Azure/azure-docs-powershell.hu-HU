---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 169E6694-82CD-4FCB-AB3D-E8A74001B8DB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVMDataDisk.md
ms.openlocfilehash: 60b8d396f981b8f22421d8994ceb085cbc7b9a70
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505203"
---
# Add-AzureRmVMDataDisk

## Áttekintés
Adatlemez felvétele virtuális gépre.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Add-AzureRmVMDataDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-DiskSizeInGB] <Int32>] [-Lun] <Int32> [-CreateOption] <DiskCreateOptionTypes>
 [[-SourceImageUri] <String>] [[-ManagedDiskId] <String>] [[-StorageAccountType] <StorageAccountTypes>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
Az **Add-AzureRmVMDataDisk** parancsmag adatlemezt ad hozzá egy virtuális géphez.
A virtuális gép létrehozásakor adatlemezt vehet fel, vagy egy meglévő virtuális géphez is hozzáadhat egy adatlemezt.

## Példák

### 1. példa: adatlemezek hozzáadása új virtuális géphez
```
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataDiskVhdUri01 = "https://contoso.blob.core.windows.net/test/data1.vhd"
PS C:\> $DataDiskVhdUri02 = "https://contoso.blob.core.windows.net/test/data2.vhd"
PS C:\> $DataDiskVhdUri03 = "https://contoso.blob.core.windows.net/test/data3.vhd"
PS C:\> $VirtualMachine = Add-AzureRmVMDataDisk -VM $VirtualMachine -Name 'DataDisk1' -Caching 'ReadOnly' -DiskSizeInGB 10 -Lun 0 -VhdUri $DataDiskVhdUri01 -CreateOption Empty
PS C:\> $VirtualMachine = Add-AzureRmVMDataDisk -VM $VirtualMachine -Name 'DataDisk2' -Caching 'ReadOnly' -DiskSizeInGB 11 -Lun 1 -VhdUri $DataDiskVhdUri02 -CreateOption Empty
PS C:\> $VirtualMachine = Add-AzureRmVMDataDisk -VM $VirtualMachine -Name 'DataDisk3' -Caching 'ReadOnly' -DiskSizeInGB 12 -Lun 2 -VhdUri $DataDiskVhdUri03 -CreateOption Empty
```

Az első parancs létrehoz egy virtuálisgép-objektumot, majd a $VirtualMachine változóban tárolja.
A parancs nevet és méretet rendel a virtuális géphez.

A következő három parancs három adatlemez elérési útját rendeli hozzá a $DataDiskVhdUri 01, $DataDiskVhdUri 02 és $DataDiskVhdUri 03 változóhoz.
Ez a megközelítés csak az alábbi parancsok olvashatóságát szolgálhatja.

Az utolsó három parancs minden olyan adatlemezt ad az $VirtualMachine-ban tárolt virtuális géphez.
A parancs a lemez nevét és helyét, valamint a lemez egyéb tulajdonságait adja meg.
Az egyes lemezek URI-ja $DataDiskVhdUri 01, $DataDiskVhdUri 02 és $DataDiskVhdUri 03-es verzióban van tárolva.

### 2. példa: adatlemez hozzáadása meglévő virtuális géphez
```
PS C:\> $VirtualMachine = Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> Add-AzureRmVMDataDisk -VM $VirtualMachine -Name "disk1" -VhdUri "https://contoso.blob.core.windows.net/vhds/diskstandard03.vhd" -LUN 0 -Caching ReadOnly -DiskSizeinGB 1 -CreateOption Empty
PS C:\> Update-AzureRmVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

Az első parancs a [Get-AzureRmVM](./Get-AzureRmVM.md) parancsmag használatával kapja meg a VirtualMachine07 nevű virtuális gépet.
A parancs a virtuális gépet a $VirtualMachine változóban tárolja.

A második parancs adatlemezt ad az $VirtualMachine-ban tárolt virtuális géphez.

A végleges parancs frissíti a $VirtualMachineban tárolt virtuális gép állapotát a ResourceGroup11-ban.

### 3. példa: adatlemez hozzáadása egy új virtuális géphez egy általános felhasználói képből
```
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataImageUri = "https://contoso.blob.core.windows.net/system/Microsoft.Compute/Images/captured/dataimage.vhd"
PS C:\> $DataDiskUri = "https://contoso.blob.core.windows.net/test/datadisk.vhd"
PS C:\> $VirtualMachine = Add-AzureRmVMDataDisk -VM $VirtualMachine -Name "disk1" -SourceImageUri $DataImageUri -VhdUri $DataDiskUri -Lun 0 -DiskSizeinGB 10 -CreateOption FromImage
```

Az első parancs létrehozza a virtuális gép objektumát, és a $VirtualMachine változóban tárolja.
A parancs nevet és méretet rendel a virtuális géphez.

A következő két parancs az Adatkép és az adatlemezek elérési útját rendeli az $DataImageUrihez, és $DataDiskUri változókat.
Ezzel a megközelítéssel javíthatja az alábbi parancsok olvashatóságát.

A végleges parancsok felveszi az adatlemezt a $VirtualMachineban tárolt virtuális géphez.
A parancs a lemez fájlnevét és helyét, valamint a lemez egyéb tulajdonságait adja meg.

### 4. példa: adatlemezek hozzáadása egy új virtuális géphez egy speciális felhasználói képből
```
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataDiskUri = "https://contoso.blob.core.windows.net/test/datadisk.vhd"
PS C:\> $VirtualMachine = Add-AzureRmVMDataDisk -VM $VirtualMachine -Name "dd1" -VhdUri $DataDiskUri -Lun 0 -DiskSizeinGB 10 -CreateOption Attach
```

Az első parancs létrehozza a virtuális gép objektumát, és a $VirtualMachine változóban tárolja.
A parancs nevet és méretet rendel a virtuális géphez.

A következő parancsok az adatlemez elérési útját a $DataDiskUri változóhoz rendelik.
Ezzel a megközelítéssel javíthatja az alábbi parancsok olvashatóságát.

A végleges parancs adatlemezt hoz létre a $VirtualMachine tárolt virtuális géphez.
A parancs a lemez nevét és helyét, valamint a lemez egyéb tulajdonságait adja meg.

## PARAMÉTEREK

### -Gyorsítótárazás
A lemez gyorsítótárazási módját adja meg.
A paraméter elfogadható értékei a következők:

- ReadOnly
- ReadWrite
- Nincs

Az alapértelmezett érték a ReadWrite.
Az érték módosításakor a virtuális gép újraindul.

Ez a beállítás befolyásolja a lemez egységességét és teljesítményét.

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
Itt adhatja meg, hogy a parancsmag létrehoz-e egy lemezt a virtuális gépen egy platformról vagy egy felhasználói képből, létrehoz egy üres lemezt, vagy csatol egy meglévő lemezt.
A paraméter elfogadható értékei a következők:

- Csatolja.
Ezt a lehetőséget választva virtuális gépet hozhat létre egy speciális merevlemezről.
Ha ezt a beállítást adja meg, ne adja meg a *SourceImageUri* paramétert.
A *VhdUri* mindent meg kell tennie ahhoz, hogy az Azure platform a virtuális merevlemez (VHD) helyét a virtuális gép adatlemezéhez csatolja.
- Üres.
Ezzel a beállítással üres adatlemezt hozhat létre.
- FromImage.
Ezt a lehetőséget választva virtuális gépet hozhat létre általános képből vagy lemezről.
Ha ezt a beállítást választja, akkor a *SourceImageUri* paramétert is meg kell adnia, hogy az Azure platform a VHD-fájlnak az adatlemezhez való csatolását adja.
A *VhdUri* paraméter az a hely, ahol az ADATlemez VHD-adatlemeze a virtuális gép általi használat után tárolódik.

```yaml
Type: Microsoft.Azure.Management.Compute.Models.DiskCreateOptionTypes
Parameter Sets: (All)
Aliases: 
Accepted values: FromImage, Empty, Attach

Required: True
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

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

### -DiskSizeInGB
Itt adhatja meg a virtuális géphez csatolni kívánt üres lemez méretét gigabájtban.

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

### -LUN
Az adatlemez logikai egységének számát adja meg.

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
A felügyelt lemezek AZONOSÍTÓját adja meg.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name (név)
A hozzáadni kívánt adatlemez nevét adja meg.

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
Annak a lemeznek az erőforrás-URI-azonosítóját adja meg, amelyre a parancsmag csatolva van.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SourceImage

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageAccountType
A felügyelt lemez tárterület-típusát adja meg.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.StorageAccountTypes]
Parameter Sets: (All)
Aliases: 
Accepted values: StandardLRS, PremiumLRS

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VhdUri
A virtuális merevlemez (VHD-fájl) egységes erőforrás-azonosítóját adja meg, amely a platform képe vagy a felhasználói kép használatakor hozható létre.
Ez a parancsmag a binárisan nagy objektumot (blob) másolja át erre a helyre.
Az a hely, ahonnan a virtuális gépet el kell indítani.

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

### -VM
Annak a helyi virtuális gépnek az objektumát adja meg, amelyhez adatlemezt kíván hozzáadni.
A **Get-AzureRmVM** parancsmaggal egy virtuálisgép-objektum beszerzése használható.
A **New-AzureRmVMConfig** parancsmaggal létrehozhatja a virtuális gép objektumát.

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

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Remove-AzureRmVMDataDisk](./Remove-AzureRmVMDataDisk.md)

[Get-AzureRmVM](./Get-AzureRmVM.md)

[Új – AzureRmVMConfig](./New-AzureRmVMConfig.md)
