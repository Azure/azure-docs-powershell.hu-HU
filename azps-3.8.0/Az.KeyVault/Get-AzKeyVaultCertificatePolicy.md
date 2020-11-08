---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 0729687C-3104-4136-A80D-16BAEBD6B76C
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificatePolicy.md
ms.openlocfilehash: d6e2225cc7441d4c370d990aa45c9b2c2bb40457
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94010692"
---
# <span data-ttu-id="4af10-101">Get-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="4af10-101">Get-AzKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="4af10-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4af10-102">SYNOPSIS</span></span>
<span data-ttu-id="4af10-103">Egy kulcshoz tartozó tanúsítvány házirendjét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="4af10-103">Gets the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="4af10-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4af10-104">SYNTAX</span></span>

### <span data-ttu-id="4af10-105">VaultAndCertName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4af10-105">VaultAndCertName (Default)</span></span>
```
Get-AzKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4af10-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="4af10-106">InputObject</span></span>
```
Get-AzKeyVaultCertificatePolicy [-InputObject] <PSKeyVaultCertificateIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4af10-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="4af10-107">DESCRIPTION</span></span>
<span data-ttu-id="4af10-108">A **Get-AzKeyVaultCertificatePolicy** parancsmag az Azure Key Vault-ban egy fő tárolóban kapja meg a tanúsítvány házirendjét.</span><span class="sxs-lookup"><span data-stu-id="4af10-108">The **Get-AzKeyVaultCertificatePolicy** cmdlet gets the policy for a certificate in a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="4af10-109">Példák</span><span class="sxs-lookup"><span data-stu-id="4af10-109">EXAMPLES</span></span>

### <span data-ttu-id="4af10-110">Példa 1: tanúsítvány-házirend beszerzése</span><span class="sxs-lookup"><span data-stu-id="4af10-110">Example 1: Get a certificate policy</span></span>
```powershell
PS C:\ >Get-AzKeyVaultCertificatePolicy -VaultName "ContosoKV01" -Name "TestCert01"

SecretContentType               : application/x-pkcs12
Kty                             : RSA
KeySize                         : 2048
Exportable                      : True
ReuseKeyOnRenewal               : True
SubjectName                     : CN=contoso.com
DnsNames                        : 
Ekus                            : {1.3.6.1.5.5.7.3.1, 1.3.6.1.5.5.7.3.2}
ValidityInMonths                : 6
IssuerName                      : Self
CertificateType                 :
RenewAtNumberOfDaysBeforeExpiry : 
RenewAtPercentageLifetime       : 80
EmailAtNumberOfDaysBeforeExpiry :
EmailAtPercentageLifetime       :
Enabled                         : True
Created                         : 2/8/2016 11:10:29 PM
Updated                         : 2/8/2016 11:10:29 PM
```

<span data-ttu-id="4af10-111">Ez a parancs beolvassa a TestCert01 tanúsítvány házirendjét a ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="4af10-111">This command gets the certificate policy for TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="4af10-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4af10-112">PARAMETERS</span></span>

### <span data-ttu-id="4af10-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4af10-113">-DefaultProfile</span></span>
<span data-ttu-id="4af10-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="4af10-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4af10-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4af10-115">-InputObject</span></span>
<span data-ttu-id="4af10-116">Certificate objektum.</span><span class="sxs-lookup"><span data-stu-id="4af10-116">Certificate Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4af10-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4af10-117">-Name</span></span>
<span data-ttu-id="4af10-118">A tanúsítvány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4af10-118">Specifies the name of a certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: VaultAndCertName
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4af10-119">-VaultName</span><span class="sxs-lookup"><span data-stu-id="4af10-119">-VaultName</span></span>
<span data-ttu-id="4af10-120">A kulcsfájl nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4af10-120">Specifies the name of a key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: VaultAndCertName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4af10-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4af10-121">CommonParameters</span></span>
<span data-ttu-id="4af10-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4af10-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4af10-123">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="4af10-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4af10-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4af10-124">INPUTS</span></span>

### <span data-ttu-id="4af10-125">Microsoft. Azure. Command. PSKeyVaultCertificateIdentityItem. models.</span><span class="sxs-lookup"><span data-stu-id="4af10-125">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span></span>

## <span data-ttu-id="4af10-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4af10-126">OUTPUTS</span></span>

### <span data-ttu-id="4af10-127">Microsoft. Azure. Command. PSKeyVaultCertificatePolicy. models.</span><span class="sxs-lookup"><span data-stu-id="4af10-127">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="4af10-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4af10-128">NOTES</span></span>

## <span data-ttu-id="4af10-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4af10-129">RELATED LINKS</span></span>

[<span data-ttu-id="4af10-130">Új – AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="4af10-130">New-AzKeyVaultCertificatePolicy</span></span>](./New-AzKeyVaultCertificatePolicy.md)

[<span data-ttu-id="4af10-131">Set-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="4af10-131">Set-AzKeyVaultCertificatePolicy</span></span>](./Set-AzKeyVaultCertificatePolicy.md)

