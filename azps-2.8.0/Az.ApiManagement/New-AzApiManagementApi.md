---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 664CF009-FC52-4F1B-933B-3DEBD05AC8C5
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApi.md
ms.openlocfilehash: b332ccc8dc9188259c897c53256f1a14fd96280e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668077"
---
# <span data-ttu-id="9fc9a-101">New-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="9fc9a-101">New-AzApiManagementApi</span></span>

## <span data-ttu-id="9fc9a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9fc9a-102">SYNOPSIS</span></span>
<span data-ttu-id="9fc9a-103">API-t hoz létre.</span><span class="sxs-lookup"><span data-stu-id="9fc9a-103">Creates an API.</span></span>

## <span data-ttu-id="9fc9a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9fc9a-104">SYNTAX</span></span>

```
New-AzApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>] -Name <String>
 [-Description <String>] -ServiceUrl <String> -Path <String> -Protocols <PsApiManagementSchema[]>
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-OpenIdProviderId <String>]
 [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-ProductIds <String[]>] [-SubscriptionRequired]
 [-ApiVersionDescription <String>] [-ApiVersionSetId <String>] [-ApiVersion <String>] [-SourceApiId <String>]
 [-SourceApiRevision <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9fc9a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9fc9a-105">DESCRIPTION</span></span>
<span data-ttu-id="9fc9a-106">A **New-AzApiManagementApi** parancsmag egy Azure API-kezelési API-t hoz létre.</span><span class="sxs-lookup"><span data-stu-id="9fc9a-106">The **New-AzApiManagementApi** cmdlet creates an Azure API Management API.</span></span>

## <span data-ttu-id="9fc9a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="9fc9a-107">EXAMPLES</span></span>

### <span data-ttu-id="9fc9a-108">Példa 1: API létrehozása</span><span class="sxs-lookup"><span data-stu-id="9fc9a-108">Example 1: Create an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementApi -Context $ApiMgmtContext -Name "Echo api" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @("http", "https") -Path "testapi"
```

<span data-ttu-id="9fc9a-109">A parancs létrehoz egy EchoApi nevű API-t a megadott URL-lel.</span><span class="sxs-lookup"><span data-stu-id="9fc9a-109">This command creates an API named EchoApi with the specified URL.</span></span>

### <span data-ttu-id="9fc9a-110">Példa 1: API létrehozása az összes művelet, címke, termék és házirend másolásával az ECHO-API-ból és egy ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="9fc9a-110">Example 1: Create an API by copying all operation, Tags, Products and Policies from echo-api and into an ApiVersionSet</span></span>
```powershell
PS D:\github\azure-powershell>$context = New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/Api-Default-West-US/providers/Microsoft.ApiManagement/service/contoso
PS D:\github\azure-powershell>$versionSet = Get-AzApiManagementApiVersionSet -Context $context -ApiVersionSetId "xmsVersionSet"
PS D:\github\azure-powershell> New-AzApiManagementApi -Context $context -Name "echoapiv4" -Description "Create Echo Api V4" -SubscriptionRequired -ServiceUrl "https://echoapi.cloudapp.net/v4" -Path "echov3" -Protocols @("http", "https") -ApiVersionSetId $versionSet.ApiVersionSetId -SourceApiId "echo-api" -ApiVersion "v4"


ApiId                         : 691b7d410125414a929c108541c60e06
Name                          : echoapiv4
Description                   : Create Echo Api V4
ServiceUrl                    : https://echoapi.cloudapp.net/v4 
Path                          : echov3
ApiType                       : http
Protocols                     : {Http, Https}
AuthorizationServerId         :
AuthorizationScope            :
OpenidProviderId              :
BearerTokenSendingMethod      : {}
SubscriptionKeyHeaderName     : Ocp-Apim-Subscription-Key
SubscriptionKeyQueryParamName : subscription-key
ApiRevision                   : 1
ApiVersion                    : v4
IsCurrent                     : True
IsOnline                      : False
SubscriptionRequired          : True
ApiRevisionDescription        :
ApiVersionSetDescription      :
ApiVersionSetId               : /subscriptions/subid/resourceGroups/Api-Default-West-US/providers/Microsoft.ApiManagement/service/contoso/apiVersionSets/xmsVersionSet
Id                            : /subscriptions/subid/resourceGroups/Api-Default-West-US/providers/Microsoft.ApiManagement/service/contoso/apis/691b7d410125414a929c108541c60e06    
ResourceGroupName             : Api-Default-West-US
ServiceName                   : contoso
```

<span data-ttu-id="9fc9a-111">Ez a parancs API `echoapiv3` -t hoz létre a ApiVersionSet-ban, `xmsVersionSet` és az összes műveletet, címkét és házirendet a forrás API-ból másolja `echo-api` .</span><span class="sxs-lookup"><span data-stu-id="9fc9a-111">This command creates an API `echoapiv3` in ApiVersionSet `xmsVersionSet` and copies all operation, Tags and Policies from source Api `echo-api`.</span></span> <span data-ttu-id="9fc9a-112">Felülbírálja a SubscriptionRequired, az ServiceUrl, az elérési utat, a protokollokat</span><span class="sxs-lookup"><span data-stu-id="9fc9a-112">It overrides the SubscriptionRequired, ServiceUrl, Path, Protocols</span></span>

## <span data-ttu-id="9fc9a-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9fc9a-113">PARAMETERS</span></span>

### <span data-ttu-id="9fc9a-114">-ApiId</span><span class="sxs-lookup"><span data-stu-id="9fc9a-114">-ApiId</span></span>
<span data-ttu-id="9fc9a-115">A létrehozandó API AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="9fc9a-115">Specifies the ID of the API to create.</span></span>
<span data-ttu-id="9fc9a-116">Ha nem adja meg ezt a paramétert, ez a parancsmag azonosítót hoz létre Önnek.</span><span class="sxs-lookup"><span data-stu-id="9fc9a-116">If you do not specify this parameter, this cmdlet generates an ID for you.</span></span>

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

### <span data-ttu-id="9fc9a-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="9fc9a-117">-ApiVersion</span></span>
<span data-ttu-id="9fc9a-118">A létrehozandó API API-verziója.</span><span class="sxs-lookup"><span data-stu-id="9fc9a-118">Api Version of the Api to create.</span></span> <span data-ttu-id="9fc9a-119">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="9fc9a-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="9fc9a-120">-ApiVersionDescription</span><span class="sxs-lookup"><span data-stu-id="9fc9a-120">-ApiVersionDescription</span></span>
<span data-ttu-id="9fc9a-121">API-verzió leírása.</span><span class="sxs-lookup"><span data-stu-id="9fc9a-121">Api Version Description.</span></span> <span data-ttu-id="9fc9a-122">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="9fc9a-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="9fc9a-123">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="9fc9a-123">-ApiVersionSetId</span></span>
<span data-ttu-id="9fc9a-124">A kapcsolódó API-verzió erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="9fc9a-124">A resource identifier for the related Api Version Set.</span></span> <span data-ttu-id="9fc9a-125">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="9fc9a-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="9fc9a-126">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="9fc9a-126">-AuthorizationScope</span></span>
<span data-ttu-id="9fc9a-127">A OAuth-műveletek hatókörét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9fc9a-127">Specifies the OAuth operations scope.</span></span>
<span data-ttu-id="9fc9a-128">Az alapértelmezett érték $Null.</span><span class="sxs-lookup"><span data-stu-id="9fc9a-128">The default value is $Null.</span></span>

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

### <span data-ttu-id="9fc9a-129">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="9fc9a-129">-AuthorizationServerId</span></span>
<span data-ttu-id="9fc9a-130">A OAuth-engedélyezési kiszolgáló AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="9fc9a-130">Specifies the OAuth authorization server ID.</span></span>
<span data-ttu-id="9fc9a-131">Az alapértelmezett érték $Null.</span><span class="sxs-lookup"><span data-stu-id="9fc9a-131">The default value is $Null.</span></span>
<span data-ttu-id="9fc9a-132">Ezt a paramétert akkor kell megadnia, ha a *AuthorizationScope* meg van adva.</span><span class="sxs-lookup"><span data-stu-id="9fc9a-132">You must specify this parameter if *AuthorizationScope* is specified.</span></span>

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

### <span data-ttu-id="9fc9a-133">-BearerTokenSendingMethod</span><span class="sxs-lookup"><span data-stu-id="9fc9a-133">-BearerTokenSendingMethod</span></span>
<span data-ttu-id="9fc9a-134">Az OpenId engedélyezési kiszolgáló mechanizmusa, amellyel az Access-tokent átadták az API-nek.</span><span class="sxs-lookup"><span data-stu-id="9fc9a-134">OpenId authorization server mechanism by which access token is passed to the API.</span></span> <span data-ttu-id="9fc9a-135">Lásd: http://tools.ietf.org/html/rfc6749#section-4 .</span><span class="sxs-lookup"><span data-stu-id="9fc9a-135">Refer to http://tools.ietf.org/html/rfc6749#section-4.</span></span> <span data-ttu-id="9fc9a-136">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="9fc9a-136">This parameter is optional.</span></span> <span data-ttu-id="9fc9a-137">Az alapértelmezett érték $null.</span><span class="sxs-lookup"><span data-stu-id="9fc9a-137">Default value is $null.</span></span>

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

### <span data-ttu-id="9fc9a-138">-Környezet</span><span class="sxs-lookup"><span data-stu-id="9fc9a-138">-Context</span></span>
<span data-ttu-id="9fc9a-139">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="9fc9a-139">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9fc9a-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fc9a-140">-DefaultProfile</span></span>
<span data-ttu-id="9fc9a-141">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9fc9a-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9fc9a-142">-Leírás</span><span class="sxs-lookup"><span data-stu-id="9fc9a-142">-Description</span></span>
<span data-ttu-id="9fc9a-143">A webes API leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="9fc9a-143">Specifies a description for the web API.</span></span>

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

### <span data-ttu-id="9fc9a-144">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9fc9a-144">-Name</span></span>
<span data-ttu-id="9fc9a-145">A webes API nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9fc9a-145">Specifies the name of the web API.</span></span>
<span data-ttu-id="9fc9a-146">Ez az API nyilvános neve a fejlesztői és a rendszergazdai portálon.</span><span class="sxs-lookup"><span data-stu-id="9fc9a-146">This is the public name of the API as it appears on the developer and admin portals.</span></span>

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

### <span data-ttu-id="9fc9a-147">-OpenIdProviderId</span><span class="sxs-lookup"><span data-stu-id="9fc9a-147">-OpenIdProviderId</span></span>
<span data-ttu-id="9fc9a-148">OpenId engedélyezési kiszolgáló azonosítója</span><span class="sxs-lookup"><span data-stu-id="9fc9a-148">OpenId authorization server identifier.</span></span> <span data-ttu-id="9fc9a-149">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="9fc9a-149">This parameter is optional.</span></span> <span data-ttu-id="9fc9a-150">Az alapértelmezett érték $null.</span><span class="sxs-lookup"><span data-stu-id="9fc9a-150">Default value is $null.</span></span> <span data-ttu-id="9fc9a-151">Meg kell adni, ha a BearerTokenSendingMethods meg van adva.</span><span class="sxs-lookup"><span data-stu-id="9fc9a-151">Must be specified if BearerTokenSendingMethods is specified.</span></span>

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

### <span data-ttu-id="9fc9a-152">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="9fc9a-152">-Path</span></span>
<span data-ttu-id="9fc9a-153">A webes API elérési útvonalát adja meg, amely az API nyilvános URL-címe utolsó része, és a felügyeleti portál webapi URL-utótag mezőjének felel meg.</span><span class="sxs-lookup"><span data-stu-id="9fc9a-153">Specifies the web API path, which is the last part of the API's public URL and corresponds to the Web API URL suffix field in the admin portal.</span></span>
<span data-ttu-id="9fc9a-154">Ezt az URL-címet használják az API-felhasználóknak a kérések webszolgáltatáshoz való küldéséhez, és egy-egy 400 karakter hosszúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="9fc9a-154">This URL is used by API consumers to send requests to the web service, and must be one to 400 characters long.</span></span>
<span data-ttu-id="9fc9a-155">Az alapértelmezett érték $Null.</span><span class="sxs-lookup"><span data-stu-id="9fc9a-155">The default value is $Null.</span></span>

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

### <span data-ttu-id="9fc9a-156">-Termékkód</span><span class="sxs-lookup"><span data-stu-id="9fc9a-156">-ProductIds</span></span>
<span data-ttu-id="9fc9a-157">Az új API hozzáadására szolgáló termékazonosítók tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9fc9a-157">Specifies an array of product IDs to which to add the new API.</span></span>

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

### <span data-ttu-id="9fc9a-158">-Protokollok</span><span class="sxs-lookup"><span data-stu-id="9fc9a-158">-Protocols</span></span>
<span data-ttu-id="9fc9a-159">A webes API-protokollok tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9fc9a-159">Specifies an array of web API protocols.</span></span>
<span data-ttu-id="9fc9a-160">Érvényes értékek: http, HTTPS.</span><span class="sxs-lookup"><span data-stu-id="9fc9a-160">Valid values are http, https.</span></span>
<span data-ttu-id="9fc9a-161">Ezek azok a webes protokollok, amelyek az API-t elérhetővé tették.</span><span class="sxs-lookup"><span data-stu-id="9fc9a-161">These are the web protocols over which the API is made available.</span></span>
<span data-ttu-id="9fc9a-162">Az alapértelmezett érték $Null.</span><span class="sxs-lookup"><span data-stu-id="9fc9a-162">The default value is $Null.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]
Parameter Sets: (All)
Aliases:
Accepted values: Http, Https

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fc9a-163">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="9fc9a-163">-ServiceUrl</span></span>
<span data-ttu-id="9fc9a-164">Annak a webszolgáltatásnak az URL-címe, amely kiteszi az API-t.</span><span class="sxs-lookup"><span data-stu-id="9fc9a-164">Specifies the URL of the web service that exposes the API.</span></span>
<span data-ttu-id="9fc9a-165">Ezt az URL-címet csak az Azure API-kezelés használja, és nem jelenik meg nyilvánosan.</span><span class="sxs-lookup"><span data-stu-id="9fc9a-165">This URL is used only by Azure API Management, and is not made public.</span></span>
<span data-ttu-id="9fc9a-166">Az URL-címnek egy 2000 karakter hosszúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="9fc9a-166">The URL must be one to 2000 characters long.</span></span>

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

### <span data-ttu-id="9fc9a-167">-SourceApiId</span><span class="sxs-lookup"><span data-stu-id="9fc9a-167">-SourceApiId</span></span>
<span data-ttu-id="9fc9a-168">A forrás API API-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="9fc9a-168">Api identifier of the source API.</span></span> <span data-ttu-id="9fc9a-169">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="9fc9a-169">This parameter is optional.</span></span>

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

### <span data-ttu-id="9fc9a-170">-SourceApiRevision</span><span class="sxs-lookup"><span data-stu-id="9fc9a-170">-SourceApiRevision</span></span>
<span data-ttu-id="9fc9a-171">A forrás API API-verziója.</span><span class="sxs-lookup"><span data-stu-id="9fc9a-171">Api Revision of the source API.</span></span> <span data-ttu-id="9fc9a-172">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="9fc9a-172">This parameter is optional.</span></span>

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

### <span data-ttu-id="9fc9a-173">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="9fc9a-173">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="9fc9a-174">Az előfizetés kulcs fejlécének nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9fc9a-174">Specifies the subscription key header name.</span></span>
<span data-ttu-id="9fc9a-175">Az alapértelmezett érték $Null.</span><span class="sxs-lookup"><span data-stu-id="9fc9a-175">The default value is $Null.</span></span>

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

### <span data-ttu-id="9fc9a-176">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="9fc9a-176">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="9fc9a-177">Az előfizetési kulcs lekérdezési karakterláncának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9fc9a-177">Specifies the subscription key query string parameter name.</span></span>
<span data-ttu-id="9fc9a-178">Az alapértelmezett érték $Null.</span><span class="sxs-lookup"><span data-stu-id="9fc9a-178">The default value is $Null.</span></span>

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

### <span data-ttu-id="9fc9a-179">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="9fc9a-179">-SubscriptionRequired</span></span>
<span data-ttu-id="9fc9a-180">Megjelölés az API-SubscriptionRequired vonatkozó kérelmek érvényesítéséhez.</span><span class="sxs-lookup"><span data-stu-id="9fc9a-180">Flag to enforce SubscriptionRequired for requests to the Api.</span></span> <span data-ttu-id="9fc9a-181">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="9fc9a-181">This parameter is optional.</span></span>

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

### <span data-ttu-id="9fc9a-182">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fc9a-182">CommonParameters</span></span>
<span data-ttu-id="9fc9a-183">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9fc9a-183">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fc9a-184">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="9fc9a-184">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fc9a-185">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9fc9a-185">INPUTS</span></span>

### <span data-ttu-id="9fc9a-186">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="9fc9a-186">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="9fc9a-187">System. String</span><span class="sxs-lookup"><span data-stu-id="9fc9a-187">System.String</span></span>

### <span data-ttu-id="9fc9a-188">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementSchema []</span><span class="sxs-lookup"><span data-stu-id="9fc9a-188">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="9fc9a-189">System. string []</span><span class="sxs-lookup"><span data-stu-id="9fc9a-189">System.String[]</span></span>

## <span data-ttu-id="9fc9a-190">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9fc9a-190">OUTPUTS</span></span>

### <span data-ttu-id="9fc9a-191">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="9fc9a-191">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="9fc9a-192">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9fc9a-192">NOTES</span></span>

## <span data-ttu-id="9fc9a-193">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9fc9a-193">RELATED LINKS</span></span>

[<span data-ttu-id="9fc9a-194">Exportálás – AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="9fc9a-194">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="9fc9a-195">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="9fc9a-195">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="9fc9a-196">Importálás – AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="9fc9a-196">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="9fc9a-197">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="9fc9a-197">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="9fc9a-198">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="9fc9a-198">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


