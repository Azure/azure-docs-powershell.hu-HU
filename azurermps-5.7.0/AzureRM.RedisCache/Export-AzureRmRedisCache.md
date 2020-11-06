---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: B447E492-D87E-4DA3-A8B0-0BAF603CCC26
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/export-azurermrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Export-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Export-AzureRmRedisCache.md
ms.openlocfilehash: cd19fe8052ae95f547971452f4364f279f365cac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494397"
---
# <span data-ttu-id="eb166-101">Export-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="eb166-101">Export-AzureRmRedisCache</span></span>

## <span data-ttu-id="eb166-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="eb166-102">SYNOPSIS</span></span>
<span data-ttu-id="eb166-103">Az Azure Redis-gyorsítótárból származó adatot egy tárolóba exportálja.</span><span class="sxs-lookup"><span data-stu-id="eb166-103">Exports data from Azure Redis Cache to a container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eb166-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="eb166-104">SYNTAX</span></span>

```
Export-AzureRmRedisCache [-ResourceGroupName <String>] -Name <String> -Prefix <String> -Container <String>
 [-Format <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="eb166-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="eb166-105">DESCRIPTION</span></span>
<span data-ttu-id="eb166-106">Az **export-AzureRmRedisCache** parancsmag az Azure Redis-gyorsítótárából származó adatot exportálja tárolóba.</span><span class="sxs-lookup"><span data-stu-id="eb166-106">The **Export-AzureRmRedisCache** cmdlet exports data from Azure Redis Cache to a container.</span></span>

## <span data-ttu-id="eb166-107">Példák</span><span class="sxs-lookup"><span data-stu-id="eb166-107">EXAMPLES</span></span>

### <span data-ttu-id="eb166-108">1. példa: az adatexportálás</span><span class="sxs-lookup"><span data-stu-id="eb166-108">Example 1: Export data</span></span>
```
PS C:\>Export-AzureRmRedisCache -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -Prefix "blobprefix" -Container "https://mystorageaccount.blob.core.windows.net/container18?sv=2015-04-05&sr=c&sig=HezZtBZ3DURmEGDduauE7pvETY4kqlPI8JCNa8ATmaw%3D&st=2016-05-27T00%3A00%3A00Z&se=2016-05-28T00%3A00%3A00Z&sp=rwdl"
```

<span data-ttu-id="eb166-109">Ez a parancs az Azure Redis-gyorsítótárból származó adatot exportálja a SAS URL-címe által megadott tárolóba.</span><span class="sxs-lookup"><span data-stu-id="eb166-109">This command exports data from an Azure Redis Cache instance into the container that is specified by the SAS URL.</span></span>

## <span data-ttu-id="eb166-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="eb166-110">PARAMETERS</span></span>

### <span data-ttu-id="eb166-111">-Container</span><span class="sxs-lookup"><span data-stu-id="eb166-111">-Container</span></span>
<span data-ttu-id="eb166-112">Annak a tárolónak a szolgáltatás-URL-címét adja meg, ahol a parancsmag az adatot exportálja.</span><span class="sxs-lookup"><span data-stu-id="eb166-112">Specifies the Service SAS URL of container where this cmdlet exports data.</span></span> <span data-ttu-id="eb166-113">A következő PowerShell-parancsok segítségével létrehozhatja a szolgáltatás SAS URL-címét:</span><span class="sxs-lookup"><span data-stu-id="eb166-113">You can generate a Service SAS URL using the following PowerShell commands:</span></span>

<span data-ttu-id="eb166-114">$storageAccountContext = New-AzureStorageContext-StorageAccountName "storageName"-StorageAccountKey "kulcs"</span><span class="sxs-lookup"><span data-stu-id="eb166-114">$storageAccountContext = New-AzureStorageContext -StorageAccountName "storageName" -StorageAccountKey "key"</span></span>

<span data-ttu-id="eb166-115">$sasKeyForContainer = New-AzureStorageContainerSASToken név "ContainerName" – Permission "rwdl" – kezdő időpont ([System. DateTime]:: most). AddMinutes (-15)-ExpiryTime ([System. DateTime]:: most). AddHours (5) – környezet $storageAccountContext-FullUri</span><span class="sxs-lookup"><span data-stu-id="eb166-115">$sasKeyForContainer = New-AzureStorageContainerSASToken -Name "containername" -Permission "rwdl" -StartTime ([System.DateTime]::Now).AddMinutes(-15) -ExpiryTime ([System.DateTime]::Now).AddHours(5) -Context $storageAccountContext -FullUri</span></span> 

<span data-ttu-id="eb166-116">Export-AzureRmRedisCache-ResourceGroupName "ResourceGroupName"-Name "cacheName"-prefix "blobprefix"-Container ($sasKeyForContainer)</span><span class="sxs-lookup"><span data-stu-id="eb166-116">Export-AzureRmRedisCache -ResourceGroupName "ResourceGroupName" -Name "cacheName" -Prefix "blobprefix" -Container ($sasKeyForContainer)</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb166-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb166-117">-DefaultProfile</span></span>
<span data-ttu-id="eb166-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="eb166-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb166-119">Formátumú</span><span class="sxs-lookup"><span data-stu-id="eb166-119">-Format</span></span>
<span data-ttu-id="eb166-120">A blob formátumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="eb166-120">Specifies a format for the blob.</span></span>
<span data-ttu-id="eb166-121">Jelenleg a RDB az egyetlen támogatott formátum.</span><span class="sxs-lookup"><span data-stu-id="eb166-121">Currently rdb is the only supported format.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb166-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="eb166-122">-Name</span></span>
<span data-ttu-id="eb166-123">A gyorsítótár nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="eb166-123">Specifies the name of a cache.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb166-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="eb166-124">-PassThru</span></span>
<span data-ttu-id="eb166-125">Jelzi, hogy ez a parancsmag olyan logikai értéket ad eredményül, amely azt jelzi, hogy a művelet sikerül-e.</span><span class="sxs-lookup"><span data-stu-id="eb166-125">Indicates that this cmdlet returns a Boolean that indicates whether the operation succeeds.</span></span>
<span data-ttu-id="eb166-126">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="eb166-126">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb166-127">-Prefix</span><span class="sxs-lookup"><span data-stu-id="eb166-127">-Prefix</span></span>
<span data-ttu-id="eb166-128">A blob-nevekhez használni kívánt előtagot adja meg.</span><span class="sxs-lookup"><span data-stu-id="eb166-128">Specifies a prefix to use for blob names.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb166-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb166-129">-ResourceGroupName</span></span>
<span data-ttu-id="eb166-130">A gyorsítótárat tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="eb166-130">Specifies the name of the resource group that contains the cache.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb166-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="eb166-131">-Confirm</span></span>
<span data-ttu-id="eb166-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="eb166-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb166-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb166-133">-WhatIf</span></span>
<span data-ttu-id="eb166-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="eb166-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="eb166-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="eb166-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb166-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb166-136">CommonParameters</span></span>
<span data-ttu-id="eb166-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="eb166-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb166-138">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb166-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb166-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="eb166-139">INPUTS</span></span>

### <span data-ttu-id="eb166-140">Nincs</span><span class="sxs-lookup"><span data-stu-id="eb166-140">None</span></span>
<span data-ttu-id="eb166-141">A parancsmagot tulajdonság nevében, de nem érték szerint is beírhatja.</span><span class="sxs-lookup"><span data-stu-id="eb166-141">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="eb166-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="eb166-142">OUTPUTS</span></span>

### <span data-ttu-id="eb166-143">Nincs</span><span class="sxs-lookup"><span data-stu-id="eb166-143">None</span></span>

## <span data-ttu-id="eb166-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="eb166-144">NOTES</span></span>
* <span data-ttu-id="eb166-145">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Redis, gyorsítótár, web, WebApp, webhely</span><span class="sxs-lookup"><span data-stu-id="eb166-145">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="eb166-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="eb166-146">RELATED LINKS</span></span>

[<span data-ttu-id="eb166-147">Importálás – AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="eb166-147">Import-AzureRmRedisCache</span></span>](./Import-AzureRmRedisCache.md)

[<span data-ttu-id="eb166-148">Új – AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="eb166-148">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="eb166-149">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="eb166-149">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="eb166-150">Reset-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="eb166-150">Reset-AzureRmRedisCache</span></span>](./Reset-AzureRmRedisCache.md)

[<span data-ttu-id="eb166-151">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="eb166-151">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)


