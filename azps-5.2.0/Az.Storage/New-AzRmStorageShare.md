---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzRmStorageShare.md
ms.openlocfilehash: 4dc3914e4a8bc9113dd16ab431db53ddcf00ab5a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98349506"
---
# <span data-ttu-id="976c6-101">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="976c6-101">New-AzRmStorageShare</span></span>

## <span data-ttu-id="976c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="976c6-102">SYNOPSIS</span></span>
<span data-ttu-id="976c6-103">Tárterületfájl-megosztást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="976c6-103">Creates a Storage file share.</span></span>

## <span data-ttu-id="976c6-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="976c6-104">SYNTAX</span></span>

### <span data-ttu-id="976c6-105">AccountName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="976c6-105">AccountName (Default)</span></span>
```
New-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-QuotaGiB <Int32>] [-Metadata <Hashtable>] [-AccessTier <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="976c6-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="976c6-106">AccountObject</span></span>
```
New-AzRmStorageShare -StorageAccount <PSStorageAccount> -Name <String> [-QuotaGiB <Int32>]
 [-Metadata <Hashtable>] [-AccessTier <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="976c6-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="976c6-107">DESCRIPTION</span></span>
<span data-ttu-id="976c6-108">A **New-AzRmStorageShare** parancsmag tárhelyfájlmegosztást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="976c6-108">The **New-AzRmStorageShare** cmdlet creates a Storage file share.</span></span>

## <span data-ttu-id="976c6-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="976c6-109">EXAMPLES</span></span>

### <span data-ttu-id="976c6-110">1. példa: Tárterületfájl-megosztás létrehozása a Tárfiók nevével és a megosztás nevével, metaadatokkal és 100 GiB-ként való megosztási kvótával.</span><span class="sxs-lookup"><span data-stu-id="976c6-110">Example 1: Create a Storage file share with Storage account name and share name, with metadata and share quota as 100 GiB.</span></span>
```
PS C:\>New-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -Name "myshare" -QuotaGiB 100 -Metadata @{"tag1" = "value1"; "tag2" = "value2" } 

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
myshare
```

<span data-ttu-id="976c6-111">Ez a parancs metaadatokkal és 100 GiB-ként való megosztási kvótával hoz létre tárhelyfájlmegosztást.</span><span class="sxs-lookup"><span data-stu-id="976c6-111">This command creates a Storage file share with metadata and share quota as 100 GiB.</span></span>

### <span data-ttu-id="976c6-112">2. példa: Tárterületfájl-megosztás létrehozása a Tárfiók objektummal</span><span class="sxs-lookup"><span data-stu-id="976c6-112">Example 2: Create a Storage file share with Storage account object</span></span>
```
Get-AzStorageAccount -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" | New-AzRmStorageShare -Name "myshare"

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
myshare
```

<span data-ttu-id="976c6-113">Ez a parancs tárterületfájlmegosztást hoz létre a Tárfiók objektummal és a megosztás nevével.</span><span class="sxs-lookup"><span data-stu-id="976c6-113">This command creates a Storage file share with Storage account object and share name.</span></span>

### <span data-ttu-id="976c6-114">3. példa: Tárterületfájl-megosztás létrehozása a gyorselérési eléréssel</span><span class="sxs-lookup"><span data-stu-id="976c6-114">Example 3: Create a Storage file share with accesstier as Hot</span></span>
```
PS C:\>$share = New-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -Name "myshare" -AccessTier Hot

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocols AccessTier Deleted Version ShareUsageBytes
----     -------- ---------------- ---------- ------- ------- ---------------
myshare                            Hot
```

<span data-ttu-id="976c6-115">Ez a parancs egy Tárterületfájl-megosztást hoz létre az accesstier hot (Gyors) formátumban.</span><span class="sxs-lookup"><span data-stu-id="976c6-115">This command creates a Storage file share with accesstier as Hot.</span></span>

## <span data-ttu-id="976c6-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="976c6-116">PARAMETERS</span></span>

### <span data-ttu-id="976c6-117">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="976c6-117">-AccessTier</span></span>
<span data-ttu-id="976c6-118">Adott megosztás hozzáférési rétege.</span><span class="sxs-lookup"><span data-stu-id="976c6-118">Access tier for specific share.</span></span> <span data-ttu-id="976c6-119">A StorageV2-fiók választhat a TransactionOptimized (alapértelmezett), a Gyors és a Gyors beállítás közül.</span><span class="sxs-lookup"><span data-stu-id="976c6-119">StorageV2 account can choose between TransactionOptimized (default), Hot, and Cool.</span></span> <span data-ttu-id="976c6-120">A FileStorage-fiók választhatja a Prémium kategóriát.</span><span class="sxs-lookup"><span data-stu-id="976c6-120">FileStorage account can choose Premium.</span></span>

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

### <span data-ttu-id="976c6-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="976c6-121">-DefaultProfile</span></span>
<span data-ttu-id="976c6-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="976c6-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="976c6-123">-Metadata</span><span class="sxs-lookup"><span data-stu-id="976c6-123">-Metadata</span></span>
<span data-ttu-id="976c6-124">Metaadatok megosztása</span><span class="sxs-lookup"><span data-stu-id="976c6-124">Share Metadata</span></span>

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

### <span data-ttu-id="976c6-125">-Name</span><span class="sxs-lookup"><span data-stu-id="976c6-125">-Name</span></span>
<span data-ttu-id="976c6-126">Azure-fájlmegosztás neve</span><span class="sxs-lookup"><span data-stu-id="976c6-126">Azure File share name</span></span>

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

### <span data-ttu-id="976c6-127">-QuotaGiB</span><span class="sxs-lookup"><span data-stu-id="976c6-127">-QuotaGiB</span></span>
<span data-ttu-id="976c6-128">Share Quota in Gibibyte.</span><span class="sxs-lookup"><span data-stu-id="976c6-128">Share Quota in Gibibyte.</span></span>

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

### <span data-ttu-id="976c6-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="976c6-129">-ResourceGroupName</span></span>
<span data-ttu-id="976c6-130">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="976c6-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="976c6-131">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="976c6-131">-StorageAccount</span></span>
<span data-ttu-id="976c6-132">Tárfiók objektum</span><span class="sxs-lookup"><span data-stu-id="976c6-132">Storage account object</span></span>

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

### <span data-ttu-id="976c6-133">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="976c6-133">-StorageAccountName</span></span>
<span data-ttu-id="976c6-134">Tárfiók neve.</span><span class="sxs-lookup"><span data-stu-id="976c6-134">Storage Account Name.</span></span>

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

### <span data-ttu-id="976c6-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="976c6-135">-Confirm</span></span>
<span data-ttu-id="976c6-136">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="976c6-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="976c6-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="976c6-137">-WhatIf</span></span>
<span data-ttu-id="976c6-138">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="976c6-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="976c6-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="976c6-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="976c6-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="976c6-140">CommonParameters</span></span>
<span data-ttu-id="976c6-141">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="976c6-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="976c6-142">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="976c6-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="976c6-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="976c6-143">INPUTS</span></span>

### <span data-ttu-id="976c6-144">System.String</span><span class="sxs-lookup"><span data-stu-id="976c6-144">System.String</span></span>

### <span data-ttu-id="976c6-145">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="976c6-145">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="976c6-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="976c6-146">OUTPUTS</span></span>

### <span data-ttu-id="976c6-147">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span><span class="sxs-lookup"><span data-stu-id="976c6-147">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="976c6-148">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="976c6-148">NOTES</span></span>

## <span data-ttu-id="976c6-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="976c6-149">RELATED LINKS</span></span>
