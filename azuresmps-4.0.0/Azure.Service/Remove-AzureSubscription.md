---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: ABC303ED-8712-4958-B871-E95357012277
online version: ''
schema: 2.0.0
ms.openlocfilehash: 706c1dee2bc4bb21a8cf116d15bfa3e53daeed99
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016095"
---
# Remove-AzureSubscription

## Áttekintés
Azure-előfizetés törlése a Windows PowerShellből

## SZINTAXISA

### Név (alapértelmezett)
```
Remove-AzureSubscription -SubscriptionName <String> [-Force] [-PassThru] [-Profile <AzureSMProfile>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### Azonosító
```
Remove-AzureSubscription -SubscriptionId <String> [-Force] [-PassThru] [-Profile <AzureSMProfile>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## Leírás
A **Remove-AzureSubscription** parancsmag Azure-előfizetést töröl az előfizetési adatfájlból, így a Windows PowerShell nem találja.
Ez a parancsmag nem törli a Microsoft Azure-előfizetést, vagy semmilyen módon nem változtatja meg a tényleges előfizetést.

Ez a témakör a Microsoft Azure PowerShell modul 0.8.10 verziójában található parancsmagot ismerteti.
A használt modul verziójának beszerzéséhez az Azure PowerShell konzolon írja be a következőt: `(Get-Module -Name Azure).Version` .

## Példák

### Példa 1: előfizetés törlése
```
C:\PS> Remove-AzureSubscription -SubscriptionName Test

Confirm
Are you sure you want to perform this action?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"):
```

Ez a parancs törli a "teszt" előfizetést az alapértelmezett előfizetési adatfájlból.

### 2. példa: törlés másik előfizetési adatfájlból
```
C:\PS> Remove-AzureSubscription -SubscriptionName Test -SubscriptionDataFile C:\Subs\MySubscriptions.xml -Force
```

Ez a parancs törli a teszt-előfizetést az MySubscriptions.xml-előfizetési adatfájlból.
A parancs az *erő* paramétert használja a megerősítési kérdés elrejtéséhez.

### 3. példa: előfizetés törlése parancsfájlból
```
C:\PS> ...if (Remove-AzureSubscription -SubscriptionName Test -PassThru) {...}
```

Ez a parancs a **Ha** utasításban a **Remove-AzureSubscription** parancsot használja.
A *PassThru* paramétert használja, amely logikai értéket ad eredményül annak megállapításához, hogy a parancsfájl blokkolva van-e a **Ha** utasításban.

## PARAMÉTEREK

### -Force
Letiltja a megerősítési kérdést.

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

### -SubscriptionId
```yaml
Type: String
Parameter Sets: Id
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SubscriptionName
```yaml
Type: String
Parameter Sets: Name
Aliases: Name

Required: True
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

### Nincs
A parancsmagot tulajdonság nevében, de nem érték szerint is beírhatja.

## KIMENETEK

### Nincs vagy System. Boolean
Ha a *PassThru* paramétert használja, ez a parancsmag logikai értéket ad eredményül.
Ellenkező esetben nem ad vissza semmilyen eredményt.

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureSubscription](./Get-AzureSubscription.md)

[Select-AzureSubscription](./Select-AzureSubscription.md)

[Set-AzureSubscription](./Set-AzureSubscription.md)


