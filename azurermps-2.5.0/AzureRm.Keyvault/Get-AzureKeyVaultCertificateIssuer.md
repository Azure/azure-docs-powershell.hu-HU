---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 5F856280-C561-47B5-AA96-27E34C86D604
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultcertificateissuer
schema: 2.0.0
ms.openlocfilehash: fcbb19936bb9924f95aa3a20fa026a9c8c723033
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849678"
---
# <span data-ttu-id="76066-101">Get-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="76066-101">Get-AzureKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="76066-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="76066-102">SYNOPSIS</span></span>
<span data-ttu-id="76066-103">Kinyeri a tanúsítványát a kulcs boltozatához.</span><span class="sxs-lookup"><span data-stu-id="76066-103">Gets a certificate issuer for a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="76066-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="76066-104">SYNTAX</span></span>

### <span data-ttu-id="76066-105">ByVaultName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="76066-105">ByVaultName (Default)</span></span>
```
Get-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="76066-106">ByName</span><span class="sxs-lookup"><span data-stu-id="76066-106">ByName</span></span>
```
Get-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="76066-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="76066-107">DESCRIPTION</span></span>
<span data-ttu-id="76066-108">A **Get-AzureKeyVaultCertificateIssuer** parancsmag a megadott tanúsítvány-kibocsátót vagy az összes tanúsítvány kibocsátóját bekapja az Azure Key Vault-ban.</span><span class="sxs-lookup"><span data-stu-id="76066-108">The **Get-AzureKeyVaultCertificateIssuer** cmdlet gets a specified certificate issuer or all certificate issuers for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="76066-109">Példák</span><span class="sxs-lookup"><span data-stu-id="76066-109">EXAMPLES</span></span>

### <span data-ttu-id="76066-110">Példa 1: tanúsítvány kibocsátásának beszerzése</span><span class="sxs-lookup"><span data-stu-id="76066-110">Example 1: Get a certificate issuer</span></span>
```
PS C:\>Get-AzureKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01"
Name                : TestIssuer01
IssuerProvider      : Test
AccountId           : 555
ApiKey              : 
OrganizationDetails : Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateOrganizationDetails
```

<span data-ttu-id="76066-111">Ez a parancs a TestIssuer01 nevű tanúsítványt kapja meg.</span><span class="sxs-lookup"><span data-stu-id="76066-111">This command gets the certificate issuer named TestIssuer01.</span></span>

## <span data-ttu-id="76066-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="76066-112">PARAMETERS</span></span>

### <span data-ttu-id="76066-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76066-113">-DefaultProfile</span></span>
<span data-ttu-id="76066-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="76066-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="76066-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="76066-115">-Name</span></span>
<span data-ttu-id="76066-116">A beolvasott tanúsítvány nevének megadása.</span><span class="sxs-lookup"><span data-stu-id="76066-116">Specifies the name of the certificate issuer to get.</span></span>

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

### <span data-ttu-id="76066-117">-VaultName</span><span class="sxs-lookup"><span data-stu-id="76066-117">-VaultName</span></span>
<span data-ttu-id="76066-118">A kulcsfájl nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="76066-118">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="76066-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76066-119">CommonParameters</span></span>
<span data-ttu-id="76066-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="76066-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76066-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76066-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76066-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="76066-122">INPUTS</span></span>

## <span data-ttu-id="76066-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="76066-123">OUTPUTS</span></span>

### <span data-ttu-id="76066-124">Lista<Microsoft. Azure. commands. CertificateIssuerIdentityItem. modellek.>, Microsoft. Azure. Command. KeyVaultCertificateIssuer. models.</span><span class="sxs-lookup"><span data-stu-id="76066-124">List<Microsoft.Azure.Commands.KeyVault.Models.CertificateIssuerIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="76066-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="76066-125">NOTES</span></span>

## <span data-ttu-id="76066-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="76066-126">RELATED LINKS</span></span>

[<span data-ttu-id="76066-127">Remove-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="76066-127">Remove-AzureKeyVaultCertificateIssuer</span></span>](./Remove-AzureKeyVaultCertificateIssuer.md)

[<span data-ttu-id="76066-128">Set-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="76066-128">Set-AzureKeyVaultCertificateIssuer</span></span>](./Set-AzureKeyVaultCertificateIssuer.md)


