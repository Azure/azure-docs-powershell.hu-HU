---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/backup-azurekeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Backup-AzureKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Backup-AzureKeyVaultCertificate.md
ms.openlocfilehash: 7f75f07ee8f53a57cdb2e359fb4addb51b1d7f76
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493686"
---
# Backup-AzureKeyVaultCertificate

## Áttekintés
Biztonsági másolatot készíthet a tanúsítványról egy kulcs boltozatáról.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### ByCertificateName (alapértelmezett)
```
Backup-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByCertificate
```
Backup-AzureKeyVaultCertificate [-InputObject] <PSKeyVaultCertificateIdentityItem> [[-OutputFile] <String>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Leírás
A **biztonsági másolat-AzureKeyVaultCertificate** parancsmag a megadott tanúsítvány biztonsági másolatát egy kulcsos tárolóban, letöltéssel és fájlba történő tárolással támogatja.
Ha a tanúsítvány több verzióból áll, a biztonsági másolatban minden verziója szerepelni fog.
Mivel a letöltött tartalom titkosítva van, nem használható az Azure Key Vault-on kívül.
A mentett tanúsítványokat visszaállíthatja az előfizetésből, amelyből biztonsági másolatot készít, mindaddig, amíg a boltozat ugyanahhoz az Azure-földrajzhoz tartozik.
A parancsmag használatának tipikus okai a következők: 
- Szeretné megőrizni a tanúsítvány kapcsolat nélküli másolatát abban az esetben, ha véletlenül törli az eredetit a boltozatról.
 
- A kulccsal létrehozta a tanúsítványt, és most szeretné az objektumot egy másik Azure-területre beilleszteni, így a kiosztott alkalmazás minden példányában használhatja azt.
Használja a **Backup-AzureKeyVaultCertificate** parancsmagot a tanúsítvány titkosított formátumban való visszakereséséhez, majd használja a **Restore-AzureKeyVaultCertificate** parancsmagot, és adja meg a második régióban a kulcs boltozatát.

## Példák

### Példa 1: tanúsítvány biztonsági mentése automatikusan létrehozott fájlnévvel
```powershell
PS C:\Users\username\> Backup-AzureKeyVaultCertificate -VaultName 'mykeyvault' -Name 'mycert'

C:\Users\username\mykeyvault-mycert-1527029447.01191
```

Ez a parancs beolvassa a MyCert nevű tanúsítványt a MyKeyVault nevű kulcs-tárolóból, és menti az adott tanúsítvány biztonsági másolatát egy automatikusan megnevezett fájlba, és megjeleníti a fájl nevét.

### 2. példa: tanúsítvány biztonsági mentése megadott fájlnévre
```powershell
PS C:\> Backup-AzureKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyCert' -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

Ez a parancs beolvassa a MyCert nevű tanúsítványt a MyKeyVault nevű kulcs-tárolóból, és egy biztonsági másolatot ment a biztonsági másolat. blob nevű fájlra.

### 3. példa: egy korábban beolvasott tanúsítvány biztonsági mentése egy megadott fájlnévre, a célfájl felülírása a kérés nélkül.
```powershell
PS C:\> $cert = Get-AzureKeyVaultCertificate -VaultName 'MyKeyVault' -Name 'MyCert'
PS C:\> Backup-AzureKeyVaultCertificate -Certificate $cert -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

Ez a parancs létrehoz egy biztonsági másolatot a $cert nevű tanúsítványról. Nevezze el a $cert nevű boltozatot. VaultName egy backup. blob nevű fájlhoz, a fájl csendes felülírásával, ha már létezik.

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

### -Force
A megadott fájl felülírása ha létezik

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
Titok, hogy biztonsági másolatot készítsen a lekérési hívás kimenetéről.

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem
Parameter Sets: ByCertificate
Aliases: Certificate

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name (név)
Titkos név.
A parancsmag a boltozat nevéből, az aktuálisan kijelölt környezetből és a titkos névvel elkészíti a titkos FQDN-t.

```yaml
Type: System.String
Parameter Sets: ByCertificateName
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OutputFile
Kimeneti fájl.
A kimeneti fájl a tanúsítvány biztonsági másolatának tárolásához.
Ha nincs megadva, a program egy alapértelmezett fájlnevet hoz létre.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VaultName
Boltozat neve.
A parancsmag a pince teljes tartománynevét a név és a jelenleg kijelölt környezet alapján építi fel.

```yaml
Type: System.String
Parameter Sets: ByCertificateName
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Annak megjelenítése, hogy mi történik, ha a parancsmag fut.
A parancsmag nem fut.

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

### Microsoft. Azure. Command. PSKeyVaultCertificateIdentityItem. models.
Paraméterek: InputObject (ByValue)

## KIMENETEK

### System. String

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK
