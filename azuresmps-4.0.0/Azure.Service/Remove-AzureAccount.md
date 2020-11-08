---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 3CD1A989-902C-48B3-81E9-7B78EDA5F880
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7003abf263fd4c669956f65c990246295cf7158d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015870"
---
# Remove-AzureAccount

## Áttekintés
Azure-fiók törlése a Windows PowerShellből

## SZINTAXISA

```
Remove-AzureAccount -Name <String> [-Force] [-PassThru] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Leírás
A **Remove-AzureAccount** parancsmag az Azure-fiókokat és az előfizetéseket az előfizetési adatfájlból törli a központi felhasználói profilból.
A fiók nem törlődik a Microsoft Azure-ból, vagy semmilyen módon nem változtatja meg a tényleges fiókot.

A parancsmag használata nagyon hasonlít az Azure-fiókból való kijelentkezésre.
Ha ismét be szeretne jelentkezni a fiókba, a **Add-AzureAccount** vagy az **import-AzurePublishSettingsFile** segítségével ismét felveheti a fiókot a Windows powershellbe.

A **Remove-AzureAccount** parancsmag használatával megváltoztathatja az Azure PowerShell-parancsmagok Azure-fiókjába való bejelentkezésének módját.
Ha a fiókja mind az **AzurePublishSettingsFile** , mind pedig az Access-jogkivonat felügyeleti tanúsítványát tartalmazza, az Azure PowerShell-parancsmagok csak a hozzáférési jogkivonatot használják, a **AzureAccount**. figyelmen kívül hagyják a kezelési tanúsítványt.
A felügyeleti tanúsítvány használatához futtassa a **Remove-AzureAccount**.
Ha a **Remove-AzureAccount** felügyeleti tanúsítványt és hozzáférési jogkivonatot keres, akkor a fiók törlése helyett csak a hozzáférési jogkivonat törlődik.
A felügyeleti tanúsítvány továbbra is fennáll, így a fiók továbbra is elérhető a Windows PowerShellben.

Ez a témakör a Microsoft Azure PowerShell modul 0.8.10 verziójában található parancsmagot ismerteti.
A használt modul verziójának beszerzéséhez az Azure PowerShell konzolon írja be a következőt: `(Get-Module -Name Azure).Version` .

## Példák

### 1. példa: fiók eltávolítása
```
PS C:\> Remove-AzureAccount -Name admin@contoso.com
```

Ez a parancs eltávolítja az admin@contoso.com előfizetési adatfájlból.
Amikor a parancs befejeződött, a fiók már nem érhető el a Windows PowerShellben.

## PARAMÉTEREK

### -Force
Letiltja a megerősítési kérdést.
A **Remove-AzureAccount** alapértelmezés szerint a fiók Windows powershellből való eltávolítása előtt kéri.

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
Az eltávolítandó fiók nevét adja meg.
A paraméter értéke megkülönbözteti a kis-és nagybetűket.
A helyettesítő karakterek használata nem támogatott.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
A parancs eredményét $True, ha a parancs sikerül, és a $False sikertelen.
Ez a parancsmag alapértelmezés szerint nem ad vissza semmilyen eredményt.

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

### -Profil
Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható. Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.

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

### Nincs
A parancsmagot tulajdonság nevében, de nem érték szerint is beírhatja.

## KIMENETEK

### Nincs vagy System. Boolean
Ha a *PassThru* paramétert használja, ez a parancsmag logikai értéket ad eredményül.
Ellenkező esetben nem ad vissza semmilyen eredményt.

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Add-AzureAccount](./Add-AzureAccount.md)

[Get-AzureAccount](./Get-AzureAccount.md)


