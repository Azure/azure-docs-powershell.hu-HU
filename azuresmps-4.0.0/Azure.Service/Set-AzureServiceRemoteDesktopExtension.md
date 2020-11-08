---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 5C8B1482-80B0-4060-A35D-E9D394156886
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9a6303e685ea02408772a237c6b5f154764107e4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015813"
---
# Set-AzureServiceRemoteDesktopExtension

## Áttekintés
Engedélyezi a távoli asztali bővítményt meghatározott szerepkör (ek) vagy az összes szerepkör egy telepített szolgáltatásban vagy a központi telepítésben.

## SZINTAXISA

### SetExtension (alapértelmezett)
```
Set-AzureServiceRemoteDesktopExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [[-X509Certificate] <X509Certificate2>] [[-ThumbprintAlgorithm] <String>] [-Credential] <PSCredential>
 [[-Expiration] <DateTime>] [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### SetExtensionUsingThumbprint
```
Set-AzureServiceRemoteDesktopExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [-CertificateThumbprint] <String> [[-ThumbprintAlgorithm] <String>] [-Credential] <PSCredential>
 [[-Expiration] <DateTime>] [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## Leírás
A **set-AzureServiceRemoteDesktopExtension** parancsmag a megadott szerepkörökre vagy a telepített szolgáltatásokban vagy a telepítéshez tartozó összes szerepkörre vonatkozóan engedélyezi a távoli asztali bővítményt.

## Példák

### 1. példa: a távoli asztali bővítmény engedélyezése
```
PS C:\> Set-AzureServiceRemoteDesktopExtension -ServiceName $svc -Credentials $creds
```

Ez a parancs engedélyezi a megadott szolgáltatáshoz tartozó távoli asztali bővítményt.

### 2. példa: a távoli asztali bővítmény engedélyezése meghatározott szerepkörhöz
```
PS C:\> Set-AzureServiceRemoteDesktopExtension -ServiceName $svc -Credentials $creds -Role "WebRole1"
```

Ez a parancs lehetővé teszi a megadott szolgáltatáshoz és szerepkörhöz tartozó távoli asztali bővítményt.

## PARAMÉTEREK

### -CertificateThumbprint
A magánjellegű konfiguráció titkosításához használt tanúsítvány-ujjlenyomatot adja meg.
Ez a tanúsítvány már létezik a tanúsítványtárolóban.
Ha nem ad meg tanúsítványt, a parancsmag létrehoz egy tanúsítványt.

```yaml
Type: String
Parameter Sets: SetExtensionUsingThumbprint
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Hitelesítő adatok
Adja meg a távoli asztalhoz engedélyezni kívánt hitelesítő adatokat.
A hitelesítő adatok tartalmazzák a felhasználónevet és a jelszót.

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Lejárat
Megadja azt a dátum-idő objektumot, amely lehetővé teszi, hogy a felhasználó megadhatja, hogy mikor jár le a felhasználói fiók.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ExtensionId
A bővítmény AZONOSÍTÓját adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -InformationAction
Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.

A paraméter elfogadható értékei a következők:

- Folytassa
- Mellőzése
- Érdeklődni
- SilentlyContinue
- állj
- Felfüggesztheti

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
Egy információs változót ad meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
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

### -Role (szerepkör)
Azt a választható szerepköröket adja meg, amelyekhez a távoli asztali konfigurációt meg szeretné adni.
Ha ez a paraméter nincs megadva, a program az összes szerepkör alapértelmezett konfigurációjának megfelelően alkalmazza a távoli asztali konfigurációt.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Szolgáltatásnév
A központi üzembe helyezés Azure-szolgáltatás nevét adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Slot
A módosítani kívánt központi verzió környezetét adja meg.
A paraméter elfogadható értékei a következők: termelés, megállóhelyek.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ThumbprintAlgorithm
Egy ujjlenyomat-ujjlenyomat-algoritmust ad meg, amely a tanúsítvány meghatározásához használt ujjlenyomatmal van meghatározva.
Ez a paraméter nem kötelező, és az alapértelmezett érték az SHA1.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Verzió
A bővítmény verziószámát adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -X509Certificate
Itt adhatja meg azt a x509-tanúsítványt, amelyet a rendszer automatikusan feltölt a felhőalapú szolgáltatásba, és a kiterjesztés privát konfigurációjának titkosítására szolgál.

```yaml
Type: X509Certificate2
Parameter Sets: SetExtension
Aliases: 

Required: False
Position: 3
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

[Get-AzureServiceRemoteDesktopExtension](./Get-AzureServiceRemoteDesktopExtension.md)


