---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: BC00DEF9-6A93-4DF5-8E5B-C488551BA1D1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Import-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Import-AzureRmRedisCache.md
ms.openlocfilehash: 792a76d024b34dd90fd8818303c61daafeb4f46b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494725"
---
# <span data-ttu-id="97e99-101">Import-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="97e99-101">Import-AzureRmRedisCache</span></span>

## <span data-ttu-id="97e99-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="97e99-102">SYNOPSIS</span></span>
<span data-ttu-id="97e99-103">Az adatimportálást a Blobs-ról Azure Redis-gyorsítótárba importálja.</span><span class="sxs-lookup"><span data-stu-id="97e99-103">Imports data from blobs to Azure Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="97e99-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="97e99-104">SYNTAX</span></span>

```
Import-AzureRmRedisCache -ResourceGroupName <String> -Name <String> -Files <String[]> [-Format <String>]
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="97e99-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="97e99-105">DESCRIPTION</span></span>
<span data-ttu-id="97e99-106">Az **import-AzureRmRedisCache** parancsmag az adatait a Blobs-ról Azure Redis-gyorsítótárba importálja.</span><span class="sxs-lookup"><span data-stu-id="97e99-106">The **Import-AzureRmRedisCache** cmdlet imports data from blobs into Azure Redis Cache.</span></span>

## <span data-ttu-id="97e99-107">Példák</span><span class="sxs-lookup"><span data-stu-id="97e99-107">EXAMPLES</span></span>

### <span data-ttu-id="97e99-108">1. példa: az adatimportálás</span><span class="sxs-lookup"><span data-stu-id="97e99-108">Example 1: Import data</span></span>
```
PS C:\>Import-AzureRmRedisCache -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -Files @("https://mystorageaccount.blob.core.windows.net/container22/blobname?sv=2015-04-05&sr=b&sig=caIwutG2uDa0NZ8mjdNJdgOY8%2F8mhwRuGNdICU%2B0pI4%3D&st=2016-05-27T00%3A00%3A00Z&se=2016-05-28T00%3A00%3A00Z&sp=rwd") -Force
```

<span data-ttu-id="97e99-109">Ez a parancs a biztonsági társítás URL-címének az Azure Redis-gyorsítótárba történő importálására szolgáló blob-adatot importálja.</span><span class="sxs-lookup"><span data-stu-id="97e99-109">This command imports data from the blob that is specified by the SAS URL into Azure Redis Cache.</span></span>

## <span data-ttu-id="97e99-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="97e99-110">PARAMETERS</span></span>

### <span data-ttu-id="97e99-111">-Files</span><span class="sxs-lookup"><span data-stu-id="97e99-111">-Files</span></span>
<span data-ttu-id="97e99-112">Itt adhatja meg, hogy a program miként importálja a gyorsítótárba a parancsmagok által importált bináris fájlokat.</span><span class="sxs-lookup"><span data-stu-id="97e99-112">Specifies the SAS URLs of blobs whose content this cmdlet imports into the cache.</span></span> <span data-ttu-id="97e99-113">A SAS URL-címét a következő PowerShell-parancsok segítségével hozhatja létre:</span><span class="sxs-lookup"><span data-stu-id="97e99-113">You can generate the SAS URLs using the following PowerShell commands:</span></span>

<span data-ttu-id="97e99-114">$storageAccountContext = New-AzureStorageContext-StorageAccountName "storageName"-StorageAccountKey "kulcs"</span><span class="sxs-lookup"><span data-stu-id="97e99-114">$storageAccountContext = New-AzureStorageContext -StorageAccountName "storageName" -StorageAccountKey "key"</span></span>

<span data-ttu-id="97e99-115">$sasKeyForBlob = New-AzureStorageBlobSASToken-Container "containerName"-blob "blobName"-Permission "rwdl"-kezdési időpont ([System. DateTime]:: Now). AddMinutes (-15)-ExpiryTime ([System. DateTime]:: most). AddHours (5) – környezet $storageAccountContext-FullUri</span><span class="sxs-lookup"><span data-stu-id="97e99-115">$sasKeyForBlob = New-AzureStorageBlobSASToken -Container "containerName" -blob "blobName" -Permission "rwdl" -StartTime ([System.DateTime]::Now).AddMinutes(-15) -ExpiryTime ([System.DateTime]::Now).AddHours(5) -Context $storageAccountContext -FullUri</span></span>

<span data-ttu-id="97e99-116">Import-AzureRmRedisCache-ResourceGroupName "ResourceGroupName" név "cacheName"-Files ($sasKeyForBlob)-Force</span><span class="sxs-lookup"><span data-stu-id="97e99-116">Import-AzureRmRedisCache -ResourceGroupName "ResourceGroupName" -Name "cacheName" -Files ($sasKeyForBlob) -Force</span></span>

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

### <span data-ttu-id="97e99-117">-Force</span><span class="sxs-lookup"><span data-stu-id="97e99-117">-Force</span></span>
<span data-ttu-id="97e99-118">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="97e99-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="97e99-119">Formátumú</span><span class="sxs-lookup"><span data-stu-id="97e99-119">-Format</span></span>
<span data-ttu-id="97e99-120">A blob formátumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="97e99-120">Specifies the format of the blob.</span></span>
<span data-ttu-id="97e99-121">Jelenleg a RDB az egyetlen támogatott formátum.</span><span class="sxs-lookup"><span data-stu-id="97e99-121">Currently rdb is the only supported format.</span></span>

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

### <span data-ttu-id="97e99-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="97e99-122">-Name</span></span>
<span data-ttu-id="97e99-123">A gyorsítótár nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="97e99-123">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="97e99-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="97e99-124">-PassThru</span></span>
<span data-ttu-id="97e99-125">Jelzi, hogy ez a parancsmag olyan logikai értéket ad eredményül, amely azt jelzi, hogy a művelet sikerül-e.</span><span class="sxs-lookup"><span data-stu-id="97e99-125">Indicates that this cmdlet returns a Boolean that indicates whether the operation succeeds.</span></span>
<span data-ttu-id="97e99-126">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="97e99-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="97e99-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97e99-127">-ResourceGroupName</span></span>
<span data-ttu-id="97e99-128">A gyorsítótárat tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="97e99-128">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="97e99-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="97e99-129">-Confirm</span></span>
<span data-ttu-id="97e99-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="97e99-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97e99-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97e99-131">-WhatIf</span></span>
<span data-ttu-id="97e99-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="97e99-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="97e99-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="97e99-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97e99-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97e99-134">-DefaultProfile</span></span>
<span data-ttu-id="97e99-135">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="97e99-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="97e99-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97e99-136">CommonParameters</span></span>
<span data-ttu-id="97e99-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="97e99-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97e99-138">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97e99-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97e99-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="97e99-139">INPUTS</span></span>

### <span data-ttu-id="97e99-140">Nincs</span><span class="sxs-lookup"><span data-stu-id="97e99-140">None</span></span>
<span data-ttu-id="97e99-141">A parancsmagot tulajdonság nevében, de nem érték szerint is beírhatja.</span><span class="sxs-lookup"><span data-stu-id="97e99-141">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="97e99-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="97e99-142">OUTPUTS</span></span>

### <span data-ttu-id="97e99-143">Nincs</span><span class="sxs-lookup"><span data-stu-id="97e99-143">None</span></span>

## <span data-ttu-id="97e99-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="97e99-144">NOTES</span></span>
* <span data-ttu-id="97e99-145">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Redis, gyorsítótár, web, WebApp, webhely</span><span class="sxs-lookup"><span data-stu-id="97e99-145">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="97e99-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="97e99-146">RELATED LINKS</span></span>

[<span data-ttu-id="97e99-147">Exportálás – AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="97e99-147">Export-AzureRmRedisCache</span></span>](./Export-AzureRmRedisCache.md)

[<span data-ttu-id="97e99-148">Új – AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="97e99-148">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="97e99-149">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="97e99-149">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="97e99-150">Reset-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="97e99-150">Reset-AzureRmRedisCache</span></span>](./Reset-AzureRmRedisCache.md)

[<span data-ttu-id="97e99-151">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="97e99-151">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)


