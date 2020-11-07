---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 200C68A3-A79C-4517-8E5D-8128F6C73A5C
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/get-AzKeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateContact.md
ms.openlocfilehash: e02b60055818d1ed79e93e6853353795e78c5830
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842165"
---
# <span data-ttu-id="bb415-101">Get-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="bb415-101">Get-AzKeyVaultCertificateContact</span></span>

## <span data-ttu-id="bb415-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bb415-102">SYNOPSIS</span></span>
<span data-ttu-id="bb415-103">A tanúsítványok értesítéseihez regisztrált partnerek beolvasása.</span><span class="sxs-lookup"><span data-stu-id="bb415-103">Gets contacts that are registered for certificate notifications for a key vault.</span></span>

## <span data-ttu-id="bb415-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bb415-104">SYNTAX</span></span>

```
Get-AzKeyVaultCertificateContact [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bb415-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="bb415-105">DESCRIPTION</span></span>
<span data-ttu-id="bb415-106">A **Get-AzKeyVaultCertificateContact** parancsmag az Azure Key Vault-ban egy fő boltozattal regisztrált névjegyeket kap.</span><span class="sxs-lookup"><span data-stu-id="bb415-106">The **Get-AzKeyVaultCertificateContact** cmdlet gets contacts that are registered for certificate notifications for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="bb415-107">Példák</span><span class="sxs-lookup"><span data-stu-id="bb415-107">EXAMPLES</span></span>

### <span data-ttu-id="bb415-108">1. példa: az összes tanúsítvány-névjegy beolvasása</span><span class="sxs-lookup"><span data-stu-id="bb415-108">Example 1: Get all certificate contacts</span></span>
```
PS C:\>$Contacts = Get-AzKeyVaultCertificateContact -VaultName "Contoso"
```

<span data-ttu-id="bb415-109">Ez a parancs a contoso Key Vault-ban megkapja az összes névjegyet, majd a $Contacts változóban tárolja őket.</span><span class="sxs-lookup"><span data-stu-id="bb415-109">This command gets all of the contacts for the certificate objects in the Contoso key vault, and then stores them in the $Contacts variable.</span></span>

## <span data-ttu-id="bb415-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bb415-110">PARAMETERS</span></span>

### <span data-ttu-id="bb415-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb415-111">-DefaultProfile</span></span>
<span data-ttu-id="bb415-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="bb415-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bb415-113">-VaultName</span><span class="sxs-lookup"><span data-stu-id="bb415-113">-VaultName</span></span>
<span data-ttu-id="bb415-114">A fő pince nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bb415-114">Specifies the name of the key vault.</span></span>

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

### <span data-ttu-id="bb415-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb415-115">CommonParameters</span></span>
<span data-ttu-id="bb415-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bb415-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb415-117">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb415-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb415-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bb415-118">INPUTS</span></span>

### <span data-ttu-id="bb415-119">Nincs</span><span class="sxs-lookup"><span data-stu-id="bb415-119">None</span></span>
<span data-ttu-id="bb415-120">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="bb415-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="bb415-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bb415-121">OUTPUTS</span></span>

### <span data-ttu-id="bb415-122">Lista<Microsoft. Azure. Command. KeyVaultCertificateContact. models.></span><span class="sxs-lookup"><span data-stu-id="bb415-122">List<Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateContact></span></span>

## <span data-ttu-id="bb415-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bb415-123">NOTES</span></span>

## <span data-ttu-id="bb415-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bb415-124">RELATED LINKS</span></span>

[<span data-ttu-id="bb415-125">Add-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="bb415-125">Add-AzKeyVaultCertificateContact</span></span>](./Add-AzKeyVaultCertificateContact.md)

[<span data-ttu-id="bb415-126">Remove-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="bb415-126">Remove-AzKeyVaultCertificateContact</span></span>](./Remove-AzKeyVaultCertificateContact.md)

