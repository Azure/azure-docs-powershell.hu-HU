---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 5CC89899-00B6-424A-8896-FD32DE9DDA28
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVmssVaultCertificateConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVmssVaultCertificateConfig.md
ms.openlocfilehash: 9014c91626d41e66f316b870e042af7d5655f07a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499032"
---
# New-AzureRmVmssVaultCertificateConfig

## Áttekintés
A fő pince-tanúsítványok konfigurációját hozza létre.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
New-AzureRmVmssVaultCertificateConfig [[-CertificateUrl] <String>] [[-CertificateStore] <String>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## Leírás
A **New-AzureRmVmssVaultCertificateConfig** parancsmag a Virtual Machine Scale set (VMSS) virtuális gépeken elhelyezni kívánt titkot adja meg.
A parancsmag kimenete az Add-AzureRmVmssSecret parancsmaggal való használatra szolgál.

## Példák

### Példa 1: kulcs boltozatos tanúsítvány-konfiguráció létrehozása
```
PS C:\> New-AzureRmVmssVaultCertificateConfig -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion" -CertificateStore "MyCerts"
```

Ez a parancs létrehoz egy fő pince-bizonyítvány-konfigurációt, amely a megadott tanúsítvány URL-címében található MyCerts nevű tanúsítványtárolót használja.

## PARAMÉTEREK

### -CertificateStore
A tanúsítványtárolót adja meg a virtuális számítógépeken abban a méretarányban, ahol a tanúsítványt felveszi.
Ez csak a Windows virtuális gép méretarányos készletei esetén érvényes.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CertificateUrl
A kulcs-Boltozatban tárolt tanúsítvány URI-azonosítóját adja meg.

Az alábbi, UTF-8 kódolású JSON objektum Base64 kódolása:


{"Data": " \<Base64-encoded-certificate\> "; "adattípus": "pfx", "password": " \<pfx-file-password\> "}

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Annak megjelenítése, hogy mi történik, ha a parancsmag fut. A parancsmag nem fut.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
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

###  
Ez a parancsmag semmilyen kimenetet nem hoz létre.

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Add-AzureRmVmssSecret](./Add-AzureRmVmssSecret.md)
