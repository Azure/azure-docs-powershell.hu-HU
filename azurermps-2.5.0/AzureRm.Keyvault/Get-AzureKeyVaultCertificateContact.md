---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 200C68A3-A79C-4517-8E5D-8128F6C73A5C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultcertificatecontact
schema: 2.0.0
ms.openlocfilehash: d6d2070afcb4a5b9b0b13af1fa54dc93621c5a97
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849294"
---
# <span data-ttu-id="cfd21-101">Get-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="cfd21-101">Get-AzureKeyVaultCertificateContact</span></span>

## <span data-ttu-id="cfd21-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cfd21-102">SYNOPSIS</span></span>
<span data-ttu-id="cfd21-103">A tanúsítványok értesítéseihez regisztrált partnerek beolvasása.</span><span class="sxs-lookup"><span data-stu-id="cfd21-103">Gets contacts that are registered for certificate notifications for a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cfd21-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cfd21-104">SYNTAX</span></span>

```
Get-AzureKeyVaultCertificateContact [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cfd21-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="cfd21-105">DESCRIPTION</span></span>
<span data-ttu-id="cfd21-106">A **Get-AzureKeyVaultCertificateContact** parancsmag az Azure Key Vault-ban egy fő boltozattal regisztrált névjegyeket kap.</span><span class="sxs-lookup"><span data-stu-id="cfd21-106">The **Get-AzureKeyVaultCertificateContact** cmdlet gets contacts that are registered for certificate notifications for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="cfd21-107">Példák</span><span class="sxs-lookup"><span data-stu-id="cfd21-107">EXAMPLES</span></span>

### <span data-ttu-id="cfd21-108">1. példa: az összes tanúsítvány-névjegy beolvasása</span><span class="sxs-lookup"><span data-stu-id="cfd21-108">Example 1: Get all certificate contacts</span></span>
```
PS C:\>$Contacts = Get-AzureKeyVaultCertificateContact -VaultName "Contoso"
```

<span data-ttu-id="cfd21-109">Ez a parancs a contoso Key Vault-ban megkapja az összes névjegyet, majd a $Contacts változóban tárolja őket.</span><span class="sxs-lookup"><span data-stu-id="cfd21-109">This command gets all of the contacts for the certificate objects in the Contoso key vault, and then stores them in the $Contacts variable.</span></span>

## <span data-ttu-id="cfd21-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cfd21-110">PARAMETERS</span></span>

### <span data-ttu-id="cfd21-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfd21-111">-DefaultProfile</span></span>
<span data-ttu-id="cfd21-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="cfd21-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cfd21-113">-VaultName</span><span class="sxs-lookup"><span data-stu-id="cfd21-113">-VaultName</span></span>
<span data-ttu-id="cfd21-114">A fő pince nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cfd21-114">Specifies the name of the key vault.</span></span>

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

### <span data-ttu-id="cfd21-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfd21-115">CommonParameters</span></span>
<span data-ttu-id="cfd21-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cfd21-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfd21-117">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cfd21-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfd21-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cfd21-118">INPUTS</span></span>

## <span data-ttu-id="cfd21-119">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cfd21-119">OUTPUTS</span></span>

### <span data-ttu-id="cfd21-120">Lista<Microsoft. Azure. Command. KeyVaultCertificateContact. models.></span><span class="sxs-lookup"><span data-stu-id="cfd21-120">List<Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateContact></span></span>

## <span data-ttu-id="cfd21-121">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cfd21-121">NOTES</span></span>

## <span data-ttu-id="cfd21-122">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cfd21-122">RELATED LINKS</span></span>

[<span data-ttu-id="cfd21-123">Add-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="cfd21-123">Add-AzureKeyVaultCertificateContact</span></span>](./Add-AzureKeyVaultCertificateContact.md)

[<span data-ttu-id="cfd21-124">Remove-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="cfd21-124">Remove-AzureKeyVaultCertificateContact</span></span>](./Remove-AzureKeyVaultCertificateContact.md)

