---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 664CF009-FC52-4F1B-933B-3DEBD05AC8C5
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApi.md
ms.openlocfilehash: 3312c725d63bcb42aab7d82144c5a8f6f8e67641
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024955"
---
# <span data-ttu-id="6f8b5-101">New-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="6f8b5-101">New-AzApiManagementApi</span></span>

## <span data-ttu-id="6f8b5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6f8b5-102">SYNOPSIS</span></span>
<span data-ttu-id="6f8b5-103">API-t hoz létre.</span><span class="sxs-lookup"><span data-stu-id="6f8b5-103">Creates an API.</span></span>

## <span data-ttu-id="6f8b5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6f8b5-104">SYNTAX</span></span>

```
New-AzApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>] -Name <String>
 [-Description <String>] -ServiceUrl <String> -Path <String> -Protocols <PsApiManagementSchema[]>
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-OpenIdProviderId <String>]
 [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-ProductIds <String[]>] [-SubscriptionRequired]
 [-ApiVersionDescription <String>] [-ApiVersionSetId <String>] [-ApiVersion <String>] [-SourceApiId <String>]
 [-SourceApiRevision <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6f8b5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6f8b5-105">DESCRIPTION</span></span>
<span data-ttu-id="6f8b5-106">A **New-AzApiManagementApi** parancsmag egy Azure API-kezelési API-t hoz létre.</span><span class="sxs-lookup"><span data-stu-id="6f8b5-106">The **New-AzApiManagementApi** cmdlet creates an Azure API Management API.</span></span>

## <span data-ttu-id="6f8b5-107">Példák</span><span class="sxs-lookup"><span data-stu-id="6f8b5-107">EXAMPLES</span></span>

### <span data-ttu-id="6f8b5-108">Példa 1: API létrehozása</span><span class="sxs-lookup"><span data-stu-id="6f8b5-108">Example 1: Create an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementApi -Context $ApiMgmtContext -Name "Echo api" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @("http", "https") -Path "testapi"
```

<span data-ttu-id="6f8b5-109">A parancs létrehoz egy EchoApi nevű API-t a megadott URL-lel.</span><span class="sxs-lookup"><span data-stu-id="6f8b5-109">This command creates an API named EchoApi with the specified URL.</span></span>

### <span data-ttu-id="6f8b5-110">2. példa: hozzon létre egy API-t, ha az összes műveletet, címkét, terméket és házirendet az ECHO-API-ból és egy ApiVersionSet másolja.</span><span class="sxs-lookup"><span data-stu-id="6f8b5-110">Example 2: Create an API by copying all operation, Tags, Products and Policies from echo-api and into an ApiVersionSet</span></span>
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

<span data-ttu-id="6f8b5-111">Ez a parancs API `echoapiv3` -t hoz létre a ApiVersionSet-ban, `xmsVersionSet` és az összes műveletet, címkét és házirendet a forrás API-ból másolja `echo-api` .</span><span class="sxs-lookup"><span data-stu-id="6f8b5-111">This command creates an API `echoapiv3` in ApiVersionSet `xmsVersionSet` and copies all operation, Tags and Policies from source Api `echo-api`.</span></span> <span data-ttu-id="6f8b5-112">Felülbírálja a SubscriptionRequired, az ServiceUrl, az elérési utat, a protokollokat</span><span class="sxs-lookup"><span data-stu-id="6f8b5-112">It overrides the SubscriptionRequired, ServiceUrl, Path, Protocols</span></span>

### <span data-ttu-id="6f8b5-113">3. példa</span><span class="sxs-lookup"><span data-stu-id="6f8b5-113">Example 3</span></span>

<span data-ttu-id="6f8b5-114">API-t hoz létre.</span><span class="sxs-lookup"><span data-stu-id="6f8b5-114">Creates an API.</span></span> <span data-ttu-id="6f8b5-115">autogenerated</span><span class="sxs-lookup"><span data-stu-id="6f8b5-115">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
New-AzApiManagementApi -ApiId '0001' -Context <PsApiManagementContext> -Name 'Echo api' -Path 'echov3' -Protocols Http -ServiceUrl 'https://contoso.com/apis/echo'
```

## <span data-ttu-id="6f8b5-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6f8b5-116">PARAMETERS</span></span>

### <span data-ttu-id="6f8b5-117">-ApiId</span><span class="sxs-lookup"><span data-stu-id="6f8b5-117">-ApiId</span></span>
<span data-ttu-id="6f8b5-118">A létrehozandó API AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="6f8b5-118">Specifies the ID of the API to create.</span></span>
<span data-ttu-id="6f8b5-119">Ha nem adja meg ezt a paramétert, ez a parancsmag azonosítót hoz létre Önnek.</span><span class="sxs-lookup"><span data-stu-id="6f8b5-119">If you do not specify this parameter, this cmdlet generates an ID for you.</span></span>

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

### <span data-ttu-id="6f8b5-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="6f8b5-120">-ApiVersion</span></span>
<span data-ttu-id="6f8b5-121">A létrehozandó API API-verziója.</span><span class="sxs-lookup"><span data-stu-id="6f8b5-121">Api Version of the Api to create.</span></span> <span data-ttu-id="6f8b5-122">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="6f8b5-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="6f8b5-123">-ApiVersionDescription</span><span class="sxs-lookup"><span data-stu-id="6f8b5-123">-ApiVersionDescription</span></span>
<span data-ttu-id="6f8b5-124">API-verzió leírása.</span><span class="sxs-lookup"><span data-stu-id="6f8b5-124">Api Version Description.</span></span> <span data-ttu-id="6f8b5-125">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="6f8b5-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="6f8b5-126">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="6f8b5-126">-ApiVersionSetId</span></span>
<span data-ttu-id="6f8b5-127">A kapcsolódó API-verzió erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="6f8b5-127">A resource identifier for the related Api Version Set.</span></span> <span data-ttu-id="6f8b5-128">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="6f8b5-128">This parameter is optional.</span></span>

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

### <span data-ttu-id="6f8b5-129">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="6f8b5-129">-AuthorizationScope</span></span>
<span data-ttu-id="6f8b5-130">A OAuth-műveletek hatókörét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6f8b5-130">Specifies the OAuth operations scope.</span></span>
<span data-ttu-id="6f8b5-131">Az alapértelmezett érték $Null.</span><span class="sxs-lookup"><span data-stu-id="6f8b5-131">The default value is $Null.</span></span>

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

### <span data-ttu-id="6f8b5-132">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="6f8b5-132">-AuthorizationServerId</span></span>
<span data-ttu-id="6f8b5-133">A OAuth-engedélyezési kiszolgáló AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="6f8b5-133">Specifies the OAuth authorization server ID.</span></span>
<span data-ttu-id="6f8b5-134">Az alapértelmezett érték $Null.</span><span class="sxs-lookup"><span data-stu-id="6f8b5-134">The default value is $Null.</span></span>
<span data-ttu-id="6f8b5-135">Ezt a paramétert akkor kell megadnia, ha a *AuthorizationScope* meg van adva.</span><span class="sxs-lookup"><span data-stu-id="6f8b5-135">You must specify this parameter if *AuthorizationScope* is specified.</span></span>

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

### <span data-ttu-id="6f8b5-136">-BearerTokenSendingMethod</span><span class="sxs-lookup"><span data-stu-id="6f8b5-136">-BearerTokenSendingMethod</span></span>
<span data-ttu-id="6f8b5-137">Az OpenId engedélyezési kiszolgáló mechanizmusa, amellyel az Access-tokent átadták az API-nek.</span><span class="sxs-lookup"><span data-stu-id="6f8b5-137">OpenId authorization server mechanism by which access token is passed to the API.</span></span> <span data-ttu-id="6f8b5-138">Lásd: http://tools.ietf.org/html/rfc6749#section-4 .</span><span class="sxs-lookup"><span data-stu-id="6f8b5-138">Refer to http://tools.ietf.org/html/rfc6749#section-4.</span></span> <span data-ttu-id="6f8b5-139">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="6f8b5-139">This parameter is optional.</span></span> <span data-ttu-id="6f8b5-140">Az alapértelmezett érték $null.</span><span class="sxs-lookup"><span data-stu-id="6f8b5-140">Default value is $null.</span></span>

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

### <span data-ttu-id="6f8b5-141">-Környezet</span><span class="sxs-lookup"><span data-stu-id="6f8b5-141">-Context</span></span>
<span data-ttu-id="6f8b5-142">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="6f8b5-142">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="6f8b5-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f8b5-143">-DefaultProfile</span></span>
<span data-ttu-id="6f8b5-144">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6f8b5-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6f8b5-145">-Leírás</span><span class="sxs-lookup"><span data-stu-id="6f8b5-145">-Description</span></span>
<span data-ttu-id="6f8b5-146">A webes API leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="6f8b5-146">Specifies a description for the web API.</span></span>

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

### <span data-ttu-id="6f8b5-147">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6f8b5-147">-Name</span></span>
<span data-ttu-id="6f8b5-148">A webes API nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6f8b5-148">Specifies the name of the web API.</span></span>
<span data-ttu-id="6f8b5-149">Ez az API nyilvános neve a fejlesztői és a rendszergazdai portálon.</span><span class="sxs-lookup"><span data-stu-id="6f8b5-149">This is the public name of the API as it appears on the developer and admin portals.</span></span>

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

### <span data-ttu-id="6f8b5-150">-OpenIdProviderId</span><span class="sxs-lookup"><span data-stu-id="6f8b5-150">-OpenIdProviderId</span></span>
<span data-ttu-id="6f8b5-151">OpenId engedélyezési kiszolgáló azonosítója</span><span class="sxs-lookup"><span data-stu-id="6f8b5-151">OpenId authorization server identifier.</span></span> <span data-ttu-id="6f8b5-152">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="6f8b5-152">This parameter is optional.</span></span> <span data-ttu-id="6f8b5-153">Az alapértelmezett érték $null.</span><span class="sxs-lookup"><span data-stu-id="6f8b5-153">Default value is $null.</span></span> <span data-ttu-id="6f8b5-154">Meg kell adni, ha a BearerTokenSendingMethods meg van adva.</span><span class="sxs-lookup"><span data-stu-id="6f8b5-154">Must be specified if BearerTokenSendingMethods is specified.</span></span>

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

### <span data-ttu-id="6f8b5-155">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="6f8b5-155">-Path</span></span>
<span data-ttu-id="6f8b5-156">A webes API elérési útvonalát adja meg, amely az API nyilvános URL-címe utolsó része, és a felügyeleti portál webapi URL-utótag mezőjének felel meg.</span><span class="sxs-lookup"><span data-stu-id="6f8b5-156">Specifies the web API path, which is the last part of the API's public URL and corresponds to the Web API URL suffix field in the admin portal.</span></span>
<span data-ttu-id="6f8b5-157">Ezt az URL-címet használják az API-felhasználóknak a kérések webszolgáltatáshoz való küldéséhez, és egy-egy 400 karakter hosszúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="6f8b5-157">This URL is used by API consumers to send requests to the web service, and must be one to 400 characters long.</span></span>
<span data-ttu-id="6f8b5-158">Az alapértelmezett érték $Null.</span><span class="sxs-lookup"><span data-stu-id="6f8b5-158">The default value is $Null.</span></span>

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

### <span data-ttu-id="6f8b5-159">-Termékkód</span><span class="sxs-lookup"><span data-stu-id="6f8b5-159">-ProductIds</span></span>
<span data-ttu-id="6f8b5-160">Az új API hozzáadására szolgáló termékazonosítók tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6f8b5-160">Specifies an array of product IDs to which to add the new API.</span></span>

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

### <span data-ttu-id="6f8b5-161">-Protokollok</span><span class="sxs-lookup"><span data-stu-id="6f8b5-161">-Protocols</span></span>
<span data-ttu-id="6f8b5-162">A webes API-protokollok tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6f8b5-162">Specifies an array of web API protocols.</span></span>
<span data-ttu-id="6f8b5-163">Érvényes értékek: http, HTTPS.</span><span class="sxs-lookup"><span data-stu-id="6f8b5-163">Valid values are http, https.</span></span>
<span data-ttu-id="6f8b5-164">Ezek azok a webes protokollok, amelyek az API-t elérhetővé tették.</span><span class="sxs-lookup"><span data-stu-id="6f8b5-164">These are the web protocols over which the API is made available.</span></span>
<span data-ttu-id="6f8b5-165">Az alapértelmezett érték $Null.</span><span class="sxs-lookup"><span data-stu-id="6f8b5-165">The default value is $Null.</span></span>

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

### <span data-ttu-id="6f8b5-166">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="6f8b5-166">-ServiceUrl</span></span>
<span data-ttu-id="6f8b5-167">Annak a webszolgáltatásnak az URL-címe, amely kiteszi az API-t.</span><span class="sxs-lookup"><span data-stu-id="6f8b5-167">Specifies the URL of the web service that exposes the API.</span></span>
<span data-ttu-id="6f8b5-168">Ezt az URL-címet csak az Azure API-kezelés használja, és nem jelenik meg nyilvánosan.</span><span class="sxs-lookup"><span data-stu-id="6f8b5-168">This URL is used only by Azure API Management, and is not made public.</span></span>
<span data-ttu-id="6f8b5-169">Az URL-címnek egy 2000 karakter hosszúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="6f8b5-169">The URL must be one to 2000 characters long.</span></span>

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

### <span data-ttu-id="6f8b5-170">-SourceApiId</span><span class="sxs-lookup"><span data-stu-id="6f8b5-170">-SourceApiId</span></span>
<span data-ttu-id="6f8b5-171">A forrás API API-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="6f8b5-171">Api identifier of the source API.</span></span> <span data-ttu-id="6f8b5-172">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="6f8b5-172">This parameter is optional.</span></span>

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

### <span data-ttu-id="6f8b5-173">-SourceApiRevision</span><span class="sxs-lookup"><span data-stu-id="6f8b5-173">-SourceApiRevision</span></span>
<span data-ttu-id="6f8b5-174">A forrás API API-verziója.</span><span class="sxs-lookup"><span data-stu-id="6f8b5-174">Api Revision of the source API.</span></span> <span data-ttu-id="6f8b5-175">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="6f8b5-175">This parameter is optional.</span></span>

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

### <span data-ttu-id="6f8b5-176">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="6f8b5-176">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="6f8b5-177">Az előfizetés kulcs fejlécének nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6f8b5-177">Specifies the subscription key header name.</span></span>
<span data-ttu-id="6f8b5-178">Az alapértelmezett érték $Null.</span><span class="sxs-lookup"><span data-stu-id="6f8b5-178">The default value is $Null.</span></span>

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

### <span data-ttu-id="6f8b5-179">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="6f8b5-179">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="6f8b5-180">Az előfizetési kulcs lekérdezési karakterláncának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6f8b5-180">Specifies the subscription key query string parameter name.</span></span>
<span data-ttu-id="6f8b5-181">Az alapértelmezett érték $Null.</span><span class="sxs-lookup"><span data-stu-id="6f8b5-181">The default value is $Null.</span></span>

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

### <span data-ttu-id="6f8b5-182">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="6f8b5-182">-SubscriptionRequired</span></span>
<span data-ttu-id="6f8b5-183">Megjelölés az API-SubscriptionRequired vonatkozó kérelmek érvényesítéséhez.</span><span class="sxs-lookup"><span data-stu-id="6f8b5-183">Flag to enforce SubscriptionRequired for requests to the Api.</span></span> <span data-ttu-id="6f8b5-184">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="6f8b5-184">This parameter is optional.</span></span>

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

### <span data-ttu-id="6f8b5-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f8b5-185">CommonParameters</span></span>
<span data-ttu-id="6f8b5-186">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6f8b5-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f8b5-187">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="6f8b5-187">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f8b5-188">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6f8b5-188">INPUTS</span></span>

### <span data-ttu-id="6f8b5-189">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="6f8b5-189">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="6f8b5-190">System. String</span><span class="sxs-lookup"><span data-stu-id="6f8b5-190">System.String</span></span>

### <span data-ttu-id="6f8b5-191">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementSchema []</span><span class="sxs-lookup"><span data-stu-id="6f8b5-191">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="6f8b5-192">System. string []</span><span class="sxs-lookup"><span data-stu-id="6f8b5-192">System.String[]</span></span>

## <span data-ttu-id="6f8b5-193">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6f8b5-193">OUTPUTS</span></span>

### <span data-ttu-id="6f8b5-194">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="6f8b5-194">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="6f8b5-195">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6f8b5-195">NOTES</span></span>

## <span data-ttu-id="6f8b5-196">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6f8b5-196">RELATED LINKS</span></span>

[<span data-ttu-id="6f8b5-197">Exportálás – AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="6f8b5-197">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="6f8b5-198">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="6f8b5-198">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="6f8b5-199">Importálás – AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="6f8b5-199">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="6f8b5-200">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="6f8b5-200">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="6f8b5-201">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="6f8b5-201">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


