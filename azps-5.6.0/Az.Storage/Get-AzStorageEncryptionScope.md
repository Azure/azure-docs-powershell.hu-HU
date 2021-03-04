---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstorageencryptionscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageEncryptionScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageEncryptionScope.md
ms.openlocfilehash: 02d91338063a1c06654fa30cbbf584a6f62ea34a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101933377"
---
# Get-AzStorageEncryptionScope

## SYNOPSIS
Tárfiók titkosítási hatókörének be- vagy listába való be szereznie vagy listába kell vennie a titkosítási hatókört.

## SZINTAXIS

### AccountName (alapértelmezett)
```
Get-AzStorageEncryptionScope [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-EncryptionScopeName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### AccountObject
```
Get-AzStorageEncryptionScope -StorageAccount <PSStorageAccount> [-EncryptionScopeName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## LEÍRÁS
A **Get-AzStorageEncryptionScope** parancsmag titkosítási hatókört kap vagy listázzon egy tárfiókból.

## PÉLDÁK

### 1. példa: Egyetlen titkosítási hatókör használata
```
PS C:\> Get-AzStorageEncryptionScope -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -EncryptionScopeName $scopename


   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name      State    Source             KeyVaultKeyUri                                         
----      -----    ------             --------------                                         
testscope Disabled Microsoft.Keyvault https://keyvalutname.vault.azure.net:443/keys/keyname
```

Ez a parancs egyetlen titkosítási hatókört kap.

### 2. példa: Tárfiók összes titkosítási hatókörének felsorolása
```
PS C:\> Get-AzStorageEncryptionScope -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" 


   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name      State    Source             KeyVaultKeyUri                                         
----      -----    ------             --------------                                         
testscope Disabled Microsoft.Keyvault https://keyvalutname.vault.azure.net:443/keys/keyname
scope2    Enabled  Microsoft.Storage
```

Ez a parancs felsorolja a tárfiók összes titkosítási hatókörét.

## PARAMETERS

### -DefaultProfile
Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EncryptionScopeName
Azure Storage EncryptionScope-név

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Erőforráscsoport neve.

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageAccount
Tárfiók objektum

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -StorageAccountName
Tárfiók neve.

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount

## KIMENETEK

### Microsoft.Azure.Commands.Management.Storage.Models.PSEncryptionScope

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK
