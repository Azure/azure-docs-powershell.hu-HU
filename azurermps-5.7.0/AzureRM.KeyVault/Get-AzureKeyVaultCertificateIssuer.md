---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 5F856280-C561-47B5-AA96-27E34C86D604
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateIssuer.md
ms.openlocfilehash: f19fa119bf307724fb318e0a1d9a390190523bd1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494484"
---
# <span data-ttu-id="25278-101">Get-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="25278-101">Get-AzureKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="25278-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="25278-102">SYNOPSIS</span></span>
<span data-ttu-id="25278-103">Kinyeri a tanúsítványát a kulcs boltozatához.</span><span class="sxs-lookup"><span data-stu-id="25278-103">Gets a certificate issuer for a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="25278-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="25278-104">SYNTAX</span></span>

### <span data-ttu-id="25278-105">ByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="25278-105">ByName (Default)</span></span>
```
Get-AzureKeyVaultCertificateIssuer [-VaultName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="25278-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="25278-106">ByInputObject</span></span>
```
Get-AzureKeyVaultCertificateIssuer [-InputObject] <PSKeyVault> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="25278-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="25278-107">DESCRIPTION</span></span>
<span data-ttu-id="25278-108">A **Get-AzureKeyVaultCertificateIssuer** parancsmag a megadott tanúsítvány-kibocsátót vagy az összes tanúsítvány kibocsátóját bekapja az Azure Key Vault-ban.</span><span class="sxs-lookup"><span data-stu-id="25278-108">The **Get-AzureKeyVaultCertificateIssuer** cmdlet gets a specified certificate issuer or all certificate issuers for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="25278-109">Példák</span><span class="sxs-lookup"><span data-stu-id="25278-109">EXAMPLES</span></span>

### <span data-ttu-id="25278-110">Példa 1: tanúsítvány kibocsátásának beszerzése</span><span class="sxs-lookup"><span data-stu-id="25278-110">Example 1: Get a certificate issuer</span></span>
```
PS C:\>Get-AzureKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01"
Name                : TestIssuer01
IssuerProvider      : Test
AccountId           : 555
ApiKey              : 
OrganizationDetails : Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateOrganizationDetails
```

<span data-ttu-id="25278-111">Ez a parancs a TestIssuer01 nevű tanúsítványt kapja meg.</span><span class="sxs-lookup"><span data-stu-id="25278-111">This command gets the certificate issuer named TestIssuer01.</span></span>

## <span data-ttu-id="25278-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="25278-112">PARAMETERS</span></span>

### <span data-ttu-id="25278-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25278-113">-DefaultProfile</span></span>
<span data-ttu-id="25278-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="25278-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="25278-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="25278-115">-InputObject</span></span>
<span data-ttu-id="25278-116">A boltozat objektum.</span><span class="sxs-lookup"><span data-stu-id="25278-116">KeyVault object.</span></span>

```yaml
Type: PSKeyVault
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="25278-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="25278-117">-Name</span></span>
<span data-ttu-id="25278-118">A beolvasott tanúsítvány nevének megadása.</span><span class="sxs-lookup"><span data-stu-id="25278-118">Specifies the name of the certificate issuer to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IssuerName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25278-119">-VaultName</span><span class="sxs-lookup"><span data-stu-id="25278-119">-VaultName</span></span>
<span data-ttu-id="25278-120">A kulcsfájl nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="25278-120">Specifies the name of a key vault.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25278-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25278-121">CommonParameters</span></span>
<span data-ttu-id="25278-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="25278-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25278-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25278-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25278-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="25278-124">INPUTS</span></span>

### <span data-ttu-id="25278-125">Nincs</span><span class="sxs-lookup"><span data-stu-id="25278-125">None</span></span>
<span data-ttu-id="25278-126">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="25278-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="25278-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="25278-127">OUTPUTS</span></span>

### <span data-ttu-id="25278-128">Lista<Microsoft. Azure. commands. PSKeyVaultCertificateIssuerIdentityItem. modellek.>, Microsoft. Azure. Command. PSKeyVaultCertificateIssuer. models.</span><span class="sxs-lookup"><span data-stu-id="25278-128">List<Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="25278-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="25278-129">NOTES</span></span>

## <span data-ttu-id="25278-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="25278-130">RELATED LINKS</span></span>

[<span data-ttu-id="25278-131">Remove-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="25278-131">Remove-AzureKeyVaultCertificateIssuer</span></span>](./Remove-AzureKeyVaultCertificateIssuer.md)

[<span data-ttu-id="25278-132">Set-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="25278-132">Set-AzureKeyVaultCertificateIssuer</span></span>](./Set-AzureKeyVaultCertificateIssuer.md)


