---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: FD43AFDA-E37D-4B5E-8EB5-CC2CF1E36AFA
online version: ''
schema: 2.0.0
ms.openlocfilehash: ea09f45de760de7ff02a768094c6f98c3f2a0643
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015974"
---
# New-AzureSiteRecoveryVault

## Áttekintés
Webhely-helyreállítási szolgáltatások boltozatának létrehozása.

## SZINTAXISA

```
New-AzureSiteRecoveryVault -Name <String> -Location <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
A **New-AzureSiteRecoveryVault** parancsmag létrehoz egy Azure site Recovery Services Vault-t.

## Példák

### 1. példa: boltozat létrehozása
```
PS C:\> New-AzureSiteRecoveryVault -Location "West US" -Name "ContosoVault" 
Response
--------
Vault has been created
```

Ez a parancs létrehoz egy ContosoVault nevű boltozatot a Nyugat-amerikai térségben.

## PARAMÉTEREK

### -Hely
A földrajzi helyet adja meg.

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

### -Name (név)
A boltozat nevét adja meg.

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

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureSiteRecoveryVault](./Get-AzureSiteRecoveryVault.md)


