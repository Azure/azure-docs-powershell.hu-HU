---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzRmStorageShare.md
ms.openlocfilehash: 6e3c71900e5fe4a4ac8e4f092691dcde3e759c2f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011492"
---
# <span data-ttu-id="c344d-101">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="c344d-101">Update-AzRmStorageShare</span></span>

## <span data-ttu-id="c344d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c344d-102">SYNOPSIS</span></span>
<span data-ttu-id="c344d-103">A tárterület-fájlmegosztás módosítása.</span><span class="sxs-lookup"><span data-stu-id="c344d-103">Modifies a Storage file share.</span></span>

## <span data-ttu-id="c344d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c344d-104">SYNTAX</span></span>

### <span data-ttu-id="c344d-105">AccountName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c344d-105">AccountName (Default)</span></span>
```
Update-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-QuotaGiB <Int32>] [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c344d-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="c344d-106">AccountObject</span></span>
```
Update-AzRmStorageShare -Name <String> -StorageAccount <PSStorageAccount> [-QuotaGiB <Int32>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c344d-107">ShareResourceId</span><span class="sxs-lookup"><span data-stu-id="c344d-107">ShareResourceId</span></span>
```
Update-AzRmStorageShare [-ResourceId] <String> [-QuotaGiB <Int32>] [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c344d-108">ShareObject</span><span class="sxs-lookup"><span data-stu-id="c344d-108">ShareObject</span></span>
```
Update-AzRmStorageShare -InputObject <PSShare> [-QuotaGiB <Int32>] [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c344d-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="c344d-109">DESCRIPTION</span></span>
<span data-ttu-id="c344d-110">A **New-AzRmStorageShare** parancsmag módosította a tárterület-megosztást.</span><span class="sxs-lookup"><span data-stu-id="c344d-110">The **New-AzRmStorageShare** cmdlet modifies a Storage file share.</span></span>

## <span data-ttu-id="c344d-111">Példák</span><span class="sxs-lookup"><span data-stu-id="c344d-111">EXAMPLES</span></span>

### <span data-ttu-id="c344d-112">Példa 1: a tárterület-fájlmegosztás metaadatait módosítja, és megoszthatja a kvótát a tárolási fiók nevével és a megosztási névvel</span><span class="sxs-lookup"><span data-stu-id="c344d-112">Example 1: Modifies a Storage file share's metadata and share quota with Storage account name and share name</span></span>
```
PS C:\>$share = Update-AzRmStorageShare -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount" -Name "myshare" -QuotaGiB 200 -Metadata @{tag0="value0";tag1="value1"}

PS C:\>$share

Name     StorageAccountName ResourceGroupName Etag                QuotaGiB LastModifiedTime    
----     ------------------ ----------------- ----                -------- ----------------    
myshare  myStorageAccount   myResourceGroup                       200     

PS C:\>$share.Metadata

Key  Value  
---  ----- 
tag0 value0
tag1 value1
```

<span data-ttu-id="c344d-113">Ez a parancs módosítja a tárterület-megosztás metaadatait, és megosztja a kvótát a tárolási fiók nevével és a megosztási névvel, valamint megjeleníti a módosítás eredményét a visszaadott fájlmegosztás objektummal.</span><span class="sxs-lookup"><span data-stu-id="c344d-113">This command modifies a Storage file share's metadata and share quota with Storage account name and share name, and show the modify result with the returned file share object.</span></span>

### <span data-ttu-id="c344d-114">2. példa: egy tárterület-megosztásban tárolt metaadatok módosítása a Storage Account objektummal és a megosztási névvel</span><span class="sxs-lookup"><span data-stu-id="c344d-114">Example 2: Modifies metadata on a Storage file share with Storage account object and share name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount"
PS C:\>$share = Update-AzRmStorageShare -StorageAccount $accountObject -Name "myshare" -Metadata @{tag0="value0";tag1="value1"}
```

<span data-ttu-id="c344d-115">Ez a parancs a tárterület-megosztásban lévő metaadatokat módosította a tárterület-objektummal, és megoszthatja a nevet.</span><span class="sxs-lookup"><span data-stu-id="c344d-115">This command modifies metadata on a Storage file share with Storage account object and share name.</span></span>

### <span data-ttu-id="c344d-116">3. példa: módosítja a kvótát a tárterületet tároló tárterületet tartalmazó tárterületen lévő összes tárterület-megosztásban.</span><span class="sxs-lookup"><span data-stu-id="c344d-116">Example 3: Modifies share quota for all Storage file shares in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount" | Update-AzRmStorageShare -QuotaGiB 5000

Name     StorageAccountName ResourceGroupName Etag                QuotaGiB LastModifiedTime    
----     ------------------ ----------------- ----                -------- ----------------    
share1   myStorageAccount   myResourceGroup                       5000
share2   myStorageAccount   myResourceGroup                       5000
```

<span data-ttu-id="c344d-117">Ez a parancs módosítja a megosztási kvótát 5000-as GiB-fájlként az összes tárterület-megosztáshoz egy csővezetéket tartalmazó tárterület-fiókban.</span><span class="sxs-lookup"><span data-stu-id="c344d-117">This command modifies share quota as 5000 GiB for all Storage file shares in a Storage account with pipeline.</span></span>

## <span data-ttu-id="c344d-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c344d-118">PARAMETERS</span></span>

### <span data-ttu-id="c344d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c344d-119">-DefaultProfile</span></span>
<span data-ttu-id="c344d-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c344d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c344d-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c344d-121">-InputObject</span></span>
<span data-ttu-id="c344d-122">Tárterület-megosztás objektum</span><span class="sxs-lookup"><span data-stu-id="c344d-122">Storage Share object</span></span>

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

### <span data-ttu-id="c344d-123">-Metadata</span><span class="sxs-lookup"><span data-stu-id="c344d-123">-Metadata</span></span>
<span data-ttu-id="c344d-124">Metaadatok megosztása</span><span class="sxs-lookup"><span data-stu-id="c344d-124">Share Metadata</span></span>

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

### <span data-ttu-id="c344d-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c344d-125">-Name</span></span>
<span data-ttu-id="c344d-126">Megosztás neve</span><span class="sxs-lookup"><span data-stu-id="c344d-126">Share Name</span></span>

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

### <span data-ttu-id="c344d-127">-QuotaGiB</span><span class="sxs-lookup"><span data-stu-id="c344d-127">-QuotaGiB</span></span>
<span data-ttu-id="c344d-128">Kvóta megosztása az Gibibyte-on.</span><span class="sxs-lookup"><span data-stu-id="c344d-128">Share Quota in Gibibyte.</span></span>

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

### <span data-ttu-id="c344d-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c344d-129">-ResourceGroupName</span></span>
<span data-ttu-id="c344d-130">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="c344d-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="c344d-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c344d-131">-ResourceId</span></span>
<span data-ttu-id="c344d-132">Adjon meg egy fájlmegosztási erőforrás-azonosítót.</span><span class="sxs-lookup"><span data-stu-id="c344d-132">Input a File Share Resource Id.</span></span>

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

### <span data-ttu-id="c344d-133">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="c344d-133">-StorageAccount</span></span>
<span data-ttu-id="c344d-134">Storage Account objektum</span><span class="sxs-lookup"><span data-stu-id="c344d-134">Storage account object</span></span>

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

### <span data-ttu-id="c344d-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="c344d-135">-StorageAccountName</span></span>
<span data-ttu-id="c344d-136">Tárolási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="c344d-136">Storage Account Name.</span></span>

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

### <span data-ttu-id="c344d-137">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c344d-137">-Confirm</span></span>
<span data-ttu-id="c344d-138">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c344d-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c344d-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c344d-139">-WhatIf</span></span>
<span data-ttu-id="c344d-140">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c344d-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c344d-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c344d-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c344d-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c344d-142">CommonParameters</span></span>
<span data-ttu-id="c344d-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c344d-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c344d-144">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c344d-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c344d-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c344d-145">INPUTS</span></span>

### <span data-ttu-id="c344d-146">System. String</span><span class="sxs-lookup"><span data-stu-id="c344d-146">System.String</span></span>

### <span data-ttu-id="c344d-147">Microsoft. Azure. Command. Management. Storage. models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c344d-147">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="c344d-148">Microsoft. Azure. Command. Management. Storage. models. PSShare</span><span class="sxs-lookup"><span data-stu-id="c344d-148">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="c344d-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c344d-149">OUTPUTS</span></span>

### <span data-ttu-id="c344d-150">Microsoft. Azure. Command. Management. Storage. models. PSShare</span><span class="sxs-lookup"><span data-stu-id="c344d-150">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="c344d-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c344d-151">NOTES</span></span>

## <span data-ttu-id="c344d-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c344d-152">RELATED LINKS</span></span>
