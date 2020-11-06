---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 6BCB36BC-F5E6-4EDD-983C-8BDE7A9B004D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMDiskEncryptionExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMDiskEncryptionExtension.md
ms.openlocfilehash: c10b55ae0d1243320171d898058947d4781a7de1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492505"
---
# <span data-ttu-id="7f54a-101">Set-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="7f54a-101">Set-AzureRmVMDiskEncryptionExtension</span></span>

## <span data-ttu-id="7f54a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7f54a-102">SYNOPSIS</span></span>
<span data-ttu-id="7f54a-103">Engedélyezi a titkosítást egy futó IaaS virtuális gépen az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="7f54a-103">Enables encryption on a running IaaS virtual machine in Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7f54a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7f54a-104">SYNTAX</span></span>

### <span data-ttu-id="7f54a-105">AAD-ügyfél titkos paraméterei (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7f54a-105">AAD Client Secret Parameters (Default)</span></span>
```
Set-AzureRmVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [-AadClientID] <String>
 [-AadClientSecret] <String> [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String>
 [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>] [[-KeyEncryptionAlgorithm] <String>]
 [[-VolumeType] <String>] [[-SequenceVersion] <String>] [[-TypeHandlerVersion] <String>] [[-Name] <String>]
 [[-Passphrase] <String>] [-Force] [-DisableAutoUpgradeMinorVersion] [-SkipVmBackup]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f54a-106">AAD ügyfél CERT-paraméterei</span><span class="sxs-lookup"><span data-stu-id="7f54a-106">AAD Client Cert Parameters</span></span>
```
Set-AzureRmVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [-AadClientID] <String>
 [-AadClientCertThumbprint] <String> [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String>
 [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>] [[-KeyEncryptionAlgorithm] <String>]
 [[-VolumeType] <String>] [[-SequenceVersion] <String>] [[-TypeHandlerVersion] <String>] [[-Name] <String>]
 [[-Passphrase] <String>] [-Force] [-DisableAutoUpgradeMinorVersion] [-SkipVmBackup]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f54a-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="7f54a-107">DESCRIPTION</span></span>
<span data-ttu-id="7f54a-108">A **set-AzureRmVMDiskEncryptionExtension** parancsmag egy futó infrastruktúra titkosítását engedélyezi az Azure rendszer Service (IaaS) virtuális számítógépén.</span><span class="sxs-lookup"><span data-stu-id="7f54a-108">The **Set-AzureRmVMDiskEncryptionExtension** cmdlet enables encryption on a running infrastructure as a service (IaaS) virtual machine in Azure.</span></span>
<span data-ttu-id="7f54a-109">Ez a parancsmag lehetővé teszi a titkosítást, ha telepíti a merevlemez-titkosítási bővítményt a virtuális gépen.</span><span class="sxs-lookup"><span data-stu-id="7f54a-109">This cmdlet enables encryption by installing the disk encryption extension on the virtual machine.</span></span>
<span data-ttu-id="7f54a-110">Ha nincs megadva *név* paraméter, akkor a program a Windows operációs rendszert futtató virtuális gépekhez használt alapértelmezett név AzureDiskEncryption, illetve a AzureDiskEncryptionForLinux virtuális gépekhez telepített virtuális gépekhez bővítményt tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="7f54a-110">If no *Name* parameter is specified, an extension with the default name AzureDiskEncryption for virtual machines that run the Windows operating system or AzureDiskEncryptionForLinux for Linux virtual machines are installed.</span></span>
<span data-ttu-id="7f54a-111">Ehhez a parancsmaghoz a felhasználóknak megerősítést kell engedélyezni a virtuális gép újraindítását igénylik.</span><span class="sxs-lookup"><span data-stu-id="7f54a-111">This cmdlet requires confirmation from the users as one of the steps to enable encryption requires a restart of the virtual machine.</span></span>
<span data-ttu-id="7f54a-112">Javasoljuk, hogy a parancsmag futtatása előtt mentse a munkáját a virtuális gépen.</span><span class="sxs-lookup"><span data-stu-id="7f54a-112">It is advised that you save your work on the virtual machine before you run this cmdlet.</span></span>

## <span data-ttu-id="7f54a-113">Példák</span><span class="sxs-lookup"><span data-stu-id="7f54a-113">EXAMPLES</span></span>

### <span data-ttu-id="7f54a-114">1. példa: a titkosítás engedélyezése az Azure AD Client ID azonosítójával és az ügyfél titkos azonosítójával</span><span class="sxs-lookup"><span data-stu-id="7f54a-114">Example 1: Enable encryption using Azure AD Client ID and Client Secret</span></span>
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

<span data-ttu-id="7f54a-115">Ez a példa engedélyezi az Azure AD Client ID és az ügyfél titkos verziójának titkosítását.</span><span class="sxs-lookup"><span data-stu-id="7f54a-115">This example enables encryption using Azure AD client ID, and client secret.</span></span>

### <span data-ttu-id="7f54a-116">2. példa: a titkosítás engedélyezése az Azure AD Client ID és az ügyfél tanúsítási ujjlenyomatával</span><span class="sxs-lookup"><span data-stu-id="7f54a-116">Example 2: Enable encryption using Azure AD client ID and client certification thumbprint</span></span>
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

<span data-ttu-id="7f54a-117">Ez a példa engedélyezi az Azure AD Client ID és az ügyfél tanúsítási thumbprints való titkosítást.</span><span class="sxs-lookup"><span data-stu-id="7f54a-117">This example enables encryption using Azure AD client ID and client certification thumbprints.</span></span>

### <span data-ttu-id="7f54a-118">3. példa: a titkosítás engedélyezése Azure AD Client ID, Client Secret és wrap Disk titkosítási kulccsal a kulcs titkosítási kulccsal</span><span class="sxs-lookup"><span data-stu-id="7f54a-118">Example 3: Enable encryption using Azure AD client ID, client secret, and wrap disk encryption key by using key encryption key</span></span>
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

<span data-ttu-id="7f54a-119">Ez a példa az Azure AD Client ID, az Client Secret és a wrap Disk titkosítási kulccsal titkosítja a titkosítást a kulcs titkosítási kulcs használatával.</span><span class="sxs-lookup"><span data-stu-id="7f54a-119">This example enables encryption using Azure AD client ID, client secret, and wrap disk encryption key by using the key encryption key.</span></span>

### <span data-ttu-id="7f54a-120">4. példa: a titkosítás engedélyezése Azure AD Client ID, Client CERT ujjlenyomat és wrap Disk encryptionkey kulccsal a kulcs-titkosítási kulccsal</span><span class="sxs-lookup"><span data-stu-id="7f54a-120">Example 4: Enable encryption using Azure AD client ID, client cert thumbprint, and wrap disk encryptionkey by using key encryption key</span></span>
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

<span data-ttu-id="7f54a-121">Ez a példa lehetővé teszi a titkosítást az Azure AD Client ID, az ügyfél CERT ujjlenyomat és a wrap Disk titkosítási kulccsal a kulcs titkosítási kulccsal.</span><span class="sxs-lookup"><span data-stu-id="7f54a-121">This example enables encryption using Azure AD client ID, client cert thumbprint, and wrap disk encryption key by using key encryption key.</span></span>

## <span data-ttu-id="7f54a-122">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7f54a-122">PARAMETERS</span></span>

### <span data-ttu-id="7f54a-123">-AadClientCertThumbprint</span><span class="sxs-lookup"><span data-stu-id="7f54a-123">-AadClientCertThumbprint</span></span>
<span data-ttu-id="7f54a-124">Itt adhatja meg a AzureActive-címtár (Azure AD) ügyfélalkalmazás ujjlenyomatát, amely jogosultságokkal rendelkezik a kulcsok **írásához.**</span><span class="sxs-lookup"><span data-stu-id="7f54a-124">Specifies the thumbprint of the AzureActive Directory (Azure AD) application client certificate that has permissions to write secrets to **KeyVault**.</span></span>
<span data-ttu-id="7f54a-125">Előfeltételként az Azure AD ügyfélalkalmazás tanúsítványát előbb telepíteni kell a virtuális gép helyi `my` tanúsítványtárolójában.</span><span class="sxs-lookup"><span data-stu-id="7f54a-125">As a prerequisite, the Azure AD client certificate must be previously deployed to the virtual machine's local computer `my` certificate store.</span></span>
<span data-ttu-id="7f54a-126">Az Add-AzureRmVMSecret parancsmag segítségével tanúsítványokat telepíthet egy virtuális gépre az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="7f54a-126">The Add-AzureRmVMSecret cmdlet can be used to deploy a certificate to a virtual machine in Azure.</span></span>
<span data-ttu-id="7f54a-127">További információt az **Add-AzureRmVMSecret** parancsmag súgójában talál.</span><span class="sxs-lookup"><span data-stu-id="7f54a-127">For more details, see the **Add-AzureRmVMSecret** cmdlet help.</span></span>
<span data-ttu-id="7f54a-128">A tanúsítványt előzőleg telepíteni kell a virtuális gép helyi számítógépére a tanúsítványtárolóban.</span><span class="sxs-lookup"><span data-stu-id="7f54a-128">The certificate must be previously deployed to the virtual machine local computer my certificate store.</span></span>

```yaml
Type: System.String
Parameter Sets: AAD Client Cert Parameters
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f54a-129">-AadClientID</span><span class="sxs-lookup"><span data-stu-id="7f54a-129">-AadClientID</span></span>
<span data-ttu-id="7f54a-130">Annak az Azure AD-alkalmazásnak az ügyfél-AZONOSÍTÓját adja meg, amely jogosultságokat **tartalmaz a kulcsok írásához.**</span><span class="sxs-lookup"><span data-stu-id="7f54a-130">Specifies the client ID of the Azure AD application that has permissions to write secrets to **KeyVault**.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f54a-131">-AadClientSecret</span><span class="sxs-lookup"><span data-stu-id="7f54a-131">-AadClientSecret</span></span>
<span data-ttu-id="7f54a-132">Annak az Azure AD-alkalmazásnak az ügyfél titkát adja meg, amely jogosultságokat **tartalmaz a kulcsok írásához.**</span><span class="sxs-lookup"><span data-stu-id="7f54a-132">Specifies the client secret of the Azure AD application that has permissions to write secrets to **KeyVault**.</span></span>

```yaml
Type: System.String
Parameter Sets: AAD Client Secret Parameters
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f54a-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f54a-133">-DefaultProfile</span></span>
<span data-ttu-id="7f54a-134">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7f54a-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7f54a-135">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="7f54a-135">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="7f54a-136">Azt jelzi, hogy ez a parancsmag letiltja a bővítmény alverziójának automatikus frissítését.</span><span class="sxs-lookup"><span data-stu-id="7f54a-136">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

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

### <span data-ttu-id="7f54a-137">-DiskEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="7f54a-137">-DiskEncryptionKeyVaultId</span></span>
<span data-ttu-id="7f54a-138">Annak a kulcsnak az erőforrás **-** azonosítóját adja meg, amelybe a virtuálisgép-titkosítási kulcsokat fel szeretné tölteni.</span><span class="sxs-lookup"><span data-stu-id="7f54a-138">Specifies the resource ID of the **KeyVault** to which the virtual machine encryption keys should be uploaded.</span></span>

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

### <span data-ttu-id="7f54a-139">-DiskEncryptionKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="7f54a-139">-DiskEncryptionKeyVaultUrl</span></span>
<span data-ttu-id="7f54a-140">Annak a billentyűzetnek **az URL-** címe, amelyhez a virtuális gép titkosítási kulcsait fel kell tölteni.</span><span class="sxs-lookup"><span data-stu-id="7f54a-140">Specifies the **KeyVault** URL to which the virtual machine encryption keys should be uploaded.</span></span>

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

### <span data-ttu-id="7f54a-141">-Force</span><span class="sxs-lookup"><span data-stu-id="7f54a-141">-Force</span></span>
<span data-ttu-id="7f54a-142">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="7f54a-142">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7f54a-143">-KeyEncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="7f54a-143">-KeyEncryptionAlgorithm</span></span>
<span data-ttu-id="7f54a-144">A virtuális gép kulcs-titkosítási kulcsának körbefuttatására és kicsomagolására szolgáló algoritmust adja meg.</span><span class="sxs-lookup"><span data-stu-id="7f54a-144">Specifies the algorithm that is used to wrap and unwrap the key encryption key of the virtual machine.</span></span>
<span data-ttu-id="7f54a-145">Az alapértelmezett érték az RSA-OAEP.</span><span class="sxs-lookup"><span data-stu-id="7f54a-145">The default value is RSA-OAEP.</span></span>

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

### <span data-ttu-id="7f54a-146">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="7f54a-146">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="7f54a-147">Annak a kulcs titkosítási kulcsnak az URL-címét adja meg, amely a virtuálisgép-titkosítási kulcs körbefuttatásához és kicsomagolásához használatos.</span><span class="sxs-lookup"><span data-stu-id="7f54a-147">Specifies the URL of the key encryption key that is used to wrap and unwrap the virtual machine encryption key.</span></span>
<span data-ttu-id="7f54a-148">Ennek a teljes verziójú URL-címnek kell lennie.</span><span class="sxs-lookup"><span data-stu-id="7f54a-148">This must be the full versioned URL.</span></span>

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

### <span data-ttu-id="7f54a-149">-KeyEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="7f54a-149">-KeyEncryptionKeyVaultId</span></span>
<span data-ttu-id="7f54a-150">**A virtuálisgép** -titkosítási kulcs körbefuttatását és kicsomagolását tartalmazó kulcs titkosítási kulcsát tartalmazó kulcskezelő erőforrás-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="7f54a-150">Specifies the resource ID of the **KeyVault** that contains key encryption key that is used to wrap and unwrap the virtual machine encryption key.</span></span>
<span data-ttu-id="7f54a-151">Ennek a teljes verziójú URL-címnek kell lennie.</span><span class="sxs-lookup"><span data-stu-id="7f54a-151">This must be a full versioned URL.</span></span>

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

### <span data-ttu-id="7f54a-152">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7f54a-152">-Name</span></span>
<span data-ttu-id="7f54a-153">A bővítményt jelképező Azure Resource Manager-erőforrás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7f54a-153">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="7f54a-154">Az alapértelmezett érték a AzureDiskEncryption, amely a Windows operációs rendszert futtató virtuális gépeket vagy a AzureDiskEncryptionForLinux virtuális gépeket futtatja.</span><span class="sxs-lookup"><span data-stu-id="7f54a-154">The default value is AzureDiskEncryption for virtual machines that run the Windows operating system or AzureDiskEncryptionForLinux for Linux virtual machines.</span></span>

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

### <span data-ttu-id="7f54a-155">-Jelmondat</span><span class="sxs-lookup"><span data-stu-id="7f54a-155">-Passphrase</span></span>
<span data-ttu-id="7f54a-156">A Linux virtuális gépek titkosításához használt jelmondatot adja meg.</span><span class="sxs-lookup"><span data-stu-id="7f54a-156">Specifies the passphrase used for encrypting Linux virtual machines only.</span></span>
<span data-ttu-id="7f54a-157">Ezt a paramétert nem használják a Windows operációs rendszert futtató virtuális gépekhez.</span><span class="sxs-lookup"><span data-stu-id="7f54a-157">This parameter is not used for virtual machines that run the Windows operating system.</span></span>

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

### <span data-ttu-id="7f54a-158">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f54a-158">-ResourceGroupName</span></span>
<span data-ttu-id="7f54a-159">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7f54a-159">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="7f54a-160">-SequenceVersion</span><span class="sxs-lookup"><span data-stu-id="7f54a-160">-SequenceVersion</span></span>
<span data-ttu-id="7f54a-161">A virtuális gép titkosítási műveleteinek sorszámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="7f54a-161">Specifies the sequence number of the encryption operations for a virtual machine.</span></span>
<span data-ttu-id="7f54a-162">Ez a beállítás minden, ugyanazon a virtuális gépen végzett titkosítási műveletnél egyedi.</span><span class="sxs-lookup"><span data-stu-id="7f54a-162">This is unique per each encryption operation performed on the same virtual machine.</span></span>
<span data-ttu-id="7f54a-163">A Get-AzureRmVMExtension parancsmag használatával lekérdezheti az előző sorszámot.</span><span class="sxs-lookup"><span data-stu-id="7f54a-163">The Get-AzureRmVMExtension cmdlet can be used to retrieve the previous sequence number that was used.</span></span>

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

### <span data-ttu-id="7f54a-164">-SkipVmBackup</span><span class="sxs-lookup"><span data-stu-id="7f54a-164">-SkipVmBackup</span></span>
<span data-ttu-id="7f54a-165">A Linux VMs biztonsági másolatának kihagyása</span><span class="sxs-lookup"><span data-stu-id="7f54a-165">Skip backup creation for Linux VMs</span></span>

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

### <span data-ttu-id="7f54a-166">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="7f54a-166">-TypeHandlerVersion</span></span>
<span data-ttu-id="7f54a-167">A titkosítási bővítmény verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="7f54a-167">Specifies the version of the encryption extension.</span></span>

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

### <span data-ttu-id="7f54a-168">-VMName</span><span class="sxs-lookup"><span data-stu-id="7f54a-168">-VMName</span></span>
<span data-ttu-id="7f54a-169">A virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7f54a-169">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="7f54a-170">-VolumeType</span><span class="sxs-lookup"><span data-stu-id="7f54a-170">-VolumeType</span></span>
<span data-ttu-id="7f54a-171">A titkosítási művelet végrehajtásához használt virtuálisgép-kötetek típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="7f54a-171">Specifies the type of virtual machine volumes to perform the encryption operation.</span></span>
<span data-ttu-id="7f54a-172">A Windows operációs rendszert futtató virtuális gépek megengedett értékei az alábbiak: mind, operációs rendszer és adatok.</span><span class="sxs-lookup"><span data-stu-id="7f54a-172">Allowed values for virtual machines that run the Windows operating system are as follows: All, OS, and Data.</span></span>
<span data-ttu-id="7f54a-173">A linuxos virtuális gépek megengedett értékei a következők: csak adatok.</span><span class="sxs-lookup"><span data-stu-id="7f54a-173">The allowed values for Linux virtual machines are as follows: Data only.</span></span>

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

### <span data-ttu-id="7f54a-174">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7f54a-174">-Confirm</span></span>
<span data-ttu-id="7f54a-175">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7f54a-175">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f54a-176">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f54a-176">-WhatIf</span></span>
<span data-ttu-id="7f54a-177">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7f54a-177">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="7f54a-178">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7f54a-178">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f54a-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f54a-179">CommonParameters</span></span>
<span data-ttu-id="7f54a-180">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7f54a-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f54a-181">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f54a-181">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f54a-182">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7f54a-182">INPUTS</span></span>

## <span data-ttu-id="7f54a-183">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7f54a-183">OUTPUTS</span></span>

## <span data-ttu-id="7f54a-184">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7f54a-184">NOTES</span></span>

## <span data-ttu-id="7f54a-185">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7f54a-185">RELATED LINKS</span></span>

[<span data-ttu-id="7f54a-186">Add-AzureRmVMSecret</span><span class="sxs-lookup"><span data-stu-id="7f54a-186">Add-AzureRmVMSecret</span></span>](./Add-AzureRmVMSecret.md)

[<span data-ttu-id="7f54a-187">Get-AzureRmVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="7f54a-187">Get-AzureRmVMDiskEncryptionStatus</span></span>](./Get-AzureRmVMDiskEncryptionStatus.md)

[<span data-ttu-id="7f54a-188">Remove-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="7f54a-188">Remove-AzureRmVMDiskEncryptionExtension</span></span>](./Remove-AzureRmVMDiskEncryptionExtension.md)


