---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementapirevision
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiRevision.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiRevision.md
ms.openlocfilehash: e7074b799e1c664ceb17499b04b8d4d2ff3acb5d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013864"
---
# <span data-ttu-id="24147-101">Set-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="24147-101">Set-AzApiManagementApiRevision</span></span>

## <span data-ttu-id="24147-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="24147-102">SYNOPSIS</span></span>
<span data-ttu-id="24147-103">API-módosítás módosítása</span><span class="sxs-lookup"><span data-stu-id="24147-103">Modifies an API Revision</span></span>

## <span data-ttu-id="24147-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="24147-104">SYNTAX</span></span>

### <span data-ttu-id="24147-105">ExpandedParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="24147-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementApiRevision -ApiRevision <String> -Context <PsApiManagementContext> -ApiId <String>
 [-Name <String>] [-Description <String>] [-ServiceUrl <String>] [-Path <String>]
 [-Protocols <PsApiManagementSchema[]>] [-AuthorizationServerId <String>] [-AuthorizationScope <String>]
 [-OpenIdProviderId <String>] [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-SubscriptionRequired] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24147-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="24147-106">ByInputObject</span></span>
```
Set-AzApiManagementApiRevision -InputObject <PsApiManagementApi> [-Name <String>] [-Description <String>]
 [-ServiceUrl <String>] [-Path <String>] [-Protocols <PsApiManagementSchema[]>]
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-OpenIdProviderId <String>]
 [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-SubscriptionRequired] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24147-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="24147-107">DESCRIPTION</span></span>
<span data-ttu-id="24147-108">A **set-AzApiManagementApiRevision** parancsmag egy Azure API-kezelési API-módosítást módosít.</span><span class="sxs-lookup"><span data-stu-id="24147-108">The **Set-AzApiManagementApiRevision** cmdlet modifies an Azure API Management API Revision.</span></span>

## <span data-ttu-id="24147-109">Példák</span><span class="sxs-lookup"><span data-stu-id="24147-109">EXAMPLES</span></span>

### <span data-ttu-id="24147-110">Példa 1 API-módosítás módosítása</span><span class="sxs-lookup"><span data-stu-id="24147-110">Example 1 Modify an API Revision</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementApiRevision -Context $ApiMgmtContext -ApiId "echo-api" -ApiRevision "2" -Name "EchoApi" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @('https') -Description "Responds with what was sent" -Path "echo"
```

<span data-ttu-id="24147-111">A parancsmag frissíti az `2` API `echo-api` új leírását, protokollját és elérési útját.</span><span class="sxs-lookup"><span data-stu-id="24147-111">The cmdlet updates the `2` revision of the API `echo-api` with a new description, protocol and path.</span></span>

## <span data-ttu-id="24147-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="24147-112">PARAMETERS</span></span>

### <span data-ttu-id="24147-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="24147-113">-ApiId</span></span>
<span data-ttu-id="24147-114">A meglévő API-azonosító.</span><span class="sxs-lookup"><span data-stu-id="24147-114">Identifier of existing API.</span></span>
<span data-ttu-id="24147-115">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="24147-115">This parameter is required.</span></span>

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

### <span data-ttu-id="24147-116">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="24147-116">-ApiRevision</span></span>
<span data-ttu-id="24147-117">A meglévő API-verzió verziószámának azonosítója</span><span class="sxs-lookup"><span data-stu-id="24147-117">Identifier of existing API Revision.</span></span> <span data-ttu-id="24147-118">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="24147-118">This parameter is required.</span></span>

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

### <span data-ttu-id="24147-119">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="24147-119">-AuthorizationScope</span></span>
<span data-ttu-id="24147-120">OAuth-műveletek hatóköre</span><span class="sxs-lookup"><span data-stu-id="24147-120">OAuth operations scope.</span></span>
<span data-ttu-id="24147-121">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="24147-121">This parameter is optional.</span></span>
<span data-ttu-id="24147-122">Az alapértelmezett érték $null.</span><span class="sxs-lookup"><span data-stu-id="24147-122">Default value is $null.</span></span>

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

### <span data-ttu-id="24147-123">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="24147-123">-AuthorizationServerId</span></span>
<span data-ttu-id="24147-124">OAuth-engedélyezési kiszolgáló azonosítója</span><span class="sxs-lookup"><span data-stu-id="24147-124">OAuth authorization server identifier.</span></span>
<span data-ttu-id="24147-125">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="24147-125">This parameter is optional.</span></span>
<span data-ttu-id="24147-126">Az alapértelmezett érték $null.</span><span class="sxs-lookup"><span data-stu-id="24147-126">Default value is $null.</span></span>
<span data-ttu-id="24147-127">Meg kell adni, ha a AuthorizationScope meg van adva.</span><span class="sxs-lookup"><span data-stu-id="24147-127">Must be specified if AuthorizationScope specified.</span></span>

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

### <span data-ttu-id="24147-128">-BearerTokenSendingMethod</span><span class="sxs-lookup"><span data-stu-id="24147-128">-BearerTokenSendingMethod</span></span>
<span data-ttu-id="24147-129">Az OpenId engedélyezési kiszolgáló mechanizmusa, amellyel az Access-tokent átadták az API-nek.</span><span class="sxs-lookup"><span data-stu-id="24147-129">OpenId authorization server mechanism by which access token is passed to the API.</span></span> <span data-ttu-id="24147-130">Lásd: http://tools.ietf.org/html/rfc6749#section-4 .</span><span class="sxs-lookup"><span data-stu-id="24147-130">Refer to http://tools.ietf.org/html/rfc6749#section-4.</span></span> <span data-ttu-id="24147-131">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="24147-131">This parameter is optional.</span></span> <span data-ttu-id="24147-132">Az alapértelmezett érték $null.</span><span class="sxs-lookup"><span data-stu-id="24147-132">Default value is $null.</span></span>

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

### <span data-ttu-id="24147-133">-Környezet</span><span class="sxs-lookup"><span data-stu-id="24147-133">-Context</span></span>
<span data-ttu-id="24147-134">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="24147-134">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="24147-135">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="24147-135">This parameter is required.</span></span>

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

### <span data-ttu-id="24147-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24147-136">-DefaultProfile</span></span>
<span data-ttu-id="24147-137">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="24147-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24147-138">-Leírás</span><span class="sxs-lookup"><span data-stu-id="24147-138">-Description</span></span>
<span data-ttu-id="24147-139">Webes API leírása.</span><span class="sxs-lookup"><span data-stu-id="24147-139">Web API description.</span></span>
<span data-ttu-id="24147-140">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="24147-140">This parameter is optional.</span></span>

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

### <span data-ttu-id="24147-141">-InputObject</span><span class="sxs-lookup"><span data-stu-id="24147-141">-InputObject</span></span>
<span data-ttu-id="24147-142">A PsApiManagementApi példánya.</span><span class="sxs-lookup"><span data-stu-id="24147-142">Instance of PsApiManagementApi.</span></span> <span data-ttu-id="24147-143">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="24147-143">This parameter is required.</span></span>

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

### <span data-ttu-id="24147-144">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="24147-144">-Name</span></span>
<span data-ttu-id="24147-145">Web API-név.</span><span class="sxs-lookup"><span data-stu-id="24147-145">Web API name.</span></span>
<span data-ttu-id="24147-146">Az API-t a fejlesztői és a felügyeleti portálokon megjelenő nyilvános név.</span><span class="sxs-lookup"><span data-stu-id="24147-146">Public name of the API as it would appear on the developer and admin portals.</span></span>
<span data-ttu-id="24147-147">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="24147-147">This parameter is required.</span></span>

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

### <span data-ttu-id="24147-148">-OpenIdProviderId</span><span class="sxs-lookup"><span data-stu-id="24147-148">-OpenIdProviderId</span></span>
<span data-ttu-id="24147-149">OpenId engedélyezési kiszolgáló azonosítója</span><span class="sxs-lookup"><span data-stu-id="24147-149">OpenId authorization server identifier.</span></span> <span data-ttu-id="24147-150">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="24147-150">This parameter is optional.</span></span> <span data-ttu-id="24147-151">Az alapértelmezett érték $null.</span><span class="sxs-lookup"><span data-stu-id="24147-151">Default value is $null.</span></span> <span data-ttu-id="24147-152">Meg kell adni, ha a BearerTokenSendingMethods meg van adva.</span><span class="sxs-lookup"><span data-stu-id="24147-152">Must be specified if BearerTokenSendingMethods is specified.</span></span>

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

### <span data-ttu-id="24147-153">-PassThru</span><span class="sxs-lookup"><span data-stu-id="24147-153">-PassThru</span></span>
<span data-ttu-id="24147-154">Ha meg van adva, akkor a Microsoft. Azure. commands. ApiManagement. ServiceManagement. models. PsApiManagementApi típusa a set API-t jelképezi.</span><span class="sxs-lookup"><span data-stu-id="24147-154">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi type representing the set API.</span></span>

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

### <span data-ttu-id="24147-155">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="24147-155">-Path</span></span>
<span data-ttu-id="24147-156">Web API-elérési út.</span><span class="sxs-lookup"><span data-stu-id="24147-156">Web API Path.</span></span>
<span data-ttu-id="24147-157">Az API nyilvános URL-címének utolsó része.</span><span class="sxs-lookup"><span data-stu-id="24147-157">Last part of the API's public URL.</span></span>
<span data-ttu-id="24147-158">Ezt az URL-címet az API-felhasználók fogják használni a webszolgáltatásra irányuló kérések elküldéséhez.</span><span class="sxs-lookup"><span data-stu-id="24147-158">This URL will be used by API consumers for sending requests to the web service.</span></span>
<span data-ttu-id="24147-159">1 – 400 karakter hosszúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="24147-159">Must be 1 to 400 characters long.</span></span>
<span data-ttu-id="24147-160">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="24147-160">This parameter is optional.</span></span>
<span data-ttu-id="24147-161">Az alapértelmezett érték $null.</span><span class="sxs-lookup"><span data-stu-id="24147-161">Default value is $null.</span></span>

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

### <span data-ttu-id="24147-162">-Protokollok</span><span class="sxs-lookup"><span data-stu-id="24147-162">-Protocols</span></span>
<span data-ttu-id="24147-163">Webes API-protokollok (http, HTTPS).</span><span class="sxs-lookup"><span data-stu-id="24147-163">Web API protocols (http, https).</span></span>
<span data-ttu-id="24147-164">Azok a protokollok, amelyek az API-t elérhetővé tették.</span><span class="sxs-lookup"><span data-stu-id="24147-164">Protocols over which API is made available.</span></span>
<span data-ttu-id="24147-165">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="24147-165">This parameter is required.</span></span>
<span data-ttu-id="24147-166">Az alapértelmezett érték $null.</span><span class="sxs-lookup"><span data-stu-id="24147-166">Default value is $null.</span></span>

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

### <span data-ttu-id="24147-167">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="24147-167">-ServiceUrl</span></span>
<span data-ttu-id="24147-168">A webszolgáltatás URL-címe kiteszi az API-t.</span><span class="sxs-lookup"><span data-stu-id="24147-168">A URL of the web service exposing the API.</span></span>
<span data-ttu-id="24147-169">Ezt az URL-címet csak az Azure API-kezelés fogja használni, és ezek nem lesznek nyilvánosan elérhetők.</span><span class="sxs-lookup"><span data-stu-id="24147-169">This URL will be used by Azure API Management only, and will not be made public.</span></span>
<span data-ttu-id="24147-170">1 – 2000 karakter hosszúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="24147-170">Must be 1 to 2000 characters long.</span></span>
<span data-ttu-id="24147-171">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="24147-171">This parameter is required.</span></span>

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

### <span data-ttu-id="24147-172">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="24147-172">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="24147-173">Az előfizetés kulcs fejlécének neve.</span><span class="sxs-lookup"><span data-stu-id="24147-173">Subscription key header name.</span></span>
<span data-ttu-id="24147-174">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="24147-174">This parameter is optional.</span></span>
<span data-ttu-id="24147-175">Az alapértelmezett érték $null.</span><span class="sxs-lookup"><span data-stu-id="24147-175">Default value is $null.</span></span>

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

### <span data-ttu-id="24147-176">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="24147-176">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="24147-177">Az előfizetés kulcs lekérdezése karakterlánc paraméterének neve.</span><span class="sxs-lookup"><span data-stu-id="24147-177">Subscription key query string parameter name.</span></span>
<span data-ttu-id="24147-178">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="24147-178">This parameter is optional.</span></span>
<span data-ttu-id="24147-179">Az alapértelmezett érték $null.</span><span class="sxs-lookup"><span data-stu-id="24147-179">Default value is $null.</span></span>

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

### <span data-ttu-id="24147-180">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="24147-180">-SubscriptionRequired</span></span>
<span data-ttu-id="24147-181">Megjelölés az API-SubscriptionRequired vonatkozó kérelmek érvényesítéséhez.</span><span class="sxs-lookup"><span data-stu-id="24147-181">Flag to enforce SubscriptionRequired for requests to the Api.</span></span> <span data-ttu-id="24147-182">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="24147-182">This parameter is optional.</span></span>

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

### <span data-ttu-id="24147-183">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="24147-183">-Confirm</span></span>
<span data-ttu-id="24147-184">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="24147-184">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24147-185">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24147-185">-WhatIf</span></span>
<span data-ttu-id="24147-186">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="24147-186">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24147-187">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="24147-187">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24147-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24147-188">CommonParameters</span></span>
<span data-ttu-id="24147-189">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="24147-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24147-190">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="24147-190">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24147-191">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="24147-191">INPUTS</span></span>

### <span data-ttu-id="24147-192">System. String</span><span class="sxs-lookup"><span data-stu-id="24147-192">System.String</span></span>

### <span data-ttu-id="24147-193">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="24147-193">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="24147-194">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="24147-194">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

### <span data-ttu-id="24147-195">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementSchema []</span><span class="sxs-lookup"><span data-stu-id="24147-195">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="24147-196">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="24147-196">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="24147-197">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="24147-197">OUTPUTS</span></span>

### <span data-ttu-id="24147-198">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="24147-198">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="24147-199">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="24147-199">NOTES</span></span>

## <span data-ttu-id="24147-200">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="24147-200">RELATED LINKS</span></span>

[<span data-ttu-id="24147-201">Get-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="24147-201">Get-AzApiManagementApiRevision</span></span>](./Get-AzApiManagementApiRevision.md)

[<span data-ttu-id="24147-202">Új – AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="24147-202">New-AzApiManagementApiRevision</span></span>](./New-AzApiManagementApiRevision.md)

[<span data-ttu-id="24147-203">Remove-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="24147-203">Remove-AzApiManagementApiRevision</span></span>](./Remove-AzApiManagementApiRevision.md)