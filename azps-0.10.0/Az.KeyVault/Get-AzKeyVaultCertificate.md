---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 363FA51E-D075-4800-A4BE-BFF63FD25C90
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/get-AzKeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificate.md
ms.openlocfilehash: 40514bdd6ed8d37679d3002f80146e622a0614e9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842161"
---
# <span data-ttu-id="7004a-101">Get-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="7004a-101">Get-AzKeyVaultCertificate</span></span>

## <span data-ttu-id="7004a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7004a-102">SYNOPSIS</span></span>
<span data-ttu-id="7004a-103">Egy kulcsos boltozattól kapja a tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="7004a-103">Gets a certificate from a key vault.</span></span>

## <span data-ttu-id="7004a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7004a-104">SYNTAX</span></span>

### <span data-ttu-id="7004a-105">ByVaultName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7004a-105">ByVaultName (Default)</span></span>
```
Get-AzKeyVaultCertificate [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7004a-106">ByCertificateName</span><span class="sxs-lookup"><span data-stu-id="7004a-106">ByCertificateName</span></span>
```
Get-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7004a-107">ByCertificateVersions</span><span class="sxs-lookup"><span data-stu-id="7004a-107">ByCertificateVersions</span></span>
```
Get-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7004a-108">ByDeletedCertificates</span><span class="sxs-lookup"><span data-stu-id="7004a-108">ByDeletedCertificates</span></span>
```
Get-AzKeyVaultCertificate [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7004a-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="7004a-109">DESCRIPTION</span></span>
<span data-ttu-id="7004a-110">A **Get-AzKeyVaultCertificate** parancsmag az Azure Key Vault-ban a megadott tanúsítványt vagy egy tanúsítvány verziószámát kapja.</span><span class="sxs-lookup"><span data-stu-id="7004a-110">The **Get-AzKeyVaultCertificate** cmdlet gets the specified certificate or the versions of a certificate from a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="7004a-111">Példák</span><span class="sxs-lookup"><span data-stu-id="7004a-111">EXAMPLES</span></span>

### <span data-ttu-id="7004a-112">Példa 1: tanúsítvány beszerzése</span><span class="sxs-lookup"><span data-stu-id="7004a-112">Example 1: Get a certificate</span></span>
```
PS C:\>Get-AzKeyVaultCertificate -VaultName "ContosoKV01" -Name "TestCert01"
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

<span data-ttu-id="7004a-113">Ez a parancs a TestCert01 nevű tanúsítványt a ContosoKV01 nevű kulcs-boltozattal kapja meg.</span><span class="sxs-lookup"><span data-stu-id="7004a-113">This command gets the certificate named TestCert01 from the key vault named ContosoKV01.</span></span>

### <span data-ttu-id="7004a-114">2. példa: az összes olyan tanúsítvány beszerzése, amelyet töröltek, de ez a kulcsfájl nem törlődik.</span><span class="sxs-lookup"><span data-stu-id="7004a-114">Example 2: Get all the certificates that have been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzKeyVaultCertificate -VaultName 'Contoso' -InRemovedState
```

<span data-ttu-id="7004a-115">Ez a parancs beilleszti a korábban törölt, de el nem távolított tanúsítványokat a contoso nevű fő boltozatba.</span><span class="sxs-lookup"><span data-stu-id="7004a-115">This command gets all the certificates that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="7004a-116">3. példa: beolvassa a MyCert, amelyet törölték, de erre a kulcsra nincs kitisztítva.</span><span class="sxs-lookup"><span data-stu-id="7004a-116">Example 3: Gets the certificate MyCert that has been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzKeyVaultCertificate -VaultName 'Contoso' -Name 'MyCert' -InRemovedState
```

<span data-ttu-id="7004a-117">Ez a parancs a contoso nevű kulcsfájl "MyCert" nevű tanúsítványát kapja meg, amelyet korábban törölt, de nem.</span><span class="sxs-lookup"><span data-stu-id="7004a-117">This command gets the certificate named 'MyCert' that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="7004a-118">Ez a parancs metaadatokat ad vissza, például a törlési dátumot, valamint a törölt tanúsítvány ütemezett végleges dátumát.</span><span class="sxs-lookup"><span data-stu-id="7004a-118">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted certificate.</span></span>

## <span data-ttu-id="7004a-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7004a-119">PARAMETERS</span></span>

### <span data-ttu-id="7004a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7004a-120">-DefaultProfile</span></span>
<span data-ttu-id="7004a-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="7004a-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7004a-122">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="7004a-122">-IncludeVersions</span></span>
<span data-ttu-id="7004a-123">Azt jelzi, hogy ez a művelet a tanúsítvány minden változatát bekapja.</span><span class="sxs-lookup"><span data-stu-id="7004a-123">Indicates that this operation gets all versions of the certificate.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByCertificateVersions
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7004a-124">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="7004a-124">-InRemovedState</span></span>
<span data-ttu-id="7004a-125">Annak megadása, hogy a kimenetben a korábban törölt tanúsítványokat szeretné-e szerepeltetni</span><span class="sxs-lookup"><span data-stu-id="7004a-125">Specifies whether to include previously deleted certificates in the output</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByDeletedCertificates
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7004a-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7004a-126">-Name</span></span>
<span data-ttu-id="7004a-127">A beolvasott tanúsítvány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7004a-127">Specifies the name of the certificate to get.</span></span>

```yaml
Type: String
Parameter Sets: ByCertificateName, ByCertificateVersions
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByDeletedCertificates
Aliases: CertificateName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7004a-128">-VaultName</span><span class="sxs-lookup"><span data-stu-id="7004a-128">-VaultName</span></span>
<span data-ttu-id="7004a-129">A kulcsfájl nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7004a-129">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="7004a-130">-Verzió</span><span class="sxs-lookup"><span data-stu-id="7004a-130">-Version</span></span>
<span data-ttu-id="7004a-131">A tanúsítvány verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="7004a-131">Specifies the version of a certificate.</span></span>

```yaml
Type: String
Parameter Sets: ByCertificateName
Aliases: CertificateVersion

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7004a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7004a-132">CommonParameters</span></span>
<span data-ttu-id="7004a-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7004a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7004a-134">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7004a-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7004a-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7004a-135">INPUTS</span></span>

### <span data-ttu-id="7004a-136">Nincs</span><span class="sxs-lookup"><span data-stu-id="7004a-136">None</span></span>
<span data-ttu-id="7004a-137">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="7004a-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7004a-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7004a-138">OUTPUTS</span></span>

### <span data-ttu-id="7004a-139">System. Collections. Generic. list ' 1 [Microsoft. Azure. commands. devault. models. CertificateIdentityItem]</span><span class="sxs-lookup"><span data-stu-id="7004a-139">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.KeyVault.Models.CertificateIdentityItem]</span></span>

### <span data-ttu-id="7004a-140">Microsoft. Azure. Command. KeyVaultCertificate. models.</span><span class="sxs-lookup"><span data-stu-id="7004a-140">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificate</span></span>

## <span data-ttu-id="7004a-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7004a-141">NOTES</span></span>

## <span data-ttu-id="7004a-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7004a-142">RELATED LINKS</span></span>

[<span data-ttu-id="7004a-143">Add-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="7004a-143">Add-AzKeyVaultCertificate</span></span>](./Add-AzKeyVaultCertificate.md)

[<span data-ttu-id="7004a-144">Importálás – AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="7004a-144">Import-AzKeyVaultCertificate</span></span>](./Import-AzKeyVaultCertificate.md)

[<span data-ttu-id="7004a-145">Remove-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="7004a-145">Remove-AzKeyVaultCertificate</span></span>](./Remove-AzKeyVaultCertificate.md)

[<span data-ttu-id="7004a-146">Visszavonás – AzKeyVaultSecretCertificate</span><span class="sxs-lookup"><span data-stu-id="7004a-146">Undo-AzKeyVaultSecretCertificate</span></span>](./Undo-AzKeyVaultSecretCertificate.md)
