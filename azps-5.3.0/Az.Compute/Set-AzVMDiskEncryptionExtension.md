---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 6BCB36BC-F5E6-4EDD-983C-8BDE7A9B004D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmdiskencryptionextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDiskEncryptionExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDiskEncryptionExtension.md
ms.openlocfilehash: 1c69d79e148eae92307855ecfe308f5208a2f455
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480698"
---
# <span data-ttu-id="e3320-101">Set-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="e3320-101">Set-AzVMDiskEncryptionExtension</span></span>

## <span data-ttu-id="e3320-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3320-102">SYNOPSIS</span></span>
<span data-ttu-id="e3320-103">Lehetővé teszi a titkosítást egy futó IaaS virtuális gépen az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="e3320-103">Enables encryption on a running IaaS virtual machine in Azure.</span></span>

## <span data-ttu-id="e3320-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e3320-104">SYNTAX</span></span>

### <span data-ttu-id="e3320-105">SinglePassParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e3320-105">SinglePassParameterSet (Default)</span></span>
```
Set-AzVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String>
 [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String> [[-KeyEncryptionKeyUrl] <String>]
 [[-KeyEncryptionKeyVaultId] <String>] [[-KeyEncryptionAlgorithm] <String>] [[-VolumeType] <String>]
 [[-SequenceVersion] <String>] [[-TypeHandlerVersion] <String>] [[-Name] <String>] [[-Passphrase] <String>]
 [-Force] [-DisableAutoUpgradeMinorVersion] [-SkipVmBackup] [-ExtensionType <String>]
 [-ExtensionPublisherName <String>] [-EncryptFormatAll] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3320-106">AADClientSecretParameterSet</span><span class="sxs-lookup"><span data-stu-id="e3320-106">AADClientSecretParameterSet</span></span>
```
Set-AzVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [-AadClientID] <String>
 [-AadClientSecret] <String> [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String>
 [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>] [[-KeyEncryptionAlgorithm] <String>]
 [[-VolumeType] <String>] [[-SequenceVersion] <String>] [[-TypeHandlerVersion] <String>] [[-Name] <String>]
 [[-Passphrase] <String>] [-Force] [-DisableAutoUpgradeMinorVersion] [-SkipVmBackup] [-ExtensionType <String>]
 [-ExtensionPublisherName <String>] [-EncryptFormatAll] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3320-107">AADClientCertParameterSet</span><span class="sxs-lookup"><span data-stu-id="e3320-107">AADClientCertParameterSet</span></span>
```
Set-AzVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [-AadClientID] <String>
 [-AadClientCertThumbprint] <String> [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String>
 [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>] [[-KeyEncryptionAlgorithm] <String>]
 [[-VolumeType] <String>] [[-SequenceVersion] <String>] [[-TypeHandlerVersion] <String>] [[-Name] <String>]
 [[-Passphrase] <String>] [-Force] [-DisableAutoUpgradeMinorVersion] [-SkipVmBackup] [-ExtensionType <String>]
 [-ExtensionPublisherName <String>] [-EncryptFormatAll] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3320-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e3320-108">DESCRIPTION</span></span>
<span data-ttu-id="e3320-109">A **Set-AzVMDiskEncryptionExtension parancsmag** lehetővé teszi a titkosítást a futó infrastruktúra szolgáltatásként (IaaS) virtuális gépén az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="e3320-109">The **Set-AzVMDiskEncryptionExtension** cmdlet enables encryption on a running infrastructure as a service (IaaS) virtual machine in Azure.</span></span>  <span data-ttu-id="e3320-110">A titkosítást úgy teszi lehetővé, hogy telepíti a lemeztitkosítási bővítményt a virtuális gépre.</span><span class="sxs-lookup"><span data-stu-id="e3320-110">It enables encryption by installing the disk encryption extension on the virtual machine.</span></span> 

<span data-ttu-id="e3320-111">Ez a parancsmag a felhasználóktól megerősítést igényel, mivel a titkosítás engedélyezésének egyik lépése a virtuális gép újraindítását igényli.</span><span class="sxs-lookup"><span data-stu-id="e3320-111">This cmdlet requires confirmation from the users as one of the steps to enable encryption requires a restart of the virtual machine.</span></span>

<span data-ttu-id="e3320-112">A parancsmag futtatása előtt javasoljuk, hogy mentse a munkáját a virtuális gépre.</span><span class="sxs-lookup"><span data-stu-id="e3320-112">It is advised that you save your work on the virtual machine before you run this cmdlet.</span></span>

<span data-ttu-id="e3320-113">Linux: A **VolumeType** paraméterre linuxos virtuális gépek titkosíthatók, és a Linux-terjesztés által támogatott értékre ("Os", "Data" vagy "All") kell állítani.</span><span class="sxs-lookup"><span data-stu-id="e3320-113">Linux: The **VolumeType** parameter is required when encrypting Linux virtual machines, and must be set to a value ("Os", "Data", or "All") supported by the Linux distribution.</span></span> 

<span data-ttu-id="e3320-114">Windows: A **VolumeType** paraméter elhagyható, ebben az esetben a művelet alapértelmezés szerint Az összes; ha a VolumeType paraméter egy windowsos virtuális géphez tartozik, akkor vagy Az összes, vagy az operációs rendszer paramétert kell beállítania.</span><span class="sxs-lookup"><span data-stu-id="e3320-114">Windows: The **VolumeType** parameter may be omitted, in which case the operation defaults to All; if the VolumeType parameter is present for a Windows virtual machine, it must be set to either All or OS.</span></span>

## <span data-ttu-id="e3320-115">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e3320-115">EXAMPLES</span></span>

### <span data-ttu-id="e3320-116">1. példa: Titkosítás engedélyezése</span><span class="sxs-lookup"><span data-stu-id="e3320-116">Example 1: Enable encryption</span></span>
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

<span data-ttu-id="e3320-117">Ez a példa lehetővé teszi a titkosítást a VM-en az AD hitelesítő adatok megadása nélkül.</span><span class="sxs-lookup"><span data-stu-id="e3320-117">This example enables encryption on a VM without specifying AD credentials.</span></span>

### <span data-ttu-id="e3320-118">2. példa: A titkosítás engedélyezése folyamatbemenettel</span><span class="sxs-lookup"><span data-stu-id="e3320-118">Example 2: Enable encryption with pipelined input</span></span>
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

<span data-ttu-id="e3320-119">Ez a példa az AD hitelesítő adatok megadása nélkül küldi el a paramétereket a folyamat által bevitt adatokkal a virtuális gép titkosításának engedélyezéséhez.</span><span class="sxs-lookup"><span data-stu-id="e3320-119">This example sends parameters using pipelined input to enable encryption on a VM, without specifying AD credentials.</span></span>

### <span data-ttu-id="e3320-120">3. példa: Titkosítás engedélyezése az Azure AD-ügyfélazonosító és a titkos ügyfélprogram használatával</span><span class="sxs-lookup"><span data-stu-id="e3320-120">Example 3: Enable encryption using Azure AD Client ID and Client Secret</span></span>
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

<span data-ttu-id="e3320-121">Ez a példa Azure AD ügyfélazonosítót és ügyfélkódot használ a virtuális gép titkosításának engedélyezéséhez.</span><span class="sxs-lookup"><span data-stu-id="e3320-121">This example uses Azure AD client ID and client secret to enable encryption on a VM.</span></span>

### <span data-ttu-id="e3320-122">4. példa: Titkosítás engedélyezése az Azure AD-ügyfélazonosító és az ügyféltanúsítási thumbprint használatával</span><span class="sxs-lookup"><span data-stu-id="e3320-122">Example 4: Enable encryption using Azure AD client ID and client certification thumbprint</span></span>
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

<span data-ttu-id="e3320-123">Ebben a példában az Azure AD-ügyfélazonosító és az ügyféltanúsítási thumbprints lehetővé teszi a titkosítást a VM-en.</span><span class="sxs-lookup"><span data-stu-id="e3320-123">This example uses Azure AD client ID and client certification thumbprints to enable encryption on a VM.</span></span>

### <span data-ttu-id="e3320-124">5. példa: Titkosítás engedélyezése az Azure AD-ügyfélazonosító, az ügyfélkulcs és a titkosítási kulcs titkosításának titkosítása kulcs használatával</span><span class="sxs-lookup"><span data-stu-id="e3320-124">Example 5: Enable encryption using Azure AD client ID, client secret, and wrap disk encryption key by using key encryption key</span></span>
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

<span data-ttu-id="e3320-125">Ebben a példában az Azure AD-ügyfélazonosító és az ügyfélkulcs használatával engedélyezi a titkosítást a VM-en, és egy kulcstitkosítási kulccsal tördeli a lemeztitkosítási kulcsot.</span><span class="sxs-lookup"><span data-stu-id="e3320-125">This example uses Azure AD client ID and client secret to enable encryption on a VM, and wraps the disk encryption key using a key encryption key.</span></span>

### <span data-ttu-id="e3320-126">6. példa: Titkosítás engedélyezése Az Azure AD ügyfélazonosító, az ügyfél-tanúsítvány thumbprint és a wrap disk encryptionkey by using key encryption key</span><span class="sxs-lookup"><span data-stu-id="e3320-126">Example 6: Enable encryption using Azure AD client ID, client cert thumbprint, and wrap disk encryptionkey by using key encryption key</span></span>
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

<span data-ttu-id="e3320-127">Ebben a példában az Azure AD-ügyfélazonosító és az ügyfél-tanúsítvány thumbprint használatával lehetővé teszi a titkosítást a VM-en, és egy kulcstitkosítási kulccsal tördeli a lemeztitkosítási kulcsot.</span><span class="sxs-lookup"><span data-stu-id="e3320-127">This example uses Azure AD client ID and client cert thumbprint to enable encryption on a VM, and wraps the disk encryption key using a key encryption key.</span></span>

## <span data-ttu-id="e3320-128">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e3320-128">PARAMETERS</span></span>

### <span data-ttu-id="e3320-129">-AadClientCertThumbprint</span><span class="sxs-lookup"><span data-stu-id="e3320-129">-AadClientCertThumbprint</span></span>
<span data-ttu-id="e3320-130">Az AzureActive Directory (Azure AD) alkalmazás ügyfélalkalmazás tanúsítványának thumbprint-ját adja meg, amely rendelkezik a KeyVault számára titkos kulcsok **írására vonatkozó engedélyekkel.**</span><span class="sxs-lookup"><span data-stu-id="e3320-130">Specifies the thumbprint of the AzureActive Directory (Azure AD) application client certificate that has permissions to write secrets to **KeyVault**.</span></span>
<span data-ttu-id="e3320-131">Előfeltételeként az Azure AD-ügyfél tanúsítványát korábban telepíteni kell a virtuális gép helyi számítógép `my` tanúsítványtárában.</span><span class="sxs-lookup"><span data-stu-id="e3320-131">As a prerequisite, the Azure AD client certificate must be previously deployed to the virtual machine's local computer `my` certificate store.</span></span>
<span data-ttu-id="e3320-132">A Add-AzVMSecret parancsmag használatával tanúsítványt telepíthet egy virtuális gépre az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="e3320-132">The Add-AzVMSecret cmdlet can be used to deploy a certificate to a virtual machine in Azure.</span></span>
<span data-ttu-id="e3320-133">További részletekért lásd az **Add-AzVMSecret** parancsmag súgóját.</span><span class="sxs-lookup"><span data-stu-id="e3320-133">For more details, see the **Add-AzVMSecret** cmdlet help.</span></span>
<span data-ttu-id="e3320-134">A tanúsítványt korábban a tanúsítványtároló virtuális számítógép helyi számítógépére kell telepíteni.</span><span class="sxs-lookup"><span data-stu-id="e3320-134">The certificate must be previously deployed to the virtual machine local computer my certificate store.</span></span>

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

### <span data-ttu-id="e3320-135">-AadClientID</span><span class="sxs-lookup"><span data-stu-id="e3320-135">-AadClientID</span></span>
<span data-ttu-id="e3320-136">Annak az Azure AD-alkalmazásnak az ügyfélazonosítóját adja meg, amely rendelkezik a KeyVaultnak titkos kulcsok **írásához szükséges engedélyekkel.**</span><span class="sxs-lookup"><span data-stu-id="e3320-136">Specifies the client ID of the Azure AD application that has permissions to write secrets to **KeyVault**.</span></span>

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

### <span data-ttu-id="e3320-137">-AadClientSecret</span><span class="sxs-lookup"><span data-stu-id="e3320-137">-AadClientSecret</span></span>
<span data-ttu-id="e3320-138">Annak az Azure AD-alkalmazásnak az ügyfélkulcsát adja meg, amely rendelkezik a KeyVaultnak való titkos kulcsok **írásához szükséges engedélyekkel.**</span><span class="sxs-lookup"><span data-stu-id="e3320-138">Specifies the client secret of the Azure AD application that has permissions to write secrets to **KeyVault**.</span></span>

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

### <span data-ttu-id="e3320-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3320-139">-DefaultProfile</span></span>
<span data-ttu-id="e3320-140">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e3320-140">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3320-141">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="e3320-141">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="e3320-142">Azt jelzi, hogy ez a parancsmag letiltja a bővítmény alverziója automatikus frissítését.</span><span class="sxs-lookup"><span data-stu-id="e3320-142">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

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

### <span data-ttu-id="e3320-143">-DiskEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="e3320-143">-DiskEncryptionKeyVaultId</span></span>
<span data-ttu-id="e3320-144">Annak a **KeyVault-kulcsnak** az erőforrás-azonosítója, amelybe a virtuális gép titkosítási kulcsait fel kell tölteni.</span><span class="sxs-lookup"><span data-stu-id="e3320-144">Specifies the resource ID of the **KeyVault** to which the virtual machine encryption keys should be uploaded.</span></span>

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

### <span data-ttu-id="e3320-145">-DiskEncryptionKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="e3320-145">-DiskEncryptionKeyVaultUrl</span></span>
<span data-ttu-id="e3320-146">Megadja a **KeyVault URL-címét,** amelyre a virtuális gép titkosítási kulcsait fel kell tölteni.</span><span class="sxs-lookup"><span data-stu-id="e3320-146">Specifies the **KeyVault** URL to which the virtual machine encryption keys should be uploaded.</span></span>

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

### <span data-ttu-id="e3320-147">-EncryptFormatAll</span><span class="sxs-lookup"><span data-stu-id="e3320-147">-EncryptFormatAll</span></span>
<span data-ttu-id="e3320-148">Encrypt-Format összes olyan adatmeghajtót, amely még nincs titkosítva</span><span class="sxs-lookup"><span data-stu-id="e3320-148">Encrypt-Format all data drives that are not already encrypted</span></span>

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

### <span data-ttu-id="e3320-149">-ExtensionPublisherName</span><span class="sxs-lookup"><span data-stu-id="e3320-149">-ExtensionPublisherName</span></span>
<span data-ttu-id="e3320-150">A bővítmény közzétevőjának neve.</span><span class="sxs-lookup"><span data-stu-id="e3320-150">The extension publisher name.</span></span> <span data-ttu-id="e3320-151">Ezt a paramétert csak a "Microsoft.Azure.Security" alapértelmezett értékének felülbírálása érdekében adja meg.</span><span class="sxs-lookup"><span data-stu-id="e3320-151">Specify this parameter only to override the default value of "Microsoft.Azure.Security".</span></span>

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

### <span data-ttu-id="e3320-152">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="e3320-152">-ExtensionType</span></span>
<span data-ttu-id="e3320-153">A bővítmény típusa.</span><span class="sxs-lookup"><span data-stu-id="e3320-153">The extension type.</span></span> <span data-ttu-id="e3320-154">Ezt a paramétert megadva felülbírálhatja a Windows-VMs -hez használt "AzureDiskEncryption" és a Linux-alapú "AzureDiskEncryptionForLinux" alapértelmezett értékét.</span><span class="sxs-lookup"><span data-stu-id="e3320-154">Specify this parameter to override its default value of "AzureDiskEncryption" for Windows VMs and "AzureDiskEncryptionForLinux" for Linux VMs.</span></span>

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

### <span data-ttu-id="e3320-155">-Force</span><span class="sxs-lookup"><span data-stu-id="e3320-155">-Force</span></span>
<span data-ttu-id="e3320-156">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="e3320-156">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e3320-157">-KeyEncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="e3320-157">-KeyEncryptionAlgorithm</span></span>
<span data-ttu-id="e3320-158">Megadja a virtuális gép kulcstitkosítási kulcsának tördelt és tördelt algoritmusát.</span><span class="sxs-lookup"><span data-stu-id="e3320-158">Specifies the algorithm that is used to wrap and unwrap the key encryption key of the virtual machine.</span></span>
<span data-ttu-id="e3320-159">Az alapértelmezett érték az RSA-OAEP.</span><span class="sxs-lookup"><span data-stu-id="e3320-159">The default value is RSA-OAEP.</span></span>

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

### <span data-ttu-id="e3320-160">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="e3320-160">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="e3320-161">A virtuális gépi titkosítási kulcs tördelt és tördelt kulcsának URL-címe.</span><span class="sxs-lookup"><span data-stu-id="e3320-161">Specifies the URL of the key encryption key that is used to wrap and unwrap the virtual machine encryption key.</span></span>
<span data-ttu-id="e3320-162">Ennek a teljes verziójú URL-címnek kell lennie.</span><span class="sxs-lookup"><span data-stu-id="e3320-162">This must be the full versioned URL.</span></span>

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

### <span data-ttu-id="e3320-163">-KeyEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="e3320-163">-KeyEncryptionKeyVaultId</span></span>
<span data-ttu-id="e3320-164">Annak a **KeyVault-kulcsnak** az erőforrásazonosítóját adja meg, amely a virtuális gép titkosítási kulcsának tördelt és tördelt kulcsát tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="e3320-164">Specifies the resource ID of the **KeyVault** that contains key encryption key that is used to wrap and unwrap the virtual machine encryption key.</span></span>
<span data-ttu-id="e3320-165">Ennek teljes verziójú URL-címnek kell lennie.</span><span class="sxs-lookup"><span data-stu-id="e3320-165">This must be a full versioned URL.</span></span>

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

### <span data-ttu-id="e3320-166">-Name</span><span class="sxs-lookup"><span data-stu-id="e3320-166">-Name</span></span>
<span data-ttu-id="e3320-167">Megadja a bővítményt képviselő Azure Resource Manager-erőforrás nevét.</span><span class="sxs-lookup"><span data-stu-id="e3320-167">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span> <span data-ttu-id="e3320-168">Ha a *Name paramétert* nem ad meg, a telepített bővítmény neve AzureDiskEncryption lesz Windows virtuális gépeken és AzureDiskEncryptionForLinux Linux-virtuális gépeken.</span><span class="sxs-lookup"><span data-stu-id="e3320-168">If the *Name* parameter is omitted, the installed extension will be named AzureDiskEncryption on Windows virtual machines and AzureDiskEncryptionForLinux on Linux virtual machines.</span></span>


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

### <span data-ttu-id="e3320-169">-Passphrase</span><span class="sxs-lookup"><span data-stu-id="e3320-169">-Passphrase</span></span>
<span data-ttu-id="e3320-170">Csak a Linux-virtuális gépek titkosításához használt jelszavakat adja meg.</span><span class="sxs-lookup"><span data-stu-id="e3320-170">Specifies the passphrase used for encrypting Linux virtual machines only.</span></span>
<span data-ttu-id="e3320-171">Ez a paraméter nem használható a Windows operációs rendszert futtató virtuális gépekhez.</span><span class="sxs-lookup"><span data-stu-id="e3320-171">This parameter is not used for virtual machines that run the Windows operating system.</span></span>

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

### <span data-ttu-id="e3320-172">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3320-172">-ResourceGroupName</span></span>
<span data-ttu-id="e3320-173">A virtuális gép erőforráscsoportját adja meg.</span><span class="sxs-lookup"><span data-stu-id="e3320-173">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="e3320-174">-SequenceVersion</span><span class="sxs-lookup"><span data-stu-id="e3320-174">-SequenceVersion</span></span>
<span data-ttu-id="e3320-175">Egy virtuális gép titkosítási műveleteinek sorszámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="e3320-175">Specifies the sequence number of the encryption operations for a virtual machine.</span></span>
<span data-ttu-id="e3320-176">Ez minden, ugyanazon a virtuális gépen végrehajtott titkosítási műveletre egyedi.</span><span class="sxs-lookup"><span data-stu-id="e3320-176">This is unique per each encryption operation performed on the same virtual machine.</span></span>
<span data-ttu-id="e3320-177">A Get-AzVMExtension parancsmag a korábban használt sorszám beolvasásához használható.</span><span class="sxs-lookup"><span data-stu-id="e3320-177">The Get-AzVMExtension cmdlet can be used to retrieve the previous sequence number that was used.</span></span>

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

### <span data-ttu-id="e3320-178">-SkipVmBackup</span><span class="sxs-lookup"><span data-stu-id="e3320-178">-SkipVmBackup</span></span>
<span data-ttu-id="e3320-179">Biztonsági másolatok létrehozásának kihagyása Linuxos virtuális gépeken</span><span class="sxs-lookup"><span data-stu-id="e3320-179">Skip backup creation for Linux VMs</span></span>

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

### <span data-ttu-id="e3320-180">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="e3320-180">-TypeHandlerVersion</span></span>
<span data-ttu-id="e3320-181">A titkosítási bővítmény verzióját határozza meg.</span><span class="sxs-lookup"><span data-stu-id="e3320-181">Specifies the version of the encryption extension.</span></span>

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

### <span data-ttu-id="e3320-182">-VMName</span><span class="sxs-lookup"><span data-stu-id="e3320-182">-VMName</span></span>
<span data-ttu-id="e3320-183">A virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e3320-183">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="e3320-184">-VolumeType</span><span class="sxs-lookup"><span data-stu-id="e3320-184">-VolumeType</span></span>
<span data-ttu-id="e3320-185">Megadja, hogy milyen típusú virtuális gépköteteket kell titkosítási műveletet végrehajtani: operációs rendszer, adatok vagy mind.</span><span class="sxs-lookup"><span data-stu-id="e3320-185">Specifies the type of virtual machine volumes on which to perform encryption operation: OS, Data, or All.</span></span> 

<span data-ttu-id="e3320-186">Linux: A **VolumeType** paraméterre linuxos virtuális gépek titkosíthatók, és a Linux-terjesztés által támogatott értékre ("Os", "Data" vagy "All") kell állítani.</span><span class="sxs-lookup"><span data-stu-id="e3320-186">Linux: The **VolumeType** parameter is required when encrypting Linux virtual machines, and must be set to a value ("Os", "Data", or "All") supported by the Linux distribution.</span></span> 

<span data-ttu-id="e3320-187">Windows: A **VolumeType** paraméter elhagyható, ebben az esetben a művelet alapértelmezés szerint Az összes; ha a VolumeType paraméter egy windowsos virtuális géphez tartozik, akkor vagy Az összes, vagy az operációs rendszer paramétert kell beállítania.</span><span class="sxs-lookup"><span data-stu-id="e3320-187">Windows: The **VolumeType** parameter may be omitted, in which case the operation defaults to All; if the VolumeType parameter is present for a Windows virtual machine, it must be set to either All or OS.</span></span>

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

### <span data-ttu-id="e3320-188">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e3320-188">-Confirm</span></span>
<span data-ttu-id="e3320-189">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="e3320-189">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3320-190">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3320-190">-WhatIf</span></span>
<span data-ttu-id="e3320-191">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="e3320-191">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3320-192">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e3320-192">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3320-193">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3320-193">CommonParameters</span></span>
<span data-ttu-id="e3320-194">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3320-194">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3320-195">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e3320-195">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3320-196">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e3320-196">INPUTS</span></span>

### <span data-ttu-id="e3320-197">System.String</span><span class="sxs-lookup"><span data-stu-id="e3320-197">System.String</span></span>

### <span data-ttu-id="e3320-198">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="e3320-198">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e3320-199">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e3320-199">OUTPUTS</span></span>

### <span data-ttu-id="e3320-200">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="e3320-200">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="e3320-201">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e3320-201">NOTES</span></span>

## <span data-ttu-id="e3320-202">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e3320-202">RELATED LINKS</span></span>

[<span data-ttu-id="e3320-203">Add-AzVMSecret</span><span class="sxs-lookup"><span data-stu-id="e3320-203">Add-AzVMSecret</span></span>](./Add-AzVMSecret.md)

[<span data-ttu-id="e3320-204">Get-AzVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="e3320-204">Get-AzVMDiskEncryptionStatus</span></span>](./Get-AzVMDiskEncryptionStatus.md)

[<span data-ttu-id="e3320-205">Remove-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="e3320-205">Remove-AzVMDiskEncryptionExtension</span></span>](./Remove-AzVMDiskEncryptionExtension.md)


