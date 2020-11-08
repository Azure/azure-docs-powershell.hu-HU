---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 0DF54C9D-7A19-4591-A1FC-33C6A4C9BF33
online version: ''
schema: 2.0.0
ms.openlocfilehash: 05a99e1a4965329c0eeb29fe0e014814fd1807b2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015937"
---
# Test-AzureName

## Áttekintés
Annak vizsgálata, hogy a Microsoft Azure Cloud szolgáltatás neve, tárolási szolgáltatás neve vagy a szolgáltatás busza névtér neve létezik-e vagy sem.

## SZINTAXISA

### Szolgáltatás
```
Test-AzureName [-Service] -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### Tárterület
```
Test-AzureName [-Storage] -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ServiceBusNamespace
```
Test-AzureName [-ServiceBusNamespace] -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### Webhely
```
Test-AzureName [-Website] -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
Ha a név létezik, a parancsmag $Truet ad eredményül.
Ha a név nem létezik, akkor az a $False értéket adja eredményül.

## Példák

### Példa 1
```
PS C:\> Test-AzureName -Service "MyNameService1"
```

Ez a parancs azt vizsgálja, hogy az "MyNameService1" egy meglévő Microsoft Azure Cloud-szolgáltatás neve-e.

### 2. példa
```
PS C:\> Test-AzureName -Storage "mystorename1"
```

Ez a parancs azt vizsgálja, hogy a "mystorename1" egy meglévő Microsoft Azure Storage Service Name.

### 3. példa
```
PS C:\> Test-AzureName -ServiceBusNamespace "mynamespace"
```

Ez a parancs azt vizsgálja, hogy az "mynamespace" egy meglévő Microsoft Azure Service Bus névtér-név.

## PARAMÉTEREK

### -Name (név)
A tesztelni kívánt szolgáltatás vagy tárolási fiók nevét adja meg.

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

### -Szolgáltatás
A meglévő szolgáltatásfiók tesztelését adja meg.

```yaml
Type: SwitchParameter
Parameter Sets: Service
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServiceBusNamespace
Itt határozhatja meg, hogy egy meglévő szolgáltatási busz névteret szeretne-e tesztelni.

```yaml
Type: SwitchParameter
Parameter Sets: ServiceBusNamespace
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tárterület
A meglévő tárterület-fiók tesztelését adja meg.

```yaml
Type: SwitchParameter
Parameter Sets: Storage
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Webhely
A meglévő webhelyek tesztelését adja meg.

```yaml
Type: SwitchParameter
Parameter Sets: Website
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

## MEGJEGYZI
* Node-dev, php-dev, Python-dev

## KAPCSOLÓDÓ HIVATKOZÁSOK

