---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 200C68A3-A79C-4517-8E5D-8128F6C73A5C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateContact.md
ms.openlocfilehash: 6a59b49da2ae283af50487bec21da6c1d2457878
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679770"
---
# Get-AzureKeyVaultCertificateContact

## Áttekintés
A tanúsítványok értesítéseihez regisztrált partnerek beolvasása.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Get-AzureKeyVaultCertificateContact [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Leírás
A **Get-AzureKeyVaultCertificateContact** parancsmag az Azure Key Vault-ban egy fő boltozattal regisztrált névjegyeket kap.

## Példák

### 1. példa: az összes tanúsítvány-névjegy beolvasása
```
PS C:\>$Contacts = Get-AzureKeyVaultCertificateContact -VaultName "Contoso"
```

Ez a parancs a contoso Key Vault-ban megkapja az összes névjegyet, majd a $Contacts változóban tárolja őket.

## PARAMÉTEREK

### -VaultName
A fő pince nevét adja meg.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
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

## KIMENETEK

### Lista<Microsoft. Azure. Command. KeyVaultCertificateContact. models.>

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Add-AzureKeyVaultCertificateContact](./Add-AzureKeyVaultCertificateContact.md)

[Remove-AzureKeyVaultCertificateContact](./Remove-AzureKeyVaultCertificateContact.md)

