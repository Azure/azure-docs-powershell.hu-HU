---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 43E5EC54-5DF4-4D32-8657-D7039DD04513
online version: ''
schema: 2.0.0
ms.openlocfilehash: 68152b80711544a76abc17f697fe9730d1a6f1bc
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015892"
---
# New-AzureSiteRecoverySite

## Áttekintés
Webhely-helyreállítási webhelyet hoz létre.

## SZINTAXISA

```
New-AzureSiteRecoverySite -Name <String> [-Vault <ASRVault>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
A **New-AzureSiteRecoverySite** parancsmag létrehoz egy Azure webhely-helyreállítási webhelyet az aktuális boltívben.

## Példák

### 1. példa: webhely-helyreállítási webhely létrehozása
```
PS C:\> New-AzureSiteRecoverySite -Name "RecoverySite07"
```

Ez a parancs létrehoz egy RecoverySite07 nevű webhely-helyreállítási webhelyet.

## PARAMÉTEREK

### -Name (név)
A webhely nevét adja meg.

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

### -Boltozat
Azt a boltozatot adja meg, amelybe a webhelyet létre szeretné hozni.
Ha **ASRVault** objektumot szeretne beolvasni, használja a **Get-AzureSiteRecoveryVault** parancsmagot.

```yaml
Type: ASRVault
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

[Get-AzureSiteRecoveryVault](./Get-AzureSiteRecoveryVault.md)

[Get-AzureSiteRecoverySite](./Get-AzureSiteRecoverySite.md)


