---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 6BCB36BC-F5E6-4EDD-983C-8BDE7A9B004D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmdiskencryptionextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDiskEncryptionExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDiskEncryptionExtension.md
ms.openlocfilehash: da50845ff5012d466eed0c68103cdbd0baea4e7f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836654"
---
# Set-AzVMDiskEncryptionExtension

## Áttekintés
Engedélyezi a titkosítást egy futó IaaS virtuális gépen az Azure-ban.

## SZINTAXISA

### SinglePassParameterSet (alapértelmezett)
```
Set-AzVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String>
 [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String> [[-KeyEncryptionKeyUrl] <String>]
 [[-KeyEncryptionKeyVaultId] <String>] [[-KeyEncryptionAlgorithm] <String>] [[-VolumeType] <String>]
 [[-SequenceVersion] <String>] [[-TypeHandlerVersion] <String>] [[-Name] <String>] [[-Passphrase] <String>]
 [-Force] [-DisableAutoUpgradeMinorVersion] [-SkipVmBackup] [-ExtensionType <String>]
 [-ExtensionPublisherName <String>] [-EncryptFormatAll] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### AADClientSecretParameterSet
```
Set-AzVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [-AadClientID] <String>
 [-AadClientSecret] <String> [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String>
 [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>] [[-KeyEncryptionAlgorithm] <String>]
 [[-VolumeType] <String>] [[-SequenceVersion] <String>] [[-TypeHandlerVersion] <String>] [[-Name] <String>]
 [[-Passphrase] <String>] [-Force] [-DisableAutoUpgradeMinorVersion] [-SkipVmBackup] [-ExtensionType <String>]
 [-ExtensionPublisherName <String>] [-EncryptFormatAll] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### AADClientCertParameterSet
```
Set-AzVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [-AadClientID] <String>
 [-AadClientCertThumbprint] <String> [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String>
 [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>] [[-KeyEncryptionAlgorithm] <String>]
 [[-VolumeType] <String>] [[-SequenceVersion] <String>] [[-TypeHandlerVersion] <String>] [[-Name] <String>]
 [[-Passphrase] <String>] [-Force] [-DisableAutoUpgradeMinorVersion] [-SkipVmBackup] [-ExtensionType <String>]
 [-ExtensionPublisherName <String>] [-EncryptFormatAll] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## Leírás
A **set-AzVMDiskEncryptionExtension** parancsmag egy futó infrastruktúra titkosítását engedélyezi az Azure rendszer Service (IaaS) virtuális számítógépén.
Ez a parancsmag lehetővé teszi a titkosítást, ha telepíti a merevlemez-titkosítási bővítményt a virtuális gépen.
Ha nincs megadva *név* paraméter, akkor a program a Windows operációs rendszert futtató virtuális gépekhez használt alapértelmezett név AzureDiskEncryption, illetve a AzureDiskEncryptionForLinux virtuális gépekhez telepített virtuális gépekhez bővítményt tartalmaz.
Ehhez a parancsmaghoz a felhasználóknak megerősítést kell engedélyezni a virtuális gép újraindítását igénylik.
Javasoljuk, hogy a parancsmag futtatása előtt mentse a munkáját a virtuális gépen.

## Példák

### 1. példa: titkosítás engedélyezése
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"
$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
Set-AzVMDiskEncryptionExtension -ResourceGroupName $RGName -VMName $VMName -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId
```

Ez a példa bemutatja a titkosítás engedélyezését az AD-hitelesítő adatok megadása nélkül.   

### 2. példa: a titkosítás engedélyezése a csővezetékes bemenettel
```
$params = New-Object PSObject -Property @{
    ResourceGroupName = "[resource-group-name]"
    VMName = "[vm-name]"
    DiskEncryptionKeyVaultId = "/subscriptions/[subscription-id-guid]/resourceGroups/[resource-group-name]/providers/Microsoft.KeyVault/vaults/[keyvault-name]"
    DiskEncryptionKeyVaultUrl = "https://[keyvault-name].vault.azure.net"
    KeyEncryptionKeyVaultId = "/subscriptions/[subscription-id-guid]/resourceGroups/[resource-group-name]/providers/Microsoft.KeyVault/vaults/[keyvault-name]"
    KeyEncryptionKeyUrl = "https://[keyvault-name].vault.azure.net/keys/[kekname]/[kek-unique-id]"
    VolumeType = "All"
}

$params | Set-AzVmDiskEncryptionExtension
```

Ez a példa bemutatja, hogyan lehet a paramétereket csővezetékes bemenettel elküldeni, hogy az AD-hitelesítő adatok megadása nélkül engedélyezze a titkosítást.  

### 3. példa: a titkosítás engedélyezése az Azure AD Client ID azonosítójával és az ügyfél titkos azonosítójával
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"
$AADClientID = "<clientID of your Azure AD app>"
$AADClientSecret = "<clientSecret of your Azure AD app>"
$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
Set-AzVMDiskEncryptionExtension -ResourceGroupName $RGName -VMName $VMName -AadClientID $AADClientID -AadClientSecret $AADClientSecret -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId
```

Ez a példa engedélyezi az Azure AD Client ID és az ügyfél titkos verziójának titkosítását.

### 4. példa: a titkosítás engedélyezése az Azure AD Client ID és az ügyfél tanúsítási ujjlenyomatával
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"
#The KeyVault must have enabledForDiskEncryption property set on it
$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId

# create Azure AD application and associate the certificate
$CertPath = "C:\certificates\examplecert.pfx"
$CertPassword = "Password"
$Cert = New-Object System.Security.Cryptography.X509Certificates.X509Certificate2($CertPath, $CertPassword)
$CertValue = [System.Convert]::ToBase64String($cert.GetRawCertData())
$AzureAdApplication = New-AzADApplication -DisplayName "<Your Application Display Name>" -HomePage "<https://YourApplicationHomePage>" -IdentifierUris "<https://YouApplicationUri>" -CertValue $CertValue 
$ServicePrincipal = New-AzADServicePrincipal -ApplicationId $AzureAdApplication.ApplicationId

$AADClientID = $AzureAdApplication.ApplicationId
$aadClientCertThumbprint= $cert.Thumbprint

#Upload pfx to KeyVault 
$KeyVaultSecretName = "MyAADCert"
$FileContentBytes = get-content $CertPath -Encoding Byte
$FileContentEncoded = [System.Convert]::ToBase64String($fileContentBytes)
$JSONObject = @"
    { 
        "data" : "$filecontentencoded", 
        "dataType" : "pfx", 
        "password" : "$CertPassword" 
    } 
"@
$JSONObjectBytes = [System.Text.Encoding]::UTF8.GetBytes($jsonObject)
$JSONEncoded = [System.Convert]::ToBase64String($jsonObjectBytes)

$Secret = ConvertTo-SecureString -String $JSONEncoded -AsPlainText -Force
Set-AzKeyVaultSecret -VaultName $VaultName -Name $KeyVaultSecretName -SecretValue $Secret
Set-AzKeyVaultAccessPolicy -VaultName $VaultName -ResourceGroupName $RGName -EnabledForDeployment

#deploy cert to VM
$CertUrl = (Get-AzKeyVaultSecret -VaultName $VaultName -Name $KeyVaultSecretName).Id
$SourceVaultId = (Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName).ResourceId
$VM = Get-AzVM -ResourceGroupName $RGName -Name $VMName 
$VM = Add-AzVMSecret -VM $VM -SourceVaultId $SourceVaultId -CertificateStore "My" -CertificateUrl $CertUrl
Update-AzVM -VM $VM -ResourceGroupName $RGName 

#Enable encryption on the virtual machine using Azure AD client ID and client cert thumbprint
Set-AzVMDiskEncryptionExtension -ResourceGroupName $RGName -VMName $VMName -AadClientID $AADClientID -AadClientCertThumbprint $AADClientCertThumbprint -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId
```

Ez a példa engedélyezi az Azure AD Client ID és az ügyfél tanúsítási thumbprints való titkosítást.

### Példa 5: a titkosítás engedélyezése Azure AD Client ID, Client Secret és wrap Disk titkosítási kulccsal a kulcs-titkosítási kulccsal
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"

$AADClientID = "<clientID of your Azure AD app>"
$AADClientSecret = "<clientSecret of your Azure AD app>"

$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId

$KEKName = "MyKeyEncryptionKey"
$KEK = Add-AzKeyVaultKey -VaultName $VaultName -Name $KEKName -Destination "Software"
$KeyEncryptionKeyUrl = $KEK.Key.kid

Set-AzVMDiskEncryptionExtension -ResourceGroupName $RGName -VMName $VMName -AadClientID $AADClientID -AadClientSecret $AADClientSecret -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl -KeyEncryptionKeyVaultId $KeyVaultResourceId
```

Ez a példa az Azure AD Client ID, az Client Secret és a wrap Disk titkosítási kulccsal titkosítja a titkosítást a kulcs titkosítási kulcs használatával.

### 6. példa: a titkosítás engedélyezése Azure AD Client ID, Client CERT ujjlenyomat és wrap Disk encryptionkey kulccsal a kulcs-titkosítási kulccsal
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"
#The KeyVault must have enabledForDiskEncryption property set on it
$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
$KEKName = "MyKeyEncryptionKey"
$KEK = Add-AzKeyVaultKey -VaultName $VaultName -Name $KEKName -Destination "Software"
$KeyEncryptionKeyUrl = $KEK.Key.kid

# create Azure AD application and associate the certificate
$CertPath = "C:\certificates\examplecert.pfx"
$CertPassword = "Password"
$Cert = New-Object System.Security.Cryptography.X509Certificates.X509Certificate2($CertPath, $CertPassword)
$CertValue = [System.Convert]::ToBase64String($cert.GetRawCertData())
$AzureAdApplication = New-AzADApplication -DisplayName "<Your Application Display Name>" -HomePage "<https://YourApplicationHomePage>" -IdentifierUris "<https://YouApplicationUri>" -CertValue $CertValue
$ServicePrincipal = New-AzADServicePrincipal -ApplicationId $AzureAdApplication.ApplicationId

$AADClientID = $AzureAdApplication.ApplicationId
$AADClientCertThumbprint= $Cert.Thumbprint

#Upload pfx to KeyVault 
$KeyVaultSecretName = "MyAADCert"
$FileContentBytes = get-content $CertPath -Encoding Byte
$FileContentEncoded = [System.Convert]::ToBase64String($FileContentBytes)
$JSONObject = @"
    { 
        "data" : "$filecontentencoded", 
        "dataType" : "pfx", 
        "password" : "$CertPassword" 
    } 
"@
$JSONObjectBytes = [System.Text.Encoding]::UTF8.GetBytes($JSONObject)
$JsonEncoded = [System.Convert]::ToBase64String($JSONObjectBytes)
$Secret = ConvertTo-SecureString -String $JSONEncoded -AsPlainText -Force
Set-AzKeyVaultSecret -VaultName $VaultName-Name $KeyVaultSecretName -SecretValue $Secret
Set-AzKeyVaultAccessPolicy -VaultName $VaultName -ResourceGroupName $RGName -EnabledForDeployment

#deploy cert to VM
$CertUrl = (Get-AzKeyVaultSecret -VaultName $VaultName -Name $KeyVaultSecretName).Id
$SourceVaultId = (Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName).ResourceId
$VM = Get-AzVM -ResourceGroupName $RGName -Name $VMName 
$VM = Add-AzVMSecret -VM $VM -SourceVaultId $SourceVaultId -CertificateStore "My" -CertificateUrl $CertUrl 
Update-AzVM -VM $VM -ResourceGroupName $RGName 

#Enable encryption on the virtual machine using Azure AD client ID and client cert thumbprint
Set-AzVMDiskEncryptionExtension -ResourceGroupName $RGname -VMName $VMName -AadClientID $AADClientID -AadClientCertThumbprint $AADClientCertThumbprint -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl -KeyEncryptionKeyVaultId $KeyVaultResourceId
```

Ez a példa lehetővé teszi a titkosítást az Azure AD Client ID, az ügyfél CERT ujjlenyomat és a wrap Disk titkosítási kulccsal a kulcs titkosítási kulccsal.

## PARAMÉTEREK

### -AadClientCertThumbprint
Itt adhatja meg a AzureActive-címtár (Azure AD) ügyfélalkalmazás ujjlenyomatát, amely jogosultságokkal rendelkezik a kulcsok **írásához.**
Előfeltételként az Azure AD ügyfélalkalmazás tanúsítványát előbb telepíteni kell a virtuális gép helyi `my` tanúsítványtárolójában.
Az Add-AzVMSecret parancsmag segítségével tanúsítványokat telepíthet egy virtuális gépre az Azure-ban.
További információt az **Add-AzVMSecret** parancsmag súgójában talál.
A tanúsítványt előzőleg telepíteni kell a virtuális gép helyi számítógépére a tanúsítványtárolóban.

```yaml
Type: System.String
Parameter Sets: AADClientCertParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AadClientID
Annak az Azure AD-alkalmazásnak az ügyfél-AZONOSÍTÓját adja meg, amely jogosultságokat **tartalmaz a kulcsok írásához.**

```yaml
Type: System.String
Parameter Sets: AADClientSecretParameterSet, AADClientCertParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AadClientSecret
Annak az Azure AD-alkalmazásnak az ügyfél titkát adja meg, amely jogosultságokat **tartalmaz a kulcsok írásához.**

```yaml
Type: System.String
Parameter Sets: AADClientSecretParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

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

### -DisableAutoUpgradeMinorVersion
Azt jelzi, hogy ez a parancsmag letiltja a bővítmény alverziójának automatikus frissítését.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 14
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DiskEncryptionKeyVaultId
Annak a kulcsnak az erőforrás **-** azonosítóját adja meg, amelybe a virtuálisgép-titkosítási kulcsokat fel szeretné tölteni.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DiskEncryptionKeyVaultUrl
Annak a billentyűzetnek **az URL-** címe, amelyhez a virtuális gép titkosítási kulcsait fel kell tölteni.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EncryptFormatAll
Az összes olyan adatmeghajtó Encrypt-Format, amely még nincs titkosítva

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

### -ExtensionPublisherName
A bővítmény közzétevője név. Csak akkor adja meg ezt a paramétert, ha a "Microsoft. Azure. Security" alapértelmezett értékét szeretné felülbírálni.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ExtensionType
A bővítmény típusa. Adja meg ezt a paramétert, ha a Windows VMs "AzureDiskEncryption" alapértelmezett értékét szeretné felülbírálni, és a Linux VMs esetében a "AzureDiskEncryptionForLinux".

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -KeyEncryptionAlgorithm
A virtuális gép kulcs-titkosítási kulcsának körbefuttatására és kicsomagolására szolgáló algoritmust adja meg.
Az alapértelmezett érték az RSA-OAEP.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: RSA-OAEP, RSA1_5

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -KeyEncryptionKeyUrl
Annak a kulcs titkosítási kulcsnak az URL-címét adja meg, amely a virtuálisgép-titkosítási kulcs körbefuttatásához és kicsomagolásához használatos.
Ennek a teljes verziójú URL-címnek kell lennie.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -KeyEncryptionKeyVaultId
**A virtuálisgép** -titkosítási kulcs körbefuttatását és kicsomagolását tartalmazó kulcs titkosítási kulcsát tartalmazó kulcskezelő erőforrás-azonosítóját adja meg.
Ennek a teljes verziójú URL-címnek kell lennie.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name (név)
A bővítményt jelképező Azure Resource Manager-erőforrás nevét adja meg.
Az alapértelmezett érték a AzureDiskEncryption, amely a Windows operációs rendszert futtató virtuális gépeket vagy a AzureDiskEncryptionForLinux virtuális gépeket futtatja.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 12
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Jelmondat
A Linux virtuális gépek titkosításához használt jelmondatot adja meg.
Ezt a paramétert nem használják a Windows operációs rendszert futtató virtuális gépekhez.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 13
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
A virtuális gép erőforráscsoport-csoportjának nevét adja meg.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SequenceVersion
A virtuális gép titkosítási műveleteinek sorszámát adja meg.
Ez a beállítás minden, ugyanazon a virtuális gépen végzett titkosítási műveletnél egyedi.
A Get-AzVMExtension parancsmag használatával lekérdezheti az előző sorszámot.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SkipVmBackup
A Linux VMs biztonsági másolatának kihagyása

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 15
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TypeHandlerVersion
A titkosítási bővítmény verziószámát adja meg.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMName
A virtuális gép nevét adja meg.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VolumeType
A titkosítási művelet végrehajtásához használt virtuálisgép-kötetek típusát adja meg.
A Windows operációs rendszert futtató virtuális gépek megengedett értékei az alábbiak: mind, operációs rendszer és adatok.
A linuxos virtuális gépek megengedett értékei a következők: csak adatok.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: OS, Data, All

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### System. String

### System. Management. Automation. SwitchParameter

## KIMENETEK

### Microsoft. Azure. commands. kiszámítás. models. PSAzureOperationResponse

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Add-AzVMSecret](./Add-AzVMSecret.md)

[Get-AzVMDiskEncryptionStatus](./Get-AzVMDiskEncryptionStatus.md)

[Remove-AzVMDiskEncryptionExtension](./Remove-AzVMDiskEncryptionExtension.md)


