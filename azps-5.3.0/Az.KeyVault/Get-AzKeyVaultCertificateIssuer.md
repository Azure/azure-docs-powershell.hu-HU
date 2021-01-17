---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 5F856280-C561-47B5-AA96-27E34C86D604
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateIssuer.md
ms.openlocfilehash: d089cf44e14e70be8b377de310ab4a332ae2d1a1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469585"
---
# <span data-ttu-id="33567-101">Get-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="33567-101">Get-AzKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="33567-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="33567-102">SYNOPSIS</span></span>
<span data-ttu-id="33567-103">Tanúsítvány kibocsátóját kap egy kulcstárolóhoz.</span><span class="sxs-lookup"><span data-stu-id="33567-103">Gets a certificate issuer for a key vault.</span></span>

## <span data-ttu-id="33567-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="33567-104">SYNTAX</span></span>

### <span data-ttu-id="33567-105">ByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="33567-105">ByName (Default)</span></span>
```
Get-AzKeyVaultCertificateIssuer [-VaultName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="33567-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="33567-106">ByInputObject</span></span>
```
Get-AzKeyVaultCertificateIssuer [-InputObject] <PSKeyVault> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="33567-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="33567-107">ByResourceId</span></span>
```
Get-AzKeyVaultCertificateIssuer [-ResourceId] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="33567-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="33567-108">DESCRIPTION</span></span>
<span data-ttu-id="33567-109">A **Get-AzKeyVaultCertificateIssuer** parancsmag kap egy adott tanúsítványkibocsátót vagy az összes tanúsítványkibocsátót egy azure-kulcstár kulcstárolójában.</span><span class="sxs-lookup"><span data-stu-id="33567-109">The **Get-AzKeyVaultCertificateIssuer** cmdlet gets a specified certificate issuer or all certificate issuers for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="33567-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="33567-110">EXAMPLES</span></span>

### <span data-ttu-id="33567-111">1. példa: Tanúsítvány kibocsátójának kérelme</span><span class="sxs-lookup"><span data-stu-id="33567-111">Example 1: Get a certificate issuer</span></span>
```powershell
PS C:\> Get-AzKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01"

AccountId           : 555
ApiKey              :
OrganizationDetails : Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails
Name                : TestIssuer01
IssuerProvider      : Test
VaultName           : Contosokv01
```

<span data-ttu-id="33567-112">Ez a parancs a TestIssuer01 nevű tanúsítvány kibocsátóját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="33567-112">This command gets the certificate issuer named TestIssuer01.</span></span>

### <span data-ttu-id="33567-113">2. példa: A tanúsítvány kibocsátójának felsorolása szűrés használatával</span><span class="sxs-lookup"><span data-stu-id="33567-113">Example 2: List certificate issuers using filtering</span></span>
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

<span data-ttu-id="33567-114">Ez a parancs a "teszt" kezdettől indulva kapja meg a tanúsítványkibocsátókat.</span><span class="sxs-lookup"><span data-stu-id="33567-114">This command gets the certificate issuers that start with "test".</span></span>

## <span data-ttu-id="33567-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="33567-115">PARAMETERS</span></span>

### <span data-ttu-id="33567-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33567-116">-DefaultProfile</span></span>
<span data-ttu-id="33567-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="33567-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="33567-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="33567-118">-InputObject</span></span>
<span data-ttu-id="33567-119">KeyVault objektum.</span><span class="sxs-lookup"><span data-stu-id="33567-119">KeyVault object.</span></span>

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

### <span data-ttu-id="33567-120">-Name</span><span class="sxs-lookup"><span data-stu-id="33567-120">-Name</span></span>
<span data-ttu-id="33567-121">Megadja a bekérni szükséges tanúsítvány kibocsátójának nevét.</span><span class="sxs-lookup"><span data-stu-id="33567-121">Specifies the name of the certificate issuer to get.</span></span>

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

### <span data-ttu-id="33567-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="33567-122">-ResourceId</span></span>
<span data-ttu-id="33567-123">KeyVault-erőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="33567-123">KeyVault Resource Id.</span></span>

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

### <span data-ttu-id="33567-124">-VaultName</span><span class="sxs-lookup"><span data-stu-id="33567-124">-VaultName</span></span>
<span data-ttu-id="33567-125">Egy kulcstár nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="33567-125">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="33567-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33567-126">CommonParameters</span></span>
<span data-ttu-id="33567-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33567-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33567-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="33567-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33567-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="33567-129">INPUTS</span></span>

### <span data-ttu-id="33567-130">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="33567-130">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="33567-131">System.String</span><span class="sxs-lookup"><span data-stu-id="33567-131">System.String</span></span>

## <span data-ttu-id="33567-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="33567-132">OUTPUTS</span></span>

### <span data-ttu-id="33567-133">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem</span><span class="sxs-lookup"><span data-stu-id="33567-133">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem</span></span>

### <span data-ttu-id="33567-134">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="33567-134">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="33567-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="33567-135">NOTES</span></span>

## <span data-ttu-id="33567-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="33567-136">RELATED LINKS</span></span>

[<span data-ttu-id="33567-137">Remove-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="33567-137">Remove-AzKeyVaultCertificateIssuer</span></span>](./Remove-AzKeyVaultCertificateIssuer.md)

[<span data-ttu-id="33567-138">Set-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="33567-138">Set-AzKeyVaultCertificateIssuer</span></span>](./Set-AzKeyVaultCertificateIssuer.md)


