---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
ms.assetid: D4C465CE-1B8A-4CFC-BAA8-21CC66B7D6D6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementhostnameconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementHostnameConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementHostnameConfiguration.md
ms.openlocfilehash: 066538db3a763c5a3c6d9de9f621ca2b81552983
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492423"
---
# New-AzureRmApiManagementHostnameConfiguration

## Áttekintés
Létrehozza a PsApiManagementHostnameConfiguration példányát.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
New-AzureRmApiManagementHostnameConfiguration -CertificateThumbprint <String> -Hostname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **New-AzureRmApiManagementHostnameConfiguration** parancsmag egy olyan segítő parancs, amely a **PsApiManagementHostnameConfiguration** példányát hozza létre.
Ezt a parancsot a Set-AzureRmApiManagementHostnames parancsmag használja.

## Példák

### 1. példa: PsApiManagementHostnameConfiguration-példány létrehozása és inicializálása
```
PS C:\>New-AzureRmApiManagementHostnameConfiguration -Hostname "portal.contoso.com" -CertificateThumbprint "33CC47C6FCA848DC9B14A6F071C1EF7C"
```

Ezzel a paranccsal létrehozhatja és inicializálhatja a **PsApiManagementHostnameConfiguration** példányát.

## PARAMÉTEREK

### -CertificateThumbprint
A tanúsítvány ujjlenyomatát adja meg.
A tanúsítványt először az Import-AzureRmApiManagementHostnameCertificate parancsmaggal kell importálni.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.
 
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

### -Hostname (állomásnév)
Azt az egyéni állomásnevet adja meg, amelyhez a parancsmag létrehozta a **PsApiManagementHostnameConfiguration** -példányt.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Nincs
Ez a parancsmag nem fogadja el a bevitelt.

## KIMENETEK

### Microsoft. Azure. Command. ApiManagement. models. PsApiManagementHostnameConfiguration

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Importálás – AzureRmApiManagementHostnameCertificate](./Import-AzureRmApiManagementHostnameCertificate.md)

[Set-AzureRmApiManagementHostnames](./Set-AzureRmApiManagementHostnames.md)


