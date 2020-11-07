---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 3BD243C7-A40E-4061-93FF-DDE7DECAD0A7
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/set-AzKeyvaultcertificateattribute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificateAttribute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificateAttribute.md
ms.openlocfilehash: 9297e523e623542c19df1915d3da29d9e39cec40
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843857"
---
# Set-AzKeyVaultCertificateAttribute

## Áttekintés
Módosítja a tanúsítványok szerkeszthető attribútumait.

## SZINTAXISA

```
Set-AzKeyVaultCertificateAttribute [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-Enable <Boolean>] [-Tag <Hashtable>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## Leírás
A **set-AzKeyVaultCertificateAttribute** parancsmag a tanúsítványok szerkeszthető attribútumait módosítja.

## Példák

### Példa 1: a tanúsítvánnyal társított címkék módosítása
```
PS C:\>$Tags = @{ "Team" = "Azure" ; "Role" = "Engg" }
PS C:\> Set-AzKeyVaultCertificateAttribute -VaultName "ContosoKV01" -Name "TestCert01" -Tag $Tags
PS C:\> Get-AzKeyVaultCertificate -VaultName "ContosoKV01" -Name "TestCert01"
Name        : "TestCert01"
Certificate : [Subject]
                CN=AZURE

              [Issuer]
                CN=AZURE

              [Serial Number]
                5A2EF60501F241D6A4336841B36FEA41

              [Not Before]
                7/27/2016 6:50:01 PM

              [Not After]
                7/27/2018 7:00:01 PM

              [Thumbprint]
                A565D568082FEE2BE33B356ECC3703C2E9886555

Id          : https://ContosoKV01.vault.azure.net:443/certificates/tt02
KeyId       : https://ContosoKV01.vault.azure.net:443/keys/tt02
SecretId    : https://ContosoKV01.vault.azure.net:443/secrets/tt02
Thumbprint  : A565D568082FEE2BE33B356ECC3703C2E9886555
Tags        : {[Role, Engg], [Team, Azure]}
Enabled     : True
Created     : 7/28/2016 2:00:01 AM
Updated     : 8/1/2016 5:37:48 PM
```

Az első parancs kulcs/érték párok tömbjét rendeli hozzá a $Tags változóhoz.

A második parancs beállítja a TestCert01 nevű tanúsítvány címkék értékét $Tags.

A végleges parancs a TestCert01 tanúsítványát az Get-AzKeyVaultCertificate parancsmag használatával jeleníti meg a művelet ellenőrzéséhez.

## PARAMÉTEREK

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés

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

### – Engedélyezés
Azt jelzi, hogy be van-e jelölve a tanúsítványok engedélyezése vagy letiltása.
Adja meg, hogy a $True engedélyezze vagy $False a letiltást.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (név)
A módosítani kívánt tanúsítvány nevét adja meg. Ez a parancsmag a tanúsítványok teljes tartománynevét, az aktuálisan kijelölt környezetet, a tanúsítvány nevét és a tanúsítvány verziószámát építi fel.

```yaml
Type: String
Parameter Sets: (All)
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.
Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Címke
A kulcs-érték párok a hash-táblázatok formájában. Példa:

@ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VaultName
Annak a kulcsnak a neve, amelyben ez a parancsmag módosította a tanúsítványt.
Ez a parancsmag a kulcsfájl teljes tartománynevét építi ki a név és a jelenleg kijelölt környezet alapján.

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

### -Verzió
A tanúsítvány verziószámát adja meg.
Ez a parancsmag a tanúsítványok teljes tartománynevét, az aktuálisan kijelölt környezetet, a tanúsítvány nevét és a tanúsítvány verziószámát építi fel.

```yaml
Type: String
Parameter Sets: (All)
Aliases: CertificateVersion

Required: False
Position: 2
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
Annak megjelenítése, hogy mi történik, ha a parancsmag fut.
A parancsmag nem fut.

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
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Nincs
Ez a parancsmag nem fogadja el a bevitelt.

## KIMENETEK

### Microsoft. Azure. Command. KeyVaultCertificate. models.

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Add-AzKeyVaultCertificate](./Add-AzKeyVaultCertificate.md)
