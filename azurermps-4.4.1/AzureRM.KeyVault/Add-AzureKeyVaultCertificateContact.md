---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 2D3021B3-12C5-4797-8BF2-800E3CEAC56C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Add-AzureKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Add-AzureKeyVaultCertificateContact.md
ms.openlocfilehash: af66ad82d37c29d1dcd455cb3ccf7ae11676828c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504119"
---
# <span data-ttu-id="ecab9-101">Add-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="ecab9-101">Add-AzureKeyVaultCertificateContact</span></span>

## <span data-ttu-id="ecab9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ecab9-102">SYNOPSIS</span></span>
<span data-ttu-id="ecab9-103">Partnerek felvétele a tanúsítvány-értesítésekhez.</span><span class="sxs-lookup"><span data-stu-id="ecab9-103">Adds a contact for certificate notifications.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ecab9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ecab9-104">SYNTAX</span></span>

```
Add-AzureKeyVaultCertificateContact [-VaultName] <String> [-EmailAddress] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ecab9-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ecab9-105">DESCRIPTION</span></span>
<span data-ttu-id="ecab9-106">Az **Add-AzureKeyVaultCertificateContact** parancsmag az Azure Key Vault-ban felvesz egy, a fő boltozathoz tartozó névjegykártyát.</span><span class="sxs-lookup"><span data-stu-id="ecab9-106">The **Add-AzureKeyVaultCertificateContact** cmdlet adds a contact for a key vault for certificate notifications in Azure Key Vault.</span></span>
<span data-ttu-id="ecab9-107">A névjegy frissítéseket kap az eseményekről, például a tanúsítványról, a Lejáratról, a megújult tanúsítványról stb.</span><span class="sxs-lookup"><span data-stu-id="ecab9-107">The contact receives updates about events such as certificate close to expiry, certificate renewed, and so on.</span></span>
<span data-ttu-id="ecab9-108">Ezeket az eseményeket a tanúsítvány-házirend határozza meg.</span><span class="sxs-lookup"><span data-stu-id="ecab9-108">These events are determined by the certificate policy.</span></span>

## <span data-ttu-id="ecab9-109">Példák</span><span class="sxs-lookup"><span data-stu-id="ecab9-109">EXAMPLES</span></span>

### <span data-ttu-id="ecab9-110">1. példa: kulcs pince-bizonyítvány felvétele</span><span class="sxs-lookup"><span data-stu-id="ecab9-110">Example 1: Add a key vault certificate contact</span></span>
```
PS C:\>Add-AzureKeyVaultCertificateContact -VaultName "ContosoKV01" -EmailAddress "patti.fuller@contoso.com" -PassThru
```

<span data-ttu-id="ecab9-111">Ehhez a parancshoz a ContosoKV01-kulcs boltozata, és a **KeyVaultCertificateContact** objektumot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="ecab9-111">This command adds Patti Fuller as a certificate contact for the ContosoKV01 key vault and returns the **KeyVaultCertificateContact** object.</span></span>

## <span data-ttu-id="ecab9-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ecab9-112">PARAMETERS</span></span>

### <span data-ttu-id="ecab9-113">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="ecab9-113">-EmailAddress</span></span>
<span data-ttu-id="ecab9-114">A névjegykártya e-mail-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ecab9-114">Specifies the email address of the contact.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ecab9-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ecab9-115">-PassThru</span></span>
<span data-ttu-id="ecab9-116">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="ecab9-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ecab9-117">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="ecab9-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ecab9-118">-VaultName</span><span class="sxs-lookup"><span data-stu-id="ecab9-118">-VaultName</span></span>
<span data-ttu-id="ecab9-119">A fő pince nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ecab9-119">Specifies the name of the key vault.</span></span>

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

### <span data-ttu-id="ecab9-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ecab9-120">-Confirm</span></span>
<span data-ttu-id="ecab9-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ecab9-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ecab9-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ecab9-122">-WhatIf</span></span>
<span data-ttu-id="ecab9-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ecab9-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ecab9-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ecab9-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ecab9-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecab9-125">-DefaultProfile</span></span>
<span data-ttu-id="ecab9-126">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ecab9-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ecab9-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecab9-127">CommonParameters</span></span>
<span data-ttu-id="ecab9-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ecab9-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecab9-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ecab9-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecab9-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ecab9-130">INPUTS</span></span>

## <span data-ttu-id="ecab9-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ecab9-131">OUTPUTS</span></span>

### <span data-ttu-id="ecab9-132">Lista<Microsoft. Azure. Command. KeyVaultCertificateContact. models.></span><span class="sxs-lookup"><span data-stu-id="ecab9-132">List<Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateContact></span></span>

## <span data-ttu-id="ecab9-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ecab9-133">NOTES</span></span>

## <span data-ttu-id="ecab9-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ecab9-134">RELATED LINKS</span></span>

[<span data-ttu-id="ecab9-135">Get-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="ecab9-135">Get-AzureKeyVaultCertificateContact</span></span>](./Get-AzureKeyVaultCertificateContact.md)

[<span data-ttu-id="ecab9-136">Remove-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="ecab9-136">Remove-AzureKeyVaultCertificateContact</span></span>](./Remove-AzureKeyVaultCertificateContact.md)

