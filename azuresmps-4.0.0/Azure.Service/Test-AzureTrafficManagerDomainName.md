---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: 92E2409B-14BC-428F-8BAF-60D8DAFA5F57
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1adaafdfdd4331bbba86530eb532964430ed7c69
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015935"
---
# Test-AzureTrafficManagerDomainName

## Áttekintés
Ellenőrzi, hogy egy tartománynév elérhető-e Traffic Manager-profilként.

## SZINTAXISA

```
Test-AzureTrafficManagerDomainName -DomainName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
A **AzureTrafficManagerDomainName-** parancsmag ellenőrzi, hogy egy tartománynév elérhető-e Microsoft Azure Traffic Manager-profilként.
Ha a tartománynév elérhető, a parancsmag a $True értékét adja eredményül.

## Példák

### Példa 1: annak ellenőrzése, hogy elérhető-e tartománynév
```
PS C:\>Test-AzureTrafficManagerDomainName -DomainName "ContosoApp.trafficmanager.net"
$True
```

Ez a parancs azt ellenőrzi, hogy a tartománynév ContosoApp.trafficmanager.net elérhető-e Traffic Manager-profilként.

## PARAMÉTEREK

### -Tartománynév
A tesztelni kívánt tartomány nevét adja meg.
A következő karakterláncot kell tartalmaznia: 

. trafficmanager.net

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
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

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

### System. Boolean
Ez a parancsmag $True vagy $Falset hoz létre.
Ha a tartománynév elérhető, a parancsmag a $True értékét adja eredményül.

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

