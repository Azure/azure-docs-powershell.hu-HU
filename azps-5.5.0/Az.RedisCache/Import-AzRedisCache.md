---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: BC00DEF9-6A93-4DF5-8E5B-C488551BA1D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/import-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Import-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Import-AzRedisCache.md
ms.openlocfilehash: 1f51f156a0f45b014e9ff521adb959bdbd86bef7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100151042"
---
# <span data-ttu-id="9977b-101">Import-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="9977b-101">Import-AzRedisCache</span></span>

## <span data-ttu-id="9977b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9977b-102">SYNOPSIS</span></span>
<span data-ttu-id="9977b-103">Blobok adatait importálja az Azure Redis-gyorsítótárba.</span><span class="sxs-lookup"><span data-stu-id="9977b-103">Imports data from blobs to Azure Redis Cache.</span></span>

## <span data-ttu-id="9977b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9977b-104">SYNTAX</span></span>

```
Import-AzRedisCache [-ResourceGroupName <String>] -Name <String> -Files <String[]> [-Format <String>] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9977b-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9977b-105">DESCRIPTION</span></span>
<span data-ttu-id="9977b-106">Az **Import-AzRedisCache** parancsmag adatokat importál blobból az Azure Redis-gyorsítótárba.</span><span class="sxs-lookup"><span data-stu-id="9977b-106">The **Import-AzRedisCache** cmdlet imports data from blobs into Azure Redis Cache.</span></span>

## <span data-ttu-id="9977b-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9977b-107">EXAMPLES</span></span>

### <span data-ttu-id="9977b-108">1. példa: Adatok importálása</span><span class="sxs-lookup"><span data-stu-id="9977b-108">Example 1: Import data</span></span>
```
PS C:\>Import-AzRedisCache -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -Files @("https://mystorageaccount.blob.core.windows.net/container22/blobname?sv=2015-04-05&sr=b&sig=caIwutG2uDa0NZ8mjdNJdgOY8%2F8mhwRuGNdICU%2B0pI4%3D&st=2016-05-27T00%3A00%3A00Z&se=2016-05-28T00%3A00%3A00Z&sp=rwd") -Force
```

<span data-ttu-id="9977b-109">Ez a parancs az SAS URL-cím által megadott blob adatait importálja az Azure Redis-gyorsítótárba.</span><span class="sxs-lookup"><span data-stu-id="9977b-109">This command imports data from the blob that is specified by the SAS URL into Azure Redis Cache.</span></span>

## <span data-ttu-id="9977b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9977b-110">PARAMETERS</span></span>

### <span data-ttu-id="9977b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9977b-111">-DefaultProfile</span></span>
<span data-ttu-id="9977b-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9977b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9977b-113">-Files</span><span class="sxs-lookup"><span data-stu-id="9977b-113">-Files</span></span>
<span data-ttu-id="9977b-114">Megadja a blobok SAS-URL-eit, amelyek tartalma importálva van a gyorsítótárba.</span><span class="sxs-lookup"><span data-stu-id="9977b-114">Specifies the SAS URLs of blobs whose content this cmdlet imports into the cache.</span></span> <span data-ttu-id="9977b-115">Az SAS URL-címeket a következő PowerShell-parancsokkal hozhatja létre: $storageAccountContext = New-AzStorageContext -StorageAccountName "storageName" -StorageAccountKey "kulcs" $sasKeyForBlob = New-AzStorageBlobSASToken -Container "containerName" -blob "blobName" -Permission "rwdl" -StartTime ([System.DateTime]::Now). AddMinutes(-15) -ExpiryTime ([System.DateTime]:::Now). AddHours(5) -Context $storageAccountContext -FullUri Import-AzRedisCache -ResourceGroupName "ResourceGroupName" -Name "cacheName" -Files ($sasKeyForBlob) -Force</span><span class="sxs-lookup"><span data-stu-id="9977b-115">You can generate the SAS URLs using the following PowerShell commands: $storageAccountContext = New-AzStorageContext -StorageAccountName "storageName" -StorageAccountKey "key" $sasKeyForBlob = New-AzStorageBlobSASToken -Container "containerName" -blob "blobName" -Permission "rwdl" -StartTime ([System.DateTime]::Now).AddMinutes(-15) -ExpiryTime ([System.DateTime]::Now).AddHours(5) -Context $storageAccountContext -FullUri Import-AzRedisCache -ResourceGroupName "ResourceGroupName" -Name "cacheName" -Files ($sasKeyForBlob) -Force</span></span>

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

### <span data-ttu-id="9977b-116">-Force</span><span class="sxs-lookup"><span data-stu-id="9977b-116">-Force</span></span>
<span data-ttu-id="9977b-117">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="9977b-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9977b-118">-Format</span><span class="sxs-lookup"><span data-stu-id="9977b-118">-Format</span></span>
<span data-ttu-id="9977b-119">A blob formátumát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="9977b-119">Specifies the format of the blob.</span></span>
<span data-ttu-id="9977b-120">Jelenleg az rdb az egyetlen támogatott formátum.</span><span class="sxs-lookup"><span data-stu-id="9977b-120">Currently rdb is the only supported format.</span></span>

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

### <span data-ttu-id="9977b-121">-Name</span><span class="sxs-lookup"><span data-stu-id="9977b-121">-Name</span></span>
<span data-ttu-id="9977b-122">A gyorsítótár nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9977b-122">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="9977b-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9977b-123">-PassThru</span></span>
<span data-ttu-id="9977b-124">Azt jelzi, hogy ez a parancsmag egy logikai értéket ad vissza, amely jelzi, hogy a művelet sikeres-e.</span><span class="sxs-lookup"><span data-stu-id="9977b-124">Indicates that this cmdlet returns a Boolean that indicates whether the operation succeeds.</span></span>
<span data-ttu-id="9977b-125">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="9977b-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9977b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9977b-126">-ResourceGroupName</span></span>
<span data-ttu-id="9977b-127">A gyorsítótárat tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9977b-127">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="9977b-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9977b-128">-Confirm</span></span>
<span data-ttu-id="9977b-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="9977b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9977b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9977b-130">-WhatIf</span></span>
<span data-ttu-id="9977b-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="9977b-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9977b-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9977b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9977b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9977b-133">CommonParameters</span></span>
<span data-ttu-id="9977b-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9977b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9977b-135">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9977b-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9977b-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9977b-136">INPUTS</span></span>

### <span data-ttu-id="9977b-137">System.String</span><span class="sxs-lookup"><span data-stu-id="9977b-137">System.String</span></span>

### <span data-ttu-id="9977b-138">System.String[]</span><span class="sxs-lookup"><span data-stu-id="9977b-138">System.String[]</span></span>

## <span data-ttu-id="9977b-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9977b-139">OUTPUTS</span></span>

### <span data-ttu-id="9977b-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9977b-140">System.Boolean</span></span>

## <span data-ttu-id="9977b-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9977b-141">NOTES</span></span>
* <span data-ttu-id="9977b-142">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, redis, cache, web, webapp, webhely</span><span class="sxs-lookup"><span data-stu-id="9977b-142">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="9977b-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9977b-143">RELATED LINKS</span></span>

[<span data-ttu-id="9977b-144">Export-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="9977b-144">Export-AzRedisCache</span></span>](./Export-AzRedisCache.md)

[<span data-ttu-id="9977b-145">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="9977b-145">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="9977b-146">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="9977b-146">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="9977b-147">Reset-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="9977b-147">Reset-AzRedisCache</span></span>](./Reset-AzRedisCache.md)

[<span data-ttu-id="9977b-148">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="9977b-148">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)


