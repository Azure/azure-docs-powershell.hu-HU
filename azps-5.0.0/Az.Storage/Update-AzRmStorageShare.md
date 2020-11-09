---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzRmStorageShare.md
ms.openlocfilehash: 0f2d86fca85364fa71d50c05d83f278bd997252e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301730"
---
# <span data-ttu-id="ad10e-101">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="ad10e-101">Update-AzRmStorageShare</span></span>

## <span data-ttu-id="ad10e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ad10e-102">SYNOPSIS</span></span>
<span data-ttu-id="ad10e-103">A tárterület-fájlmegosztás módosítása.</span><span class="sxs-lookup"><span data-stu-id="ad10e-103">Modifies a Storage file share.</span></span>

## <span data-ttu-id="ad10e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ad10e-104">SYNTAX</span></span>

### <span data-ttu-id="ad10e-105">AccountName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ad10e-105">AccountName (Default)</span></span>
```
Update-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-QuotaGiB <Int32>] [-Metadata <Hashtable>] [-AccessTier <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad10e-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="ad10e-106">AccountObject</span></span>
```
Update-AzRmStorageShare -Name <String> -StorageAccount <PSStorageAccount> [-QuotaGiB <Int32>]
 [-Metadata <Hashtable>] [-AccessTier <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ad10e-107">ShareResourceId</span><span class="sxs-lookup"><span data-stu-id="ad10e-107">ShareResourceId</span></span>
```
Update-AzRmStorageShare [-ResourceId] <String> [-QuotaGiB <Int32>] [-Metadata <Hashtable>]
 [-AccessTier <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad10e-108">ShareObject</span><span class="sxs-lookup"><span data-stu-id="ad10e-108">ShareObject</span></span>
```
Update-AzRmStorageShare -InputObject <PSShare> [-QuotaGiB <Int32>] [-Metadata <Hashtable>]
 [-AccessTier <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad10e-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="ad10e-109">DESCRIPTION</span></span>
<span data-ttu-id="ad10e-110">A **New-AzRmStorageShare** parancsmag módosította a tárterület-megosztást.</span><span class="sxs-lookup"><span data-stu-id="ad10e-110">The **New-AzRmStorageShare** cmdlet modifies a Storage file share.</span></span>

## <span data-ttu-id="ad10e-111">Példák</span><span class="sxs-lookup"><span data-stu-id="ad10e-111">EXAMPLES</span></span>

### <span data-ttu-id="ad10e-112">Példa 1: a tárterület-fájlmegosztás metaadatait módosítja, és megoszthatja a kvótát a tárolási fiók nevével és a megosztási névvel</span><span class="sxs-lookup"><span data-stu-id="ad10e-112">Example 1: Modifies a Storage file share's metadata and share quota with Storage account name and share name</span></span>
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

<span data-ttu-id="ad10e-113">Ez a parancs módosítja a tárterület-megosztás metaadatait, és megosztja a kvótát a tárolási fiók nevével és a megosztási névvel, valamint megjeleníti a módosítás eredményét a visszaadott fájlmegosztás objektummal.</span><span class="sxs-lookup"><span data-stu-id="ad10e-113">This command modifies a Storage file share's metadata and share quota with Storage account name and share name, and show the modify result with the returned file share object.</span></span>

### <span data-ttu-id="ad10e-114">2. példa: egy tárterület-megosztásban tárolt metaadatok módosítása a Storage Account objektummal és a megosztási névvel</span><span class="sxs-lookup"><span data-stu-id="ad10e-114">Example 2: Modifies metadata on a Storage file share with Storage account object and share name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount"
PS C:\>$share = Update-AzRmStorageShare -StorageAccount $accountObject -Name "myshare" -Metadata @{tag0="value0";tag1="value1"}
```

<span data-ttu-id="ad10e-115">Ez a parancs a tárterület-megosztásban lévő metaadatokat módosította a tárterület-objektummal, és megoszthatja a nevet.</span><span class="sxs-lookup"><span data-stu-id="ad10e-115">This command modifies metadata on a Storage file share with Storage account object and share name.</span></span>

### <span data-ttu-id="ad10e-116">3. példa: módosítja a kvótát a tárterületet tároló tárterületet tartalmazó tárterületen lévő összes tárterület-megosztásban.</span><span class="sxs-lookup"><span data-stu-id="ad10e-116">Example 3: Modifies share quota for all Storage file shares in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" | Update-AzRmStorageShare -QuotaGiB 5000

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
share1   5000
share2   5000
```

<span data-ttu-id="ad10e-117">Ez a parancs módosítja a megosztási kvótát 5000-as GiB-fájlként az összes tárterület-megosztáshoz egy csővezetéket tartalmazó tárterület-fiókban.</span><span class="sxs-lookup"><span data-stu-id="ad10e-117">This command modifies share quota as 5000 GiB for all Storage file shares in a Storage account with pipeline.</span></span>

### <span data-ttu-id="ad10e-118">Példa 4: tárterület-megosztás módosítása a accesstier-ban hűvös módon</span><span class="sxs-lookup"><span data-stu-id="ad10e-118">Example 4: Modify a Storage file share with accesstier as Cool</span></span>
```
PS C:\>$share = Update-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -Name "myshare" -AccessTier Cool

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocols AccessTier Deleted Version ShareUsageBytes
----     -------- ---------------- ---------- ------- ------- ---------------
myshare                            Cool
```

<span data-ttu-id="ad10e-119">Ez a parancs a tárterület-megosztást a accesstier-ban, hűvös formátumban módosítja.</span><span class="sxs-lookup"><span data-stu-id="ad10e-119">This command modifies a Storage file share with accesstier as Cool.</span></span>

## <span data-ttu-id="ad10e-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ad10e-120">PARAMETERS</span></span>

### <span data-ttu-id="ad10e-121">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="ad10e-121">-AccessTier</span></span>
<span data-ttu-id="ad10e-122">Access-szint adott megosztáshoz.</span><span class="sxs-lookup"><span data-stu-id="ad10e-122">Access tier for specific share.</span></span> <span data-ttu-id="ad10e-123">Az StorageV2-fiók a TransactionOptimized (alapértelmezett), a meleg és a hűvös beállítás között választhatja ki.</span><span class="sxs-lookup"><span data-stu-id="ad10e-123">StorageV2 account can choose between TransactionOptimized (default), Hot, and Cool.</span></span> <span data-ttu-id="ad10e-124">Az FileStorage-fiók a prémium lehetőséget is választhatja.</span><span class="sxs-lookup"><span data-stu-id="ad10e-124">FileStorage account can choose Premium.</span></span>

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

### <span data-ttu-id="ad10e-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad10e-125">-DefaultProfile</span></span>
<span data-ttu-id="ad10e-126">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ad10e-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad10e-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ad10e-127">-InputObject</span></span>
<span data-ttu-id="ad10e-128">Tárterület-megosztás objektum</span><span class="sxs-lookup"><span data-stu-id="ad10e-128">Storage Share object</span></span>

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

### <span data-ttu-id="ad10e-129">-Metadata</span><span class="sxs-lookup"><span data-stu-id="ad10e-129">-Metadata</span></span>
<span data-ttu-id="ad10e-130">Metaadatok megosztása</span><span class="sxs-lookup"><span data-stu-id="ad10e-130">Share Metadata</span></span>

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

### <span data-ttu-id="ad10e-131">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ad10e-131">-Name</span></span>
<span data-ttu-id="ad10e-132">Megosztás neve</span><span class="sxs-lookup"><span data-stu-id="ad10e-132">Share Name</span></span>

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

### <span data-ttu-id="ad10e-133">-QuotaGiB</span><span class="sxs-lookup"><span data-stu-id="ad10e-133">-QuotaGiB</span></span>
<span data-ttu-id="ad10e-134">Kvóta megosztása az Gibibyte-on.</span><span class="sxs-lookup"><span data-stu-id="ad10e-134">Share Quota in Gibibyte.</span></span>

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

### <span data-ttu-id="ad10e-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad10e-135">-ResourceGroupName</span></span>
<span data-ttu-id="ad10e-136">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="ad10e-136">Resource Group Name.</span></span>

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

### <span data-ttu-id="ad10e-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ad10e-137">-ResourceId</span></span>
<span data-ttu-id="ad10e-138">Adjon meg egy fájlmegosztási erőforrás-azonosítót.</span><span class="sxs-lookup"><span data-stu-id="ad10e-138">Input a File Share Resource Id.</span></span>

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

### <span data-ttu-id="ad10e-139">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="ad10e-139">-StorageAccount</span></span>
<span data-ttu-id="ad10e-140">Storage Account objektum</span><span class="sxs-lookup"><span data-stu-id="ad10e-140">Storage account object</span></span>

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

### <span data-ttu-id="ad10e-141">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="ad10e-141">-StorageAccountName</span></span>
<span data-ttu-id="ad10e-142">Tárolási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="ad10e-142">Storage Account Name.</span></span>

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

### <span data-ttu-id="ad10e-143">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ad10e-143">-Confirm</span></span>
<span data-ttu-id="ad10e-144">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ad10e-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad10e-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad10e-145">-WhatIf</span></span>
<span data-ttu-id="ad10e-146">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ad10e-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad10e-147">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ad10e-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad10e-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad10e-148">CommonParameters</span></span>
<span data-ttu-id="ad10e-149">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ad10e-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad10e-150">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad10e-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad10e-151">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ad10e-151">INPUTS</span></span>

### <span data-ttu-id="ad10e-152">System. String</span><span class="sxs-lookup"><span data-stu-id="ad10e-152">System.String</span></span>

### <span data-ttu-id="ad10e-153">Microsoft. Azure. Command. Management. Storage. models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ad10e-153">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="ad10e-154">Microsoft. Azure. Command. Management. Storage. models. PSShare</span><span class="sxs-lookup"><span data-stu-id="ad10e-154">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="ad10e-155">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ad10e-155">OUTPUTS</span></span>

### <span data-ttu-id="ad10e-156">Microsoft. Azure. Command. Management. Storage. models. PSShare</span><span class="sxs-lookup"><span data-stu-id="ad10e-156">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="ad10e-157">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ad10e-157">NOTES</span></span>

## <span data-ttu-id="ad10e-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ad10e-158">RELATED LINKS</span></span>
