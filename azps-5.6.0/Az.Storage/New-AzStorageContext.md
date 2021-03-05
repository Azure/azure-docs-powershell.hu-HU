---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 383402B2-6B7C-41AB-AFF9-36C86156B0A9
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azstoragecontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContext.md
ms.openlocfilehash: 4e4a86d5054a5554cb473c60550d32adffae5e46
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002486"
---
# New-AzStorageContext

## SYNOPSIS
Azure-tárterület környezetét hozza létre.

## SZINTAXIS

### OAuthAccount (alapértelmezett)
```
New-AzStorageContext [-StorageAccountName] <String> [-UseConnectedAccount] [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### AccountNameAndKey
```
New-AzStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### AccountNameAndKeyEnvironment
```
New-AzStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 -Environment <String> [<CommonParameters>]
```

### AnonymousAccount
```
New-AzStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] [-Endpoint <String>]
 [<CommonParameters>]
```

### AnonymousAccountEnvironment
```
New-AzStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] -Environment <String>
 [<CommonParameters>]
```

### SasToken
```
New-AzStorageContext [-StorageAccountName] <String> -SasToken <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### SasTokenWithAzureEnvironment
```
New-AzStorageContext [-StorageAccountName] <String> -SasToken <String> -Environment <String>
 [<CommonParameters>]
```

### OAuthAccountEnvironment
```
New-AzStorageContext [-StorageAccountName] <String> [-UseConnectedAccount] [-Protocol <String>]
 -Environment <String> [<CommonParameters>]
```

### ConnectionString
```
New-AzStorageContext -ConnectionString <String> [<CommonParameters>]
```

### LocalDevelopment
```
New-AzStorageContext [-Local] [<CommonParameters>]
```

## LEÍRÁS
A **New-AzStorageContext** parancsmag létrehoz egy Azure Storage-környezetet.
A tárolási környezet alapértelmezett hitelesítése az OAuth (Azure AD), ha csak bemeneti tárfiók neve.
A társzolgáltatás hitelesítésének részleteit itt https://docs.microsoft.com/rest/api/storageservices/authorization-for-the-azure-storage-services olvashatja.

## PÉLDÁK

### 1. példa: Környezet létrehozása tárfiók nevének és kulcsának megadásával
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
```

Ez a parancs létrehoz egy környezetet a ContosoGeneral nevű fiókhoz, amely a megadott kulcsot használja.

### 2. példa: Környezet létrehozása kapcsolati karakterlánc megadásával
```
PS C:\>New-AzStorageContext -ConnectionString "DefaultEndpointsProtocol=https;AccountName=ContosoGeneral;AccountKey=< Storage Key for ContosoGeneral ends with == >;"
```

Ez a parancs a ContosoGeneral fiókhoz megadott kapcsolati karakterlánc alapján hoz létre környezetet.

### 3. példa: Környezet létrehozása névtelen tárfiókhoz
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -Anonymous -Protocol "http"
```

Ez a parancs kontextust hoz létre névtelen használatra a ContosoGeneral nevű fiókhoz.
A parancs a HTTP protokollt adja meg kapcsolati protokollként.

### 4. példa: Környezet létrehozása a helyi fejlesztési tárfiók használatával
```
PS C:\>New-AzStorageContext -Local
```

Ez a parancs a helyi fejlesztési tárfiók használatával hoz létre környezetet.
A parancs a *Helyi paramétert adja* meg.

### 5. példa: A helyi fejlesztői tárfiók tárolója
```
PS C:\>New-AzStorageContext -Local | Get-AzStorageContainer
```

Ez a parancs a helyi fejlesztési tárfiók használatával létrehoz egy környezetet, majd átadja az új környezetnek a **Get-AzStorageContainer** parancsmagot a folyamat műveleti operátorával.
A parancs a helyi fejlesztői tárfiók Azure Storage tárolóját kapja meg.

### 6. példa: Több tároló lekérte
```
PS C:\>$Context01 = New-AzStorageContext -Local 
PS C:\> $Context02 = New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
PS C:\> ($Context01, $Context02) | Get-AzStorageContainer
```

Az első parancs a helyi fejlesztési tárfiók használatával létrehoz egy környezetet, majd ezt a környezetet a $Context 01 változóban tárolja.
A második parancs létrehoz egy környezetet a ContosoGeneral nevű fiókhoz, amely a megadott kulcsot használja, majd ezt a kontextust a $Context 02 változóban tárolja.
A végleges parancs a $Context 01-ben és a $Context 02-ben a **Get-AzStorageContainer** használatával tárolt környezetek tárolóit kapja meg.

### 7. példa: Környezet létrehozása végponttal
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Endpoint "contosoaccount.core.windows.net"
```

Ez a parancs létrehoz egy Azure Storage környezetet, amely a megadott tárolási végponttal rendelkezik.
A parancs létrehozza a megadott kulcsot használó ContosoGeneral nevű fiók környezetét.

### 8. példa: Környezet létrehozása egy adott környezetben
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Environment "AzureChinaCloud"
```

Ez a parancs létrehoz egy Azure-tárterületkörnyezetet, amely a megadott Azure-környezettel rendelkezik.
A parancs létrehozza a megadott kulcsot használó ContosoGeneral nevű fiók környezetét.

### 9. példa: Környezet létrehozása SAS-jogkivonat használatával
```
PS C:\>$SasToken = New-AzStorageContainerSASToken -Name "ContosoMain" -Permission "rad"
PS C:\> $Context = New-AzStorageContext -StorageAccountName "ContosoGeneral" -SasToken $SasToken
PS C:\> $Context | Get-AzStorageBlob -Container "ContosoMain"
```

Az első parancs egy SAS-jogkivonatot hoz létre a ContosoMain nevű tároló **New-AzStorageContainerSASToken** parancsmagját használva, majd a tokent a $SasToken változóban tárolja.
Ez a jogkivonat olvasási, hozzáadási, frissítési és törlési engedélyekhez szükséges.
A második parancs létrehoz egy környezetet a ContosoGeneral nevű fiókhoz, amely az $SasToken-ban tárolt SAS-jogkivonatot használja, majd a környezet a $Context változóban tárolja.
Az utolsó parancs felsorolja a ContosoMain nevű tárolóval társított összes blobot a $Context.

### 10. példa: Környezet létrehozása OAuth-hitelesítéssel
```
PS C:\>Connect-AzAccount
PS C:\> $Context = New-AzStorageContext -StorageAccountName "myaccountname" -UseConnectedAccount
```

Ez a parancs az OAuth (Azure AD) hitelesítéssel hoz létre környezetet.

## PARAMETERS

### -Anonymous
Azt jelzi, hogy ez a parancsmag létrehoz egy Azure Storage környezetet a névtelen bejelentkezéshez.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AnonymousAccount, AnonymousAccountEnvironment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ConnectionString
Egy kapcsolati karakterláncot ad meg az Azure Storage környezethez.

```yaml
Type: System.String
Parameter Sets: ConnectionString
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Endpoint
Az Azure Storage környezet végpontját határozza meg.

```yaml
Type: System.String
Parameter Sets: OAuthAccount, AccountNameAndKey, AnonymousAccount, SasToken
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Környezet
Az Azure-környezetet határozza meg.
A paraméter elfogadható értékei: AzureCloud és AzureChinaCloud.
További információért írja be a `Get-Help Get-AzEnvironment` .

```yaml
Type: System.String
Parameter Sets: AccountNameAndKeyEnvironment, AnonymousAccountEnvironment
Aliases: Name, EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SasTokenWithAzureEnvironment, OAuthAccountEnvironment
Aliases: Name, EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Local
Azt jelzi, hogy ez a parancsmag környezetet hoz létre a helyi fejlesztési tárfiók használatával.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: LocalDevelopment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Protocol
Transfer Protocol (https/http).

```yaml
Type: System.String
Parameter Sets: OAuthAccount, AccountNameAndKey, AccountNameAndKeyEnvironment, AnonymousAccount, AnonymousAccountEnvironment, SasToken, OAuthAccountEnvironment
Aliases:
Accepted values: Http, Https

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SasToken
Egy SAS-jogkivonatot ad meg a környezethez.

```yaml
Type: System.String
Parameter Sets: SasToken, SasTokenWithAzureEnvironment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageAccountKey
Egy Azure Storage-fiókkulcsot ad meg.
Ez a parancsmag a paraméter által megadott kulcs környezetét hozza létre.

```yaml
Type: System.String
Parameter Sets: AccountNameAndKey, AccountNameAndKeyEnvironment
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageAccountName
Egy Azure Storage-fiók nevét adja meg.
Ez a parancsmag a paraméter által megadott fiók környezetét hozza létre.

```yaml
Type: System.String
Parameter Sets: OAuthAccount, AccountNameAndKey, AccountNameAndKeyEnvironment, AnonymousAccount, AnonymousAccountEnvironment, SasToken, SasTokenWithAzureEnvironment, OAuthAccountEnvironment
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UseConnectedAccount
Azt jelzi, hogy ez a parancsmag Azure Storage-környezetet hoz létre OAuth (Azure AD) hitelesítéssel.
A parancsmag alapértelmezés szerint OAuth-hitelesítést fog használni, ha más hitelesítés nincs megadva.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: OAuthAccount, OAuthAccountEnvironment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### System.String

## KIMENETEK

### Microsoft.WindowsAzure.Commands.Storage.AzureStorageContext

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzStorageBlob](./Get-AzStorageBlob.md)

[New-AzStorageContainerSASToken](./New-AzStorageContainerSASToken.md)


