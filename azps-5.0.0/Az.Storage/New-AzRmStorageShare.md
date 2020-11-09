---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzRmStorageShare.md
ms.openlocfilehash: 4dc3914e4a8bc9113dd16ab431db53ddcf00ab5a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301736"
---
# <span data-ttu-id="e8c28-101">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="e8c28-101">New-AzRmStorageShare</span></span>

## <span data-ttu-id="e8c28-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e8c28-102">SYNOPSIS</span></span>
<span data-ttu-id="e8c28-103">Létrehoz egy tárterület-megosztást.</span><span class="sxs-lookup"><span data-stu-id="e8c28-103">Creates a Storage file share.</span></span>

## <span data-ttu-id="e8c28-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e8c28-104">SYNTAX</span></span>

### <span data-ttu-id="e8c28-105">AccountName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e8c28-105">AccountName (Default)</span></span>
```
New-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-QuotaGiB <Int32>] [-Metadata <Hashtable>] [-AccessTier <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8c28-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="e8c28-106">AccountObject</span></span>
```
New-AzRmStorageShare -StorageAccount <PSStorageAccount> -Name <String> [-QuotaGiB <Int32>]
 [-Metadata <Hashtable>] [-AccessTier <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e8c28-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="e8c28-107">DESCRIPTION</span></span>
<span data-ttu-id="e8c28-108">A **New-AzRmStorageShare** parancsmag létrehoz egy tárterület-megosztást.</span><span class="sxs-lookup"><span data-stu-id="e8c28-108">The **New-AzRmStorageShare** cmdlet creates a Storage file share.</span></span>

## <span data-ttu-id="e8c28-109">Példák</span><span class="sxs-lookup"><span data-stu-id="e8c28-109">EXAMPLES</span></span>

### <span data-ttu-id="e8c28-110">Példa 1: tárterület-megosztás létrehozása tárterület-fiók nevével és megosztási névvel, a metaadatok és a kvóta megosztása 100 GiB formátumban.</span><span class="sxs-lookup"><span data-stu-id="e8c28-110">Example 1: Create a Storage file share with Storage account name and share name, with metadata and share quota as 100 GiB.</span></span>
```
PS C:\>New-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -Name "myshare" -QuotaGiB 100 -Metadata @{"tag1" = "value1"; "tag2" = "value2" } 

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
myshare
```

<span data-ttu-id="e8c28-111">A parancs létrehoz egy tárterület-megosztást a metaadatokkal, és megoszthatja a kvótát 100 GiB formátumban.</span><span class="sxs-lookup"><span data-stu-id="e8c28-111">This command creates a Storage file share with metadata and share quota as 100 GiB.</span></span>

### <span data-ttu-id="e8c28-112">2. példa: tárterület-megosztás létrehozása a Storage Account objektummal</span><span class="sxs-lookup"><span data-stu-id="e8c28-112">Example 2: Create a Storage file share with Storage account object</span></span>
```
Get-AzStorageAccount -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" | New-AzRmStorageShare -Name "myshare"

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
myshare
```

<span data-ttu-id="e8c28-113">Ez a parancs létrehoz egy tárterület-megosztást a Storage Account objektummal és a megosztási névvel.</span><span class="sxs-lookup"><span data-stu-id="e8c28-113">This command creates a Storage file share with Storage account object and share name.</span></span>

### <span data-ttu-id="e8c28-114">3. példa: tárterület-megosztás létrehozása a accesstier (Hot)</span><span class="sxs-lookup"><span data-stu-id="e8c28-114">Example 3: Create a Storage file share with accesstier as Hot</span></span>
```
PS C:\>$share = New-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -Name "myshare" -AccessTier Hot

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocols AccessTier Deleted Version ShareUsageBytes
----     -------- ---------------- ---------- ------- ------- ---------------
myshare                            Hot
```

<span data-ttu-id="e8c28-115">A parancs létrehoz egy tárterület-megosztást a accesstier-ban forró fájlként.</span><span class="sxs-lookup"><span data-stu-id="e8c28-115">This command creates a Storage file share with accesstier as Hot.</span></span>

## <span data-ttu-id="e8c28-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e8c28-116">PARAMETERS</span></span>

### <span data-ttu-id="e8c28-117">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="e8c28-117">-AccessTier</span></span>
<span data-ttu-id="e8c28-118">Access-szint adott megosztáshoz.</span><span class="sxs-lookup"><span data-stu-id="e8c28-118">Access tier for specific share.</span></span> <span data-ttu-id="e8c28-119">Az StorageV2-fiók a TransactionOptimized (alapértelmezett), a meleg és a hűvös beállítás között választhatja ki.</span><span class="sxs-lookup"><span data-stu-id="e8c28-119">StorageV2 account can choose between TransactionOptimized (default), Hot, and Cool.</span></span> <span data-ttu-id="e8c28-120">Az FileStorage-fiók a prémium lehetőséget is választhatja.</span><span class="sxs-lookup"><span data-stu-id="e8c28-120">FileStorage account can choose Premium.</span></span>

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

### <span data-ttu-id="e8c28-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8c28-121">-DefaultProfile</span></span>
<span data-ttu-id="e8c28-122">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e8c28-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8c28-123">-Metadata</span><span class="sxs-lookup"><span data-stu-id="e8c28-123">-Metadata</span></span>
<span data-ttu-id="e8c28-124">Metaadatok megosztása</span><span class="sxs-lookup"><span data-stu-id="e8c28-124">Share Metadata</span></span>

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

### <span data-ttu-id="e8c28-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e8c28-125">-Name</span></span>
<span data-ttu-id="e8c28-126">Azure-fájl megosztási neve</span><span class="sxs-lookup"><span data-stu-id="e8c28-126">Azure File share name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, ShareName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8c28-127">-QuotaGiB</span><span class="sxs-lookup"><span data-stu-id="e8c28-127">-QuotaGiB</span></span>
<span data-ttu-id="e8c28-128">Kvóta megosztása az Gibibyte-on.</span><span class="sxs-lookup"><span data-stu-id="e8c28-128">Share Quota in Gibibyte.</span></span>

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

### <span data-ttu-id="e8c28-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8c28-129">-ResourceGroupName</span></span>
<span data-ttu-id="e8c28-130">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="e8c28-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="e8c28-131">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="e8c28-131">-StorageAccount</span></span>
<span data-ttu-id="e8c28-132">Storage Account objektum</span><span class="sxs-lookup"><span data-stu-id="e8c28-132">Storage account object</span></span>

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

### <span data-ttu-id="e8c28-133">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="e8c28-133">-StorageAccountName</span></span>
<span data-ttu-id="e8c28-134">Tárolási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="e8c28-134">Storage Account Name.</span></span>

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

### <span data-ttu-id="e8c28-135">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e8c28-135">-Confirm</span></span>
<span data-ttu-id="e8c28-136">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e8c28-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8c28-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8c28-137">-WhatIf</span></span>
<span data-ttu-id="e8c28-138">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e8c28-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8c28-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e8c28-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8c28-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8c28-140">CommonParameters</span></span>
<span data-ttu-id="e8c28-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e8c28-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8c28-142">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8c28-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8c28-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e8c28-143">INPUTS</span></span>

### <span data-ttu-id="e8c28-144">System. String</span><span class="sxs-lookup"><span data-stu-id="e8c28-144">System.String</span></span>

### <span data-ttu-id="e8c28-145">Microsoft. Azure. Command. Management. Storage. models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e8c28-145">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="e8c28-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e8c28-146">OUTPUTS</span></span>

### <span data-ttu-id="e8c28-147">Microsoft. Azure. Command. Management. Storage. models. PSShare</span><span class="sxs-lookup"><span data-stu-id="e8c28-147">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="e8c28-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e8c28-148">NOTES</span></span>

## <span data-ttu-id="e8c28-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e8c28-149">RELATED LINKS</span></span>
