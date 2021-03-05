---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageShare.md
ms.openlocfilehash: 44ad4fadb86b84b5eacb82a15bf92b7b1d831b70
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002822"
---
# <span data-ttu-id="69bfa-101">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="69bfa-101">Get-AzRmStorageShare</span></span>

## <span data-ttu-id="69bfa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69bfa-102">SYNOPSIS</span></span>
<span data-ttu-id="69bfa-103">Tárterületfájlmegosztások lekérte vagy listázza azokat.</span><span class="sxs-lookup"><span data-stu-id="69bfa-103">Gets or lists Storage file shares.</span></span>

## <span data-ttu-id="69bfa-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="69bfa-104">SYNTAX</span></span>

### <span data-ttu-id="69bfa-105">AccountNameSingle (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="69bfa-105">AccountNameSingle (Default)</span></span>
```
Get-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> [-Name <String>]
 [-GetShareUsage] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="69bfa-106">AccountName</span><span class="sxs-lookup"><span data-stu-id="69bfa-106">AccountName</span></span>
```
Get-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> [-IncludeDeleted]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="69bfa-107">AccountObjectSingle</span><span class="sxs-lookup"><span data-stu-id="69bfa-107">AccountObjectSingle</span></span>
```
Get-AzRmStorageShare -StorageAccount <PSStorageAccount> -Name <String> [-GetShareUsage]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="69bfa-108">AccountObject</span><span class="sxs-lookup"><span data-stu-id="69bfa-108">AccountObject</span></span>
```
Get-AzRmStorageShare -StorageAccount <PSStorageAccount> [-IncludeDeleted]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="69bfa-109">ShareResourceId</span><span class="sxs-lookup"><span data-stu-id="69bfa-109">ShareResourceId</span></span>
```
Get-AzRmStorageShare [-ResourceId] <String> [-Name <String>] [-GetShareUsage]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="69bfa-110">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="69bfa-110">DESCRIPTION</span></span>
<span data-ttu-id="69bfa-111">A **Get-AzRmStorageShare** parancsmag tárhelyfájl-megosztásokat kap vagy sorol fel.</span><span class="sxs-lookup"><span data-stu-id="69bfa-111">The **Get-AzRmStorageShare** cmdlet gets or lists Storage file shares.</span></span>

## <span data-ttu-id="69bfa-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="69bfa-112">EXAMPLES</span></span>

### <span data-ttu-id="69bfa-113">1. példa: Tárterületfájl-megosztás a Tárfiók nevével és a megosztás nevével</span><span class="sxs-lookup"><span data-stu-id="69bfa-113">Example 1: Get a Storage file share with Storage account name and share name</span></span>
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -Name "myshare"

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
myshare  5120
```

<span data-ttu-id="69bfa-114">Ez a parancs egy Tárterületfájl-megosztást kap a Tárfiók nevével és a megosztás nevével.</span><span class="sxs-lookup"><span data-stu-id="69bfa-114">This command gets a Storage file share with Storage account name and share name.</span></span>

### <span data-ttu-id="69bfa-115">2. példa: Tárfiók összes tárterületfájl-megosztásának felsorolása</span><span class="sxs-lookup"><span data-stu-id="69bfa-115">Example 2: List all Storage file shares of a Storage account</span></span>
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount"

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier           Deleted Version ShareUsageBytes
----     -------- --------------- ----------           ------- ------- ---------------
share1   5120                     TransactionOptimized
share2   5120                     TransactionOptimized
```

<span data-ttu-id="69bfa-116">Ez a parancs felsorolja a Tárfiók tárfiók összes tárfájl-megosztását a Tárfiók nevével.</span><span class="sxs-lookup"><span data-stu-id="69bfa-116">This command lists all Storage file shares of a Storage account with Storage account name.</span></span>

### <span data-ttu-id="69bfa-117">3. példa: Tárterület blobtárolója tárfiók-objektummal és tárolónévvel.</span><span class="sxs-lookup"><span data-stu-id="69bfa-117">Example 3: Get a Storage blob container with Storage account object and container name.</span></span>
```
Get-AzStorageAccount -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" | Get-AzRmStorageShare -Name "myshare"

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
myshare  5120
```

<span data-ttu-id="69bfa-118">Ez a parancs egy Tároló blobtárolót kap a Tárfiók-objektummal és a tároló nevével.</span><span class="sxs-lookup"><span data-stu-id="69bfa-118">This command gets a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="69bfa-119">4. példa: Tárterületfájl-megosztás bájtban</span><span class="sxs-lookup"><span data-stu-id="69bfa-119">Example 4: Get a Storage file share with the share usage in bytes</span></span>
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -Name "myshare" -GetShareUsage

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
myshare  5120                                                2097152
```

<span data-ttu-id="69bfa-120">Ez a parancs egy Tárterületfájl-megosztást kap a Tárfiók nevével és a megosztás nevével, valamint a megosztási használatot bájtban.</span><span class="sxs-lookup"><span data-stu-id="69bfa-120">This command gets a Storage file share with Storage account name and share name, and include the share usage in bytes.</span></span>

### <span data-ttu-id="69bfa-121">5. példa: Tárfiók összes tárterületfájl-megosztásának felsorolása, a törölt megosztások felsorolása</span><span class="sxs-lookup"><span data-stu-id="69bfa-121">Example 5: List all Storage file shares of a Storage account, include the deleted shares</span></span>
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -IncludeDeleted 

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier           Deleted Version          ShareUsageBytes
----     -------- --------------- ----------           ------- -------          ---------------
test     100                      TransactionOptimized                                         
share1   100                      TransactionOptimized True    01D61FD1FC5498B6
```

<span data-ttu-id="69bfa-122">Ez a parancs felsorolja az összes tárfájlmegosztást, például a Tárfiók nevével törölt megosztásokat.</span><span class="sxs-lookup"><span data-stu-id="69bfa-122">This command lists all Storage file shares include the deleted shares of a Storage account with Storage account name.</span></span>

## <span data-ttu-id="69bfa-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="69bfa-123">PARAMETERS</span></span>

### <span data-ttu-id="69bfa-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69bfa-124">-DefaultProfile</span></span>
<span data-ttu-id="69bfa-125">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="69bfa-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="69bfa-126">-GetShareUsage</span><span class="sxs-lookup"><span data-stu-id="69bfa-126">-GetShareUsage</span></span>
<span data-ttu-id="69bfa-127">Ezt a paramétert megadva bájtban is be lehet szerezni a Megosztás kihasználtság értékét.</span><span class="sxs-lookup"><span data-stu-id="69bfa-127">Specify this parameter to get the Share Usage in Bytes.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AccountNameSingle, AccountObjectSingle, ShareResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69bfa-128">-IncludeDeleted</span><span class="sxs-lookup"><span data-stu-id="69bfa-128">-IncludeDeleted</span></span>
<span data-ttu-id="69bfa-129">Törölt megosztások is, alapértelmezés szerint a listamegosztások nem fogják tartalmazni a törölt megosztásokat</span><span class="sxs-lookup"><span data-stu-id="69bfa-129">Include deleted shares, by default list shares won't include deleted shares</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AccountName, AccountObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69bfa-130">-Name</span><span class="sxs-lookup"><span data-stu-id="69bfa-130">-Name</span></span>
<span data-ttu-id="69bfa-131">Név megosztása</span><span class="sxs-lookup"><span data-stu-id="69bfa-131">Share Name</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameSingle, ShareResourceId
Aliases: N, ShareName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AccountObjectSingle
Aliases: N, ShareName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69bfa-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69bfa-132">-ResourceGroupName</span></span>
<span data-ttu-id="69bfa-133">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="69bfa-133">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameSingle, AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69bfa-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="69bfa-134">-ResourceId</span></span>
<span data-ttu-id="69bfa-135">Fájlmegosztási erőforrás-azonosító bevitele</span><span class="sxs-lookup"><span data-stu-id="69bfa-135">Input a File Share Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69bfa-136">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="69bfa-136">-StorageAccount</span></span>
<span data-ttu-id="69bfa-137">Tárfiók objektum</span><span class="sxs-lookup"><span data-stu-id="69bfa-137">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObjectSingle, AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="69bfa-138">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="69bfa-138">-StorageAccountName</span></span>
<span data-ttu-id="69bfa-139">Tárfiók neve.</span><span class="sxs-lookup"><span data-stu-id="69bfa-139">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameSingle, AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69bfa-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69bfa-140">CommonParameters</span></span>
<span data-ttu-id="69bfa-141">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69bfa-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69bfa-142">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69bfa-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69bfa-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="69bfa-143">INPUTS</span></span>

### <span data-ttu-id="69bfa-144">System.String</span><span class="sxs-lookup"><span data-stu-id="69bfa-144">System.String</span></span>

### <span data-ttu-id="69bfa-145">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="69bfa-145">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="69bfa-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="69bfa-146">OUTPUTS</span></span>

### <span data-ttu-id="69bfa-147">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span><span class="sxs-lookup"><span data-stu-id="69bfa-147">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="69bfa-148">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="69bfa-148">NOTES</span></span>

## <span data-ttu-id="69bfa-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="69bfa-149">RELATED LINKS</span></span>
