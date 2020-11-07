---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azkeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Add-AzKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Add-AzKeyVaultCertificateContact.md
ms.openlocfilehash: 375cc5493bd3b3cac31f4318df57e155eda918c3
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843914"
---
# <span data-ttu-id="11052-101">Add-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="11052-101">Add-AzKeyVaultCertificateContact</span></span>

## <span data-ttu-id="11052-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="11052-102">SYNOPSIS</span></span>
<span data-ttu-id="11052-103">Partnerek felvétele a tanúsítvány-értesítésekhez.</span><span class="sxs-lookup"><span data-stu-id="11052-103">Adds a contact for certificate notifications.</span></span>

## <span data-ttu-id="11052-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="11052-104">SYNTAX</span></span>

```
Add-AzKeyVaultCertificateContact [-VaultName] <String> [-EmailAddress] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11052-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="11052-105">DESCRIPTION</span></span>
<span data-ttu-id="11052-106">Az **Add-AzKeyVaultCertificateContact** parancsmag az Azure Key Vault-ban felvesz egy, a fő boltozathoz tartozó névjegykártyát.</span><span class="sxs-lookup"><span data-stu-id="11052-106">The **Add-AzKeyVaultCertificateContact** cmdlet adds a contact for a key vault for certificate notifications in Azure Key Vault.</span></span>
<span data-ttu-id="11052-107">A névjegy frissítéseket kap az eseményekről, például a tanúsítványról, a Lejáratról, a megújult tanúsítványról stb.</span><span class="sxs-lookup"><span data-stu-id="11052-107">The contact receives updates about events such as certificate close to expiry, certificate renewed, and so on.</span></span>
<span data-ttu-id="11052-108">Ezeket az eseményeket a tanúsítvány-házirend határozza meg.</span><span class="sxs-lookup"><span data-stu-id="11052-108">These events are determined by the certificate policy.</span></span>

## <span data-ttu-id="11052-109">Példák</span><span class="sxs-lookup"><span data-stu-id="11052-109">EXAMPLES</span></span>

### <span data-ttu-id="11052-110">1. példa: kulcs pince-bizonyítvány felvétele</span><span class="sxs-lookup"><span data-stu-id="11052-110">Example 1: Add a key vault certificate contact</span></span>
```
PS C:\>Add-AzKeyVaultCertificateContact -VaultName "ContosoKV01" -EmailAddress "patti.fuller@contoso.com" -PassThru
```

<span data-ttu-id="11052-111">Ehhez a parancshoz a ContosoKV01-kulcs boltozata, és a **KeyVaultCertificateContact** objektumot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="11052-111">This command adds Patti Fuller as a certificate contact for the ContosoKV01 key vault and returns the **KeyVaultCertificateContact** object.</span></span>

## <span data-ttu-id="11052-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="11052-112">PARAMETERS</span></span>

### <span data-ttu-id="11052-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11052-113">-DefaultProfile</span></span>
<span data-ttu-id="11052-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="11052-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11052-115">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="11052-115">-EmailAddress</span></span>
<span data-ttu-id="11052-116">A névjegykártya e-mail-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="11052-116">Specifies the email address of the contact.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11052-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="11052-117">-PassThru</span></span>
<span data-ttu-id="11052-118">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="11052-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="11052-119">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="11052-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="11052-120">-VaultName</span><span class="sxs-lookup"><span data-stu-id="11052-120">-VaultName</span></span>
<span data-ttu-id="11052-121">A fő pince nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="11052-121">Specifies the name of the key vault.</span></span>

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

### <span data-ttu-id="11052-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="11052-122">-Confirm</span></span>
<span data-ttu-id="11052-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="11052-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11052-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11052-124">-WhatIf</span></span>
<span data-ttu-id="11052-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="11052-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11052-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="11052-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11052-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11052-127">CommonParameters</span></span>
<span data-ttu-id="11052-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="11052-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11052-129">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11052-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11052-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="11052-130">INPUTS</span></span>

### <span data-ttu-id="11052-131">Nincs</span><span class="sxs-lookup"><span data-stu-id="11052-131">None</span></span>
<span data-ttu-id="11052-132">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="11052-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="11052-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="11052-133">OUTPUTS</span></span>

### <span data-ttu-id="11052-134">Lista<Microsoft. Azure. Command. KeyVaultCertificateContact. models.></span><span class="sxs-lookup"><span data-stu-id="11052-134">List<Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateContact></span></span>

## <span data-ttu-id="11052-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="11052-135">NOTES</span></span>

## <span data-ttu-id="11052-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="11052-136">RELATED LINKS</span></span>

[<span data-ttu-id="11052-137">Get-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="11052-137">Get-AzKeyVaultCertificateContact</span></span>](./Get-AzKeyVaultCertificateContact.md)

[<span data-ttu-id="11052-138">Remove-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="11052-138">Remove-AzKeyVaultCertificateContact</span></span>](./Remove-AzKeyVaultCertificateContact.md)

