---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 200C68A3-A79C-4517-8E5D-8128F6C73A5C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateContact.md
ms.openlocfilehash: cf60626ec04a2466fc9565aef5daff896281345d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672370"
---
# <span data-ttu-id="94459-101">Get-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="94459-101">Get-AzureKeyVaultCertificateContact</span></span>

## <span data-ttu-id="94459-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="94459-102">SYNOPSIS</span></span>
<span data-ttu-id="94459-103">A tanúsítványok értesítéseihez regisztrált partnerek beolvasása.</span><span class="sxs-lookup"><span data-stu-id="94459-103">Gets contacts that are registered for certificate notifications for a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="94459-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="94459-104">SYNTAX</span></span>

### <span data-ttu-id="94459-105">VaultName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="94459-105">VaultName (Default)</span></span>
```
Get-AzureKeyVaultCertificateContact [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="94459-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="94459-106">ByInputObject</span></span>
```
Get-AzureKeyVaultCertificateContact [-InputObject] <PSKeyVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="94459-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="94459-107">ByResourceId</span></span>
```
Get-AzureKeyVaultCertificateContact [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="94459-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="94459-108">DESCRIPTION</span></span>
<span data-ttu-id="94459-109">A **Get-AzureKeyVaultCertificateContact** parancsmag az Azure Key Vault-ban egy fő boltozattal regisztrált névjegyeket kap.</span><span class="sxs-lookup"><span data-stu-id="94459-109">The **Get-AzureKeyVaultCertificateContact** cmdlet gets contacts that are registered for certificate notifications for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="94459-110">Példák</span><span class="sxs-lookup"><span data-stu-id="94459-110">EXAMPLES</span></span>

### <span data-ttu-id="94459-111">1. példa: az összes tanúsítvány-névjegy beolvasása</span><span class="sxs-lookup"><span data-stu-id="94459-111">Example 1: Get all certificate contacts</span></span>
```
PS C:\>$Contacts = Get-AzureKeyVaultCertificateContact -VaultName "Contoso"
```

<span data-ttu-id="94459-112">Ez a parancs a contoso Key Vault-ban megkapja az összes névjegyet, majd a $Contacts változóban tárolja őket.</span><span class="sxs-lookup"><span data-stu-id="94459-112">This command gets all of the contacts for the certificate objects in the Contoso key vault, and then stores them in the $Contacts variable.</span></span>

## <span data-ttu-id="94459-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="94459-113">PARAMETERS</span></span>

### <span data-ttu-id="94459-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94459-114">-DefaultProfile</span></span>
<span data-ttu-id="94459-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="94459-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="94459-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="94459-116">-InputObject</span></span>
<span data-ttu-id="94459-117">A boltozat objektum.</span><span class="sxs-lookup"><span data-stu-id="94459-117">KeyVault object.</span></span>

```yaml
Type: PSKeyVault
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="94459-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="94459-118">-ResourceId</span></span>
<span data-ttu-id="94459-119">A megjelenő azonosító.</span><span class="sxs-lookup"><span data-stu-id="94459-119">KeyVault Id.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94459-120">-VaultName</span><span class="sxs-lookup"><span data-stu-id="94459-120">-VaultName</span></span>
<span data-ttu-id="94459-121">A fő pince nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="94459-121">Specifies the name of the key vault.</span></span>

```yaml
Type: String
Parameter Sets: VaultName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94459-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94459-122">CommonParameters</span></span>
<span data-ttu-id="94459-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="94459-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94459-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94459-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94459-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="94459-125">INPUTS</span></span>

### <span data-ttu-id="94459-126">Nincs</span><span class="sxs-lookup"><span data-stu-id="94459-126">None</span></span>
<span data-ttu-id="94459-127">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="94459-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="94459-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="94459-128">OUTPUTS</span></span>

### <span data-ttu-id="94459-129">Lista<Microsoft. Azure. Command. PSKeyVaultCertificateContact. models.></span><span class="sxs-lookup"><span data-stu-id="94459-129">List<Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact></span></span>

## <span data-ttu-id="94459-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="94459-130">NOTES</span></span>

## <span data-ttu-id="94459-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="94459-131">RELATED LINKS</span></span>

[<span data-ttu-id="94459-132">Add-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="94459-132">Add-AzureKeyVaultCertificateContact</span></span>](./Add-AzureKeyVaultCertificateContact.md)

[<span data-ttu-id="94459-133">Remove-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="94459-133">Remove-AzureKeyVaultCertificateContact</span></span>](./Remove-AzureKeyVaultCertificateContact.md)

