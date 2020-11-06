---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 015E3BC9-C535-4EA2-8A30-C728385DBFF8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/new-azurermbackupvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/New-AzureRmBackupVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/New-AzureRmBackupVault.md
ms.openlocfilehash: ad3619d2d0fcb9b60639a19b0c7d3fea45833857
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498471"
---
# New-AzureRmBackupVault

## Áttekintés
Létrehoz egy biztonságimásolat-tárolót.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
New-AzureRmBackupVault [-ResourceGroupName] <String> [-Name] <String> [-Region] <String>
 [[-Storage] <AzureBackupVaultStorageType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **New-AzureRmBackupVault** parancsmag egy Azure Backup boltozatot hoz létre.
Ez a parancsmag egy **AzureRmBackupVault** objektumot ad eredményül, amely a boltozat entitásra mutató hivatkozásként működik.

## Példák

### 1. példa: biztonságimásolat-tároló létrehozása
```
PS C:\>New-AzureRmBackupVault -ResourceGroupName "ResourceGroup01" -Name "Vault03" -Region "westus"
ResourceId        : /subscriptions/4bfbe168-f42a-4a06-8f5a-331cad1f497e/resourceGroups/ResourceGroup01/providers/Microsoft.Backup
                    /BackupVault/Vault03
Name              : Vault03
ResourceGroupName : ResourceGroup01
Region            : westus
Storage           : GeoRedundant
```

Ez a parancs létrehoz egy Vault03 nevű Azure Backup Vault-t.
A boltozat a ResourceGroup01 nevű erőforrás-csoportban található a West US régióban.
A boltozat az alapértelmezett GeoRedundant-tárolási típust használja.

### 2. példa: helyileg redundáns tárterületet használó biztonságimásolat-tároló létrehozása
```
PS C:\>New-AzureRmBackupVault -ResourceGroupName "ResourceGroup02" -Name "Vault03" -Region "westus" -Storage LocallyRedundant
ResourceId        : /subscriptions/4bfbe168-f42a-4a06-8f5a-331cad1f497e/resourceGroups/ResourceGroup02/providers/Microsoft.Backup
                    /BackupVault/Vault03
Name              : Vault03
ResourceGroupName : ResourceGroup02
Region            : westus
Storage           : LocallyRedundant
```

Ez a parancs létrehoz egy Vault03 nevű Azure Backup Vault-t.
A boltozat a ResourceGroup02 nevű erőforrás-csoportban található a West US régióban.
A boltozat a LocallyRedundant-tároló típusát használja.

## PARAMÉTEREK

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés

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

### -Name (név)
Az Azure Backup Vault nevét adja meg.
A névnek egyedinek kell lennie egy erőforrás-csoportban.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Region (régió)
Itt adhatja meg azt az Azure-körzetet, amelyben a biztonságimásolat-tároló található.
A hibrid biztonságimásolat-forgatókönyvek esetében azt javasoljuk, hogy a helyi kiszolgálóhoz közeli területen hozzon létre egy boltozatot a késés csökkentéséhez.
Az Azure Infrastructure biztonsági másolatának (IaaS) virtuális gépei esetén a boltozat a helyi virtuális gépek felderítési pontja lesz.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Annak a meglévő Azure erőforrás-csoportnak a nevét adja meg, amelyben ez a parancsmag létrehoz egy biztonságimásolat-tárolót.
Erőforráscsoport létrehozásához használja az New-AzureRMResourceGroup parancsmagot.
Az erőforráscsoport és az Azure Backup Vault nem kell ugyanazon a területen lennie.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tárterület
A biztonsági másolat adatainak tárolási típusát adja meg.
A paraméter elfogadható értékei a következők: LocallyRedundant és GeoRedundant.
Az alapértelmezett érték a GeoRedundant.

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureBackupVaultStorageType
Parameter Sets: (All)
Aliases:
Accepted values: GeoRedundant, LocallyRedundant

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Nincs

## KIMENETEK

### Microsoft. Azure. Command. AzureBackup. models. AzureRMBackupVault

## MEGJEGYZI
* Nincs

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureRmBackupVault](./Get-AzureRmBackupVault.md)

[Remove-AzureRmBackupVault](./Remove-AzureRmBackupVault.md)

[Set-AzureRmBackupVault](./Set-AzureRmBackupVault.md)


