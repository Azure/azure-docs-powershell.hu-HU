---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlserverkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerKeyVaultKey.md
ms.openlocfilehash: 333e4b1e5f01c76947ca32277fd8ca7ff75218eb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672347"
---
# Remove-AzureRmSqlServerKeyVaultKey

## Áttekintés
Kulcs-Vault-kulcs eltávolítása egy SQL Server-kiszolgálóról.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Remove-AzureRmSqlServerKeyVaultKey [-KeyId] <String> [-AsJob] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Leírás
A Remove-AzureRmSqlServerKeyVaultKey parancsmag a megadott SQL-kiszolgálóról eltávolítja a Key Vault-kulcsot.

Fontos tudni, hogy az SQL Server-engedélyek a kulcs boltozatára nem változnak.
Az engedélyek módosításához használja a set-AzureRmKeyVaultAccessPolicy.

Ne feledje, hogy ez a parancsmag nem változtatja meg a Key Vault-t.
Ha el szeretne távolítani egy billentyűt a Key Vault-ról, használja a Remove-AzureKeyVaultKey.

## Példák

### 1. példa: kulcs-Vault-kulcs eltávolítása
```
PS C:\> Remove-AzureRmSqlServerKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

Ez a parancs eltávolítja a "'" azonosítójú Key Vault https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 -kulcsot a megadott kiszolgálóról.

ResourceGroupName: ContosoResourceGroup kiszolgálónév: ContosoServer ServerKeyName: contoso_contosokey_01234567890123456789012345678901 típusa: AzureKeyVault URI: https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ujjlenyomat: 1122334455667788990011223344556677889900 CreationDate: 1/1/2017 12:00:00 am

## PARAMÉTEREK

### -AsJob
A parancsmag futtatása a háttérben
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -KeyId
Az Azure Key Vault KeyId.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Az erőforráscsoport neve

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Kiszolgálónév
Az Azure SQL-kiszolgáló neve.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### – Megerősítés
A parancsmag futtatása előtt kéri a megerősítést.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Annak megjelenítése, hogy mi történik, ha a parancsmag fut.
A parancsmag nem fut.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### System. String

## KIMENETEK

### System. Object (rendszer. objektum)

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[SQL-adatbázis dokumentációja](https://docs.microsoft.com/azure/sql-database/)
