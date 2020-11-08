---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: B447E492-D87E-4DA3-A8B0-0BAF603CCC26
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/export-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Export-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Export-AzRedisCache.md
ms.openlocfilehash: fb44ca997fd3b7599c25c5ba986ed0ca0771b3e6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194873"
---
# <span data-ttu-id="69be6-101">Export-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="69be6-101">Export-AzRedisCache</span></span>

## <span data-ttu-id="69be6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="69be6-102">SYNOPSIS</span></span>
<span data-ttu-id="69be6-103">Az Azure Redis-gyorsítótárból származó adatot egy tárolóba exportálja.</span><span class="sxs-lookup"><span data-stu-id="69be6-103">Exports data from Azure Redis Cache to a container.</span></span>

## <span data-ttu-id="69be6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="69be6-104">SYNTAX</span></span>

```
Export-AzRedisCache [-ResourceGroupName <String>] -Name <String> -Prefix <String> -Container <String>
 [-Format <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="69be6-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="69be6-105">DESCRIPTION</span></span>
<span data-ttu-id="69be6-106">Az **export-AzRedisCache** parancsmag az Azure Redis-gyorsítótárából származó adatot exportálja tárolóba.</span><span class="sxs-lookup"><span data-stu-id="69be6-106">The **Export-AzRedisCache** cmdlet exports data from Azure Redis Cache to a container.</span></span>

## <span data-ttu-id="69be6-107">Példák</span><span class="sxs-lookup"><span data-stu-id="69be6-107">EXAMPLES</span></span>

### <span data-ttu-id="69be6-108">1. példa: az adatexportálás</span><span class="sxs-lookup"><span data-stu-id="69be6-108">Example 1: Export data</span></span>
```
PS C:\>Export-AzRedisCache -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -Prefix "blobprefix" -Container "https://mystorageaccount.blob.core.windows.net/container18?sv=2015-04-05&sr=c&sig=HezZtBZ3DURmEGDduauE7pvETY4kqlPI8JCNa8ATmaw%3D&st=2016-05-27T00%3A00%3A00Z&se=2016-05-28T00%3A00%3A00Z&sp=rwdl"
```

<span data-ttu-id="69be6-109">Ez a parancs az Azure Redis-gyorsítótárból származó adatot exportálja a SAS URL-címe által megadott tárolóba.</span><span class="sxs-lookup"><span data-stu-id="69be6-109">This command exports data from an Azure Redis Cache instance into the container that is specified by the SAS URL.</span></span>

## <span data-ttu-id="69be6-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="69be6-110">PARAMETERS</span></span>

### <span data-ttu-id="69be6-111">-Container</span><span class="sxs-lookup"><span data-stu-id="69be6-111">-Container</span></span>
<span data-ttu-id="69be6-112">Annak a tárolónak a szolgáltatás-URL-címét adja meg, ahol a parancsmag az adatot exportálja.</span><span class="sxs-lookup"><span data-stu-id="69be6-112">Specifies the Service SAS URL of container where this cmdlet exports data.</span></span> <span data-ttu-id="69be6-113">A következő PowerShell-parancsokkal hozhat létre szolgáltatás-URL-címet: $storageAccountContext = New-AzStorageContext-StorageAccountName "storageName"-StorageAccountKey "kulcs" $sasKeyForContainer = New-AzStorageContainerSASToken-Name "ContainerName"-Permission "rwdl"-kezdési időpont ([System. DateTime]:: Now). AddMinutes (-15)-ExpiryTime ([System. DateTime]:: most). AddHours (5)-Context $storageAccountContext-FullUri Export-AzRedisCache-ResourceGroupName "ResourceGroupName"-Name "cacheName"-prefix "blobprefix"-Container ($sasKeyForContainer)</span><span class="sxs-lookup"><span data-stu-id="69be6-113">You can generate a Service SAS URL using the following PowerShell commands: $storageAccountContext = New-AzStorageContext -StorageAccountName "storageName" -StorageAccountKey "key" $sasKeyForContainer = New-AzStorageContainerSASToken -Name "containername" -Permission "rwdl" -StartTime ([System.DateTime]::Now).AddMinutes(-15) -ExpiryTime ([System.DateTime]::Now).AddHours(5) -Context $storageAccountContext -FullUri Export-AzRedisCache -ResourceGroupName "ResourceGroupName" -Name "cacheName" -Prefix "blobprefix" -Container ($sasKeyForContainer)</span></span>

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

### <span data-ttu-id="69be6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69be6-114">-DefaultProfile</span></span>
<span data-ttu-id="69be6-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="69be6-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="69be6-116">Formátumú</span><span class="sxs-lookup"><span data-stu-id="69be6-116">-Format</span></span>
<span data-ttu-id="69be6-117">A blob formátumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="69be6-117">Specifies a format for the blob.</span></span>
<span data-ttu-id="69be6-118">Jelenleg a RDB az egyetlen támogatott formátum.</span><span class="sxs-lookup"><span data-stu-id="69be6-118">Currently rdb is the only supported format.</span></span>

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

### <span data-ttu-id="69be6-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="69be6-119">-Name</span></span>
<span data-ttu-id="69be6-120">A gyorsítótár nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="69be6-120">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="69be6-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="69be6-121">-PassThru</span></span>
<span data-ttu-id="69be6-122">Jelzi, hogy ez a parancsmag olyan logikai értéket ad eredményül, amely azt jelzi, hogy a művelet sikerül-e.</span><span class="sxs-lookup"><span data-stu-id="69be6-122">Indicates that this cmdlet returns a Boolean that indicates whether the operation succeeds.</span></span>
<span data-ttu-id="69be6-123">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="69be6-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="69be6-124">-Prefix</span><span class="sxs-lookup"><span data-stu-id="69be6-124">-Prefix</span></span>
<span data-ttu-id="69be6-125">A blob-nevekhez használni kívánt előtagot adja meg.</span><span class="sxs-lookup"><span data-stu-id="69be6-125">Specifies a prefix to use for blob names.</span></span>

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

### <span data-ttu-id="69be6-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69be6-126">-ResourceGroupName</span></span>
<span data-ttu-id="69be6-127">A gyorsítótárat tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="69be6-127">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="69be6-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="69be6-128">-Confirm</span></span>
<span data-ttu-id="69be6-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="69be6-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69be6-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69be6-130">-WhatIf</span></span>
<span data-ttu-id="69be6-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="69be6-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="69be6-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="69be6-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69be6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69be6-133">CommonParameters</span></span>
<span data-ttu-id="69be6-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="69be6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69be6-135">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69be6-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69be6-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="69be6-136">INPUTS</span></span>

### <span data-ttu-id="69be6-137">System. String</span><span class="sxs-lookup"><span data-stu-id="69be6-137">System.String</span></span>

## <span data-ttu-id="69be6-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="69be6-138">OUTPUTS</span></span>

### <span data-ttu-id="69be6-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="69be6-139">System.Boolean</span></span>

## <span data-ttu-id="69be6-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="69be6-140">NOTES</span></span>
* <span data-ttu-id="69be6-141">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Redis, gyorsítótár, web, WebApp, webhely</span><span class="sxs-lookup"><span data-stu-id="69be6-141">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="69be6-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="69be6-142">RELATED LINKS</span></span>

[<span data-ttu-id="69be6-143">Importálás – AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="69be6-143">Import-AzRedisCache</span></span>](./Import-AzRedisCache.md)

[<span data-ttu-id="69be6-144">Új – AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="69be6-144">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="69be6-145">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="69be6-145">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="69be6-146">Reset-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="69be6-146">Reset-AzRedisCache</span></span>](./Reset-AzRedisCache.md)

[<span data-ttu-id="69be6-147">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="69be6-147">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)

