---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 06a78584437021df570bc5ff2b6ec19e332bffd8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491320"
---
# Save-AzureRmProfile

## Áttekintés
Az aktuális hitelesítési adatokat menti a többi PowerShell-munkamenetben való használatra.

## SZINTAXISA

```
Save-AzureRmProfile [[-Profile] <AzureRMProfile>] [-Path] <String> [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Leírás
Az Save-AzureRmProfile parancsmag az aktuális hitelesítési adatokat menti a többi PowerShell-munkamenetben való használatra.

## Példák

### 1. példa: az aktuális munkamenet profiljának mentése
```
PS C:\> Add-AzureRmAccount
PS C:\> Save-AzureRmProfile -Path C:\test.json
```

Ebben a példában az aktuális munkamenet Azure-profilját az adott JSON-fájlba menti.

### 2. példa: adott profil mentése
```
PS C:\> Save-AzureRmProfile -Profile (Add-AzureRmAccount) -Path C:\test.json
```

Ebben a példában az Azure-profilt átmenti a parancsmagra a JSON-fájlra.

## PARAMÉTEREK

### -Force
A megadott fájl felülírása ha létezik

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -Path (elérési út)
Annak a fájlnak az elérési útját adja meg, amelyre menteni szeretné a hitelesítési adatokat.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profil
Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.
Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.

```yaml
Type: AzureRMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### – Megerősítés
A parancsmag futtatása előtt kéri a megerősítést.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Annak megjelenítése, hogy mi történik, ha a parancsmag fut. A parancsmag nem fut.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

### PSAzureProfile

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Select-AzureRMProfile]()

