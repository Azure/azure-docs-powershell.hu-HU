---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 6e7cbaf9ed6e9f0d9751e8e16004891a7fcbb056
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94010689"
---
# <span data-ttu-id="65ba7-101">Get-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="65ba7-101">Get-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="65ba7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="65ba7-102">SYNOPSIS</span></span>
<span data-ttu-id="65ba7-103">Felügyeli az Azure-tárterületet az Azure Storage-fiókokban.</span><span class="sxs-lookup"><span data-stu-id="65ba7-103">Gets Key Vault managed Azure Storage Accounts.</span></span>

## <span data-ttu-id="65ba7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="65ba7-104">SYNTAX</span></span>

### <span data-ttu-id="65ba7-105">ByAccountName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="65ba7-105">ByAccountName (Default)</span></span>
```
Get-AzKeyVaultManagedStorageAccount [-VaultName] <String> [[-AccountName] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="65ba7-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="65ba7-106">ByInputObject</span></span>
```
Get-AzKeyVaultManagedStorageAccount [-InputObject] <PSKeyVault> [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="65ba7-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="65ba7-107">ByResourceId</span></span>
```
Get-AzKeyVaultManagedStorageAccount [-ResourceId] <String> [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="65ba7-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="65ba7-108">DESCRIPTION</span></span>
<span data-ttu-id="65ba7-109">Ha a fiók neve meg van adva, és a fiók kulcsait a megadott pince kezeli, akkor a rendszer egy fontos Vault-felügyelt Azure-tároló fiókot kap.</span><span class="sxs-lookup"><span data-stu-id="65ba7-109">Gets a Key Vault managed Azure Storage Account if the name of the account is specified and the account keys are managed by the specified vault.</span></span> <span data-ttu-id="65ba7-110">Ha a fióknév nincs megadva, akkor az összes olyan fiók szerepel a listában, amelynek kulcsait a megadott boltozat kezeli.</span><span class="sxs-lookup"><span data-stu-id="65ba7-110">If the account name is not specified, then all the accounts whose keys are managed by specified vault are listed.</span></span>

## <span data-ttu-id="65ba7-111">Példák</span><span class="sxs-lookup"><span data-stu-id="65ba7-111">EXAMPLES</span></span>

### <span data-ttu-id="65ba7-112">1. példa: az összes fontos boltíves kezelt tárolási fiók listázása</span><span class="sxs-lookup"><span data-stu-id="65ba7-112">Example 1: List all Key Vault managed Storage Accounts</span></span>
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

<span data-ttu-id="65ba7-113">Felsorolja azokat a fiókokat, amelyek kulcsait a Vault ' myvault ' kezeli.</span><span class="sxs-lookup"><span data-stu-id="65ba7-113">Lists all the accounts whose keys are managed by vault 'myvault'</span></span>

### <span data-ttu-id="65ba7-114">2. példa: fontos boltozatos tárterület-fiók beszerzése</span><span class="sxs-lookup"><span data-stu-id="65ba7-114">Example 2: Get a Key Vault managed Storage Account</span></span>
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

<span data-ttu-id="65ba7-115">A "mystorageaccount" kulcs boltozatos tárterület-fiókjának részleteit kapja meg, ha a kulcsokat az "myvault" kezeli.</span><span class="sxs-lookup"><span data-stu-id="65ba7-115">Gets the details of Key Vault managed Storage Account of 'mystorageaccount' if its keys are managed by vault 'myvault'</span></span>

### <span data-ttu-id="65ba7-116">3. példa: az összes fontos boltíves kezelt tárolási fiók listázása szűréssel</span><span class="sxs-lookup"><span data-stu-id="65ba7-116">Example 3: List all Key Vault managed Storage Accounts using filtering</span></span>
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

<span data-ttu-id="65ba7-117">Felsorolja azokat a fiókokat, amelyek kulcsait az "myvault" és a "teszt" kezdetű Vault kezeli.</span><span class="sxs-lookup"><span data-stu-id="65ba7-117">Lists all the accounts whose keys are managed by vault 'myvault' that start with "test"</span></span>

## <span data-ttu-id="65ba7-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="65ba7-118">PARAMETERS</span></span>

### <span data-ttu-id="65ba7-119">-AccountName</span><span class="sxs-lookup"><span data-stu-id="65ba7-119">-AccountName</span></span>
<span data-ttu-id="65ba7-120">Fontos: a boltozattal felügyelt tárolási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="65ba7-120">Key Vault managed storage account name.</span></span> <span data-ttu-id="65ba7-121">Parancsmag: a felügyelt tárterület-fióknév teljes tartománynevét építi a Vault neve, a jelenleg kijelölt környezet és a Mangal-tároló fiók nevéből.</span><span class="sxs-lookup"><span data-stu-id="65ba7-121">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAccountName
Aliases: StorageAccountName, Name

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65ba7-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65ba7-122">-DefaultProfile</span></span>
<span data-ttu-id="65ba7-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="65ba7-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="65ba7-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="65ba7-124">-InputObject</span></span>
<span data-ttu-id="65ba7-125">Boltozat objektum.</span><span class="sxs-lookup"><span data-stu-id="65ba7-125">Vault object.</span></span>

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

### <span data-ttu-id="65ba7-126">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="65ba7-126">-InRemovedState</span></span>
<span data-ttu-id="65ba7-127">Azt adja meg, hogy megjelenjen-e a korábban törölt tárolási fiókok a kimenetben.</span><span class="sxs-lookup"><span data-stu-id="65ba7-127">Specifies whether to show the previously deleted storage accounts in the output.</span></span>

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

### <span data-ttu-id="65ba7-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="65ba7-128">-ResourceId</span></span>
<span data-ttu-id="65ba7-129">Vault-erőforrás azonosítója</span><span class="sxs-lookup"><span data-stu-id="65ba7-129">Vault resource id.</span></span>

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

### <span data-ttu-id="65ba7-130">-VaultName</span><span class="sxs-lookup"><span data-stu-id="65ba7-130">-VaultName</span></span>
<span data-ttu-id="65ba7-131">Boltozat neve.</span><span class="sxs-lookup"><span data-stu-id="65ba7-131">Vault name.</span></span>
<span data-ttu-id="65ba7-132">A parancsmag a pince teljes tartománynevét a név és a jelenleg kijelölt környezet alapján építi fel.</span><span class="sxs-lookup"><span data-stu-id="65ba7-132">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="65ba7-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65ba7-133">CommonParameters</span></span>
<span data-ttu-id="65ba7-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="65ba7-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65ba7-135">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="65ba7-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65ba7-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="65ba7-136">INPUTS</span></span>

### <span data-ttu-id="65ba7-137">Microsoft. Azure. Command. PSKeyVault. models.</span><span class="sxs-lookup"><span data-stu-id="65ba7-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="65ba7-138">System. String</span><span class="sxs-lookup"><span data-stu-id="65ba7-138">System.String</span></span>

## <span data-ttu-id="65ba7-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="65ba7-139">OUTPUTS</span></span>

### <span data-ttu-id="65ba7-140">Microsoft. Azure. Command. PSKeyVaultManagedStorageAccountIdentityItem. models.</span><span class="sxs-lookup"><span data-stu-id="65ba7-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

### <span data-ttu-id="65ba7-141">Microsoft. Azure. Command. PSKeyVaultManagedStorageAccount. models.</span><span class="sxs-lookup"><span data-stu-id="65ba7-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

### <span data-ttu-id="65ba7-142">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="65ba7-142">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccountIdentityItem</span></span>

### <span data-ttu-id="65ba7-143">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="65ba7-143">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="65ba7-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="65ba7-144">NOTES</span></span>

## <span data-ttu-id="65ba7-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="65ba7-145">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

