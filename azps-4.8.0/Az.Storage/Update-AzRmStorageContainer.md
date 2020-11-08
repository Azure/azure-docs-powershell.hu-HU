---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azrmstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzRmStorageContainer.md
ms.openlocfilehash: 3ece496830cf3d6b1618bd410e2352d65f6e2fad
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182043"
---
# <span data-ttu-id="65d88-101">Update-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="65d88-101">Update-AzRmStorageContainer</span></span>

## <span data-ttu-id="65d88-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="65d88-102">SYNOPSIS</span></span>
<span data-ttu-id="65d88-103">Tárterület-tároló blob-tárolójának módosítása</span><span class="sxs-lookup"><span data-stu-id="65d88-103">Modifies a Storage blob container</span></span>

## <span data-ttu-id="65d88-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="65d88-104">SYNTAX</span></span>

### <span data-ttu-id="65d88-105">AccountName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="65d88-105">AccountName (Default)</span></span>
```
Update-AzRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-PublicAccess <PSPublicAccess>] [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65d88-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="65d88-106">AccountObject</span></span>
```
Update-AzRmStorageContainer -Name <String> -StorageAccount <PSStorageAccount> [-PublicAccess <PSPublicAccess>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65d88-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="65d88-107">ContainerObject</span></span>
```
Update-AzRmStorageContainer -InputObject <PSContainer> [-PublicAccess <PSPublicAccess>] [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65d88-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="65d88-108">DESCRIPTION</span></span>
<span data-ttu-id="65d88-109">Az **Update-AzRmStorageContainer** parancsmag a tároló blob-tárolóját módosítja.</span><span class="sxs-lookup"><span data-stu-id="65d88-109">The **Update-AzRmStorageContainer** cmdlet modifies a Storage blob container</span></span>

## <span data-ttu-id="65d88-110">Példák</span><span class="sxs-lookup"><span data-stu-id="65d88-110">EXAMPLES</span></span>

### <span data-ttu-id="65d88-111">Példa 1: a Storage blob-tároló metaadatait és a nyilvános hozzáférést a tárolási fiók nevével és a tároló nevével módosítja.</span><span class="sxs-lookup"><span data-stu-id="65d88-111">Example 1: Modifies a Storage blob container's metadata and public access with Storage account name and container name</span></span>
```
PS C:\>Update-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -PublicAccess Container -Metadata @{tag0="value0";tag1="value1"}
```

<span data-ttu-id="65d88-112">Ez a parancs módosítja a blob-tároló metaadatait és a nyilvános hozzáférést a tárolási fiók nevével és a tároló nevével.</span><span class="sxs-lookup"><span data-stu-id="65d88-112">This command modifies a Storage blob container's metadata and public access with Storage account name and container name.</span></span>

### <span data-ttu-id="65d88-113">2. példa: a nyilvános hozzáférés letiltása a tároló blob-tárolójában a tárolási fiók objektummal és a tároló nevével</span><span class="sxs-lookup"><span data-stu-id="65d88-113">Example 2: Disable public access on a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Update-AzRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer" -PublicAccess None
```

<span data-ttu-id="65d88-114">Ez a parancs letiltja a nyilvános hozzáférést a tároló blob-tárolóban a tárolási fiók objektummal és a tároló nevével.</span><span class="sxs-lookup"><span data-stu-id="65d88-114">This command disables public access on a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="65d88-115">3. példa: a nyilvános hozzáférés beállítása blob-ként az adattároló blob-tárolók esetén a csővezetéket tartalmazó tárolási fiókban</span><span class="sxs-lookup"><span data-stu-id="65d88-115">Example 3: Set public access as Blob for all Storage blob containers in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Update-AzRmStorageContainer -PublicAccess Blob
```

<span data-ttu-id="65d88-116">Ez a parancs a nyilvános hozzáférést blob-ként adja meg a csővezetéken tárolt tárterület-tárolókban.</span><span class="sxs-lookup"><span data-stu-id="65d88-116">This command set public access as Blob for all Storage blob containers in a Storage account with pipeline.</span></span>

## <span data-ttu-id="65d88-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="65d88-117">PARAMETERS</span></span>

### <span data-ttu-id="65d88-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65d88-118">-DefaultProfile</span></span>
<span data-ttu-id="65d88-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="65d88-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="65d88-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="65d88-120">-InputObject</span></span>
<span data-ttu-id="65d88-121">Tároló tároló objektum</span><span class="sxs-lookup"><span data-stu-id="65d88-121">Storage container object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSContainer
Parameter Sets: ContainerObject
Aliases: Container

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="65d88-122">-Metadata</span><span class="sxs-lookup"><span data-stu-id="65d88-122">-Metadata</span></span>
<span data-ttu-id="65d88-123">Tároló-metaadatok</span><span class="sxs-lookup"><span data-stu-id="65d88-123">Container Metadata</span></span>

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

### <span data-ttu-id="65d88-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="65d88-124">-Name</span></span>
<span data-ttu-id="65d88-125">Tároló neve</span><span class="sxs-lookup"><span data-stu-id="65d88-125">Container Name</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases: N, ContainerName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="65d88-126">-PublicAccess</span><span class="sxs-lookup"><span data-stu-id="65d88-126">-PublicAccess</span></span>
<span data-ttu-id="65d88-127">Tároló PublicAccess</span><span class="sxs-lookup"><span data-stu-id="65d88-127">Container PublicAccess</span></span>

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

### <span data-ttu-id="65d88-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65d88-128">-ResourceGroupName</span></span>
<span data-ttu-id="65d88-129">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="65d88-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="65d88-130">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="65d88-130">-StorageAccount</span></span>
<span data-ttu-id="65d88-131">Storage Account objektum</span><span class="sxs-lookup"><span data-stu-id="65d88-131">Storage account object</span></span>

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

### <span data-ttu-id="65d88-132">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="65d88-132">-StorageAccountName</span></span>
<span data-ttu-id="65d88-133">Tárolási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="65d88-133">Storage Account Name.</span></span>

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

### <span data-ttu-id="65d88-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="65d88-134">-Confirm</span></span>
<span data-ttu-id="65d88-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="65d88-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65d88-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65d88-136">-WhatIf</span></span>
<span data-ttu-id="65d88-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="65d88-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="65d88-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="65d88-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65d88-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65d88-139">CommonParameters</span></span>
<span data-ttu-id="65d88-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="65d88-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65d88-141">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65d88-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65d88-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="65d88-142">INPUTS</span></span>

### <span data-ttu-id="65d88-143">System. String</span><span class="sxs-lookup"><span data-stu-id="65d88-143">System.String</span></span>

### <span data-ttu-id="65d88-144">Microsoft. Azure. Command. Management. Storage. models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="65d88-144">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="65d88-145">Microsoft. Azure. Command. Management. Storage. models. PSContainer</span><span class="sxs-lookup"><span data-stu-id="65d88-145">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="65d88-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="65d88-146">OUTPUTS</span></span>

### <span data-ttu-id="65d88-147">Microsoft. Azure. Command. Management. Storage. models. PSContainer</span><span class="sxs-lookup"><span data-stu-id="65d88-147">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="65d88-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="65d88-148">NOTES</span></span>

## <span data-ttu-id="65d88-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="65d88-149">RELATED LINKS</span></span>
