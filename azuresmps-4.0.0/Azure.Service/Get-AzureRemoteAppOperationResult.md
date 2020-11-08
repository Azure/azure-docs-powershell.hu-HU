---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 4136A0EF-2682-4B17-BC37-53CD43F5940B
online version: ''
schema: 2.0.0
ms.openlocfilehash: e7b884da0395313ddc8aa4d0e301b37849ec3d57
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016322"
---
# Get-AzureRemoteAppOperationResult

## Áttekintés
Beolvassa az Azure RemoteApp művelet eredményét.

## SZINTAXISA

```
Get-AzureRemoteAppOperationResult [-TrackingId] <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
A **Get-AzureRemoteAppOperationResult** parancsmag beolvassa az Azure-alapú, hosszú ideig futó Azure-RemoteApp műveletek eredményét.
Az Azure RemoteApp hosszú futású műveleteket végez sok olyan műveletnél, amely a szolgáltatás általi feldolgozást igényel, és nem tud azonnal visszaadni.
Példák a nyomkövetési azonosítókat tartalmazó parancsmagokra: **Update-AzureRemoteAppCollection** , **set-AzureRemoteAppWorkspace** , **Disconnect-AzureRemoteAppSession** és egyebek.

## Példák

### 1. példa: a nyomkövetési azonosító használata a műveleti eredmény eléréséhez
```
PS C:\> $result = New-AzureRemoteAppCollection -CollectionName Contoso -ImageName "Windows Server 2012 R2" -Plan Standard -Location "West US" -Description CloudOnly
PS C:\> Get-AzureRemoteAppOperationResult -TrackingId $result.Tracking
```

Ez a parancs az Azure RemoteApp műveletből visszaadott nyomkövetési azonosítót menti.
A rendszer átadja a nyomkövetési azonosítót a **Get-AzureRemoteAppOperationResult** az alábbi parancsban.

## PARAMÉTEREK

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

### -TrackingId
Egy művelet nyomkövetési AZONOSÍTÓját adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
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

[Disconnect-AzureRemoteAppSession](./Disconnect-AzureRemoteAppSession.md)

[Set-AzureRemoteAppWorkspace](./Set-AzureRemoteAppWorkspace.md)

[Update-AzureRemoteAppCollection](./Update-AzureRemoteAppCollection.md)


