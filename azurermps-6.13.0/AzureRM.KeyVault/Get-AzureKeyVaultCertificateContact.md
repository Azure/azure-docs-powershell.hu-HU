---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 200C68A3-A79C-4517-8E5D-8128F6C73A5C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateContact.md
ms.openlocfilehash: 31619366c1d2a1a025cb7ff563a04b166abb2a46
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679563"
---
# <span data-ttu-id="78880-101">Get-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="78880-101">Get-AzureKeyVaultCertificateContact</span></span>

## <span data-ttu-id="78880-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="78880-102">SYNOPSIS</span></span>
<span data-ttu-id="78880-103">A tanúsítványok értesítéseihez regisztrált partnerek beolvasása.</span><span class="sxs-lookup"><span data-stu-id="78880-103">Gets contacts that are registered for certificate notifications for a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="78880-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="78880-104">SYNTAX</span></span>

### <span data-ttu-id="78880-105">VaultName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="78880-105">VaultName (Default)</span></span>
```
Get-AzureKeyVaultCertificateContact [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="78880-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="78880-106">ByInputObject</span></span>
```
Get-AzureKeyVaultCertificateContact [-InputObject] <PSKeyVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="78880-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="78880-107">ByResourceId</span></span>
```
Get-AzureKeyVaultCertificateContact [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="78880-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="78880-108">DESCRIPTION</span></span>
<span data-ttu-id="78880-109">A **Get-AzureKeyVaultCertificateContact** parancsmag az Azure Key Vault-ban egy fő boltozattal regisztrált névjegyeket kap.</span><span class="sxs-lookup"><span data-stu-id="78880-109">The **Get-AzureKeyVaultCertificateContact** cmdlet gets contacts that are registered for certificate notifications for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="78880-110">Példák</span><span class="sxs-lookup"><span data-stu-id="78880-110">EXAMPLES</span></span>

### <span data-ttu-id="78880-111">1. példa: az összes tanúsítvány-névjegy beolvasása</span><span class="sxs-lookup"><span data-stu-id="78880-111">Example 1: Get all certificate contacts</span></span>
```powershell
PS C:\> $Contacts = Get-AzureKeyVaultCertificateContact -VaultName "Contoso"

Email                   VaultName
-----                   ---------
username@microsoft.com  Contoso
username1@microsoft.com Contoso
```

<span data-ttu-id="78880-112">Ez a parancs a contoso Key Vault-ban megkapja az összes névjegyet, majd a $Contacts változóban tárolja őket.</span><span class="sxs-lookup"><span data-stu-id="78880-112">This command gets all of the contacts for the certificate objects in the Contoso key vault, and then stores them in the $Contacts variable.</span></span>

## <span data-ttu-id="78880-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="78880-113">PARAMETERS</span></span>

### <span data-ttu-id="78880-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78880-114">-DefaultProfile</span></span>
<span data-ttu-id="78880-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="78880-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="78880-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="78880-116">-InputObject</span></span>
<span data-ttu-id="78880-117">A boltozat objektum.</span><span class="sxs-lookup"><span data-stu-id="78880-117">KeyVault object.</span></span>

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

### <span data-ttu-id="78880-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="78880-118">-ResourceId</span></span>
<span data-ttu-id="78880-119">A megjelenő azonosító.</span><span class="sxs-lookup"><span data-stu-id="78880-119">KeyVault Id.</span></span>

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

### <span data-ttu-id="78880-120">-VaultName</span><span class="sxs-lookup"><span data-stu-id="78880-120">-VaultName</span></span>
<span data-ttu-id="78880-121">A fő pince nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="78880-121">Specifies the name of the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: VaultName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78880-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78880-122">CommonParameters</span></span>
<span data-ttu-id="78880-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="78880-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78880-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78880-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78880-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="78880-125">INPUTS</span></span>

### <span data-ttu-id="78880-126">Microsoft. Azure. Command. PSKeyVault. models.</span><span class="sxs-lookup"><span data-stu-id="78880-126">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>
<span data-ttu-id="78880-127">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="78880-127">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="78880-128">System. String</span><span class="sxs-lookup"><span data-stu-id="78880-128">System.String</span></span>

## <span data-ttu-id="78880-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="78880-129">OUTPUTS</span></span>

### <span data-ttu-id="78880-130">Microsoft. Azure. Command. PSKeyVaultCertificateContact. models.</span><span class="sxs-lookup"><span data-stu-id="78880-130">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact</span></span>

## <span data-ttu-id="78880-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="78880-131">NOTES</span></span>

## <span data-ttu-id="78880-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="78880-132">RELATED LINKS</span></span>

[<span data-ttu-id="78880-133">Add-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="78880-133">Add-AzureKeyVaultCertificateContact</span></span>](./Add-AzureKeyVaultCertificateContact.md)

[<span data-ttu-id="78880-134">Remove-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="78880-134">Remove-AzureKeyVaultCertificateContact</span></span>](./Remove-AzureKeyVaultCertificateContact.md)

