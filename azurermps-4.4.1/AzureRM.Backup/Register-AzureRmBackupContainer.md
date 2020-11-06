---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 394500DB-D2BB-4793-8D9F-2CAF4D892A55
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Register-AzureRmBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Register-AzureRmBackupContainer.md
ms.openlocfilehash: fe1e1075e14e3752024edff1b68db88419d5bcd6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497928"
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

### -Name (név)
Annak a virtuális gépnek a nevét adja meg, amelyre a parancsmag van regisztrálva.

```yaml
Type: System.String
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
Type: System.String
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
Type: System.String
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
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault
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

### AzureRmBackupVault

## KIMENETEK

### AzureRmBackupJob

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureRmBackupVault](./Get-AzureRmBackupVault.md)


