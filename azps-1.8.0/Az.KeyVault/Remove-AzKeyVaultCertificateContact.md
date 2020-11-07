---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 35FAA57F-B2BD-4E43-8238-12F7A8269E4D
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateContact.md
ms.openlocfilehash: 0f1768bec11c5a85e97cdb27e6e9a3195c3880b2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93835701"
---
# <span data-ttu-id="a5e59-101">Remove-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="a5e59-101">Remove-AzKeyVaultCertificateContact</span></span>

## <span data-ttu-id="a5e59-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a5e59-102">SYNOPSIS</span></span>
<span data-ttu-id="a5e59-103">Törli a tanúsítványok értesítéseihez regisztrált névjegykártyát.</span><span class="sxs-lookup"><span data-stu-id="a5e59-103">Deletes a contact that is registered for certificate notifications from a key vault.</span></span>

## <span data-ttu-id="a5e59-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a5e59-104">SYNTAX</span></span>

### <span data-ttu-id="a5e59-105">ByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a5e59-105">ByName (Default)</span></span>
```
Remove-AzKeyVaultCertificateContact [-VaultName] <String> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5e59-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="a5e59-106">ByObject</span></span>
```
Remove-AzKeyVaultCertificateContact [-InputObject] <PSKeyVault> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5e59-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a5e59-107">ByResourceId</span></span>
```
Remove-AzKeyVaultCertificateContact [-ResourceId] <String> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5e59-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="a5e59-108">DESCRIPTION</span></span>
<span data-ttu-id="a5e59-109">A **Remove-AzKeyVaultCertificateContact** parancsmag törli a tanúsítványok értesítéseihez regisztrált ügyfelet.</span><span class="sxs-lookup"><span data-stu-id="a5e59-109">The **Remove-AzKeyVaultCertificateContact** cmdlet deletes a contact that is registered for certificate notifications from a key vault.</span></span>

## <span data-ttu-id="a5e59-110">Példák</span><span class="sxs-lookup"><span data-stu-id="a5e59-110">EXAMPLES</span></span>

### <span data-ttu-id="a5e59-111">1. példa: a tanúsítvány-névjegykártya eltávolítása</span><span class="sxs-lookup"><span data-stu-id="a5e59-111">Example 1: Remove a certificate contact</span></span>
```powershell
PS C:\> Remove-AzKeyVaultCertificateContact -VaultName "Contoso01" -EmailAddress "patti.fuller@contoso.com" -PassThru

Email               VaultName
-----               ---------
user1@microsoft.com mvault2
user2@microsoft.com mvault2
user3@microsoft.com mvault2
user4@microsoft.com mvault2
```

<span data-ttu-id="a5e59-112">Ez a parancs eltávolítja a Patti Fuller-t a Contoso01-kulcs boltozatához.</span><span class="sxs-lookup"><span data-stu-id="a5e59-112">This command removes Patti Fuller as a certificate contact for the Contoso01 key vault.</span></span>  <span data-ttu-id="a5e59-113">Ha a PassThru meg van adva, a parancsmag a fennmaradó tanúsítvány-névjegyek listáját adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="a5e59-113">If PassThru is specified, the cmdlet returns the list of remaining certificate contacts.</span></span>

## <span data-ttu-id="a5e59-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a5e59-114">PARAMETERS</span></span>

### <span data-ttu-id="a5e59-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5e59-115">-DefaultProfile</span></span>
<span data-ttu-id="a5e59-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="a5e59-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a5e59-117">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="a5e59-117">-EmailAddress</span></span>
<span data-ttu-id="a5e59-118">Az eltávolítandó ügyfél e-mail-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a5e59-118">Specifies the email address of the contact to remove.</span></span>

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

### <span data-ttu-id="a5e59-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a5e59-119">-InputObject</span></span>
<span data-ttu-id="a5e59-120">A boltozat objektum.</span><span class="sxs-lookup"><span data-stu-id="a5e59-120">KeyVault object.</span></span>

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

### <span data-ttu-id="a5e59-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a5e59-121">-PassThru</span></span>
<span data-ttu-id="a5e59-122">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="a5e59-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="a5e59-123">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="a5e59-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a5e59-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a5e59-124">-ResourceId</span></span>
<span data-ttu-id="a5e59-125">A főkészlet erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="a5e59-125">KeyVault Resource Id.</span></span>

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

### <span data-ttu-id="a5e59-126">-VaultName</span><span class="sxs-lookup"><span data-stu-id="a5e59-126">-VaultName</span></span>
<span data-ttu-id="a5e59-127">A kulcsfájl nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a5e59-127">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="a5e59-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a5e59-128">-Confirm</span></span>
<span data-ttu-id="a5e59-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a5e59-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5e59-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5e59-130">-WhatIf</span></span>
<span data-ttu-id="a5e59-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a5e59-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5e59-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a5e59-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5e59-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5e59-133">CommonParameters</span></span>
<span data-ttu-id="a5e59-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a5e59-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5e59-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5e59-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5e59-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a5e59-136">INPUTS</span></span>

### <span data-ttu-id="a5e59-137">Microsoft. Azure. Command. PSKeyVault. models.</span><span class="sxs-lookup"><span data-stu-id="a5e59-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="a5e59-138">System. String</span><span class="sxs-lookup"><span data-stu-id="a5e59-138">System.String</span></span>

## <span data-ttu-id="a5e59-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a5e59-139">OUTPUTS</span></span>

### <span data-ttu-id="a5e59-140">Microsoft. Azure. Command. PSKeyVaultCertificateContact. models.</span><span class="sxs-lookup"><span data-stu-id="a5e59-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact</span></span>

## <span data-ttu-id="a5e59-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a5e59-141">NOTES</span></span>

## <span data-ttu-id="a5e59-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a5e59-142">RELATED LINKS</span></span>

[<span data-ttu-id="a5e59-143">Add-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="a5e59-143">Add-AzKeyVaultCertificateContact</span></span>](./Add-AzKeyVaultCertificateContact.md)

[<span data-ttu-id="a5e59-144">Get-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="a5e59-144">Get-AzKeyVaultCertificateContact</span></span>](./Get-AzKeyVaultCertificateContact.md)

