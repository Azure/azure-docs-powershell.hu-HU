---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 35FAA57F-B2BD-4E43-8238-12F7A8269E4D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificateContact.md
ms.openlocfilehash: 1fbf5a5541fe3e1360e696f9c06a26d6ea131dc0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502720"
---
# <span data-ttu-id="3cff9-101">Remove-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="3cff9-101">Remove-AzureKeyVaultCertificateContact</span></span>

## <span data-ttu-id="3cff9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3cff9-102">SYNOPSIS</span></span>
<span data-ttu-id="3cff9-103">Törli a tanúsítványok értesítéseihez regisztrált névjegykártyát.</span><span class="sxs-lookup"><span data-stu-id="3cff9-103">Deletes a contact that is registered for certificate notifications from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3cff9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3cff9-104">SYNTAX</span></span>

```
Remove-AzureKeyVaultCertificateContact [-VaultName] <String> [-EmailAddress] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3cff9-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3cff9-105">DESCRIPTION</span></span>
<span data-ttu-id="3cff9-106">A **Remove-AzureKeyVaultCertificateContact** parancsmag törli a tanúsítványok értesítéseihez regisztrált ügyfelet.</span><span class="sxs-lookup"><span data-stu-id="3cff9-106">The **Remove-AzureKeyVaultCertificateContact** cmdlet deletes a contact that is registered for certificate notifications from a key vault.</span></span>

## <span data-ttu-id="3cff9-107">Példák</span><span class="sxs-lookup"><span data-stu-id="3cff9-107">EXAMPLES</span></span>

### <span data-ttu-id="3cff9-108">1. példa: a tanúsítvány-névjegykártya eltávolítása</span><span class="sxs-lookup"><span data-stu-id="3cff9-108">Example 1: Remove a certificate contact</span></span>
```
PS C:\>Remove-AzureKeyVaultCertificateContact -VaultName "Contoso01" -EmailAddress "patti.fuller@contoso.com"
```

<span data-ttu-id="3cff9-109">Ez a parancs eltávolítja a Patti Fuller-t a Contoso01-kulcs boltozatához.</span><span class="sxs-lookup"><span data-stu-id="3cff9-109">This command removes Patti Fuller as a certificate contact for the Contoso01 key vault.</span></span>

## <span data-ttu-id="3cff9-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3cff9-110">PARAMETERS</span></span>

### <span data-ttu-id="3cff9-111">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="3cff9-111">-EmailAddress</span></span>
<span data-ttu-id="3cff9-112">Az eltávolítandó ügyfél e-mail-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3cff9-112">Specifies the email address of the contact to remove.</span></span>

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

### <span data-ttu-id="3cff9-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3cff9-113">-PassThru</span></span>
<span data-ttu-id="3cff9-114">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="3cff9-114">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="3cff9-115">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="3cff9-115">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3cff9-116">-VaultName</span><span class="sxs-lookup"><span data-stu-id="3cff9-116">-VaultName</span></span>
<span data-ttu-id="3cff9-117">A kulcsfájl nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3cff9-117">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="3cff9-118">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3cff9-118">-Confirm</span></span>
<span data-ttu-id="3cff9-119">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3cff9-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3cff9-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3cff9-120">-WhatIf</span></span>
<span data-ttu-id="3cff9-121">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3cff9-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3cff9-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3cff9-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3cff9-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cff9-123">-DefaultProfile</span></span>
<span data-ttu-id="3cff9-124">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3cff9-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3cff9-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cff9-125">CommonParameters</span></span>
<span data-ttu-id="3cff9-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3cff9-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cff9-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3cff9-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cff9-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3cff9-128">INPUTS</span></span>

## <span data-ttu-id="3cff9-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3cff9-129">OUTPUTS</span></span>

### <span data-ttu-id="3cff9-130">System. Collections. Generic. list ' 1 [Microsoft. Azure. commands. devault. models. KeyVaultCertificateContact]</span><span class="sxs-lookup"><span data-stu-id="3cff9-130">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateContact]</span></span>

## <span data-ttu-id="3cff9-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3cff9-131">NOTES</span></span>

## <span data-ttu-id="3cff9-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3cff9-132">RELATED LINKS</span></span>

[<span data-ttu-id="3cff9-133">Add-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="3cff9-133">Add-AzureKeyVaultCertificateContact</span></span>](./Add-AzureKeyVaultCertificateContact.md)

[<span data-ttu-id="3cff9-134">Get-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="3cff9-134">Get-AzureKeyVaultCertificateContact</span></span>](./Get-AzureKeyVaultCertificateContact.md)

