---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 363FA51E-D075-4800-A4BE-BFF63FD25C90
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificate.md
ms.openlocfilehash: 87b030229eb2a1f4bb91122aaec8a119134d27fb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494485"
---
# <span data-ttu-id="4be7e-101">Get-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="4be7e-101">Get-AzureKeyVaultCertificate</span></span>

## <span data-ttu-id="4be7e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4be7e-102">SYNOPSIS</span></span>
<span data-ttu-id="4be7e-103">Egy kulcsos boltozattól kapja a tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="4be7e-103">Gets a certificate from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4be7e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4be7e-104">SYNTAX</span></span>

### <span data-ttu-id="4be7e-105">ByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4be7e-105">ByName (Default)</span></span>
```
Get-AzureKeyVaultCertificate [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4be7e-106">ByCertificateNameAndVersion</span><span class="sxs-lookup"><span data-stu-id="4be7e-106">ByCertificateNameAndVersion</span></span>
```
Get-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4be7e-107">ByCertificateAllVersions</span><span class="sxs-lookup"><span data-stu-id="4be7e-107">ByCertificateAllVersions</span></span>
```
Get-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4be7e-108">ByNameInputObject</span><span class="sxs-lookup"><span data-stu-id="4be7e-108">ByNameInputObject</span></span>
```
Get-AzureKeyVaultCertificate [-InputObject] <PSKeyVault> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4be7e-109">ByCertificateNameAndVersionInputObject</span><span class="sxs-lookup"><span data-stu-id="4be7e-109">ByCertificateNameAndVersionInputObject</span></span>
```
Get-AzureKeyVaultCertificate [-InputObject] <PSKeyVault> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4be7e-110">ByCertificateAllVersionsInputObject</span><span class="sxs-lookup"><span data-stu-id="4be7e-110">ByCertificateAllVersionsInputObject</span></span>
```
Get-AzureKeyVaultCertificate [-InputObject] <PSKeyVault> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4be7e-111">Leírás</span><span class="sxs-lookup"><span data-stu-id="4be7e-111">DESCRIPTION</span></span>
<span data-ttu-id="4be7e-112">A **Get-AzureKeyVaultCertificate** parancsmag az Azure Key Vault-ban a megadott tanúsítványt vagy egy tanúsítvány verziószámát kapja.</span><span class="sxs-lookup"><span data-stu-id="4be7e-112">The **Get-AzureKeyVaultCertificate** cmdlet gets the specified certificate or the versions of a certificate from a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="4be7e-113">Példák</span><span class="sxs-lookup"><span data-stu-id="4be7e-113">EXAMPLES</span></span>

### <span data-ttu-id="4be7e-114">Példa 1: tanúsítvány beszerzése</span><span class="sxs-lookup"><span data-stu-id="4be7e-114">Example 1: Get a certificate</span></span>
```
PS C:\>Get-AzureKeyVaultCertificate -VaultName "ContosoKV01" -Name "TestCert01"
Name        : testCert01
Certificate : [Subject] 
                CN=contoso.com

              [Issuer] 
                CN=contoso.com

              [Serial Number] 
                05979C5A2F0741D5A3B6F97673E8A118

              [Not Before] 
                2/8/2016 3:11:45 PM

              [Not After] 
                8/8/2016 4:21:45 PM

              [Thumbprint] 
                3E9B6848AD1834284157D68B060F748037F663C8

Thumbprint  : 3E9B6848AD1834284157D68B060F748037F663C8
Tags        : 
Enabled     : True
Created     : 2/8/2016 11:21:45 PM
Updated     : 2/8/2016 11:21:45 PM
```

<span data-ttu-id="4be7e-115">Ez a parancs a TestCert01 nevű tanúsítványt a ContosoKV01 nevű kulcs-boltozattal kapja meg.</span><span class="sxs-lookup"><span data-stu-id="4be7e-115">This command gets the certificate named TestCert01 from the key vault named ContosoKV01.</span></span>

### <span data-ttu-id="4be7e-116">2. példa: az összes olyan tanúsítvány beszerzése, amelyet töröltek, de ez a kulcsfájl nem törlődik.</span><span class="sxs-lookup"><span data-stu-id="4be7e-116">Example 2: Get all the certificates that have been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzureKeyVaultCertificate -VaultName 'Contoso' -InRemovedState
```

<span data-ttu-id="4be7e-117">Ez a parancs beilleszti a korábban törölt, de el nem távolított tanúsítványokat a contoso nevű fő boltozatba.</span><span class="sxs-lookup"><span data-stu-id="4be7e-117">This command gets all the certificates that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="4be7e-118">3. példa: beolvassa a MyCert, amelyet törölték, de erre a kulcsra nincs kitisztítva.</span><span class="sxs-lookup"><span data-stu-id="4be7e-118">Example 3: Gets the certificate MyCert that has been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzureKeyVaultCertificate -VaultName 'Contoso' -Name 'MyCert' -InRemovedState
```

<span data-ttu-id="4be7e-119">Ez a parancs a contoso nevű kulcsfájl "MyCert" nevű tanúsítványát kapja meg, amelyet korábban törölt, de nem.</span><span class="sxs-lookup"><span data-stu-id="4be7e-119">This command gets the certificate named 'MyCert' that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="4be7e-120">Ez a parancs metaadatokat ad vissza, például a törlési dátumot, valamint a törölt tanúsítvány ütemezett végleges dátumát.</span><span class="sxs-lookup"><span data-stu-id="4be7e-120">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted certificate.</span></span>

## <span data-ttu-id="4be7e-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4be7e-121">PARAMETERS</span></span>

### <span data-ttu-id="4be7e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4be7e-122">-DefaultProfile</span></span>
<span data-ttu-id="4be7e-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="4be7e-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4be7e-124">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="4be7e-124">-IncludeVersions</span></span>
<span data-ttu-id="4be7e-125">Azt jelzi, hogy ez a művelet a tanúsítvány minden változatát bekapja.</span><span class="sxs-lookup"><span data-stu-id="4be7e-125">Indicates that this operation gets all versions of the certificate.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByCertificateAllVersions, ByCertificateAllVersionsInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4be7e-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4be7e-126">-InputObject</span></span>
<span data-ttu-id="4be7e-127">A boltozat objektum.</span><span class="sxs-lookup"><span data-stu-id="4be7e-127">KeyVault object.</span></span>

```yaml
Type: PSKeyVault
Parameter Sets: ByNameInputObject, ByCertificateNameAndVersionInputObject, ByCertificateAllVersionsInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4be7e-128">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="4be7e-128">-InRemovedState</span></span>
<span data-ttu-id="4be7e-129">Annak megadása, hogy a kimenetben a korábban törölt tanúsítványokat szeretné-e szerepeltetni</span><span class="sxs-lookup"><span data-stu-id="4be7e-129">Specifies whether to include previously deleted certificates in the output</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByName, ByNameInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4be7e-130">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4be7e-130">-Name</span></span>
<span data-ttu-id="4be7e-131">A beolvasott tanúsítvány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4be7e-131">Specifies the name of the certificate to get.</span></span>

```yaml
Type: String
Parameter Sets: ByName, ByNameInputObject
Aliases: CertificateName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByCertificateNameAndVersion, ByCertificateAllVersions, ByCertificateNameAndVersionInputObject, ByCertificateAllVersionsInputObject
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4be7e-132">-VaultName</span><span class="sxs-lookup"><span data-stu-id="4be7e-132">-VaultName</span></span>
<span data-ttu-id="4be7e-133">A kulcsfájl nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4be7e-133">Specifies the name of a key vault.</span></span>

```yaml
Type: String
Parameter Sets: ByName, ByCertificateNameAndVersion, ByCertificateAllVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4be7e-134">-Verzió</span><span class="sxs-lookup"><span data-stu-id="4be7e-134">-Version</span></span>
<span data-ttu-id="4be7e-135">A tanúsítvány verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="4be7e-135">Specifies the version of a certificate.</span></span>

```yaml
Type: String
Parameter Sets: ByCertificateNameAndVersion, ByCertificateNameAndVersionInputObject
Aliases: CertificateVersion

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4be7e-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4be7e-136">CommonParameters</span></span>
<span data-ttu-id="4be7e-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4be7e-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4be7e-138">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4be7e-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4be7e-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4be7e-139">INPUTS</span></span>

### <span data-ttu-id="4be7e-140">Nincs</span><span class="sxs-lookup"><span data-stu-id="4be7e-140">None</span></span>
<span data-ttu-id="4be7e-141">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="4be7e-141">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4be7e-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4be7e-142">OUTPUTS</span></span>

### <span data-ttu-id="4be7e-143">System. Collections. Generic. list ' 1 [Microsoft. Azure. commands. devault. models. PSKeyVaultCertificateIdentityItem]</span><span class="sxs-lookup"><span data-stu-id="4be7e-143">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem]</span></span>

### <span data-ttu-id="4be7e-144">Microsoft. Azure. Command. PSKeyVaultCertificate. models.</span><span class="sxs-lookup"><span data-stu-id="4be7e-144">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span></span>

## <span data-ttu-id="4be7e-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4be7e-145">NOTES</span></span>

## <span data-ttu-id="4be7e-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4be7e-146">RELATED LINKS</span></span>

[<span data-ttu-id="4be7e-147">Add-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="4be7e-147">Add-AzureKeyVaultCertificate</span></span>](./Add-AzureKeyVaultCertificate.md)

[<span data-ttu-id="4be7e-148">Importálás – AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="4be7e-148">Import-AzureKeyVaultCertificate</span></span>](./Import-AzureKeyVaultCertificate.md)

[<span data-ttu-id="4be7e-149">Remove-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="4be7e-149">Remove-AzureKeyVaultCertificate</span></span>](./Remove-AzureKeyVaultCertificate.md)

[<span data-ttu-id="4be7e-150">Visszavonás – AzureKeyVaultSecretCertificate</span><span class="sxs-lookup"><span data-stu-id="4be7e-150">Undo-AzureKeyVaultSecretCertificate</span></span>](./Undo-AzureKeyVaultSecretCertificate.md)
