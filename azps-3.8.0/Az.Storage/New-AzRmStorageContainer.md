---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azrmstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzRmStorageContainer.md
ms.openlocfilehash: 06a37226c1915ef858d72ec123dd238011c19f19
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013150"
---
# <span data-ttu-id="f83bd-101">New-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="f83bd-101">New-AzRmStorageContainer</span></span>

## <span data-ttu-id="f83bd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f83bd-102">SYNOPSIS</span></span>
<span data-ttu-id="f83bd-103">Tároló blob-tároló létrehozása</span><span class="sxs-lookup"><span data-stu-id="f83bd-103">Creates a Storage blob container</span></span>

## <span data-ttu-id="f83bd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f83bd-104">SYNTAX</span></span>

### <span data-ttu-id="f83bd-105">AccountName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f83bd-105">AccountName (Default)</span></span>
```
New-AzRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-PublicAccess <PSPublicAccess>] [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f83bd-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="f83bd-106">AccountObject</span></span>
```
New-AzRmStorageContainer -StorageAccount <PSStorageAccount> -Name <String> [-PublicAccess <PSPublicAccess>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f83bd-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="f83bd-107">DESCRIPTION</span></span>
<span data-ttu-id="f83bd-108">A **New-AzRmStorageContainer** parancsmag tároló BLOB-tárolót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="f83bd-108">The **New-AzRmStorageContainer** cmdlet creates a Storage blob container</span></span>

## <span data-ttu-id="f83bd-109">Példák</span><span class="sxs-lookup"><span data-stu-id="f83bd-109">EXAMPLES</span></span>

### <span data-ttu-id="f83bd-110">Példa 1: adattároló blob-tároló létrehozása a tárolási fiók nevével és a tároló nevével, metaadatokkal</span><span class="sxs-lookup"><span data-stu-id="f83bd-110">Example 1: Create a Storage blob container with Storage account name and container name, with metadata</span></span>
```
PS C:\>New-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Metadata @{tag0="value0";tag1="value1";tag2="value2"}
```

<span data-ttu-id="f83bd-111">Ez a parancs a tároló BLOB-tárolót hoz létre a tárolási fiók nevével és a tároló nevével, a metaadatokkal.</span><span class="sxs-lookup"><span data-stu-id="f83bd-111">This command creates a Storage blob container with Storage account name and container name, with metadata.</span></span>

### <span data-ttu-id="f83bd-112">2. példa: adattároló blob-tároló létrehozása a tárolási fiók objektummal és a tároló nevével, a nyilvános hozzáférés blob-ként</span><span class="sxs-lookup"><span data-stu-id="f83bd-112">Example 2: Create a Storage blob container with Storage account object and container name, with public access as Blob</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>New-AzRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer" -PublicAccess Blob
```

<span data-ttu-id="f83bd-113">Ez a parancs létrehoz egy tároló BLOB-tárolót a tárolási fiók objektummal és a tároló nevével, a nyilvános hozzáférés blob-ként.</span><span class="sxs-lookup"><span data-stu-id="f83bd-113">This command creates a Storage blob container with Storage account object and container name, with public access as Blob.</span></span>

## <span data-ttu-id="f83bd-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f83bd-114">PARAMETERS</span></span>

### <span data-ttu-id="f83bd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f83bd-115">-DefaultProfile</span></span>
<span data-ttu-id="f83bd-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f83bd-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f83bd-117">-Metadata</span><span class="sxs-lookup"><span data-stu-id="f83bd-117">-Metadata</span></span>
<span data-ttu-id="f83bd-118">Tároló-metaadatok</span><span class="sxs-lookup"><span data-stu-id="f83bd-118">Container Metadata</span></span>

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

### <span data-ttu-id="f83bd-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f83bd-119">-Name</span></span>
<span data-ttu-id="f83bd-120">Tároló neve</span><span class="sxs-lookup"><span data-stu-id="f83bd-120">Container Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, ContainerName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f83bd-121">-PublicAccess</span><span class="sxs-lookup"><span data-stu-id="f83bd-121">-PublicAccess</span></span>
<span data-ttu-id="f83bd-122">Tároló PublicAccess</span><span class="sxs-lookup"><span data-stu-id="f83bd-122">Container PublicAccess</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSPublicAccess
Parameter Sets: (All)
Aliases:
Accepted values: Container, Blob, None

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f83bd-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f83bd-123">-ResourceGroupName</span></span>
<span data-ttu-id="f83bd-124">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="f83bd-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="f83bd-125">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="f83bd-125">-StorageAccount</span></span>
<span data-ttu-id="f83bd-126">Storage Account objektum</span><span class="sxs-lookup"><span data-stu-id="f83bd-126">Storage account object</span></span>

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

### <span data-ttu-id="f83bd-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="f83bd-127">-StorageAccountName</span></span>
<span data-ttu-id="f83bd-128">Tárolási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="f83bd-128">Storage Account Name.</span></span>

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

### <span data-ttu-id="f83bd-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f83bd-129">-Confirm</span></span>
<span data-ttu-id="f83bd-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f83bd-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f83bd-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f83bd-131">-WhatIf</span></span>
<span data-ttu-id="f83bd-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f83bd-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f83bd-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f83bd-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f83bd-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f83bd-134">CommonParameters</span></span>
<span data-ttu-id="f83bd-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f83bd-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f83bd-136">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f83bd-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f83bd-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f83bd-137">INPUTS</span></span>

### <span data-ttu-id="f83bd-138">System. String</span><span class="sxs-lookup"><span data-stu-id="f83bd-138">System.String</span></span>

### <span data-ttu-id="f83bd-139">Microsoft. Azure. Command. Management. Storage. models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f83bd-139">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="f83bd-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f83bd-140">OUTPUTS</span></span>

### <span data-ttu-id="f83bd-141">Microsoft. Azure. Command. Management. Storage. models. PSContainer</span><span class="sxs-lookup"><span data-stu-id="f83bd-141">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="f83bd-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f83bd-142">NOTES</span></span>

## <span data-ttu-id="f83bd-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f83bd-143">RELATED LINKS</span></span>
