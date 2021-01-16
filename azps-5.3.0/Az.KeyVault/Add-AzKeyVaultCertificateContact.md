---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 2D3021B3-12C5-4797-8BF2-800E3CEAC56C
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azkeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultCertificateContact.md
ms.openlocfilehash: 5b6661bada9b63485f937a0401064de2c33e3336
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480128"
---
# <span data-ttu-id="8291d-101">Add-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="8291d-101">Add-AzKeyVaultCertificateContact</span></span>

## <span data-ttu-id="8291d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8291d-102">SYNOPSIS</span></span>
<span data-ttu-id="8291d-103">Névjegyet ad hozzá a tanúsítványértesítésekért.</span><span class="sxs-lookup"><span data-stu-id="8291d-103">Adds a contact for certificate notifications.</span></span>

## <span data-ttu-id="8291d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8291d-104">SYNTAX</span></span>

### <span data-ttu-id="8291d-105">Interaktív (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8291d-105">Interactive (Default)</span></span>
```
Add-AzKeyVaultCertificateContact [-VaultName] <String> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8291d-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="8291d-106">ByObject</span></span>
```
Add-AzKeyVaultCertificateContact [-InputObject] <PSKeyVault> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8291d-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="8291d-107">ByResourceId</span></span>
```
Add-AzKeyVaultCertificateContact [-ResourceId] <String> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8291d-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8291d-108">DESCRIPTION</span></span>
<span data-ttu-id="8291d-109">Az **Add-AzKeyVaultCertificateContact parancsmag** hozzáadja a tanúsítványértesítések kulcstárának névjegyét az Azure Key Vaultban.</span><span class="sxs-lookup"><span data-stu-id="8291d-109">The **Add-AzKeyVaultCertificateContact** cmdlet adds a contact for a key vault for certificate notifications in Azure Key Vault.</span></span>
<span data-ttu-id="8291d-110">A partner frissítéseket kap az eseményekről, például a hamarosan lejáró tanúsítványról, a megújított tanúsítványról stb.</span><span class="sxs-lookup"><span data-stu-id="8291d-110">The contact receives updates about events such as certificate close to expiry, certificate renewed, and so on.</span></span>
<span data-ttu-id="8291d-111">Ezeket az eseményeket a tanúsítvány-házirend határozza meg.</span><span class="sxs-lookup"><span data-stu-id="8291d-111">These events are determined by the certificate policy.</span></span>

## <span data-ttu-id="8291d-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8291d-112">EXAMPLES</span></span>

### <span data-ttu-id="8291d-113">1. példa: Kulcstároló tanúsítvány kapcsolattartója</span><span class="sxs-lookup"><span data-stu-id="8291d-113">Example 1: Add a key vault certificate contact</span></span>
```powershell
PS C:\> Add-AzKeyVaultCertificateContact -VaultName "ContosoKV01" -EmailAddress "patti.fuller@contoso.com" -PassThru

Email                    VaultName
-----                    ---------
patti.fuller@contoso.com ContosoKV01
```

<span data-ttu-id="8291d-114">Ez a parancs hozzáadja Patti Fullert a ContosoKV01 kulcstároló tanúsítvány kapcsolattartójaként, és visszaadja a "ContosoKV01" tároló névjegyeit.</span><span class="sxs-lookup"><span data-stu-id="8291d-114">This command adds Patti Fuller as a certificate contact for the ContosoKV01 key vault and returns the list of contacts for the "ContosoKV01" vault.</span></span>

## <span data-ttu-id="8291d-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8291d-115">PARAMETERS</span></span>

### <span data-ttu-id="8291d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8291d-116">-DefaultProfile</span></span>
<span data-ttu-id="8291d-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="8291d-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8291d-118">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="8291d-118">-EmailAddress</span></span>
<span data-ttu-id="8291d-119">A partner e-mail-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8291d-119">Specifies the email address of the contact.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8291d-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8291d-120">-InputObject</span></span>
<span data-ttu-id="8291d-121">KeyVault objektum.</span><span class="sxs-lookup"><span data-stu-id="8291d-121">KeyVault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8291d-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8291d-122">-PassThru</span></span>
<span data-ttu-id="8291d-123">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amellyel dolgozik.</span><span class="sxs-lookup"><span data-stu-id="8291d-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="8291d-124">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="8291d-124">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8291d-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8291d-125">-ResourceId</span></span>
<span data-ttu-id="8291d-126">KeyVault-erőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="8291d-126">KeyVault Resource Id.</span></span>

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

### <span data-ttu-id="8291d-127">-VaultName</span><span class="sxs-lookup"><span data-stu-id="8291d-127">-VaultName</span></span>
<span data-ttu-id="8291d-128">A kulcstár nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8291d-128">Specifies the name of the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8291d-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8291d-129">-Confirm</span></span>
<span data-ttu-id="8291d-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="8291d-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8291d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8291d-131">-WhatIf</span></span>
<span data-ttu-id="8291d-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="8291d-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8291d-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8291d-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8291d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8291d-134">CommonParameters</span></span>
<span data-ttu-id="8291d-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8291d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8291d-136">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8291d-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8291d-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8291d-137">INPUTS</span></span>

### <span data-ttu-id="8291d-138">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="8291d-138">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="8291d-139">System.String</span><span class="sxs-lookup"><span data-stu-id="8291d-139">System.String</span></span>

## <span data-ttu-id="8291d-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8291d-140">OUTPUTS</span></span>

### <span data-ttu-id="8291d-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="8291d-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact</span></span>

## <span data-ttu-id="8291d-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8291d-142">NOTES</span></span>

## <span data-ttu-id="8291d-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8291d-143">RELATED LINKS</span></span>

[<span data-ttu-id="8291d-144">Get-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="8291d-144">Get-AzKeyVaultCertificateContact</span></span>](./Get-AzKeyVaultCertificateContact.md)

[<span data-ttu-id="8291d-145">Remove-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="8291d-145">Remove-AzKeyVaultCertificateContact</span></span>](./Remove-AzKeyVaultCertificateContact.md)

