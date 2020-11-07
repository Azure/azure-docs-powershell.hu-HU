---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 5CC89899-00B6-424A-8896-FD32DE9DDA28
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmssvaultcertificateconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssVaultCertificateConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssVaultCertificateConfig.md
ms.openlocfilehash: 5ae0a867f18fadc8ff424a9e8249103ee558f4ed
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836744"
---
# New-AzVmssVaultCertificateConfig

## Áttekintés
A fő pince-tanúsítványok konfigurációját hozza létre.

## SZINTAXISA

```
New-AzVmssVaultCertificateConfig [[-CertificateUrl] <String>] [[-CertificateStore] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Leírás
A **New-AzVmssVaultCertificateConfig** parancsmag a Virtual Machine Scale set (VMSS) virtuális gépeken elhelyezni kívánt titkot adja meg.
A parancsmag kimenete az Add-AzVmssSecret parancsmaggal való használatra szolgál.

## Példák

### Példa 1: kulcs boltozatos tanúsítvány-konfiguráció létrehozása
```
PS C:\> New-AzVmssVaultCertificateConfig -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion" -CertificateStore "MyCerts"
```

Ez a parancs létrehoz egy fő pince-bizonyítvány-konfigurációt, amely a megadott tanúsítvány URL-címében található MyCerts nevű tanúsítványtárolót használja.

## PARAMÉTEREK

### -CertificateStore
A tanúsítványtárolót adja meg a virtuális számítógépeken abban a méretarányban, ahol a tanúsítványt felveszi.
Ez csak a Windows virtuális gép méretarányos készletei esetén érvényes.

```yaml
Type: System.String
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
Ez a következő JSON-objektum Base64 kódolása, amely UTF-8-ban kódolt: {"Data": " \< Base64-kódolt tanúsítvány \> ", "adattípus": "pfx", "password": " \< pfx-fájl – jelszó" \> }

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

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

### – Megerősítés
A parancsmag futtatása előtt kéri a megerősítést.

```yaml
Type: System.Management.Automation.SwitchParameter
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
Type: System.Management.Automation.SwitchParameter
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

### System. String

## KIMENETEK

### Microsoft. Azure. Management. kiszámítás. models. VaultCertificate

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Add-AzVmssSecret](./Add-AzVmssSecret.md)
