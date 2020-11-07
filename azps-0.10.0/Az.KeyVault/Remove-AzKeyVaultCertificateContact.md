---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 35FAA57F-B2BD-4E43-8238-12F7A8269E4D
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/remove-AzKeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateContact.md
ms.openlocfilehash: 0b92fcb3725d42ac7c2978600f7903d6bf7f6142
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842117"
---
# <span data-ttu-id="7add9-101">Remove-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="7add9-101">Remove-AzKeyVaultCertificateContact</span></span>

## <span data-ttu-id="7add9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7add9-102">SYNOPSIS</span></span>
<span data-ttu-id="7add9-103">Törli a tanúsítványok értesítéseihez regisztrált névjegykártyát.</span><span class="sxs-lookup"><span data-stu-id="7add9-103">Deletes a contact that is registered for certificate notifications from a key vault.</span></span>

## <span data-ttu-id="7add9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7add9-104">SYNTAX</span></span>

```
Remove-AzKeyVaultCertificateContact [-VaultName] <String> [-EmailAddress] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7add9-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7add9-105">DESCRIPTION</span></span>
<span data-ttu-id="7add9-106">A **Remove-AzKeyVaultCertificateContact** parancsmag törli a tanúsítványok értesítéseihez regisztrált ügyfelet.</span><span class="sxs-lookup"><span data-stu-id="7add9-106">The **Remove-AzKeyVaultCertificateContact** cmdlet deletes a contact that is registered for certificate notifications from a key vault.</span></span>

## <span data-ttu-id="7add9-107">Példák</span><span class="sxs-lookup"><span data-stu-id="7add9-107">EXAMPLES</span></span>

### <span data-ttu-id="7add9-108">1. példa: a tanúsítvány-névjegykártya eltávolítása</span><span class="sxs-lookup"><span data-stu-id="7add9-108">Example 1: Remove a certificate contact</span></span>
```
PS C:\>Remove-AzKeyVaultCertificateContact -VaultName "Contoso01" -EmailAddress "patti.fuller@contoso.com"
```

<span data-ttu-id="7add9-109">Ez a parancs eltávolítja a Patti Fuller-t a Contoso01-kulcs boltozatához.</span><span class="sxs-lookup"><span data-stu-id="7add9-109">This command removes Patti Fuller as a certificate contact for the Contoso01 key vault.</span></span>

## <span data-ttu-id="7add9-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7add9-110">PARAMETERS</span></span>

### <span data-ttu-id="7add9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7add9-111">-DefaultProfile</span></span>
<span data-ttu-id="7add9-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="7add9-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7add9-113">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="7add9-113">-EmailAddress</span></span>
<span data-ttu-id="7add9-114">Az eltávolítandó ügyfél e-mail-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7add9-114">Specifies the email address of the contact to remove.</span></span>

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

### <span data-ttu-id="7add9-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7add9-115">-PassThru</span></span>
<span data-ttu-id="7add9-116">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="7add9-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="7add9-117">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="7add9-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="7add9-118">-VaultName</span><span class="sxs-lookup"><span data-stu-id="7add9-118">-VaultName</span></span>
<span data-ttu-id="7add9-119">A kulcsfájl nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7add9-119">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="7add9-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7add9-120">-Confirm</span></span>
<span data-ttu-id="7add9-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7add9-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7add9-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7add9-122">-WhatIf</span></span>
<span data-ttu-id="7add9-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7add9-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7add9-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7add9-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7add9-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7add9-125">CommonParameters</span></span>
<span data-ttu-id="7add9-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7add9-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7add9-127">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7add9-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7add9-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7add9-128">INPUTS</span></span>

### <span data-ttu-id="7add9-129">Nincs</span><span class="sxs-lookup"><span data-stu-id="7add9-129">None</span></span>
<span data-ttu-id="7add9-130">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="7add9-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7add9-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7add9-131">OUTPUTS</span></span>

### <span data-ttu-id="7add9-132">System. Collections. Generic. list ' 1 [Microsoft. Azure. commands. devault. models. KeyVaultCertificateContact]</span><span class="sxs-lookup"><span data-stu-id="7add9-132">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateContact]</span></span>

## <span data-ttu-id="7add9-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7add9-133">NOTES</span></span>

## <span data-ttu-id="7add9-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7add9-134">RELATED LINKS</span></span>

[<span data-ttu-id="7add9-135">Add-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="7add9-135">Add-AzKeyVaultCertificateContact</span></span>](./Add-AzKeyVaultCertificateContact.md)

[<span data-ttu-id="7add9-136">Get-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="7add9-136">Get-AzKeyVaultCertificateContact</span></span>](./Get-AzKeyVaultCertificateContact.md)

