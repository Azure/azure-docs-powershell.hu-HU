---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 1085388B-0855-4E29-9043-3FE2C638F58D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 22c97045cb5f85256ec4d252cdbfb13c59643008
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015924"
---
# New-AzureDns

## Áttekintés
Azure DNS Settings-objektum létrehozása

## SZINTAXISA

```
New-AzureDns [-Name] <String> [-IPAddress] <String> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## Leírás
A **New-AzureDns** parancsmag egy Azure DNS Settings objektumot hoz létre.
Ha virtuális gépet hoz létre a **New-AzureVM** parancsmaggal, akkor használhatja a DNS Settings objektumot.

## Példák

### Példa 1: DNS-beállítások objektum létrehozása
```
PS C:\> $Dns = New-AzureDns -Name "Dns01" -IPAddress "10.1.2.4"
```

A parancs Azure DNS Settings objektumot hoz létre.
A DNS-kiszolgáló rendelkezik a megadott címmel és a felhasználóbarát név Dns01.
A parancs az objektumot a **New-AzureVM** parancsmag által használt $DNS változóban tárolja.

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

### -Ip_cím
A DNS-kiszolgáló IP-címét adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (név)
A DNS-kiszolgáló felhasználóbarát nevét adja meg.
Ez a név nem feltétlenül teljesen minősített tartománynév.

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

[Add-AzureDns](./Add-AzureDns.md)

[Get-AzureDns](./Get-AzureDns.md)

[Új – AzureVM](./New-AzureVM.md)

[Remove-AzureDns](./Remove-AzureDns.md)

[Set-AzureDns](./Set-AzureDns.md)


