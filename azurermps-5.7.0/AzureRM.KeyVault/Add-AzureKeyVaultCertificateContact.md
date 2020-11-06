---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 2D3021B3-12C5-4797-8BF2-800E3CEAC56C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/add-azurekeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Add-AzureKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Add-AzureKeyVaultCertificateContact.md
ms.openlocfilehash: 96f793c763a3e9a710c7e401c29880ccc0136b38
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503747"
---
# <span data-ttu-id="c788f-101">Add-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="c788f-101">Add-AzureKeyVaultCertificateContact</span></span>

## <span data-ttu-id="c788f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c788f-102">SYNOPSIS</span></span>
<span data-ttu-id="c788f-103">Partnerek felvétele a tanúsítvány-értesítésekhez.</span><span class="sxs-lookup"><span data-stu-id="c788f-103">Adds a contact for certificate notifications.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c788f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c788f-104">SYNTAX</span></span>

### <span data-ttu-id="c788f-105">Interaktív (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c788f-105">Interactive (Default)</span></span>
```
Add-AzureKeyVaultCertificateContact [-VaultName] <String> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c788f-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="c788f-106">ByObject</span></span>
```
Add-AzureKeyVaultCertificateContact [-InputObject] <PSKeyVault> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c788f-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="c788f-107">DESCRIPTION</span></span>
<span data-ttu-id="c788f-108">Az **Add-AzureKeyVaultCertificateContact** parancsmag az Azure Key Vault-ban felvesz egy, a fő boltozathoz tartozó névjegykártyát.</span><span class="sxs-lookup"><span data-stu-id="c788f-108">The **Add-AzureKeyVaultCertificateContact** cmdlet adds a contact for a key vault for certificate notifications in Azure Key Vault.</span></span>
<span data-ttu-id="c788f-109">A névjegy frissítéseket kap az eseményekről, például a tanúsítványról, a Lejáratról, a megújult tanúsítványról stb.</span><span class="sxs-lookup"><span data-stu-id="c788f-109">The contact receives updates about events such as certificate close to expiry, certificate renewed, and so on.</span></span>
<span data-ttu-id="c788f-110">Ezeket az eseményeket a tanúsítvány-házirend határozza meg.</span><span class="sxs-lookup"><span data-stu-id="c788f-110">These events are determined by the certificate policy.</span></span>

## <span data-ttu-id="c788f-111">Példák</span><span class="sxs-lookup"><span data-stu-id="c788f-111">EXAMPLES</span></span>

### <span data-ttu-id="c788f-112">1. példa: kulcs pince-bizonyítvány felvétele</span><span class="sxs-lookup"><span data-stu-id="c788f-112">Example 1: Add a key vault certificate contact</span></span>
```
PS C:\>Add-AzureKeyVaultCertificateContact -VaultName "ContosoKV01" -EmailAddress "patti.fuller@contoso.com" -PassThru
```

<span data-ttu-id="c788f-113">Ehhez a parancshoz a ContosoKV01-kulcs boltozata, és a **KeyVaultCertificateContact** objektumot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="c788f-113">This command adds Patti Fuller as a certificate contact for the ContosoKV01 key vault and returns the **KeyVaultCertificateContact** object.</span></span>

## <span data-ttu-id="c788f-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c788f-114">PARAMETERS</span></span>

### <span data-ttu-id="c788f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c788f-115">-DefaultProfile</span></span>
<span data-ttu-id="c788f-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="c788f-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c788f-117">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="c788f-117">-EmailAddress</span></span>
<span data-ttu-id="c788f-118">A névjegykártya e-mail-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c788f-118">Specifies the email address of the contact.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c788f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c788f-119">-InputObject</span></span>
<span data-ttu-id="c788f-120">A boltozat objektum.</span><span class="sxs-lookup"><span data-stu-id="c788f-120">KeyVault object.</span></span>

```yaml
Type: PSKeyVault
Parameter Sets: ByObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c788f-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c788f-121">-PassThru</span></span>
<span data-ttu-id="c788f-122">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="c788f-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="c788f-123">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="c788f-123">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c788f-124">-VaultName</span><span class="sxs-lookup"><span data-stu-id="c788f-124">-VaultName</span></span>
<span data-ttu-id="c788f-125">A fő pince nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c788f-125">Specifies the name of the key vault.</span></span>

```yaml
Type: String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c788f-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c788f-126">-Confirm</span></span>
<span data-ttu-id="c788f-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c788f-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c788f-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c788f-128">-WhatIf</span></span>
<span data-ttu-id="c788f-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c788f-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c788f-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c788f-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c788f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c788f-131">CommonParameters</span></span>
<span data-ttu-id="c788f-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c788f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c788f-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c788f-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c788f-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c788f-134">INPUTS</span></span>

### <span data-ttu-id="c788f-135">Nincs</span><span class="sxs-lookup"><span data-stu-id="c788f-135">None</span></span>
<span data-ttu-id="c788f-136">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="c788f-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c788f-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c788f-137">OUTPUTS</span></span>

### <span data-ttu-id="c788f-138">Lista<Microsoft. Azure. Command. PSKeyVaultCertificateContact. models.></span><span class="sxs-lookup"><span data-stu-id="c788f-138">List<Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact></span></span>

## <span data-ttu-id="c788f-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c788f-139">NOTES</span></span>

## <span data-ttu-id="c788f-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c788f-140">RELATED LINKS</span></span>

[<span data-ttu-id="c788f-141">Get-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="c788f-141">Get-AzureKeyVaultCertificateContact</span></span>](./Get-AzureKeyVaultCertificateContact.md)

[<span data-ttu-id="c788f-142">Remove-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="c788f-142">Remove-AzureKeyVaultCertificateContact</span></span>](./Remove-AzureKeyVaultCertificateContact.md)

