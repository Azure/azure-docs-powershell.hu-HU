---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D2B5BC27-6D51-45BC-AE6A-F7FED11B8651
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/save-azvmimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Save-AzVMImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Save-AzVMImage.md
ms.openlocfilehash: b663087437097b3e059f9d88c7720696222134e3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836690"
---
# Save-AzVMImage

## Áttekintés
Virtuális gép mentése VMImage.

## SZINTAXISA

### ResourceGroupNameParameterSetName (alapértelmezett)
```
Save-AzVMImage [-Name] <String> [-DestinationContainerName] <String> [-VHDNamePrefix] <String> [-Overwrite]
 [[-Path] <String>] [-ResourceGroupName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### IdParameterSetName
```
Save-AzVMImage [[-Name] <String>] [-DestinationContainerName] <String> [-VHDNamePrefix] <String> [-Overwrite]
 [[-Path] <String>] [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **Save-AzVMImage** parancsmag a virtuális gépet VMImage menti.
A virtuálisgép-képek létrehozása előtt a Sysprep a virtuális gépet használja, és a Set-AzVM parancsmaggal jelölje meg.
Ennek a parancsmagnak a kimenete egy JavaScript-objektum típusú (JSON) sablon.
A virtuális gépeket a rögzített képből is telepítheti.

## Példák

### Példa 1: virtuális gép rögzítése
```
PS C:\> Set-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Generalized 
PS C:\> Save-AzVMImage -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -DestinationContainerName "VMContainer01" -VHDNamePrefix "VM07"
```

Az első parancs a VirtualMachine07 nevű virtuális gépet általánosként jelöli meg.
A második parancs rögzíti a VirtualMachine07 nevű virtuális gépet VMImage.
A **kimenet** tulajdonság egy JSON-sablont ad eredményül.

## PARAMÉTEREK

### -AsJob
Futtassa a parancsmagot a háttérben, és a tevékenység visszaadása a folyamat nyomon követéséhez.

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

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

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

### -DestinationContainerName
A "rendszer" tárolóban lévő tároló nevét adja meg, amelyre a képeket tárolni szeretné.
Ha a tároló nem létezik, akkor létrejön Önnek.
A VMImage alkotó virtuális merevlemezek (VHD-EK) a paraméterben megadott tárolóban találhatók.
Ha a VHD-es merevlemezek több tárolási fiók között oszlanak el, ez a parancsmag egy olyan tárolót hoz létre, amelynek a neve minden tárolási fiókban szerepel.
A mentett kép URL-címe a következőhöz hasonló: https:// \< storageAccountName \> . blob.Core.Windows.net/System/Microsoft.Compute/images/ \< imagesContainer vhdPrefix. \> / \< \> osDisk. vhd.

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

### -Azonosító
A virtuális gép erőforrás-AZONOSÍTÓját adja meg.

```yaml
Type: System.String
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
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases: VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: IdParameterSetName
Aliases: VMName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Átír
Azt jelzi, hogy ez a parancsmag felülírja azokat a VHD-ket, amelyek azonos előtaggal rendelkeznek a célhely tárolóban.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Path (elérési út)
Annak a fájlnak az elérési útvonala, amelyben a rögzített kép sablonja van tárolva.

```yaml
Type: System.String
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
Type: System.String
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
Egy operációs rendszerhez használt előtag vhdPrefix például a vhdPrefix-osdisk nevet adja eredményül. \< GUID \> . vhd.

```yaml
Type: System.String
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

### System. String

### System. Management. Automation. SwitchParameter

## KIMENETEK

### Microsoft. Azure. commands. kiszámítás. models. PSComputeLongRunningOperation

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzVMImage](./Get-AzVMImage.md)

[Get-AzVMImageOffer](./Get-AzVMImageOffer.md)

[Get-AzVMImagePublisher](./Get-AzVMImagePublisher.md)

[Get-AzVMImageSku](./Get-AzVMImageSku.md)

[Set-AzVM](./Set-AzVM.md)


