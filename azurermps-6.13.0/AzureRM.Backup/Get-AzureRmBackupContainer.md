---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: F3774658-A5E4-40BE-9A85-B33C70BC0A09
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/get-azurermbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupContainer.md
ms.openlocfilehash: e20276d8a2dfec8ffb39665e5122cfe4be74dc42
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672492"
---
# Get-AzureRmBackupContainer

## Áttekintés
Kapja a biztonsági másolat tárolóit.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Get-AzureRmBackupContainer [-Name <String>] -Type <AzureBackupContainerType>
 [-ManagedResourceGroupName <String>] [-Status <AzureBackupContainerRegistrationStatus>]
 [-Vault] <AzureRMBackupVault> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **Get-AzureRmBackupContainer** parancsmag Azure Backup-tárolókat kap.
Egy **AzureBackupContainer** beágyazza az adatforrásokat, a védett elemeket és a helyreállítási pontokat.
Egy **AzureBackupContainer** az alábbiak egyike lehet: 
- Windows Server rendszerű számítógépen
- A System Center Data Protection Manager (SCDPM) kiszolgálója 
- Azure-infrastruktúra szolgáltatásként (IaaS) virtuális gép biztonsági mentése előtt biztonsági másolatot készíthet egy adatforrásról vagy elemről, regisztrálnia kell az azt tároló tárolót, amely az Azure Backup szolgáltatással rendelkezik.
A tárolónak hitelesítettnek kell lennie, hogy biztonsági másolatot küldjön a biztonságimásolat-tárolónak.
Windows Server rendszerű számítógépek és SCDPM-kiszolgálók esetén a regisztráció a kiszolgáló teljesen minősített tartománynevével történik.

## Példák

### Példa 1: a boltozathoz regisztrált összes kiszolgáló megtekintése
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> Get-AzureRmBackupContainer -Vault $Vault -Type Windows
Name                         Type               Status
----                         ----               ------
SERVER01.CONTOSO.COM          Windows            Registered
SERVER02.CONTOSO.COM          Windows            Registered
```

Az első parancs a Vault03 nevű boltozatot a **Get-AzureRmBackupVault** parancsmag használatával kapja.
A parancs az objektumot a $Vault változóban tárolja.
A második parancs beolvassa a Windows rendszer minden típusú tárolóját a boltozatról $Vault.

### 2. példa: adott tároló beszerzése
```
PS C:\>Get-AzureRmBackupContainer -Vault $Vault -Type SCDPM -Name "DPMSERVER.CONTOSO.COM"
Name                         Type               Status
----                         ----               ------
DPMSERVER.CONTOSO.COM        SCDPM              Registered
```

Ez a parancs a DPMSERVER nevű tárolót kapja meg. CONTOSO.COM.
A parancs a $Vault és a tároló típusát adja meg.

### 3. példa: az összes regisztrált Azure virtuális gép megtekintése
```
PS C:\>Get-AzureRmBackupContainer -Vault $Vault -Type AzureVM -Status Registered 
Name                         Type               Status
----                         ----               ------
co03-vm                      AzureVM            Registered
```

Ez a parancs a regisztrált virtuális gépeket az $Vault boltozatáról kapja.

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

### -ManagedResourceGroupName
A tárolóhoz társított erőforráscsoport nevét adja meg.
Ez a név ugyanazt az értéket adja meg, amelyet az Register-AzureRmBackupContainer parancsmag *szolgáltatásnév* vagy *ResourceGroupName* paramétereként megadott.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (név)
Annak a tárolónak a nevét adja meg, amely a parancsmagot kapja.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Állapot
A parancsmag által kapott tárolók pillanatnyi állapotát adja meg.
A paraméter elfogadható értékei a következők:
- NotRegistered 
- Regisztrált 
- Regisztráció

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureBackupContainerRegistrationStatus
Parameter Sets: (All)
Aliases:
Accepted values: Registered, Registering, NotRegistered

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Type (típus)
Itt adhatja meg, hogy a parancsmag milyen típusú tárolókat kap.

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureBackupContainerType
Parameter Sets: (All)
Aliases:
Accepted values: Windows, SCDPM, AzureVM, AzureBackupServer, Other

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Boltozat
A parancsmagot tároló biztonságimásolat-tárolót adja meg.
Ha **AzureRmBackupVault** szeretne beolvasni, használja az Get-AzureRmBackupVault parancsmagot.

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault
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

### Microsoft. Azure. Command. AzureBackup. models. AzureRMBackupVault
Paraméterek: Vault (ByValue)

## KIMENETEK

### Microsoft. Azure. Command. AzureBackup. models. AzureRMBackupContainer

## MEGJEGYZI
* Nincs

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureRmBackupVault](./Get-AzureRmBackupVault.md)

[Register-AzureRmBackupContainer](./Register-AzureRmBackupContainer.md)

[Regisztráció törlése – AzureRmBackupContainer](./Unregister-AzureRmBackupContainer.md)


