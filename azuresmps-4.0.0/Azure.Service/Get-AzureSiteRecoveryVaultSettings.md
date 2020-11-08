---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 305511DC-477F-4A33-8B16-063B39B19ED3
online version: ''
schema: 2.0.0
ms.openlocfilehash: cd96d7dd63791c5ef2e4a8a036949823d5c73313
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016566"
---
# Get-AzureSiteRecoveryVaultSettings

## Áttekintés
A webhely-helyreállítási boltozat beállításait kapja meg.

## SZINTAXISA

```
Get-AzureSiteRecoveryVaultSettings [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
A **Get-AzureSiteRecoveryVaultSettings** parancsmag a jelenlegi Azure-webhely helyreállítási boltozatához kapcsolódó beállításokat kapja meg.

## Példák

### Példa 1: beállítási adatok beszerzése
```
PS C:\> Get-AzureSiteRecoveryVaultSettings
ResourceName                                                CloudServiceName
------------                                                ----------------
ContosoVault                                                RecoveryServices-6JP23WE3SKKOM5AFQG2YQAI22MNOWK52QDKWMUP...
```

Ez a parancs a jelenlegi Azure webhely-helyreállítási boltozat beállításaival kapcsolatos információkat kapja meg.

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

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureSiteRecoveryVaultSettingsFile](./Get-AzureSiteRecoveryVaultSettingsFile.md)

[Importálás – AzureSiteRecoveryVaultSettingsFile](./Import-AzureSiteRecoveryVaultSettingsFile.md)


