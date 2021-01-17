---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 230DAE05-C197-451F-A24C-F4A2DAE4AD04
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssstorageprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssStorageProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssStorageProfile.md
ms.openlocfilehash: 7bf5e6b765fee14ca9ba12a289d6445e063ff9df
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98364138"
---
# Set-AzVmssStorageProfile

## SYNOPSIS
Beállítja a VMSS tárolóprofil-tulajdonságait.

## SZINTAXIS

```
Set-AzVmssStorageProfile [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-ImageReferencePublisher] <String>] [[-ImageReferenceOffer] <String>] [[-ImageReferenceSku] <String>]
 [[-ImageReferenceVersion] <String>] [[-OsDiskName] <String>] [[-OsDiskCaching] <CachingTypes>]
 [[-OsDiskCreateOption] <String>] [[-OsDiskOsType] <OperatingSystemTypes>] [[-Image] <String>]
 [[-VhdContainer] <String[]>] [-ImageReferenceId <String>] [-OsDiskWriteAccelerator]
 [-DiffDiskSetting <String>] [-ManagedDisk <String>] [-DiskEncryptionSetId <String>]
 [-DataDisk <VirtualMachineScaleSetDataDisk[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## LEÍRÁS
A **Set-AzVmssStorageProfile** parancsmag beállítja a virtuális gép méretaránykészletének (VMSS) tárolóprofil-tulajdonságait.

## PÉLDÁK

### 1. példa: A VMSS tárolóprofil-tulajdonságainak beállítása
```
PS C:\> Set-AzVmssStorageProfile -VirtualMachineScaleSet "ContosoVMSS" -Name "Test" -OsDiskCreateOption "FromImage" -OsDiskCaching "None" `
            -ImageReferenceOffer $ImgRef.Offer -ImageReferenceSku $ImgRef.Skus -ImageReferenceVersion $ImgRef.Version `
            -ImageReferencePublisher $ImgRef.PublisherName -VhdContainer $VhdContainer
```

Ez a parancs beállítja a ContosoVMSS nevű VMSS tárolóprofil-tulajdonságait.

## PARAMETERS

### -DataDisk
Az adatlemez-objektumot adja meg.

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetDataDisk[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
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

### -DiskEncryptionSetId
Az ügyfél által felügyelt lemeztitkosítási készlet erőforrás-azonosítóját adja meg.  Ez csak felügyelt lemezhez lehet megadni.

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

### -Image
A felhasználói kép blob-URI-ját adja meg.
A VMSS egy operációs rendszerlemezt hoz létre a felhasználói lemezkép ugyanazon tárolóban.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ImageReferenceId
A képhivatkozás azonosítóját adja meg.

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

### -ImageReferenceOffer
A virtuális gép lemezképének (VMImage) ajánlat típusát határozza meg.
Képajánlat beszerzéséhez használja a Get-AzVMImageOffer parancsmagot.

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

### -ImageReferencePublisher
Egy VMImage-közzétevő nevét adja meg.
Közzétevő beszerzéséhez használja a Get-AzVMImagePublisher parancsmagot.

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

### -ImageReferenceSku
A VMImage termékváltozatot adja meg.
Az SKUs-k beszerzéséhez használja a Get-AzVMImageSku parancsmagot.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ImageReferenceVersion
A VMImage verziójának megadása.
A legújabb verzió csak akkor használható, ha az adott verzió helyett a legújabb értéket adja meg.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ManagedDisk
A felügyelt lemez megadása.

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

### -OsDiskCaching
Az operációs rendszer lemezének gyorsítótárazása. A paraméter elfogadható értékei a következőek:
- ReadOnly
- ReadWrite The default value is ReadWrite.
Ha módosítja a gyorsítótárazás értékét, a parancsmag újraindítja a virtuális gépet.
Ez a beállítás befolyásolja a lemez konzisztenciáját és teljesítményét.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.CachingTypes]
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -OsDiskCreateOption
Azt adja meg, hogy ez a parancsmag hogyan hozza létre a VMSS virtuális gépeket.
A paraméter elfogadható értékei a következőek:
- Csatolás: Ezt az értéket akkor használja a rendszer, ha egy speciális lemezen hozza létre a VMSS virtuális gépet. 
- FromImage: Ez az érték akkor használatos, amikor egy képet használ a VMSS virtuális gép létrehozásához.
Platformkép használata esetén a *imageReference paramétert is használhatja.*

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -OsDiskName
Az operációs rendszer lemezének nevét adja meg.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -OsDiskOsType
A lemezen található operációs rendszer típusát határozza meg.
Erre csak felhasználói kép esetén van szükség, platformkép esetén nem.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes]
Parameter Sets: (All)
Aliases:
Accepted values: Windows, Linux

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -OsDiskWriteAccelerator
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

### -VhdContainer
Megadja a VMSS operációs rendszer lemezének tárolására használt tároló URL-eket.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualMachineScaleSet
A VMSS-objektumot adja meg.
Az objektum beszerzéséhez használja a New-AzVmssConfig objektumot.

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Confirm
A parancsmag futtatása előtt a rendszer megerősítést kér.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
A parancsmag futtatásakor a program megjeleníti, hogy mi történik. A parancsmag nem fut.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet

### System.String

### System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0,0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]

### System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0,0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]

### System.String[]

### Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetDataDisk[]

## KIMENETEK

### Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzVMImageOffer](./Get-AzVMImageOffer.md)

[Get-AzVMImagePublisher](./Get-AzVMImagePublisher.md)

[Get-AzVMImageSku](./Get-AzVMImageSku.md)

[New-AzVmssConfig](./New-AzVmssConfig.md)


