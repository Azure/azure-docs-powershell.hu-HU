---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 394500DB-D2BB-4793-8D9F-2CAF4D892A55
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/register-azurermbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Register-AzureRmBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Register-AzureRmBackupContainer.md
ms.openlocfilehash: 71c7d883994897e4dc4b450391fb50949a125c77
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501503"
---
# Register-AzureRmBackupContainer

## Áttekintés
A tároló rögzítése a biztonsági mentést tartalmazó boltozattal.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### V1VM
```
Register-AzureRmBackupContainer -Name <String> -ServiceName <String> [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### V2VM
```
Register-AzureRmBackupContainer -Name <String> -ResourceGroupName <String> [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **Register-AzureRmBackupContainer** parancsmag a tárolót egy Azure Backup Vault-tárolóval regisztrálja.
Ha az Azure Backup segítségével szeretné konfigurálni a biztonsági mentést, először regisztrálja a kiszolgálót vagy a virtuális gépet egy biztonsági másolattal.
Ez a parancsmag egy infrastruktúrát (IaaS) virtuális gépet regisztrál a megadott boltozattal.
A Register művelet az Azure Virtual machinet a biztonsági mentés boltozatával társítja, és a virtuális gépet a biztonsági életcikluson keresztül követi nyomon.

## Példák

### 1. példa: virtuális gép rögzítése biztonsági tárolóban
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> Register-AzureRmBackupContainer -Vault $Vault -Name "Contoso03Vm" -ServiceName "ContosoService27"
```

Az első parancs a Vault03 nevű boltozatot az Get-AzureRmBackupVault parancsmag segítségével kapja meg.
A parancs a $Vault változóban tárolja a boltozatot.

A második parancs a Contoso03Vm nevű virtuális gépet $Vault-ban a boltozattal regisztrálja.
Ez a virtuális gép a ContosoService27 nevű szolgáltatáshoz tartozik.

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

### -Name (név)
Annak a virtuális gépnek a nevét adja meg, amelyre a parancsmag van regisztrálva.

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

### -ResourceGroupName
A virtuális gép erőforráscsoport-csoportjának nevét adja meg.

```yaml
Type: String
Parameter Sets: V2VM
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Szolgáltatásnév
Annak a virtuális gépnek a szolgáltatásának a nevét adja meg, amelyre a parancsmag van regisztrálva.

A Felhőbeli szolgáltatások nevének általában egy utótag. cloudapp.net kell lennie.
A paraméter megadásakor ne szerepeljen az utótag.

Ha információt szeretne kapni egy virtuális gépre vonatkozóan, használja az Get-AzureRMVM parancsmagot.
A szolgáltatás neve a Virtual Machine objektum **DeploymentName** tulajdonsága.

```yaml
Type: String
Parameter Sets: V1VM
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Boltozat
Annak a biztonságimásolat-tárolónak a megadása, amelyhez ez a parancsmag a virtuális gépet regisztrálja.
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

### AzureRmBackupVault

## KIMENETEK

### AzureRmBackupJob

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureRmBackupVault](./Get-AzureRmBackupVault.md)


