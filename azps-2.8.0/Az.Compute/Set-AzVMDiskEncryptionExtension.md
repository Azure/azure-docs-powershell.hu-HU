---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 6BCB36BC-F5E6-4EDD-983C-8BDE7A9B004D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmdiskencryptionextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDiskEncryptionExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDiskEncryptionExtension.md
ms.openlocfilehash: 5bd0e525607180659365c81825d6ad6899578fae
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667213"
---
# <span data-ttu-id="ba5fb-101">Set-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="ba5fb-101">Set-AzVMDiskEncryptionExtension</span></span>

## <span data-ttu-id="ba5fb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ba5fb-102">SYNOPSIS</span></span>
<span data-ttu-id="ba5fb-103">Engedélyezi a titkosítást egy futó IaaS virtuális gépen az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="ba5fb-103">Enables encryption on a running IaaS virtual machine in Azure.</span></span>

## <span data-ttu-id="ba5fb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ba5fb-104">SYNTAX</span></span>

### <span data-ttu-id="ba5fb-105">SinglePassParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ba5fb-105">SinglePassParameterSet (Default)</span></span>
```
Set-AzVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String>
 [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String> [[-KeyEncryptionKeyUrl] <String>]
 [[-KeyEncryptionKeyVaultId] <String>] [[-KeyEncryptionAlgorithm] <String>] [[-VolumeType] <String>]
 [[-SequenceVersion] <String>] [[-TypeHandlerVersion] <String>] [[-Name] <String>] [[-Passphrase] <String>]
 [-Force] [-DisableAutoUpgradeMinorVersion] [-SkipVmBackup] [-ExtensionType <String>]
 [-ExtensionPublisherName <String>] [-EncryptFormatAll] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba5fb-106">AADClientSecretParameterSet</span><span class="sxs-lookup"><span data-stu-id="ba5fb-106">AADClientSecretParameterSet</span></span>
```
Set-AzVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [-AadClientID] <String>
 [-AadClientSecret] <String> [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String>
 [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>] [[-KeyEncryptionAlgorithm] <String>]
 [[-VolumeType] <String>] [[-SequenceVersion] <String>] [[-TypeHandlerVersion] <String>] [[-Name] <String>]
 [[-Passphrase] <String>] [-Force] [-DisableAutoUpgradeMinorVersion] [-SkipVmBackup] [-ExtensionType <String>]
 [-ExtensionPublisherName <String>] [-EncryptFormatAll] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba5fb-107">AADClientCertParameterSet</span><span class="sxs-lookup"><span data-stu-id="ba5fb-107">AADClientCertParameterSet</span></span>
```
Set-AzVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [-AadClientID] <String>
 [-AadClientCertThumbprint] <String> [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String>
 [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>] [[-KeyEncryptionAlgorithm] <String>]
 [[-VolumeType] <String>] [[-SequenceVersion] <String>] [[-TypeHandlerVersion] <String>] [[-Name] <String>]
 [[-Passphrase] <String>] [-Force] [-DisableAutoUpgradeMinorVersion] [-SkipVmBackup] [-ExtensionType <String>]
 [-ExtensionPublisherName <String>] [-EncryptFormatAll] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba5fb-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="ba5fb-108">DESCRIPTION</span></span>
<span data-ttu-id="ba5fb-109">A **set-AzVMDiskEncryptionExtension** parancsmag egy futó infrastruktúra titkosítását engedélyezi az Azure rendszer Service (IaaS) virtuális számítógépén.</span><span class="sxs-lookup"><span data-stu-id="ba5fb-109">The **Set-AzVMDiskEncryptionExtension** cmdlet enables encryption on a running infrastructure as a service (IaaS) virtual machine in Azure.</span></span>  <span data-ttu-id="ba5fb-110">A titkosítási funkció a virtuális gép Lemezkezelés bővítményének telepítésével lehetővé teszi a titkosítást.</span><span class="sxs-lookup"><span data-stu-id="ba5fb-110">It enables encryption by installing the disk encryption extension on the virtual machine.</span></span> 

<span data-ttu-id="ba5fb-111">Ehhez a parancsmaghoz a felhasználóknak megerősítést kell engedélyezni a virtuális gép újraindítását igénylik.</span><span class="sxs-lookup"><span data-stu-id="ba5fb-111">This cmdlet requires confirmation from the users as one of the steps to enable encryption requires a restart of the virtual machine.</span></span>

<span data-ttu-id="ba5fb-112">Javasoljuk, hogy a parancsmag futtatása előtt mentse a munkáját a virtuális gépen.</span><span class="sxs-lookup"><span data-stu-id="ba5fb-112">It is advised that you save your work on the virtual machine before you run this cmdlet.</span></span>

<span data-ttu-id="ba5fb-113">Linux: a **VolumeType** paraméter a Linux virtuális gépek titkosításakor szükséges, és a Linux disztribúció által támogatott érték ("operációs rendszer", "Data" vagy "minden") értékre kell állítani.</span><span class="sxs-lookup"><span data-stu-id="ba5fb-113">Linux: The **VolumeType** parameter is required when encrypting Linux virtual machines, and must be set to a value ("Os", "Data", or "All") supported by the Linux distribution.</span></span> 

<span data-ttu-id="ba5fb-114">Windows: a **VolumeType** paraméter kihagyható, ebben az esetben a művelet alapértelmezés szerint az összes; Ha a VolumeType paraméter egy olyan Windows Virtual Machine-géphez van megadva, amelyet az All vagy az OS értékre kell beállítania.</span><span class="sxs-lookup"><span data-stu-id="ba5fb-114">Windows: The **VolumeType** parameter may be omitted, in which case the operation defaults to All; if the VolumeType parameter is present for a Windows virtual machine, it must be set to either All or OS.</span></span>

## <span data-ttu-id="ba5fb-115">Példák</span><span class="sxs-lookup"><span data-stu-id="ba5fb-115">EXAMPLES</span></span>

### <span data-ttu-id="ba5fb-116">1. példa: titkosítás engedélyezése</span><span class="sxs-lookup"><span data-stu-id="ba5fb-116">Example 1: Enable encryption</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"
$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
$VolumeType = "All"
Set-AzVMDiskEncryptionExtension -ResourceGroupName $RGName -VMName $VMName -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId -VolumeType $VolumeType
```

<span data-ttu-id="ba5fb-117">Ez a példa engedélyezi a VM titkosítását az AD-hitelesítő adatok megadása nélkül.</span><span class="sxs-lookup"><span data-stu-id="ba5fb-117">This example enables encryption on a VM without specifying AD credentials.</span></span>

### <span data-ttu-id="ba5fb-118">2. példa: a titkosítás engedélyezése a csővezetékes bemenettel</span><span class="sxs-lookup"><span data-stu-id="ba5fb-118">Example 2: Enable encryption with pipelined input</span></span>
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

<span data-ttu-id="ba5fb-119">Ez a példa a következő módon küldi el a paramétereket a csővezetékes bemenettel a VM-titkosítás engedélyezéséhez, az AD-hitelesítő adatok megadása nélkül.</span><span class="sxs-lookup"><span data-stu-id="ba5fb-119">This example sends parameters using pipelined input to enable encryption on a VM, without specifying AD credentials.</span></span>

### <span data-ttu-id="ba5fb-120">3. példa: a titkosítás engedélyezése az Azure AD Client ID azonosítójával és az ügyfél titkos azonosítójával</span><span class="sxs-lookup"><span data-stu-id="ba5fb-120">Example 3: Enable encryption using Azure AD Client ID and Client Secret</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"
$AADClientID = "<clientID of your Azure AD app>"
$AADClientSecret = "<clientSecret of your Azure AD app>"
$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
$VolumeType = "All"
Set-AzVMDiskEncryptionExtension -ResourceGroupName $RGName -VMName $VMName -AadClientID $AADClientID -AadClientSecret $AADClientSecret -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId -VolumeType $VolumeType
```

<span data-ttu-id="ba5fb-121">Ez a példa az Azure AD Client ID azonosítót és az ügyfél titkát használja a VM titkosításának engedélyezéséhez.</span><span class="sxs-lookup"><span data-stu-id="ba5fb-121">This example uses Azure AD client ID and client secret to enable encryption on a VM.</span></span>

### <span data-ttu-id="ba5fb-122">4. példa: a titkosítás engedélyezése az Azure AD Client ID és az ügyfél tanúsítási ujjlenyomatával</span><span class="sxs-lookup"><span data-stu-id="ba5fb-122">Example 4: Enable encryption using Azure AD client ID and client certification thumbprint</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"
#The KeyVault must have enabledForDiskEncryption property set on it
$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
$VolumeType = "All"

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
Set-AzVMDiskEncryptionExtension -ResourceGroupName $RGName -VMName $VMName -AadClientID $AADClientID -AadClientCertThumbprint $AADClientCertThumbprint -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId -VolumeType $VolumeType
```

<span data-ttu-id="ba5fb-123">Ez a példa az Azure AD Client ID azonosítóját és az ügyfél tanúsítási thumbprints használja a VM titkosításának engedélyezéséhez.</span><span class="sxs-lookup"><span data-stu-id="ba5fb-123">This example uses Azure AD client ID and client certification thumbprints to enable encryption on a VM.</span></span>

### <span data-ttu-id="ba5fb-124">Példa 5: a titkosítás engedélyezése Azure AD Client ID, Client Secret és wrap Disk titkosítási kulccsal a kulcs-titkosítási kulccsal</span><span class="sxs-lookup"><span data-stu-id="ba5fb-124">Example 5: Enable encryption using Azure AD client ID, client secret, and wrap disk encryption key by using key encryption key</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"

$AADClientID = "<clientID of your Azure AD app>"
$AADClientSecret = "<clientSecret of your Azure AD app>"

$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
$VolumeType = "All"

$KEKName = "MyKeyEncryptionKey"
$KEK = Add-AzKeyVaultKey -VaultName $VaultName -Name $KEKName -Destination "Software"
$KeyEncryptionKeyUrl = $KEK.Key.kid

Set-AzVMDiskEncryptionExtension -ResourceGroupName $RGName -VMName $VMName -AadClientID $AADClientID -AadClientSecret $AADClientSecret -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl -KeyEncryptionKeyVaultId $KeyVaultResourceId -VolumeType $VolumeType
```

<span data-ttu-id="ba5fb-125">Ez a példa az Azure AD Client ID azonosítót és az ügyfél titkát használja a VM titkosítási funkciójának engedélyezéséhez, és egy kulcsos titkosítási kulccsal betakarja a lemez titkosítási kulcsát.</span><span class="sxs-lookup"><span data-stu-id="ba5fb-125">This example uses Azure AD client ID and client secret to enable encryption on a VM, and wraps the disk encryption key using a key encryption key.</span></span>

### <span data-ttu-id="ba5fb-126">6. példa: a titkosítás engedélyezése Azure AD Client ID, Client CERT ujjlenyomat és wrap Disk encryptionkey kulccsal a kulcs-titkosítási kulccsal</span><span class="sxs-lookup"><span data-stu-id="ba5fb-126">Example 6: Enable encryption using Azure AD client ID, client cert thumbprint, and wrap disk encryptionkey by using key encryption key</span></span>
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
$VolumeType = "All"

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
Set-AzVMDiskEncryptionExtension -ResourceGroupName $RGname -VMName $VMName -AadClientID $AADClientID -AadClientCertThumbprint $AADClientCertThumbprint -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl -KeyEncryptionKeyVaultId $KeyVaultResourceId -VolumeType $VolumeType
```

<span data-ttu-id="ba5fb-127">Ez a példa az Azure AD Client ID azonosítót és az ügyfél CERT ujjlenyomatát használja a VM titkosítási funkciójának engedélyezéséhez, és egy kulcs titkosítási kulccsal betakarja a lemez titkosítási kulcsát.</span><span class="sxs-lookup"><span data-stu-id="ba5fb-127">This example uses Azure AD client ID and client cert thumbprint to enable encryption on a VM, and wraps the disk encryption key using a key encryption key.</span></span>

## <span data-ttu-id="ba5fb-128">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ba5fb-128">PARAMETERS</span></span>

### <span data-ttu-id="ba5fb-129">-AadClientCertThumbprint</span><span class="sxs-lookup"><span data-stu-id="ba5fb-129">-AadClientCertThumbprint</span></span>
<span data-ttu-id="ba5fb-130">Itt adhatja meg a AzureActive-címtár (Azure AD) ügyfélalkalmazás ujjlenyomatát, amely jogosultságokkal rendelkezik a kulcsok **írásához.**</span><span class="sxs-lookup"><span data-stu-id="ba5fb-130">Specifies the thumbprint of the AzureActive Directory (Azure AD) application client certificate that has permissions to write secrets to **KeyVault**.</span></span>
<span data-ttu-id="ba5fb-131">Előfeltételként az Azure AD ügyfélalkalmazás tanúsítványát előbb telepíteni kell a virtuális gép helyi `my` tanúsítványtárolójában.</span><span class="sxs-lookup"><span data-stu-id="ba5fb-131">As a prerequisite, the Azure AD client certificate must be previously deployed to the virtual machine's local computer `my` certificate store.</span></span>
<span data-ttu-id="ba5fb-132">Az Add-AzVMSecret parancsmag segítségével tanúsítványokat telepíthet egy virtuális gépre az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="ba5fb-132">The Add-AzVMSecret cmdlet can be used to deploy a certificate to a virtual machine in Azure.</span></span>
<span data-ttu-id="ba5fb-133">További információt az **Add-AzVMSecret** parancsmag súgójában talál.</span><span class="sxs-lookup"><span data-stu-id="ba5fb-133">For more details, see the **Add-AzVMSecret** cmdlet help.</span></span>
<span data-ttu-id="ba5fb-134">A tanúsítványt előzőleg telepíteni kell a virtuális gép helyi számítógépére a tanúsítványtárolóban.</span><span class="sxs-lookup"><span data-stu-id="ba5fb-134">The certificate must be previously deployed to the virtual machine local computer my certificate store.</span></span>

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

### <span data-ttu-id="ba5fb-135">-AadClientID</span><span class="sxs-lookup"><span data-stu-id="ba5fb-135">-AadClientID</span></span>
<span data-ttu-id="ba5fb-136">Annak az Azure AD-alkalmazásnak az ügyfél-AZONOSÍTÓját adja meg, amely jogosultságokat **tartalmaz a kulcsok írásához.**</span><span class="sxs-lookup"><span data-stu-id="ba5fb-136">Specifies the client ID of the Azure AD application that has permissions to write secrets to **KeyVault**.</span></span>

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

### <span data-ttu-id="ba5fb-137">-AadClientSecret</span><span class="sxs-lookup"><span data-stu-id="ba5fb-137">-AadClientSecret</span></span>
<span data-ttu-id="ba5fb-138">Annak az Azure AD-alkalmazásnak az ügyfél titkát adja meg, amely jogosultságokat **tartalmaz a kulcsok írásához.**</span><span class="sxs-lookup"><span data-stu-id="ba5fb-138">Specifies the client secret of the Azure AD application that has permissions to write secrets to **KeyVault**.</span></span>

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

### <span data-ttu-id="ba5fb-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba5fb-139">-DefaultProfile</span></span>
<span data-ttu-id="ba5fb-140">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ba5fb-140">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ba5fb-141">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="ba5fb-141">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="ba5fb-142">Azt jelzi, hogy ez a parancsmag letiltja a bővítmény alverziójának automatikus frissítését.</span><span class="sxs-lookup"><span data-stu-id="ba5fb-142">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

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

### <span data-ttu-id="ba5fb-143">-DiskEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="ba5fb-143">-DiskEncryptionKeyVaultId</span></span>
<span data-ttu-id="ba5fb-144">Annak a kulcsnak az erőforrás **-** azonosítóját adja meg, amelybe a virtuálisgép-titkosítási kulcsokat fel szeretné tölteni.</span><span class="sxs-lookup"><span data-stu-id="ba5fb-144">Specifies the resource ID of the **KeyVault** to which the virtual machine encryption keys should be uploaded.</span></span>

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

### <span data-ttu-id="ba5fb-145">-DiskEncryptionKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="ba5fb-145">-DiskEncryptionKeyVaultUrl</span></span>
<span data-ttu-id="ba5fb-146">Annak a billentyűzetnek **az URL-** címe, amelyhez a virtuális gép titkosítási kulcsait fel kell tölteni.</span><span class="sxs-lookup"><span data-stu-id="ba5fb-146">Specifies the **KeyVault** URL to which the virtual machine encryption keys should be uploaded.</span></span>

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

### <span data-ttu-id="ba5fb-147">-EncryptFormatAll</span><span class="sxs-lookup"><span data-stu-id="ba5fb-147">-EncryptFormatAll</span></span>
<span data-ttu-id="ba5fb-148">Az összes olyan adatmeghajtó Encrypt-Format, amely még nincs titkosítva</span><span class="sxs-lookup"><span data-stu-id="ba5fb-148">Encrypt-Format all data drives that are not already encrypted</span></span>

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

### <span data-ttu-id="ba5fb-149">-ExtensionPublisherName</span><span class="sxs-lookup"><span data-stu-id="ba5fb-149">-ExtensionPublisherName</span></span>
<span data-ttu-id="ba5fb-150">A bővítmény közzétevője név.</span><span class="sxs-lookup"><span data-stu-id="ba5fb-150">The extension publisher name.</span></span> <span data-ttu-id="ba5fb-151">Csak akkor adja meg ezt a paramétert, ha a "Microsoft. Azure. Security" alapértelmezett értékét szeretné felülbírálni.</span><span class="sxs-lookup"><span data-stu-id="ba5fb-151">Specify this parameter only to override the default value of "Microsoft.Azure.Security".</span></span>

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

### <span data-ttu-id="ba5fb-152">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="ba5fb-152">-ExtensionType</span></span>
<span data-ttu-id="ba5fb-153">A bővítmény típusa.</span><span class="sxs-lookup"><span data-stu-id="ba5fb-153">The extension type.</span></span> <span data-ttu-id="ba5fb-154">Adja meg ezt a paramétert, ha a Windows VMs "AzureDiskEncryption" alapértelmezett értékét szeretné felülbírálni, és a Linux VMs esetében a "AzureDiskEncryptionForLinux".</span><span class="sxs-lookup"><span data-stu-id="ba5fb-154">Specify this parameter to override its default value of "AzureDiskEncryption" for Windows VMs and "AzureDiskEncryptionForLinux" for Linux VMs.</span></span>

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

### <span data-ttu-id="ba5fb-155">-Force</span><span class="sxs-lookup"><span data-stu-id="ba5fb-155">-Force</span></span>
<span data-ttu-id="ba5fb-156">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="ba5fb-156">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ba5fb-157">-KeyEncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="ba5fb-157">-KeyEncryptionAlgorithm</span></span>
<span data-ttu-id="ba5fb-158">A virtuális gép kulcs-titkosítási kulcsának körbefuttatására és kicsomagolására szolgáló algoritmust adja meg.</span><span class="sxs-lookup"><span data-stu-id="ba5fb-158">Specifies the algorithm that is used to wrap and unwrap the key encryption key of the virtual machine.</span></span>
<span data-ttu-id="ba5fb-159">Az alapértelmezett érték az RSA-OAEP.</span><span class="sxs-lookup"><span data-stu-id="ba5fb-159">The default value is RSA-OAEP.</span></span>

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

### <span data-ttu-id="ba5fb-160">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="ba5fb-160">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="ba5fb-161">Annak a kulcs titkosítási kulcsnak az URL-címét adja meg, amely a virtuálisgép-titkosítási kulcs körbefuttatásához és kicsomagolásához használatos.</span><span class="sxs-lookup"><span data-stu-id="ba5fb-161">Specifies the URL of the key encryption key that is used to wrap and unwrap the virtual machine encryption key.</span></span>
<span data-ttu-id="ba5fb-162">Ennek a teljes verziójú URL-címnek kell lennie.</span><span class="sxs-lookup"><span data-stu-id="ba5fb-162">This must be the full versioned URL.</span></span>

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

### <span data-ttu-id="ba5fb-163">-KeyEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="ba5fb-163">-KeyEncryptionKeyVaultId</span></span>
<span data-ttu-id="ba5fb-164">**A virtuálisgép** -titkosítási kulcs körbefuttatását és kicsomagolását tartalmazó kulcs titkosítási kulcsát tartalmazó kulcskezelő erőforrás-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="ba5fb-164">Specifies the resource ID of the **KeyVault** that contains key encryption key that is used to wrap and unwrap the virtual machine encryption key.</span></span>
<span data-ttu-id="ba5fb-165">Ennek a teljes verziójú URL-címnek kell lennie.</span><span class="sxs-lookup"><span data-stu-id="ba5fb-165">This must be a full versioned URL.</span></span>

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

### <span data-ttu-id="ba5fb-166">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ba5fb-166">-Name</span></span>
<span data-ttu-id="ba5fb-167">A bővítményt jelképező Azure Resource Manager-erőforrás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ba5fb-167">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span> <span data-ttu-id="ba5fb-168">Ha a *Name* paraméter nincs megadva, a telepített bővítmény neve AzureDiskEncryption lesz a Windows virtuális gépeken és a AzureDiskEncryptionForLinux a Linux virtuális gépeken.</span><span class="sxs-lookup"><span data-stu-id="ba5fb-168">If the *Name* parameter is omitted, the installed extension will be named AzureDiskEncryption on Windows virtual machines and AzureDiskEncryptionForLinux on Linux virtual machines.</span></span>


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

### <span data-ttu-id="ba5fb-169">-Jelmondat</span><span class="sxs-lookup"><span data-stu-id="ba5fb-169">-Passphrase</span></span>
<span data-ttu-id="ba5fb-170">A Linux virtuális gépek titkosításához használt jelmondatot adja meg.</span><span class="sxs-lookup"><span data-stu-id="ba5fb-170">Specifies the passphrase used for encrypting Linux virtual machines only.</span></span>
<span data-ttu-id="ba5fb-171">Ezt a paramétert nem használják a Windows operációs rendszert futtató virtuális gépekhez.</span><span class="sxs-lookup"><span data-stu-id="ba5fb-171">This parameter is not used for virtual machines that run the Windows operating system.</span></span>

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

### <span data-ttu-id="ba5fb-172">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba5fb-172">-ResourceGroupName</span></span>
<span data-ttu-id="ba5fb-173">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ba5fb-173">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="ba5fb-174">-SequenceVersion</span><span class="sxs-lookup"><span data-stu-id="ba5fb-174">-SequenceVersion</span></span>
<span data-ttu-id="ba5fb-175">A virtuális gép titkosítási műveleteinek sorszámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="ba5fb-175">Specifies the sequence number of the encryption operations for a virtual machine.</span></span>
<span data-ttu-id="ba5fb-176">Ez a beállítás minden, ugyanazon a virtuális gépen végzett titkosítási műveletnél egyedi.</span><span class="sxs-lookup"><span data-stu-id="ba5fb-176">This is unique per each encryption operation performed on the same virtual machine.</span></span>
<span data-ttu-id="ba5fb-177">A Get-AzVMExtension parancsmag használatával lekérdezheti az előző sorszámot.</span><span class="sxs-lookup"><span data-stu-id="ba5fb-177">The Get-AzVMExtension cmdlet can be used to retrieve the previous sequence number that was used.</span></span>

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

### <span data-ttu-id="ba5fb-178">-SkipVmBackup</span><span class="sxs-lookup"><span data-stu-id="ba5fb-178">-SkipVmBackup</span></span>
<span data-ttu-id="ba5fb-179">A Linux VMs biztonsági másolatának kihagyása</span><span class="sxs-lookup"><span data-stu-id="ba5fb-179">Skip backup creation for Linux VMs</span></span>

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

### <span data-ttu-id="ba5fb-180">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="ba5fb-180">-TypeHandlerVersion</span></span>
<span data-ttu-id="ba5fb-181">A titkosítási bővítmény verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="ba5fb-181">Specifies the version of the encryption extension.</span></span>

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

### <span data-ttu-id="ba5fb-182">-VMName</span><span class="sxs-lookup"><span data-stu-id="ba5fb-182">-VMName</span></span>
<span data-ttu-id="ba5fb-183">A virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ba5fb-183">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="ba5fb-184">-VolumeType</span><span class="sxs-lookup"><span data-stu-id="ba5fb-184">-VolumeType</span></span>
<span data-ttu-id="ba5fb-185">Annak a virtuálisgép-köteteknek a típusát adja meg, amelyeken titkosítási műveletet kell végrehajtani: operációs rendszer, adat vagy mind.</span><span class="sxs-lookup"><span data-stu-id="ba5fb-185">Specifies the type of virtual machine volumes on which to perform encryption operation: OS, Data, or All.</span></span> 

<span data-ttu-id="ba5fb-186">Linux: a **VolumeType** paraméter a Linux virtuális gépek titkosításakor szükséges, és a Linux disztribúció által támogatott érték ("operációs rendszer", "Data" vagy "minden") értékre kell állítani.</span><span class="sxs-lookup"><span data-stu-id="ba5fb-186">Linux: The **VolumeType** parameter is required when encrypting Linux virtual machines, and must be set to a value ("Os", "Data", or "All") supported by the Linux distribution.</span></span> 

<span data-ttu-id="ba5fb-187">Windows: a **VolumeType** paraméter kihagyható, ebben az esetben a művelet alapértelmezés szerint az összes; Ha a VolumeType paraméter egy olyan Windows Virtual Machine-géphez van megadva, amelyet az All vagy az OS értékre kell beállítania.</span><span class="sxs-lookup"><span data-stu-id="ba5fb-187">Windows: The **VolumeType** parameter may be omitted, in which case the operation defaults to All; if the VolumeType parameter is present for a Windows virtual machine, it must be set to either All or OS.</span></span>

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

### <span data-ttu-id="ba5fb-188">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ba5fb-188">-Confirm</span></span>
<span data-ttu-id="ba5fb-189">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ba5fb-189">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba5fb-190">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba5fb-190">-WhatIf</span></span>
<span data-ttu-id="ba5fb-191">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ba5fb-191">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba5fb-192">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ba5fb-192">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba5fb-193">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba5fb-193">CommonParameters</span></span>
<span data-ttu-id="ba5fb-194">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ba5fb-194">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba5fb-195">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ba5fb-195">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba5fb-196">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ba5fb-196">INPUTS</span></span>

### <span data-ttu-id="ba5fb-197">System. String</span><span class="sxs-lookup"><span data-stu-id="ba5fb-197">System.String</span></span>

### <span data-ttu-id="ba5fb-198">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ba5fb-198">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="ba5fb-199">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ba5fb-199">OUTPUTS</span></span>

### <span data-ttu-id="ba5fb-200">Microsoft. Azure. commands. kiszámítás. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="ba5fb-200">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="ba5fb-201">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ba5fb-201">NOTES</span></span>

## <span data-ttu-id="ba5fb-202">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ba5fb-202">RELATED LINKS</span></span>

[<span data-ttu-id="ba5fb-203">Add-AzVMSecret</span><span class="sxs-lookup"><span data-stu-id="ba5fb-203">Add-AzVMSecret</span></span>](./Add-AzVMSecret.md)

[<span data-ttu-id="ba5fb-204">Get-AzVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="ba5fb-204">Get-AzVMDiskEncryptionStatus</span></span>](./Get-AzVMDiskEncryptionStatus.md)

[<span data-ttu-id="ba5fb-205">Remove-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="ba5fb-205">Remove-AzVMDiskEncryptionExtension</span></span>](./Remove-AzVMDiskEncryptionExtension.md)


