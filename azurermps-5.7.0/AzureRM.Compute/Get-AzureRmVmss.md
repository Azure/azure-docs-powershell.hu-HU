---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: FC6BC096-DBC4-48DA-A366-B87EB18A0496
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVmss.md
ms.openlocfilehash: b3e9f2608703eebd5ad24846aad7b5a1ad11e8ab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503852"
---
# Get-AzureRmVmss

## Áttekintés
Beolvassa a VMSS tulajdonságait.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### DefaultParameter (alapértelmezett)
```
Get-AzureRmVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [<CommonParameters>]
```

### FriendMethod
```
Get-AzureRmVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [-InstanceView]
 [<CommonParameters>]
```

## Leírás
A **Get-AzureRmVmss** parancsmag a virtuálisgép-készlet (VMSS) modell-és példány nézetét kapja.
A modell nézet a virtuális gép felhasználó által megadott tulajdonságai.
A példány nézet a virtuális gép példány szintjének állapota.
Adja meg az *állapot* paramétert, hogy csak a virtuális gép példány nézete legyen látható.

## Példák

### Példa 1: VMSS tulajdonságainak beolvasása
```
PS C:\> Get-AzureRmVmss -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

Ez a parancs beolvassa a Group001 nevű erőforráscsoport VMSS001 tartozó VMSS tulajdonságait.
Mivel a parancs nem adja meg a *InstanceView* kapcsoló paramétert, a parancsmag a virtuális gép modell nézetét kapja.

## PARAMÉTEREK

### -InstanceView
Azt jelzi, hogy ez a parancsmag csak a virtuális gép példány nézetét kapja meg.

```yaml
Type: SwitchParameter
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
A VMSS erőforráscsoport-csoportjának nevét adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMScaleSetName
Faj: a VMSS neve.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
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

### Ez a parancsmag semmilyen kimenetet nem hoz létre.

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Új – AzureRmVmss](./New-AzureRmVmss.md)

[Remove-AzureRmVmss](./Remove-AzureRmVmss.md)

[Újraindítás – AzureRmVmss](./Restart-AzureRmVmss.md)

[Set-AzureRmVmss](./Set-AzureRmVmss.md)

[Start-AzureRmVmss](./Start-AzureRmVmss.md)

[Stop-AzureRmVmss](./Stop-AzureRmVmss.md)

[Update-AzureRmVmss](./Update-AzureRmVmss.md)


