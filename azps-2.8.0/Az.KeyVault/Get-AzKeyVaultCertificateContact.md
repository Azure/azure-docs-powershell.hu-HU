---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 200C68A3-A79C-4517-8E5D-8128F6C73A5C
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateContact.md
ms.openlocfilehash: 9c7b82c8ec884cc16bc3c593d9f00f1789b98e52
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666204"
---
# <span data-ttu-id="d977d-101">Get-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="d977d-101">Get-AzKeyVaultCertificateContact</span></span>

## <span data-ttu-id="d977d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d977d-102">SYNOPSIS</span></span>
<span data-ttu-id="d977d-103">A tanúsítványok értesítéseihez regisztrált partnerek beolvasása.</span><span class="sxs-lookup"><span data-stu-id="d977d-103">Gets contacts that are registered for certificate notifications for a key vault.</span></span>

## <span data-ttu-id="d977d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d977d-104">SYNTAX</span></span>

### <span data-ttu-id="d977d-105">VaultName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d977d-105">VaultName (Default)</span></span>
```
Get-AzKeyVaultCertificateContact [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d977d-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="d977d-106">ByInputObject</span></span>
```
Get-AzKeyVaultCertificateContact [-InputObject] <PSKeyVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d977d-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d977d-107">ByResourceId</span></span>
```
Get-AzKeyVaultCertificateContact [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d977d-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="d977d-108">DESCRIPTION</span></span>
<span data-ttu-id="d977d-109">A **Get-AzKeyVaultCertificateContact** parancsmag az Azure Key Vault-ban egy fő boltozattal regisztrált névjegyeket kap.</span><span class="sxs-lookup"><span data-stu-id="d977d-109">The **Get-AzKeyVaultCertificateContact** cmdlet gets contacts that are registered for certificate notifications for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="d977d-110">Példák</span><span class="sxs-lookup"><span data-stu-id="d977d-110">EXAMPLES</span></span>

### <span data-ttu-id="d977d-111">1. példa: az összes tanúsítvány-névjegy beolvasása</span><span class="sxs-lookup"><span data-stu-id="d977d-111">Example 1: Get all certificate contacts</span></span>
```powershell
PS C:\> $Contacts = Get-AzKeyVaultCertificateContact -VaultName "Contoso"

Email                   VaultName
-----                   ---------
username@microsoft.com  Contoso
username1@microsoft.com Contoso
```

<span data-ttu-id="d977d-112">Ez a parancs a contoso Key Vault-ban megkapja az összes névjegyet, majd a $Contacts változóban tárolja őket.</span><span class="sxs-lookup"><span data-stu-id="d977d-112">This command gets all of the contacts for the certificate objects in the Contoso key vault, and then stores them in the $Contacts variable.</span></span>

## <span data-ttu-id="d977d-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d977d-113">PARAMETERS</span></span>

### <span data-ttu-id="d977d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d977d-114">-DefaultProfile</span></span>
<span data-ttu-id="d977d-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="d977d-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d977d-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d977d-116">-InputObject</span></span>
<span data-ttu-id="d977d-117">A boltozat objektum.</span><span class="sxs-lookup"><span data-stu-id="d977d-117">KeyVault object.</span></span>

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

### <span data-ttu-id="d977d-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d977d-118">-ResourceId</span></span>
<span data-ttu-id="d977d-119">A megjelenő azonosító.</span><span class="sxs-lookup"><span data-stu-id="d977d-119">KeyVault Id.</span></span>

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

### <span data-ttu-id="d977d-120">-VaultName</span><span class="sxs-lookup"><span data-stu-id="d977d-120">-VaultName</span></span>
<span data-ttu-id="d977d-121">A fő pince nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d977d-121">Specifies the name of the key vault.</span></span>

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

### <span data-ttu-id="d977d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d977d-122">CommonParameters</span></span>
<span data-ttu-id="d977d-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d977d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d977d-124">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d977d-124">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d977d-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d977d-125">INPUTS</span></span>

### <span data-ttu-id="d977d-126">Microsoft. Azure. Command. PSKeyVault. models.</span><span class="sxs-lookup"><span data-stu-id="d977d-126">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="d977d-127">System. String</span><span class="sxs-lookup"><span data-stu-id="d977d-127">System.String</span></span>

## <span data-ttu-id="d977d-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d977d-128">OUTPUTS</span></span>

### <span data-ttu-id="d977d-129">Microsoft. Azure. Command. PSKeyVaultCertificateContact. models.</span><span class="sxs-lookup"><span data-stu-id="d977d-129">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact</span></span>

## <span data-ttu-id="d977d-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d977d-130">NOTES</span></span>

## <span data-ttu-id="d977d-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d977d-131">RELATED LINKS</span></span>

[<span data-ttu-id="d977d-132">Add-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="d977d-132">Add-AzKeyVaultCertificateContact</span></span>](./Add-AzKeyVaultCertificateContact.md)

[<span data-ttu-id="d977d-133">Remove-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="d977d-133">Remove-AzKeyVaultCertificateContact</span></span>](./Remove-AzKeyVaultCertificateContact.md)

