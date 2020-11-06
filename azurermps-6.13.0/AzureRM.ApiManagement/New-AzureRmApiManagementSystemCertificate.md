---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementsystemcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementSystemCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementSystemCertificate.md
ms.openlocfilehash: fa64e9bade3a6cd8ec4edc8e04956c97306328ea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492083"
---
# New-AzureRmApiManagementSystemCertificate

## Áttekintés
Létrehozza a példányát `PsApiManagementSystemCertificate` . A tanúsítványt a privát HITELESÍTÉSSZOLGÁLTATÓ bocsáthatja ki, és az API-kezelési szolgáltatásba telepíti, és `CertificateAuthority` az `Root` áruházba kerül.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
New-AzureRmApiManagementSystemCertificate -StoreName <String> -PfxPath <String> [-PfxPassword <SecureString>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **New-AzureRmApiManagementSystemCertificate** parancsmag egy olyan segítő parancs, amely a **PsApiManagementSystemCertificate** példányát hozza létre.
Ezt a parancsot a New-AzureRmApiManagement és a Set-AzureRmApiManagement parancsmag használja.

## Példák

### Példa 1: PsApiManagementSystemCertificate-példány létrehozása és inicializálása SSL-tanúsítvánnyal fájlból
```powershell
PS C:\>$rootCa = New-AzureRmApiManagementSystemCertificate -StoreName "Root" -PfxPath "C:\contoso\certificates\privateCa.cer"
PS C:\>$systemCert = @($rootCa)
PS C:\>New-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -SystemCertificateConfiguration $systemCert
```

Ezzel a paranccsal létrehozhatja és inicializálhatja a **PsApiManagementSystemCertificate** példányát a legfelső szintű hitelesítésszolgáltatói tanúsítvánnyal. Ekkor létrejön és API-kezelési szolgáltatás, amely a HITELESÍTÉSSZOLGÁLTATÓ tanúsítványát telepíti a legfelső szintű tárolónak.

## PARAMÉTEREK

### -DefaultProfile
Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

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

### -PfxPassword
A. pfx tanúsítványfájl jelszava.

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
A. pfx tanúsítványfájl elérési útvonala.

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

### -StoreName mezőt
Tanúsítvány StoreName mezőt

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
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### System. String

### System. Security. SecureString

## KIMENETEK

### Microsoft. Azure. Command. ApiManagement. models. PsApiManagementSystemCertificate

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Új – AzureRmApiManagement](./New-AzureRmApiManagement.md)

[Set-AzureRmApiManagement](./Set-AzureRmApiManagement.md)
