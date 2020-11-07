---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 5F856280-C561-47B5-AA96-27E34C86D604
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateIssuer.md
ms.openlocfilehash: 83e81e479807c3eada25456d53521dfcecd81f40
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679562"
---
# <span data-ttu-id="af706-101">Get-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="af706-101">Get-AzureKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="af706-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="af706-102">SYNOPSIS</span></span>
<span data-ttu-id="af706-103">Kinyeri a tanúsítványát a kulcs boltozatához.</span><span class="sxs-lookup"><span data-stu-id="af706-103">Gets a certificate issuer for a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="af706-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="af706-104">SYNTAX</span></span>

### <span data-ttu-id="af706-105">ByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="af706-105">ByName (Default)</span></span>
```
Get-AzureKeyVaultCertificateIssuer [-VaultName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="af706-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="af706-106">ByInputObject</span></span>
```
Get-AzureKeyVaultCertificateIssuer [-InputObject] <PSKeyVault> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="af706-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="af706-107">ByResourceId</span></span>
```
Get-AzureKeyVaultCertificateIssuer [-ResourceId] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="af706-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="af706-108">DESCRIPTION</span></span>
<span data-ttu-id="af706-109">A **Get-AzureKeyVaultCertificateIssuer** parancsmag a megadott tanúsítvány-kibocsátót vagy az összes tanúsítvány kibocsátóját bekapja az Azure Key Vault-ban.</span><span class="sxs-lookup"><span data-stu-id="af706-109">The **Get-AzureKeyVaultCertificateIssuer** cmdlet gets a specified certificate issuer or all certificate issuers for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="af706-110">Példák</span><span class="sxs-lookup"><span data-stu-id="af706-110">EXAMPLES</span></span>

### <span data-ttu-id="af706-111">Példa 1: tanúsítvány kibocsátásának beszerzése</span><span class="sxs-lookup"><span data-stu-id="af706-111">Example 1: Get a certificate issuer</span></span>
```powershell
PS C:\> Get-AzureKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01"

AccountId           : 555
ApiKey              :
OrganizationDetails : Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails
Name                : TestIssuer01
IssuerProvider      : Test
VaultName           : Contosokv01
```

<span data-ttu-id="af706-112">Ez a parancs a TestIssuer01 nevű tanúsítványt kapja meg.</span><span class="sxs-lookup"><span data-stu-id="af706-112">This command gets the certificate issuer named TestIssuer01.</span></span>

## <span data-ttu-id="af706-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="af706-113">PARAMETERS</span></span>

### <span data-ttu-id="af706-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af706-114">-DefaultProfile</span></span>
<span data-ttu-id="af706-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="af706-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="af706-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="af706-116">-InputObject</span></span>
<span data-ttu-id="af706-117">A boltozat objektum.</span><span class="sxs-lookup"><span data-stu-id="af706-117">KeyVault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="af706-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="af706-118">-Name</span></span>
<span data-ttu-id="af706-119">A beolvasott tanúsítvány nevének megadása.</span><span class="sxs-lookup"><span data-stu-id="af706-119">Specifies the name of the certificate issuer to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IssuerName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af706-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="af706-120">-ResourceId</span></span>
<span data-ttu-id="af706-121">A főkészlet erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="af706-121">KeyVault Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af706-122">-VaultName</span><span class="sxs-lookup"><span data-stu-id="af706-122">-VaultName</span></span>
<span data-ttu-id="af706-123">A kulcsfájl nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="af706-123">Specifies the name of a key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af706-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af706-124">CommonParameters</span></span>
<span data-ttu-id="af706-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="af706-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af706-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af706-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af706-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="af706-127">INPUTS</span></span>

### <span data-ttu-id="af706-128">Microsoft. Azure. Command. PSKeyVault. models.</span><span class="sxs-lookup"><span data-stu-id="af706-128">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>
<span data-ttu-id="af706-129">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="af706-129">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="af706-130">System. String</span><span class="sxs-lookup"><span data-stu-id="af706-130">System.String</span></span>

## <span data-ttu-id="af706-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="af706-131">OUTPUTS</span></span>

### <span data-ttu-id="af706-132">Microsoft. Azure. Command. PSKeyVaultCertificateIssuerIdentityItem. models.</span><span class="sxs-lookup"><span data-stu-id="af706-132">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem</span></span>

### <span data-ttu-id="af706-133">Microsoft. Azure. Command. PSKeyVaultCertificateIssuer. models.</span><span class="sxs-lookup"><span data-stu-id="af706-133">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="af706-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="af706-134">NOTES</span></span>

## <span data-ttu-id="af706-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="af706-135">RELATED LINKS</span></span>

[<span data-ttu-id="af706-136">Remove-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="af706-136">Remove-AzureKeyVaultCertificateIssuer</span></span>](./Remove-AzureKeyVaultCertificateIssuer.md)

[<span data-ttu-id="af706-137">Set-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="af706-137">Set-AzureKeyVaultCertificateIssuer</span></span>](./Set-AzureKeyVaultCertificateIssuer.md)


