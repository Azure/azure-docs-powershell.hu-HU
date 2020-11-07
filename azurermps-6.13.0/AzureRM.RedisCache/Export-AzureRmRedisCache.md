---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: B447E492-D87E-4DA3-A8B0-0BAF603CCC26
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/export-azurermrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Export-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Export-AzureRmRedisCache.md
ms.openlocfilehash: ceba71f729de627e0e7231b9c295d0cad1ccc105
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679152"
---
# <span data-ttu-id="6c0f9-101">Export-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="6c0f9-101">Export-AzureRmRedisCache</span></span>

## <span data-ttu-id="6c0f9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6c0f9-102">SYNOPSIS</span></span>
<span data-ttu-id="6c0f9-103">Az Azure Redis-gyorsítótárból származó adatot egy tárolóba exportálja.</span><span class="sxs-lookup"><span data-stu-id="6c0f9-103">Exports data from Azure Redis Cache to a container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6c0f9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6c0f9-104">SYNTAX</span></span>

```
Export-AzureRmRedisCache [-ResourceGroupName <String>] -Name <String> -Prefix <String> -Container <String>
 [-Format <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6c0f9-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6c0f9-105">DESCRIPTION</span></span>
<span data-ttu-id="6c0f9-106">Az **export-AzureRmRedisCache** parancsmag az Azure Redis-gyorsítótárából származó adatot exportálja tárolóba.</span><span class="sxs-lookup"><span data-stu-id="6c0f9-106">The **Export-AzureRmRedisCache** cmdlet exports data from Azure Redis Cache to a container.</span></span>

## <span data-ttu-id="6c0f9-107">Példák</span><span class="sxs-lookup"><span data-stu-id="6c0f9-107">EXAMPLES</span></span>

### <span data-ttu-id="6c0f9-108">1. példa: az adatexportálás</span><span class="sxs-lookup"><span data-stu-id="6c0f9-108">Example 1: Export data</span></span>
```
PS C:\>Export-AzureRmRedisCache -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -Prefix "blobprefix" -Container "https://mystorageaccount.blob.core.windows.net/container18?sv=2015-04-05&sr=c&sig=HezZtBZ3DURmEGDduauE7pvETY4kqlPI8JCNa8ATmaw%3D&st=2016-05-27T00%3A00%3A00Z&se=2016-05-28T00%3A00%3A00Z&sp=rwdl"
```

<span data-ttu-id="6c0f9-109">Ez a parancs az Azure Redis-gyorsítótárból származó adatot exportálja a SAS URL-címe által megadott tárolóba.</span><span class="sxs-lookup"><span data-stu-id="6c0f9-109">This command exports data from an Azure Redis Cache instance into the container that is specified by the SAS URL.</span></span>

## <span data-ttu-id="6c0f9-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6c0f9-110">PARAMETERS</span></span>

### <span data-ttu-id="6c0f9-111">-Container</span><span class="sxs-lookup"><span data-stu-id="6c0f9-111">-Container</span></span>
<span data-ttu-id="6c0f9-112">Annak a tárolónak a szolgáltatás-URL-címét adja meg, ahol a parancsmag az adatot exportálja.</span><span class="sxs-lookup"><span data-stu-id="6c0f9-112">Specifies the Service SAS URL of container where this cmdlet exports data.</span></span> <span data-ttu-id="6c0f9-113">A következő PowerShell-parancsokkal hozhat létre szolgáltatás-URL-címet: $storageAccountContext = New-AzureStorageContext-StorageAccountName "storageName"-StorageAccountKey "kulcs" $sasKeyForContainer = New-AzureStorageContainerSASToken-Name "ContainerName"-Permission "rwdl"-kezdési időpont ([System. DateTime]:: Now). AddMinutes (-15)-ExpiryTime ([System. DateTime]:: most). AddHours (5)-Context $storageAccountContext-FullUri Export-AzureRmRedisCache-ResourceGroupName "ResourceGroupName"-Name "cacheName"-prefix "blobprefix"-Container ($sasKeyForContainer)</span><span class="sxs-lookup"><span data-stu-id="6c0f9-113">You can generate a Service SAS URL using the following PowerShell commands: $storageAccountContext = New-AzureStorageContext -StorageAccountName "storageName" -StorageAccountKey "key" $sasKeyForContainer = New-AzureStorageContainerSASToken -Name "containername" -Permission "rwdl" -StartTime ([System.DateTime]::Now).AddMinutes(-15) -ExpiryTime ([System.DateTime]::Now).AddHours(5) -Context $storageAccountContext -FullUri Export-AzureRmRedisCache -ResourceGroupName "ResourceGroupName" -Name "cacheName" -Prefix "blobprefix" -Container ($sasKeyForContainer)</span></span>

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

### <span data-ttu-id="6c0f9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c0f9-114">-DefaultProfile</span></span>
<span data-ttu-id="6c0f9-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6c0f9-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c0f9-116">Formátumú</span><span class="sxs-lookup"><span data-stu-id="6c0f9-116">-Format</span></span>
<span data-ttu-id="6c0f9-117">A blob formátumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="6c0f9-117">Specifies a format for the blob.</span></span>
<span data-ttu-id="6c0f9-118">Jelenleg a RDB az egyetlen támogatott formátum.</span><span class="sxs-lookup"><span data-stu-id="6c0f9-118">Currently rdb is the only supported format.</span></span>

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

### <span data-ttu-id="6c0f9-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6c0f9-119">-Name</span></span>
<span data-ttu-id="6c0f9-120">A gyorsítótár nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6c0f9-120">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="6c0f9-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6c0f9-121">-PassThru</span></span>
<span data-ttu-id="6c0f9-122">Jelzi, hogy ez a parancsmag olyan logikai értéket ad eredményül, amely azt jelzi, hogy a művelet sikerül-e.</span><span class="sxs-lookup"><span data-stu-id="6c0f9-122">Indicates that this cmdlet returns a Boolean that indicates whether the operation succeeds.</span></span>
<span data-ttu-id="6c0f9-123">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="6c0f9-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="6c0f9-124">-Prefix</span><span class="sxs-lookup"><span data-stu-id="6c0f9-124">-Prefix</span></span>
<span data-ttu-id="6c0f9-125">A blob-nevekhez használni kívánt előtagot adja meg.</span><span class="sxs-lookup"><span data-stu-id="6c0f9-125">Specifies a prefix to use for blob names.</span></span>

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

### <span data-ttu-id="6c0f9-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c0f9-126">-ResourceGroupName</span></span>
<span data-ttu-id="6c0f9-127">A gyorsítótárat tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6c0f9-127">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="6c0f9-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6c0f9-128">-Confirm</span></span>
<span data-ttu-id="6c0f9-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6c0f9-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c0f9-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c0f9-130">-WhatIf</span></span>
<span data-ttu-id="6c0f9-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6c0f9-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6c0f9-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6c0f9-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c0f9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c0f9-133">CommonParameters</span></span>
<span data-ttu-id="6c0f9-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6c0f9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c0f9-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c0f9-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c0f9-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6c0f9-136">INPUTS</span></span>

### <span data-ttu-id="6c0f9-137">System. String</span><span class="sxs-lookup"><span data-stu-id="6c0f9-137">System.String</span></span>

## <span data-ttu-id="6c0f9-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6c0f9-138">OUTPUTS</span></span>

### <span data-ttu-id="6c0f9-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6c0f9-139">System.Boolean</span></span>

## <span data-ttu-id="6c0f9-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6c0f9-140">NOTES</span></span>
* <span data-ttu-id="6c0f9-141">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Redis, gyorsítótár, web, WebApp, webhely</span><span class="sxs-lookup"><span data-stu-id="6c0f9-141">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="6c0f9-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6c0f9-142">RELATED LINKS</span></span>

[<span data-ttu-id="6c0f9-143">Importálás – AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="6c0f9-143">Import-AzureRmRedisCache</span></span>](./Import-AzureRmRedisCache.md)

[<span data-ttu-id="6c0f9-144">Új – AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="6c0f9-144">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="6c0f9-145">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="6c0f9-145">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="6c0f9-146">Reset-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="6c0f9-146">Reset-AzureRmRedisCache</span></span>](./Reset-AzureRmRedisCache.md)

[<span data-ttu-id="6c0f9-147">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="6c0f9-147">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)


