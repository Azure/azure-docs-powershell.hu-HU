---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/new-azapimanagementsystemcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSystemCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSystemCertificate.md
ms.openlocfilehash: cc3cc5d0e7ae617fc745c2f119f7da9df88417a3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101922210"
---
# New-AzApiManagementSystemCertificate

## SYNOPSIS
Létrehozza a `PsApiManagementSystemCertificate` . A tanúsítványt a privát hitelesítésszolgáltatók is kibocsáthatja, és az API-kezelési szolgáltatásba telepítve vagy `CertificateAuthority` `Root` tárolva lesznek.

## SZINTAXIS

```
New-AzApiManagementSystemCertificate -StoreName <String> -PfxPath <String> [-PfxPassword <SecureString>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## LEÍRÁS
A **New-AzApiManagementSystemCertificate** parancsmag egy segítő parancs, amely létrehozza a **PsApiManagementSystemCertificate példányát.**
Ez a parancs a parancsmaggal New-AzApiManagement és Set-AzApiManagement is használható.

## PÉLDÁK

### 1. példa: A PsApiManagementSystemCertificate példány létrehozása és inicializálása ssl-tanúsítvány használatával fájlból
```powershell
PS C:\>$rootCa = New-AzApiManagementSystemCertificate -StoreName "Root" -PfxPath "C:\contoso\certificates\privateCa.cer"
PS C:\>$systemCert = @($rootCa)
PS C:\>New-AzApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -SystemCertificateConfiguration $systemCert
```

Ez a parancs létrehozza és inicializálja a **PsApiManagementSystemCertificate** egy példányát egy legfelső szintű hitelesítésszolgáltatói tanúsítvánnyal. Ezután létrehozza és API-kezelő szolgáltatást hoz létre, amely telepíti a hitelesítésszolgáltatói tanúsítványt a gyökértárba.

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

### -PfxPassword
A .pfx tanúsítványfájl jelszava.

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PfxPath
A .pfx tanúsítványfájl elérési útja.

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

### -StoreName
Certificate StoreName

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: CertificateAuthority, Root

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### System.String

### System.Security.SecureString

## KIMENETEK

### Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSystemCertificate

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[New-AzApiManagement](./New-AzApiManagement.md)

[Set-AzApiManagement](./Set-AzApiManagement.md)