---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/restore-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Restore-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Restore-AzRmStorageShare.md
ms.openlocfilehash: 70d3c8c435a88b4f0f968d1519efd9af6d9907e8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185791"
---
# <span data-ttu-id="79b49-101">Restore-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="79b49-101">Restore-AzRmStorageShare</span></span>

## <span data-ttu-id="79b49-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="79b49-102">SYNOPSIS</span></span>
<span data-ttu-id="79b49-103">Visszaállítja a törölt fájlok megosztását.</span><span class="sxs-lookup"><span data-stu-id="79b49-103">Restores a deleted file share.</span></span>

## <span data-ttu-id="79b49-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="79b49-104">SYNTAX</span></span>

### <span data-ttu-id="79b49-105">AccountName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="79b49-105">AccountName (Default)</span></span>
```
Restore-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 -DeletedShareVersion <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="79b49-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="79b49-106">AccountObject</span></span>
```
Restore-AzRmStorageShare -StorageAccount <PSStorageAccount> -Name <String> -DeletedShareVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79b49-107">ShareObject</span><span class="sxs-lookup"><span data-stu-id="79b49-107">ShareObject</span></span>
```
Restore-AzRmStorageShare -InputObject <PSShare> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="79b49-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="79b49-108">DESCRIPTION</span></span>
<span data-ttu-id="79b49-109">A **Restore-AzRmStorageShare** parancsmag érvényes adatmegőrzési napokon belül visszaállítja a törölt fájlok megosztását, ha engedélyezve van a Soft delete használata.</span><span class="sxs-lookup"><span data-stu-id="79b49-109">The **Restore-AzRmStorageShare** cmdlet restores a deleted file share within a valid retention days if share soft delete is enabled.</span></span>

## <span data-ttu-id="79b49-110">Példák</span><span class="sxs-lookup"><span data-stu-id="79b49-110">EXAMPLES</span></span>

### <span data-ttu-id="79b49-111">1. példa: megosztás eltávolítása és visszaállítása</span><span class="sxs-lookup"><span data-stu-id="79b49-111">Example 1: Remove and restore a share</span></span>
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

<span data-ttu-id="79b49-112">Ez a parancs először törli a fájlokat, majd felsorolja a megosztásokat, és megtekinti a törölt megosztási verziót, végül visszaállítja a normál megosztást.</span><span class="sxs-lookup"><span data-stu-id="79b49-112">This command first delete a file share, and then list shares and see the deleted share version, finally restore it back to a normal share.</span></span> <span data-ttu-id="79b49-113">A megosztás törlése előtt engedélyeznie kell a "Soft Delete" (frissítés – AzStorageFileServiceProperty) lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="79b49-113">Need enabled share soft delete with Update-AzStorageFileServiceProperty, before delete the share.</span></span>

## <span data-ttu-id="79b49-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="79b49-114">PARAMETERS</span></span>

### <span data-ttu-id="79b49-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79b49-115">-DefaultProfile</span></span>
<span data-ttu-id="79b49-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="79b49-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="79b49-117">-DeletedShareVersion</span><span class="sxs-lookup"><span data-stu-id="79b49-117">-DeletedShareVersion</span></span>
<span data-ttu-id="79b49-118">Törölt megosztási verzió, amelyet vissza fog állítani.</span><span class="sxs-lookup"><span data-stu-id="79b49-118">Deleted Share Version, which will be restored from.</span></span>

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

### <span data-ttu-id="79b49-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="79b49-119">-InputObject</span></span>
<span data-ttu-id="79b49-120">Megosztási objektum törlése</span><span class="sxs-lookup"><span data-stu-id="79b49-120">Deleted Share object</span></span>

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

### <span data-ttu-id="79b49-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="79b49-121">-Name</span></span>
<span data-ttu-id="79b49-122">Törölt megosztás neve, amelyet vissza fog állítani.</span><span class="sxs-lookup"><span data-stu-id="79b49-122">Deleted Share Name, which will be restored.</span></span>

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

### <span data-ttu-id="79b49-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79b49-123">-ResourceGroupName</span></span>
<span data-ttu-id="79b49-124">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="79b49-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="79b49-125">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="79b49-125">-StorageAccount</span></span>
<span data-ttu-id="79b49-126">Storage Account objektum</span><span class="sxs-lookup"><span data-stu-id="79b49-126">Storage account object</span></span>

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

### <span data-ttu-id="79b49-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="79b49-127">-StorageAccountName</span></span>
<span data-ttu-id="79b49-128">Tárolási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="79b49-128">Storage Account Name.</span></span>

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

### <span data-ttu-id="79b49-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="79b49-129">-Confirm</span></span>
<span data-ttu-id="79b49-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="79b49-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79b49-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79b49-131">-WhatIf</span></span>
<span data-ttu-id="79b49-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="79b49-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79b49-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="79b49-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79b49-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79b49-134">CommonParameters</span></span>
<span data-ttu-id="79b49-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="79b49-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79b49-136">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79b49-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79b49-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="79b49-137">INPUTS</span></span>

### <span data-ttu-id="79b49-138">Microsoft. Azure. Command. Management. Storage. models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="79b49-138">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="79b49-139">Microsoft. Azure. Command. Management. Storage. models. PSShare</span><span class="sxs-lookup"><span data-stu-id="79b49-139">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="79b49-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="79b49-140">OUTPUTS</span></span>

### <span data-ttu-id="79b49-141">Microsoft. Azure. Command. Management. Storage. models. PSShare</span><span class="sxs-lookup"><span data-stu-id="79b49-141">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="79b49-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="79b49-142">NOTES</span></span>

## <span data-ttu-id="79b49-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="79b49-143">RELATED LINKS</span></span>
