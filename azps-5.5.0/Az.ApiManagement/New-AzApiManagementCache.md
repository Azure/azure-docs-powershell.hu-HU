---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementcache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementCache.md
ms.openlocfilehash: cfa2024064256b780121aeb489a3e8988b0a688e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100162642"
---
# <span data-ttu-id="4acec-101">New-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="4acec-101">New-AzApiManagementCache</span></span>

## <span data-ttu-id="4acec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4acec-102">SYNOPSIS</span></span>
<span data-ttu-id="4acec-103">Új gyorsítótárazási entitás létrehozása</span><span class="sxs-lookup"><span data-stu-id="4acec-103">Creates a new Cache entity</span></span>

## <span data-ttu-id="4acec-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="4acec-104">SYNTAX</span></span>

```
New-AzApiManagementCache -Context <PsApiManagementContext> [-CacheId <String>] -ConnectionString <String>
 [-AzureRedisResourceId <String>] [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4acec-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="4acec-105">DESCRIPTION</span></span>
<span data-ttu-id="4acec-106">A **New-AzApiManagementCache** parancsmag létrehoz egy új gyorsítótár-entitást az Api Management szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="4acec-106">The cmdlet **New-AzApiManagementCache** creates a new cache entity in Api Management service.</span></span>

## <span data-ttu-id="4acec-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="4acec-107">EXAMPLES</span></span>

### <span data-ttu-id="4acec-108">1. példa: Új gyorsítótárazási entitás létrehozása</span><span class="sxs-lookup"><span data-stu-id="4acec-108">Example 1 : Create a new Cache entity</span></span>
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

<span data-ttu-id="4acec-109">A parancsmagok új gyorsítótárat hoznak létre az Api Management szolgáltatás fő helyén.</span><span class="sxs-lookup"><span data-stu-id="4acec-109">The cmdlets creates a new cache entity in the master location of the Api Management service.</span></span>

## <span data-ttu-id="4acec-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4acec-110">PARAMETERS</span></span>

### <span data-ttu-id="4acec-111">-AzureRedisResourceId</span><span class="sxs-lookup"><span data-stu-id="4acec-111">-AzureRedisResourceId</span></span>
<span data-ttu-id="4acec-112">Arm ResourceId of the Azure Redis Cache instance.</span><span class="sxs-lookup"><span data-stu-id="4acec-112">Arm ResourceId of the Azure Redis Cache instance.</span></span> <span data-ttu-id="4acec-113">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="4acec-113">This parameter is optional.</span></span>

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

### <span data-ttu-id="4acec-114">-CacheId</span><span class="sxs-lookup"><span data-stu-id="4acec-114">-CacheId</span></span>
<span data-ttu-id="4acec-115">Az új gyorsítótár azonosítója.</span><span class="sxs-lookup"><span data-stu-id="4acec-115">Identifier of new cache.</span></span>
<span data-ttu-id="4acec-116">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="4acec-116">This parameter is optional.</span></span>
<span data-ttu-id="4acec-117">Ha nincs megadva, akkor a program létrehoz egy újat.</span><span class="sxs-lookup"><span data-stu-id="4acec-117">If not specified will be generated.</span></span>

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

### <span data-ttu-id="4acec-118">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="4acec-118">-ConnectionString</span></span>
<span data-ttu-id="4acec-119">Kapcsolati karakterlánc redis.</span><span class="sxs-lookup"><span data-stu-id="4acec-119">Redis Connection String.</span></span>
<span data-ttu-id="4acec-120">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="4acec-120">This parameter is required.</span></span>

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

### <span data-ttu-id="4acec-121">-Környezet</span><span class="sxs-lookup"><span data-stu-id="4acec-121">-Context</span></span>
<span data-ttu-id="4acec-122">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="4acec-122">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="4acec-123">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="4acec-123">This parameter is required.</span></span>

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

### <span data-ttu-id="4acec-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4acec-124">-DefaultProfile</span></span>
<span data-ttu-id="4acec-125">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4acec-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4acec-126">-Leírás</span><span class="sxs-lookup"><span data-stu-id="4acec-126">-Description</span></span>
<span data-ttu-id="4acec-127">Gyorsítótár leírása.</span><span class="sxs-lookup"><span data-stu-id="4acec-127">Cache Description.</span></span>
<span data-ttu-id="4acec-128">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="4acec-128">This parameter is optional.</span></span>

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

### <span data-ttu-id="4acec-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4acec-129">-Confirm</span></span>
<span data-ttu-id="4acec-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="4acec-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4acec-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4acec-131">-WhatIf</span></span>
<span data-ttu-id="4acec-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="4acec-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4acec-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4acec-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4acec-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4acec-134">CommonParameters</span></span>
<span data-ttu-id="4acec-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4acec-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4acec-136">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4acec-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4acec-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4acec-137">INPUTS</span></span>

### <span data-ttu-id="4acec-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="4acec-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="4acec-139">System.String</span><span class="sxs-lookup"><span data-stu-id="4acec-139">System.String</span></span>

## <span data-ttu-id="4acec-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4acec-140">OUTPUTS</span></span>

### <span data-ttu-id="4acec-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="4acec-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span></span>

## <span data-ttu-id="4acec-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="4acec-142">NOTES</span></span>

## <span data-ttu-id="4acec-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4acec-143">RELATED LINKS</span></span>

[<span data-ttu-id="4acec-144">Get-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="4acec-144">Get-AzApiManagementCache</span></span>](./Get-AzApiManagementCache.md)

[<span data-ttu-id="4acec-145">Remove-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="4acec-145">Remove-AzApiManagementCache</span></span>](./Remove-AzApiManagementCache.md)

[<span data-ttu-id="4acec-146">Update-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="4acec-146">Update-AzApiManagementCache</span></span>](./Update-AzApiManagementCache.md)
