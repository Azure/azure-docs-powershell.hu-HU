---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 200C68A3-A79C-4517-8E5D-8128F6C73A5C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateContact.md
ms.openlocfilehash: 6a59b49da2ae283af50487bec21da6c1d2457878
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679770"
---
# <span data-ttu-id="3881f-101">Get-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="3881f-101">Get-AzureKeyVaultCertificateContact</span></span>

## <span data-ttu-id="3881f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3881f-102">SYNOPSIS</span></span>
<span data-ttu-id="3881f-103">A tanúsítványok értesítéseihez regisztrált partnerek beolvasása.</span><span class="sxs-lookup"><span data-stu-id="3881f-103">Gets contacts that are registered for certificate notifications for a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3881f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3881f-104">SYNTAX</span></span>

```
Get-AzureKeyVaultCertificateContact [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3881f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3881f-105">DESCRIPTION</span></span>
<span data-ttu-id="3881f-106">A **Get-AzureKeyVaultCertificateContact** parancsmag az Azure Key Vault-ban egy fő boltozattal regisztrált névjegyeket kap.</span><span class="sxs-lookup"><span data-stu-id="3881f-106">The **Get-AzureKeyVaultCertificateContact** cmdlet gets contacts that are registered for certificate notifications for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="3881f-107">Példák</span><span class="sxs-lookup"><span data-stu-id="3881f-107">EXAMPLES</span></span>

### <span data-ttu-id="3881f-108">1. példa: az összes tanúsítvány-névjegy beolvasása</span><span class="sxs-lookup"><span data-stu-id="3881f-108">Example 1: Get all certificate contacts</span></span>
```
PS C:\>$Contacts = Get-AzureKeyVaultCertificateContact -VaultName "Contoso"
```

<span data-ttu-id="3881f-109">Ez a parancs a contoso Key Vault-ban megkapja az összes névjegyet, majd a $Contacts változóban tárolja őket.</span><span class="sxs-lookup"><span data-stu-id="3881f-109">This command gets all of the contacts for the certificate objects in the Contoso key vault, and then stores them in the $Contacts variable.</span></span>

## <span data-ttu-id="3881f-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3881f-110">PARAMETERS</span></span>

### <span data-ttu-id="3881f-111">-VaultName</span><span class="sxs-lookup"><span data-stu-id="3881f-111">-VaultName</span></span>
<span data-ttu-id="3881f-112">A fő pince nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3881f-112">Specifies the name of the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3881f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3881f-113">-DefaultProfile</span></span>
<span data-ttu-id="3881f-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3881f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3881f-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3881f-115">CommonParameters</span></span>
<span data-ttu-id="3881f-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3881f-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3881f-117">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3881f-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3881f-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3881f-118">INPUTS</span></span>

## <span data-ttu-id="3881f-119">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3881f-119">OUTPUTS</span></span>

### <span data-ttu-id="3881f-120">Lista<Microsoft. Azure. Command. KeyVaultCertificateContact. models.></span><span class="sxs-lookup"><span data-stu-id="3881f-120">List<Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateContact></span></span>

## <span data-ttu-id="3881f-121">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3881f-121">NOTES</span></span>

## <span data-ttu-id="3881f-122">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3881f-122">RELATED LINKS</span></span>

[<span data-ttu-id="3881f-123">Add-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="3881f-123">Add-AzureKeyVaultCertificateContact</span></span>](./Add-AzureKeyVaultCertificateContact.md)

[<span data-ttu-id="3881f-124">Remove-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="3881f-124">Remove-AzureKeyVaultCertificateContact</span></span>](./Remove-AzureKeyVaultCertificateContact.md)

