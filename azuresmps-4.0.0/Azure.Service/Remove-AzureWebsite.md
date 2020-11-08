---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 8062D57E-8381-4715-9AA8-551F15DCC492
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2627bdb2f098d5b09851ec5970dd2a73840d24e6
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015483"
---
# Remove-AzureWebsite

## Áttekintés
Eltávolítja a megadott webhelyet az Azureról.

## SZINTAXISA

```
Remove-AzureWebsite [-Force] [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Leírás
Ez a témakör a Microsoft Azure PowerShell modul 0.8.10 verziójában található parancsmagot ismerteti.
A használt modul verziójának beszerzéséhez az Azure PowerShell konzolon írja be a következőt: `(Get-Module -Name Azure).Version` .

A **Remove-AzureWebsite** parancsmag eltávolítja a megadott webhelyet az Azure-ról a megerősítési kéréssel vagy anélkül.

## Példák

### 1. példa: az aktuális webhely eltávolítása
```
PS C:\> Remove-AzureWebsite
```

Ez a példa eltávolítja az Azure webhelyét az aktuális címtárral társítva.

### 2. példa: webhely eltávolítása megerősítés nélkül
```
PS C:\> Remove-AzureWebsite -Name mySite -Force
```

Ez a példa törli a mySite nevű webhelyet a megerősítés kérése nélkül.

## PARAMÉTEREK

### -Force
Ha meg van adva, a megadott webhely törlése megerősítés kérése nélkül.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (név)
Annak a webhelynek a neve, amelyet törölni szeretne.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Profil
Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.
Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Slot
A webhely tárolóhelyének a nevét adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureWebsite](./Get-AzureWebsite.md)


