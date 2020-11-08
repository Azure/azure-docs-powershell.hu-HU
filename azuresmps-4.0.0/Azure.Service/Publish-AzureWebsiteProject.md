---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: D866554F-78B0-4691-BA06-F625F9B0DFC8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 366941504c020910735015e3d8b282af376d54d9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015877"
---
# Publish-AzureWebsiteProject

## Áttekintés
Visual Studio-webprojektet közzétehet a Microsoft Azure-webhelyről webtelepítéssel.

## SZINTAXISA

### ProjectFile
```
Publish-AzureWebsiteProject -ProjectFile <String> [-Configuration <String>] [-ConnectionString <Hashtable>]
 [-SkipAppData] [-DoNotDelete] [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### Csomag
```
Publish-AzureWebsiteProject -Package <String> [-ConnectionString <Hashtable>] [-Tokens <String>]
 [-SetParametersFile <String>] [-SkipAppData] [-DoNotDelete] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
Visual Studio-webprojektet közzétehet a Microsoft Azure-webhelyről webtelepítéssel.
Létrehozhat egy webtelepítési csomagot, és közzéteheti közvetlenül, vagy készíthet egy Visual Studio web projectet, és közzéteheti a projektet.
A közzététel során az Web.config a kapcsolati karakterláncokat is lecserélheti.

## Példák

### Példa 1
```
PS C:\> Publish-AzureWebsiteProject -Name site1 -ProjectFile .\WebApplication1.csproj -Configuration Debug
```

Készítsen egy Visual Studio-webprojektet a "debug" konfigurációval (jelentése: Web.Debug.config), és tegye közzé a Microsoft Azure-webhelyeken a webes telepítés segítségével.

### 2. példa
```
PS C:\> Publish-AzureWebsiteProject -Name site1 -Package .\WebApplication1.zip
```

Webdeploy Package. zip fájl közzététele webtelepítéssel a Microsoft Azure-webhelyre.

### 3. példa
```
PS C:\> Publish-AzureWebsiteProject -Name site1 -Package .\WebApplication1
```

Webdeploy Package-mappa közzététele webközponti verziós Microsoft Azure-webhelyen

### 4. példa
```
PS C:\> Publish-AzureWebsiteProject -Name site1 -ProjectFile .\WebApplication1.csproj -ConnectionString @{ DefaultConnection = "my connection string" }
```

Létrehozhat egy Visual Studio-webprojektet, felülírhatja a "DefaultConnection" kapcsolódási karakterláncot Web.config és közzéteheti a Microsoft Azure-webhelyeken webtelepítéssel.

### Példa 5
```
PS C:\> Publish-AzureWebsiteProject -Name site1 -ProjectFile .\WebApplication1.csproj -DefaultConnection "my connection string"
```

Létrehozhat egy Visual Studio-webprojektet, felülírhatja a "DefaultConnection" kapcsolódási karakterláncot Web.config és közzéteheti a Microsoft Azure-webhelyeken webtelepítéssel.
Figyelje meg, hogy a DefaultConnection egy dinamikus paraméter, amelyet az Web.config elemzésével kap hozzá.

## PARAMÉTEREK

### -Configuration
A Visual Studio webalkalmazás-projekt létrehozásához használt konfiguráció.

```yaml
Type: String
Parameter Sets: ProjectFile
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ConnectionString
A bevezetéshez használandó kapcsolati karakterláncok.

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DoNotDelete
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
A webhely neve.

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

### -Package (csomag)
A közzétenni kívánt Visual Studio-webalkalmazás-projekt zip-fájljának webdeploy Package mappája.

```yaml
Type: String
Parameter Sets: Package
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

### -ProjectFile
Közzé kell tennie a Visual Studio webalkalmazás-projektet.

```yaml
Type: String
Parameter Sets: ProjectFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SetParametersFile
```yaml
Type: String
Parameter Sets: Package
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SkipAppData
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

### -Slot
A webhely tárolóhelyének neve.

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

### -Tokenek
```yaml
Type: String
Parameter Sets: Package
Aliases: 

Required: False
Position: Named
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

[Get-AzureWebsite](./Get-AzureWebsite.md)

[Új – AzureWebsite](./New-AzureWebsite.md)

[Remove-AzureWebsite](./Remove-AzureWebsite.md)

[Set-AzureWebsite](./Set-AzureWebsite.md)


