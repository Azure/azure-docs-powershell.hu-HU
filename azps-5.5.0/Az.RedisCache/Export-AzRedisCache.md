---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: B447E492-D87E-4DA3-A8B0-0BAF603CCC26
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/export-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Export-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Export-AzRedisCache.md
ms.openlocfilehash: fb44ca997fd3b7599c25c5ba986ed0ca0771b3e6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100153794"
---
# <span data-ttu-id="a0e28-101">Export-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="a0e28-101">Export-AzRedisCache</span></span>

## <span data-ttu-id="a0e28-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a0e28-102">SYNOPSIS</span></span>
<span data-ttu-id="a0e28-103">Adatokat exportál az Azure Redis Cache-ból egy tárolóba.</span><span class="sxs-lookup"><span data-stu-id="a0e28-103">Exports data from Azure Redis Cache to a container.</span></span>

## <span data-ttu-id="a0e28-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a0e28-104">SYNTAX</span></span>

```
Export-AzRedisCache [-ResourceGroupName <String>] -Name <String> -Prefix <String> -Container <String>
 [-Format <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a0e28-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a0e28-105">DESCRIPTION</span></span>
<span data-ttu-id="a0e28-106">Az **Export-AzRedisCache** parancsmag adatokat exportál az Azure Redis-gyorsítótárból egy tárolóba.</span><span class="sxs-lookup"><span data-stu-id="a0e28-106">The **Export-AzRedisCache** cmdlet exports data from Azure Redis Cache to a container.</span></span>

## <span data-ttu-id="a0e28-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a0e28-107">EXAMPLES</span></span>

### <span data-ttu-id="a0e28-108">1. példa: Adatok exportálása</span><span class="sxs-lookup"><span data-stu-id="a0e28-108">Example 1: Export data</span></span>
```
PS C:\>Export-AzRedisCache -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -Prefix "blobprefix" -Container "https://mystorageaccount.blob.core.windows.net/container18?sv=2015-04-05&sr=c&sig=HezZtBZ3DURmEGDduauE7pvETY4kqlPI8JCNa8ATmaw%3D&st=2016-05-27T00%3A00%3A00Z&se=2016-05-28T00%3A00%3A00Z&sp=rwdl"
```

<span data-ttu-id="a0e28-109">Ez a parancs adatokat exportál egy Azure Redis Cache-példányból az SAS URL-cím által megadott tárolóba.</span><span class="sxs-lookup"><span data-stu-id="a0e28-109">This command exports data from an Azure Redis Cache instance into the container that is specified by the SAS URL.</span></span>

## <span data-ttu-id="a0e28-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a0e28-110">PARAMETERS</span></span>

### <span data-ttu-id="a0e28-111">-Container</span><span class="sxs-lookup"><span data-stu-id="a0e28-111">-Container</span></span>
<span data-ttu-id="a0e28-112">Annak a tárolónak a Service SAS URL-címét adja meg, amelyből a parancsmag adatokat exportál.</span><span class="sxs-lookup"><span data-stu-id="a0e28-112">Specifies the Service SAS URL of container where this cmdlet exports data.</span></span> <span data-ttu-id="a0e28-113">A Szolgáltatás SAS URL-címét a következő PowerShell-parancsokkal generálhatja: $storageAccountContext = New-AzStorageContext -StorageAccountName "storageName" -StorageAccountKey "key" $sasKeyForContainer = New-AzStorageContainerSASToken -Name "containername" -Permission "rwdl" -StartTime ([System.DateTime]:::Now). AddMinutes(-15) -ExpiryTime ([System.DateTime]:::Now). AddHours(5) -Context $storageAccountContext -FullUri Export-AzRedisCache -ResourceGroupName "ResourceGroupName" -Name "cacheName" -Prefix "blobprefix" -Container ($sasKeyForContainer)</span><span class="sxs-lookup"><span data-stu-id="a0e28-113">You can generate a Service SAS URL using the following PowerShell commands: $storageAccountContext = New-AzStorageContext -StorageAccountName "storageName" -StorageAccountKey "key" $sasKeyForContainer = New-AzStorageContainerSASToken -Name "containername" -Permission "rwdl" -StartTime ([System.DateTime]::Now).AddMinutes(-15) -ExpiryTime ([System.DateTime]::Now).AddHours(5) -Context $storageAccountContext -FullUri Export-AzRedisCache -ResourceGroupName "ResourceGroupName" -Name "cacheName" -Prefix "blobprefix" -Container ($sasKeyForContainer)</span></span>

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

### <span data-ttu-id="a0e28-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0e28-114">-DefaultProfile</span></span>
<span data-ttu-id="a0e28-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a0e28-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a0e28-116">-Format</span><span class="sxs-lookup"><span data-stu-id="a0e28-116">-Format</span></span>
<span data-ttu-id="a0e28-117">A blob formátumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="a0e28-117">Specifies a format for the blob.</span></span>
<span data-ttu-id="a0e28-118">Jelenleg az rdb az egyetlen támogatott formátum.</span><span class="sxs-lookup"><span data-stu-id="a0e28-118">Currently rdb is the only supported format.</span></span>

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

### <span data-ttu-id="a0e28-119">-Name</span><span class="sxs-lookup"><span data-stu-id="a0e28-119">-Name</span></span>
<span data-ttu-id="a0e28-120">A gyorsítótár nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a0e28-120">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="a0e28-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a0e28-121">-PassThru</span></span>
<span data-ttu-id="a0e28-122">Azt jelzi, hogy ez a parancsmag egy logikai értéket ad vissza, amely jelzi, hogy a művelet sikeres-e.</span><span class="sxs-lookup"><span data-stu-id="a0e28-122">Indicates that this cmdlet returns a Boolean that indicates whether the operation succeeds.</span></span>
<span data-ttu-id="a0e28-123">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="a0e28-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a0e28-124">-Előtag</span><span class="sxs-lookup"><span data-stu-id="a0e28-124">-Prefix</span></span>
<span data-ttu-id="a0e28-125">A blobnevekhez használt előtagot adja meg.</span><span class="sxs-lookup"><span data-stu-id="a0e28-125">Specifies a prefix to use for blob names.</span></span>

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

### <span data-ttu-id="a0e28-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0e28-126">-ResourceGroupName</span></span>
<span data-ttu-id="a0e28-127">A gyorsítótárat tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a0e28-127">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="a0e28-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a0e28-128">-Confirm</span></span>
<span data-ttu-id="a0e28-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="a0e28-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0e28-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0e28-130">-WhatIf</span></span>
<span data-ttu-id="a0e28-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="a0e28-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a0e28-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a0e28-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0e28-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0e28-133">CommonParameters</span></span>
<span data-ttu-id="a0e28-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0e28-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0e28-135">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0e28-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0e28-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a0e28-136">INPUTS</span></span>

### <span data-ttu-id="a0e28-137">System.String</span><span class="sxs-lookup"><span data-stu-id="a0e28-137">System.String</span></span>

## <span data-ttu-id="a0e28-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a0e28-138">OUTPUTS</span></span>

### <span data-ttu-id="a0e28-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a0e28-139">System.Boolean</span></span>

## <span data-ttu-id="a0e28-140">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a0e28-140">NOTES</span></span>
* <span data-ttu-id="a0e28-141">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, redis, cache, web, webapp, webhely</span><span class="sxs-lookup"><span data-stu-id="a0e28-141">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="a0e28-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a0e28-142">RELATED LINKS</span></span>

[<span data-ttu-id="a0e28-143">Import-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="a0e28-143">Import-AzRedisCache</span></span>](./Import-AzRedisCache.md)

[<span data-ttu-id="a0e28-144">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="a0e28-144">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="a0e28-145">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="a0e28-145">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="a0e28-146">Reset-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="a0e28-146">Reset-AzRedisCache</span></span>](./Reset-AzRedisCache.md)

[<span data-ttu-id="a0e28-147">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="a0e28-147">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)


