---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: D2B5BC27-6D51-45BC-AE6A-F7FED11B8651
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Save-AzureRmVMImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Save-AzureRmVMImage.md
ms.openlocfilehash: 8f3aebe1e9e79423d7251fa79084d6fa85407b9d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503832"
---
# Save-AzureRmVMImage

## Áttekintés
Virtuális gép mentése VMImage.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### ResourceGroupNameParameterSetName (alapértelmezett)
```
Save-AzureRmVMImage [-Name] <String> [-DestinationContainerName] <String> [-VHDNamePrefix] <String>
 [-Overwrite] [[-Path] <String>] [-ResourceGroupName] <String> [<CommonParameters>]
```

### IdParameterSetName
```
Save-AzureRmVMImage [-Name] <String> [-DestinationContainerName] <String> [-VHDNamePrefix] <String>
 [-Overwrite] [[-Path] <String>] [-Id] <String> [<CommonParameters>]
```

## Leírás
A **Save-AzureRmVMImage** parancsmag a virtuális gépet VMImage menti.
A virtuálisgép-képek létrehozása előtt a Sysprep a virtuális gépet használja, és a Set-AzureRmVM parancsmaggal jelölje meg.

Ennek a parancsmagnak a kimenete egy JavaScript-objektum típusú (JSON) sablon.
A virtuális gépeket a rögzített képből is telepítheti.

## Példák

### Példa 1: virtuális gép rögzítése
```
PS C:\> Set-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Generalized 
PS C:\> Save-AzureRmVMImage -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -DestinationContainerName "VMContainer01" -VHDNamePrefix "VM07"
```

Az első parancs a VirtualMachine07 nevű virtuális gépet általánosként jelöli meg.

A második parancs rögzíti a VirtualMachine07 nevű virtuális gépet VMImage.
A **kimenet** tulajdonság egy JSON-sablont ad eredményül.

## PARAMÉTEREK

### -DestinationContainerName
A "rendszer" tárolóban lévő tároló nevét adja meg, amelyre a képeket tárolni szeretné.

Ha a tároló nem létezik, akkor létrejön Önnek.
A VMImage alkotó virtuális merevlemezek (VHD-EK) a paraméterben megadott tárolóban találhatók.
Ha a VHD-es merevlemezek több tárolási fiók között oszlanak el, ez a parancsmag egy olyan tárolót hoz létre, amelynek a neve minden tárolási fiókban szerepel.
A mentett kép URL-címe a következőhöz hasonló: 

https:// \<storageAccountName\> . blob.Core.Windows.net/System/Microsoft.Compute/images/ \<imagesContainer\> / \<vhdPrefix-osDisk\> . XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX. vhd.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Azonosító
A virtuális gép erőforrás-AZONOSÍTÓját adja meg.

```yaml
Type: String
Parameter Sets: IdParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name (név)
Egy nevet ad meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Átír
Azt jelzi, hogy ez a parancsmag felülírja azokat a VHD-ket, amelyek azonos előtaggal rendelkeznek a célhely tárolóban.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Path (elérési út)
A virtuális merevlemez elérési útvonalát adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
A virtuális gép erőforráscsoport-csoportjának nevét adja meg.

```yaml
Type: String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VHDNamePrefix
Annak az előtagnak a neve, amely a VMImage tárolási profilját képezi.

Egy operációs rendszerhez használt előtag vhdPrefix például a vhdPrefix- \<guid\> osdisk. VHD.

```yaml
Type: String
Parameter Sets: (All)
Aliases: VirtualHardDiskNamePrefix

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Nincs
Ez a parancsmag nem fogadja el a bevitelt.

## KIMENETEK

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureRmVMImage](./Get-AzureRmVMImage.md)

[Get-AzureRmVMImageOffer](./Get-AzureRmVMImageOffer.md)

[Get-AzureRmVMImagePublisher](./Get-AzureRmVMImagePublisher.md)

[Get-AzureRmVMImageSku](./Get-AzureRmVMImageSku.md)

[Set-AzureRmVM](./Set-AzureRmVM.md)


