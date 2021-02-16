---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzRmStorageShare.md
ms.openlocfilehash: 0f2d86fca85364fa71d50c05d83f278bd997252e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209086"
---
# <span data-ttu-id="5202b-101">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="5202b-101">Update-AzRmStorageShare</span></span>

## <span data-ttu-id="5202b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5202b-102">SYNOPSIS</span></span>
<span data-ttu-id="5202b-103">Tárterületfájl-megosztást módosít.</span><span class="sxs-lookup"><span data-stu-id="5202b-103">Modifies a Storage file share.</span></span>

## <span data-ttu-id="5202b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5202b-104">SYNTAX</span></span>

### <span data-ttu-id="5202b-105">AccountName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5202b-105">AccountName (Default)</span></span>
```
Update-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-QuotaGiB <Int32>] [-Metadata <Hashtable>] [-AccessTier <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5202b-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="5202b-106">AccountObject</span></span>
```
Update-AzRmStorageShare -Name <String> -StorageAccount <PSStorageAccount> [-QuotaGiB <Int32>]
 [-Metadata <Hashtable>] [-AccessTier <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5202b-107">ShareResourceId</span><span class="sxs-lookup"><span data-stu-id="5202b-107">ShareResourceId</span></span>
```
Update-AzRmStorageShare [-ResourceId] <String> [-QuotaGiB <Int32>] [-Metadata <Hashtable>]
 [-AccessTier <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5202b-108">ShareObject</span><span class="sxs-lookup"><span data-stu-id="5202b-108">ShareObject</span></span>
```
Update-AzRmStorageShare -InputObject <PSShare> [-QuotaGiB <Int32>] [-Metadata <Hashtable>]
 [-AccessTier <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5202b-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5202b-109">DESCRIPTION</span></span>
<span data-ttu-id="5202b-110">A **New-AzRmStorageShare** parancsmag módosítja a tárfájl megosztását.</span><span class="sxs-lookup"><span data-stu-id="5202b-110">The **New-AzRmStorageShare** cmdlet modifies a Storage file share.</span></span>

## <span data-ttu-id="5202b-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5202b-111">EXAMPLES</span></span>

### <span data-ttu-id="5202b-112">1. példa: A tárfájl-megosztás metaadatainak és megosztási kvótájának módosítja a tárfiók nevét és a megosztás nevét</span><span class="sxs-lookup"><span data-stu-id="5202b-112">Example 1: Modifies a Storage file share's metadata and share quota with Storage account name and share name</span></span>
```
PS C:\>$share = Update-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -Name "myshare" -QuotaGiB 200 -Metadata @{tag0="value0";tag1="value1"}

PS C:\>$share

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
myshare  200

PS C:\>$share.Metadata

Key  Value  
---  ----- 
tag0 value0
tag1 value1
```

<span data-ttu-id="5202b-113">Ez a parancs módosítja a tárfájl-megosztás metaadatait és a megosztási kvótát a Tárfiók nevével és a megosztás nevével, valamint a módosítás eredményét a visszaadott fájlmegosztási objektummal együtt.</span><span class="sxs-lookup"><span data-stu-id="5202b-113">This command modifies a Storage file share's metadata and share quota with Storage account name and share name, and show the modify result with the returned file share object.</span></span>

### <span data-ttu-id="5202b-114">2. példa: A Tárfiók objektummal és a megosztás nevével módosítja a tárfájl-megosztás metaadatait</span><span class="sxs-lookup"><span data-stu-id="5202b-114">Example 2: Modifies metadata on a Storage file share with Storage account object and share name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount"
PS C:\>$share = Update-AzRmStorageShare -StorageAccount $accountObject -Name "myshare" -Metadata @{tag0="value0";tag1="value1"}
```

<span data-ttu-id="5202b-115">Ez a parancs módosítja a tárfiók-megosztás metaadatait a Tárfiók objektummal és a megosztás nevével.</span><span class="sxs-lookup"><span data-stu-id="5202b-115">This command modifies metadata on a Storage file share with Storage account object and share name.</span></span>

### <span data-ttu-id="5202b-116">3. példa: Egy tárfiók tárfájl-megosztási kvótáját módosítja folyamaton keresztül</span><span class="sxs-lookup"><span data-stu-id="5202b-116">Example 3: Modifies share quota for all Storage file shares in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" | Update-AzRmStorageShare -QuotaGiB 5000

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
share1   5000
share2   5000
```

<span data-ttu-id="5202b-117">Ez a parancs 5000 GiB-ként módosítja a tárfiók tárterületfájl-megosztási kvótáját.</span><span class="sxs-lookup"><span data-stu-id="5202b-117">This command modifies share quota as 5000 GiB for all Storage file shares in a Storage account with pipeline.</span></span>

### <span data-ttu-id="5202b-118">4. példa: Tárterületfájl megosztásának módosítása a hozzáértővel Cool formátumban</span><span class="sxs-lookup"><span data-stu-id="5202b-118">Example 4: Modify a Storage file share with accesstier as Cool</span></span>
```
PS C:\>$share = Update-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -Name "myshare" -AccessTier Cool

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocols AccessTier Deleted Version ShareUsageBytes
----     -------- ---------------- ---------- ------- ------- ---------------
myshare                            Cool
```

<span data-ttu-id="5202b-119">Ez a parancs a Tárterületfájl megosztását a hozzáértővel Cool formátumban módosítja.</span><span class="sxs-lookup"><span data-stu-id="5202b-119">This command modifies a Storage file share with accesstier as Cool.</span></span>

## <span data-ttu-id="5202b-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5202b-120">PARAMETERS</span></span>

### <span data-ttu-id="5202b-121">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="5202b-121">-AccessTier</span></span>
<span data-ttu-id="5202b-122">Adott megosztás hozzáférési rétege.</span><span class="sxs-lookup"><span data-stu-id="5202b-122">Access tier for specific share.</span></span> <span data-ttu-id="5202b-123">A StorageV2-fiók választhat a TransactionOptimized (alapértelmezett), a Gyors és a Gyors beállítás közül.</span><span class="sxs-lookup"><span data-stu-id="5202b-123">StorageV2 account can choose between TransactionOptimized (default), Hot, and Cool.</span></span> <span data-ttu-id="5202b-124">A FileStorage-fiók választhatja a Prémium kategóriát.</span><span class="sxs-lookup"><span data-stu-id="5202b-124">FileStorage account can choose Premium.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: TransactionOptimized, Premium, Hot, Cool

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5202b-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5202b-125">-DefaultProfile</span></span>
<span data-ttu-id="5202b-126">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5202b-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5202b-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5202b-127">-InputObject</span></span>
<span data-ttu-id="5202b-128">Tárterület megosztása objektum</span><span class="sxs-lookup"><span data-stu-id="5202b-128">Storage Share object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSShare
Parameter Sets: ShareObject
Aliases: Share

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5202b-129">-Metadata</span><span class="sxs-lookup"><span data-stu-id="5202b-129">-Metadata</span></span>
<span data-ttu-id="5202b-130">Metaadatok megosztása</span><span class="sxs-lookup"><span data-stu-id="5202b-130">Share Metadata</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5202b-131">-Name</span><span class="sxs-lookup"><span data-stu-id="5202b-131">-Name</span></span>
<span data-ttu-id="5202b-132">Név megosztása</span><span class="sxs-lookup"><span data-stu-id="5202b-132">Share Name</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases: N, ShareName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5202b-133">-QuotaGiB</span><span class="sxs-lookup"><span data-stu-id="5202b-133">-QuotaGiB</span></span>
<span data-ttu-id="5202b-134">Share Quota in Gibibyte.</span><span class="sxs-lookup"><span data-stu-id="5202b-134">Share Quota in Gibibyte.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: Quota

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5202b-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5202b-135">-ResourceGroupName</span></span>
<span data-ttu-id="5202b-136">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="5202b-136">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5202b-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5202b-137">-ResourceId</span></span>
<span data-ttu-id="5202b-138">Fájlmegosztási erőforrás-azonosító bevitele</span><span class="sxs-lookup"><span data-stu-id="5202b-138">Input a File Share Resource Id.</span></span>

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

### <span data-ttu-id="5202b-139">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="5202b-139">-StorageAccount</span></span>
<span data-ttu-id="5202b-140">Tárfiók objektum</span><span class="sxs-lookup"><span data-stu-id="5202b-140">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5202b-141">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="5202b-141">-StorageAccountName</span></span>
<span data-ttu-id="5202b-142">Tárfiók neve.</span><span class="sxs-lookup"><span data-stu-id="5202b-142">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5202b-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5202b-143">-Confirm</span></span>
<span data-ttu-id="5202b-144">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="5202b-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5202b-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5202b-145">-WhatIf</span></span>
<span data-ttu-id="5202b-146">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="5202b-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5202b-147">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5202b-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5202b-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5202b-148">CommonParameters</span></span>
<span data-ttu-id="5202b-149">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5202b-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5202b-150">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5202b-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5202b-151">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5202b-151">INPUTS</span></span>

### <span data-ttu-id="5202b-152">System.String</span><span class="sxs-lookup"><span data-stu-id="5202b-152">System.String</span></span>

### <span data-ttu-id="5202b-153">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5202b-153">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="5202b-154">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span><span class="sxs-lookup"><span data-stu-id="5202b-154">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="5202b-155">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5202b-155">OUTPUTS</span></span>

### <span data-ttu-id="5202b-156">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span><span class="sxs-lookup"><span data-stu-id="5202b-156">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="5202b-157">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5202b-157">NOTES</span></span>

## <span data-ttu-id="5202b-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5202b-158">RELATED LINKS</span></span>
