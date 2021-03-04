---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 70DB088D-4AF5-406B-8D66-118A0F766041
online version: https://docs.microsoft.com/powershell/module/az.keyvault/restore-azkeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultSecret.md
ms.openlocfilehash: 56f5279b1d3645717a29e392fd45599344515a29
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101931833"
---
# <span data-ttu-id="16525-101">Restore-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="16525-101">Restore-AzKeyVaultSecret</span></span>

## <span data-ttu-id="16525-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16525-102">SYNOPSIS</span></span>
<span data-ttu-id="16525-103">Egy titkos kulcsot hoz létre egy kulcstárban egy biztonságimentett titkos kulcsból.</span><span class="sxs-lookup"><span data-stu-id="16525-103">Creates a secret in a key vault from a backed-up secret.</span></span>

## <span data-ttu-id="16525-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="16525-104">SYNTAX</span></span>

### <span data-ttu-id="16525-105">ByVaultName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="16525-105">ByVaultName (Default)</span></span>
```
Restore-AzKeyVaultSecret [-VaultName] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16525-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="16525-106">ByInputObject</span></span>
```
Restore-AzKeyVaultSecret [-InputObject] <PSKeyVault> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16525-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="16525-107">ByResourceId</span></span>
```
Restore-AzKeyVaultSecret [-ResourceId] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16525-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="16525-108">DESCRIPTION</span></span>
<span data-ttu-id="16525-109">A **Restore-AzKeyVaultSecret** parancsmag létrehoz egy titkos kulcsot a megadott kulcstárban.</span><span class="sxs-lookup"><span data-stu-id="16525-109">The **Restore-AzKeyVaultSecret** cmdlet creates a secret in the specified key vault.</span></span>
<span data-ttu-id="16525-110">Ez a titkos adat a bemeneti fájlban található biztonsági másolat másolata, és neve megegyezik az eredetivel.</span><span class="sxs-lookup"><span data-stu-id="16525-110">This secret is a replica of the backed-up secret in the input file and has the same name as the original secret.</span></span>
<span data-ttu-id="16525-111">Ha a kulcstárnak már van ugyanaz a neve, a parancsmag nem tudja felülírni az eredetit.</span><span class="sxs-lookup"><span data-stu-id="16525-111">If the key vault already has a secret by the same name, this cmdlet fails instead of overwriting the original secret.</span></span>
<span data-ttu-id="16525-112">Ha a biztonsági másolat egy titkos fájl több verzióját tartalmazza, a rendszer az összes verziót visszaállítja.</span><span class="sxs-lookup"><span data-stu-id="16525-112">If the backup contains multiple versions of a secret, all versions are restored.</span></span>
<span data-ttu-id="16525-113">Az a kulcstár, amelybe visszaállítja a titkos kulcsot, különbözik attól a kulcstártól, amelyről a titkos kulcsot biztonsági másolatként tárolta.</span><span class="sxs-lookup"><span data-stu-id="16525-113">The key vault that you restore the secret into can be different from the key vault that you backed up the secret from.</span></span>
<span data-ttu-id="16525-114">A kulcstárnak azonban ugyanazt az előfizetést kell használnia, és ugyanabban a földrajzi régióban (például Észak-Amerikában) kell lennie egy Azure-régióban.</span><span class="sxs-lookup"><span data-stu-id="16525-114">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="16525-115">Az Azure-régiók földrajzokkal való megfeleltetését a Microsoft Azure Trust Center https://azure.microsoft.com/support/trust-center/) webhelyén tudja meg.</span><span class="sxs-lookup"><span data-stu-id="16525-115">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="16525-116">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="16525-116">EXAMPLES</span></span>

### <span data-ttu-id="16525-117">1. példa: Biztonsági másolat visszaállítása</span><span class="sxs-lookup"><span data-stu-id="16525-117">Example 1: Restore a backed-up secret</span></span>
```powershell
PS C:\> Restore-AzKeyVaultSecret -VaultName 'contoso' -InputFile "C:\Backup.blob"

Vault Name   : contoso
Name         : secret1
Version      : 7128133570f84a71b48d7d0550deb74c
Id           : https://contoso.vault.azure.net:443/secrets/secret1/7128133570f84a71b48d7d0550deb74c
Enabled      : True
Expires      : 4/6/2018 3:59:43 PM
Not Before   :
Created      : 4/5/2018 11:46:28 PM
Updated      : 4/6/2018 11:30:17 PM
Content Type :
Tags         :
```

<span data-ttu-id="16525-118">Ez a parancs a Biztonsági másolat.blob nevű biztonságimásolat-fájlból a contoso nevű kulcstárolóba visszaállít egy titkos másolatot, annak minden verziójával együtt.</span><span class="sxs-lookup"><span data-stu-id="16525-118">This command restores a secret, including all of its versions, from the backup file named Backup.blob into the key vault named contoso.</span></span>

## <span data-ttu-id="16525-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="16525-119">PARAMETERS</span></span>

### <span data-ttu-id="16525-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16525-120">-DefaultProfile</span></span>
<span data-ttu-id="16525-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="16525-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="16525-122">-InputFile</span><span class="sxs-lookup"><span data-stu-id="16525-122">-InputFile</span></span>
<span data-ttu-id="16525-123">Azt a bemeneti fájlt adja meg, amely a visszaállítani kívánt titkos fájl biztonsági másolatát tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="16525-123">Specifies the input file that contains the backup of the secret to restore.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16525-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="16525-124">-InputObject</span></span>
<span data-ttu-id="16525-125">KeyVault objektum</span><span class="sxs-lookup"><span data-stu-id="16525-125">KeyVault object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="16525-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="16525-126">-ResourceId</span></span>
<span data-ttu-id="16525-127">KeyVault Resource Id</span><span class="sxs-lookup"><span data-stu-id="16525-127">KeyVault Resource Id</span></span>

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

### <span data-ttu-id="16525-128">-VaultName</span><span class="sxs-lookup"><span data-stu-id="16525-128">-VaultName</span></span>
<span data-ttu-id="16525-129">Annak a kulcstárnak a nevét adja meg, amelybe vissza kell állítani a titkos kulcsot.</span><span class="sxs-lookup"><span data-stu-id="16525-129">Specifies the name of the key vault into which to restore the secret.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16525-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="16525-130">-Confirm</span></span>
<span data-ttu-id="16525-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="16525-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16525-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16525-132">-WhatIf</span></span>
<span data-ttu-id="16525-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="16525-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16525-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="16525-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16525-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16525-135">CommonParameters</span></span>
<span data-ttu-id="16525-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16525-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16525-137">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="16525-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16525-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="16525-138">INPUTS</span></span>

### <span data-ttu-id="16525-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="16525-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="16525-140">System.String</span><span class="sxs-lookup"><span data-stu-id="16525-140">System.String</span></span>

## <span data-ttu-id="16525-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="16525-141">OUTPUTS</span></span>

### <span data-ttu-id="16525-142">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="16525-142">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

## <span data-ttu-id="16525-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="16525-143">NOTES</span></span>

## <span data-ttu-id="16525-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="16525-144">RELATED LINKS</span></span>

[<span data-ttu-id="16525-145">Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="16525-145">Set-AzKeyVaultSecret</span></span>](./Set-AzKeyVaultSecret.md)

[<span data-ttu-id="16525-146">Backup-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="16525-146">Backup-AzKeyVaultSecret</span></span>](./Backup-AzKeyVaultSecret.md)

[<span data-ttu-id="16525-147">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="16525-147">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)

[<span data-ttu-id="16525-148">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="16525-148">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)

