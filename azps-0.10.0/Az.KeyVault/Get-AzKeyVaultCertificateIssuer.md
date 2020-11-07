---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 5F856280-C561-47B5-AA96-27E34C86D604
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/get-AzKeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateIssuer.md
ms.openlocfilehash: b9188e1bb4d5de4896bf0ca3b2844c7718593ca2
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842154"
---
# <span data-ttu-id="aadb8-101">Get-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="aadb8-101">Get-AzKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="aadb8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="aadb8-102">SYNOPSIS</span></span>
<span data-ttu-id="aadb8-103">Kinyeri a tanúsítványát a kulcs boltozatához.</span><span class="sxs-lookup"><span data-stu-id="aadb8-103">Gets a certificate issuer for a key vault.</span></span>

## <span data-ttu-id="aadb8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="aadb8-104">SYNTAX</span></span>

### <span data-ttu-id="aadb8-105">ByVaultName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="aadb8-105">ByVaultName (Default)</span></span>
```
Get-AzKeyVaultCertificateIssuer [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="aadb8-106">ByName</span><span class="sxs-lookup"><span data-stu-id="aadb8-106">ByName</span></span>
```
Get-AzKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aadb8-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="aadb8-107">DESCRIPTION</span></span>
<span data-ttu-id="aadb8-108">A **Get-AzKeyVaultCertificateIssuer** parancsmag a megadott tanúsítvány-kibocsátót vagy az összes tanúsítvány kibocsátóját bekapja az Azure Key Vault-ban.</span><span class="sxs-lookup"><span data-stu-id="aadb8-108">The **Get-AzKeyVaultCertificateIssuer** cmdlet gets a specified certificate issuer or all certificate issuers for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="aadb8-109">Példák</span><span class="sxs-lookup"><span data-stu-id="aadb8-109">EXAMPLES</span></span>

### <span data-ttu-id="aadb8-110">Példa 1: tanúsítvány kibocsátásának beszerzése</span><span class="sxs-lookup"><span data-stu-id="aadb8-110">Example 1: Get a certificate issuer</span></span>
```
PS C:\>Get-AzKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01"
Name                : TestIssuer01
IssuerProvider      : Test
AccountId           : 555
ApiKey              : 
OrganizationDetails : Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateOrganizationDetails
```

<span data-ttu-id="aadb8-111">Ez a parancs a TestIssuer01 nevű tanúsítványt kapja meg.</span><span class="sxs-lookup"><span data-stu-id="aadb8-111">This command gets the certificate issuer named TestIssuer01.</span></span>

## <span data-ttu-id="aadb8-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="aadb8-112">PARAMETERS</span></span>

### <span data-ttu-id="aadb8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aadb8-113">-DefaultProfile</span></span>
<span data-ttu-id="aadb8-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="aadb8-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="aadb8-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="aadb8-115">-Name</span></span>
<span data-ttu-id="aadb8-116">A beolvasott tanúsítvány nevének megadása.</span><span class="sxs-lookup"><span data-stu-id="aadb8-116">Specifies the name of the certificate issuer to get.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: IssuerName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aadb8-117">-VaultName</span><span class="sxs-lookup"><span data-stu-id="aadb8-117">-VaultName</span></span>
<span data-ttu-id="aadb8-118">A kulcsfájl nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="aadb8-118">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="aadb8-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aadb8-119">CommonParameters</span></span>
<span data-ttu-id="aadb8-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="aadb8-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aadb8-121">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aadb8-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aadb8-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="aadb8-122">INPUTS</span></span>

### <span data-ttu-id="aadb8-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="aadb8-123">None</span></span>
<span data-ttu-id="aadb8-124">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="aadb8-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="aadb8-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="aadb8-125">OUTPUTS</span></span>

### <span data-ttu-id="aadb8-126">Lista<Microsoft. Azure. commands. CertificateIssuerIdentityItem. modellek.>, Microsoft. Azure. Command. KeyVaultCertificateIssuer. models.</span><span class="sxs-lookup"><span data-stu-id="aadb8-126">List<Microsoft.Azure.Commands.KeyVault.Models.CertificateIssuerIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="aadb8-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="aadb8-127">NOTES</span></span>

## <span data-ttu-id="aadb8-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="aadb8-128">RELATED LINKS</span></span>

[<span data-ttu-id="aadb8-129">Remove-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="aadb8-129">Remove-AzKeyVaultCertificateIssuer</span></span>](./Remove-AzKeyVaultCertificateIssuer.md)

[<span data-ttu-id="aadb8-130">Set-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="aadb8-130">Set-AzKeyVaultCertificateIssuer</span></span>](./Set-AzKeyVaultCertificateIssuer.md)


