---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 70DB088D-4AF5-406B-8D66-118A0F766041
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/restore-azurekeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Restore-AzureKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Restore-AzureKeyVaultSecret.md
ms.openlocfilehash: ea2478225c3e5b3c0a3746a44aca13745e1af963
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672247"
---
# <span data-ttu-id="03129-101">Restore-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="03129-101">Restore-AzureKeyVaultSecret</span></span>

## <span data-ttu-id="03129-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="03129-102">SYNOPSIS</span></span>
<span data-ttu-id="03129-103">Titkos kulccsal elkészített titkos kulccsal hoz létre titkos kulcsot.</span><span class="sxs-lookup"><span data-stu-id="03129-103">Creates a secret in a key vault from a backed-up secret.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="03129-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="03129-104">SYNTAX</span></span>

### <span data-ttu-id="03129-105">ByVaultName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="03129-105">ByVaultName (Default)</span></span>
```
Restore-AzureKeyVaultSecret [-VaultName] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03129-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="03129-106">ByInputObject</span></span>
```
Restore-AzureKeyVaultSecret [-InputObject] <PSKeyVault> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03129-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="03129-107">ByResourceId</span></span>
```
Restore-AzureKeyVaultSecret [-ResourceId] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03129-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="03129-108">DESCRIPTION</span></span>
<span data-ttu-id="03129-109">A **Restore-AzureKeyVaultSecret** parancsmag titkot hoz létre a megadott kulcs boltozata alatt.</span><span class="sxs-lookup"><span data-stu-id="03129-109">The **Restore-AzureKeyVaultSecret** cmdlet creates a secret in the specified key vault.</span></span>
<span data-ttu-id="03129-110">Ez a titok a bemeneti fájlban lévő mentett titok másolata, és az eredeti titok nevével megegyező.</span><span class="sxs-lookup"><span data-stu-id="03129-110">This secret is a replica of the backed-up secret in the input file and has the same name as the original secret.</span></span>
<span data-ttu-id="03129-111">Ha a kulcs boltozata már rendelkezik ugyanazzal a névvel, a parancsmag nem felülírja az eredeti titkot.</span><span class="sxs-lookup"><span data-stu-id="03129-111">If the key vault already has a secret by the same name, this cmdlet fails instead of overwriting the original secret.</span></span>
<span data-ttu-id="03129-112">Ha a biztonsági másolat több titkos verziót tartalmaz, az összes verzió visszaállítása visszakerül.</span><span class="sxs-lookup"><span data-stu-id="03129-112">If the backup contains multiple versions of a secret, all versions are restored.</span></span>
<span data-ttu-id="03129-113">A titkot visszaadó kulcsfájl eltérhet attól a fő boltozattól, amelyről biztonsági másolatot készített.</span><span class="sxs-lookup"><span data-stu-id="03129-113">The key vault that you restore the secret into can be different from the key vault that you backed up the secret from.</span></span>
<span data-ttu-id="03129-114">A kulcs boltozatának azonban ugyanazt az előfizetést kell használnia, és egy Azure-régióban kell lennie ugyanazon a földrajzon (például Észak-Amerikában).</span><span class="sxs-lookup"><span data-stu-id="03129-114">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="03129-115">Lásd: a Microsoft Azure Trust Center ( https://azure.microsoft.com/support/trust-center/) Az Azure-régiók földrajzi megfeleltetéséhez.</span><span class="sxs-lookup"><span data-stu-id="03129-115">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="03129-116">Példák</span><span class="sxs-lookup"><span data-stu-id="03129-116">EXAMPLES</span></span>

### <span data-ttu-id="03129-117">Példa 1: biztonsági mentett titok visszaállítása</span><span class="sxs-lookup"><span data-stu-id="03129-117">Example 1: Restore a backed-up secret</span></span>
```powershell
PS C:\> Restore-AzureKeyVaultSecret -VaultName 'contoso' -InputFile "C:\Backup.blob"

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

<span data-ttu-id="03129-118">Ez a parancs visszaállít egy titkot, benne az összes változatát, a biztonsági másolat. blob nevű biztonsági másolatból a contoso nevű biztonsági mentési fájlból.</span><span class="sxs-lookup"><span data-stu-id="03129-118">This command restores a secret, including all of its versions, from the backup file named Backup.blob into the key vault named contoso.</span></span>

## <span data-ttu-id="03129-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="03129-119">PARAMETERS</span></span>

### <span data-ttu-id="03129-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03129-120">-DefaultProfile</span></span>
<span data-ttu-id="03129-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="03129-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="03129-122">-InputFile</span><span class="sxs-lookup"><span data-stu-id="03129-122">-InputFile</span></span>
<span data-ttu-id="03129-123">Azt a bemeneti fájlt adja meg, amely a visszaállítandó titok biztonsági másolatát tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="03129-123">Specifies the input file that contains the backup of the secret to restore.</span></span>

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

### <span data-ttu-id="03129-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="03129-124">-InputObject</span></span>
<span data-ttu-id="03129-125">A boltozat objektum</span><span class="sxs-lookup"><span data-stu-id="03129-125">KeyVault object</span></span>

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

### <span data-ttu-id="03129-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="03129-126">-ResourceId</span></span>
<span data-ttu-id="03129-127">A főkészlet erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="03129-127">KeyVault Resource Id</span></span>

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

### <span data-ttu-id="03129-128">-VaultName</span><span class="sxs-lookup"><span data-stu-id="03129-128">-VaultName</span></span>
<span data-ttu-id="03129-129">Annak a kulcsnak a nevét adja meg, amelybe vissza szeretné állítani a titkot.</span><span class="sxs-lookup"><span data-stu-id="03129-129">Specifies the name of the key vault into which to restore the secret.</span></span>

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

### <span data-ttu-id="03129-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="03129-130">-Confirm</span></span>
<span data-ttu-id="03129-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="03129-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03129-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03129-132">-WhatIf</span></span>
<span data-ttu-id="03129-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="03129-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03129-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="03129-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03129-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03129-135">CommonParameters</span></span>
<span data-ttu-id="03129-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="03129-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03129-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03129-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03129-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="03129-138">INPUTS</span></span>

### <span data-ttu-id="03129-139">Microsoft. Azure. Command. PSKeyVault. models.</span><span class="sxs-lookup"><span data-stu-id="03129-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>
<span data-ttu-id="03129-140">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="03129-140">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="03129-141">System. String</span><span class="sxs-lookup"><span data-stu-id="03129-141">System.String</span></span>

## <span data-ttu-id="03129-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="03129-142">OUTPUTS</span></span>

### <span data-ttu-id="03129-143">Microsoft. Azure. Command. PSKeyVaultSecret. models.</span><span class="sxs-lookup"><span data-stu-id="03129-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

## <span data-ttu-id="03129-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="03129-144">NOTES</span></span>

## <span data-ttu-id="03129-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="03129-145">RELATED LINKS</span></span>

[<span data-ttu-id="03129-146">Set-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="03129-146">Set-AzureKeyVaultSecret</span></span>](./Set-AzureKeyVaultSecret.md)

[<span data-ttu-id="03129-147">Backup-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="03129-147">Backup-AzureKeyVaultSecret</span></span>](./Backup-AzureKeyVaultSecret.md)

[<span data-ttu-id="03129-148">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="03129-148">Get-AzureKeyVaultSecret</span></span>](./Get-AzureKeyVaultSecret.md)

[<span data-ttu-id="03129-149">Remove-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="03129-149">Remove-AzureKeyVaultSecret</span></span>](./Remove-AzureKeyVaultSecret.md)

