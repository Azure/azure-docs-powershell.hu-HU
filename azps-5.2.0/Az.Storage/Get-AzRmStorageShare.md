---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageShare.md
ms.openlocfilehash: 90edd254eb77b03f4f4d26761020d71025960426
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98325090"
---
# <span data-ttu-id="55aec-101">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="55aec-101">Get-AzRmStorageShare</span></span>

## <span data-ttu-id="55aec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="55aec-102">SYNOPSIS</span></span>
<span data-ttu-id="55aec-103">Tárterületfájl-megosztásokat kap vagy sorol fel.</span><span class="sxs-lookup"><span data-stu-id="55aec-103">Gets or lists Storage file shares.</span></span>

## <span data-ttu-id="55aec-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="55aec-104">SYNTAX</span></span>

### <span data-ttu-id="55aec-105">AccountNameSingle (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="55aec-105">AccountNameSingle (Default)</span></span>
```
Get-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> [-Name <String>]
 [-GetShareUsage] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="55aec-106">AccountName</span><span class="sxs-lookup"><span data-stu-id="55aec-106">AccountName</span></span>
```
Get-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> [-IncludeDeleted]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="55aec-107">AccountObjectSingle</span><span class="sxs-lookup"><span data-stu-id="55aec-107">AccountObjectSingle</span></span>
```
Get-AzRmStorageShare -StorageAccount <PSStorageAccount> -Name <String> [-GetShareUsage]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="55aec-108">AccountObject</span><span class="sxs-lookup"><span data-stu-id="55aec-108">AccountObject</span></span>
```
Get-AzRmStorageShare -StorageAccount <PSStorageAccount> [-IncludeDeleted]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="55aec-109">ShareResourceId</span><span class="sxs-lookup"><span data-stu-id="55aec-109">ShareResourceId</span></span>
```
Get-AzRmStorageShare [-ResourceId] <String> [-Name <String>] [-GetShareUsage]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="55aec-110">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="55aec-110">DESCRIPTION</span></span>
<span data-ttu-id="55aec-111">A **Get-AzRmStorageShare** parancsmag tárhelyfájl-megosztásokat kap vagy sorol fel.</span><span class="sxs-lookup"><span data-stu-id="55aec-111">The **Get-AzRmStorageShare** cmdlet gets or lists Storage file shares.</span></span>

## <span data-ttu-id="55aec-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="55aec-112">EXAMPLES</span></span>

### <span data-ttu-id="55aec-113">1. példa: Tárterületfájl-megosztás a Tárfiók nevével és a megosztás nevével</span><span class="sxs-lookup"><span data-stu-id="55aec-113">Example 1: Get a Storage file share with Storage account name and share name</span></span>
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -Name "myshare"

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
myshare  5120
```

<span data-ttu-id="55aec-114">Ez a parancs egy Tárterületfájl-megosztást kap a Tárfiók nevével és a megosztás nevével.</span><span class="sxs-lookup"><span data-stu-id="55aec-114">This command gets a Storage file share with Storage account name and share name.</span></span>

### <span data-ttu-id="55aec-115">2. példa: Tárfiók összes tárterületfájl-megosztásának felsorolása</span><span class="sxs-lookup"><span data-stu-id="55aec-115">Example 2: List all Storage file shares of a Storage account</span></span>
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount"

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier           Deleted Version ShareUsageBytes
----     -------- --------------- ----------           ------- ------- ---------------
share1   5120                     TransactionOptimized
share2   5120                     TransactionOptimized
```

<span data-ttu-id="55aec-116">Ez a parancs felsorolja a Tárfiók tárfiók összes tárfájl-megosztását a Tárfiók nevével.</span><span class="sxs-lookup"><span data-stu-id="55aec-116">This command lists all Storage file shares of a Storage account with Storage account name.</span></span>

### <span data-ttu-id="55aec-117">3. példa: Tárterület blobtárolója tárfiók-objektummal és tárolónévvel.</span><span class="sxs-lookup"><span data-stu-id="55aec-117">Example 3: Get a Storage blob container with Storage account object and container name.</span></span>
```
Get-AzStorageAccount -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" | Get-AzRmStorageShare -Name "myshare"

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
myshare  5120
```

<span data-ttu-id="55aec-118">Ez a parancs egy Tároló blobtárolót kap a Tárfiók objektummal és a tároló nevével.</span><span class="sxs-lookup"><span data-stu-id="55aec-118">This command gets a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="55aec-119">4. példa: Tárterületfájl-megosztás bájtban</span><span class="sxs-lookup"><span data-stu-id="55aec-119">Example 4: Get a Storage file share with the share usage in bytes</span></span>
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -Name "myshare" -GetShareUsage

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
myshare  5120                                                2097152
```

<span data-ttu-id="55aec-120">Ez a parancs egy Tárterületfájl-megosztást kap a Tárfiók nevével és a megosztás nevével, valamint a megosztási használatot bájtban.</span><span class="sxs-lookup"><span data-stu-id="55aec-120">This command gets a Storage file share with Storage account name and share name, and include the share usage in bytes.</span></span>

### <span data-ttu-id="55aec-121">5. példa: Tárfiók összes tárterületfájl-megosztásának felsorolása, a törölt megosztások felsorolása</span><span class="sxs-lookup"><span data-stu-id="55aec-121">Example 5: List all Storage file shares of a Storage account, include the deleted shares</span></span>
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -IncludeDeleted 

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier           Deleted Version          ShareUsageBytes
----     -------- --------------- ----------           ------- -------          ---------------
test     100                      TransactionOptimized                                         
share1   100                      TransactionOptimized True    01D61FD1FC5498B6
```

<span data-ttu-id="55aec-122">Ez a parancs felsorolja a tárterületfájl-megosztásokat, például a Tárfiók nevével törölt megosztásokat.</span><span class="sxs-lookup"><span data-stu-id="55aec-122">This command lists all Storage file shares include the deleted shares of a Storage account with Storage account name.</span></span>

## <span data-ttu-id="55aec-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="55aec-123">PARAMETERS</span></span>

### <span data-ttu-id="55aec-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55aec-124">-DefaultProfile</span></span>
<span data-ttu-id="55aec-125">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="55aec-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="55aec-126">-GetShareUsage</span><span class="sxs-lookup"><span data-stu-id="55aec-126">-GetShareUsage</span></span>
<span data-ttu-id="55aec-127">Ezt a paramétert megadva bájtban adhatja meg a megosztási használatot.</span><span class="sxs-lookup"><span data-stu-id="55aec-127">Specify this parameter to get the Share Usage in Bytes.</span></span>

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

### <span data-ttu-id="55aec-128">-IncludeDeleted</span><span class="sxs-lookup"><span data-stu-id="55aec-128">-IncludeDeleted</span></span>
<span data-ttu-id="55aec-129">Törölt megosztások is, alapértelmezés szerint a listamegosztások nem fogják tartalmazni a törölt megosztásokat</span><span class="sxs-lookup"><span data-stu-id="55aec-129">Include deleted shares, by default list shares won't include deleted shares</span></span>

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

### <span data-ttu-id="55aec-130">-Name</span><span class="sxs-lookup"><span data-stu-id="55aec-130">-Name</span></span>
<span data-ttu-id="55aec-131">Név megosztása</span><span class="sxs-lookup"><span data-stu-id="55aec-131">Share Name</span></span>

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

### <span data-ttu-id="55aec-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55aec-132">-ResourceGroupName</span></span>
<span data-ttu-id="55aec-133">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="55aec-133">Resource Group Name.</span></span>

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

### <span data-ttu-id="55aec-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="55aec-134">-ResourceId</span></span>
<span data-ttu-id="55aec-135">Fájlmegosztási erőforrás-azonosító bevitele</span><span class="sxs-lookup"><span data-stu-id="55aec-135">Input a File Share Resource Id.</span></span>

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

### <span data-ttu-id="55aec-136">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="55aec-136">-StorageAccount</span></span>
<span data-ttu-id="55aec-137">Tárfiók objektum</span><span class="sxs-lookup"><span data-stu-id="55aec-137">Storage account object</span></span>

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

### <span data-ttu-id="55aec-138">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="55aec-138">-StorageAccountName</span></span>
<span data-ttu-id="55aec-139">Tárfiók neve.</span><span class="sxs-lookup"><span data-stu-id="55aec-139">Storage Account Name.</span></span>

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

### <span data-ttu-id="55aec-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55aec-140">CommonParameters</span></span>
<span data-ttu-id="55aec-141">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55aec-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55aec-142">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55aec-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55aec-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="55aec-143">INPUTS</span></span>

### <span data-ttu-id="55aec-144">System.String</span><span class="sxs-lookup"><span data-stu-id="55aec-144">System.String</span></span>

### <span data-ttu-id="55aec-145">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="55aec-145">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="55aec-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="55aec-146">OUTPUTS</span></span>

### <span data-ttu-id="55aec-147">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span><span class="sxs-lookup"><span data-stu-id="55aec-147">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="55aec-148">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="55aec-148">NOTES</span></span>

## <span data-ttu-id="55aec-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="55aec-149">RELATED LINKS</span></span>
