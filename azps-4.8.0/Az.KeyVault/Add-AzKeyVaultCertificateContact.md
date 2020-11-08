---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 2D3021B3-12C5-4797-8BF2-800E3CEAC56C
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azkeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultCertificateContact.md
ms.openlocfilehash: 5b6661bada9b63485f937a0401064de2c33e3336
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181741"
---
# <span data-ttu-id="53eef-101">Add-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="53eef-101">Add-AzKeyVaultCertificateContact</span></span>

## <span data-ttu-id="53eef-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="53eef-102">SYNOPSIS</span></span>
<span data-ttu-id="53eef-103">Partnerek felvétele a tanúsítvány-értesítésekhez.</span><span class="sxs-lookup"><span data-stu-id="53eef-103">Adds a contact for certificate notifications.</span></span>

## <span data-ttu-id="53eef-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="53eef-104">SYNTAX</span></span>

### <span data-ttu-id="53eef-105">Interaktív (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="53eef-105">Interactive (Default)</span></span>
```
Add-AzKeyVaultCertificateContact [-VaultName] <String> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53eef-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="53eef-106">ByObject</span></span>
```
Add-AzKeyVaultCertificateContact [-InputObject] <PSKeyVault> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53eef-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="53eef-107">ByResourceId</span></span>
```
Add-AzKeyVaultCertificateContact [-ResourceId] <String> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="53eef-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="53eef-108">DESCRIPTION</span></span>
<span data-ttu-id="53eef-109">Az **Add-AzKeyVaultCertificateContact** parancsmag az Azure Key Vault-ban felvesz egy, a fő boltozathoz tartozó névjegykártyát.</span><span class="sxs-lookup"><span data-stu-id="53eef-109">The **Add-AzKeyVaultCertificateContact** cmdlet adds a contact for a key vault for certificate notifications in Azure Key Vault.</span></span>
<span data-ttu-id="53eef-110">A névjegy frissítéseket kap az eseményekről, például a tanúsítványról, a Lejáratról, a megújult tanúsítványról stb.</span><span class="sxs-lookup"><span data-stu-id="53eef-110">The contact receives updates about events such as certificate close to expiry, certificate renewed, and so on.</span></span>
<span data-ttu-id="53eef-111">Ezeket az eseményeket a tanúsítvány-házirend határozza meg.</span><span class="sxs-lookup"><span data-stu-id="53eef-111">These events are determined by the certificate policy.</span></span>

## <span data-ttu-id="53eef-112">Példák</span><span class="sxs-lookup"><span data-stu-id="53eef-112">EXAMPLES</span></span>

### <span data-ttu-id="53eef-113">1. példa: kulcs pince-bizonyítvány felvétele</span><span class="sxs-lookup"><span data-stu-id="53eef-113">Example 1: Add a key vault certificate contact</span></span>
```powershell
PS C:\> Add-AzKeyVaultCertificateContact -VaultName "ContosoKV01" -EmailAddress "patti.fuller@contoso.com" -PassThru

Email                    VaultName
-----                    ---------
patti.fuller@contoso.com ContosoKV01
```

<span data-ttu-id="53eef-114">Ebben a parancsban a ContosoKV01-os kulcs boltozata, és a "ContosoKV01" boltozat névjegyeinek listáját adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="53eef-114">This command adds Patti Fuller as a certificate contact for the ContosoKV01 key vault and returns the list of contacts for the "ContosoKV01" vault.</span></span>

## <span data-ttu-id="53eef-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="53eef-115">PARAMETERS</span></span>

### <span data-ttu-id="53eef-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53eef-116">-DefaultProfile</span></span>
<span data-ttu-id="53eef-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="53eef-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="53eef-118">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="53eef-118">-EmailAddress</span></span>
<span data-ttu-id="53eef-119">A névjegykártya e-mail-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="53eef-119">Specifies the email address of the contact.</span></span>

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

### <span data-ttu-id="53eef-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="53eef-120">-InputObject</span></span>
<span data-ttu-id="53eef-121">A boltozat objektum.</span><span class="sxs-lookup"><span data-stu-id="53eef-121">KeyVault object.</span></span>

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

### <span data-ttu-id="53eef-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="53eef-122">-PassThru</span></span>
<span data-ttu-id="53eef-123">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="53eef-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="53eef-124">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="53eef-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="53eef-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="53eef-125">-ResourceId</span></span>
<span data-ttu-id="53eef-126">A főkészlet erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="53eef-126">KeyVault Resource Id.</span></span>

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

### <span data-ttu-id="53eef-127">-VaultName</span><span class="sxs-lookup"><span data-stu-id="53eef-127">-VaultName</span></span>
<span data-ttu-id="53eef-128">A fő pince nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="53eef-128">Specifies the name of the key vault.</span></span>

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

### <span data-ttu-id="53eef-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="53eef-129">-Confirm</span></span>
<span data-ttu-id="53eef-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="53eef-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53eef-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53eef-131">-WhatIf</span></span>
<span data-ttu-id="53eef-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="53eef-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53eef-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="53eef-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53eef-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53eef-134">CommonParameters</span></span>
<span data-ttu-id="53eef-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="53eef-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53eef-136">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="53eef-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53eef-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="53eef-137">INPUTS</span></span>

### <span data-ttu-id="53eef-138">Microsoft. Azure. Command. PSKeyVault. models.</span><span class="sxs-lookup"><span data-stu-id="53eef-138">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="53eef-139">System. String</span><span class="sxs-lookup"><span data-stu-id="53eef-139">System.String</span></span>

## <span data-ttu-id="53eef-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="53eef-140">OUTPUTS</span></span>

### <span data-ttu-id="53eef-141">Microsoft. Azure. Command. PSKeyVaultCertificateContact. models.</span><span class="sxs-lookup"><span data-stu-id="53eef-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact</span></span>

## <span data-ttu-id="53eef-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="53eef-142">NOTES</span></span>

## <span data-ttu-id="53eef-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="53eef-143">RELATED LINKS</span></span>

[<span data-ttu-id="53eef-144">Get-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="53eef-144">Get-AzKeyVaultCertificateContact</span></span>](./Get-AzKeyVaultCertificateContact.md)

[<span data-ttu-id="53eef-145">Remove-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="53eef-145">Remove-AzKeyVaultCertificateContact</span></span>](./Remove-AzKeyVaultCertificateContact.md)

