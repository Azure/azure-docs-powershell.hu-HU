---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 89452f2a00aea9d3ab42300c2f28bde67fec0905
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98323941"
---
# <span data-ttu-id="15f8a-101">Get-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="15f8a-101">Get-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="15f8a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="15f8a-102">SYNOPSIS</span></span>
<span data-ttu-id="15f8a-103">Lekérte a kulcstár által kezelt Azure Storage-fiókokat.</span><span class="sxs-lookup"><span data-stu-id="15f8a-103">Gets Key Vault managed Azure Storage Accounts.</span></span>

## <span data-ttu-id="15f8a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="15f8a-104">SYNTAX</span></span>

### <span data-ttu-id="15f8a-105">ByAccountName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="15f8a-105">ByAccountName (Default)</span></span>
```
Get-AzKeyVaultManagedStorageAccount [-VaultName] <String> [[-AccountName] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="15f8a-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="15f8a-106">ByInputObject</span></span>
```
Get-AzKeyVaultManagedStorageAccount [-InputObject] <PSKeyVault> [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="15f8a-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="15f8a-107">ByResourceId</span></span>
```
Get-AzKeyVaultManagedStorageAccount [-ResourceId] <String> [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="15f8a-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="15f8a-108">DESCRIPTION</span></span>
<span data-ttu-id="15f8a-109">Egy kulcstár által kezelt Azure Storage-fiókot kap, ha a fiók neve meg van adva, és a fiókkulcsokat a megadott tároló kezeli.</span><span class="sxs-lookup"><span data-stu-id="15f8a-109">Gets a Key Vault managed Azure Storage Account if the name of the account is specified and the account keys are managed by the specified vault.</span></span> <span data-ttu-id="15f8a-110">Ha a fióknév nincs megadva, akkor az összes olyan fiók megjelenik a listában, amelynek a kulcsait a megadott tároló kezeli.</span><span class="sxs-lookup"><span data-stu-id="15f8a-110">If the account name is not specified, then all the accounts whose keys are managed by specified vault are listed.</span></span>

## <span data-ttu-id="15f8a-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="15f8a-111">EXAMPLES</span></span>

### <span data-ttu-id="15f8a-112">1. példa: Az összes felügyelt tárfiók felsorolása a kulcstárban</span><span class="sxs-lookup"><span data-stu-id="15f8a-112">Example 1: List all Key Vault managed Storage Accounts</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedStorageAccount -VaultName 'myvault'

Id                  : https://myvault.vault.azure.net:443/storage/mystorageaccount
Vault Name          : myvault
AccountName         : mystorageaccount
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.St
                      orage/storageAccounts/mystorageaccount
Enabled             : True
Created             : 4/25/2018 1:50:32 AM
Updated             : 4/25/2018 1:50:32 AM
Tags                :
```

<span data-ttu-id="15f8a-113">Azokat a fiókokat sorolja fel, amelyek kulcsait a myvault tároló kezeli</span><span class="sxs-lookup"><span data-stu-id="15f8a-113">Lists all the accounts whose keys are managed by vault 'myvault'</span></span>

### <span data-ttu-id="15f8a-114">2. példa: A kulcstár felügyelt tárfiókja</span><span class="sxs-lookup"><span data-stu-id="15f8a-114">Example 2: Get a Key Vault managed Storage Account</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -Name 'mystorageaccount'

Id                  : https://myvault.vault.azure.net:443/storage/mystorageaccount
Vault Name          : myvault
AccountName         : mystorageaccount
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/maddie1/providers/Microsoft.St
                      orage/storageAccounts/mystorageaccount
Active Key Name     : key2
Auto Regenerate Key : False
Regeneration Period : 90.00:00:00
Enabled             : True
Created             : 4/25/2018 1:50:32 AM
Updated             : 4/25/2018 1:50:32 AM
Tags                :
```

<span data-ttu-id="15f8a-115">A kulcstár által felügyelt tárfiók adatait (mystorageaccount) kapja meg, ha a kulcsait a "myvault" tároló kezeli</span><span class="sxs-lookup"><span data-stu-id="15f8a-115">Gets the details of Key Vault managed Storage Account of 'mystorageaccount' if its keys are managed by vault 'myvault'</span></span>

### <span data-ttu-id="15f8a-116">3. példa: Az összes kulcstár által felügyelt tárfiók felsorolása szűrés használatával</span><span class="sxs-lookup"><span data-stu-id="15f8a-116">Example 3: List all Key Vault managed Storage Accounts using filtering</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -Name "test*"

Id                  : https://myvault.vault.azure.net:443/storage/test1
Vault Name          : myvault
AccountName         : test1
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.St
                      orage/storageAccounts/test1
Enabled             : True
Created             : 4/25/2018 1:50:32 AM
Updated             : 4/25/2018 1:50:32 AM
Tags                :

Id                  : https://myvault.vault.azure.net:443/storage/test2
Vault Name          : myvault
AccountName         : test2
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.St
                      orage/storageAccounts/test2
Enabled             : True
Created             : 4/25/2018 1:50:32 AM
Updated             : 4/25/2018 1:50:32 AM
Tags                :
```

<span data-ttu-id="15f8a-117">Azokat a fiókokat sorolja fel, amelyeknek a kulcsait a "myvault" tároló kezeli, és a "teszt" kezdetű</span><span class="sxs-lookup"><span data-stu-id="15f8a-117">Lists all the accounts whose keys are managed by vault 'myvault' that start with "test"</span></span>

## <span data-ttu-id="15f8a-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="15f8a-118">PARAMETERS</span></span>

### <span data-ttu-id="15f8a-119">-AccountName</span><span class="sxs-lookup"><span data-stu-id="15f8a-119">-AccountName</span></span>
<span data-ttu-id="15f8a-120">Key Vault managed storage account name.</span><span class="sxs-lookup"><span data-stu-id="15f8a-120">Key Vault managed storage account name.</span></span> <span data-ttu-id="15f8a-121">A parancsmag egy felügyelt tárfiók nevének FQDN-ét építi fel a tárolónévből, az aktuálisan kijelölt környezetből és a felügyelt tárfiók nevéből.</span><span class="sxs-lookup"><span data-stu-id="15f8a-121">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAccountName
Aliases: StorageAccountName, Name

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="15f8a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15f8a-122">-DefaultProfile</span></span>
<span data-ttu-id="15f8a-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="15f8a-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="15f8a-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="15f8a-124">-InputObject</span></span>
<span data-ttu-id="15f8a-125">Tárolóobjektum.</span><span class="sxs-lookup"><span data-stu-id="15f8a-125">Vault object.</span></span>

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

### <span data-ttu-id="15f8a-126">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="15f8a-126">-InRemovedState</span></span>
<span data-ttu-id="15f8a-127">Azt adja meg, hogy a korábban törölt tárfiókokat a kimenetben is meg kell-e mutatni.</span><span class="sxs-lookup"><span data-stu-id="15f8a-127">Specifies whether to show the previously deleted storage accounts in the output.</span></span>

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

### <span data-ttu-id="15f8a-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="15f8a-128">-ResourceId</span></span>
<span data-ttu-id="15f8a-129">Tároló erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="15f8a-129">Vault resource id.</span></span>

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

### <span data-ttu-id="15f8a-130">-VaultName</span><span class="sxs-lookup"><span data-stu-id="15f8a-130">-VaultName</span></span>
<span data-ttu-id="15f8a-131">Tároló neve.</span><span class="sxs-lookup"><span data-stu-id="15f8a-131">Vault name.</span></span>
<span data-ttu-id="15f8a-132">A parancsmag a név és a jelenleg kijelölt környezet alapján építi fel egy tároló teljes tartománynevét.</span><span class="sxs-lookup"><span data-stu-id="15f8a-132">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15f8a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15f8a-133">CommonParameters</span></span>
<span data-ttu-id="15f8a-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15f8a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15f8a-135">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="15f8a-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15f8a-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="15f8a-136">INPUTS</span></span>

### <span data-ttu-id="15f8a-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="15f8a-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="15f8a-138">System.String</span><span class="sxs-lookup"><span data-stu-id="15f8a-138">System.String</span></span>

## <span data-ttu-id="15f8a-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="15f8a-139">OUTPUTS</span></span>

### <span data-ttu-id="15f8a-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="15f8a-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

### <span data-ttu-id="15f8a-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="15f8a-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

### <span data-ttu-id="15f8a-142">Microsoft.Azure.Commands.KeyVault.Models.PSDKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="15f8a-142">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccountIdentityItem</span></span>

### <span data-ttu-id="15f8a-143">Microsoft.Azure.Commands.KeyVault.Models.PSDKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="15f8a-143">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="15f8a-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="15f8a-144">NOTES</span></span>

## <span data-ttu-id="15f8a-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="15f8a-145">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

