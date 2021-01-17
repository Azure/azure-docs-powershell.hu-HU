---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssVMDataDisk.md
ms.openlocfilehash: 5e7901f3e2d18b0707ccf9c5f62f9ab55789a45e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98370045"
---
# Add-AzVmssVMDataDisk

## SYNOPSIS
Adatlemezt ad a Vmss VM-hez.

## SZINTAXIS

```
Add-AzVmssVMDataDisk [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [-Lun] <Int32>
 [-CreateOption] <String> [-ManagedDiskId] <String> [-StorageAccountType <String>]
 [-DiskEncryptionSetId <String>] [-Caching <CachingTypes>] [-DiskSizeInGB <Int32>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## LEÍRÁS
Az **Add-AzVmssVMDataDisk** parancsmag hozzáad egy adatlemezt a Vmss VM-hez.

## PÉLDÁK

### 1. példa: Felügyelt adatlemez hozzáadása Vmss VM-hez.
```powershell
PS C:\> $disk = Get-AzDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> $VmssVM = Add-AzVmssVMDataDisk -VirtualMachineScaleSetVM $VmssVM -Lun 0 -DiskSizeInGB 10 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> Update-AzVmssVM -VirtualMachineScaleSetVM $VmssVM
```

Az első parancs egy meglévő felügyelt lemezhez jut.
A következő parancs egy meglévő Vmss VM-et kap, amelyet az erőforráscsoport neve, a vmss neve és a példányazonosító ad meg.
A következő parancs hozzáadja a felügyelt lemezt a helyileg tárolt Vmss VM-hez a $VmssVM.
Az utolsó parancs frissíti a Vmss VM-et hozzáadott adatlemezzel.

## PARAMETERS

### -Gyorsítótárazás
A lemez gyorsítótárazása.
A paraméter elfogadható értékei a következőek:
- ReadOnly
- ReadWrite
- Nincs az alapértelmezett érték a Beolvasott érték.
Ennek az értéknek a módosítása a virtuális gép újraindítását okozza.
Ez a beállítás befolyásolja a lemez konzisztenciáját és teljesítményét.

```yaml
Type: Microsoft.Azure.Management.Compute.Models.CachingTypes
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: Named
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
Position: 2
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
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Lun
Egy adatlemez logikai egységszámát (LUN) adja meg.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ManagedDiskId
Egy felügyelt lemez azonosítóját adja meg.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualMachineScaleSetVM
Megadja a virtuális gép méretarányát tároló virtuális gépi objektumot, amelyhez adatlemezt szeretne hozzáadni.
A **Get-AzVmssVM** parancsmag használatával virtuális gépi méretezésű VM-objektumot szerezhet be.

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -WriteAccelerator
Azt adja meg, hogy a WriteAccelerator engedélyezve vagy letiltva legyen-e felügyelt adatlemezen.

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

### Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM

### System.Int32

### System.String

### Microsoft.Azure.Management.Compute.Models.CachingTypes

## KIMENETEK

### Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK
