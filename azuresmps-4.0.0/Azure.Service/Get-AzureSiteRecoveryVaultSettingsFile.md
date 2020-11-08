---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: AFAA1BDF-3F6A-437A-ADC2-C5EBD970F57D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 94e86fdb7f1e995af71e09bdce17754b11819bec
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016564"
---
# Get-AzureSiteRecoveryVaultSettingsFile

## Áttekintés
Megkapja a webhely-helyreállítási Vault beállítási fájlját.

## SZINTAXISA

### ByParam (alapértelmezett)
```
Get-AzureSiteRecoveryVaultSettingsFile -Name <String> -Location <String> [-SiteName <String>]
 [-SiteId <String>] [-Path <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByObject
```
Get-AzureSiteRecoveryVaultSettingsFile -Vault <ASRVault> [-Site <ASRSite>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Leírás
A **Get-AzureSiteRecoveryVaultSettingsFile** parancsmag az Azure-webhely helyreállítási boltozatának beállítási fájlját kapja meg.

## Példák

### Példa 1: a beállítások fájl beszerzése egy boltozathoz
```
PS C:\> $Vault = Get-AzureSiteRecoveryVault -Name "ContosoVault"
PS C:\> Get-AzureSiteRecoveryVaultSettingsFile -Vault $Vault
FilePath 
-------- 
C:\Users\ContosoAdmin\ContosoVault_2015-02-02T05-39-23.VaultCredentials
```

Az első parancs a **Get-AzureSiteRecoveryVault** parancsmaggal kapja meg a ContosoVault nevű aktív Azure site Recovery Vault nevet.
A parancs a $Vault változóban tárolja a boltozatot.

A második parancs beolvassa a $Vault-ban tárolt Vault-tároló beállítási fájlját.

## PARAMÉTEREK

### -Hely
Azt a földrajzi helyet adja meg, ahová a boltozat tartozik.

```yaml
Type: String
Parameter Sets: ByParam
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
Parameter Sets: ByParam
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Path (elérési út)
A webhely-helyreállítási boltozat beállítási fájljának elérési útját adja meg.
Ha helyileg szeretné menteni a fájlt, töltse le a webhely-helyreállítási központ webhelyről a parancs futásának befejezése után.

```yaml
Type: String
Parameter Sets: ByParam
Aliases: 

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

### -Webhely
Itt adhatja meg azt a webhelyet, amelyhez beállítási fájlt szeretne beszerezni.
Ha egy **webhely** -objektumot szeretne beolvasni, használja a **Get-AzureSiteRecoverySite** parancsmagot.

```yaml
Type: ASRSite
Parameter Sets: ByObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Helyazonosító
Egy webhely AZONOSÍTÓját adja meg.

```yaml
Type: String
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteName
A webhely nevét adja meg.

```yaml
Type: String
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Boltozat
A webhely boltozatát adja meg.

```yaml
Type: ASRVault
Parameter Sets: ByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureSiteRecoverySite](./Get-AzureSiteRecoverySite.md)

[Get-AzureSiteRecoveryVault](./Get-AzureSiteRecoveryVault.md)

[Get-AzureSiteRecoveryVaultSettings](./Get-AzureSiteRecoveryVaultSettings.md)

[Importálás – AzureSiteRecoveryVaultSettingsFile](./Import-AzureSiteRecoveryVaultSettingsFile.md)


