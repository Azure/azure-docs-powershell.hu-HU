---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/restore-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 4750561aed6643c17fed6e42d13551be76635d72
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100152762"
---
# <span data-ttu-id="4f174-101">Restore-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4f174-101">Restore-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="4f174-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4f174-102">SYNOPSIS</span></span>
<span data-ttu-id="4f174-103">Visszaállít egy felügyelt tárfiókot egy kulcstárolóban egy biztonsági másolatból.</span><span class="sxs-lookup"><span data-stu-id="4f174-103">Restores a managed storage account in a key vault from a backup file.</span></span>

## <span data-ttu-id="4f174-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="4f174-104">SYNTAX</span></span>

### <span data-ttu-id="4f174-105">ByVaultName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4f174-105">ByVaultName (Default)</span></span>
```
Restore-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f174-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="4f174-106">ByInputObject</span></span>
```
Restore-AzKeyVaultManagedStorageAccount [-InputObject] <PSKeyVault> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f174-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="4f174-107">ByResourceId</span></span>
```
Restore-AzKeyVaultManagedStorageAccount [-ResourceId] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4f174-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="4f174-108">DESCRIPTION</span></span>
<span data-ttu-id="4f174-109">A **Restore-AzKeyVaultManagedStorageAccount** parancsmag egy biztonsági másolatból létrehoz egy felügyelt tárfiókot a megadott kulcstárolóban.</span><span class="sxs-lookup"><span data-stu-id="4f174-109">The **Restore-AzKeyVaultManagedStorageAccount** cmdlet creates a managed storage account in the specified key vault from a backup file.</span></span>
<span data-ttu-id="4f174-110">Ez a felügyelt tárfiók a bemeneti fájlban található biztonsági másolat másolata, és a neve megegyezik az eredetivel.</span><span class="sxs-lookup"><span data-stu-id="4f174-110">This managed storage account is a replica of the backed-up managed storage account in the input file and has the same name as the original.</span></span>
<span data-ttu-id="4f174-111">Ha a kulcstároló már tartalmaz azonos nevű felügyelt tárfiókot, ez a parancsmag nem tudja felülírni az eredetit.</span><span class="sxs-lookup"><span data-stu-id="4f174-111">If the key vault already contains a managed storage account by the same name, this cmdlet fails instead of overwriting the original.</span></span>
<span data-ttu-id="4f174-112">Az a kulcstároló, amelybe visszaállítja a felügyelt tárfiókot, eltérhet attól a kulcstártól, amelyről a felügyelt tárfiókról biztonsági mentést tárolt.</span><span class="sxs-lookup"><span data-stu-id="4f174-112">The key vault that you restore the managed storage account into can be different from the key vault that you backed up the managed storage account from.</span></span>
<span data-ttu-id="4f174-113">A kulcstárnak azonban ugyanazt az előfizetést kell használnia, és ugyanabban a földrajzi régióban (például Észak-Amerikában) kell lennie egy Azure-régióban.</span><span class="sxs-lookup"><span data-stu-id="4f174-113">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="4f174-114">Az Azure-régiók földrajzokkal való megfeleltetését a Microsoft Azure Trust Center https://azure.microsoft.com/support/trust-center/) webhelyén tudja meg.</span><span class="sxs-lookup"><span data-stu-id="4f174-114">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="4f174-115">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="4f174-115">EXAMPLES</span></span>

### <span data-ttu-id="4f174-116">1. példa: Biztonsági másolatból törölt felügyelt tárfiók visszaállítása</span><span class="sxs-lookup"><span data-stu-id="4f174-116">Example 1: Restore a backed-up managed storage account</span></span>
```powershell
PS C:\> Restore-AzKeyVaultManagedStorageAccount -VaultName 'MyKeyVault' -InputFile "C:\Backup.blob"

Id                  : https://mykeyvault.vault.azure.net:443/storage/mystorageaccount
Vault Name          : MyKeyVault
AccountName         : mystorageaccount
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.St
                      orage/storageAccounts/mystorageaccount
Active Key Name     : key1
Auto Regenerate Key : True
Regeneration Period : 90.00:00:00
Enabled             : True
Created             : 5/21/2018 11:55:58 PM
Updated             : 5/21/2018 11:55:58 PM
Tags                :
```

<span data-ttu-id="4f174-117">Ez a parancs visszaállít egy felügyelt tárfiókot az összes verziójával együtt a Backup.blob nevű biztonságimásolat-fájlból a MyKeyVault nevű kulcstárba.</span><span class="sxs-lookup"><span data-stu-id="4f174-117">This command restores a managed storage account, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="4f174-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4f174-118">PARAMETERS</span></span>

### <span data-ttu-id="4f174-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f174-119">-DefaultProfile</span></span>
<span data-ttu-id="4f174-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4f174-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4f174-121">-InputFile</span><span class="sxs-lookup"><span data-stu-id="4f174-121">-InputFile</span></span>
<span data-ttu-id="4f174-122">Bemeneti fájl.</span><span class="sxs-lookup"><span data-stu-id="4f174-122">Input file.</span></span>
<span data-ttu-id="4f174-123">A háttérként tárolt blobot tartalmazó bemeneti fájl</span><span class="sxs-lookup"><span data-stu-id="4f174-123">The input file containing the backed-up blob</span></span>

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

### <span data-ttu-id="4f174-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4f174-124">-InputObject</span></span>
<span data-ttu-id="4f174-125">KeyVault objektum</span><span class="sxs-lookup"><span data-stu-id="4f174-125">KeyVault object</span></span>

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

### <span data-ttu-id="4f174-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4f174-126">-ResourceId</span></span>
<span data-ttu-id="4f174-127">KeyVault Resource Id</span><span class="sxs-lookup"><span data-stu-id="4f174-127">KeyVault Resource Id</span></span>

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

### <span data-ttu-id="4f174-128">-VaultName</span><span class="sxs-lookup"><span data-stu-id="4f174-128">-VaultName</span></span>
<span data-ttu-id="4f174-129">Tároló neve.</span><span class="sxs-lookup"><span data-stu-id="4f174-129">Vault name.</span></span>
<span data-ttu-id="4f174-130">A parancsmag a név és a jelenleg kijelölt környezet alapján építi fel egy tároló teljes tartománynevét.</span><span class="sxs-lookup"><span data-stu-id="4f174-130">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="4f174-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4f174-131">-Confirm</span></span>
<span data-ttu-id="4f174-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="4f174-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f174-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f174-133">-WhatIf</span></span>
<span data-ttu-id="4f174-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="4f174-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4f174-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4f174-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f174-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f174-136">CommonParameters</span></span>
<span data-ttu-id="4f174-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f174-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f174-138">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4f174-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f174-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4f174-139">INPUTS</span></span>

### <span data-ttu-id="4f174-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="4f174-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="4f174-141">System.String</span><span class="sxs-lookup"><span data-stu-id="4f174-141">System.String</span></span>

## <span data-ttu-id="4f174-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4f174-142">OUTPUTS</span></span>

### <span data-ttu-id="4f174-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4f174-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="4f174-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="4f174-144">NOTES</span></span>

## <span data-ttu-id="4f174-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4f174-145">RELATED LINKS</span></span>
