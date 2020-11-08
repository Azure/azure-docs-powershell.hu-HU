---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 363FA51E-D075-4800-A4BE-BFF63FD25C90
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificate.md
ms.openlocfilehash: ede0598162fdecc760f33646c86171501ec46db4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195938"
---
# <span data-ttu-id="e16d5-101">Get-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="e16d5-101">Get-AzKeyVaultCertificate</span></span>

## <span data-ttu-id="e16d5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e16d5-102">SYNOPSIS</span></span>
<span data-ttu-id="e16d5-103">Egy kulcsos boltozattól kapja a tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="e16d5-103">Gets a certificate from a key vault.</span></span>

## <span data-ttu-id="e16d5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e16d5-104">SYNTAX</span></span>

### <span data-ttu-id="e16d5-105">ByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e16d5-105">ByName (Default)</span></span>
```
Get-AzKeyVaultCertificate [-VaultName] <String> [[-Name] <String>] [-InRemovedState] [-IncludePending]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e16d5-106">ByCertificateNameAndVersion</span><span class="sxs-lookup"><span data-stu-id="e16d5-106">ByCertificateNameAndVersion</span></span>
```
Get-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e16d5-107">ByCertificateAllVersions</span><span class="sxs-lookup"><span data-stu-id="e16d5-107">ByCertificateAllVersions</span></span>
```
Get-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e16d5-108">ByNameInputObject</span><span class="sxs-lookup"><span data-stu-id="e16d5-108">ByNameInputObject</span></span>
```
Get-AzKeyVaultCertificate [-InputObject] <PSKeyVault> [[-Name] <String>] [-InRemovedState] [-IncludePending]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e16d5-109">ByCertificateNameAndVersionInputObject</span><span class="sxs-lookup"><span data-stu-id="e16d5-109">ByCertificateNameAndVersionInputObject</span></span>
```
Get-AzKeyVaultCertificate [-InputObject] <PSKeyVault> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e16d5-110">ByCertificateAllVersionsInputObject</span><span class="sxs-lookup"><span data-stu-id="e16d5-110">ByCertificateAllVersionsInputObject</span></span>
```
Get-AzKeyVaultCertificate [-InputObject] <PSKeyVault> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e16d5-111">ByNameResourceId</span><span class="sxs-lookup"><span data-stu-id="e16d5-111">ByNameResourceId</span></span>
```
Get-AzKeyVaultCertificate [-ResourceId] <String> [[-Name] <String>] [-InRemovedState] [-IncludePending]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e16d5-112">ByCertificateNameAndVersionResourceId</span><span class="sxs-lookup"><span data-stu-id="e16d5-112">ByCertificateNameAndVersionResourceId</span></span>
```
Get-AzKeyVaultCertificate [-ResourceId] <String> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e16d5-113">ByCertificateAllVersionsResourceId</span><span class="sxs-lookup"><span data-stu-id="e16d5-113">ByCertificateAllVersionsResourceId</span></span>
```
Get-AzKeyVaultCertificate [-ResourceId] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e16d5-114">Leírás</span><span class="sxs-lookup"><span data-stu-id="e16d5-114">DESCRIPTION</span></span>
<span data-ttu-id="e16d5-115">A **Get-AzKeyVaultCertificate** parancsmag az Azure Key Vault-ban a megadott tanúsítványt vagy egy tanúsítvány verziószámát kapja.</span><span class="sxs-lookup"><span data-stu-id="e16d5-115">The **Get-AzKeyVaultCertificate** cmdlet gets the specified certificate or the versions of a certificate from a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="e16d5-116">Példák</span><span class="sxs-lookup"><span data-stu-id="e16d5-116">EXAMPLES</span></span>

### <span data-ttu-id="e16d5-117">Példa 1: tanúsítvány beszerzése</span><span class="sxs-lookup"><span data-stu-id="e16d5-117">Example 1: Get a certificate</span></span>
```powershell
PS C:\> Get-AzKeyVaultCertificate -VaultName "ContosoKV01" -Name "TestCert01"
Name        : testCert01
Certificate : [Subject] 
                CN=contoso.com

              [Issuer] 
                CN=contoso.com

              [Serial Number] 
                XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

              [Not Before] 
                2/8/2016 3:11:45 PM

              [Not After] 
                8/8/2016 4:21:45 PM

              [Thumbprint] 
                XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

KeyId       : https://contoso.vault.azure.net:443/keys/TestCert01/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
SecretId    : https://contoso.vault.azure.net:443/secrets/TestCert01/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
Thumbprint  : XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
Tags        : 
Enabled     : True
Created     : 2/8/2016 11:21:45 PM
Updated     : 2/8/2016 11:21:45 PM
```

### <span data-ttu-id="e16d5-118">2. példa: a tanúsítvány beszerzése és mentése pfx-ként</span><span class="sxs-lookup"><span data-stu-id="e16d5-118">Example 2: Get cert and save it as pfx</span></span>
<span data-ttu-id="e16d5-119">Ez a parancs a TestCert01 nevű tanúsítványt a ContosoKV01 nevű kulcs-boltozattal kapja meg.</span><span class="sxs-lookup"><span data-stu-id="e16d5-119">This command gets the certificate named TestCert01 from the key vault named ContosoKV01.</span></span> <span data-ttu-id="e16d5-120">A tanúsítvány PFX-fájlként való letöltéséhez futtassa az alábbi parancsot.</span><span class="sxs-lookup"><span data-stu-id="e16d5-120">To download the certificate as pfx file, run following command.</span></span> <span data-ttu-id="e16d5-121">Ezek a parancsok az Access SecretId, majd a tartalmat pfx-fájlként menti.</span><span class="sxs-lookup"><span data-stu-id="e16d5-121">These commands access SecretId and then save the content as a pfx file.</span></span>

```powershell
$cert = Get-AzKeyVaultCertificate -VaultName "ContosoKV01" -Name "TestCert01"
$secret = Get-AzKeyVaultSecret -VaultName $vaultName -Name $cert.Name
$secretValueText = '';
$ssPtr = [System.Runtime.InteropServices.Marshal]::SecureStringToBSTR($secret.SecretValue)
try {
    $secretValueText = [System.Runtime.InteropServices.Marshal]::PtrToStringBSTR($ssPtr)
} finally {
    [System.Runtime.InteropServices.Marshal]::ZeroFreeBSTR($ssPtr)
}
$secretByte = [Convert]::FromBase64String($secretValueText)
$x509Cert = new-object System.Security.Cryptography.X509Certificates.X509Certificate2
$x509Cert.Import($secretByte, "", "Exportable,PersistKeySet")
$type = [System.Security.Cryptography.X509Certificates.X509ContentType]::Pfx
$pfxFileByte = $x509Cert.Export($type, $password)

# Write to a file
[System.IO.File]::WriteAllBytes("KeyVault.pfx", $pfxFileByte)
```

### <span data-ttu-id="e16d5-122">3. példa: az összes olyan tanúsítvány beszerzése, amelyet töröltek, de ez a kulcsfájl nem törlődik.</span><span class="sxs-lookup"><span data-stu-id="e16d5-122">Example 3: Get all the certificates that have been deleted but not purged for this key vault.</span></span>
```powershell
PS C:\> Get-AzKeyVaultCertificate -VaultName 'contoso' -InRemovedState

DeletedDate        : 5/24/2018 6:08:32 PM
Enabled            : True
Expires            : 11/24/2018 6:08:13 PM
NotBefore          : 5/24/2018 5:58:13 PM
Created            : 5/24/2018 6:08:13 PM
Updated            : 5/24/2018 6:08:13 PM
Tags               :
VaultName          : contoso
Name               : test1
Version            :
Id                 : https://contoso.vault.azure.net:443/certificates/test1

ScheduledPurgeDate : 8/22/2018 6:10:47 PM
DeletedDate        : 5/24/2018 6:10:47 PM
Enabled            : True
Expires            : 11/24/2018 6:09:44 PM
NotBefore          : 5/24/2018 5:59:44 PM
Created            : 5/24/2018 6:09:44 PM
Updated            : 5/24/2018 6:09:44 PM
Tags               :
VaultName          : contoso
Name               : test2
Version            :
Id                 : https://contoso.vault.azure.net:443/certificates/test2
```

<span data-ttu-id="e16d5-123">Ez a parancs beilleszti a korábban törölt, de el nem távolított tanúsítványokat a contoso nevű fő boltozatba.</span><span class="sxs-lookup"><span data-stu-id="e16d5-123">This command gets all the certificates that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="e16d5-124">Példa 4: beolvassa a MyCert, amelyet töröltek, de erre a gombra nincs kitisztítva.</span><span class="sxs-lookup"><span data-stu-id="e16d5-124">Example 4: Gets the certificate MyCert that has been deleted but not purged for this key vault.</span></span>
```powershell
PS C:\> Get-AzKeyVaultCertificate -VaultName 'contoso' -Name 'test1' -InRemovedState

Certificate        : [Subject]
                       CN=contoso.com

                     [Issuer]
                       CN=contoso.com

                     [Serial Number]
                       XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

                     [Not Before]
                       5/24/2018 10:58:13 AM

                     [Not After]
                       11/24/2018 10:08:13 AM

                     [Thumbprint]
                       XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

KeyId              : https://contoso.vault.azure.net:443/keys/test1/7fe415d5518240c1a6fce89986b8d334
SecretId           : https://contoso.vault.azure.net:443/secrets/test1/7fe415d5518240c1a6fce89986b8d334
Thumbprint         : XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
RecoveryLevel      : Recoverable+Purgeable
ScheduledPurgeDate : 8/22/2018 6:08:32 PM
DeletedDate        : 5/24/2018 6:08:32 PM
Enabled            : True
Expires            : 11/24/2018 6:08:13 PM
NotBefore          : 5/24/2018 5:58:13 PM
Created            : 5/24/2018 6:08:13 PM
Updated            : 5/24/2018 6:08:13 PM
Tags               :
VaultName          : contoso
Name               : test1
Version            : 7fe415d5518240c1a6fce89986b8d334
Id                 : https://contoso.vault.azure.net:443/certificates/test1/7fe415d5518240c1a6fce89986b8d334
```

<span data-ttu-id="e16d5-125">Ez a parancs a contoso nevű kulcsfájl "MyCert" nevű tanúsítványát kapja meg, amelyet korábban törölt, de nem.</span><span class="sxs-lookup"><span data-stu-id="e16d5-125">This command gets the certificate named 'MyCert' that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="e16d5-126">Ez a parancs metaadatokat ad vissza, például a törlési dátumot, valamint a törölt tanúsítvány ütemezett végleges dátumát.</span><span class="sxs-lookup"><span data-stu-id="e16d5-126">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted certificate.</span></span>

### <span data-ttu-id="e16d5-127">Példa 5: szűrést használó tanúsítványok listázása</span><span class="sxs-lookup"><span data-stu-id="e16d5-127">Example 5: List certificates using filtering</span></span>
```powershell
PS C:\> Get-AzKeyVaultCertificate -VaultName "ContosoKV01" -Name "test*"

Enabled   : True
Expires   : 8/5/2019 2:39:25 AM
NotBefore : 2/5/2019 2:29:25 AM
Created   : 2/5/2019 2:39:25 AM
Updated   : 2/5/2019 2:39:25 AM
Tags      :
VaultName : ContosoKV01
Name      : test1
Version   :
Id        : https://ContosoKV01.vault.azure.net:443/certificates/test1

Enabled   : True
Expires   : 8/5/2019 2:39:25 AM
NotBefore : 2/5/2019 2:29:25 AM
Created   : 2/5/2019 2:39:25 AM
Updated   : 2/5/2019 2:39:25 AM
Tags      :
VaultName : ContosoKV01
Name      : test2
Version   :
Id        : https://ContosoKV01.vault.azure.net:443/certificates/test2

This command gets all certificates starting with "test" from the key vault named ContosoKV01.
```

## <span data-ttu-id="e16d5-128">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e16d5-128">PARAMETERS</span></span>

### <span data-ttu-id="e16d5-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e16d5-129">-DefaultProfile</span></span>
<span data-ttu-id="e16d5-130">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="e16d5-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e16d5-131">-IncludePending</span><span class="sxs-lookup"><span data-stu-id="e16d5-131">-IncludePending</span></span>
<span data-ttu-id="e16d5-132">Annak megadása, hogy függőben lévő tanúsítványokat szeretne-e szerepeltetni a kimenetben</span><span class="sxs-lookup"><span data-stu-id="e16d5-132">Specifies whether to include pending certificates in the output</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByName, ByNameInputObject, ByNameResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e16d5-133">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="e16d5-133">-IncludeVersions</span></span>
<span data-ttu-id="e16d5-134">Azt jelzi, hogy ez a művelet a tanúsítvány minden változatát bekapja.</span><span class="sxs-lookup"><span data-stu-id="e16d5-134">Indicates that this operation gets all versions of the certificate.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByCertificateAllVersions, ByCertificateAllVersionsInputObject, ByCertificateAllVersionsResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e16d5-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e16d5-135">-InputObject</span></span>
<span data-ttu-id="e16d5-136">A boltozat objektum.</span><span class="sxs-lookup"><span data-stu-id="e16d5-136">KeyVault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByNameInputObject, ByCertificateNameAndVersionInputObject, ByCertificateAllVersionsInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e16d5-137">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="e16d5-137">-InRemovedState</span></span>
<span data-ttu-id="e16d5-138">Annak megadása, hogy a kimenetben a korábban törölt tanúsítványokat szeretné-e szerepeltetni</span><span class="sxs-lookup"><span data-stu-id="e16d5-138">Specifies whether to include previously deleted certificates in the output</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByName, ByNameInputObject, ByNameResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e16d5-139">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e16d5-139">-Name</span></span>
<span data-ttu-id="e16d5-140">A beolvasott tanúsítvány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e16d5-140">Specifies the name of the certificate to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName, ByNameInputObject, ByNameResourceId
Aliases: CertificateName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByCertificateNameAndVersion, ByCertificateAllVersions, ByCertificateNameAndVersionInputObject, ByCertificateAllVersionsInputObject, ByCertificateNameAndVersionResourceId, ByCertificateAllVersionsResourceId
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e16d5-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e16d5-141">-ResourceId</span></span>
<span data-ttu-id="e16d5-142">A főkészlet erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="e16d5-142">KeyVault Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameResourceId, ByCertificateNameAndVersionResourceId, ByCertificateAllVersionsResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e16d5-143">-VaultName</span><span class="sxs-lookup"><span data-stu-id="e16d5-143">-VaultName</span></span>
<span data-ttu-id="e16d5-144">A kulcsfájl nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e16d5-144">Specifies the name of a key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName, ByCertificateNameAndVersion, ByCertificateAllVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e16d5-145">-Verzió</span><span class="sxs-lookup"><span data-stu-id="e16d5-145">-Version</span></span>
<span data-ttu-id="e16d5-146">A tanúsítvány verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="e16d5-146">Specifies the version of a certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: ByCertificateNameAndVersion, ByCertificateNameAndVersionInputObject, ByCertificateNameAndVersionResourceId
Aliases: CertificateVersion

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e16d5-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e16d5-147">CommonParameters</span></span>
<span data-ttu-id="e16d5-148">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e16d5-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e16d5-149">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e16d5-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e16d5-150">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e16d5-150">INPUTS</span></span>

### <span data-ttu-id="e16d5-151">Microsoft. Azure. Command. PSKeyVault. models.</span><span class="sxs-lookup"><span data-stu-id="e16d5-151">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="e16d5-152">System. String</span><span class="sxs-lookup"><span data-stu-id="e16d5-152">System.String</span></span>

## <span data-ttu-id="e16d5-153">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e16d5-153">OUTPUTS</span></span>

### <span data-ttu-id="e16d5-154">Microsoft. Azure. Command. PSKeyVaultCertificateIdentityItem. models.</span><span class="sxs-lookup"><span data-stu-id="e16d5-154">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span></span>

### <span data-ttu-id="e16d5-155">Microsoft. Azure. Command. PSKeyVaultCertificate. models.</span><span class="sxs-lookup"><span data-stu-id="e16d5-155">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span></span>

### <span data-ttu-id="e16d5-156">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="e16d5-156">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificate</span></span>

### <span data-ttu-id="e16d5-157">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificateIdentityItem</span><span class="sxs-lookup"><span data-stu-id="e16d5-157">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificateIdentityItem</span></span>

## <span data-ttu-id="e16d5-158">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e16d5-158">NOTES</span></span>

## <span data-ttu-id="e16d5-159">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e16d5-159">RELATED LINKS</span></span>

[<span data-ttu-id="e16d5-160">Add-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="e16d5-160">Add-AzKeyVaultCertificate</span></span>](./Add-AzKeyVaultCertificate.md)

[<span data-ttu-id="e16d5-161">Importálás – AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="e16d5-161">Import-AzKeyVaultCertificate</span></span>](./Import-AzKeyVaultCertificate.md)

[<span data-ttu-id="e16d5-162">Remove-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="e16d5-162">Remove-AzKeyVaultCertificate</span></span>](./Remove-AzKeyVaultCertificate.md)

[<span data-ttu-id="e16d5-163">Visszavonás – AzKeyVaultSecretCertificate</span><span class="sxs-lookup"><span data-stu-id="e16d5-163">Undo-AzKeyVaultSecretCertificate</span></span>](./Undo-AzKeyVaultSecretCertificate.md)
