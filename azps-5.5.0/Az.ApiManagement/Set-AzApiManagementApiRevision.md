---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementapirevision
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiRevision.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiRevision.md
ms.openlocfilehash: fcae55c69b1874e06ce9110631baaf3b679fe99a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100210311"
---
# <span data-ttu-id="dd9ad-101">Set-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="dd9ad-101">Set-AzApiManagementApiRevision</span></span>

## <span data-ttu-id="dd9ad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dd9ad-102">SYNOPSIS</span></span>
<span data-ttu-id="dd9ad-103">Módosítja az API-változatot</span><span class="sxs-lookup"><span data-stu-id="dd9ad-103">Modifies an API Revision</span></span>

## <span data-ttu-id="dd9ad-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="dd9ad-104">SYNTAX</span></span>

### <span data-ttu-id="dd9ad-105">ExpandedParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="dd9ad-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementApiRevision -ApiRevision <String> -Context <PsApiManagementContext> -ApiId <String>
 [-Name <String>] [-Description <String>] [-ServiceUrl <String>] [-Path <String>]
 [-Protocols <PsApiManagementSchema[]>] [-AuthorizationServerId <String>] [-AuthorizationScope <String>]
 [-OpenIdProviderId <String>] [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-SubscriptionRequired] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd9ad-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="dd9ad-106">ByInputObject</span></span>
```
Set-AzApiManagementApiRevision -InputObject <PsApiManagementApi> [-Name <String>] [-Description <String>]
 [-ServiceUrl <String>] [-Path <String>] [-Protocols <PsApiManagementSchema[]>]
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-OpenIdProviderId <String>]
 [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-SubscriptionRequired] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd9ad-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="dd9ad-107">DESCRIPTION</span></span>
<span data-ttu-id="dd9ad-108">A **Set-AzApiManagementApiRevision** parancsmag módosítja az Azure API Felügyeleti API-változatot.</span><span class="sxs-lookup"><span data-stu-id="dd9ad-108">The **Set-AzApiManagementApiRevision** cmdlet modifies an Azure API Management API Revision.</span></span>

## <span data-ttu-id="dd9ad-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="dd9ad-109">EXAMPLES</span></span>

### <span data-ttu-id="dd9ad-110">1. példa: API-változat módosítása</span><span class="sxs-lookup"><span data-stu-id="dd9ad-110">Example 1: Modify an API Revision</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementApiRevision -Context $ApiMgmtContext -ApiId "echo-api" -ApiRevision "2" -Name "EchoApi" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @('https') -Description "Responds with what was sent" -Path "echo"
```

<span data-ttu-id="dd9ad-111">A parancsmag egy új leírással, protokollal és elérési útkal frissíti az `2` API `echo-api` átdolgozását.</span><span class="sxs-lookup"><span data-stu-id="dd9ad-111">The cmdlet updates the `2` revision of the API `echo-api` with a new description, protocol and path.</span></span>

## <span data-ttu-id="dd9ad-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dd9ad-112">PARAMETERS</span></span>

### <span data-ttu-id="dd9ad-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="dd9ad-113">-ApiId</span></span>
<span data-ttu-id="dd9ad-114">A meglévő API azonosítója.</span><span class="sxs-lookup"><span data-stu-id="dd9ad-114">Identifier of existing API.</span></span>
<span data-ttu-id="dd9ad-115">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="dd9ad-115">This parameter is required.</span></span>

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

### <span data-ttu-id="dd9ad-116">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="dd9ad-116">-ApiRevision</span></span>
<span data-ttu-id="dd9ad-117">A meglévő API-változat azonosítója.</span><span class="sxs-lookup"><span data-stu-id="dd9ad-117">Identifier of existing API Revision.</span></span> <span data-ttu-id="dd9ad-118">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="dd9ad-118">This parameter is required.</span></span>

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

### <span data-ttu-id="dd9ad-119">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="dd9ad-119">-AuthorizationScope</span></span>
<span data-ttu-id="dd9ad-120">OAuth-műveletek hatóköre.</span><span class="sxs-lookup"><span data-stu-id="dd9ad-120">OAuth operations scope.</span></span>
<span data-ttu-id="dd9ad-121">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="dd9ad-121">This parameter is optional.</span></span>
<span data-ttu-id="dd9ad-122">Az alapértelmezett érték $null.</span><span class="sxs-lookup"><span data-stu-id="dd9ad-122">Default value is $null.</span></span>

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

### <span data-ttu-id="dd9ad-123">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="dd9ad-123">-AuthorizationServerId</span></span>
<span data-ttu-id="dd9ad-124">OAuth engedélyezési kiszolgáló azonosítója.</span><span class="sxs-lookup"><span data-stu-id="dd9ad-124">OAuth authorization server identifier.</span></span>
<span data-ttu-id="dd9ad-125">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="dd9ad-125">This parameter is optional.</span></span>
<span data-ttu-id="dd9ad-126">Az alapértelmezett érték $null.</span><span class="sxs-lookup"><span data-stu-id="dd9ad-126">Default value is $null.</span></span>
<span data-ttu-id="dd9ad-127">Ha az AuthorizationScope meg van adva, meg kell adni.</span><span class="sxs-lookup"><span data-stu-id="dd9ad-127">Must be specified if AuthorizationScope specified.</span></span>

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

### <span data-ttu-id="dd9ad-128">-BearerTokenSendingMethod</span><span class="sxs-lookup"><span data-stu-id="dd9ad-128">-BearerTokenSendingMethod</span></span>
<span data-ttu-id="dd9ad-129">OpenId engedélyezési kiszolgálói mechanizmus, amellyel hozzáférési jogkivonatot ad át az API-nak.</span><span class="sxs-lookup"><span data-stu-id="dd9ad-129">OpenId authorization server mechanism by which access token is passed to the API.</span></span> <span data-ttu-id="dd9ad-130">Lásd: http://tools.ietf.org/html/rfc6749#section-4 .</span><span class="sxs-lookup"><span data-stu-id="dd9ad-130">Refer to http://tools.ietf.org/html/rfc6749#section-4.</span></span> <span data-ttu-id="dd9ad-131">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="dd9ad-131">This parameter is optional.</span></span> <span data-ttu-id="dd9ad-132">Az alapértelmezett érték $null.</span><span class="sxs-lookup"><span data-stu-id="dd9ad-132">Default value is $null.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd9ad-133">-Környezet</span><span class="sxs-lookup"><span data-stu-id="dd9ad-133">-Context</span></span>
<span data-ttu-id="dd9ad-134">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="dd9ad-134">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="dd9ad-135">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="dd9ad-135">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dd9ad-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd9ad-136">-DefaultProfile</span></span>
<span data-ttu-id="dd9ad-137">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="dd9ad-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd9ad-138">-Leírás</span><span class="sxs-lookup"><span data-stu-id="dd9ad-138">-Description</span></span>
<span data-ttu-id="dd9ad-139">Web API-leírás.</span><span class="sxs-lookup"><span data-stu-id="dd9ad-139">Web API description.</span></span>
<span data-ttu-id="dd9ad-140">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="dd9ad-140">This parameter is optional.</span></span>

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

### <span data-ttu-id="dd9ad-141">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dd9ad-141">-InputObject</span></span>
<span data-ttu-id="dd9ad-142">A PsApiManagementApi példánya.</span><span class="sxs-lookup"><span data-stu-id="dd9ad-142">Instance of PsApiManagementApi.</span></span> <span data-ttu-id="dd9ad-143">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="dd9ad-143">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dd9ad-144">-Name</span><span class="sxs-lookup"><span data-stu-id="dd9ad-144">-Name</span></span>
<span data-ttu-id="dd9ad-145">Web API-név.</span><span class="sxs-lookup"><span data-stu-id="dd9ad-145">Web API name.</span></span>
<span data-ttu-id="dd9ad-146">Az API nyilvános neve úgy, ahogyan a fejlesztői és rendszergazdai portálon látható lenne.</span><span class="sxs-lookup"><span data-stu-id="dd9ad-146">Public name of the API as it would appear on the developer and admin portals.</span></span>
<span data-ttu-id="dd9ad-147">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="dd9ad-147">This parameter is required.</span></span>

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

### <span data-ttu-id="dd9ad-148">-OpenIdProviderId</span><span class="sxs-lookup"><span data-stu-id="dd9ad-148">-OpenIdProviderId</span></span>
<span data-ttu-id="dd9ad-149">OpenId engedélyezési kiszolgáló azonosítója.</span><span class="sxs-lookup"><span data-stu-id="dd9ad-149">OpenId authorization server identifier.</span></span> <span data-ttu-id="dd9ad-150">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="dd9ad-150">This parameter is optional.</span></span> <span data-ttu-id="dd9ad-151">Az alapértelmezett érték $null.</span><span class="sxs-lookup"><span data-stu-id="dd9ad-151">Default value is $null.</span></span> <span data-ttu-id="dd9ad-152">Meg kell adni, ha a BearerTokenSendingMethods érték meg van adva.</span><span class="sxs-lookup"><span data-stu-id="dd9ad-152">Must be specified if BearerTokenSendingMethods is specified.</span></span>

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

### <span data-ttu-id="dd9ad-153">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dd9ad-153">-PassThru</span></span>
<span data-ttu-id="dd9ad-154">Ha ez meg van adva, akkor a Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi típus képviseli a beállított API-t.</span><span class="sxs-lookup"><span data-stu-id="dd9ad-154">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi type representing the set API.</span></span>

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

### <span data-ttu-id="dd9ad-155">-Path</span><span class="sxs-lookup"><span data-stu-id="dd9ad-155">-Path</span></span>
<span data-ttu-id="dd9ad-156">Web API Elérési út.</span><span class="sxs-lookup"><span data-stu-id="dd9ad-156">Web API Path.</span></span>
<span data-ttu-id="dd9ad-157">Az API nyilvános URL-címének utolsó része.</span><span class="sxs-lookup"><span data-stu-id="dd9ad-157">Last part of the API's public URL.</span></span>
<span data-ttu-id="dd9ad-158">Ezt az URL-címet használják az API-t használó ügyfelek arra, hogy kéréseket küldenek a webszolgáltatásnak.</span><span class="sxs-lookup"><span data-stu-id="dd9ad-158">This URL will be used by API consumers for sending requests to the web service.</span></span>
<span data-ttu-id="dd9ad-159">1–400 karakter hosszúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="dd9ad-159">Must be 1 to 400 characters long.</span></span>
<span data-ttu-id="dd9ad-160">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="dd9ad-160">This parameter is optional.</span></span>
<span data-ttu-id="dd9ad-161">Az alapértelmezett érték $null.</span><span class="sxs-lookup"><span data-stu-id="dd9ad-161">Default value is $null.</span></span>

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

### <span data-ttu-id="dd9ad-162">-Protocols</span><span class="sxs-lookup"><span data-stu-id="dd9ad-162">-Protocols</span></span>
<span data-ttu-id="dd9ad-163">Web API-protokollok (http, https).</span><span class="sxs-lookup"><span data-stu-id="dd9ad-163">Web API protocols (http, https).</span></span>
<span data-ttu-id="dd9ad-164">Protokollok, amelyeken keresztül az API elérhetővé válik.</span><span class="sxs-lookup"><span data-stu-id="dd9ad-164">Protocols over which API is made available.</span></span>
<span data-ttu-id="dd9ad-165">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="dd9ad-165">This parameter is required.</span></span>
<span data-ttu-id="dd9ad-166">Az alapértelmezett érték $null.</span><span class="sxs-lookup"><span data-stu-id="dd9ad-166">Default value is $null.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]
Parameter Sets: (All)
Aliases:
Accepted values: Http, Https

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd9ad-167">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="dd9ad-167">-ServiceUrl</span></span>
<span data-ttu-id="dd9ad-168">A webszolgáltatás API-t kitűnő URL-címe.</span><span class="sxs-lookup"><span data-stu-id="dd9ad-168">A URL of the web service exposing the API.</span></span>
<span data-ttu-id="dd9ad-169">Ezt az URL-címet csak az Azure API Management fogja használni, és nem teszi nyilvánosra.</span><span class="sxs-lookup"><span data-stu-id="dd9ad-169">This URL will be used by Azure API Management only, and will not be made public.</span></span>
<span data-ttu-id="dd9ad-170">1–2000 karakter hosszúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="dd9ad-170">Must be 1 to 2000 characters long.</span></span>
<span data-ttu-id="dd9ad-171">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="dd9ad-171">This parameter is required.</span></span>

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

### <span data-ttu-id="dd9ad-172">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="dd9ad-172">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="dd9ad-173">Az előfizetés kulcsfejlécének neve.</span><span class="sxs-lookup"><span data-stu-id="dd9ad-173">Subscription key header name.</span></span>
<span data-ttu-id="dd9ad-174">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="dd9ad-174">This parameter is optional.</span></span>
<span data-ttu-id="dd9ad-175">Az alapértelmezett érték $null.</span><span class="sxs-lookup"><span data-stu-id="dd9ad-175">Default value is $null.</span></span>

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

### <span data-ttu-id="dd9ad-176">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="dd9ad-176">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="dd9ad-177">Az előfizetéskulcs lekérdezési karakterláncának paraméterneve.</span><span class="sxs-lookup"><span data-stu-id="dd9ad-177">Subscription key query string parameter name.</span></span>
<span data-ttu-id="dd9ad-178">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="dd9ad-178">This parameter is optional.</span></span>
<span data-ttu-id="dd9ad-179">Az alapértelmezett érték $null.</span><span class="sxs-lookup"><span data-stu-id="dd9ad-179">Default value is $null.</span></span>

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

### <span data-ttu-id="dd9ad-180">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="dd9ad-180">-SubscriptionRequired</span></span>
<span data-ttu-id="dd9ad-181">Flag to enforce SubscriptionRequired for requests to the Api.</span><span class="sxs-lookup"><span data-stu-id="dd9ad-181">Flag to enforce SubscriptionRequired for requests to the Api.</span></span> <span data-ttu-id="dd9ad-182">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="dd9ad-182">This parameter is optional.</span></span>

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

### <span data-ttu-id="dd9ad-183">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dd9ad-183">-Confirm</span></span>
<span data-ttu-id="dd9ad-184">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="dd9ad-184">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd9ad-185">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd9ad-185">-WhatIf</span></span>
<span data-ttu-id="dd9ad-186">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="dd9ad-186">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd9ad-187">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="dd9ad-187">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd9ad-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd9ad-188">CommonParameters</span></span>
<span data-ttu-id="dd9ad-189">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd9ad-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd9ad-190">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dd9ad-190">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd9ad-191">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dd9ad-191">INPUTS</span></span>

### <span data-ttu-id="dd9ad-192">System.String</span><span class="sxs-lookup"><span data-stu-id="dd9ad-192">System.String</span></span>

### <span data-ttu-id="dd9ad-193">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="dd9ad-193">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="dd9ad-194">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="dd9ad-194">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

### <span data-ttu-id="dd9ad-195">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span><span class="sxs-lookup"><span data-stu-id="dd9ad-195">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="dd9ad-196">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="dd9ad-196">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="dd9ad-197">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dd9ad-197">OUTPUTS</span></span>

### <span data-ttu-id="dd9ad-198">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="dd9ad-198">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="dd9ad-199">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="dd9ad-199">NOTES</span></span>

## <span data-ttu-id="dd9ad-200">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dd9ad-200">RELATED LINKS</span></span>

[<span data-ttu-id="dd9ad-201">Get-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="dd9ad-201">Get-AzApiManagementApiRevision</span></span>](./Get-AzApiManagementApiRevision.md)

[<span data-ttu-id="dd9ad-202">New-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="dd9ad-202">New-AzApiManagementApiRevision</span></span>](./New-AzApiManagementApiRevision.md)

[<span data-ttu-id="dd9ad-203">Remove-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="dd9ad-203">Remove-AzApiManagementApiRevision</span></span>](./Remove-AzApiManagementApiRevision.md)