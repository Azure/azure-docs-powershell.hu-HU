---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 2D3021B3-12C5-4797-8BF2-800E3CEAC56C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/add-azurekeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Add-AzureKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Add-AzureKeyVaultCertificateContact.md
ms.openlocfilehash: c56dad380d1e5a43b3f4dafdc0e0e964e6264ef3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504412"
---
# <span data-ttu-id="0254f-101">Add-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="0254f-101">Add-AzureKeyVaultCertificateContact</span></span>

## <span data-ttu-id="0254f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0254f-102">SYNOPSIS</span></span>
<span data-ttu-id="0254f-103">Partnerek felvétele a tanúsítvány-értesítésekhez.</span><span class="sxs-lookup"><span data-stu-id="0254f-103">Adds a contact for certificate notifications.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0254f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0254f-104">SYNTAX</span></span>

### <span data-ttu-id="0254f-105">Interaktív (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0254f-105">Interactive (Default)</span></span>
```
Add-AzureKeyVaultCertificateContact [-VaultName] <String> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0254f-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="0254f-106">ByObject</span></span>
```
Add-AzureKeyVaultCertificateContact [-InputObject] <PSKeyVault> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0254f-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="0254f-107">ByResourceId</span></span>
```
Add-AzureKeyVaultCertificateContact [-ResourceId] <String> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0254f-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="0254f-108">DESCRIPTION</span></span>
<span data-ttu-id="0254f-109">Az **Add-AzureKeyVaultCertificateContact** parancsmag az Azure Key Vault-ban felvesz egy, a fő boltozathoz tartozó névjegykártyát.</span><span class="sxs-lookup"><span data-stu-id="0254f-109">The **Add-AzureKeyVaultCertificateContact** cmdlet adds a contact for a key vault for certificate notifications in Azure Key Vault.</span></span>
<span data-ttu-id="0254f-110">A névjegy frissítéseket kap az eseményekről, például a tanúsítványról, a Lejáratról, a megújult tanúsítványról stb.</span><span class="sxs-lookup"><span data-stu-id="0254f-110">The contact receives updates about events such as certificate close to expiry, certificate renewed, and so on.</span></span>
<span data-ttu-id="0254f-111">Ezeket az eseményeket a tanúsítvány-házirend határozza meg.</span><span class="sxs-lookup"><span data-stu-id="0254f-111">These events are determined by the certificate policy.</span></span>

## <span data-ttu-id="0254f-112">Példák</span><span class="sxs-lookup"><span data-stu-id="0254f-112">EXAMPLES</span></span>

### <span data-ttu-id="0254f-113">1. példa: kulcs pince-bizonyítvány felvétele</span><span class="sxs-lookup"><span data-stu-id="0254f-113">Example 1: Add a key vault certificate contact</span></span>
```powershell
PS C:\> Add-AzureKeyVaultCertificateContact -VaultName "ContosoKV01" -EmailAddress "patti.fuller@contoso.com" -PassThru

Email                    VaultName
-----                    ---------
patti.fuller@contoso.com ContosoKV01
```

<span data-ttu-id="0254f-114">Ebben a parancsban a ContosoKV01-os kulcs boltozata, és a "ContosoKV01" boltozat névjegyeinek listáját adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="0254f-114">This command adds Patti Fuller as a certificate contact for the ContosoKV01 key vault and returns the list of contacts for the "ContosoKV01" vault.</span></span>

## <span data-ttu-id="0254f-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0254f-115">PARAMETERS</span></span>

### <span data-ttu-id="0254f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0254f-116">-DefaultProfile</span></span>
<span data-ttu-id="0254f-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="0254f-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0254f-118">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="0254f-118">-EmailAddress</span></span>
<span data-ttu-id="0254f-119">A névjegykártya e-mail-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0254f-119">Specifies the email address of the contact.</span></span>

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

### <span data-ttu-id="0254f-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0254f-120">-InputObject</span></span>
<span data-ttu-id="0254f-121">A boltozat objektum.</span><span class="sxs-lookup"><span data-stu-id="0254f-121">KeyVault object.</span></span>

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

### <span data-ttu-id="0254f-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0254f-122">-PassThru</span></span>
<span data-ttu-id="0254f-123">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="0254f-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="0254f-124">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="0254f-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0254f-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0254f-125">-ResourceId</span></span>
<span data-ttu-id="0254f-126">A főkészlet erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="0254f-126">KeyVault Resource Id.</span></span>

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

### <span data-ttu-id="0254f-127">-VaultName</span><span class="sxs-lookup"><span data-stu-id="0254f-127">-VaultName</span></span>
<span data-ttu-id="0254f-128">A fő pince nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0254f-128">Specifies the name of the key vault.</span></span>

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

### <span data-ttu-id="0254f-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0254f-129">-Confirm</span></span>
<span data-ttu-id="0254f-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0254f-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0254f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0254f-131">-WhatIf</span></span>
<span data-ttu-id="0254f-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0254f-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0254f-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0254f-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0254f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0254f-134">CommonParameters</span></span>
<span data-ttu-id="0254f-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0254f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0254f-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0254f-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0254f-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0254f-137">INPUTS</span></span>

### <span data-ttu-id="0254f-138">Microsoft. Azure. Command. PSKeyVault. models.</span><span class="sxs-lookup"><span data-stu-id="0254f-138">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>
<span data-ttu-id="0254f-139">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="0254f-139">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="0254f-140">System. String</span><span class="sxs-lookup"><span data-stu-id="0254f-140">System.String</span></span>

## <span data-ttu-id="0254f-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0254f-141">OUTPUTS</span></span>

### <span data-ttu-id="0254f-142">Microsoft. Azure. Command. PSKeyVaultCertificateContact. models.</span><span class="sxs-lookup"><span data-stu-id="0254f-142">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact</span></span>

## <span data-ttu-id="0254f-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0254f-143">NOTES</span></span>

## <span data-ttu-id="0254f-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0254f-144">RELATED LINKS</span></span>

[<span data-ttu-id="0254f-145">Get-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="0254f-145">Get-AzureKeyVaultCertificateContact</span></span>](./Get-AzureKeyVaultCertificateContact.md)

[<span data-ttu-id="0254f-146">Remove-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="0254f-146">Remove-AzureKeyVaultCertificateContact</span></span>](./Remove-AzureKeyVaultCertificateContact.md)

