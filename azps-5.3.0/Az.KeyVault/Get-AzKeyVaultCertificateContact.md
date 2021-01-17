---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 200C68A3-A79C-4517-8E5D-8128F6C73A5C
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateContact.md
ms.openlocfilehash: ca7f0f87ebcbad3d613939f2e73a743763b134c9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98476981"
---
# <span data-ttu-id="16e90-101">Get-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="16e90-101">Get-AzKeyVaultCertificateContact</span></span>

## <span data-ttu-id="16e90-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16e90-102">SYNOPSIS</span></span>
<span data-ttu-id="16e90-103">Egy kulcstároló tanúsítványértesítéseihez regisztrált névjegyeket kap.</span><span class="sxs-lookup"><span data-stu-id="16e90-103">Gets contacts that are registered for certificate notifications for a key vault.</span></span>

## <span data-ttu-id="16e90-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="16e90-104">SYNTAX</span></span>

### <span data-ttu-id="16e90-105">VaultName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="16e90-105">VaultName (Default)</span></span>
```
Get-AzKeyVaultCertificateContact [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="16e90-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="16e90-106">ByInputObject</span></span>
```
Get-AzKeyVaultCertificateContact [-InputObject] <PSKeyVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="16e90-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="16e90-107">ByResourceId</span></span>
```
Get-AzKeyVaultCertificateContact [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="16e90-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="16e90-108">DESCRIPTION</span></span>
<span data-ttu-id="16e90-109">A **Get-AzKeyVaultCertificateContact parancsmag** olyan névjegyeket kap, amelyek egy kulcstároló tanúsítványértesítéseihez vannak regisztrálva az Azure Key Vaultban.</span><span class="sxs-lookup"><span data-stu-id="16e90-109">The **Get-AzKeyVaultCertificateContact** cmdlet gets contacts that are registered for certificate notifications for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="16e90-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="16e90-110">EXAMPLES</span></span>

### <span data-ttu-id="16e90-111">1. példa: Az összes tanúsítvány kapcsolattartója</span><span class="sxs-lookup"><span data-stu-id="16e90-111">Example 1: Get all certificate contacts</span></span>
```powershell
PS C:\> $Contacts = Get-AzKeyVaultCertificateContact -VaultName "Contoso"

Email                   VaultName
-----                   ---------
username@microsoft.com  Contoso
username1@microsoft.com Contoso
```

<span data-ttu-id="16e90-112">Ez a parancs a Contoso kulcstárolóban lévő tanúsítványobjektumok összes névjegyét bekéri, majd a $Contacts tárolja.</span><span class="sxs-lookup"><span data-stu-id="16e90-112">This command gets all of the contacts for the certificate objects in the Contoso key vault, and then stores them in the $Contacts variable.</span></span>

## <span data-ttu-id="16e90-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="16e90-113">PARAMETERS</span></span>

### <span data-ttu-id="16e90-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16e90-114">-DefaultProfile</span></span>
<span data-ttu-id="16e90-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="16e90-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="16e90-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="16e90-116">-InputObject</span></span>
<span data-ttu-id="16e90-117">KeyVault objektum.</span><span class="sxs-lookup"><span data-stu-id="16e90-117">KeyVault object.</span></span>

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

### <span data-ttu-id="16e90-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="16e90-118">-ResourceId</span></span>
<span data-ttu-id="16e90-119">KeyVault-azonosító.</span><span class="sxs-lookup"><span data-stu-id="16e90-119">KeyVault Id.</span></span>

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

### <span data-ttu-id="16e90-120">-VaultName</span><span class="sxs-lookup"><span data-stu-id="16e90-120">-VaultName</span></span>
<span data-ttu-id="16e90-121">A kulcstár nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="16e90-121">Specifies the name of the key vault.</span></span>

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

### <span data-ttu-id="16e90-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16e90-122">CommonParameters</span></span>
<span data-ttu-id="16e90-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16e90-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16e90-124">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="16e90-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16e90-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="16e90-125">INPUTS</span></span>

### <span data-ttu-id="16e90-126">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="16e90-126">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="16e90-127">System.String</span><span class="sxs-lookup"><span data-stu-id="16e90-127">System.String</span></span>

## <span data-ttu-id="16e90-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="16e90-128">OUTPUTS</span></span>

### <span data-ttu-id="16e90-129">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="16e90-129">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact</span></span>

## <span data-ttu-id="16e90-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="16e90-130">NOTES</span></span>

## <span data-ttu-id="16e90-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="16e90-131">RELATED LINKS</span></span>

[<span data-ttu-id="16e90-132">Add-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="16e90-132">Add-AzKeyVaultCertificateContact</span></span>](./Add-AzKeyVaultCertificateContact.md)

[<span data-ttu-id="16e90-133">Remove-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="16e90-133">Remove-AzKeyVaultCertificateContact</span></span>](./Remove-AzKeyVaultCertificateContact.md)

