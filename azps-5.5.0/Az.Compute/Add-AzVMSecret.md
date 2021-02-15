---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 5008F83F-AF3E-47CF-99A3-55129E654128
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMSecret.md
ms.openlocfilehash: 059aedf6ca3b5c229092f9ce536d23a8fc602830
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100166594"
---
# Add-AzVMSecret

## SYNOPSIS
Hozzáad egy titkos értéket egy virtuális géphez.

## SZINTAXIS

```
Add-AzVMSecret [-VM] <PSVirtualMachine> [[-SourceVaultId] <String>] [[-CertificateStore] <String>]
 [[-CertificateUrl] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## LEÍRÁS
Az **Add-AzVMSecret** parancsmag hozzáad egy titkos értéket egy virtuális géphez.
Ez az érték lehetővé teszi egy tanúsítvány hozzáadását a virtuális géphez.
A titkos kulcsot egy kulcstárolóban kell tárolni.
A kulcstárról további információt a [Mi az Azure-kulcstár?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/)
A parancsmagokkal kapcsolatos további információkért lásd az [Azure Key Vault](/powershell/module/az.keyvault) parancsmagokat vagy a [Set-AzKeyVaultSecret](/powershell/module/az.keyvault/set-azkeyvaultsecret) parancsmagot.

## PÉLDÁK

### 1. példa: Titkos titkos gép hozzáadása virtuális géphez
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
PS C:\> $Credential = Get-Credential
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine  -Windows -ComputerName "Contoso26" -Credential $Credential
PS C:\> $SourceVaultId = "/subscriptions/46f8cea4-2de6-4179-8ab1-365da4211af4/resourceGroups/vault/providers/Microsoft.KeyVault/vaults/keyvault"
PS C:\> $CertificateStore01 = "My"
PS C:\> $CertificateUrl01 = "https://contosovault.vault.azure.net/secrets/514ceb769c984379a7e0230bdd703272"
PS C:\> $VirtualMachine = Add-AzVMSecret -VM $VirtualMachine -SourceVaultId $SourceVaultId -CertificateStore $CertificateStore01 -CertificateUrl $CertificateUrl01
```

Az első parancs létrehoz egy virtuális gépi objektumot, majd tárolja azt a $VirtualMachine változóban.
A parancs nevet és méretet rendel a virtuális géphez.
A második parancs létrehoz egy hitelesítőadat-objektumot a Get-Credential parancsmag használatával, majd az eredményt a $Credential változóban tárolja.
A parancs felhasználónevet és jelszót kér.
További információért írja be a `Get-Help Get-Credential` .
A harmadik parancs a **Set-AzVMOperatingSystem** parancsmag használatával konfigurálja a $VirtualMachine.
A negyedik parancs hozzárendel egy forrástár-azonosítót a $SourceVaultId változóhoz későbbi használatra.
A parancs feltételezi, hogy a $SubscriptionId megfelelő értékkel rendelkezik.
Az ötödik parancs egy értéket rendel a $CertificateStore 01 változóhoz későbbi használatra.
A hatodik parancs egy tanúsítványtároló URL-címét rendeli hozzá.
A hetedik parancs hozzáad egy titkos értéket a virtuális géphez, amely a $VirtualMachine.
A SourceVaultId paraméter a kulcstárat adja meg.
A parancs a tanúsítványtár nevét és URL-címét adja meg.
Az **Add-AzVMSecret** bővítményt ismétlődően futtatva további tanúsítványokat is felvehet.

## PARAMETERS

### -CertificateStore
A Windows operációs rendszert futtató virtuális gépen található tanúsítványtároló nevét adja meg.
Ez a parancsmag hozzáadja a tanúsítványt a tárolóhoz, amit ez a paraméter megad.
Ezt a paramétert csak a Windows operációs rendszert futtató virtuális gépekhez adhatja meg.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CertificateUrl
Megadja azt az URL-címet, amely egy tanúsítványt tartalmazó kulcstároló-kódra mutat.
A tanúsítvány a következő JavaScript Object Notation (JSON) objektum Base64 kódolású kódolása, amely UTF-8 kódolású: { "data": " \<Base64-encoded-file\> ", "dataType": " ", "password": " " } Jelenleg a dataType csak .pfx fájlokat fogad \<file-format\> \<pfx-file-password\> el.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### -SourceVaultId
Annak a kulcstárnak az erőforrás-azonosítója, amely a virtuális géphez hozzáadhatja a tanúsítványokat.
Ez az érték egyben a több tanúsítvány hozzáadásának kulcsa is.
Ez azt jelenti, hogy ugyanazt az értéket használhatja *a SourceVaultId* értékhez, ha több tanúsítványt ad hozzá ugyanattól a kulcstártól.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Id

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VM
Azt a virtuális gépi objektumot adja meg, amit ez a parancsmag módosít.
Virtuális gépi objektum beszerzéséhez használja a [Get-AzVM](./Get-AzVM.md) parancsmagot.
A [New-AzVMConfig](./New-AzVMConfig.md) parancsmaggal virtuális gépi objektumot hozhat létre.

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine

### System.String

## KIMENETEK

### Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzVM](./Get-AzVM.md)

[New-AzVMConfig](./New-AzVMConfig.md)

[Set-AzVMOperatingSystem](./Set-AzVMOperatingSystem.md)
