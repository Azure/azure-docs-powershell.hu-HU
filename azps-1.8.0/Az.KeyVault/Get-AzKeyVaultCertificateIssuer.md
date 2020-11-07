---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 5F856280-C561-47B5-AA96-27E34C86D604
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateIssuer.md
ms.openlocfilehash: dc1ee6f168a417c612e01d02c93d8729cc2563af
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93835761"
---
# <span data-ttu-id="45d7f-101">Get-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="45d7f-101">Get-AzKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="45d7f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="45d7f-102">SYNOPSIS</span></span>
<span data-ttu-id="45d7f-103">Kinyeri a tanúsítványát a kulcs boltozatához.</span><span class="sxs-lookup"><span data-stu-id="45d7f-103">Gets a certificate issuer for a key vault.</span></span>

## <span data-ttu-id="45d7f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="45d7f-104">SYNTAX</span></span>

### <span data-ttu-id="45d7f-105">ByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="45d7f-105">ByName (Default)</span></span>
```
Get-AzKeyVaultCertificateIssuer [-VaultName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="45d7f-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="45d7f-106">ByInputObject</span></span>
```
Get-AzKeyVaultCertificateIssuer [-InputObject] <PSKeyVault> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="45d7f-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="45d7f-107">ByResourceId</span></span>
```
Get-AzKeyVaultCertificateIssuer [-ResourceId] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="45d7f-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="45d7f-108">DESCRIPTION</span></span>
<span data-ttu-id="45d7f-109">A **Get-AzKeyVaultCertificateIssuer** parancsmag a megadott tanúsítvány-kibocsátót vagy az összes tanúsítvány kibocsátóját bekapja az Azure Key Vault-ban.</span><span class="sxs-lookup"><span data-stu-id="45d7f-109">The **Get-AzKeyVaultCertificateIssuer** cmdlet gets a specified certificate issuer or all certificate issuers for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="45d7f-110">Példák</span><span class="sxs-lookup"><span data-stu-id="45d7f-110">EXAMPLES</span></span>

### <span data-ttu-id="45d7f-111">Példa 1: tanúsítvány kibocsátásának beszerzése</span><span class="sxs-lookup"><span data-stu-id="45d7f-111">Example 1: Get a certificate issuer</span></span>
```powershell
PS C:\> Get-AzKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01"

AccountId           : 555
ApiKey              :
OrganizationDetails : Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails
Name                : TestIssuer01
IssuerProvider      : Test
VaultName           : Contosokv01
```

<span data-ttu-id="45d7f-112">Ez a parancs a TestIssuer01 nevű tanúsítványt kapja meg.</span><span class="sxs-lookup"><span data-stu-id="45d7f-112">This command gets the certificate issuer named TestIssuer01.</span></span>

### <span data-ttu-id="45d7f-113">2. példa: a bizonyítvány-kibocsátók listája szűréssel</span><span class="sxs-lookup"><span data-stu-id="45d7f-113">Example 2: List certificate issuers using filtering</span></span>
```powershell
PS C:\> Get-AzKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "test*"

AccountId           : 555
ApiKey              :
OrganizationDetails : Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails
Name                : TestIssuer01
IssuerProvider      : Test
VaultName           : Contosokv01

AccountId           : 555
ApiKey              :
OrganizationDetails : Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails
Name                : TestIssuer02
IssuerProvider      : Test
VaultName           : Contosokv01
```

<span data-ttu-id="45d7f-114">Ez a parancs a "teszt" kezdetű tanúsítvány-kibocsátókat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="45d7f-114">This command gets the certificate issuers that start with "test".</span></span>

## <span data-ttu-id="45d7f-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="45d7f-115">PARAMETERS</span></span>

### <span data-ttu-id="45d7f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45d7f-116">-DefaultProfile</span></span>
<span data-ttu-id="45d7f-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="45d7f-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="45d7f-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="45d7f-118">-InputObject</span></span>
<span data-ttu-id="45d7f-119">A boltozat objektum.</span><span class="sxs-lookup"><span data-stu-id="45d7f-119">KeyVault object.</span></span>

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

### <span data-ttu-id="45d7f-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="45d7f-120">-Name</span></span>
<span data-ttu-id="45d7f-121">A beolvasott tanúsítvány nevének megadása.</span><span class="sxs-lookup"><span data-stu-id="45d7f-121">Specifies the name of the certificate issuer to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IssuerName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="45d7f-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="45d7f-122">-ResourceId</span></span>
<span data-ttu-id="45d7f-123">A főkészlet erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="45d7f-123">KeyVault Resource Id.</span></span>

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

### <span data-ttu-id="45d7f-124">-VaultName</span><span class="sxs-lookup"><span data-stu-id="45d7f-124">-VaultName</span></span>
<span data-ttu-id="45d7f-125">A kulcsfájl nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="45d7f-125">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="45d7f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45d7f-126">CommonParameters</span></span>
<span data-ttu-id="45d7f-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="45d7f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45d7f-128">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="45d7f-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45d7f-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="45d7f-129">INPUTS</span></span>

### <span data-ttu-id="45d7f-130">Microsoft. Azure. Command. PSKeyVault. models.</span><span class="sxs-lookup"><span data-stu-id="45d7f-130">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="45d7f-131">System. String</span><span class="sxs-lookup"><span data-stu-id="45d7f-131">System.String</span></span>

## <span data-ttu-id="45d7f-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="45d7f-132">OUTPUTS</span></span>

### <span data-ttu-id="45d7f-133">Microsoft. Azure. Command. PSKeyVaultCertificateIssuerIdentityItem. models.</span><span class="sxs-lookup"><span data-stu-id="45d7f-133">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem</span></span>

### <span data-ttu-id="45d7f-134">Microsoft. Azure. Command. PSKeyVaultCertificateIssuer. models.</span><span class="sxs-lookup"><span data-stu-id="45d7f-134">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="45d7f-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="45d7f-135">NOTES</span></span>

## <span data-ttu-id="45d7f-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="45d7f-136">RELATED LINKS</span></span>

[<span data-ttu-id="45d7f-137">Remove-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="45d7f-137">Remove-AzKeyVaultCertificateIssuer</span></span>](./Remove-AzKeyVaultCertificateIssuer.md)

[<span data-ttu-id="45d7f-138">Set-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="45d7f-138">Set-AzKeyVaultCertificateIssuer</span></span>](./Set-AzKeyVaultCertificateIssuer.md)


