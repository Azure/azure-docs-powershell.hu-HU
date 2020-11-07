---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 1097FF29-1C23-4960-930C-5C1227419359
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupContainer.md
ms.openlocfilehash: c47c3e51d970302281af5a7ae3a6175f4af79739
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679527"
---
# Get-AzureRmRecoveryServicesBackupContainer

## Áttekintés
Kapja a biztonsági másolat tárolóit.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Get-AzureRmRecoveryServicesBackupContainer [-ContainerType] <ContainerType> [[-BackupManagementType] <String>]
 [[-Name] <String>] [[-FriendlyName] <String>] [[-ResourceGroupName] <String>]
 [[-Status] <ContainerRegistrationStatus>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Leírás
A **Get-AzureRmRecoveryServicesBackupContainer** parancsmag biztonsági tárolót kap.
A biztonságimásolat-tároló a biztonsági elemekként modellezett adatforrásokat ágyazza be.
Állítsa be a boltozat környezetét az Set-AzureRmRecoveryServicesVaultContext parancsmag használatával, mielőtt az aktuális parancsmagot használja.

## Példák

### 1. példa: adott tároló beszerzése
```
PS C:\>Get-AzureRmRecoveryServicesContainer -ContainerType "AzureVM" -Status "Registered" -Name "V2VM";
```

Ez a parancs a AzureVM V2VM nevű tárolót kapja.

### 2. példa: egy adott típus minden tárolójának beolvasása
```
PS C:\>Get-AzureRmRecoveryServicesBackupContainer -ContainerType Windows -BackupManagementType MARS
```

Ez a parancs az Azure Backup Agent által védett Windows-tárolókat kapja meg.
A *BackupManagementType* paraméter csak a Windows-tárolók esetében szükséges.

## PARAMÉTEREK

### -BackupManagementType
A biztonságimásolat-kezelés típusát adja meg.
A paraméter elfogadható értékei a következők:
- AzureVM
- MARS
- AzureSQL
- AzureStorage

Ezzel a paraméterrel megkülönböztetheti a MARS-ügynökkel vagy más tartalék motorokkal mentett Windows-gépeket.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, MARS, AzureSQL, AzureStorage

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ContainerType
A biztonságimásolat-tároló típusát adja meg.
A paraméter elfogadható értékei a következők:
- AzureVM 
- Windows
- AzureSQL
- AzureStorage

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, Windows, AzureSQL, AzureStorage

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Típusú megjelenített
A beolvasott tároló rövid nevét adja meg.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (név)
A beolvasott tároló nevét adja meg.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Az erőforráscsoport nevét adja meg.
Ez a paraméter csak az Azure Virtual Machines esetén használható.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Állapot
A tároló regisztrációjának állapotát adja meg.
A paraméter elfogadható értékei a következők:
- Regisztrált

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerRegistrationStatus
Parameter Sets: (All)
Aliases:
Accepted values: Registered

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VaultId
A helyreállítási szolgáltatások boltozatának azonosítója

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### System. String
Paraméterek: VaultId (ByValue)

## KIMENETEK

### Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. ContainerBase

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureRmRecoveryServicesBackupItem](./Get-AzureRmRecoveryServicesBackupItem.md)

[Get-AzureRmRecoveryServicesBackupManagementServer](./Get-AzureRmRecoveryServicesBackupManagementServer.md)

[Regisztráció törlése – AzureRmRecoveryServicesBackupContainer](./Unregister-AzureRmRecoveryServicesBackupContainer.md)


