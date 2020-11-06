---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 4B7ACEC8-29BB-4791-8087-801300F246B4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackupmanagementserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupManagementServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupManagementServer.md
ms.openlocfilehash: 0dac27b7e17a9336db198906cdfb60fb15738795
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493073"
---
# Get-AzureRmRecoveryServicesBackupManagementServer

## Áttekintés
Megkapja a SCDPM és az Azure Backup Management kiszolgálókat.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Get-AzureRmRecoveryServicesBackupManagementServer [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Leírás
A **Get-AzureRmRecoveryServicesBackupManagementServer** parancsmag a boltívben regisztrált biztonságimásolat-kezelési kiszolgálók listáját kapja.

A biztonságimásolat-kezelési kiszolgálók két típusa van: a System Center Data Protection Manager (SCDPM) és az Azure Backup Management Servers.
A biztonságimásolat-kezelési kiszolgálók külön vannak telepítve a biztonságimásolat-hangszerelések kezeléséhez.

Állítsa be a boltozat környezetét az Set-AzureRmRecoveryServicesVaultContext parancsmag használatával, mielőtt az aktuális parancsmagot használja.

## Példák

### Példa 1: a biztonsági másolatok kezelésének összes kiszolgálójának beolvasása
```
PS C:\>Get-AzureRmRecoveryServicesBackupManagementServer
```

Ez a parancs a boltozattal regisztrált összes biztonságimásolat-kezelési kiszolgálót megkapja.

## PARAMÉTEREK

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (név)
A beolvasott biztonságimásolat-kezelési kiszolgáló nevét adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Nincs
Ez a parancsmag nem fogadja el a bevitelt.

## KIMENETEK

### Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. BackupEngineBase

### System. Collections. Generic. IList ' 1 [Microsoft. Azure. commands. RecoveryServices. backup. Parancsmags. models. BackupEngineBase]

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Regisztráció törlése – AzureRmRecoveryServicesBackupManagementServer](./Unregister-AzureRmRecoveryServicesBackupManagementServer.md)


