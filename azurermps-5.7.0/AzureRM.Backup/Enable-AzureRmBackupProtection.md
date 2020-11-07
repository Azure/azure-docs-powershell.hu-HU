---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: DD150A2C-27D5-4119-9B43-FAB82F9F7D5B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/enable-azurermbackupprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Enable-AzureRmBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Enable-AzureRmBackupProtection.md
ms.openlocfilehash: 87f269042b6d0f660f621a865dda7619afd9be5e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679300"
---
# Enable-AzureRmBackupProtection

## Áttekintés
Egy elem társítása az Azure Backup Protection házirenddel

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Enable-AzureRmBackupProtection -Policy <AzureRMBackupProtectionPolicy>
 [-Item] <AzureRMBackupContainerContextObject> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
Az **enable-AzureRmBackupProtection** parancsmag egy, az Azure Backup Protection házirenddel rendelkező elemet társít.
A védelmi házirend engedélyezéséhez egy meglévő biztonsági elemmel és egy meglévő házirenddel kell rendelkeznie.
Mindkettőnek ugyanahhoz a biztonságimásolat-tárolóhoz kell tartoznia.
A biztonsági mentés ütemezése az elem teljes eredeti példányát és a későbbi biztonsági mentések növekményes másolatát használja.

## Példák

### 1. példa: védelem engedélyezése Azure virtuális gépen
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Policy = Get-AzureRmBackupProtectionPolicy -Vault $Vault -Name "DefaultPolicy"
PS C:\> Get-AzureRmBackupContainer -Vault $Vault -Type AzureVM -Status Registered | Get-AzureRmBackupItem | Enable-AzureRmBackupProtection -Policy $Policy
WorkloadName    Operation        Status          StartTime              EndTime
------------    ---------        ------          ---------              -------
co03-vm         ConfigureBackup  Completed       26-Aug-15 12:19:49 PM  26-Aug-15 12:19:54 PM
```

Az első parancs a Vault03 nevű boltozatot a **Get-AzureRmBackupVault** parancsmag használatával kapja.
A parancs az objektumot a $Vault változóban tárolja.

A második parancs beolvassa a DefaultPolicy nevű biztonsági házirendet a $Vault boltozatához.
A parancs az objektumot a $Policy változóban tárolja.

A végleges parancs a pipeline operátorral adja át az értékeket az egyik parancsmagból a következőre.
A Get-AzureRmBackupContainer parancsmag használatával kap egy tárolót.
A parancs a Get-AzureRmBackupItem parancsmag használatával kapja meg az adott tároló biztonsági mentési elemét.
Az aktuális parancsmag lehetővé teszi, hogy az $Policy-ban tárolt házirend a parancs által az adott parancsmaghoz átadott elemre kerüljön.

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

### -Elem
Annak a biztonsági másolatnak a biztonsági másolatát adja meg, amelyhez ez a parancsmag engedélyezi a védelmet.
Ha **AzureRmBackupItem** szeretne beolvasni, használja az Get-AzureRmBackupItem parancsmagot.

```yaml
Type: AzureRMBackupContainerContextObject
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Házirend
Azt a védelmi házirendet adja meg, amelyet a parancsmag társít egy elemhez.
**AzureRmBackupProtectionPolicy** objektum beolvasásához használja az Get-AzureRmBackupProtectionPolicy parancsmagot.

```yaml
Type: AzureRMBackupProtectionPolicy
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### AzureRmBackupItem

## KIMENETEK

### AzureRmBackupJob

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Backup-AzureRmBackupItem](./Backup-AzureRmBackupItem.md)

[Get-AzureRmBackupItem](./Get-AzureRmBackupItem.md)

[Get-AzureRmBackupProtectionPolicy](./Get-AzureRmBackupProtectionPolicy.md)


