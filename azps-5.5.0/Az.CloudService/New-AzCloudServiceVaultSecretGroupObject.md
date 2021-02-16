---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.CloudService/new-AzCloudServiceVaultSecretGroupObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceVaultSecretGroupObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceVaultSecretGroupObject.md
ms.openlocfilehash: 925d29e7d567613bbf10e88c65860ebe2ef40c2e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100167970"
---
# New-AzCloudServiceVaultSecretGroupObject

## SYNOPSIS
Create a in-memory object for Vault Secret Group

## SZINTAXIS

```
New-AzCloudServiceVaultSecretGroupObject [-CertificateUrl <String[]>] [-Id <String>] [<CommonParameters>]
```

## LEÍRÁS
Create a in-memory object for Secret Group

## PÉLDÁK

### 1. példa: Titkos csoportobjektum létrehozása a tárolóban
```powershell
$keyVault = Get-AzKeyVault -VaultName 'ContosoKeyVault'
$certificate = Get-AzKeyVaultCertificate -VaultName 'ContosoKeyVault' -Name 'ContosoCert'
$secretGroup = New-AzCloudServiceVaultSecretGroupObject -Id $keyVault.ResourceId -CertificateUrl $certificate.SecretId
```

Ez a parancs egy titkos tárolócsoport-objektumot hoz létre, amely egy felhőszolgáltatás létrehozására vagy frissítésére használható.
További részletekért lásd: New-AzCloudService.

## PARAMETERS

### -CertificateUrl
Ez annak a tanúsítványnak az URL-címe, amely titkosként lett feltöltve a kulcstárolóba.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Id
Kulcstár erőforrásazonosítója.

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

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

## KIMENETEK

### Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.CloudServiceVaultSecretGroup

## MEGJEGYZÉSEK

ALIASOK

## KAPCSOLÓDÓ HIVATKOZÁSOK

