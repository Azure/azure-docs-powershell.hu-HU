---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementcache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementCache.md
ms.openlocfilehash: 4ae5bdd5dc9c15ab72b2f35f5d67eeaa732296bd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012246"
---
# <span data-ttu-id="02797-101">New-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="02797-101">New-AzApiManagementCache</span></span>

## <span data-ttu-id="02797-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="02797-102">SYNOPSIS</span></span>
<span data-ttu-id="02797-103">Új gyorsítótár-entitás létrehozása</span><span class="sxs-lookup"><span data-stu-id="02797-103">Creates a new Cache entity</span></span>

## <span data-ttu-id="02797-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="02797-104">SYNTAX</span></span>

```
New-AzApiManagementCache -Context <PsApiManagementContext> [-CacheId <String>] -ConnectionString <String>
 [-AzureRedisResourceId <String>] [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02797-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="02797-105">DESCRIPTION</span></span>
<span data-ttu-id="02797-106">A **New-AzApiManagementCache** parancsmag új gyorsítótár-entitást hoz létre az API-kezelési szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="02797-106">The cmdlet **New-AzApiManagementCache** creates a new cache entity in Api Management service.</span></span>

## <span data-ttu-id="02797-107">Példák</span><span class="sxs-lookup"><span data-stu-id="02797-107">EXAMPLES</span></span>

### <span data-ttu-id="02797-108">Példa 1: új gyorsítótár-entitás létrehozása</span><span class="sxs-lookup"><span data-stu-id="02797-108">Example 1 : Create a new Cache entity</span></span>
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

<span data-ttu-id="02797-109">A parancsmagok új gyorsítótár-entitást hoznak létre az API-kezelési szolgáltatás fő helyéről.</span><span class="sxs-lookup"><span data-stu-id="02797-109">The cmdlets creates a new cache entity in the master location of the Api Management service.</span></span>

## <span data-ttu-id="02797-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="02797-110">PARAMETERS</span></span>

### <span data-ttu-id="02797-111">-AzureRedisResourceId</span><span class="sxs-lookup"><span data-stu-id="02797-111">-AzureRedisResourceId</span></span>
<span data-ttu-id="02797-112">A kar ResourceId az Azure Redis-gyorsítótár példánya.</span><span class="sxs-lookup"><span data-stu-id="02797-112">Arm ResourceId of the Azure Redis Cache instance.</span></span> <span data-ttu-id="02797-113">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="02797-113">This parameter is optional.</span></span>

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

### <span data-ttu-id="02797-114">-CacheId</span><span class="sxs-lookup"><span data-stu-id="02797-114">-CacheId</span></span>
<span data-ttu-id="02797-115">Az új gyorsítótár azonosítója.</span><span class="sxs-lookup"><span data-stu-id="02797-115">Identifier of new cache.</span></span>
<span data-ttu-id="02797-116">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="02797-116">This parameter is optional.</span></span>
<span data-ttu-id="02797-117">Ha a program nem adja meg a megadott értéket.</span><span class="sxs-lookup"><span data-stu-id="02797-117">If not specified will be generated.</span></span>

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

### <span data-ttu-id="02797-118">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="02797-118">-ConnectionString</span></span>
<span data-ttu-id="02797-119">A Redis kapcsolati karakterlánca.</span><span class="sxs-lookup"><span data-stu-id="02797-119">Redis Connection String.</span></span>
<span data-ttu-id="02797-120">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="02797-120">This parameter is required.</span></span>

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

### <span data-ttu-id="02797-121">-Környezet</span><span class="sxs-lookup"><span data-stu-id="02797-121">-Context</span></span>
<span data-ttu-id="02797-122">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="02797-122">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="02797-123">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="02797-123">This parameter is required.</span></span>

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

### <span data-ttu-id="02797-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02797-124">-DefaultProfile</span></span>
<span data-ttu-id="02797-125">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="02797-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02797-126">-Leírás</span><span class="sxs-lookup"><span data-stu-id="02797-126">-Description</span></span>
<span data-ttu-id="02797-127">Gyorsítótár leírása.</span><span class="sxs-lookup"><span data-stu-id="02797-127">Cache Description.</span></span>
<span data-ttu-id="02797-128">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="02797-128">This parameter is optional.</span></span>

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

### <span data-ttu-id="02797-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="02797-129">-Confirm</span></span>
<span data-ttu-id="02797-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="02797-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02797-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02797-131">-WhatIf</span></span>
<span data-ttu-id="02797-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="02797-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02797-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="02797-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02797-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02797-134">CommonParameters</span></span>
<span data-ttu-id="02797-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="02797-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02797-136">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="02797-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02797-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="02797-137">INPUTS</span></span>

### <span data-ttu-id="02797-138">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="02797-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="02797-139">System. String</span><span class="sxs-lookup"><span data-stu-id="02797-139">System.String</span></span>

## <span data-ttu-id="02797-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="02797-140">OUTPUTS</span></span>

### <span data-ttu-id="02797-141">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="02797-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span></span>

## <span data-ttu-id="02797-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="02797-142">NOTES</span></span>

## <span data-ttu-id="02797-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="02797-143">RELATED LINKS</span></span>

[<span data-ttu-id="02797-144">Get-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="02797-144">Get-AzApiManagementCache</span></span>](./Get-AzApiManagementCache)

[<span data-ttu-id="02797-145">Set-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="02797-145">Set-AzApiManagementCache</span></span>](./Set-AzApiManagementCache.md)

[<span data-ttu-id="02797-146">Remove-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="02797-146">Remove-AzApiManagementCache</span></span>](./Remove-AzApiManagementCache.md)
