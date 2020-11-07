---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzRmStorageShare.md
ms.openlocfilehash: 01871c63d9a734cba88da30032f8b1da21198160
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839726"
---
# <span data-ttu-id="86f2a-101">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="86f2a-101">New-AzRmStorageShare</span></span>

## <span data-ttu-id="86f2a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="86f2a-102">SYNOPSIS</span></span>
<span data-ttu-id="86f2a-103">Létrehoz egy tárterület-megosztást.</span><span class="sxs-lookup"><span data-stu-id="86f2a-103">Creates a Storage file share.</span></span>

## <span data-ttu-id="86f2a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="86f2a-104">SYNTAX</span></span>

### <span data-ttu-id="86f2a-105">AccountName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="86f2a-105">AccountName (Default)</span></span>
```
New-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-QuotaGiB <Int32>] [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="86f2a-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="86f2a-106">AccountObject</span></span>
```
New-AzRmStorageShare -StorageAccount <PSStorageAccount> -Name <String> [-QuotaGiB <Int32>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="86f2a-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="86f2a-107">DESCRIPTION</span></span>
<span data-ttu-id="86f2a-108">A **New-AzRmStorageShare** parancsmag létrehoz egy tárterület-megosztást.</span><span class="sxs-lookup"><span data-stu-id="86f2a-108">The **New-AzRmStorageShare** cmdlet creates a Storage file share.</span></span>

## <span data-ttu-id="86f2a-109">Példák</span><span class="sxs-lookup"><span data-stu-id="86f2a-109">EXAMPLES</span></span>

### <span data-ttu-id="86f2a-110">Példa 1: tárterület-megosztás létrehozása tárterület-fiók nevével és megosztási névvel, a metaadatok és a kvóta megosztása 100 GiB formátumban.</span><span class="sxs-lookup"><span data-stu-id="86f2a-110">Example 1: Create a Storage file share with Storage account name and share name, with metadata and share quota as 100 GiB.</span></span>
```
PS C:\>New-AzRmStorageShare -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount" -Name "myshare" -QuotaGiB 100 -Metadata @{"tag1" = "value1"; "tag2" = "value2" } 

Name     StorageAccountName ResourceGroupName Etag                QuotaGiB LastModifiedTime    
----     ------------------ ----------------- ----                -------- ----------------    
myshare  myStorageAccount   myResourceGroup   
```

<span data-ttu-id="86f2a-111">A parancs létrehoz egy tárterület-megosztást a metaadatokkal, és megoszthatja a kvótát 100 GiB formátumban.</span><span class="sxs-lookup"><span data-stu-id="86f2a-111">This command creates a Storage file share with metadata and share quota as 100 GiB.</span></span>

### <span data-ttu-id="86f2a-112">2. példa: tárterület-megosztás létrehozása a Storage Account objektummal</span><span class="sxs-lookup"><span data-stu-id="86f2a-112">Example 2: Create a Storage file share with Storage account object</span></span>
```
Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount" | New-AzRmStorageShare -Name "myshare"

Name     StorageAccountName ResourceGroupName Etag                QuotaGiB LastModifiedTime    
----     ------------------ ----------------- ----                -------- ----------------    
myshare  myStorageAccount   myResourceGroup   
```

<span data-ttu-id="86f2a-113">Ez a parancs létrehoz egy tárterület-megosztást a Storage Account objektummal és a megosztási névvel.</span><span class="sxs-lookup"><span data-stu-id="86f2a-113">This command creates a Storage file share with Storage account object and share name.</span></span>

## <span data-ttu-id="86f2a-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="86f2a-114">PARAMETERS</span></span>

### <span data-ttu-id="86f2a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86f2a-115">-DefaultProfile</span></span>
<span data-ttu-id="86f2a-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="86f2a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="86f2a-117">-Metadata</span><span class="sxs-lookup"><span data-stu-id="86f2a-117">-Metadata</span></span>
<span data-ttu-id="86f2a-118">Metaadatok megosztása</span><span class="sxs-lookup"><span data-stu-id="86f2a-118">Share Metadata</span></span>

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

### <span data-ttu-id="86f2a-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="86f2a-119">-Name</span></span>
<span data-ttu-id="86f2a-120">Azure-fájl megosztási neve</span><span class="sxs-lookup"><span data-stu-id="86f2a-120">Azure File share name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, ShareName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="86f2a-121">-QuotaGiB</span><span class="sxs-lookup"><span data-stu-id="86f2a-121">-QuotaGiB</span></span>
<span data-ttu-id="86f2a-122">Kvóta megosztása az Gibibyte-on.</span><span class="sxs-lookup"><span data-stu-id="86f2a-122">Share Quota in Gibibyte.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86f2a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86f2a-123">-ResourceGroupName</span></span>
<span data-ttu-id="86f2a-124">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="86f2a-124">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86f2a-125">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="86f2a-125">-StorageAccount</span></span>
<span data-ttu-id="86f2a-126">Storage Account objektum</span><span class="sxs-lookup"><span data-stu-id="86f2a-126">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="86f2a-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="86f2a-127">-StorageAccountName</span></span>
<span data-ttu-id="86f2a-128">Tárolási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="86f2a-128">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86f2a-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="86f2a-129">-Confirm</span></span>
<span data-ttu-id="86f2a-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="86f2a-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86f2a-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86f2a-131">-WhatIf</span></span>
<span data-ttu-id="86f2a-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="86f2a-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="86f2a-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="86f2a-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="86f2a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86f2a-134">CommonParameters</span></span>
<span data-ttu-id="86f2a-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="86f2a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86f2a-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86f2a-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86f2a-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="86f2a-137">INPUTS</span></span>

### <span data-ttu-id="86f2a-138">System. String</span><span class="sxs-lookup"><span data-stu-id="86f2a-138">System.String</span></span>

### <span data-ttu-id="86f2a-139">Microsoft. Azure. Command. Management. Storage. models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="86f2a-139">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="86f2a-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="86f2a-140">OUTPUTS</span></span>

### <span data-ttu-id="86f2a-141">Microsoft. Azure. Command. Management. Storage. models. PSShare</span><span class="sxs-lookup"><span data-stu-id="86f2a-141">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="86f2a-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="86f2a-142">NOTES</span></span>

## <span data-ttu-id="86f2a-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="86f2a-143">RELATED LINKS</span></span>
