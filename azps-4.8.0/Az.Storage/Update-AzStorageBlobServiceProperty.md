---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azstorageblobserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageBlobServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageBlobServiceProperty.md
ms.openlocfilehash: 84f2303b0907e05bfe03ffacf50f4bcd895500c1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94180759"
---
# <span data-ttu-id="ee645-101">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="ee645-101">Update-AzStorageBlobServiceProperty</span></span>

## <span data-ttu-id="ee645-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ee645-102">SYNOPSIS</span></span>
<span data-ttu-id="ee645-103">Módosítja az Azure Storage blob szolgáltatás szolgáltatás tulajdonságát.</span><span class="sxs-lookup"><span data-stu-id="ee645-103">Modifies the service properties for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="ee645-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ee645-104">SYNTAX</span></span>

### <span data-ttu-id="ee645-105">AccountName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ee645-105">AccountName (Default)</span></span>
```
Update-AzStorageBlobServiceProperty [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-DefaultServiceVersion <String>] [-EnableChangeFeed <Boolean>] [-IsVersioningEnabled <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee645-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="ee645-106">AccountObject</span></span>
```
Update-AzStorageBlobServiceProperty -StorageAccount <PSStorageAccount> [-DefaultServiceVersion <String>]
 [-EnableChangeFeed <Boolean>] [-IsVersioningEnabled <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee645-107">BlobServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="ee645-107">BlobServicePropertiesResourceId</span></span>
```
Update-AzStorageBlobServiceProperty [-ResourceId] <String> [-DefaultServiceVersion <String>]
 [-EnableChangeFeed <Boolean>] [-IsVersioningEnabled <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee645-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="ee645-108">DESCRIPTION</span></span>
<span data-ttu-id="ee645-109">Az **Update-AzStorageBlobServiceProperty** parancsmag módosítja az Azure Storage blob szolgáltatás tulajdonságát.</span><span class="sxs-lookup"><span data-stu-id="ee645-109">The **Update-AzStorageBlobServiceProperty** cmdlet modifies the service properties for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="ee645-110">Példák</span><span class="sxs-lookup"><span data-stu-id="ee645-110">EXAMPLES</span></span>

### <span data-ttu-id="ee645-111">1. példa: a blob-szolgáltatás DefaultServiceVersion beállítása az 2018-03-28-be</span><span class="sxs-lookup"><span data-stu-id="ee645-111">Example 1: Set Blob service DefaultServiceVersion to 2018-03-28</span></span>
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

<span data-ttu-id="ee645-112">Ez a parancs a blob-szolgáltatás DefaultServiceVersion a 2018-03-28-ra állítja be.</span><span class="sxs-lookup"><span data-stu-id="ee645-112">This command sets the DefaultServiceVersion of Blob Service to 2018-03-28.</span></span>

### <span data-ttu-id="ee645-113">2. példa: a Changefeed engedélyezése a tárolási fiók blob-szolgáltatásában</span><span class="sxs-lookup"><span data-stu-id="ee645-113">Example 2: Enable Changefeed on Blob service of a Storage account</span></span>
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

<span data-ttu-id="ee645-114">Ez a parancs lehetővé teszi, hogy a tárolási fiók blob-szolgáltatásakor a Changefeed módosítása az Azure Blob-tárolóban a GPv2 vagy a blob tárolási fiókjával minden blob-szintű létrehozási, módosítási vagy törlési eseményre figyeljen.</span><span class="sxs-lookup"><span data-stu-id="ee645-114">This command enables Changefeed on Blob service of a Storage account Change feed support in Azure Blob Storage works by listening to a GPv2 or Blob storage account for any blob level creation, modification, or deletion events.</span></span> <span data-ttu-id="ee645-115">Ezután egy rendezett naplót ad eredményül a $blobchangefeed tárolóban tárolt blobokra vonatkozóan.</span><span class="sxs-lookup"><span data-stu-id="ee645-115">It then outputs an ordered log of events for the blobs stored in the $blobchangefeed container within the storage account.</span></span> <span data-ttu-id="ee645-116">A szerializált módosítások Apache Avro-fájlként maradnak, és aszinkron módon és fokozatosan is feldolgozhatók.</span><span class="sxs-lookup"><span data-stu-id="ee645-116">The serialized changes are persisted as an Apache Avro file and can be processed asynchronously and incrementally.</span></span>

### <span data-ttu-id="ee645-117">3. példa: a verziószámozás engedélyezése a tárolási fiók blob-szolgáltatásában</span><span class="sxs-lookup"><span data-stu-id="ee645-117">Example 3: Enable Versioning on Blob service of a Storage account</span></span>
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

<span data-ttu-id="ee645-118">Ez a parancs lehetővé teszi a tárolási fiók blob-szolgáltatásban való verziószámozását.</span><span class="sxs-lookup"><span data-stu-id="ee645-118">This command enables Versioning on Blob service of a Storage account</span></span>

## <span data-ttu-id="ee645-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ee645-119">PARAMETERS</span></span>

### <span data-ttu-id="ee645-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee645-120">-DefaultProfile</span></span>
<span data-ttu-id="ee645-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ee645-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee645-122">-DefaultServiceVersion</span><span class="sxs-lookup"><span data-stu-id="ee645-122">-DefaultServiceVersion</span></span>
<span data-ttu-id="ee645-123">A beállítani kívánt alapértelmezett szolgáltatási verzió</span><span class="sxs-lookup"><span data-stu-id="ee645-123">Default Service Version to Set</span></span>

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

### <span data-ttu-id="ee645-124">-EnableChangeFeed</span><span class="sxs-lookup"><span data-stu-id="ee645-124">-EnableChangeFeed</span></span>
<span data-ttu-id="ee645-125">Engedélyezze a tárterület-naplózás beállítását úgy, hogy a tárterületet a $true értékre állítja, tiltsa le a hírcsatorna-naplózás módosítását $false értékre.</span><span class="sxs-lookup"><span data-stu-id="ee645-125">Enable Change Feed logging for the storage account by set to $true, disable Change Feed logging by set to $false.</span></span>

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

### <span data-ttu-id="ee645-126">-IsVersioningEnabled</span><span class="sxs-lookup"><span data-stu-id="ee645-126">-IsVersioningEnabled</span></span>
<span data-ttu-id="ee645-127">A verziószámozás beírásakor vagy beállításakor a True értékre van beállítva.</span><span class="sxs-lookup"><span data-stu-id="ee645-127">Gets or sets versioning is enabled if set to true.</span></span>

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

### <span data-ttu-id="ee645-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee645-128">-ResourceGroupName</span></span>
<span data-ttu-id="ee645-129">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="ee645-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="ee645-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ee645-130">-ResourceId</span></span>
<span data-ttu-id="ee645-131">Adja meg a tárolási fiók erőforrás-azonosítóját vagy a blob-szolgáltatás tulajdonságainak erőforrás-azonosítóját.</span><span class="sxs-lookup"><span data-stu-id="ee645-131">Input a Storage account Resource Id, or a Blob service properties Resource Id.</span></span>

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

### <span data-ttu-id="ee645-132">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="ee645-132">-StorageAccount</span></span>
<span data-ttu-id="ee645-133">Storage Account objektum</span><span class="sxs-lookup"><span data-stu-id="ee645-133">Storage account object</span></span>

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

### <span data-ttu-id="ee645-134">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="ee645-134">-StorageAccountName</span></span>
<span data-ttu-id="ee645-135">Tárolási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="ee645-135">Storage Account Name.</span></span>

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

### <span data-ttu-id="ee645-136">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ee645-136">-Confirm</span></span>
<span data-ttu-id="ee645-137">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ee645-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee645-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee645-138">-WhatIf</span></span>
<span data-ttu-id="ee645-139">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ee645-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee645-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ee645-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee645-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee645-141">CommonParameters</span></span>
<span data-ttu-id="ee645-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ee645-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee645-143">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee645-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee645-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ee645-144">INPUTS</span></span>

### <span data-ttu-id="ee645-145">Microsoft. Azure. Command. Management. Storage. models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ee645-145">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="ee645-146">System. String</span><span class="sxs-lookup"><span data-stu-id="ee645-146">System.String</span></span>

## <span data-ttu-id="ee645-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ee645-147">OUTPUTS</span></span>

### <span data-ttu-id="ee645-148">Microsoft. Azure. Command. Management. Storage. models. PSBlobServiceProperties</span><span class="sxs-lookup"><span data-stu-id="ee645-148">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobServiceProperties</span></span>

## <span data-ttu-id="ee645-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ee645-149">NOTES</span></span>

## <span data-ttu-id="ee645-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ee645-150">RELATED LINKS</span></span>
