---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/restore-azurekeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Restore-AzureKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Restore-AzureKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 12e1844be497baa24a3b9b4aa9c4e5690564f4ca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493681"
---
# <span data-ttu-id="76567-101">Restore-AzureKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="76567-101">Restore-AzureKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="76567-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="76567-102">SYNOPSIS</span></span>
<span data-ttu-id="76567-103">Egy biztonsági másolatból visszaállítja a felügyelt tárterület-fiókot egy kulcsfájl segítségével.</span><span class="sxs-lookup"><span data-stu-id="76567-103">Restores a managed storage account in a key vault from a backup file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="76567-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="76567-104">SYNTAX</span></span>

### <span data-ttu-id="76567-105">ByVaultName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="76567-105">ByVaultName (Default)</span></span>
```
Restore-AzureKeyVaultManagedStorageAccount [-VaultName] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76567-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="76567-106">ByInputObject</span></span>
```
Restore-AzureKeyVaultManagedStorageAccount [-InputObject] <PSKeyVault> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76567-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="76567-107">ByResourceId</span></span>
```
Restore-AzureKeyVaultManagedStorageAccount [-ResourceId] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76567-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="76567-108">DESCRIPTION</span></span>
<span data-ttu-id="76567-109">A **Restore-AzureKeyVaultManagedStorageAccount** parancsmag egy biztonságimásolat-fájlból hoz létre felügyelt tárolási fiókot a megadott kulcsfájl alapján.</span><span class="sxs-lookup"><span data-stu-id="76567-109">The **Restore-AzureKeyVaultManagedStorageAccount** cmdlet creates a managed storage account in the specified key vault from a backup file.</span></span>
<span data-ttu-id="76567-110">Ez a felügyelt tárterület a tárolt felügyelt tárterület-fiók másolata a bemeneti fájlban, és az eredeti nevével megegyező.</span><span class="sxs-lookup"><span data-stu-id="76567-110">This managed storage account is a replica of the backed-up managed storage account in the input file and has the same name as the original.</span></span>
<span data-ttu-id="76567-111">Ha a kulcsfájl már tartalmaz egy felügyelt tárolási fiókot ugyanazzal a névvel, akkor ez a parancsmag nem felülírja az eredetit.</span><span class="sxs-lookup"><span data-stu-id="76567-111">If the key vault already contains a managed storage account by the same name, this cmdlet fails instead of overwriting the original.</span></span>
<span data-ttu-id="76567-112">A felügyelt tárterületet tároló kulcs boltozata eltérő lehet azzal a kulccsal, amelyről biztonsági másolatot készített a felügyelt tárterület-fiókról.</span><span class="sxs-lookup"><span data-stu-id="76567-112">The key vault that you restore the managed storage account into can be different from the key vault that you backed up the managed storage account from.</span></span>
<span data-ttu-id="76567-113">A kulcs boltozatának azonban ugyanazt az előfizetést kell használnia, és egy Azure-régióban kell lennie ugyanazon a földrajzon (például Észak-Amerikában).</span><span class="sxs-lookup"><span data-stu-id="76567-113">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="76567-114">Lásd: a Microsoft Azure Trust Center ( https://azure.microsoft.com/support/trust-center/) Az Azure-régiók földrajzi megfeleltetéséhez.</span><span class="sxs-lookup"><span data-stu-id="76567-114">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="76567-115">Példák</span><span class="sxs-lookup"><span data-stu-id="76567-115">EXAMPLES</span></span>

### <span data-ttu-id="76567-116">Példa 1: a felügyelt tárterület biztonsági mentése fiók visszaállítása</span><span class="sxs-lookup"><span data-stu-id="76567-116">Example 1: Restore a backed-up managed storage account</span></span>
```powershell
PS C:\> Restore-AzureKeyVaultManagedStorageAccount -VaultName 'MyKeyVault' -InputFile "C:\Backup.blob"

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

<span data-ttu-id="76567-117">Ez a parancs visszaállítja a felügyelt tárterület-fiókot (az összes verziót is) a Backup. blob nevű biztonsági másolatból a MyKeyVault nevű kulcs boltozatba.</span><span class="sxs-lookup"><span data-stu-id="76567-117">This command restores a managed storage account, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="76567-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="76567-118">PARAMETERS</span></span>

### <span data-ttu-id="76567-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76567-119">-DefaultProfile</span></span>
<span data-ttu-id="76567-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="76567-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76567-121">-InputFile</span><span class="sxs-lookup"><span data-stu-id="76567-121">-InputFile</span></span>
<span data-ttu-id="76567-122">Bemeneti fájl</span><span class="sxs-lookup"><span data-stu-id="76567-122">Input file.</span></span>
<span data-ttu-id="76567-123">A mentett blobot tartalmazó bemeneti fájl</span><span class="sxs-lookup"><span data-stu-id="76567-123">The input file containing the backed-up blob</span></span>

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

### <span data-ttu-id="76567-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="76567-124">-InputObject</span></span>
<span data-ttu-id="76567-125">A boltozat objektum</span><span class="sxs-lookup"><span data-stu-id="76567-125">KeyVault object</span></span>

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

### <span data-ttu-id="76567-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="76567-126">-ResourceId</span></span>
<span data-ttu-id="76567-127">A főkészlet erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="76567-127">KeyVault Resource Id</span></span>

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

### <span data-ttu-id="76567-128">-VaultName</span><span class="sxs-lookup"><span data-stu-id="76567-128">-VaultName</span></span>
<span data-ttu-id="76567-129">Boltozat neve.</span><span class="sxs-lookup"><span data-stu-id="76567-129">Vault name.</span></span>
<span data-ttu-id="76567-130">A parancsmag a pince teljes tartománynevét a név és a jelenleg kijelölt környezet alapján építi fel.</span><span class="sxs-lookup"><span data-stu-id="76567-130">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="76567-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="76567-131">-Confirm</span></span>
<span data-ttu-id="76567-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="76567-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76567-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76567-133">-WhatIf</span></span>
<span data-ttu-id="76567-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="76567-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76567-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="76567-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76567-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76567-136">CommonParameters</span></span>
<span data-ttu-id="76567-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="76567-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76567-138">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76567-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76567-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="76567-139">INPUTS</span></span>

### <span data-ttu-id="76567-140">Microsoft. Azure. Command. PSKeyVault. models.</span><span class="sxs-lookup"><span data-stu-id="76567-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>
<span data-ttu-id="76567-141">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="76567-141">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="76567-142">System. String</span><span class="sxs-lookup"><span data-stu-id="76567-142">System.String</span></span>

## <span data-ttu-id="76567-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="76567-143">OUTPUTS</span></span>

### <span data-ttu-id="76567-144">Microsoft. Azure. Command. PSKeyVaultManagedStorageAccount. models.</span><span class="sxs-lookup"><span data-stu-id="76567-144">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="76567-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="76567-145">NOTES</span></span>

## <span data-ttu-id="76567-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="76567-146">RELATED LINKS</span></span>
