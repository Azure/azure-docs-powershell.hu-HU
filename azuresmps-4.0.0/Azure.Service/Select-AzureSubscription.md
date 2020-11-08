---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 7A45DCAD-88DC-40F0-BBF7-0F531A571CA6
online version: ''
schema: 2.0.0
ms.openlocfilehash: 48b941691366c3af821e3a4cdaa7b07c5e958e16
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015445"
---
# Select-AzureSubscription

## Áttekintés
Az aktuális és az alapértelmezett Azure-előfizetések módosítása

## SZINTAXISA

### SelectSubscriptionByNameParameterSet (alapértelmezett)
```
Select-AzureSubscription -SubscriptionName <String> [-Account <String>] [-Current] [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### SelectDefaultSubscriptionByNameParameterSet
```
Select-AzureSubscription -SubscriptionName <String> [-Account <String>] [-Default] [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### SelectSubscriptionByIdParameterSet
```
Select-AzureSubscription -SubscriptionId <String> [-Account <String>] [-Current] [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### SelectDefaultSubscriptionByIdParameterSet
```
Select-AzureSubscription -SubscriptionId <String> [-Account <String>] [-Default] [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### NoCurrentSubscriptionParameterSet
```
Select-AzureSubscription [-Account <String>] [-NoCurrent] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### NoDefaultSubscriptionParameterSet
```
Select-AzureSubscription [-Account <String>] [-NoDefault] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Leírás
A **Select-AzureSubscription** parancsmag beállítja az aktuális és az alapértelmezett Azure-előfizetést, és törli őket.

Az "aktuális előfizetés" az aktuális Windows PowerShell-munkamenetben alapértelmezés szerint használt előfizetés.
Az alapértelmezett előfizetés alapértelmezés szerint minden Windows PowerShell-munkamenetben használatos.
A "jelenlegi előfizetés" címke lehetővé teszi, hogy az aktuális munkamenethez alapértelmezés szerint eltérő előfizetést adjon meg anélkül, hogy a többi munkamenethez az "alapértelmezett előfizetést" módosítaná.

Az "alapértelmezett" előfizetés-kijelölést az előfizetési adatfájl menti.
A munkamenet-specifikus "aktuális" kijelölést a program nem menti.

Ez a témakör a Microsoft Azure PowerShell modul 0.8.10 verziójában található parancsmagot ismerteti.
A használt modul verziójának beszerzéséhez az Azure PowerShell konzolon írja be a következőt: `(Get-Module -Name Azure).Version` .

## Példák

### Példa 1: a jelenlegi előfizetés beállítása
```
C:\PS> Select-AzureSubscription -Current -SubscriptionName ContosoEngineering
```

Ez a parancs a jelenlegi előfizetést "ContosoEngineering" teszi.

### 2. példa: az alapértelmezett előfizetés beállítása
```
C:\PS> Select-AzureSubscription -Default -SubscriptionName ContosoFinance -SubscriptionDataFile "C:\subs\MySubscriptions.xml"
```

Ez a parancs megváltoztatja az alapértelmezett "ContosoFinance" előfizetést. Az alapértelmezett előfizetési adatfájl helyett az Subscriptions.xml-előfizetés adatfájljába menti a beállítást.

## PARAMÉTEREK

### -Fiók
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

### -Current
```yaml
Type: SwitchParameter
Parameter Sets: SelectSubscriptionByNameParameterSet, SelectSubscriptionByIdParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### – Alapértelmezett
```yaml
Type: SwitchParameter
Parameter Sets: SelectDefaultSubscriptionByNameParameterSet, SelectDefaultSubscriptionByIdParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nem aktuális
```yaml
Type: SwitchParameter
Parameter Sets: NoCurrentSubscriptionParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### – Nem alapértelmezett
```yaml
Type: SwitchParameter
Parameter Sets: NoDefaultSubscriptionParameterSet
Aliases: 

Required: True
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
Parameter Sets: SelectSubscriptionByIdParameterSet, SelectDefaultSubscriptionByIdParameterSet
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
Parameter Sets: SelectSubscriptionByNameParameterSet, SelectDefaultSubscriptionByNameParameterSet
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Alapértelmezés szerint az nem hoz létre semmilyen kimenetet.

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureSubscription](./Get-AzureSubscription.md)

[Remove-AzureSubscription](./Remove-AzureSubscription.md)

[Set-AzureSubscription](./Set-AzureSubscription.md)


