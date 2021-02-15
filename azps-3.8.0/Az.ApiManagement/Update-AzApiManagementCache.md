---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/update-azapimanagementcache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementCache.md
ms.openlocfilehash: 2ac2eb7cb40cb7df4324aff276137527d4b148a5
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100398920"
---
# <span data-ttu-id="41485-101">Update-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="41485-101">Update-AzApiManagementCache</span></span>

## <span data-ttu-id="41485-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="41485-102">SYNOPSIS</span></span>
<span data-ttu-id="41485-103">frissíti a gyorsítótárat az Api Management szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="41485-103">updates a cache in Api Management service.</span></span>

## <span data-ttu-id="41485-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="41485-104">SYNTAX</span></span>

### <span data-ttu-id="41485-105">ExpandedParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="41485-105">ExpandedParameter (Default)</span></span>
```
Update-AzApiManagementCache -Context <PsApiManagementContext> -CacheId <String> [-ConnectionString <String>]
 [-AzureRedisResourceId <String>] [-Description <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41485-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="41485-106">ByInputObject</span></span>
```
Update-AzApiManagementCache -InputObject <PsApiManagementCache> [-ConnectionString <String>]
 [-AzureRedisResourceId <String>] [-Description <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41485-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="41485-107">ByResourceId</span></span>
```
Update-AzApiManagementCache -ResourceId <String> [-ConnectionString <String>] [-AzureRedisResourceId <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="41485-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="41485-108">DESCRIPTION</span></span>
<span data-ttu-id="41485-109">Az **Update-AzApiManagementCache** parancsmag frissíti a gyorsítótárat az ApiManagement szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="41485-109">The cmdlet **Update-AzApiManagementCache** updates a cache in the ApiManagement service.</span></span>

## <span data-ttu-id="41485-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="41485-110">EXAMPLES</span></span>

### <span data-ttu-id="41485-111">1. példa: A gyorsítótár leírásának frissítése a centralusban</span><span class="sxs-lookup"><span data-stu-id="41485-111">Example 1 : Updates the Description of the Cache in centralus</span></span>
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

<span data-ttu-id="41485-112">Frissíti a közép-amerikai gyorsítótár leírását.</span><span class="sxs-lookup"><span data-stu-id="41485-112">Updates the description of the Cache in Central US.</span></span>

## <span data-ttu-id="41485-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="41485-113">PARAMETERS</span></span>

### <span data-ttu-id="41485-114">-AzureRedisResourceId</span><span class="sxs-lookup"><span data-stu-id="41485-114">-AzureRedisResourceId</span></span>
<span data-ttu-id="41485-115">Arm ResourceId of the Azure Redis Cache instance.</span><span class="sxs-lookup"><span data-stu-id="41485-115">Arm ResourceId of the Azure Redis Cache instance.</span></span>
<span data-ttu-id="41485-116">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="41485-116">This parameter is optional.</span></span>

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

### <span data-ttu-id="41485-117">-CacheId</span><span class="sxs-lookup"><span data-stu-id="41485-117">-CacheId</span></span>
<span data-ttu-id="41485-118">Az új gyorsítótár azonosítója.</span><span class="sxs-lookup"><span data-stu-id="41485-118">Identifier of new cache.</span></span>
<span data-ttu-id="41485-119">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="41485-119">This parameter is required.</span></span>

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

### <span data-ttu-id="41485-120">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="41485-120">-ConnectionString</span></span>
<span data-ttu-id="41485-121">Kapcsolati karakterlánc újradirata</span><span class="sxs-lookup"><span data-stu-id="41485-121">Redis Connection String.</span></span>
<span data-ttu-id="41485-122">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="41485-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="41485-123">-Környezet</span><span class="sxs-lookup"><span data-stu-id="41485-123">-Context</span></span>
<span data-ttu-id="41485-124">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="41485-124">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="41485-125">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="41485-125">This parameter is required.</span></span>

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

### <span data-ttu-id="41485-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41485-126">-DefaultProfile</span></span>
<span data-ttu-id="41485-127">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="41485-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41485-128">-Leírás</span><span class="sxs-lookup"><span data-stu-id="41485-128">-Description</span></span>
<span data-ttu-id="41485-129">Gyorsítótár leírása.</span><span class="sxs-lookup"><span data-stu-id="41485-129">Cache Description.</span></span>
<span data-ttu-id="41485-130">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="41485-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="41485-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="41485-131">-InputObject</span></span>
<span data-ttu-id="41485-132">A PsApiManagementCache példánya.</span><span class="sxs-lookup"><span data-stu-id="41485-132">Instance of PsApiManagementCache.</span></span>
<span data-ttu-id="41485-133">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="41485-133">This parameter is required.</span></span>

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

### <span data-ttu-id="41485-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="41485-134">-PassThru</span></span>
<span data-ttu-id="41485-135">Ha ez meg van adva, akkor a módosított gyorsítótárat képviselő Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache típusú példány kimenetként lesz megírva.</span><span class="sxs-lookup"><span data-stu-id="41485-135">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache type  representing the modified cache will be written to output.</span></span>

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

### <span data-ttu-id="41485-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="41485-136">-ResourceId</span></span>
<span data-ttu-id="41485-137">Gyorsítótár erőforrásazonosítója arm.</span><span class="sxs-lookup"><span data-stu-id="41485-137">Arm ResourceId of Cache.</span></span>
<span data-ttu-id="41485-138">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="41485-138">This parameter is required.</span></span>

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

### <span data-ttu-id="41485-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="41485-139">-Confirm</span></span>
<span data-ttu-id="41485-140">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="41485-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41485-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41485-141">-WhatIf</span></span>
<span data-ttu-id="41485-142">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="41485-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41485-143">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="41485-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41485-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41485-144">CommonParameters</span></span>
<span data-ttu-id="41485-145">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41485-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41485-146">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="41485-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41485-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="41485-147">INPUTS</span></span>

### <span data-ttu-id="41485-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="41485-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="41485-149">System.String</span><span class="sxs-lookup"><span data-stu-id="41485-149">System.String</span></span>

### <span data-ttu-id="41485-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="41485-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span></span>

### <span data-ttu-id="41485-151">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="41485-151">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="41485-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="41485-152">OUTPUTS</span></span>

### <span data-ttu-id="41485-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="41485-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span></span>

## <span data-ttu-id="41485-154">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="41485-154">NOTES</span></span>

## <span data-ttu-id="41485-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="41485-155">RELATED LINKS</span></span>

[<span data-ttu-id="41485-156">New-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="41485-156">New-AzApiManagementCache</span></span>](./New-AzApiManagementCache.md)

[<span data-ttu-id="41485-157">Get-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="41485-157">Get-AzApiManagementCache</span></span>](./Get-AzApiManagementCache.md)

[<span data-ttu-id="41485-158">Remove-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="41485-158">Remove-AzApiManagementCache</span></span>](./Remove-AzApiManagementCache.md)
