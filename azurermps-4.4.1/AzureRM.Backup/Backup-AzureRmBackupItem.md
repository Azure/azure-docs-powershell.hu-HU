---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 9FF4F649-F50C-4C27-842F-1CD6C5BC7A2B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Backup-AzureRmBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Backup-AzureRmBackupItem.md
ms.openlocfilehash: 1cb5ccf56a2ef6888231ca81df0e352f5d505e7a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493587"
---
# Backup-AzureRmBackupItem

## Áttekintés
Biztonságimásolat-elem biztonsági másolatának indítása

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Backup-AzureRmBackupItem [-Item] <AzureRMBackupItem> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Leírás
A **Backup-AzureRmBackupItem** parancsmag egy olyan védett Azure biztonsági másolat biztonsági másolatát indítja el, amely nincs a biztonsági ütemtervhez kötve.
A kezdeti biztonsági mentés után azonnal elvégezheti a biztonsági mentést, ha az ütemezett biztonsági mentés után nem tud biztonsági másolatot indítani.

Ha egy meglévő biztonsági mentési feladat fut, ez a parancsmag nem hajtható végre.

## Példák

### 1. példa: a virtuális gép biztonsági mentése
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Container = Get-AzureRmBackupContainer -Vault $Vault -Type AzureVM -Name "DPMSERVER.CONTOSO.COM"
PS C:\> Get-AzureRmBackupItem -Container $Container | Backup-AzureRmBackupItem
WorkloadName    Operation       Status          StartTime              EndTime
------------    ---------       ------          ---------              -------
co03-vm         Backup          InProgress      26-Aug-15 12:24:01 PM  01-Jan-01 12:00:00 AM
```

Az első parancs a Vault03 nevű boltozatot az Get-AzureRmBackupVault parancsmag segítségével kapja meg.
A parancs az objektumot a $Vault változóban tárolja.

A második parancs egy olyan tárolót kap, amelyben a megadott név szerepel a boltozatban $Vault a Get-AzureRmBackupContainer parancsmag használatával.
A parancs az objektumot a $Container változóban tárolja.

Az utolsó parancs a Get-AzureRmBackupItem parancsmag használatával kapja meg az $Container biztonsági mentési elemeit.
A parancs a csővezeték-kezelő segítségével átadja az elemeket az aktuális parancsmagnak.
Az aktuális parancsmag a tárolóban lévő virtuális gép biztonsági mentését indítja el.

## PARAMÉTEREK

### -Elem
Annak a biztonságimásolat-elemnek a megadása, amelyhez ez a parancsmag elindítja a biztonsági mentési műveletet.

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupItem
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
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

### AzureRMBackupItem

## KIMENETEK

### AzureRmBackupJob

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureRmBackupItem](./Get-AzureRmBackupItem.md)

[Get-AzureRmBackupVault](./Get-AzureRmBackupVault.md)

[Restore-AzureRmBackupItem](./Restore-AzureRmBackupItem.md)


