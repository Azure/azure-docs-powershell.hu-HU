---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageShare.md
ms.openlocfilehash: 90edd254eb77b03f4f4d26761020d71025960426
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024316"
---
# <span data-ttu-id="93409-101">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="93409-101">Get-AzRmStorageShare</span></span>

## <span data-ttu-id="93409-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="93409-102">SYNOPSIS</span></span>
<span data-ttu-id="93409-103">Tárterület-megosztást kap vagy listáz.</span><span class="sxs-lookup"><span data-stu-id="93409-103">Gets or lists Storage file shares.</span></span>

## <span data-ttu-id="93409-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="93409-104">SYNTAX</span></span>

### <span data-ttu-id="93409-105">AccountNameSingle (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="93409-105">AccountNameSingle (Default)</span></span>
```
Get-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> [-Name <String>]
 [-GetShareUsage] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="93409-106">AccountName</span><span class="sxs-lookup"><span data-stu-id="93409-106">AccountName</span></span>
```
Get-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> [-IncludeDeleted]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="93409-107">AccountObjectSingle</span><span class="sxs-lookup"><span data-stu-id="93409-107">AccountObjectSingle</span></span>
```
Get-AzRmStorageShare -StorageAccount <PSStorageAccount> -Name <String> [-GetShareUsage]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="93409-108">AccountObject</span><span class="sxs-lookup"><span data-stu-id="93409-108">AccountObject</span></span>
```
Get-AzRmStorageShare -StorageAccount <PSStorageAccount> [-IncludeDeleted]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="93409-109">ShareResourceId</span><span class="sxs-lookup"><span data-stu-id="93409-109">ShareResourceId</span></span>
```
Get-AzRmStorageShare [-ResourceId] <String> [-Name <String>] [-GetShareUsage]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="93409-110">Leírás</span><span class="sxs-lookup"><span data-stu-id="93409-110">DESCRIPTION</span></span>
<span data-ttu-id="93409-111">A **Get-AzRmStorageShare** parancsmag a tárterület-megosztásokat kapja vagy sorolja fel.</span><span class="sxs-lookup"><span data-stu-id="93409-111">The **Get-AzRmStorageShare** cmdlet gets or lists Storage file shares.</span></span>

## <span data-ttu-id="93409-112">Példák</span><span class="sxs-lookup"><span data-stu-id="93409-112">EXAMPLES</span></span>

### <span data-ttu-id="93409-113">Példa 1: tárterület-megosztás beszerzése tárolási fiók nevével és megosztási névvel</span><span class="sxs-lookup"><span data-stu-id="93409-113">Example 1: Get a Storage file share with Storage account name and share name</span></span>
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -Name "myshare"

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
myshare  5120
```

<span data-ttu-id="93409-114">Ez a parancs tárterület-megosztást kap a tárolási fióknév és a megosztási fiók nevével.</span><span class="sxs-lookup"><span data-stu-id="93409-114">This command gets a Storage file share with Storage account name and share name.</span></span>

### <span data-ttu-id="93409-115">2. példa: tárterület-fiók tárterület-megosztásának listázása</span><span class="sxs-lookup"><span data-stu-id="93409-115">Example 2: List all Storage file shares of a Storage account</span></span>
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount"

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier           Deleted Version ShareUsageBytes
----     -------- --------------- ----------           ------- ------- ---------------
share1   5120                     TransactionOptimized
share2   5120                     TransactionOptimized
```

<span data-ttu-id="93409-116">Ebben a parancsban a tárolási fiók nevében tárolt tárterület-megosztások minden tárterülete látható.</span><span class="sxs-lookup"><span data-stu-id="93409-116">This command lists all Storage file shares of a Storage account with Storage account name.</span></span>

### <span data-ttu-id="93409-117">3. példa: adattároló blob-tároló beszerzése tárolási fiók objektummal és tároló nevével</span><span class="sxs-lookup"><span data-stu-id="93409-117">Example 3: Get a Storage blob container with Storage account object and container name.</span></span>
```
Get-AzStorageAccount -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" | Get-AzRmStorageShare -Name "myshare"

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
myshare  5120
```

<span data-ttu-id="93409-118">Ez a parancs egy tároló BLOB-tárolót kap a Storage Account objektummal és a tároló nevével.</span><span class="sxs-lookup"><span data-stu-id="93409-118">This command gets a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="93409-119">Példa 4: tárterület-megosztás beszerzése a megosztás kihasználtsága bájtban</span><span class="sxs-lookup"><span data-stu-id="93409-119">Example 4: Get a Storage file share with the share usage in bytes</span></span>
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -Name "myshare" -GetShareUsage

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
myshare  5120                                                2097152
```

<span data-ttu-id="93409-120">Ez a parancs egy tárterület-megosztást kap a tárolási fiók nevével és a megosztási névvel, és belefoglalja a megosztási kihasználtságot bájtban.</span><span class="sxs-lookup"><span data-stu-id="93409-120">This command gets a Storage file share with Storage account name and share name, and include the share usage in bytes.</span></span>

### <span data-ttu-id="93409-121">5. példa: a tárolási fiók tárterület-megosztásának listázása, a törölt megosztások felvétele</span><span class="sxs-lookup"><span data-stu-id="93409-121">Example 5: List all Storage file shares of a Storage account, include the deleted shares</span></span>
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -IncludeDeleted 

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier           Deleted Version          ShareUsageBytes
----     -------- --------------- ----------           ------- -------          ---------------
test     100                      TransactionOptimized                                         
share1   100                      TransactionOptimized True    01D61FD1FC5498B6
```

<span data-ttu-id="93409-122">Ez a parancs felsorolja az összes tárterület-megosztást, mely tartalmazza a tárolási fiók nevét tartalmazó tárterület-fiók törölt részvényeit.</span><span class="sxs-lookup"><span data-stu-id="93409-122">This command lists all Storage file shares include the deleted shares of a Storage account with Storage account name.</span></span>

## <span data-ttu-id="93409-123">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="93409-123">PARAMETERS</span></span>

### <span data-ttu-id="93409-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93409-124">-DefaultProfile</span></span>
<span data-ttu-id="93409-125">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="93409-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="93409-126">-GetShareUsage</span><span class="sxs-lookup"><span data-stu-id="93409-126">-GetShareUsage</span></span>
<span data-ttu-id="93409-127">Adja meg ezt a paramétert a megosztás bájtban való használatáról.</span><span class="sxs-lookup"><span data-stu-id="93409-127">Specify this parameter to get the Share Usage in Bytes.</span></span>

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

### <span data-ttu-id="93409-128">-IncludeDeleted</span><span class="sxs-lookup"><span data-stu-id="93409-128">-IncludeDeleted</span></span>
<span data-ttu-id="93409-129">A törölt megosztások közé tartozik alapértelmezés szerint a lista megosztása nem fogja tartalmazni a törölt megosztásokat</span><span class="sxs-lookup"><span data-stu-id="93409-129">Include deleted shares, by default list shares won't include deleted shares</span></span>

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

### <span data-ttu-id="93409-130">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="93409-130">-Name</span></span>
<span data-ttu-id="93409-131">Megosztás neve</span><span class="sxs-lookup"><span data-stu-id="93409-131">Share Name</span></span>

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

### <span data-ttu-id="93409-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93409-132">-ResourceGroupName</span></span>
<span data-ttu-id="93409-133">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="93409-133">Resource Group Name.</span></span>

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

### <span data-ttu-id="93409-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="93409-134">-ResourceId</span></span>
<span data-ttu-id="93409-135">Adjon meg egy fájlmegosztási erőforrás-azonosítót.</span><span class="sxs-lookup"><span data-stu-id="93409-135">Input a File Share Resource Id.</span></span>

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

### <span data-ttu-id="93409-136">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="93409-136">-StorageAccount</span></span>
<span data-ttu-id="93409-137">Storage Account objektum</span><span class="sxs-lookup"><span data-stu-id="93409-137">Storage account object</span></span>

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

### <span data-ttu-id="93409-138">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="93409-138">-StorageAccountName</span></span>
<span data-ttu-id="93409-139">Tárolási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="93409-139">Storage Account Name.</span></span>

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

### <span data-ttu-id="93409-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93409-140">CommonParameters</span></span>
<span data-ttu-id="93409-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="93409-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93409-142">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93409-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93409-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="93409-143">INPUTS</span></span>

### <span data-ttu-id="93409-144">System. String</span><span class="sxs-lookup"><span data-stu-id="93409-144">System.String</span></span>

### <span data-ttu-id="93409-145">Microsoft. Azure. Command. Management. Storage. models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="93409-145">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="93409-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="93409-146">OUTPUTS</span></span>

### <span data-ttu-id="93409-147">Microsoft. Azure. Command. Management. Storage. models. PSShare</span><span class="sxs-lookup"><span data-stu-id="93409-147">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="93409-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="93409-148">NOTES</span></span>

## <span data-ttu-id="93409-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="93409-149">RELATED LINKS</span></span>
