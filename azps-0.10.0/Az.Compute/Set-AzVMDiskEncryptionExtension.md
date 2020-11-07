---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 6BCB36BC-F5E6-4EDD-983C-8BDE7A9B004D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmdiskencryptionextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMDiskEncryptionExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMDiskEncryptionExtension.md
ms.openlocfilehash: d4eb596ed7c6a002239b6e30869830596beba230
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844217"
---
# <span data-ttu-id="18e68-101">Set-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="18e68-101">Set-AzVMDiskEncryptionExtension</span></span>

## <span data-ttu-id="18e68-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="18e68-102">SYNOPSIS</span></span>
<span data-ttu-id="18e68-103">Engedélyezi a titkosítást egy futó IaaS virtuális gépen az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="18e68-103">Enables encryption on a running IaaS virtual machine in Azure.</span></span>

## <span data-ttu-id="18e68-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="18e68-104">SYNTAX</span></span>

### <span data-ttu-id="18e68-105">AADClientSecretParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="18e68-105">AADClientSecretParameterSet (Default)</span></span>
```
Set-AzVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [-AadClientID] <String>
 [-AadClientSecret] <String> [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String>
 [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>] [[-KeyEncryptionAlgorithm] <String>]
 [[-VolumeType] <String>] [[-SequenceVersion] <String>] [[-TypeHandlerVersion] <String>] [[-Name] <String>]
 [[-Passphrase] <String>] [-Force] [-DisableAutoUpgradeMinorVersion] [-SkipVmBackup] [-ExtensionType <String>]
 [-ExtensionPublisherName <String>] [-EncryptFormatAll] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18e68-106">AADClientCertParameterSet</span><span class="sxs-lookup"><span data-stu-id="18e68-106">AADClientCertParameterSet</span></span>
```
Set-AzVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [-AadClientID] <String>
 [-AadClientCertThumbprint] <String> [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String>
 [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>] [[-KeyEncryptionAlgorithm] <String>]
 [[-VolumeType] <String>] [[-SequenceVersion] <String>] [[-TypeHandlerVersion] <String>] [[-Name] <String>]
 [[-Passphrase] <String>] [-Force] [-DisableAutoUpgradeMinorVersion] [-SkipVmBackup] [-ExtensionType <String>]
 [-ExtensionPublisherName <String>] [-EncryptFormatAll] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="18e68-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="18e68-107">DESCRIPTION</span></span>
<span data-ttu-id="18e68-108">A **set-AzVMDiskEncryptionExtension** parancsmag egy futó infrastruktúra titkosítását engedélyezi az Azure rendszer Service (IaaS) virtuális számítógépén.</span><span class="sxs-lookup"><span data-stu-id="18e68-108">The **Set-AzVMDiskEncryptionExtension** cmdlet enables encryption on a running infrastructure as a service (IaaS) virtual machine in Azure.</span></span>
<span data-ttu-id="18e68-109">Ez a parancsmag lehetővé teszi a titkosítást, ha telepíti a merevlemez-titkosítási bővítményt a virtuális gépen.</span><span class="sxs-lookup"><span data-stu-id="18e68-109">This cmdlet enables encryption by installing the disk encryption extension on the virtual machine.</span></span>
<span data-ttu-id="18e68-110">Ha nincs megadva *név* paraméter, akkor a program a Windows operációs rendszert futtató virtuális gépekhez használt alapértelmezett név AzureDiskEncryption, illetve a AzureDiskEncryptionForLinux virtuális gépekhez telepített virtuális gépekhez bővítményt tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="18e68-110">If no *Name* parameter is specified, an extension with the default name AzureDiskEncryption for virtual machines that run the Windows operating system or AzureDiskEncryptionForLinux for Linux virtual machines are installed.</span></span>
<span data-ttu-id="18e68-111">Ehhez a parancsmaghoz a felhasználóknak megerősítést kell engedélyezni a virtuális gép újraindítását igénylik.</span><span class="sxs-lookup"><span data-stu-id="18e68-111">This cmdlet requires confirmation from the users as one of the steps to enable encryption requires a restart of the virtual machine.</span></span>
<span data-ttu-id="18e68-112">Javasoljuk, hogy a parancsmag futtatása előtt mentse a munkáját a virtuális gépen.</span><span class="sxs-lookup"><span data-stu-id="18e68-112">It is advised that you save your work on the virtual machine before you run this cmdlet.</span></span>

## <span data-ttu-id="18e68-113">Példák</span><span class="sxs-lookup"><span data-stu-id="18e68-113">EXAMPLES</span></span>

### <span data-ttu-id="18e68-114">1. példa: a titkosítás engedélyezése az Azure AD Client ID azonosítójával és az ügyfél titkos azonosítójával</span><span class="sxs-lookup"><span data-stu-id="18e68-114">Example 1: Enable encryption using Azure AD Client ID and Client Secret</span></span>
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

<span data-ttu-id="18e68-115">Ez a példa engedélyezi az Azure AD Client ID és az ügyfél titkos verziójának titkosítását.</span><span class="sxs-lookup"><span data-stu-id="18e68-115">This example enables encryption using Azure AD client ID, and client secret.</span></span>

### <span data-ttu-id="18e68-116">2. példa: a titkosítás engedélyezése az Azure AD Client ID és az ügyfél tanúsítási ujjlenyomatával</span><span class="sxs-lookup"><span data-stu-id="18e68-116">Example 2: Enable encryption using Azure AD client ID and client certification thumbprint</span></span>
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
$KeyValue = [System.Convert]::ToBase64String($cert.GetRawCertData())
$AzureAdApplication = New-AzADApplication -DisplayName "<Your Application Display Name>" -HomePage "<https://YourApplicationHomePage>" -IdentifierUris "<https://YouApplicationUri>" -KeyValue $KeyValue -KeyType AsymmetricX509Cert 
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
Set-AzureKeyVaultSecret -VaultName $VaultName -Name $KeyVaultSecretName -SecretValue $Secret
Set-AzKeyVaultAccessPolicy -VaultName $VaultName -ResourceGroupName $RGName -EnabledForDeployment

#deploy cert to VM
$CertUrl = (Get-AzureKeyVaultSecret -VaultName $VaultName -Name $KeyVaultSecretName).Id
$SourceVaultId = (Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName).ResourceId
$VM = Get-AzVM -ResourceGroupName $RGName -Name $VMName 
$VM = Add-AzVMSecret -VM $VM -SourceVaultId $SourceVaultId -CertificateStore "My" -CertificateUrl $CertUrl
Update-AzVM -VM $VM -ResourceGroupName $RGName 

#Enable encryption on the virtual machine using Azure AD client ID and client cert thumbprint
Set-AzVMDiskEncryptionExtension -ResourceGroupName $RGName -VMName $VMName -AadClientID $AADClientID -AadClientCertThumbprint $AADClientCertThumbprint -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="18e68-117">Ez a példa engedélyezi az Azure AD Client ID és az ügyfél tanúsítási thumbprints való titkosítást.</span><span class="sxs-lookup"><span data-stu-id="18e68-117">This example enables encryption using Azure AD client ID and client certification thumbprints.</span></span>

### <span data-ttu-id="18e68-118">3. példa: a titkosítás engedélyezése Azure AD Client ID, Client Secret és wrap Disk titkosítási kulccsal a kulcs titkosítási kulccsal</span><span class="sxs-lookup"><span data-stu-id="18e68-118">Example 3: Enable encryption using Azure AD client ID, client secret, and wrap disk encryption key by using key encryption key</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"

$AADClientID = "<clientID of your Azure AD app>"
$AADClientSecret = "<clientSecret of your Azure AD app>"

$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId

$KEK = Add-AzureKeyVaultKey -VaultName $VaultName -Name $KEKName -Destination "Software"
$KeyEncryptionKeyUrl = $KEK.Key.kid

Set-AzVMDiskEncryptionExtension -ResourceGroupName $RGName -VMName $VMName -AadClientID $AADClientID -AadClientSecret $AADClientSecret -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl -KeyEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="18e68-119">Ez a példa az Azure AD Client ID, az Client Secret és a wrap Disk titkosítási kulccsal titkosítja a titkosítást a kulcs titkosítási kulcs használatával.</span><span class="sxs-lookup"><span data-stu-id="18e68-119">This example enables encryption using Azure AD client ID, client secret, and wrap disk encryption key by using the key encryption key.</span></span>

### <span data-ttu-id="18e68-120">4. példa: a titkosítás engedélyezése Azure AD Client ID, Client CERT ujjlenyomat és wrap Disk encryptionkey kulccsal a kulcs-titkosítási kulccsal</span><span class="sxs-lookup"><span data-stu-id="18e68-120">Example 4: Enable encryption using Azure AD client ID, client cert thumbprint, and wrap disk encryptionkey by using key encryption key</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"
#The KeyVault must have enabledForDiskEncryption property set on it
$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
$KEK = Add-AzureKeyVaultKey -VaultName $VaultName -Name $KEKName -Destination "Software"
$KeyEncryptionKeyUrl = $KEK.Key.kid

# create Azure AD application and associate the certificate
$CertPath = "C:\certificates\examplecert.pfx"
$CertPassword = "Password"
$Cert = New-Object System.Security.Cryptography.X509Certificates.X509Certificate2($CertPath, $CertPassword)
$KeyValue = [System.Convert]::ToBase64String($cert.GetRawCertData())
$AzureAdApplication = New-AzADApplication -DisplayName "<Your Application Display Name>" -HomePage "<https://YourApplicationHomePage>" -IdentifierUris "<https://YouApplicationUri>" -KeyValue $KeyValue -KeyType AsymmetricX509Cert 
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
Set-AzureKeyVaultSecret -VaultName $VaultName-Name $KeyVaultSecretName -SecretValue $Secret
Set-AzKeyVaultAccessPolicy -VaultName $VaultName -ResourceGroupName $RGName -EnabledForDeployment

#deploy cert to VM
$CertUrl = (Get-AzureKeyVaultSecret -VaultName $VaultName -Name $KeyVaultSecretName).Id
$SourceVaultId = (Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName).ResourceId
$VM = Get-AzVM -ResourceGroupName $RGName -Name $VMName 
$VM = Add-AzVMSecret -VM $VM -SourceVaultId $SourceVaultId -CertificateStore "My" -CertificateUrl $CertUrl 
Update-AzVM -VM $VM -ResourceGroupName $RGName 

#Enable encryption on the virtual machine using Azure AD client ID and client cert thumbprint
Set-AzVMDiskEncryptionExtension -ResourceGroupName $RGname -VMName $VMName -AadClientID $AADClientID -AadClientCertThumbprint $AADClientCertThumbprint -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="18e68-121">Ez a példa lehetővé teszi a titkosítást az Azure AD Client ID, az ügyfél CERT ujjlenyomat és a wrap Disk titkosítási kulccsal a kulcs titkosítási kulccsal.</span><span class="sxs-lookup"><span data-stu-id="18e68-121">This example enables encryption using Azure AD client ID, client cert thumbprint, and wrap disk encryption key by using key encryption key.</span></span>

## <span data-ttu-id="18e68-122">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="18e68-122">PARAMETERS</span></span>

### <span data-ttu-id="18e68-123">-AadClientCertThumbprint</span><span class="sxs-lookup"><span data-stu-id="18e68-123">-AadClientCertThumbprint</span></span>
<span data-ttu-id="18e68-124">Itt adhatja meg a AzureActive-címtár (Azure AD) ügyfélalkalmazás ujjlenyomatát, amely jogosultságokkal rendelkezik a kulcsok **írásához.**</span><span class="sxs-lookup"><span data-stu-id="18e68-124">Specifies the thumbprint of the AzureActive Directory (Azure AD) application client certificate that has permissions to write secrets to **KeyVault**.</span></span>
<span data-ttu-id="18e68-125">Előfeltételként az Azure AD ügyfélalkalmazás tanúsítványát előbb telepíteni kell a virtuális gép helyi `my` tanúsítványtárolójában.</span><span class="sxs-lookup"><span data-stu-id="18e68-125">As a prerequisite, the Azure AD client certificate must be previously deployed to the virtual machine's local computer `my` certificate store.</span></span>
<span data-ttu-id="18e68-126">Az Add-AzVMSecret parancsmag segítségével tanúsítványokat telepíthet egy virtuális gépre az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="18e68-126">The Add-AzVMSecret cmdlet can be used to deploy a certificate to a virtual machine in Azure.</span></span>
<span data-ttu-id="18e68-127">További információt az **Add-AzVMSecret** parancsmag súgójában talál.</span><span class="sxs-lookup"><span data-stu-id="18e68-127">For more details, see the **Add-AzVMSecret** cmdlet help.</span></span>
<span data-ttu-id="18e68-128">A tanúsítványt előzőleg telepíteni kell a virtuális gép helyi számítógépére a tanúsítványtárolóban.</span><span class="sxs-lookup"><span data-stu-id="18e68-128">The certificate must be previously deployed to the virtual machine local computer my certificate store.</span></span>

```yaml
Type: String
Parameter Sets: AADClientCertParameterSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18e68-129">-AadClientID</span><span class="sxs-lookup"><span data-stu-id="18e68-129">-AadClientID</span></span>
<span data-ttu-id="18e68-130">Annak az Azure AD-alkalmazásnak az ügyfél-AZONOSÍTÓját adja meg, amely jogosultságokat **tartalmaz a kulcsok írásához.**</span><span class="sxs-lookup"><span data-stu-id="18e68-130">Specifies the client ID of the Azure AD application that has permissions to write secrets to **KeyVault**.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18e68-131">-AadClientSecret</span><span class="sxs-lookup"><span data-stu-id="18e68-131">-AadClientSecret</span></span>
<span data-ttu-id="18e68-132">Annak az Azure AD-alkalmazásnak az ügyfél titkát adja meg, amely jogosultságokat **tartalmaz a kulcsok írásához.**</span><span class="sxs-lookup"><span data-stu-id="18e68-132">Specifies the client secret of the Azure AD application that has permissions to write secrets to **KeyVault**.</span></span>

```yaml
Type: String
Parameter Sets: AADClientSecretParameterSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18e68-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18e68-133">-DefaultProfile</span></span>
<span data-ttu-id="18e68-134">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="18e68-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="18e68-135">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="18e68-135">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="18e68-136">Azt jelzi, hogy ez a parancsmag letiltja a bővítmény alverziójának automatikus frissítését.</span><span class="sxs-lookup"><span data-stu-id="18e68-136">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 14
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18e68-137">-DiskEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="18e68-137">-DiskEncryptionKeyVaultId</span></span>
<span data-ttu-id="18e68-138">Annak a kulcsnak az erőforrás **-** azonosítóját adja meg, amelybe a virtuálisgép-titkosítási kulcsokat fel szeretné tölteni.</span><span class="sxs-lookup"><span data-stu-id="18e68-138">Specifies the resource ID of the **KeyVault** to which the virtual machine encryption keys should be uploaded.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18e68-139">-DiskEncryptionKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="18e68-139">-DiskEncryptionKeyVaultUrl</span></span>
<span data-ttu-id="18e68-140">Annak a billentyűzetnek **az URL-** címe, amelyhez a virtuális gép titkosítási kulcsait fel kell tölteni.</span><span class="sxs-lookup"><span data-stu-id="18e68-140">Specifies the **KeyVault** URL to which the virtual machine encryption keys should be uploaded.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18e68-141">-EncryptFormatAll</span><span class="sxs-lookup"><span data-stu-id="18e68-141">-EncryptFormatAll</span></span>
<span data-ttu-id="18e68-142">Az összes olyan adatmeghajtó Encrypt-Format, amely még nincs titkosítva</span><span class="sxs-lookup"><span data-stu-id="18e68-142">Encrypt-Format all data drives that are not already encrypted</span></span>

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

### <span data-ttu-id="18e68-143">-ExtensionPublisherName</span><span class="sxs-lookup"><span data-stu-id="18e68-143">-ExtensionPublisherName</span></span>
<span data-ttu-id="18e68-144">A bővítmény közzétevője név.</span><span class="sxs-lookup"><span data-stu-id="18e68-144">The extension publisher name.</span></span> <span data-ttu-id="18e68-145">Csak akkor adja meg ezt a paramétert, ha a "Microsoft. Azure. Security" alapértelmezett értékét szeretné felülbírálni.</span><span class="sxs-lookup"><span data-stu-id="18e68-145">Specify this parameter only to override the default value of "Microsoft.Azure.Security".</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18e68-146">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="18e68-146">-ExtensionType</span></span>
<span data-ttu-id="18e68-147">A bővítmény típusa.</span><span class="sxs-lookup"><span data-stu-id="18e68-147">The extension type.</span></span> <span data-ttu-id="18e68-148">Adja meg ezt a paramétert, ha a Windows VMs "AzureDiskEncryption" alapértelmezett értékét szeretné felülbírálni, és a Linux VMs esetében a "AzureDiskEncryptionForLinux".</span><span class="sxs-lookup"><span data-stu-id="18e68-148">Specify this parameter to override its default value of "AzureDiskEncryption" for Windows VMs and "AzureDiskEncryptionForLinux" for Linux VMs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18e68-149">-Force</span><span class="sxs-lookup"><span data-stu-id="18e68-149">-Force</span></span>
<span data-ttu-id="18e68-150">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="18e68-150">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="18e68-151">-KeyEncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="18e68-151">-KeyEncryptionAlgorithm</span></span>
<span data-ttu-id="18e68-152">A virtuális gép kulcs-titkosítási kulcsának körbefuttatására és kicsomagolására szolgáló algoritmust adja meg.</span><span class="sxs-lookup"><span data-stu-id="18e68-152">Specifies the algorithm that is used to wrap and unwrap the key encryption key of the virtual machine.</span></span>
<span data-ttu-id="18e68-153">Az alapértelmezett érték az RSA-OAEP.</span><span class="sxs-lookup"><span data-stu-id="18e68-153">The default value is RSA-OAEP.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: RSA-OAEP, RSA1_5

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18e68-154">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="18e68-154">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="18e68-155">Annak a kulcs titkosítási kulcsnak az URL-címét adja meg, amely a virtuálisgép-titkosítási kulcs körbefuttatásához és kicsomagolásához használatos.</span><span class="sxs-lookup"><span data-stu-id="18e68-155">Specifies the URL of the key encryption key that is used to wrap and unwrap the virtual machine encryption key.</span></span>
<span data-ttu-id="18e68-156">Ennek a teljes verziójú URL-címnek kell lennie.</span><span class="sxs-lookup"><span data-stu-id="18e68-156">This must be the full versioned URL.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18e68-157">-KeyEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="18e68-157">-KeyEncryptionKeyVaultId</span></span>
<span data-ttu-id="18e68-158">**A virtuálisgép** -titkosítási kulcs körbefuttatását és kicsomagolását tartalmazó kulcs titkosítási kulcsát tartalmazó kulcskezelő erőforrás-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="18e68-158">Specifies the resource ID of the **KeyVault** that contains key encryption key that is used to wrap and unwrap the virtual machine encryption key.</span></span>
<span data-ttu-id="18e68-159">Ennek a teljes verziójú URL-címnek kell lennie.</span><span class="sxs-lookup"><span data-stu-id="18e68-159">This must be a full versioned URL.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18e68-160">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="18e68-160">-Name</span></span>
<span data-ttu-id="18e68-161">A bővítményt jelképező Azure Resource Manager-erőforrás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="18e68-161">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="18e68-162">Az alapértelmezett érték a AzureDiskEncryption, amely a Windows operációs rendszert futtató virtuális gépeket vagy a AzureDiskEncryptionForLinux virtuális gépeket futtatja.</span><span class="sxs-lookup"><span data-stu-id="18e68-162">The default value is AzureDiskEncryption for virtual machines that run the Windows operating system or AzureDiskEncryptionForLinux for Linux virtual machines.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 12
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18e68-163">-Jelmondat</span><span class="sxs-lookup"><span data-stu-id="18e68-163">-Passphrase</span></span>
<span data-ttu-id="18e68-164">A Linux virtuális gépek titkosításához használt jelmondatot adja meg.</span><span class="sxs-lookup"><span data-stu-id="18e68-164">Specifies the passphrase used for encrypting Linux virtual machines only.</span></span>
<span data-ttu-id="18e68-165">Ezt a paramétert nem használják a Windows operációs rendszert futtató virtuális gépekhez.</span><span class="sxs-lookup"><span data-stu-id="18e68-165">This parameter is not used for virtual machines that run the Windows operating system.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 13
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18e68-166">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18e68-166">-ResourceGroupName</span></span>
<span data-ttu-id="18e68-167">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="18e68-167">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="18e68-168">-SequenceVersion</span><span class="sxs-lookup"><span data-stu-id="18e68-168">-SequenceVersion</span></span>
<span data-ttu-id="18e68-169">A virtuális gép titkosítási műveleteinek sorszámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="18e68-169">Specifies the sequence number of the encryption operations for a virtual machine.</span></span>
<span data-ttu-id="18e68-170">Ez a beállítás minden, ugyanazon a virtuális gépen végzett titkosítási műveletnél egyedi.</span><span class="sxs-lookup"><span data-stu-id="18e68-170">This is unique per each encryption operation performed on the same virtual machine.</span></span>
<span data-ttu-id="18e68-171">A Get-AzVMExtension parancsmag használatával lekérdezheti az előző sorszámot.</span><span class="sxs-lookup"><span data-stu-id="18e68-171">The Get-AzVMExtension cmdlet can be used to retrieve the previous sequence number that was used.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18e68-172">-SkipVmBackup</span><span class="sxs-lookup"><span data-stu-id="18e68-172">-SkipVmBackup</span></span>
<span data-ttu-id="18e68-173">A Linux VMs biztonsági másolatának kihagyása</span><span class="sxs-lookup"><span data-stu-id="18e68-173">Skip backup creation for Linux VMs</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 15
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18e68-174">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="18e68-174">-TypeHandlerVersion</span></span>
<span data-ttu-id="18e68-175">A titkosítási bővítmény verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="18e68-175">Specifies the version of the encryption extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18e68-176">-VMName</span><span class="sxs-lookup"><span data-stu-id="18e68-176">-VMName</span></span>
<span data-ttu-id="18e68-177">A virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="18e68-177">Specifies the name of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18e68-178">-VolumeType</span><span class="sxs-lookup"><span data-stu-id="18e68-178">-VolumeType</span></span>
<span data-ttu-id="18e68-179">A titkosítási művelet végrehajtásához használt virtuálisgép-kötetek típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="18e68-179">Specifies the type of virtual machine volumes to perform the encryption operation.</span></span>
<span data-ttu-id="18e68-180">A Windows operációs rendszert futtató virtuális gépek megengedett értékei az alábbiak: mind, operációs rendszer és adatok.</span><span class="sxs-lookup"><span data-stu-id="18e68-180">Allowed values for virtual machines that run the Windows operating system are as follows: All, OS, and Data.</span></span>
<span data-ttu-id="18e68-181">A linuxos virtuális gépek megengedett értékei a következők: csak adatok.</span><span class="sxs-lookup"><span data-stu-id="18e68-181">The allowed values for Linux virtual machines are as follows: Data only.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: OS, Data, All

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18e68-182">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="18e68-182">-Confirm</span></span>
<span data-ttu-id="18e68-183">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="18e68-183">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18e68-184">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18e68-184">-WhatIf</span></span>
<span data-ttu-id="18e68-185">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="18e68-185">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="18e68-186">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="18e68-186">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18e68-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18e68-187">CommonParameters</span></span>
<span data-ttu-id="18e68-188">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="18e68-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18e68-189">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18e68-189">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18e68-190">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="18e68-190">INPUTS</span></span>

### <span data-ttu-id="18e68-191">Nincs</span><span class="sxs-lookup"><span data-stu-id="18e68-191">None</span></span>
<span data-ttu-id="18e68-192">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="18e68-192">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="18e68-193">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="18e68-193">OUTPUTS</span></span>

### <span data-ttu-id="18e68-194">Microsoft. Azure. commands. kiszámítás. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="18e68-194">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="18e68-195">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="18e68-195">NOTES</span></span>

## <span data-ttu-id="18e68-196">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="18e68-196">RELATED LINKS</span></span>

[<span data-ttu-id="18e68-197">Add-AzVMSecret</span><span class="sxs-lookup"><span data-stu-id="18e68-197">Add-AzVMSecret</span></span>](./Add-AzVMSecret.md)

[<span data-ttu-id="18e68-198">Get-AzVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="18e68-198">Get-AzVMDiskEncryptionStatus</span></span>](./Get-AzVMDiskEncryptionStatus.md)

[<span data-ttu-id="18e68-199">Remove-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="18e68-199">Remove-AzVMDiskEncryptionExtension</span></span>](./Remove-AzVMDiskEncryptionExtension.md)


