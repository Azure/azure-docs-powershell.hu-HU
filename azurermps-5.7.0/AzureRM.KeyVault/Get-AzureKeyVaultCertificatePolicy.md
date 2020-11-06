---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 0729687C-3104-4136-A80D-16BAEBD6B76C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificatePolicy.md
ms.openlocfilehash: 1317b35e957b46e6f39bfb0866e0429c01d35533
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494478"
---
# <span data-ttu-id="c373d-101">Get-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="c373d-101">Get-AzureKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="c373d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c373d-102">SYNOPSIS</span></span>
<span data-ttu-id="c373d-103">Egy kulcshoz tartozó tanúsítvány házirendjét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="c373d-103">Gets the policy for a certificate in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c373d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c373d-104">SYNTAX</span></span>

### <span data-ttu-id="c373d-105">VaultAndCertName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c373d-105">VaultAndCertName (Default)</span></span>
```
Get-AzureKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c373d-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="c373d-106">InputObject</span></span>
```
Get-AzureKeyVaultCertificatePolicy [-InputObject] <PSKeyVaultCertificateIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c373d-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="c373d-107">DESCRIPTION</span></span>
<span data-ttu-id="c373d-108">A **Get-AzureKeyVaultCertificatePolicy** parancsmag az Azure Key Vault-ban egy fő tárolóban kapja meg a tanúsítvány házirendjét.</span><span class="sxs-lookup"><span data-stu-id="c373d-108">The **Get-AzureKeyVaultCertificatePolicy** cmdlet gets the policy for a certificate in a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="c373d-109">Példák</span><span class="sxs-lookup"><span data-stu-id="c373d-109">EXAMPLES</span></span>

### <span data-ttu-id="c373d-110">Példa 1: tanúsítvány-házirend beszerzése</span><span class="sxs-lookup"><span data-stu-id="c373d-110">Example 1: Get a certificate policy</span></span>
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

<span data-ttu-id="c373d-111">Ez a parancs beolvassa a TestCert01 tanúsítvány házirendjét a ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="c373d-111">This command gets the certificate policy for TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="c373d-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c373d-112">PARAMETERS</span></span>

### <span data-ttu-id="c373d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c373d-113">-DefaultProfile</span></span>
<span data-ttu-id="c373d-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="c373d-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c373d-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c373d-115">-InputObject</span></span>
<span data-ttu-id="c373d-116">Certificate objektum.</span><span class="sxs-lookup"><span data-stu-id="c373d-116">Certificate Object.</span></span>

```yaml
Type: PSKeyVaultCertificateIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c373d-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c373d-117">-Name</span></span>
<span data-ttu-id="c373d-118">A tanúsítvány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c373d-118">Specifies the name of a certificate.</span></span>

```yaml
Type: String
Parameter Sets: VaultAndCertName
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c373d-119">-VaultName</span><span class="sxs-lookup"><span data-stu-id="c373d-119">-VaultName</span></span>
<span data-ttu-id="c373d-120">A kulcsfájl nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c373d-120">Specifies the name of a key vault.</span></span>

```yaml
Type: String
Parameter Sets: VaultAndCertName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c373d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c373d-121">CommonParameters</span></span>
<span data-ttu-id="c373d-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c373d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c373d-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c373d-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c373d-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c373d-124">INPUTS</span></span>

### <span data-ttu-id="c373d-125">Nincs</span><span class="sxs-lookup"><span data-stu-id="c373d-125">None</span></span>
<span data-ttu-id="c373d-126">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="c373d-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c373d-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c373d-127">OUTPUTS</span></span>

### <span data-ttu-id="c373d-128">Microsoft. Azure. Command. PSKeyVaultCertificatePolicy. models.</span><span class="sxs-lookup"><span data-stu-id="c373d-128">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="c373d-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c373d-129">NOTES</span></span>

## <span data-ttu-id="c373d-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c373d-130">RELATED LINKS</span></span>

[<span data-ttu-id="c373d-131">Új – AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="c373d-131">New-AzureKeyVaultCertificatePolicy</span></span>](./New-AzureKeyVaultCertificatePolicy.md)

[<span data-ttu-id="c373d-132">Set-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="c373d-132">Set-AzureKeyVaultCertificatePolicy</span></span>](./Set-AzureKeyVaultCertificatePolicy.md)

