---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 35FAA57F-B2BD-4E43-8238-12F7A8269E4D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificateContact.md
ms.openlocfilehash: aee18adf3530976af4b17ffa15f94624248a7db7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496068"
---
# <span data-ttu-id="1c10f-101">Remove-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="1c10f-101">Remove-AzureKeyVaultCertificateContact</span></span>

## <span data-ttu-id="1c10f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1c10f-102">SYNOPSIS</span></span>
<span data-ttu-id="1c10f-103">Törli a tanúsítványok értesítéseihez regisztrált névjegykártyát.</span><span class="sxs-lookup"><span data-stu-id="1c10f-103">Deletes a contact that is registered for certificate notifications from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1c10f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1c10f-104">SYNTAX</span></span>

### <span data-ttu-id="1c10f-105">ByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1c10f-105">ByName (Default)</span></span>
```
Remove-AzureKeyVaultCertificateContact [-VaultName] <String> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c10f-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="1c10f-106">ByObject</span></span>
```
Remove-AzureKeyVaultCertificateContact [-InputObject] <PSKeyVault> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c10f-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="1c10f-107">ByResourceId</span></span>
```
Remove-AzureKeyVaultCertificateContact [-ResourceId] <String> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c10f-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="1c10f-108">DESCRIPTION</span></span>
<span data-ttu-id="1c10f-109">A **Remove-AzureKeyVaultCertificateContact** parancsmag törli a tanúsítványok értesítéseihez regisztrált ügyfelet.</span><span class="sxs-lookup"><span data-stu-id="1c10f-109">The **Remove-AzureKeyVaultCertificateContact** cmdlet deletes a contact that is registered for certificate notifications from a key vault.</span></span>

## <span data-ttu-id="1c10f-110">Példák</span><span class="sxs-lookup"><span data-stu-id="1c10f-110">EXAMPLES</span></span>

### <span data-ttu-id="1c10f-111">1. példa: a tanúsítvány-névjegykártya eltávolítása</span><span class="sxs-lookup"><span data-stu-id="1c10f-111">Example 1: Remove a certificate contact</span></span>
```powershell
PS C:\> Remove-AzureKeyVaultCertificateContact -VaultName "Contoso01" -EmailAddress "patti.fuller@contoso.com" -PassThru

Email               VaultName
-----               ---------
user1@microsoft.com mvault2
user2@microsoft.com mvault2
user3@microsoft.com mvault2
user4@microsoft.com mvault2
```

<span data-ttu-id="1c10f-112">Ez a parancs eltávolítja a Patti Fuller-t a Contoso01-kulcs boltozatához.</span><span class="sxs-lookup"><span data-stu-id="1c10f-112">This command removes Patti Fuller as a certificate contact for the Contoso01 key vault.</span></span>  <span data-ttu-id="1c10f-113">Ha a PassThru meg van adva, a parancsmag a fennmaradó tanúsítvány-névjegyek listáját adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="1c10f-113">If PassThru is specified, the cmdlet returns the list of remaining certificate contacts.</span></span>

## <span data-ttu-id="1c10f-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1c10f-114">PARAMETERS</span></span>

### <span data-ttu-id="1c10f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c10f-115">-DefaultProfile</span></span>
<span data-ttu-id="1c10f-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="1c10f-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1c10f-117">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="1c10f-117">-EmailAddress</span></span>
<span data-ttu-id="1c10f-118">Az eltávolítandó ügyfél e-mail-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1c10f-118">Specifies the email address of the contact to remove.</span></span>

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

### <span data-ttu-id="1c10f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1c10f-119">-InputObject</span></span>
<span data-ttu-id="1c10f-120">A boltozat objektum.</span><span class="sxs-lookup"><span data-stu-id="1c10f-120">KeyVault object.</span></span>

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

### <span data-ttu-id="1c10f-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1c10f-121">-PassThru</span></span>
<span data-ttu-id="1c10f-122">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="1c10f-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="1c10f-123">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="1c10f-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="1c10f-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1c10f-124">-ResourceId</span></span>
<span data-ttu-id="1c10f-125">A főkészlet erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="1c10f-125">KeyVault Resource Id.</span></span>

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

### <span data-ttu-id="1c10f-126">-VaultName</span><span class="sxs-lookup"><span data-stu-id="1c10f-126">-VaultName</span></span>
<span data-ttu-id="1c10f-127">A kulcsfájl nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1c10f-127">Specifies the name of a key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c10f-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="1c10f-128">-Confirm</span></span>
<span data-ttu-id="1c10f-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1c10f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c10f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c10f-130">-WhatIf</span></span>
<span data-ttu-id="1c10f-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="1c10f-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1c10f-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1c10f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c10f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c10f-133">CommonParameters</span></span>
<span data-ttu-id="1c10f-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1c10f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c10f-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c10f-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c10f-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1c10f-136">INPUTS</span></span>

### <span data-ttu-id="1c10f-137">Microsoft. Azure. Command. PSKeyVault. models.</span><span class="sxs-lookup"><span data-stu-id="1c10f-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>
<span data-ttu-id="1c10f-138">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="1c10f-138">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="1c10f-139">System. String</span><span class="sxs-lookup"><span data-stu-id="1c10f-139">System.String</span></span>

## <span data-ttu-id="1c10f-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1c10f-140">OUTPUTS</span></span>

### <span data-ttu-id="1c10f-141">Microsoft. Azure. Command. PSKeyVaultCertificateContact. models.</span><span class="sxs-lookup"><span data-stu-id="1c10f-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact</span></span>

## <span data-ttu-id="1c10f-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1c10f-142">NOTES</span></span>

## <span data-ttu-id="1c10f-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1c10f-143">RELATED LINKS</span></span>

[<span data-ttu-id="1c10f-144">Add-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="1c10f-144">Add-AzureKeyVaultCertificateContact</span></span>](./Add-AzureKeyVaultCertificateContact.md)

[<span data-ttu-id="1c10f-145">Get-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="1c10f-145">Get-AzureKeyVaultCertificateContact</span></span>](./Get-AzureKeyVaultCertificateContact.md)

