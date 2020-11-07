---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 6BCB36BC-F5E6-4EDD-983C-8BDE7A9B004D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMDiskEncryptionExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMDiskEncryptionExtension.md
ms.openlocfilehash: ed18e7de10df5762309f3bcd4ddf6dcee7ee1b94
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672750"
---
# <span data-ttu-id="323b1-101">Set-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="323b1-101">Set-AzureRmVMDiskEncryptionExtension</span></span>

## <span data-ttu-id="323b1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="323b1-102">SYNOPSIS</span></span>
<span data-ttu-id="323b1-103">Engedélyezi a titkosítást egy futó IaaS virtuális gépen az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="323b1-103">Enables encryption on a running IaaS virtual machine in Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="323b1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="323b1-104">SYNTAX</span></span>

### <span data-ttu-id="323b1-105">AAD-ügyfél titkos paraméterei (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="323b1-105">AAD Client Secret Parameters (Default)</span></span>
```
Set-AzureRmVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [-AadClientID] <String>
 [-AadClientSecret] <String> [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String>
 [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>] [[-KeyEncryptionAlgorithm] <String>]
 [[-VolumeType] <String>] [[-SequenceVersion] <String>] [[-TypeHandlerVersion] <String>] [[-Name] <String>]
 [[-Passphrase] <String>] [-Force] [-DisableAutoUpgradeMinorVersion] [-SkipVmBackup] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="323b1-106">AAD ügyfél CERT-paraméterei</span><span class="sxs-lookup"><span data-stu-id="323b1-106">AAD Client Cert Parameters</span></span>
```
Set-AzureRmVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [-AadClientID] <String>
 [-AadClientCertThumbprint] <String> [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String>
 [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>] [[-KeyEncryptionAlgorithm] <String>]
 [[-VolumeType] <String>] [[-SequenceVersion] <String>] [[-TypeHandlerVersion] <String>] [[-Name] <String>]
 [[-Passphrase] <String>] [-Force] [-DisableAutoUpgradeMinorVersion] [-SkipVmBackup] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="323b1-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="323b1-107">DESCRIPTION</span></span>
<span data-ttu-id="323b1-108">A **set-AzureRmVMDiskEncryptionExtension** parancsmag egy futó infrastruktúra titkosítását engedélyezi az Azure rendszer Service (IaaS) virtuális számítógépén.</span><span class="sxs-lookup"><span data-stu-id="323b1-108">The **Set-AzureRmVMDiskEncryptionExtension** cmdlet enables encryption on a running infrastructure as a service (IaaS) virtual machine in Azure.</span></span>
<span data-ttu-id="323b1-109">Ez a parancsmag lehetővé teszi a titkosítást, ha telepíti a merevlemez-titkosítási bővítményt a virtuális gépen.</span><span class="sxs-lookup"><span data-stu-id="323b1-109">This cmdlet enables encryption by installing the disk encryption extension on the virtual machine.</span></span>
<span data-ttu-id="323b1-110">Ha nincs megadva *név* paraméter, akkor a program a Windows operációs rendszert futtató virtuális gépekhez használt alapértelmezett név AzureDiskEncryption, illetve a AzureDiskEncryptionForLinux virtuális gépekhez telepített virtuális gépekhez bővítményt tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="323b1-110">If no *Name* parameter is specified, an extension with the default name AzureDiskEncryption for virtual machines that run the Windows operating system or AzureDiskEncryptionForLinux for Linux virtual machines are installed.</span></span>
<span data-ttu-id="323b1-111">Ehhez a parancsmaghoz a felhasználóknak megerősítést kell engedélyezni a virtuális gép újraindítását igénylik.</span><span class="sxs-lookup"><span data-stu-id="323b1-111">This cmdlet requires confirmation from the users as one of the steps to enable encryption requires a restart of the virtual machine.</span></span>
<span data-ttu-id="323b1-112">Javasoljuk, hogy a parancsmag futtatása előtt mentse a munkáját a virtuális gépen.</span><span class="sxs-lookup"><span data-stu-id="323b1-112">It is advised that you save your work on the virtual machine before you run this cmdlet.</span></span>

## <span data-ttu-id="323b1-113">Példák</span><span class="sxs-lookup"><span data-stu-id="323b1-113">EXAMPLES</span></span>

### <span data-ttu-id="323b1-114">1. példa: a titkosítás engedélyezése az Azure AD Client ID azonosítójával és az ügyfél titkos azonosítójával</span><span class="sxs-lookup"><span data-stu-id="323b1-114">Example 1: Enable encryption using Azure AD Client ID and Client Secret</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"
$AADClientID = "<clientID of your Azure AD app>"
$AADClientSecret = "<clientSecret of your Azure AD app>"
$VaultName= "MyKeyVault"
$KeyVault = Get-AzureRmKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
Set-AzureRmVMDiskEncryptionExtension -ResourceGroupName $RGName -VMName $VMName -AadClientID $AADClientID -AadClientSecret $AADClientSecret -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="323b1-115">Ez a példa engedélyezi az Azure AD Client ID és az ügyfél titkos verziójának titkosítását.</span><span class="sxs-lookup"><span data-stu-id="323b1-115">This example enables encryption using Azure AD client ID, and client secret.</span></span>

### <span data-ttu-id="323b1-116">2. példa: a titkosítás engedélyezése az Azure AD Client ID és az ügyfél tanúsítási ujjlenyomatával</span><span class="sxs-lookup"><span data-stu-id="323b1-116">Example 2: Enable encryption using Azure AD client ID and client certification thumbprint</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"
#The KeyVault must have enabledForDiskEncryption property set on it
$VaultName= "MyKeyVault"
$KeyVault = Get-AzureRmKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId

# create Azure AD application and associate the certificate
$CertPath = "C:\certificates\examplecert.pfx"
$CertPassword = "Password"
$Cert = New-Object System.Security.Cryptography.X509Certificates.X509Certificate2($CertPath, $CertPassword)
$KeyValue = [System.Convert]::ToBase64String($cert.GetRawCertData())
$AzureAdApplication = New-AzureRmADApplication -DisplayName "<Your Application Display Name>" -HomePage "<https://YourApplicationHomePage>" -IdentifierUris "<https://YouApplicationUri>" -KeyValue $KeyValue -KeyType AsymmetricX509Cert 
$ServicePrincipal = New-AzureRmADServicePrincipal -ApplicationId $AzureAdApplication.ApplicationId

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
Set-AzureRmKeyVaultAccessPolicy -VaultName $VaultName -ResourceGroupName $RGName -EnabledForDeployment

#deploy cert to VM
$CertUrl = (Get-AzureKeyVaultSecret -VaultName $VaultName -Name $KeyVaultSecretName).Id
$SourceVaultId = (Get-AzureRmKeyVault -VaultName $VaultName -ResourceGroupName $RGName).ResourceId
$VM = Get-AzureRmVM -ResourceGroupName $RGName -Name $VMName 
$VM = Add-AzureRmVMSecret -VM $VM -SourceVaultId $SourceVaultId -CertificateStore "My" -CertificateUrl $CertUrl
Update-AzureRmVM -VM $VM -ResourceGroupName $RGName 

#Enable encryption on the virtual machine using Azure AD client ID and client cert thumbprint
Set-AzureRmVMDiskEncryptionExtension -ResourceGroupName $RGName -VMName $VMName -AadClientID $AADClientID -AadClientCertThumbprint $AADClientCertThumbprint -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="323b1-117">Ez a példa engedélyezi az Azure AD Client ID és az ügyfél tanúsítási thumbprints való titkosítást.</span><span class="sxs-lookup"><span data-stu-id="323b1-117">This example enables encryption using Azure AD client ID and client certification thumbprints.</span></span>

### <span data-ttu-id="323b1-118">3. példa: a titkosítás engedélyezése Azure AD Client ID, Client Secret és wrap Disk titkosítási kulccsal a kulcs titkosítási kulccsal</span><span class="sxs-lookup"><span data-stu-id="323b1-118">Example 3: Enable encryption using Azure AD client ID, client secret, and wrap disk encryption key by using key encryption key</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"

$AADClientID = "<clientID of your Azure AD app>"
$AADClientSecret = "<clientSecret of your Azure AD app>"

$VaultName= "MyKeyVault"
$KeyVault = Get-AzureRmKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId

$KEK = Add-AzureKeyVaultKey -VaultName $VaultName -Name $KEKName -Destination "Software"
$KeyEncryptionKeyUrl = $KEK.Key.kid

Set-AzureRmVMDiskEncryptionExtension -ResourceGroupName $RGName -VMName $VMName -AadClientID $AADClientID -AadClientSecret $AADClientSecret -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl -KeyEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="323b1-119">Ez a példa az Azure AD Client ID, az Client Secret és a wrap Disk titkosítási kulccsal titkosítja a titkosítást a kulcs titkosítási kulcs használatával.</span><span class="sxs-lookup"><span data-stu-id="323b1-119">This example enables encryption using Azure AD client ID, client secret, and wrap disk encryption key by using the key encryption key.</span></span>

### <span data-ttu-id="323b1-120">4. példa: a titkosítás engedélyezése Azure AD Client ID, Client CERT ujjlenyomat és wrap Disk encryptionkey kulccsal a kulcs-titkosítási kulccsal</span><span class="sxs-lookup"><span data-stu-id="323b1-120">Example 4: Enable encryption using Azure AD client ID, client cert thumbprint, and wrap disk encryptionkey by using key encryption key</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"
#The KeyVault must have enabledForDiskEncryption property set on it
$VaultName= "MyKeyVault"
$KeyVault = Get-AzureRmKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
$KEK = Add-AzureKeyVaultKey -VaultName $VaultName -Name $KEKName -Destination "Software"
$KeyEncryptionKeyUrl = $KEK.Key.kid

# create Azure AD application and associate the certificate
$CertPath = "C:\certificates\examplecert.pfx"
$CertPassword = "Password"
$Cert = New-Object System.Security.Cryptography.X509Certificates.X509Certificate2($CertPath, $CertPassword)
$KeyValue = [System.Convert]::ToBase64String($cert.GetRawCertData())
$AzureAdApplication = New-AzureRmADApplication -DisplayName "<Your Application Display Name>" -HomePage "<https://YourApplicationHomePage>" -IdentifierUris "<https://YouApplicationUri>" -KeyValue $KeyValue -KeyType AsymmetricX509Cert 
$ServicePrincipal = New-AzureRmADServicePrincipal -ApplicationId $AzureAdApplication.ApplicationId

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
Set-AzureRmKeyVaultAccessPolicy -VaultName $VaultName -ResourceGroupName $RGName -EnabledForDeployment

#deploy cert to VM
$CertUrl = (Get-AzureKeyVaultSecret -VaultName $VaultName -Name $KeyVaultSecretName).Id
$SourceVaultId = (Get-AzureRmKeyVault -VaultName $VaultName -ResourceGroupName $RGName).ResourceId
$VM = Get-AzureRmVM -ResourceGroupName $RGName -Name $VMName 
$VM = Add-AzureRmVMSecret -VM $VM -SourceVaultId $SourceVaultId -CertificateStore "My" -CertificateUrl $CertUrl 
Update-AzureRmVM -VM $VM -ResourceGroupName $RGName 

#Enable encryption on the virtual machine using Azure AD client ID and client cert thumbprint
Set-AzureRmVMDiskEncryptionExtension -ResourceGroupName $RGname -VMName $VMName -AadClientID $AADClientID -AadClientCertThumbprint $AADClientCertThumbprint -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="323b1-121">Ez a példa lehetővé teszi a titkosítást az Azure AD Client ID, az ügyfél CERT ujjlenyomat és a wrap Disk titkosítási kulccsal a kulcs titkosítási kulccsal.</span><span class="sxs-lookup"><span data-stu-id="323b1-121">This example enables encryption using Azure AD client ID, client cert thumbprint, and wrap disk encryption key by using key encryption key.</span></span>

## <span data-ttu-id="323b1-122">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="323b1-122">PARAMETERS</span></span>

### <span data-ttu-id="323b1-123">-AadClientCertThumbprint</span><span class="sxs-lookup"><span data-stu-id="323b1-123">-AadClientCertThumbprint</span></span>
<span data-ttu-id="323b1-124">Itt adhatja meg a AzureActive-címtár (Azure AD) ügyfélalkalmazás ujjlenyomatát, amely jogosultságokkal rendelkezik a kulcsok **írásához.**</span><span class="sxs-lookup"><span data-stu-id="323b1-124">Specifies the thumbprint of the AzureActive Directory (Azure AD) application client certificate that has permissions to write secrets to **KeyVault**.</span></span>
<span data-ttu-id="323b1-125">Előfeltételként az Azure AD ügyfélalkalmazás tanúsítványát előbb telepíteni kell a virtuális gép helyi `my` tanúsítványtárolójában.</span><span class="sxs-lookup"><span data-stu-id="323b1-125">As a prerequisite, the Azure AD client certificate must be previously deployed to the virtual machine's local computer `my` certificate store.</span></span>
<span data-ttu-id="323b1-126">Az Add-AzureRmVMSecret parancsmag segítségével tanúsítványokat telepíthet egy virtuális gépre az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="323b1-126">The Add-AzureRmVMSecret cmdlet can be used to deploy a certificate to a virtual machine in Azure.</span></span>
<span data-ttu-id="323b1-127">További információt az **Add-AzureRmVMSecret** parancsmag súgójában talál.</span><span class="sxs-lookup"><span data-stu-id="323b1-127">For more details, see the **Add-AzureRmVMSecret** cmdlet help.</span></span>
<span data-ttu-id="323b1-128">A tanúsítványt előzőleg telepíteni kell a virtuális gép helyi számítógépére a tanúsítványtárolóban.</span><span class="sxs-lookup"><span data-stu-id="323b1-128">The certificate must be previously deployed to the virtual machine local computer my certificate store.</span></span>

```yaml
Type: String
Parameter Sets: AAD Client Cert Parameters
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="323b1-129">-AadClientID</span><span class="sxs-lookup"><span data-stu-id="323b1-129">-AadClientID</span></span>
<span data-ttu-id="323b1-130">Annak az Azure AD-alkalmazásnak az ügyfél-AZONOSÍTÓját adja meg, amely jogosultságokat **tartalmaz a kulcsok írásához.**</span><span class="sxs-lookup"><span data-stu-id="323b1-130">Specifies the client ID of the Azure AD application that has permissions to write secrets to **KeyVault**.</span></span>

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

### <span data-ttu-id="323b1-131">-AadClientSecret</span><span class="sxs-lookup"><span data-stu-id="323b1-131">-AadClientSecret</span></span>
<span data-ttu-id="323b1-132">Annak az Azure AD-alkalmazásnak az ügyfél titkát adja meg, amely jogosultságokat **tartalmaz a kulcsok írásához.**</span><span class="sxs-lookup"><span data-stu-id="323b1-132">Specifies the client secret of the Azure AD application that has permissions to write secrets to **KeyVault**.</span></span>

```yaml
Type: String
Parameter Sets: AAD Client Secret Parameters
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="323b1-133">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="323b1-133">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="323b1-134">Azt jelzi, hogy ez a parancsmag letiltja a bővítmény alverziójának automatikus frissítését.</span><span class="sxs-lookup"><span data-stu-id="323b1-134">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

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

### <span data-ttu-id="323b1-135">-DiskEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="323b1-135">-DiskEncryptionKeyVaultId</span></span>
<span data-ttu-id="323b1-136">Annak a kulcsnak az erőforrás **-** azonosítóját adja meg, amelybe a virtuálisgép-titkosítási kulcsokat fel szeretné tölteni.</span><span class="sxs-lookup"><span data-stu-id="323b1-136">Specifies the resource ID of the **KeyVault** to which the virtual machine encryption keys should be uploaded.</span></span>

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

### <span data-ttu-id="323b1-137">-DiskEncryptionKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="323b1-137">-DiskEncryptionKeyVaultUrl</span></span>
<span data-ttu-id="323b1-138">Annak a billentyűzetnek **az URL-** címe, amelyhez a virtuális gép titkosítási kulcsait fel kell tölteni.</span><span class="sxs-lookup"><span data-stu-id="323b1-138">Specifies the **KeyVault** URL to which the virtual machine encryption keys should be uploaded.</span></span>

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

### <span data-ttu-id="323b1-139">-Force</span><span class="sxs-lookup"><span data-stu-id="323b1-139">-Force</span></span>
<span data-ttu-id="323b1-140">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="323b1-140">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="323b1-141">-KeyEncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="323b1-141">-KeyEncryptionAlgorithm</span></span>
<span data-ttu-id="323b1-142">A virtuális gép kulcs-titkosítási kulcsának körbefuttatására és kicsomagolására szolgáló algoritmust adja meg.</span><span class="sxs-lookup"><span data-stu-id="323b1-142">Specifies the algorithm that is used to wrap and unwrap the key encryption key of the virtual machine.</span></span>
<span data-ttu-id="323b1-143">Az alapértelmezett érték az RSA-OAEP.</span><span class="sxs-lookup"><span data-stu-id="323b1-143">The default value is RSA-OAEP.</span></span>

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

### <span data-ttu-id="323b1-144">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="323b1-144">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="323b1-145">Annak a kulcs titkosítási kulcsnak az URL-címét adja meg, amely a virtuálisgép-titkosítási kulcs körbefuttatásához és kicsomagolásához használatos.</span><span class="sxs-lookup"><span data-stu-id="323b1-145">Specifies the URL of the key encryption key that is used to wrap and unwrap the virtual machine encryption key.</span></span>
<span data-ttu-id="323b1-146">Ennek a teljes verziójú URL-címnek kell lennie.</span><span class="sxs-lookup"><span data-stu-id="323b1-146">This must be the full versioned URL.</span></span>

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

### <span data-ttu-id="323b1-147">-KeyEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="323b1-147">-KeyEncryptionKeyVaultId</span></span>
<span data-ttu-id="323b1-148">**A virtuálisgép** -titkosítási kulcs körbefuttatását és kicsomagolását tartalmazó kulcs titkosítási kulcsát tartalmazó kulcskezelő erőforrás-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="323b1-148">Specifies the resource ID of the **KeyVault** that contains key encryption key that is used to wrap and unwrap the virtual machine encryption key.</span></span>
<span data-ttu-id="323b1-149">Ennek a teljes verziójú URL-címnek kell lennie.</span><span class="sxs-lookup"><span data-stu-id="323b1-149">This must be a full versioned URL.</span></span>

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

### <span data-ttu-id="323b1-150">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="323b1-150">-Name</span></span>
<span data-ttu-id="323b1-151">A bővítményt jelképező Azure Resource Manager-erőforrás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="323b1-151">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="323b1-152">Az alapértelmezett érték a AzureDiskEncryption, amely a Windows operációs rendszert futtató virtuális gépeket vagy a AzureDiskEncryptionForLinux virtuális gépeket futtatja.</span><span class="sxs-lookup"><span data-stu-id="323b1-152">The default value is AzureDiskEncryption for virtual machines that run the Windows operating system or AzureDiskEncryptionForLinux for Linux virtual machines.</span></span>

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

### <span data-ttu-id="323b1-153">-Jelmondat</span><span class="sxs-lookup"><span data-stu-id="323b1-153">-Passphrase</span></span>
<span data-ttu-id="323b1-154">A Linux virtuális gépek titkosításához használt jelmondatot adja meg.</span><span class="sxs-lookup"><span data-stu-id="323b1-154">Specifies the passphrase used for encrypting Linux virtual machines only.</span></span>
<span data-ttu-id="323b1-155">Ezt a paramétert nem használják a Windows operációs rendszert futtató virtuális gépekhez.</span><span class="sxs-lookup"><span data-stu-id="323b1-155">This parameter is not used for virtual machines that run the Windows operating system.</span></span>

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

### <span data-ttu-id="323b1-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="323b1-156">-ResourceGroupName</span></span>
<span data-ttu-id="323b1-157">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="323b1-157">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="323b1-158">-SequenceVersion</span><span class="sxs-lookup"><span data-stu-id="323b1-158">-SequenceVersion</span></span>
<span data-ttu-id="323b1-159">A virtuális gép titkosítási műveleteinek sorszámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="323b1-159">Specifies the sequence number of the encryption operations for a virtual machine.</span></span>
<span data-ttu-id="323b1-160">Ez a beállítás minden, ugyanazon a virtuális gépen végzett titkosítási műveletnél egyedi.</span><span class="sxs-lookup"><span data-stu-id="323b1-160">This is unique per each encryption operation performed on the same virtual machine.</span></span>
<span data-ttu-id="323b1-161">A Get-AzureRmVMExtension parancsmag használatával lekérdezheti az előző sorszámot.</span><span class="sxs-lookup"><span data-stu-id="323b1-161">The Get-AzureRmVMExtension cmdlet can be used to retrieve the previous sequence number that was used.</span></span>

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

### <span data-ttu-id="323b1-162">-SkipVmBackup</span><span class="sxs-lookup"><span data-stu-id="323b1-162">-SkipVmBackup</span></span>
<span data-ttu-id="323b1-163">A Linux VMs biztonsági másolatának kihagyása</span><span class="sxs-lookup"><span data-stu-id="323b1-163">Skip backup creation for Linux VMs</span></span>

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

### <span data-ttu-id="323b1-164">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="323b1-164">-TypeHandlerVersion</span></span>
<span data-ttu-id="323b1-165">A titkosítási bővítmény verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="323b1-165">Specifies the version of the encryption extension.</span></span>

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

### <span data-ttu-id="323b1-166">-VMName</span><span class="sxs-lookup"><span data-stu-id="323b1-166">-VMName</span></span>
<span data-ttu-id="323b1-167">A virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="323b1-167">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="323b1-168">-VolumeType</span><span class="sxs-lookup"><span data-stu-id="323b1-168">-VolumeType</span></span>
<span data-ttu-id="323b1-169">A titkosítási művelet végrehajtásához használt virtuálisgép-kötetek típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="323b1-169">Specifies the type of virtual machine volumes to perform the encryption operation.</span></span>
<span data-ttu-id="323b1-170">A Windows operációs rendszert futtató virtuális gépek megengedett értékei az alábbiak: mind, operációs rendszer és adatok.</span><span class="sxs-lookup"><span data-stu-id="323b1-170">Allowed values for virtual machines that run the Windows operating system are as follows: All, OS, and Data.</span></span>
<span data-ttu-id="323b1-171">A linuxos virtuális gépek megengedett értékei a következők: csak adatok.</span><span class="sxs-lookup"><span data-stu-id="323b1-171">The allowed values for Linux virtual machines are as follows: Data only.</span></span>

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

### <span data-ttu-id="323b1-172">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="323b1-172">-Confirm</span></span>
<span data-ttu-id="323b1-173">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="323b1-173">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="323b1-174">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="323b1-174">-WhatIf</span></span>
<span data-ttu-id="323b1-175">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="323b1-175">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="323b1-176">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="323b1-176">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="323b1-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="323b1-177">CommonParameters</span></span>
<span data-ttu-id="323b1-178">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="323b1-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="323b1-179">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="323b1-179">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="323b1-180">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="323b1-180">INPUTS</span></span>

### <span data-ttu-id="323b1-181">Nincs</span><span class="sxs-lookup"><span data-stu-id="323b1-181">None</span></span>
<span data-ttu-id="323b1-182">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="323b1-182">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="323b1-183">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="323b1-183">OUTPUTS</span></span>

## <span data-ttu-id="323b1-184">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="323b1-184">NOTES</span></span>

## <span data-ttu-id="323b1-185">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="323b1-185">RELATED LINKS</span></span>

[<span data-ttu-id="323b1-186">Add-AzureRmVMSecret</span><span class="sxs-lookup"><span data-stu-id="323b1-186">Add-AzureRmVMSecret</span></span>](./Add-AzureRmVMSecret.md)

[<span data-ttu-id="323b1-187">Get-AzureRmVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="323b1-187">Get-AzureRmVMDiskEncryptionStatus</span></span>](./Get-AzureRmVMDiskEncryptionStatus.md)

[<span data-ttu-id="323b1-188">Remove-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="323b1-188">Remove-AzureRmVMDiskEncryptionExtension</span></span>](./Remove-AzureRmVMDiskEncryptionExtension.md)


