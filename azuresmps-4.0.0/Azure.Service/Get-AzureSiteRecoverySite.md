---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 6DD09F28-BFAE-4F9B-BF9C-F09767F9BFEF
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9151cb5a64b5873ab1c63420a97eb2e7bcffc0ce
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015577"
---
# Get-AzureSiteRecoverySite

## Áttekintés
Beilleszti a Hyper-V-webhelyeket egy webhely-helyreállítási Vault-webhelyről.

## SZINTAXISA

```
Get-AzureSiteRecoverySite [-Vault <ASRVault>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
A **Get-AzureSiteRecoverySite** parancsmag a Hyper-V-webhelyeket egy Azure-webhely helyreállítási pincéjében kapja.

## Példák

### 1. példa: helyreállítási webhelyek beszerzése
```
PS C:\> Get-AzureSiteRecoverySite
Type                                    Name                                    ID
----                                    ----                                    --
HyperVSite                              RecoverySite07                          f16829b4-5b01-4209-a6cf-8e0aff1fe328
```

Ez a parancs az aktuális boltozat helyreállítási webhelyeit kapja.

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

### -Boltozat
A webhelyek beolvasására szolgáló boltozatot adja meg.
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

[Új – AzureSiteRecoverySite](./New-AzureSiteRecoverySite.md)


