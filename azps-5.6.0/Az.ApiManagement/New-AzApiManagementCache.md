---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/new-azapimanagementcache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementCache.md
ms.openlocfilehash: 13fe16c2612a267df0760aad939b46e427d6fab1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101923066"
---
# <span data-ttu-id="132af-101">New-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="132af-101">New-AzApiManagementCache</span></span>

## <span data-ttu-id="132af-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="132af-102">SYNOPSIS</span></span>
<span data-ttu-id="132af-103">Új gyorsítótárazási entitás létrehozása</span><span class="sxs-lookup"><span data-stu-id="132af-103">Creates a new Cache entity</span></span>

## <span data-ttu-id="132af-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="132af-104">SYNTAX</span></span>

```
New-AzApiManagementCache -Context <PsApiManagementContext> [-CacheId <String>] -ConnectionString <String>
 [-AzureRedisResourceId <String>] [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="132af-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="132af-105">DESCRIPTION</span></span>
<span data-ttu-id="132af-106">A **New-AzApiManagementCache** parancsmag létrehoz egy új gyorsítótárattitást az Api Management szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="132af-106">The cmdlet **New-AzApiManagementCache** creates a new cache entity in Api Management service.</span></span>

## <span data-ttu-id="132af-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="132af-107">EXAMPLES</span></span>

### <span data-ttu-id="132af-108">1. példa: Új gyorsítótárazási entitás létrehozása</span><span class="sxs-lookup"><span data-stu-id="132af-108">Example 1 : Create a new Cache entity</span></span>
```powershell
PS c:\> New-AzApiManagementCache -Context $context -ConnectionString "teamdemo.redis.cache.windows.net:6380,password=xxxxxx+xxxxx=,ssl=True,abortConnect=False" -Description "Team Cache"

CacheId           : centralus
Description       : Team Cache
ConnectionString  : {{5cc19889e6ed3b0524c3f7d3}}
ResourceId        :
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsof
                    t.ApiManagement/service/contoso/caches/centralus
ResourceGroupName : Api-Default-WestUS
ServiceName       : contoso
```

<span data-ttu-id="132af-109">A parancsmagok új gyorsítótárat hoznak létre az Api Management szolgáltatás fő helyén.</span><span class="sxs-lookup"><span data-stu-id="132af-109">The cmdlets creates a new cache entity in the master location of the Api Management service.</span></span>

## <span data-ttu-id="132af-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="132af-110">PARAMETERS</span></span>

### <span data-ttu-id="132af-111">-AzureRedisResourceId</span><span class="sxs-lookup"><span data-stu-id="132af-111">-AzureRedisResourceId</span></span>
<span data-ttu-id="132af-112">Arm ResourceId of the Azure Redis Cache instance.</span><span class="sxs-lookup"><span data-stu-id="132af-112">Arm ResourceId of the Azure Redis Cache instance.</span></span> <span data-ttu-id="132af-113">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="132af-113">This parameter is optional.</span></span>

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

### <span data-ttu-id="132af-114">-CacheId</span><span class="sxs-lookup"><span data-stu-id="132af-114">-CacheId</span></span>
<span data-ttu-id="132af-115">Az új gyorsítótár azonosítója.</span><span class="sxs-lookup"><span data-stu-id="132af-115">Identifier of new cache.</span></span>
<span data-ttu-id="132af-116">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="132af-116">This parameter is optional.</span></span>
<span data-ttu-id="132af-117">Ha nincs megadva, akkor a program létrehoz egy újat.</span><span class="sxs-lookup"><span data-stu-id="132af-117">If not specified will be generated.</span></span>

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

### <span data-ttu-id="132af-118">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="132af-118">-ConnectionString</span></span>
<span data-ttu-id="132af-119">Kapcsolati karakterlánc redis.</span><span class="sxs-lookup"><span data-stu-id="132af-119">Redis Connection String.</span></span>
<span data-ttu-id="132af-120">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="132af-120">This parameter is required.</span></span>

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

### <span data-ttu-id="132af-121">-Környezet</span><span class="sxs-lookup"><span data-stu-id="132af-121">-Context</span></span>
<span data-ttu-id="132af-122">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="132af-122">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="132af-123">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="132af-123">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="132af-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="132af-124">-DefaultProfile</span></span>
<span data-ttu-id="132af-125">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="132af-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="132af-126">-Leírás</span><span class="sxs-lookup"><span data-stu-id="132af-126">-Description</span></span>
<span data-ttu-id="132af-127">Gyorsítótár leírása.</span><span class="sxs-lookup"><span data-stu-id="132af-127">Cache Description.</span></span>
<span data-ttu-id="132af-128">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="132af-128">This parameter is optional.</span></span>

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

### <span data-ttu-id="132af-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="132af-129">-Confirm</span></span>
<span data-ttu-id="132af-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="132af-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="132af-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="132af-131">-WhatIf</span></span>
<span data-ttu-id="132af-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="132af-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="132af-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="132af-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="132af-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="132af-134">CommonParameters</span></span>
<span data-ttu-id="132af-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="132af-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="132af-136">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="132af-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="132af-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="132af-137">INPUTS</span></span>

### <span data-ttu-id="132af-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="132af-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="132af-139">System.String</span><span class="sxs-lookup"><span data-stu-id="132af-139">System.String</span></span>

## <span data-ttu-id="132af-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="132af-140">OUTPUTS</span></span>

### <span data-ttu-id="132af-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="132af-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span></span>

## <span data-ttu-id="132af-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="132af-142">NOTES</span></span>

## <span data-ttu-id="132af-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="132af-143">RELATED LINKS</span></span>

[<span data-ttu-id="132af-144">Get-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="132af-144">Get-AzApiManagementCache</span></span>](./Get-AzApiManagementCache.md)

[<span data-ttu-id="132af-145">Remove-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="132af-145">Remove-AzApiManagementCache</span></span>](./Remove-AzApiManagementCache.md)

[<span data-ttu-id="132af-146">Update-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="132af-146">Update-AzApiManagementCache</span></span>](./Update-AzApiManagementCache.md)
