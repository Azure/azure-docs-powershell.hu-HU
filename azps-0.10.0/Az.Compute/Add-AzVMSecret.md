---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 5008F83F-AF3E-47CF-99A3-55129E654128
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVMSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVMSecret.md
ms.openlocfilehash: 281b74aa14431a0bcfe0d138a78db73e28bcfeb4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844742"
---
# Add-AzVMSecret

## Áttekintés
Titkos kulcsot ad hozzá egy virtuális géphez.

## SZINTAXISA

```
Add-AzVMSecret [-VM] <PSVirtualMachine> [[-SourceVaultId] <String>] [[-CertificateStore] <String>]
 [[-CertificateUrl] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
Az **Add-AzVMSecret** parancsmag titkot ad egy virtuális géphez.
Ezzel az értékkel adhat hozzá tanúsítványt a virtuális géphez.
A titkot egy kulcsos boltozaton kell tárolni.
A Key Vault-ról további információt a [Mi az Azure Key Vault?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/)című témakörben talál.
A parancsmagokról további információt az [Azure Key Vault-parancsmagok](https://msdn.microsoft.com/library/azure/dn868052.aspx) a Microsoft Developer Network műsortárában vagy a [set-AzureKeyVaultSecret](/powershell/module/azurerm.keyvault/set-azurekeyvaultsecret) parancsmagban című témakörben talál.

## Példák

### 1. példa: titok hozzáadása virtuális géphez
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
PS C:\> $Credential = Get-Credential
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine  -Windows -ComputerName "Contoso26" -Credential $Credential
PS C:\> $SourceVaultId = "/subscriptions/46f8cea4-2de6-4179-8ab1-365da4211af4/resourceGroups/vault/providers/Microsoft.KeyVault/vaults/keyvault"
PS C:\> $CertificateStore01 = "My"
PS C:\> $CertificateUrl01 = "https://contosovault.vault.azure.net/secrets/514ceb769c984379a7e0230bdd703272"
PS C:\> $VirtualMachine = Add-AzVMSecret -VM $VirtualMachine -SourceVaultId $SourceVaultId -CertificateStore $CertificateStore01 -CertificateUrl $CertificateUrl01
```

Az első parancs létrehoz egy virtuálisgép-objektumot, majd a $VirtualMachine változóban tárolja.
A parancs nevet és méretet rendel a virtuális géphez.

A második parancs a hitelesítőadat-objektumot a Get-Credential parancsmag segítségével hozza létre, majd az eredményt a $Credential változóban tárolja.
A parancs a Felhasználónév és a jelszó megadását kéri.
További információért írja be a következőt: `Get-Help Get-Credential` .

A harmadik parancs a **set-AzVMOperatingSystem** parancsmagot használja az $VirtualMachine-ban tárolt virtuális gép beállításához.

A negyedik parancs a Forrásobjektum-azonosítót a $SourceVaultId változóhoz rendeli későbbi használatra.
A parancs feltételezi, hogy a $SubscriptionId változó megfelelő értékű.

Az ötödik parancs egy értéket rendel a $CertificateStore 01 változóhoz későbbi használat céljából.

A hatodik parancs a tanúsítványtároló URL-címét rendeli hozzá.

A hetedik parancs egy titkot ad a $VirtualMachine-ban tárolt virtuális gépnek.
A SourceVaultId paraméter a kulcs boltozatát adja meg.
A parancs a tanúsítványtároló nevét és a tanúsítvány URL-címét adja meg.
A **bővítményt** többször is futtathatja, ha más tanúsítványok titkát is hozzá szeretné adni.

## PARAMÉTEREK

### -CertificateStore
A Windows operációs rendszert futtató virtuális számítógépen a tanúsítványtároló nevét adja meg.
Ez a parancsmag hozzáadja a tanúsítványt a paraméter által megadott tárolóhoz.
Ezt a paramétert csak a Windows operációs rendszert futtató virtuális gépekhez adhatja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CertificateUrl
Itt adhatja meg azt az URL-címet, amely a tanúsítványokat tartalmazó kulcs-boltozati titokra mutat.

A tanúsítvány az alábbi, UTF-8 kódolású JavaScript-objektum (JSON) objektum Base64 kódolása:

{"Data": " \< Base64-kódolt fájl \> "," adattípus ":" fájlformátum " \< \> ," jelszó ":" \< pfx-fájl-jelszó " \> }


Az adattípusok jelenleg csak a. pfx fájlokat fogadják el.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -SourceVaultId
A virtuális géphez hozzáadható tanúsítványokat tartalmazó kulcsfájl erőforrás-AZONOSÍTÓját adja meg.
Ez az érték a több tanúsítvány hozzáadásának kulcsát is megadhatja.
Ez azt jelenti, hogy ugyanazt az értéket használja a *SourceVaultId* , ha több tanúsítványt vesz fel ugyanabból a kulcsfájlból.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Id

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VM
Azt a virtuálisgép-objektumot adja meg, amelyet a parancsmag módosított.
Virtuális gép objektum beszerzéséhez használja a [Get-AzVM](./Get-AzVM.md) parancsmagot.
A [New-AzVMConfig](./New-AzVMConfig.md) parancsmaggal létrehozhatja a virtuális gép objektumát.

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### PSVirtualMachine
A ' VM ' paraméter elfogadja a "PSVirtualMachine" típusú értéket a csővezetékről

## KIMENETEK

### Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachine

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzVM](./Get-AzVM.md)

[Új – AzVMConfig](./New-AzVMConfig.md)

[Set-AzVMOperatingSystem](./Set-AzVMOperatingSystem.md)
