---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 0729687C-3104-4136-A80D-16BAEBD6B76C
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/get-AzKeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificatePolicy.md
ms.openlocfilehash: d525a47dde9551e5d48c7c316cf6844323b75e81
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842142"
---
# <span data-ttu-id="75a80-101">Get-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="75a80-101">Get-AzKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="75a80-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="75a80-102">SYNOPSIS</span></span>
<span data-ttu-id="75a80-103">Egy kulcshoz tartozó tanúsítvány házirendjét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="75a80-103">Gets the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="75a80-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="75a80-104">SYNTAX</span></span>

```
Get-AzKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="75a80-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="75a80-105">DESCRIPTION</span></span>
<span data-ttu-id="75a80-106">A **Get-AzKeyVaultCertificatePolicy** parancsmag az Azure Key Vault-ban egy fő tárolóban kapja meg a tanúsítvány házirendjét.</span><span class="sxs-lookup"><span data-stu-id="75a80-106">The **Get-AzKeyVaultCertificatePolicy** cmdlet gets the policy for a certificate in a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="75a80-107">Példák</span><span class="sxs-lookup"><span data-stu-id="75a80-107">EXAMPLES</span></span>

### <span data-ttu-id="75a80-108">Példa 1: tanúsítvány-házirend beszerzése</span><span class="sxs-lookup"><span data-stu-id="75a80-108">Example 1: Get a certificate policy</span></span>
```
PS C:\>Get-AzKeyVaultCertificatePolicy -VaultName "ContosoKV01" -Name "TestCert01"
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

<span data-ttu-id="75a80-109">Ez a parancs beolvassa a TestCert01 tanúsítvány házirendjét a ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="75a80-109">This command gets the certificate policy for TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="75a80-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="75a80-110">PARAMETERS</span></span>

### <span data-ttu-id="75a80-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75a80-111">-DefaultProfile</span></span>
<span data-ttu-id="75a80-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="75a80-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="75a80-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="75a80-113">-Name</span></span>
<span data-ttu-id="75a80-114">A tanúsítvány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="75a80-114">Specifies the name of a certificate.</span></span>

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

### <span data-ttu-id="75a80-115">-VaultName</span><span class="sxs-lookup"><span data-stu-id="75a80-115">-VaultName</span></span>
<span data-ttu-id="75a80-116">A kulcsfájl nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="75a80-116">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="75a80-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75a80-117">CommonParameters</span></span>
<span data-ttu-id="75a80-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="75a80-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75a80-119">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75a80-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75a80-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="75a80-120">INPUTS</span></span>

### <span data-ttu-id="75a80-121">Nincs</span><span class="sxs-lookup"><span data-stu-id="75a80-121">None</span></span>
<span data-ttu-id="75a80-122">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="75a80-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="75a80-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="75a80-123">OUTPUTS</span></span>

### <span data-ttu-id="75a80-124">Microsoft. Azure. Command. KeyVaultCertificatePolicy. models.</span><span class="sxs-lookup"><span data-stu-id="75a80-124">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="75a80-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="75a80-125">NOTES</span></span>

## <span data-ttu-id="75a80-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="75a80-126">RELATED LINKS</span></span>

[<span data-ttu-id="75a80-127">Új – AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="75a80-127">New-AzKeyVaultCertificatePolicy</span></span>](./New-AzKeyVaultCertificatePolicy.md)

[<span data-ttu-id="75a80-128">Set-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="75a80-128">Set-AzKeyVaultCertificatePolicy</span></span>](./Set-AzKeyVaultCertificatePolicy.md)

