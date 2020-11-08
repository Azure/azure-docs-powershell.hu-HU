---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: F101382E-B015-4913-B4A0-8827EC423319
online version: ''
schema: 2.0.0
ms.openlocfilehash: b37c4bf3ad2c2aaf74f268b18d17b6af71f4f2fc
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015884"
---
# Publish-AzureRemoteAppProgram

## Áttekintés
Az Azure RemoteApp program közzététele.

## SZINTAXISA

### App-azonosító (alapértelmezett)
```
Publish-AzureRemoteAppProgram [-CollectionName] <String> [-StartMenuAppId] <String> [-CommandLine <String>]
 [-DisplayName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### Az App elérési útja
```
Publish-AzureRemoteAppProgram [-CollectionName] <String> [-FileVirtualPath] <String> [-CommandLine <String>]
 [-DisplayName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
A **Közzététel-AzureRemoteAppProgram** parancsmag egy Azure RemoteApp programot tesz közzé, amely az Azure RemoteApp gyűjtemény felhasználói számára elérhetővé teszi az alkalmazást.

## Példák

### Példa 1: program közzététele egy gyűjteményben
```
PS C:\> Publish-AzureRemoteAppProgram -CollectionName "ContosoApps" -StartMenuAppId "a3732322-89a5-4cbc-9844-9634c74d337f" -DisplayName "Finance App"
```

Ez a parancs közzéteszi a programot az ContosoApps-gyűjteményben a megadott *StartMenuAppId* a program a Start menübe való felvételéhez.
A közzétett alkalmazás a "Penzugy app" megjelenítendő nevét fogja tartalmazni.

## PARAMÉTEREK

### -CollectionName
Az Azure RemoteApp-gyűjtemény nevét adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CommandLine
A parancsmag által közzétett program parancssori argumentumait adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisplayName
Az Azure RemoteApp program felhasználóbarát megjelenítendő nevét adja meg.
A felhasználók ezt az alkalmazás nevét látják.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FileVirtualPath
Megadja a program elérési útját a program sablon képén belül.

```yaml
Type: String
Parameter Sets: App Path
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
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StartMenuAppId
Azt a globálisan egyedi azonosítót adja meg, amely a parancsmag által a programnak a Start menübe való felvételéhez használható.

```yaml
Type: String
Parameter Sets: App Id
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureRemoteAppProgram](./Get-AzureRemoteAppProgram.md)

[Közzététel megszüntetése – AzureRemoteAppProgram](./Unpublish-AzureRemoteAppProgram.md)


