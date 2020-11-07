---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 9882F1A5-6FFB-4DAF-8ED5-B14596BC939D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/get-azurermbackupvaultcredentials
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupVaultCredentials.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupVaultCredentials.md
ms.openlocfilehash: e6e56b1b9026aa0bba4442edc9652372505983ac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679297"
---
# Get-AzureRmBackupVaultCredentials

## Áttekintés
A pince hitelesítő adatait tartalmazó fájl letöltése a biztonsági mentéshez.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Get-AzureRmBackupVaultCredentials [-TargetLocation] <String> [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **Get-AzureRmBackupVaultCredentials** parancsmag letölti a Vault hitelesítő adatait tartalmazó fájlt az Azure Backup Vault-hoz.

Biztonsági másolat: egy kiszolgáló csatlakoztatása az Azure Backup Vault-hoz, és regisztrálja a kiszolgálóját a boltozat hitelesítő adataival.
Ahhoz, hogy biztonsági másolatot küldene a boltozatról, regisztrálnia kell a kiszolgálót.

## Példák

## PARAMÉTEREK

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés

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

### -TargetLocation
A cél elérési útvonalát adja meg, ahol ez a parancsmag tárolja a Vault hitelesítő adatait tartalmazó fájlt.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Boltozat
Annak a biztonságimásolat-tárolónak a megadása, amelyhez ez a parancsmag a Vault-hitelesítőadat-fájlt kapja.
**AzureRmBackupVault** objektum beolvasásához használja az Get-AzureRmBackupVault parancsmagot.

```yaml
Type: AzureRMBackupVault
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### AzureRMBackupVault

## KIMENETEK

### Karakterlánc
Ez a parancsmag a Vault hitelesítőadat-fájl nevét adja eredményül.

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureRmBackupVault](./Get-AzureRmBackupVault.md)


