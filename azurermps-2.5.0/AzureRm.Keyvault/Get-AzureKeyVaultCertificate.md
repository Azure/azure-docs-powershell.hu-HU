---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 363FA51E-D075-4800-A4BE-BFF63FD25C90
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultcertificate
schema: 2.0.0
ms.openlocfilehash: ed52e229f114666782cb24388db585fd08fa685b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850410"
---
# <span data-ttu-id="b1a78-101">Get-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="b1a78-101">Get-AzureKeyVaultCertificate</span></span>

## <span data-ttu-id="b1a78-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b1a78-102">SYNOPSIS</span></span>
<span data-ttu-id="b1a78-103">Egy kulcsos boltozattól kapja a tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="b1a78-103">Gets a certificate from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b1a78-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b1a78-104">SYNTAX</span></span>

### <span data-ttu-id="b1a78-105">ByVaultName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b1a78-105">ByVaultName (Default)</span></span>
```
Get-AzureKeyVaultCertificate [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b1a78-106">ByCertificateName</span><span class="sxs-lookup"><span data-stu-id="b1a78-106">ByCertificateName</span></span>
```
Get-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b1a78-107">ByCertificateVersions</span><span class="sxs-lookup"><span data-stu-id="b1a78-107">ByCertificateVersions</span></span>
```
Get-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b1a78-108">ByDeletedCertificates</span><span class="sxs-lookup"><span data-stu-id="b1a78-108">ByDeletedCertificates</span></span>
```
Get-AzureKeyVaultCertificate [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b1a78-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="b1a78-109">DESCRIPTION</span></span>
<span data-ttu-id="b1a78-110">A **Get-AzureKeyVaultCertificate** parancsmag az Azure Key Vault-ban a megadott tanúsítványt vagy egy tanúsítvány verziószámát kapja.</span><span class="sxs-lookup"><span data-stu-id="b1a78-110">The **Get-AzureKeyVaultCertificate** cmdlet gets the specified certificate or the versions of a certificate from a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="b1a78-111">Példák</span><span class="sxs-lookup"><span data-stu-id="b1a78-111">EXAMPLES</span></span>

### <span data-ttu-id="b1a78-112">Példa 1: tanúsítvány beszerzése</span><span class="sxs-lookup"><span data-stu-id="b1a78-112">Example 1: Get a certificate</span></span>
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

<span data-ttu-id="b1a78-113">Ez a parancs a TestCert01 nevű tanúsítványt a ContosoKV01 nevű kulcs-boltozattal kapja meg.</span><span class="sxs-lookup"><span data-stu-id="b1a78-113">This command gets the certificate named TestCert01 from the key vault named ContosoKV01.</span></span>

### <span data-ttu-id="b1a78-114">2. példa: az összes olyan tanúsítvány beszerzése, amelyet töröltek, de ez a kulcsfájl nem törlődik.</span><span class="sxs-lookup"><span data-stu-id="b1a78-114">Example 2: Get all the certificates that have been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzureKeyVaultCertificate -VaultName 'Contoso' -InRemovedState
```

<span data-ttu-id="b1a78-115">Ez a parancs beilleszti a korábban törölt, de el nem távolított tanúsítványokat a contoso nevű fő boltozatba.</span><span class="sxs-lookup"><span data-stu-id="b1a78-115">This command gets all the certificates that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="b1a78-116">3. példa: beolvassa a MyCert, amelyet törölték, de erre a kulcsra nincs kitisztítva.</span><span class="sxs-lookup"><span data-stu-id="b1a78-116">Example 3: Gets the certificate MyCert that has been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzureKeyVaultCertificate -VaultName 'Contoso' -Name 'MyCert' -InRemovedState
```

<span data-ttu-id="b1a78-117">Ez a parancs a contoso nevű kulcsfájl "MyCert" nevű tanúsítványát kapja meg, amelyet korábban törölt, de nem.</span><span class="sxs-lookup"><span data-stu-id="b1a78-117">This command gets the certificate named 'MyCert' that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="b1a78-118">Ez a parancs metaadatokat ad vissza, például a törlési dátumot, valamint a törölt tanúsítvány ütemezett végleges dátumát.</span><span class="sxs-lookup"><span data-stu-id="b1a78-118">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted certificate.</span></span>

## <span data-ttu-id="b1a78-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b1a78-119">PARAMETERS</span></span>

### <span data-ttu-id="b1a78-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1a78-120">-DefaultProfile</span></span>
<span data-ttu-id="b1a78-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="b1a78-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b1a78-122">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="b1a78-122">-IncludeVersions</span></span>
<span data-ttu-id="b1a78-123">Azt jelzi, hogy ez a művelet a tanúsítvány minden változatát bekapja.</span><span class="sxs-lookup"><span data-stu-id="b1a78-123">Indicates that this operation gets all versions of the certificate.</span></span>

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

### <span data-ttu-id="b1a78-124">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="b1a78-124">-InRemovedState</span></span>
<span data-ttu-id="b1a78-125">Annak megadása, hogy a kimenetben a korábban törölt tanúsítványokat szeretné-e szerepeltetni</span><span class="sxs-lookup"><span data-stu-id="b1a78-125">Specifies whether to include previously deleted certificates in the output</span></span>

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

### <span data-ttu-id="b1a78-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b1a78-126">-Name</span></span>
<span data-ttu-id="b1a78-127">A beolvasott tanúsítvány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b1a78-127">Specifies the name of the certificate to get.</span></span>

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

### <span data-ttu-id="b1a78-128">-VaultName</span><span class="sxs-lookup"><span data-stu-id="b1a78-128">-VaultName</span></span>
<span data-ttu-id="b1a78-129">A kulcsfájl nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b1a78-129">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="b1a78-130">-Verzió</span><span class="sxs-lookup"><span data-stu-id="b1a78-130">-Version</span></span>
<span data-ttu-id="b1a78-131">A tanúsítvány verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="b1a78-131">Specifies the version of a certificate.</span></span>

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

### <span data-ttu-id="b1a78-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1a78-132">CommonParameters</span></span>
<span data-ttu-id="b1a78-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b1a78-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1a78-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1a78-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1a78-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b1a78-135">INPUTS</span></span>

## <span data-ttu-id="b1a78-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b1a78-136">OUTPUTS</span></span>

### <span data-ttu-id="b1a78-137">System. Collections. Generic. list ' 1 [Microsoft. Azure. commands. devault. models. CertificateIdentityItem]</span><span class="sxs-lookup"><span data-stu-id="b1a78-137">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.KeyVault.Models.CertificateIdentityItem]</span></span>

### <span data-ttu-id="b1a78-138">Microsoft. Azure. Command. KeyVaultCertificate. models.</span><span class="sxs-lookup"><span data-stu-id="b1a78-138">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificate</span></span>

## <span data-ttu-id="b1a78-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b1a78-139">NOTES</span></span>

## <span data-ttu-id="b1a78-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b1a78-140">RELATED LINKS</span></span>

[<span data-ttu-id="b1a78-141">Add-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="b1a78-141">Add-AzureKeyVaultCertificate</span></span>](./Add-AzureKeyVaultCertificate.md)

[<span data-ttu-id="b1a78-142">Importálás – AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="b1a78-142">Import-AzureKeyVaultCertificate</span></span>](./Import-AzureKeyVaultCertificate.md)

[<span data-ttu-id="b1a78-143">Remove-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="b1a78-143">Remove-AzureKeyVaultCertificate</span></span>](./Remove-AzureKeyVaultCertificate.md)


