---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 70DB088D-4AF5-406B-8D66-118A0F766041
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/restore-azkeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultSecret.md
ms.openlocfilehash: 5a00bab81cad7b77873459ab58615a2836970b09
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181712"
---
# <span data-ttu-id="ccf17-101">Restore-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="ccf17-101">Restore-AzKeyVaultSecret</span></span>

## <span data-ttu-id="ccf17-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ccf17-102">SYNOPSIS</span></span>
<span data-ttu-id="ccf17-103">Titkos kulccsal elkészített titkos kulccsal hoz létre titkos kulcsot.</span><span class="sxs-lookup"><span data-stu-id="ccf17-103">Creates a secret in a key vault from a backed-up secret.</span></span>

## <span data-ttu-id="ccf17-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ccf17-104">SYNTAX</span></span>

### <span data-ttu-id="ccf17-105">ByVaultName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ccf17-105">ByVaultName (Default)</span></span>
```
Restore-AzKeyVaultSecret [-VaultName] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ccf17-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="ccf17-106">ByInputObject</span></span>
```
Restore-AzKeyVaultSecret [-InputObject] <PSKeyVault> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ccf17-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ccf17-107">ByResourceId</span></span>
```
Restore-AzKeyVaultSecret [-ResourceId] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ccf17-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="ccf17-108">DESCRIPTION</span></span>
<span data-ttu-id="ccf17-109">A **Restore-AzKeyVaultSecret** parancsmag titkot hoz létre a megadott kulcs boltozata alatt.</span><span class="sxs-lookup"><span data-stu-id="ccf17-109">The **Restore-AzKeyVaultSecret** cmdlet creates a secret in the specified key vault.</span></span>
<span data-ttu-id="ccf17-110">Ez a titok a bemeneti fájlban lévő mentett titok másolata, és az eredeti titok nevével megegyező.</span><span class="sxs-lookup"><span data-stu-id="ccf17-110">This secret is a replica of the backed-up secret in the input file and has the same name as the original secret.</span></span>
<span data-ttu-id="ccf17-111">Ha a kulcs boltozata már rendelkezik ugyanazzal a névvel, a parancsmag nem felülírja az eredeti titkot.</span><span class="sxs-lookup"><span data-stu-id="ccf17-111">If the key vault already has a secret by the same name, this cmdlet fails instead of overwriting the original secret.</span></span>
<span data-ttu-id="ccf17-112">Ha a biztonsági másolat több titkos verziót tartalmaz, az összes verzió visszaállítása visszakerül.</span><span class="sxs-lookup"><span data-stu-id="ccf17-112">If the backup contains multiple versions of a secret, all versions are restored.</span></span>
<span data-ttu-id="ccf17-113">A titkot visszaadó kulcsfájl eltérhet attól a fő boltozattól, amelyről biztonsági másolatot készített.</span><span class="sxs-lookup"><span data-stu-id="ccf17-113">The key vault that you restore the secret into can be different from the key vault that you backed up the secret from.</span></span>
<span data-ttu-id="ccf17-114">A kulcs boltozatának azonban ugyanazt az előfizetést kell használnia, és egy Azure-régióban kell lennie ugyanazon a földrajzon (például Észak-Amerikában).</span><span class="sxs-lookup"><span data-stu-id="ccf17-114">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="ccf17-115">Lásd: a Microsoft Azure Trust Center ( https://azure.microsoft.com/support/trust-center/) Az Azure-régiók földrajzi megfeleltetéséhez.</span><span class="sxs-lookup"><span data-stu-id="ccf17-115">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="ccf17-116">Példák</span><span class="sxs-lookup"><span data-stu-id="ccf17-116">EXAMPLES</span></span>

### <span data-ttu-id="ccf17-117">Példa 1: biztonsági mentett titok visszaállítása</span><span class="sxs-lookup"><span data-stu-id="ccf17-117">Example 1: Restore a backed-up secret</span></span>
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

<span data-ttu-id="ccf17-118">Ez a parancs visszaállít egy titkot, benne az összes változatát, a biztonsági másolat. blob nevű biztonsági másolatból a contoso nevű biztonsági mentési fájlból.</span><span class="sxs-lookup"><span data-stu-id="ccf17-118">This command restores a secret, including all of its versions, from the backup file named Backup.blob into the key vault named contoso.</span></span>

## <span data-ttu-id="ccf17-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ccf17-119">PARAMETERS</span></span>

### <span data-ttu-id="ccf17-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccf17-120">-DefaultProfile</span></span>
<span data-ttu-id="ccf17-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="ccf17-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ccf17-122">-InputFile</span><span class="sxs-lookup"><span data-stu-id="ccf17-122">-InputFile</span></span>
<span data-ttu-id="ccf17-123">Azt a bemeneti fájlt adja meg, amely a visszaállítandó titok biztonsági másolatát tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="ccf17-123">Specifies the input file that contains the backup of the secret to restore.</span></span>

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

### <span data-ttu-id="ccf17-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ccf17-124">-InputObject</span></span>
<span data-ttu-id="ccf17-125">A boltozat objektum</span><span class="sxs-lookup"><span data-stu-id="ccf17-125">KeyVault object</span></span>

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

### <span data-ttu-id="ccf17-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ccf17-126">-ResourceId</span></span>
<span data-ttu-id="ccf17-127">A főkészlet erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="ccf17-127">KeyVault Resource Id</span></span>

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

### <span data-ttu-id="ccf17-128">-VaultName</span><span class="sxs-lookup"><span data-stu-id="ccf17-128">-VaultName</span></span>
<span data-ttu-id="ccf17-129">Annak a kulcsnak a nevét adja meg, amelybe vissza szeretné állítani a titkot.</span><span class="sxs-lookup"><span data-stu-id="ccf17-129">Specifies the name of the key vault into which to restore the secret.</span></span>

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

### <span data-ttu-id="ccf17-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ccf17-130">-Confirm</span></span>
<span data-ttu-id="ccf17-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ccf17-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ccf17-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ccf17-132">-WhatIf</span></span>
<span data-ttu-id="ccf17-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ccf17-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ccf17-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ccf17-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ccf17-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccf17-135">CommonParameters</span></span>
<span data-ttu-id="ccf17-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ccf17-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccf17-137">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ccf17-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccf17-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ccf17-138">INPUTS</span></span>

### <span data-ttu-id="ccf17-139">Microsoft. Azure. Command. PSKeyVault. models.</span><span class="sxs-lookup"><span data-stu-id="ccf17-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="ccf17-140">System. String</span><span class="sxs-lookup"><span data-stu-id="ccf17-140">System.String</span></span>

## <span data-ttu-id="ccf17-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ccf17-141">OUTPUTS</span></span>

### <span data-ttu-id="ccf17-142">Microsoft. Azure. Command. PSKeyVaultSecret. models.</span><span class="sxs-lookup"><span data-stu-id="ccf17-142">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

## <span data-ttu-id="ccf17-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ccf17-143">NOTES</span></span>

## <span data-ttu-id="ccf17-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ccf17-144">RELATED LINKS</span></span>

[<span data-ttu-id="ccf17-145">Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="ccf17-145">Set-AzKeyVaultSecret</span></span>](./Set-AzKeyVaultSecret.md)

[<span data-ttu-id="ccf17-146">Backup-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="ccf17-146">Backup-AzKeyVaultSecret</span></span>](./Backup-AzKeyVaultSecret.md)

[<span data-ttu-id="ccf17-147">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="ccf17-147">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)

[<span data-ttu-id="ccf17-148">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="ccf17-148">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)

