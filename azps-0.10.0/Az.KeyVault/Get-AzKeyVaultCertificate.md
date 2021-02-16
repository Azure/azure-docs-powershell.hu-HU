---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 363FA51E-D075-4800-A4BE-BFF63FD25C90
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/get-AzKeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificate.md
ms.openlocfilehash: babd3d8a42ddbd740c8189a41de76c78170ecae5
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100398818"
---
# Get-AzKeyVaultCertificate

## SYNOPSIS
Tanúsítványt kap egy kulcstárolóból.

## SZINTAXIS

### ByVaultName (alapértelmezett)
```
Get-AzKeyVaultCertificate [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ByCertificateName
```
Get-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByCertificateVersions
```
Get-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByDeletedCertificates
```
Get-AzKeyVaultCertificate [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## LEÍRÁS
A **Get-AzKeyVaultCertificate** parancsmag a megadott tanúsítványt vagy egy tanúsítvány verzióit kapja meg egy kulcstárolóból az Azure Key Vaultban.

## PÉLDÁK

### 1. példa: Tanúsítvány lekérve
```
PS C:\>Get-AzKeyVaultCertificate -VaultName "ContosoKV01" -Name "TestCert01"
Name        : testCert01
Certificate : [Subject] 
                CN=contoso.com

              [Issuer] 
                CN=contoso.com

              [Serial Number] 
                05979C5A2F0741D5A3B6F97673E8A118

              [Not Before] 
                2/8/2016 3:11:45 PM

              [Not After] 
                8/8/2016 4:21:45 PM

              [Thumbprint] 
                3E9B6848AD1834284157D68B060F748037F663C8

Thumbprint  : 3E9B6848AD1834284157D68B060F748037F663C8
Tags        : 
Enabled     : True
Created     : 2/8/2016 11:21:45 PM
Updated     : 2/8/2016 11:21:45 PM
```

Ez a parancs a ContosoKV01 nevű kulcstárolóból kapja meg a TestCert01 nevű tanúsítványt.

### 2. példa: Szerezze be az összes olyan tanúsítványt, amely törlődött, de nem lett véglegesen törölve ehhez a kulcstárhoz.
```
PS C:\>Get-AzKeyVaultCertificate -VaultName 'Contoso' -InRemovedState
```

Ez a parancs a Korábban törölt, de nem véglegesen törölt összes tanúsítványt a Contoso nevű kulcstárba kapja.

### 3. példa: Annak a MyCertnek a tanúsítványát kapja meg, amely törölve lett, de nem lett véglegesen törölve ehhez a kulcstárolóhoz.
```
PS C:\>Get-AzKeyVaultCertificate -VaultName 'Contoso' -Name 'MyCert' -InRemovedState
```

Ez a parancs a Korábban törölt, de nem véglegesen törölt MyCert tanúsítványt kapja a Contoso nevű kulcstárolóban.
Ez a parancs metaadatokat, például törlési dátumot és a törölt tanúsítvány ütemezett végleges végleges törlésének dátumát adja vissza.

## PARAMETERS

### -DefaultProfile
Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IncludeVersions
Azt jelzi, hogy ez a művelet a tanúsítvány összes verzióját lekéri.

```yaml
Type: SwitchParameter
Parameter Sets: ByCertificateVersions
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InRemovedState
Megadja, hogy a korábban törölt tanúsítványok szerepeljenek-e a kimenetben

```yaml
Type: SwitchParameter
Parameter Sets: ByDeletedCertificates
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
A lekérni szükséges tanúsítvány neve.

```yaml
Type: String
Parameter Sets: ByCertificateName, ByCertificateVersions
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByDeletedCertificates
Aliases: CertificateName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VaultName
Egy kulcstár nevét adja meg.

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

### -Version
A tanúsítvány verzióját határozza meg.

```yaml
Type: String
Parameter Sets: ByCertificateName
Aliases: CertificateVersion

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### Nincs
Ez a parancsmag semmilyen bemenetet nem fogad el.

## KIMENETEK

### System.Collections.Generic.List'1[Microsoft.Azure.Commands.KeyVault.Models.CertificateIdentityItem]

### Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificate

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Add-AzKeyVaultCertificate](./Add-AzKeyVaultCertificate.md)

[Import-AzKeyVaultCertificate](./Import-AzKeyVaultCertificate.md)

[Remove-AzKeyVaultCertificate](./Remove-AzKeyVaultCertificate.md)

