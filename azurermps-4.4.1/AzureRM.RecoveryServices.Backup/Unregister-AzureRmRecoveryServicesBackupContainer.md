---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: A10DC2A2-A732-416F-9C68-6533C143AE8F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Unregister-AzureRmRecoveryServicesBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Unregister-AzureRmRecoveryServicesBackupContainer.md
ms.openlocfilehash: c5ab79ca42096ab93102be1288c772cab1ac01f8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679372"
---
# Unregister-AzureRmRecoveryServicesBackupContainer

## Áttekintés
Windows-kiszolgáló vagy más tároló regisztrációjának megszüntetése a boltozatról.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Unregister-AzureRmRecoveryServicesBackupContainer [-Container] <ContainerBase>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **unregister-AzureRmRecoveryServicesBackupContainer** parancsmag a Windows Server vagy más biztonsági tárolók nyilvántartását a boltozatról.
Ez a parancsmag eltávolítja a tárolóra mutató hivatkozást a boltozatról.
A tároló törlése előtt törölnie kell az adott tárolóhoz társított összes védett adatot.

Állítsa be a boltozat környezetét az Set-AzureRmRecoveryServicesVaultContext parancsmag használatával, mielőtt az aktuális parancsmagot használja.

## Példák

### 1. példa: Windows-kiszolgáló regisztrációjának megszüntetése a boltozatról
```
PS C:\>$Cont = Get-AzureRmRecoveryServicesContainer -ContainerType "Windows" -BackupManagementType MARS -Name "server01.contoso.com"
PS C:\> Unregister-AzureRmRecoveryServicesBackupContainer -Container $Cont
```

Az első parancs beolvassa a server01.contoso.com nevű Windows-tárolót, amely a boltozatban van regisztrálva, majd a $Cont változóban tárolja.

A második parancs az Azure Backup Vault-ról regisztrálja a megadott Windows Servert.

## PARAMÉTEREK

### -Container
Egy tartalék tároló objektumot ad meg a regisztráció törléséhez.
**BackupContainer** objektum beolvasásához használja az Get-AzureRmRecoveryServicesBackupContainer parancsmagot.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase
Parameter Sets: (All)
Aliases: 

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

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureRmRecoveryServicesBackupContainer](./Get-AzureRmRecoveryServicesBackupContainer.md)


