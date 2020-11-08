---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 5875D72D-B8DB-4F72-BF5C-242D40A13DE1
online version: ''
schema: 2.0.0
ms.openlocfilehash: d8f5dc0762021db2545b73a9ba7b9d7c53d435ce
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016260"
---
# Import-AzureSiteRecoveryVaultSettingsFile

## Áttekintés
Webhely-helyreállítási Vault-beállítási fájl importálása

## SZINTAXISA

```
Import-AzureSiteRecoveryVaultSettingsFile -Path <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
Az **import-AzureSiteRecoveryVaultSettingsFile** parancsmag az Azure webhely-helyreállítási tároló beállítási fájljába importálja az aktuális munkamenetben az azt követő helyreállítási műveletekhez tartozó Vault-környezet beállítását.

## Példák

### 1. példa: Vault-beállítási fájl importálása
```
PS C:\> Import-AzureSiteRecoveryVaultSettingsFile -Path "C:\Users\Contoso\Contosovault Monday, October 6, 2014.VaultCredentials"
VERBOSE: Vault Settings File path: C:\Users\Contoso\Contosovault Monday, October 6, 2014.VaultCredentials

ResourceName                                                CloudServiceName
------------                                                ----------------
Contosovault                                                RecoveryServices-6JP23WE3SKKOM5AFQG2YQAI22MNOWK52QDKWMUP...
```

Ez a parancs a boltozat beállítási fájlját a megadott elérési útra importálja.

## PARAMÉTEREK

### -Path (elérési út)
A webhely-helyreállítási boltozat beállítási fájljának elérési útját adja meg.
Ez a fájl letölthető a webhely-helyreállítási Vault portálról, és helyben tárolható.

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

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureSiteRecoveryVaultSettings](./Get-AzureSiteRecoveryVaultSettings.md)

[Get-AzureSiteRecoveryVaultSettingsFile](./Get-AzureSiteRecoveryVaultSettingsFile.md)


