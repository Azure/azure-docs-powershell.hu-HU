---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/update-azapimanagementcache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementCache.md
ms.openlocfilehash: 2ac2eb7cb40cb7df4324aff276137527d4b148a5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183742"
---
# <span data-ttu-id="b3ed2-101">Update-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="b3ed2-101">Update-AzApiManagementCache</span></span>

## <span data-ttu-id="b3ed2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b3ed2-102">SYNOPSIS</span></span>
<span data-ttu-id="b3ed2-103">frissít egy gyorsítótárat az API-kezelési szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="b3ed2-103">updates a cache in Api Management service.</span></span>

## <span data-ttu-id="b3ed2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b3ed2-104">SYNTAX</span></span>

### <span data-ttu-id="b3ed2-105">ExpandedParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b3ed2-105">ExpandedParameter (Default)</span></span>
```
Update-AzApiManagementCache -Context <PsApiManagementContext> -CacheId <String> [-ConnectionString <String>]
 [-AzureRedisResourceId <String>] [-Description <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3ed2-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="b3ed2-106">ByInputObject</span></span>
```
Update-AzApiManagementCache -InputObject <PsApiManagementCache> [-ConnectionString <String>]
 [-AzureRedisResourceId <String>] [-Description <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3ed2-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b3ed2-107">ByResourceId</span></span>
```
Update-AzApiManagementCache -ResourceId <String> [-ConnectionString <String>] [-AzureRedisResourceId <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b3ed2-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="b3ed2-108">DESCRIPTION</span></span>
<span data-ttu-id="b3ed2-109">A parancsmag **Update-AzApiManagementCache** frissíti a gyorsítótárat a ApiManagement szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="b3ed2-109">The cmdlet **Update-AzApiManagementCache** updates a cache in the ApiManagement service.</span></span>

## <span data-ttu-id="b3ed2-110">Példák</span><span class="sxs-lookup"><span data-stu-id="b3ed2-110">EXAMPLES</span></span>

### <span data-ttu-id="b3ed2-111">1. példa: frissíti a gyorsítótár tartalmát a CentralUS-ban</span><span class="sxs-lookup"><span data-stu-id="b3ed2-111">Example 1 : Updates the Description of the Cache in centralus</span></span>
```powershell
PS D:\github\azure-powershell> $context=New-AzApiManagementContext -ResourceGroupName Api-Default-Central-US -ServiceName contoso
PS D:\github\azure-powershell> Update-AzApiManagementCache -Context $context -CacheId centralus -Description "Team new cache" -PassThru


CacheId              : centralus
Description          : Team new cache
ConnectionString     : {{5cc19889e6ed3b0524c3f7d3}}
AzureRedisResourceId :
Id                   : /subscriptions/subid/resourceGroups/Api-Default-Central-US/providers/M
                       icrosoft.ApiManagement/service/contoso/caches/centralus
ResourceGroupName    : Api-Default-Central-US
ServiceName          : contoso
```

<span data-ttu-id="b3ed2-112">Frissíti a közép-amerikai gyorsítótár leírását.</span><span class="sxs-lookup"><span data-stu-id="b3ed2-112">Updates the description of the Cache in Central US.</span></span>

## <span data-ttu-id="b3ed2-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b3ed2-113">PARAMETERS</span></span>

### <span data-ttu-id="b3ed2-114">-AzureRedisResourceId</span><span class="sxs-lookup"><span data-stu-id="b3ed2-114">-AzureRedisResourceId</span></span>
<span data-ttu-id="b3ed2-115">A kar ResourceId az Azure Redis-gyorsítótár példánya.</span><span class="sxs-lookup"><span data-stu-id="b3ed2-115">Arm ResourceId of the Azure Redis Cache instance.</span></span>
<span data-ttu-id="b3ed2-116">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="b3ed2-116">This parameter is optional.</span></span>

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

### <span data-ttu-id="b3ed2-117">-CacheId</span><span class="sxs-lookup"><span data-stu-id="b3ed2-117">-CacheId</span></span>
<span data-ttu-id="b3ed2-118">Az új gyorsítótár azonosítója.</span><span class="sxs-lookup"><span data-stu-id="b3ed2-118">Identifier of new cache.</span></span>
<span data-ttu-id="b3ed2-119">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="b3ed2-119">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3ed2-120">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="b3ed2-120">-ConnectionString</span></span>
<span data-ttu-id="b3ed2-121">A Redis kapcsolati karakterlánca.</span><span class="sxs-lookup"><span data-stu-id="b3ed2-121">Redis Connection String.</span></span>
<span data-ttu-id="b3ed2-122">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="b3ed2-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="b3ed2-123">-Környezet</span><span class="sxs-lookup"><span data-stu-id="b3ed2-123">-Context</span></span>
<span data-ttu-id="b3ed2-124">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="b3ed2-124">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="b3ed2-125">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="b3ed2-125">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b3ed2-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3ed2-126">-DefaultProfile</span></span>
<span data-ttu-id="b3ed2-127">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b3ed2-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3ed2-128">-Leírás</span><span class="sxs-lookup"><span data-stu-id="b3ed2-128">-Description</span></span>
<span data-ttu-id="b3ed2-129">Gyorsítótár leírása.</span><span class="sxs-lookup"><span data-stu-id="b3ed2-129">Cache Description.</span></span>
<span data-ttu-id="b3ed2-130">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="b3ed2-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="b3ed2-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b3ed2-131">-InputObject</span></span>
<span data-ttu-id="b3ed2-132">A PsApiManagementCache példánya.</span><span class="sxs-lookup"><span data-stu-id="b3ed2-132">Instance of PsApiManagementCache.</span></span>
<span data-ttu-id="b3ed2-133">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="b3ed2-133">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b3ed2-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b3ed2-134">-PassThru</span></span>
<span data-ttu-id="b3ed2-135">Ha meg van adva a Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementCache típusa, ami a módosított gyorsítótárat jelképezi, a kimenetre fog írni.</span><span class="sxs-lookup"><span data-stu-id="b3ed2-135">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache type  representing the modified cache will be written to output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3ed2-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b3ed2-136">-ResourceId</span></span>
<span data-ttu-id="b3ed2-137">A kar ResourceId a gyorsítótárból.</span><span class="sxs-lookup"><span data-stu-id="b3ed2-137">Arm ResourceId of Cache.</span></span>
<span data-ttu-id="b3ed2-138">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="b3ed2-138">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3ed2-139">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b3ed2-139">-Confirm</span></span>
<span data-ttu-id="b3ed2-140">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b3ed2-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3ed2-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3ed2-141">-WhatIf</span></span>
<span data-ttu-id="b3ed2-142">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b3ed2-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3ed2-143">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b3ed2-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3ed2-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3ed2-144">CommonParameters</span></span>
<span data-ttu-id="b3ed2-145">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b3ed2-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3ed2-146">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b3ed2-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3ed2-147">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b3ed2-147">INPUTS</span></span>

### <span data-ttu-id="b3ed2-148">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b3ed2-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="b3ed2-149">System. String</span><span class="sxs-lookup"><span data-stu-id="b3ed2-149">System.String</span></span>

### <span data-ttu-id="b3ed2-150">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="b3ed2-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span></span>

### <span data-ttu-id="b3ed2-151">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="b3ed2-151">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="b3ed2-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b3ed2-152">OUTPUTS</span></span>

### <span data-ttu-id="b3ed2-153">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="b3ed2-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span></span>

## <span data-ttu-id="b3ed2-154">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b3ed2-154">NOTES</span></span>

## <span data-ttu-id="b3ed2-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b3ed2-155">RELATED LINKS</span></span>

[<span data-ttu-id="b3ed2-156">Új – AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="b3ed2-156">New-AzApiManagementCache</span></span>](./New-AzApiManagementCache.md)

[<span data-ttu-id="b3ed2-157">Get-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="b3ed2-157">Get-AzApiManagementCache</span></span>](./Get-AzApiManagementCache.md)

[<span data-ttu-id="b3ed2-158">Remove-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="b3ed2-158">Remove-AzApiManagementCache</span></span>](./Remove-AzApiManagementCache.md)
