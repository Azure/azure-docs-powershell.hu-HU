---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: B447E492-D87E-4DA3-A8B0-0BAF603CCC26
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Export-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Export-AzureRmRedisCache.md
ms.openlocfilehash: 0edfec1d98423f444b2291d43e6f2a3489e20b29
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501652"
---
# <span data-ttu-id="f02e2-101">Export-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="f02e2-101">Export-AzureRmRedisCache</span></span>

## <span data-ttu-id="f02e2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f02e2-102">SYNOPSIS</span></span>
<span data-ttu-id="f02e2-103">Az Azure Redis-gyorsítótárból származó adatot egy tárolóba exportálja.</span><span class="sxs-lookup"><span data-stu-id="f02e2-103">Exports data from Azure Redis Cache to a container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f02e2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f02e2-104">SYNTAX</span></span>

```
Export-AzureRmRedisCache -ResourceGroupName <String> -Name <String> -Prefix <String> -Container <String>
 [-Format <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f02e2-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f02e2-105">DESCRIPTION</span></span>
<span data-ttu-id="f02e2-106">Az **export-AzureRmRedisCache** parancsmag az Azure Redis-gyorsítótárából származó adatot exportálja tárolóba.</span><span class="sxs-lookup"><span data-stu-id="f02e2-106">The **Export-AzureRmRedisCache** cmdlet exports data from Azure Redis Cache to a container.</span></span>

## <span data-ttu-id="f02e2-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f02e2-107">EXAMPLES</span></span>

### <span data-ttu-id="f02e2-108">1. példa: az adatexportálás</span><span class="sxs-lookup"><span data-stu-id="f02e2-108">Example 1: Export data</span></span>
```
PS C:\>Export-AzureRmRedisCache -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -Prefix "blobprefix" -Container "https://mystorageaccount.blob.core.windows.net/container18?sv=2015-04-05&sr=c&sig=HezZtBZ3DURmEGDduauE7pvETY4kqlPI8JCNa8ATmaw%3D&st=2016-05-27T00%3A00%3A00Z&se=2016-05-28T00%3A00%3A00Z&sp=rwdl"
```

<span data-ttu-id="f02e2-109">Ez a parancs az Azure Redis-gyorsítótárból származó adatot exportálja a SAS URL-címe által megadott tárolóba.</span><span class="sxs-lookup"><span data-stu-id="f02e2-109">This command exports data from an Azure Redis Cache instance into the container that is specified by the SAS URL.</span></span>

## <span data-ttu-id="f02e2-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f02e2-110">PARAMETERS</span></span>

### <span data-ttu-id="f02e2-111">-Container</span><span class="sxs-lookup"><span data-stu-id="f02e2-111">-Container</span></span>
<span data-ttu-id="f02e2-112">Annak a tárolónak a szolgáltatás-URL-címét adja meg, ahol a parancsmag az adatot exportálja.</span><span class="sxs-lookup"><span data-stu-id="f02e2-112">Specifies the Service SAS URL of container where this cmdlet exports data.</span></span> <span data-ttu-id="f02e2-113">A következő PowerShell-parancsok segítségével létrehozhatja a szolgáltatás SAS URL-címét:</span><span class="sxs-lookup"><span data-stu-id="f02e2-113">You can generate a Service SAS URL using the following PowerShell commands:</span></span>

<span data-ttu-id="f02e2-114">$storageAccountContext = New-AzureStorageContext-StorageAccountName "storageName"-StorageAccountKey "kulcs"</span><span class="sxs-lookup"><span data-stu-id="f02e2-114">$storageAccountContext = New-AzureStorageContext -StorageAccountName "storageName" -StorageAccountKey "key"</span></span>

<span data-ttu-id="f02e2-115">$sasKeyForContainer = New-AzureStorageContainerSASToken név "ContainerName" – Permission "rwdl" – kezdő időpont ([System. DateTime]:: most). AddMinutes (-15)-ExpiryTime ([System. DateTime]:: most). AddHours (5) – környezet $storageAccountContext-FullUri</span><span class="sxs-lookup"><span data-stu-id="f02e2-115">$sasKeyForContainer = New-AzureStorageContainerSASToken -Name "containername" -Permission "rwdl" -StartTime ([System.DateTime]::Now).AddMinutes(-15) -ExpiryTime ([System.DateTime]::Now).AddHours(5) -Context $storageAccountContext -FullUri</span></span> 

<span data-ttu-id="f02e2-116">Export-AzureRmRedisCache-ResourceGroupName "ResourceGroupName"-Name "cacheName"-prefix "blobprefix"-Container ($sasKeyForContainer)</span><span class="sxs-lookup"><span data-stu-id="f02e2-116">Export-AzureRmRedisCache -ResourceGroupName "ResourceGroupName" -Name "cacheName" -Prefix "blobprefix" -Container ($sasKeyForContainer)</span></span>

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

### <span data-ttu-id="f02e2-117">Formátumú</span><span class="sxs-lookup"><span data-stu-id="f02e2-117">-Format</span></span>
<span data-ttu-id="f02e2-118">A blob formátumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="f02e2-118">Specifies a format for the blob.</span></span>
<span data-ttu-id="f02e2-119">Jelenleg a RDB az egyetlen támogatott formátum.</span><span class="sxs-lookup"><span data-stu-id="f02e2-119">Currently rdb is the only supported format.</span></span>

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

### <span data-ttu-id="f02e2-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f02e2-120">-Name</span></span>
<span data-ttu-id="f02e2-121">A gyorsítótár nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f02e2-121">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="f02e2-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f02e2-122">-PassThru</span></span>
<span data-ttu-id="f02e2-123">Jelzi, hogy ez a parancsmag olyan logikai értéket ad eredményül, amely azt jelzi, hogy a művelet sikerül-e.</span><span class="sxs-lookup"><span data-stu-id="f02e2-123">Indicates that this cmdlet returns a Boolean that indicates whether the operation succeeds.</span></span>
<span data-ttu-id="f02e2-124">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="f02e2-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f02e2-125">-Prefix</span><span class="sxs-lookup"><span data-stu-id="f02e2-125">-Prefix</span></span>
<span data-ttu-id="f02e2-126">A blob-nevekhez használni kívánt előtagot adja meg.</span><span class="sxs-lookup"><span data-stu-id="f02e2-126">Specifies a prefix to use for blob names.</span></span>

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

### <span data-ttu-id="f02e2-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f02e2-127">-ResourceGroupName</span></span>
<span data-ttu-id="f02e2-128">A gyorsítótárat tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f02e2-128">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="f02e2-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f02e2-129">-DefaultProfile</span></span>
<span data-ttu-id="f02e2-130">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f02e2-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f02e2-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f02e2-131">CommonParameters</span></span>
<span data-ttu-id="f02e2-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f02e2-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f02e2-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f02e2-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f02e2-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f02e2-134">INPUTS</span></span>

### <span data-ttu-id="f02e2-135">Nincs</span><span class="sxs-lookup"><span data-stu-id="f02e2-135">None</span></span>
<span data-ttu-id="f02e2-136">A parancsmagot tulajdonság nevében, de nem érték szerint is beírhatja.</span><span class="sxs-lookup"><span data-stu-id="f02e2-136">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="f02e2-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f02e2-137">OUTPUTS</span></span>

### <span data-ttu-id="f02e2-138">Nincs</span><span class="sxs-lookup"><span data-stu-id="f02e2-138">None</span></span>

## <span data-ttu-id="f02e2-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f02e2-139">NOTES</span></span>
* <span data-ttu-id="f02e2-140">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Redis, gyorsítótár, web, WebApp, webhely</span><span class="sxs-lookup"><span data-stu-id="f02e2-140">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="f02e2-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f02e2-141">RELATED LINKS</span></span>

[<span data-ttu-id="f02e2-142">Importálás – AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="f02e2-142">Import-AzureRmRedisCache</span></span>](./Import-AzureRmRedisCache.md)

[<span data-ttu-id="f02e2-143">Új – AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="f02e2-143">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="f02e2-144">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="f02e2-144">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="f02e2-145">Reset-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="f02e2-145">Reset-AzureRmRedisCache</span></span>](./Reset-AzureRmRedisCache.md)

[<span data-ttu-id="f02e2-146">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="f02e2-146">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)


