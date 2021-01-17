---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/restore-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Restore-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Restore-AzRmStorageShare.md
ms.openlocfilehash: 70d3c8c435a88b4f0f968d1519efd9af6d9907e8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98348402"
---
# <span data-ttu-id="43868-101">Restore-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="43868-101">Restore-AzRmStorageShare</span></span>

## <span data-ttu-id="43868-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="43868-102">SYNOPSIS</span></span>
<span data-ttu-id="43868-103">Törölt fájlmegosztás visszaállítása.</span><span class="sxs-lookup"><span data-stu-id="43868-103">Restores a deleted file share.</span></span>

## <span data-ttu-id="43868-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="43868-104">SYNTAX</span></span>

### <span data-ttu-id="43868-105">AccountName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="43868-105">AccountName (Default)</span></span>
```
Restore-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 -DeletedShareVersion <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="43868-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="43868-106">AccountObject</span></span>
```
Restore-AzRmStorageShare -StorageAccount <PSStorageAccount> -Name <String> -DeletedShareVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43868-107">ShareObject</span><span class="sxs-lookup"><span data-stu-id="43868-107">ShareObject</span></span>
```
Restore-AzRmStorageShare -InputObject <PSShare> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="43868-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="43868-108">DESCRIPTION</span></span>
<span data-ttu-id="43868-109">A **Restore-AzRmStorageShare** parancsmag érvényes adatmegőrzési napon belül visszaállítja a törölt fájlmegosztást, ha engedélyezve van a megosztás helyreállítható törlése.</span><span class="sxs-lookup"><span data-stu-id="43868-109">The **Restore-AzRmStorageShare** cmdlet restores a deleted file share within a valid retention days if share soft delete is enabled.</span></span>

## <span data-ttu-id="43868-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="43868-110">EXAMPLES</span></span>

### <span data-ttu-id="43868-111">1. példa: Megosztás eltávolítása és visszaállítása</span><span class="sxs-lookup"><span data-stu-id="43868-111">Example 1: Remove and restore a share</span></span>
```powershell
PS C:\> Remove-AzRmStorageShare -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -Name $shareName -Force

PS C:\> Get-AzRmStorageShare -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -IncludeDeleted 

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier           Deleted Version          ShareUsageBytes
----     -------- --------------- ----------           ------- -------          ---------------
test     100                      TransactionOptimized                                         
share1   100                      TransactionOptimized True    01D61FD1FC5498B6                

PS C:\> Restore-AzRmStorageShare -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -Name $shareName -DeletedShareVersion 01D61FD1FC5498B6

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
share1   100
```

<span data-ttu-id="43868-112">Ez a parancs először töröl egy fájlmegosztást, majd felsorolja a megosztásokat, és láthatja a törölt megosztási verziót, végül visszaállíthatja azt egy normál megosztásra.</span><span class="sxs-lookup"><span data-stu-id="43868-112">This command first delete a file share, and then list shares and see the deleted share version, finally restore it back to a normal share.</span></span> <span data-ttu-id="43868-113">A megosztás törlése előtt engedélyeznie kell a "soft delete" megosztást az Update-AzStorageFileServiceProperty fájlban.</span><span class="sxs-lookup"><span data-stu-id="43868-113">Need enabled share soft delete with Update-AzStorageFileServiceProperty, before delete the share.</span></span>

## <span data-ttu-id="43868-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="43868-114">PARAMETERS</span></span>

### <span data-ttu-id="43868-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43868-115">-DefaultProfile</span></span>
<span data-ttu-id="43868-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="43868-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43868-117">-DeletedShareVersion</span><span class="sxs-lookup"><span data-stu-id="43868-117">-DeletedShareVersion</span></span>
<span data-ttu-id="43868-118">Törölt megosztási verzió, amelyből a rendszer visszaállítja az adatokat.</span><span class="sxs-lookup"><span data-stu-id="43868-118">Deleted Share Version, which will be restored from.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43868-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="43868-119">-InputObject</span></span>
<span data-ttu-id="43868-120">Törölt Megosztás objektum</span><span class="sxs-lookup"><span data-stu-id="43868-120">Deleted Share object</span></span>

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

### <span data-ttu-id="43868-121">-Name</span><span class="sxs-lookup"><span data-stu-id="43868-121">-Name</span></span>
<span data-ttu-id="43868-122">Törölt megosztás neve, amelyet a rendszer visszaállít.</span><span class="sxs-lookup"><span data-stu-id="43868-122">Deleted Share Name, which will be restored.</span></span>

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

### <span data-ttu-id="43868-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43868-123">-ResourceGroupName</span></span>
<span data-ttu-id="43868-124">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="43868-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="43868-125">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="43868-125">-StorageAccount</span></span>
<span data-ttu-id="43868-126">Tárfiók objektum</span><span class="sxs-lookup"><span data-stu-id="43868-126">Storage account object</span></span>

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

### <span data-ttu-id="43868-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="43868-127">-StorageAccountName</span></span>
<span data-ttu-id="43868-128">Tárfiók neve.</span><span class="sxs-lookup"><span data-stu-id="43868-128">Storage Account Name.</span></span>

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

### <span data-ttu-id="43868-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="43868-129">-Confirm</span></span>
<span data-ttu-id="43868-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="43868-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43868-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43868-131">-WhatIf</span></span>
<span data-ttu-id="43868-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="43868-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="43868-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="43868-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43868-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43868-134">CommonParameters</span></span>
<span data-ttu-id="43868-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43868-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43868-136">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43868-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43868-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="43868-137">INPUTS</span></span>

### <span data-ttu-id="43868-138">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="43868-138">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="43868-139">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span><span class="sxs-lookup"><span data-stu-id="43868-139">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="43868-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="43868-140">OUTPUTS</span></span>

### <span data-ttu-id="43868-141">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span><span class="sxs-lookup"><span data-stu-id="43868-141">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="43868-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="43868-142">NOTES</span></span>

## <span data-ttu-id="43868-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="43868-143">RELATED LINKS</span></span>
