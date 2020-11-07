---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: BC00DEF9-6A93-4DF5-8E5B-C488551BA1D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/import-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Import-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Import-AzRedisCache.md
ms.openlocfilehash: 018518f359c1142f9e20536f795b9080a942beaa
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669553"
---
# <span data-ttu-id="3e82d-101">Import-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="3e82d-101">Import-AzRedisCache</span></span>

## <span data-ttu-id="3e82d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3e82d-102">SYNOPSIS</span></span>
<span data-ttu-id="3e82d-103">Az adatimportálást a Blobs-ról Azure Redis-gyorsítótárba importálja.</span><span class="sxs-lookup"><span data-stu-id="3e82d-103">Imports data from blobs to Azure Redis Cache.</span></span>

## <span data-ttu-id="3e82d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3e82d-104">SYNTAX</span></span>

```
Import-AzRedisCache [-ResourceGroupName <String>] -Name <String> -Files <String[]> [-Format <String>] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e82d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3e82d-105">DESCRIPTION</span></span>
<span data-ttu-id="3e82d-106">Az **import-AzRedisCache** parancsmag az adatait a Blobs-ról Azure Redis-gyorsítótárba importálja.</span><span class="sxs-lookup"><span data-stu-id="3e82d-106">The **Import-AzRedisCache** cmdlet imports data from blobs into Azure Redis Cache.</span></span>

## <span data-ttu-id="3e82d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="3e82d-107">EXAMPLES</span></span>

### <span data-ttu-id="3e82d-108">1. példa: az adatimportálás</span><span class="sxs-lookup"><span data-stu-id="3e82d-108">Example 1: Import data</span></span>
```
PS C:\>Import-AzRedisCache -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -Files @("https://mystorageaccount.blob.core.windows.net/container22/blobname?sv=2015-04-05&sr=b&sig=caIwutG2uDa0NZ8mjdNJdgOY8%2F8mhwRuGNdICU%2B0pI4%3D&st=2016-05-27T00%3A00%3A00Z&se=2016-05-28T00%3A00%3A00Z&sp=rwd") -Force
```

<span data-ttu-id="3e82d-109">Ez a parancs a biztonsági társítás URL-címének az Azure Redis-gyorsítótárba történő importálására szolgáló blob-adatot importálja.</span><span class="sxs-lookup"><span data-stu-id="3e82d-109">This command imports data from the blob that is specified by the SAS URL into Azure Redis Cache.</span></span>

## <span data-ttu-id="3e82d-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3e82d-110">PARAMETERS</span></span>

### <span data-ttu-id="3e82d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e82d-111">-DefaultProfile</span></span>
<span data-ttu-id="3e82d-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3e82d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3e82d-113">-Files</span><span class="sxs-lookup"><span data-stu-id="3e82d-113">-Files</span></span>
<span data-ttu-id="3e82d-114">Itt adhatja meg, hogy a program miként importálja a gyorsítótárba a parancsmagok által importált bináris fájlokat.</span><span class="sxs-lookup"><span data-stu-id="3e82d-114">Specifies the SAS URLs of blobs whose content this cmdlet imports into the cache.</span></span> <span data-ttu-id="3e82d-115">A SAS URL-címét a következő PowerShell-parancsokkal hozhatja létre: $storageAccountContext = New-AzStorageContext-StorageAccountName "storageName"-StorageAccountKey "kulcs" $sasKeyForBlob = New-AzStorageBlobSASToken-Container "containerName"-blob "blobName"-"rwdl" – kezdő dátum ([System. DateTime]:: most). AddMinutes (-15)-ExpiryTime ([System. DateTime]:: most). AddHours (5)-Context $storageAccountContext-FullUri Import-AzRedisCache-ResourceGroupName "ResourceGroupName"-Name "cacheName"-Files ($sasKeyForBlob)-Force</span><span class="sxs-lookup"><span data-stu-id="3e82d-115">You can generate the SAS URLs using the following PowerShell commands: $storageAccountContext = New-AzStorageContext -StorageAccountName "storageName" -StorageAccountKey "key" $sasKeyForBlob = New-AzStorageBlobSASToken -Container "containerName" -blob "blobName" -Permission "rwdl" -StartTime ([System.DateTime]::Now).AddMinutes(-15) -ExpiryTime ([System.DateTime]::Now).AddHours(5) -Context $storageAccountContext -FullUri Import-AzRedisCache -ResourceGroupName "ResourceGroupName" -Name "cacheName" -Files ($sasKeyForBlob) -Force</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e82d-116">-Force</span><span class="sxs-lookup"><span data-stu-id="3e82d-116">-Force</span></span>
<span data-ttu-id="3e82d-117">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="3e82d-117">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e82d-118">Formátumú</span><span class="sxs-lookup"><span data-stu-id="3e82d-118">-Format</span></span>
<span data-ttu-id="3e82d-119">A blob formátumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="3e82d-119">Specifies the format of the blob.</span></span>
<span data-ttu-id="3e82d-120">Jelenleg a RDB az egyetlen támogatott formátum.</span><span class="sxs-lookup"><span data-stu-id="3e82d-120">Currently rdb is the only supported format.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e82d-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3e82d-121">-Name</span></span>
<span data-ttu-id="3e82d-122">A gyorsítótár nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3e82d-122">Specifies the name of a cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e82d-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3e82d-123">-PassThru</span></span>
<span data-ttu-id="3e82d-124">Jelzi, hogy ez a parancsmag olyan logikai értéket ad eredményül, amely azt jelzi, hogy a művelet sikerül-e.</span><span class="sxs-lookup"><span data-stu-id="3e82d-124">Indicates that this cmdlet returns a Boolean that indicates whether the operation succeeds.</span></span>
<span data-ttu-id="3e82d-125">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="3e82d-125">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e82d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e82d-126">-ResourceGroupName</span></span>
<span data-ttu-id="3e82d-127">A gyorsítótárat tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3e82d-127">Specifies the name of the resource group that contains the cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e82d-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3e82d-128">-Confirm</span></span>
<span data-ttu-id="3e82d-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3e82d-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e82d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e82d-130">-WhatIf</span></span>
<span data-ttu-id="3e82d-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3e82d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e82d-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3e82d-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e82d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e82d-133">CommonParameters</span></span>
<span data-ttu-id="3e82d-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3e82d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e82d-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e82d-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e82d-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3e82d-136">INPUTS</span></span>

### <span data-ttu-id="3e82d-137">System. String</span><span class="sxs-lookup"><span data-stu-id="3e82d-137">System.String</span></span>

### <span data-ttu-id="3e82d-138">System. string []</span><span class="sxs-lookup"><span data-stu-id="3e82d-138">System.String[]</span></span>

## <span data-ttu-id="3e82d-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3e82d-139">OUTPUTS</span></span>

### <span data-ttu-id="3e82d-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3e82d-140">System.Boolean</span></span>

## <span data-ttu-id="3e82d-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3e82d-141">NOTES</span></span>
* <span data-ttu-id="3e82d-142">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Redis, gyorsítótár, web, WebApp, webhely</span><span class="sxs-lookup"><span data-stu-id="3e82d-142">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="3e82d-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3e82d-143">RELATED LINKS</span></span>

[<span data-ttu-id="3e82d-144">Exportálás – AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="3e82d-144">Export-AzRedisCache</span></span>](./Export-AzRedisCache.md)

[<span data-ttu-id="3e82d-145">Új – AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="3e82d-145">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="3e82d-146">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="3e82d-146">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="3e82d-147">Reset-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="3e82d-147">Reset-AzRedisCache</span></span>](./Reset-AzRedisCache.md)

[<span data-ttu-id="3e82d-148">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="3e82d-148">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)


