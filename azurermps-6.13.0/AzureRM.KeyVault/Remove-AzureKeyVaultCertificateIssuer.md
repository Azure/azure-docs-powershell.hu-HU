---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: FC14F6BF-BD8F-45E0-9CAA-A937E5E56288
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificateIssuer.md
ms.openlocfilehash: dc49237d4722384d04228d3b8e9736411ed41bde
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672718"
---
# Remove-AzureKeyVaultCertificateIssuer

## Áttekintés
A tanúsítvány kijavítása egy kulcs boltozatról

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### Alapértelmezett (alapértelmezett)
```
Remove-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### InputObject
```
Remove-AzureKeyVaultCertificateIssuer [-InputObject] <PSKeyVaultCertificateIssuerIdentityItem> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Leírás
A **Remove-AzureKeyVaultCertificateIssuer** parancsmag a tanúsítvány kifizetését egy kulcs boltozatról törli.

## Példák

### 1. példa: a tanúsítvány kibocsátásának eltávolítása
```powershell
PS C:\> Remove-AzureKeyVaultCertificateIssuer -VaultName "ContosoKV01" -Name "TestIssuer01" -Force

AccountId           :
ApiKey              :
OrganizationDetails :
Name                : TestIssuer01
IssuerProvider      : test
VaultName           : ContosoKV01
```

Ez a parancs eltávolítja a TestIssuer01 nevű tanúsítvány-kibocsátási kulcsot a ContosoKV01.

## PARAMÉTEREK

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés

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

### -Force
Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
A tanúsítvány-kibocsátási objektum

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name (név)
Itt adhatja meg az eltávolítandó tanúsítvány nevét.

```yaml
Type: System.String
Parameter Sets: Default
Aliases: IssuerName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.
Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VaultName
A kulcsfájl nevét adja meg.

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### – Megerősítés
A parancsmag futtatása előtt kéri a megerősítést.

```yaml
Type: System.Management.Automation.SwitchParameter
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
A parancsmag nem fut. Annak megjelenítése, hogy mi történik, ha a parancsmag fut.
A parancsmag nem fut.

```yaml
Type: System.Management.Automation.SwitchParameter
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

### Microsoft. Azure. Command. PSKeyVaultCertificateIssuerIdentityItem. models.
Paraméterek: InputObject (ByValue)

## KIMENETEK

### Microsoft. Azure. Command. PSKeyVaultCertificateIssuer. models.

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureKeyVaultCertificateIssuer](./Get-AzureKeyVaultCertificateIssuer.md)

[Set-AzureKeyVaultCertificateIssuer](./Set-AzureKeyVaultCertificateIssuer.md)


