---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7180CAC6-BFC1-4A18-A754-83D5F05C5BEF
online version: ''
schema: 2.0.0
ms.openlocfilehash: c62c30558147bccd9cdecc73925b7e1a379d1c5b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016255"
---
# Import-AzureVM

## Áttekintés
Azure Virtual Machine-állam importálása fájlból.

## SZINTAXISA

```
Import-AzureVM [-Path] <String> [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## Leírás
Az **import-AzureVM** parancsmag a virtuális gép korábban mentett állapotát XML-fájlból importálja.
Ez a parancsmag akkor hasznos, ha később egy virtuális gépet szeretne létrehozni az importált adatforrásból.

Az **AzureVM** futtatása után az **Eltávolítás – AzureVM** , majd az **Importálás – AzureVM** parancsra kattintva a virtuális gép újból létrehozhatja a virtuális gépet, mert az eredetitől eltérő IP-cím lehet.

## Példák

### 1. példa: virtuálisgép-állapot importálása
```
PS C:\> Import-AzureVM -Path "C:\VMstate.xml" | New-AzureVM -ServiceName "ContosoService02"
```

Ezzel a paranccsal importálhatja egy virtuális gép állapotát a VMstate.xml-fájlból, majd egy virtuális gépet hoz létre a megadott Felhőbeli szolgáltatásban.

## PARAMÉTEREK

### -InformationAction
Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.

A paraméter elfogadható értékei a következők:

- Folytassa
- Mellőzése
- Érdeklődni
- SilentlyContinue
- állj
- Felfüggesztheti

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
Egy információs változót ad meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Path (elérési út)
A korábban mentett virtuálisgép-állapottal rendelkező fájl elérési útvonalát adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Exportálás – AzureVM](./Export-AzureVM.md)

[Új – AzureVM](./New-AzureVM.md)


