---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azstorageblobserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageBlobServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageBlobServiceProperty.md
ms.openlocfilehash: 84f2303b0907e05bfe03ffacf50f4bcd895500c1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466878"
---
# <span data-ttu-id="1724b-101">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="1724b-101">Update-AzStorageBlobServiceProperty</span></span>

## <span data-ttu-id="1724b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1724b-102">SYNOPSIS</span></span>
<span data-ttu-id="1724b-103">Módosítja az Azure Storage Blob szolgáltatás szolgáltatástulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="1724b-103">Modifies the service properties for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="1724b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="1724b-104">SYNTAX</span></span>

### <span data-ttu-id="1724b-105">AccountName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1724b-105">AccountName (Default)</span></span>
```
Update-AzStorageBlobServiceProperty [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-DefaultServiceVersion <String>] [-EnableChangeFeed <Boolean>] [-IsVersioningEnabled <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1724b-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="1724b-106">AccountObject</span></span>
```
Update-AzStorageBlobServiceProperty -StorageAccount <PSStorageAccount> [-DefaultServiceVersion <String>]
 [-EnableChangeFeed <Boolean>] [-IsVersioningEnabled <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1724b-107">BlobServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="1724b-107">BlobServicePropertiesResourceId</span></span>
```
Update-AzStorageBlobServiceProperty [-ResourceId] <String> [-DefaultServiceVersion <String>]
 [-EnableChangeFeed <Boolean>] [-IsVersioningEnabled <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1724b-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="1724b-108">DESCRIPTION</span></span>
<span data-ttu-id="1724b-109">Az **Update-AzStorageBlobServiceProperty** parancsmag módosítja az Azure Storage Blob szolgáltatás szolgáltatás tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="1724b-109">The **Update-AzStorageBlobServiceProperty** cmdlet modifies the service properties for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="1724b-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="1724b-110">EXAMPLES</span></span>

### <span data-ttu-id="1724b-111">1. példa: A DefaultServiceVersion blobszolgáltatás beállítása 2018-03-28-ra</span><span class="sxs-lookup"><span data-stu-id="1724b-111">Example 1: Set Blob service DefaultServiceVersion to 2018-03-28</span></span>
```
C:\PS> Update-AzStorageBlobServiceProperty -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -DefaultServiceVersion 2018-03-28 

StorageAccountName            : mystorageaccount
ResourceGroupName             : myresourcegroup
DefaultServiceVersion         : 2018-03-28
DeleteRetentionPolicy.Enabled : False
DeleteRetentionPolicy.Days    : 
RestorePolicy.Enabled         : 
RestorePolicy.Days            : 
ChangeFeed                    : 
IsVersioningEnabled           :
```

<span data-ttu-id="1724b-112">Ez a parancs a Blob szolgáltatás DefaultServiceVersion-ét a 2018-03-28-asra állítja.</span><span class="sxs-lookup"><span data-stu-id="1724b-112">This command sets the DefaultServiceVersion of Blob Service to 2018-03-28.</span></span>

### <span data-ttu-id="1724b-113">2. példa: Tárfiók blobszolgáltatásának módosítása</span><span class="sxs-lookup"><span data-stu-id="1724b-113">Example 2: Enable Changefeed on Blob service of a Storage account</span></span>
```
C:\PS> Update-AzStorageBlobServiceProperty -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -EnableChangeFeed $true

StorageAccountName            : mystorageaccount
ResourceGroupName             : myresourcegroup
DefaultServiceVersion         : 
DeleteRetentionPolicy.Enabled : False
DeleteRetentionPolicy.Days    : 
RestorePolicy.Enabled         : 
RestorePolicy.Days            : 
ChangeFeed                    : True
IsVersioningEnabled           :
```

<span data-ttu-id="1724b-114">Ez a parancs lehetővé teszi a Módosítás a Blob szolgáltatásban egy tárfiók módosítási hírcsatornáját az Azure Blob Storage szolgáltatásban úgy, hogy a blobszintű létrehozási, módosítási és törlési eseményekhez figyel egy GPv2- vagy Blob-tárfiókot.</span><span class="sxs-lookup"><span data-stu-id="1724b-114">This command enables Changefeed on Blob service of a Storage account Change feed support in Azure Blob Storage works by listening to a GPv2 or Blob storage account for any blob level creation, modification, or deletion events.</span></span> <span data-ttu-id="1724b-115">Ezután kimenetként egy rendezett eseménynaplót ad a tárfiókon $blobchangefeed tárolóban tárolt blobok számára.</span><span class="sxs-lookup"><span data-stu-id="1724b-115">It then outputs an ordered log of events for the blobs stored in the $blobchangefeed container within the storage account.</span></span> <span data-ttu-id="1724b-116">A szerializált módosításokat a rendszer a Pillanatkép Avro fájlként megőrzve, aszinkron módon és növekményes módon feldolgozhatja.</span><span class="sxs-lookup"><span data-stu-id="1724b-116">The serialized changes are persisted as an Apache Avro file and can be processed asynchronously and incrementally.</span></span>

### <span data-ttu-id="1724b-117">3. példa: A verziószámozás engedélyezése tárfiók Blob szolgáltatásában</span><span class="sxs-lookup"><span data-stu-id="1724b-117">Example 3: Enable Versioning on Blob service of a Storage account</span></span>
```
C:\PS> Update-AzStorageBlobServiceProperty -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -IsVersioningEnabled $true

StorageAccountName            : mystorageaccount
ResourceGroupName             : myresourcegroup
DefaultServiceVersion         : 
DeleteRetentionPolicy.Enabled : False
DeleteRetentionPolicy.Days    : 
RestorePolicy.Enabled         : 
RestorePolicy.Days            : 
ChangeFeed                    : 
IsVersioningEnabled           : True
```

<span data-ttu-id="1724b-118">Ez a parancs lehetővé teszi a verziószámozást egy tárfiók Blob szolgáltatásában</span><span class="sxs-lookup"><span data-stu-id="1724b-118">This command enables Versioning on Blob service of a Storage account</span></span>

## <span data-ttu-id="1724b-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1724b-119">PARAMETERS</span></span>

### <span data-ttu-id="1724b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1724b-120">-DefaultProfile</span></span>
<span data-ttu-id="1724b-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1724b-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1724b-122">-DefaultServiceVersion</span><span class="sxs-lookup"><span data-stu-id="1724b-122">-DefaultServiceVersion</span></span>
<span data-ttu-id="1724b-123">Alapértelmezett szolgáltatásverzió beállítva</span><span class="sxs-lookup"><span data-stu-id="1724b-123">Default Service Version to Set</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1724b-124">-EnableChangeFeed</span><span class="sxs-lookup"><span data-stu-id="1724b-124">-EnableChangeFeed</span></span>
<span data-ttu-id="1724b-125">Engedélyezze a Hírcsatorna módosítása naplózást a tárfiókhoz úgy, hogy $true, letiltja a Hírcsatorna-naplózás módosítása beállítás $false.</span><span class="sxs-lookup"><span data-stu-id="1724b-125">Enable Change Feed logging for the storage account by set to $true, disable Change Feed logging by set to $false.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1724b-126">-IsVersioningEnabled</span><span class="sxs-lookup"><span data-stu-id="1724b-126">-IsVersioningEnabled</span></span>
<span data-ttu-id="1724b-127">A verziószámozást igaz érték esetén engedélyezi vagy állítja be.</span><span class="sxs-lookup"><span data-stu-id="1724b-127">Gets or sets versioning is enabled if set to true.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1724b-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1724b-128">-ResourceGroupName</span></span>
<span data-ttu-id="1724b-129">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="1724b-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="1724b-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1724b-130">-ResourceId</span></span>
<span data-ttu-id="1724b-131">Adja meg a tárfiók erőforrás-azonosítóját vagy blobszolgáltatás erőforrás-azonosítóját.</span><span class="sxs-lookup"><span data-stu-id="1724b-131">Input a Storage account Resource Id, or a Blob service properties Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: BlobServicePropertiesResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1724b-132">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="1724b-132">-StorageAccount</span></span>
<span data-ttu-id="1724b-133">Tárfiók objektum</span><span class="sxs-lookup"><span data-stu-id="1724b-133">Storage account object</span></span>

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

### <span data-ttu-id="1724b-134">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="1724b-134">-StorageAccountName</span></span>
<span data-ttu-id="1724b-135">Tárfiók neve.</span><span class="sxs-lookup"><span data-stu-id="1724b-135">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1724b-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1724b-136">-Confirm</span></span>
<span data-ttu-id="1724b-137">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="1724b-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1724b-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1724b-138">-WhatIf</span></span>
<span data-ttu-id="1724b-139">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="1724b-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1724b-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1724b-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1724b-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1724b-141">CommonParameters</span></span>
<span data-ttu-id="1724b-142">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1724b-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1724b-143">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1724b-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1724b-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1724b-144">INPUTS</span></span>

### <span data-ttu-id="1724b-145">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1724b-145">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="1724b-146">System.String</span><span class="sxs-lookup"><span data-stu-id="1724b-146">System.String</span></span>

## <span data-ttu-id="1724b-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1724b-147">OUTPUTS</span></span>

### <span data-ttu-id="1724b-148">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobServiceProperties</span><span class="sxs-lookup"><span data-stu-id="1724b-148">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobServiceProperties</span></span>

## <span data-ttu-id="1724b-149">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="1724b-149">NOTES</span></span>

## <span data-ttu-id="1724b-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1724b-150">RELATED LINKS</span></span>
