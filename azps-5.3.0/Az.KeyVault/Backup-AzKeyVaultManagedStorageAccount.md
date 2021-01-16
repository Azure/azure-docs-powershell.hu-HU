---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: c01d07f9408804b229921394c24e444b2a4deb8b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480113"
---
# <span data-ttu-id="8bc7a-101">Backup-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8bc7a-101">Backup-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="8bc7a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8bc7a-102">SYNOPSIS</span></span>
<span data-ttu-id="8bc7a-103">A KeyVault által felügyelt tárfiók biztonsági létrehozása.</span><span class="sxs-lookup"><span data-stu-id="8bc7a-103">Backs up a KeyVault-managed storage account.</span></span>

## <span data-ttu-id="8bc7a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8bc7a-104">SYNTAX</span></span>

### <span data-ttu-id="8bc7a-105">ByStorageAccountName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8bc7a-105">ByStorageAccountName (Default)</span></span>
```
Backup-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8bc7a-106">ByStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8bc7a-106">ByStorageAccount</span></span>
```
Backup-AzKeyVaultManagedStorageAccount [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [[-OutputFile] <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8bc7a-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8bc7a-107">DESCRIPTION</span></span>
<span data-ttu-id="8bc7a-108">A **Backup-AzKeyVaultManagedStorageAccount** parancsmag egy adott felügyelt tárfiókról biztonsági másolatot készít egy kulcstárolóban úgy, hogy letölti és egy fájlban tárolja azt.</span><span class="sxs-lookup"><span data-stu-id="8bc7a-108">The **Backup-AzKeyVaultManagedStorageAccount** cmdlet backs up a specified managed storage account in a key vault by downloading it and storing it in a file.</span></span>
<span data-ttu-id="8bc7a-109">Mivel a letöltött tartalom titkosítva van, nem használható az Azure-kulcstáron kívül.</span><span class="sxs-lookup"><span data-stu-id="8bc7a-109">Because the downloaded content is encrypted, it cannot be used outside of Azure Key Vault.</span></span>
<span data-ttu-id="8bc7a-110">Visszaállíthat egy biztonsági másolattal tárolt tárfiókot az előfizetés bármely kulcstárába, amelyről biztonsági másolat lett, ha a tároló ugyanabban az Azure geographyban van.</span><span class="sxs-lookup"><span data-stu-id="8bc7a-110">You can restore a backed-up storage account to any key vault in the subscription that it was backed up from, as long as the vault is in the same Azure geography.</span></span>
<span data-ttu-id="8bc7a-111">A parancsmag használatának tipikus okai:</span><span class="sxs-lookup"><span data-stu-id="8bc7a-111">Typical reasons to use this cmdlet are:</span></span> 
- <span data-ttu-id="8bc7a-112">Meg szeretné őrizni a tárfiók offline példányát arra az esetre, ha véletlenül törli az eredetit a tárolóból.</span><span class="sxs-lookup"><span data-stu-id="8bc7a-112">You want to retain an offline copy of the storage account in case you accidentally delete the original from the vault.</span></span>
 
- <span data-ttu-id="8bc7a-113">A kulcstár használatával létrehozott egy felügyelt tárfiókot, és most egy másik Azure-régióba szeretné klónozni az objektumot, hogy az elosztott alkalmazás összes példányából használva tudja használni.</span><span class="sxs-lookup"><span data-stu-id="8bc7a-113">You created a managed storage account using Key Vault and now want to clone the object into a different Azure region, so that you can use it from all instances of your distributed application.</span></span>
<span data-ttu-id="8bc7a-114">Az **AzKeyVaultManagedStorageAccount** parancsmaggal titkosított formátumban olvassa be a felügyelt tárfiókot, majd használja a **Restore-AzKeyVaultManagedStorageAccount** parancsmagot, és adjon meg egy kulcstárat a második régióban.</span><span class="sxs-lookup"><span data-stu-id="8bc7a-114">Use the **Backup-AzKeyVaultManagedStorageAccount** cmdlet to retrieve the managed storage account in encrypted format and then use the **Restore-AzKeyVaultManagedStorageAccount** cmdlet and specify a key vault in the second region.</span></span>

## <span data-ttu-id="8bc7a-115">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8bc7a-115">EXAMPLES</span></span>

### <span data-ttu-id="8bc7a-116">1. példa: Felügyelt tárfiók biztonsági mentése automatikusan létrehozott fájlnévvel</span><span class="sxs-lookup"><span data-stu-id="8bc7a-116">Example 1: Back up a managed storage account with an automatically generated file name</span></span>
```powershell
PS C:\Users\username\> Backup-AzKeyVaultManagedStorageAccount -VaultName 'MyKeyVault' -Name 'MyMSAK'

C:\Users\username\mykeyvault-mymsak-1527029447.01191
```

<span data-ttu-id="8bc7a-117">Ez a parancs beolvassa a MyMSAK nevű felügyelt tárfiókot a MyKeyVault nevű kulcstárból, és egy automatikusan elnevezett fájlba menti a felügyelt tárfiók biztonsági másolatát, és megjeleníti a fájl nevét.</span><span class="sxs-lookup"><span data-stu-id="8bc7a-117">This command retrieves the managed storage account named MyMSAK from the key vault named MyKeyVault and saves a backup of that managed storage account to a file that is automatically named for you, and displays the file name.</span></span>

### <span data-ttu-id="8bc7a-118">2. példa: Felügyelt tárfiók biztonsági mentése egy megadott fájlnévre</span><span class="sxs-lookup"><span data-stu-id="8bc7a-118">Example 2: Back up a managed storage account to a specified file name</span></span>
```powershell
PS C:\> Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyMSAK' -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

<span data-ttu-id="8bc7a-119">Ez a parancs beolvassa a MyMSAK nevű felügyelt tárfiókot a MyKeyVault nevű kulcstárból, és biztonsági másolatot készít a felügyelt tárfiókról egy Backup.blob nevű fájlba.</span><span class="sxs-lookup"><span data-stu-id="8bc7a-119">This command retrieves the managed storage account named MyMSAK from the key vault named MyKeyVault and saves a backup of that managed storage account to a file named Backup.blob.</span></span>

### <span data-ttu-id="8bc7a-120">3. példa: Korábban lekért felügyelt tárfiók biztonsági mentése egy megadott fájlnévre, a célfájl felülírása kérés nélkül.</span><span class="sxs-lookup"><span data-stu-id="8bc7a-120">Example 3: Back up a previously retrieved managed storage account to a specified file name, overwriting the destination file without prompting.</span></span>
```powershell
PS C:\> $msak = Get-AzKeyVaultManagedStorageAccount -VaultName 'MyKeyVault' -Name 'MyMSAK'
PS C:\> Backup-AzKeyVaultManagedStorageAccount -StorageAccount $msak -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

<span data-ttu-id="8bc7a-121">Ez a parancs biztonsági másolatot készít a $msak. Név a tárolóban $msak. A Backup.blob nevű fájl VaultName fájlja, amely csendesen felülírja a fájlt, ha már létezik.</span><span class="sxs-lookup"><span data-stu-id="8bc7a-121">This command creates a backup of the managed storage account named $msak.Name in the vault named $msak.VaultName to a file named Backup.blob, silently overwriting the file if it exists already.</span></span>

## <span data-ttu-id="8bc7a-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8bc7a-122">PARAMETERS</span></span>

### <span data-ttu-id="8bc7a-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8bc7a-123">-DefaultProfile</span></span>
<span data-ttu-id="8bc7a-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8bc7a-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8bc7a-125">-Force</span><span class="sxs-lookup"><span data-stu-id="8bc7a-125">-Force</span></span>
<span data-ttu-id="8bc7a-126">A megadott fájl felülírása( ha létezik)</span><span class="sxs-lookup"><span data-stu-id="8bc7a-126">Overwrite the given file if it exists</span></span>

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

### <span data-ttu-id="8bc7a-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8bc7a-127">-InputObject</span></span>
<span data-ttu-id="8bc7a-128">Tárfiók kötege biztonsági ként való biztonsági híváshoz, amely a beolvasási hívás kimeneteként lesz befutva.</span><span class="sxs-lookup"><span data-stu-id="8bc7a-128">Storage account bundle to be backed up, pipelined in from the output of a retrieval call.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem
Parameter Sets: ByStorageAccount
Aliases: StorageAccount

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8bc7a-129">-Name</span><span class="sxs-lookup"><span data-stu-id="8bc7a-129">-Name</span></span>
<span data-ttu-id="8bc7a-130">Titkos név.</span><span class="sxs-lookup"><span data-stu-id="8bc7a-130">Secret name.</span></span>
<span data-ttu-id="8bc7a-131">A parancsmag a tárolónévből ( jelenleg kijelölt környezetből és titkos névből ) egy titkos kulcs teljes tartománynevét építi fel.</span><span class="sxs-lookup"><span data-stu-id="8bc7a-131">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByStorageAccountName
Aliases: StorageAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bc7a-132">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="8bc7a-132">-OutputFile</span></span>
<span data-ttu-id="8bc7a-133">Kimeneti fájl.</span><span class="sxs-lookup"><span data-stu-id="8bc7a-133">Output file.</span></span>
<span data-ttu-id="8bc7a-134">A tárfiók biztonsági mentését tároló kimeneti fájl.</span><span class="sxs-lookup"><span data-stu-id="8bc7a-134">The output file to store the storage account backup.</span></span>
<span data-ttu-id="8bc7a-135">Ha nincs megadva, a rendszer létrehoz egy alapértelmezett fájlnevet.</span><span class="sxs-lookup"><span data-stu-id="8bc7a-135">If not specified, a default filename will be generated.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bc7a-136">-VaultName</span><span class="sxs-lookup"><span data-stu-id="8bc7a-136">-VaultName</span></span>
<span data-ttu-id="8bc7a-137">Tároló neve.</span><span class="sxs-lookup"><span data-stu-id="8bc7a-137">Vault name.</span></span>
<span data-ttu-id="8bc7a-138">A parancsmag a név és a jelenleg kijelölt környezet alapján építi fel egy tároló teljes tartománynevét.</span><span class="sxs-lookup"><span data-stu-id="8bc7a-138">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByStorageAccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bc7a-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8bc7a-139">-Confirm</span></span>
<span data-ttu-id="8bc7a-140">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="8bc7a-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8bc7a-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8bc7a-141">-WhatIf</span></span>
<span data-ttu-id="8bc7a-142">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="8bc7a-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8bc7a-143">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8bc7a-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8bc7a-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bc7a-144">CommonParameters</span></span>
<span data-ttu-id="8bc7a-145">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8bc7a-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bc7a-146">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8bc7a-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bc7a-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8bc7a-147">INPUTS</span></span>

### <span data-ttu-id="8bc7a-148">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="8bc7a-148">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

## <span data-ttu-id="8bc7a-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8bc7a-149">OUTPUTS</span></span>

### <span data-ttu-id="8bc7a-150">System.String</span><span class="sxs-lookup"><span data-stu-id="8bc7a-150">System.String</span></span>

## <span data-ttu-id="8bc7a-151">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8bc7a-151">NOTES</span></span>

## <span data-ttu-id="8bc7a-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8bc7a-152">RELATED LINKS</span></span>
