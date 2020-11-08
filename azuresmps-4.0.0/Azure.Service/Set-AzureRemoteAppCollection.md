---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 14B4050D-3597-4760-A152-82617B88078D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 291ea94bbdfff1da8d658074ebfb72df8943f0e8
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016053"
---
# Set-AzureRemoteAppCollection

## Áttekintés
Egy RemoteApp-gyűjtemény tulajdonságait állítja be.

## SZINTAXISA

### DescriptionOnly (alapértelmezett)
```
Set-AzureRemoteAppCollection [-CollectionName] <String> -Description <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### PlanOnly
```
Set-AzureRemoteAppCollection [-CollectionName] <String> -Plan <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### DomainJoined
```
Set-AzureRemoteAppCollection [-CollectionName] <String> -Credential <PSCredential> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### RdpPropertyOnly
```
Set-AzureRemoteAppCollection [-CollectionName] <String> -CustomRdpProperty <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### AclLevelOnly
```
Set-AzureRemoteAppCollection [-CollectionName] <String> -AclLevel <CollectionAclLevel>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
A **set-AzureRemoteAppCollection** parancsmag az Azure RemoteApp-gyűjtemény tulajdonságait állítja be.

## Példák

## PARAMÉTEREK

### -AclLevel
A gyűjtemény hozzáférés-vezérlési lista (ACL) szintjét adja meg.
A paraméter elfogadható értékei a következők: gyűjtemény és alkalmazás.

```yaml
Type: CollectionAclLevel
Parameter Sets: AclLevelOnly
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### -Hitelesítő adatok
Megadja egy olyan szolgáltatásfiók hitelesítő adatait, amely engedéllyel rendelkezik az Azure RemoteApp kiszolgálókhoz való csatlakozáshoz a tartományához.
Ha **PSCredential** objektumot szeretne beolvasni, használja a **Get-hitelesítőadat** parancsmagot.

```yaml
Type: PSCredential
Parameter Sets: DomainJoined
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CustomRdpProperty
Az RDP-tulajdonságokat adja meg, amelyek segítségével konfigurálhatók a meghajtó átirányítása és az egyéb beállítások. További információt az [RDP-beállítások a Windows Server Remote Desktop Services szolgáltatáshoz](https://technet.microsoft.com/library/ff393699(v=ws.10).aspx) című témakörben talál `(https://technet.microsoft.com/library/ff393699(v=ws.10).aspx)` .  

```yaml
Type: String
Parameter Sets: RdpPropertyOnly
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Leírás
A gyűjtemény rövid leírását adja meg.

```yaml
Type: String
Parameter Sets: DescriptionOnly
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Terv
Az Azure RemoteApp-gyűjtemény csomagját adja meg, amely meghatározza a használati korlátozásokat.
Az elérhető csomagok megtekintéséhez használja a **Get-AzureRemoteAppPlan** .

```yaml
Type: String
Parameter Sets: PlanOnly
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

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureRemoteAppCollection](./Get-AzureRemoteAppCollection.md)

[Új – AzureRemoteAppCollection](./New-AzureRemoteAppCollection.md)

[Update-AzureRemoteAppCollection](./Update-AzureRemoteAppCollection.md)


