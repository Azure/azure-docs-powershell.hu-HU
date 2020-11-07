---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 0729687C-3104-4136-A80D-16BAEBD6B76C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultcertificatepolicy
schema: 2.0.0
ms.openlocfilehash: 692c639ac42d0a8f2dc2bf121321dfc116ebce1b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849674"
---
# <span data-ttu-id="bb58a-101">Get-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="bb58a-101">Get-AzureKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="bb58a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bb58a-102">SYNOPSIS</span></span>
<span data-ttu-id="bb58a-103">Egy kulcshoz tartozó tanúsítvány házirendjét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="bb58a-103">Gets the policy for a certificate in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bb58a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bb58a-104">SYNTAX</span></span>

```
Get-AzureKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bb58a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="bb58a-105">DESCRIPTION</span></span>
<span data-ttu-id="bb58a-106">A **Get-AzureKeyVaultCertificatePolicy** parancsmag az Azure Key Vault-ban egy fő tárolóban kapja meg a tanúsítvány házirendjét.</span><span class="sxs-lookup"><span data-stu-id="bb58a-106">The **Get-AzureKeyVaultCertificatePolicy** cmdlet gets the policy for a certificate in a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="bb58a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="bb58a-107">EXAMPLES</span></span>

### <span data-ttu-id="bb58a-108">Példa 1: tanúsítvány-házirend beszerzése</span><span class="sxs-lookup"><span data-stu-id="bb58a-108">Example 1: Get a certificate policy</span></span>
```
PS C:\>Get-AzureKeyVaultCertificatePolicy -VaultName "ContosoKV01" -Name "TestCert01"
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
RenewAtNumberOfDaysBeforeExpiry : 
RenewAtPercentageLifetime       : 80
EmailOnly                       : False
Enabled                         : True
Created                         : 2/8/2016 11:10:29 PM
Updated                         : 2/8/2016 11:10:29 PM
```

<span data-ttu-id="bb58a-109">Ez a parancs beolvassa a TestCert01 tanúsítvány házirendjét a ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="bb58a-109">This command gets the certificate policy for TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="bb58a-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bb58a-110">PARAMETERS</span></span>

### <span data-ttu-id="bb58a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb58a-111">-DefaultProfile</span></span>
<span data-ttu-id="bb58a-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="bb58a-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bb58a-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="bb58a-113">-Name</span></span>
<span data-ttu-id="bb58a-114">A tanúsítvány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bb58a-114">Specifies the name of a certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb58a-115">-VaultName</span><span class="sxs-lookup"><span data-stu-id="bb58a-115">-VaultName</span></span>
<span data-ttu-id="bb58a-116">A kulcsfájl nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bb58a-116">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="bb58a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb58a-117">CommonParameters</span></span>
<span data-ttu-id="bb58a-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bb58a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb58a-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb58a-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb58a-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bb58a-120">INPUTS</span></span>

## <span data-ttu-id="bb58a-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bb58a-121">OUTPUTS</span></span>

### <span data-ttu-id="bb58a-122">Microsoft. Azure. Command. KeyVaultCertificatePolicy. models.</span><span class="sxs-lookup"><span data-stu-id="bb58a-122">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="bb58a-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bb58a-123">NOTES</span></span>

## <span data-ttu-id="bb58a-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bb58a-124">RELATED LINKS</span></span>

[<span data-ttu-id="bb58a-125">Új – AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="bb58a-125">New-AzureKeyVaultCertificatePolicy</span></span>](./New-AzureKeyVaultCertificatePolicy.md)

[<span data-ttu-id="bb58a-126">Set-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="bb58a-126">Set-AzureKeyVaultCertificatePolicy</span></span>](./Set-AzureKeyVaultCertificatePolicy.md)

