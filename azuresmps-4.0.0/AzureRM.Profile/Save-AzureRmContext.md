---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: f3afbd9b96de51f754dd87dfa42ed6f71e5b3577
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/23/2019
ms.locfileid: "93490452"
---
# Save-AzureRmContext

## Áttekintés
Az aktuális hitelesítési adatokat menti a többi PowerShell-munkamenetben való használatra.

## SZINTAXISA

```
Save-AzureRmContext [[-Profile] <AzureRmProfile>] [-Path] <String> [-Force] [-WhatIf] [-Confirm]
```

## Leírás
Az Save-AzureRmContext parancsmag az aktuális hitelesítési adatokat menti a többi PowerShell-munkamenetben való használatra.

## Példák

### 1. példa: az aktuális munkamenet környezetének mentése
```
PS C:\> Add-AzureRmAccount
PS C:\> Save-AzureRmContext -Path C:\test.json
```

Ez a példa az aktuális munkamenet Azure-környezetét az adott JSON-fájlba menti.

### 2. példa: adott környezet mentése
```
PS C:\> Save-AzureRmContext -Profile (Add-AzureRmAccount) -Path C:\test.json
```

Ez a példa menti az Azure-környezetet, amelyet áthalad a parancsmagnak a JSON-fájlra.

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
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profil
Azt az Azure-környezetet adja meg, amelyből a parancsmag olvasható.
Ha nem ad meg környezetet, a parancsmag a helyi alapértelmezett környezetből olvassa be a szöveget.

```yaml
Type: AzureRmProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
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
Annak megjelenítése, hogy mi történik, ha a parancsmag fut.
A parancsmag nem fut.

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

## BEMENETEK

### Microsoft. Azure. commands. Common. Authentication. models. AzureRMProfile

## KIMENETEK

### Microsoft. Azure. Command. profil. models. PSAzureProfile

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

