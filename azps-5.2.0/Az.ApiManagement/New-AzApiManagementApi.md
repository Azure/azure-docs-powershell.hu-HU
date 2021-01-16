---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 664CF009-FC52-4F1B-933B-3DEBD05AC8C5
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApi.md
ms.openlocfilehash: 3312c725d63bcb42aab7d82144c5a8f6f8e67641
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98364599"
---
# <span data-ttu-id="00698-101">New-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="00698-101">New-AzApiManagementApi</span></span>

## <span data-ttu-id="00698-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="00698-102">SYNOPSIS</span></span>
<span data-ttu-id="00698-103">Létrehoz egy API-t.</span><span class="sxs-lookup"><span data-stu-id="00698-103">Creates an API.</span></span>

## <span data-ttu-id="00698-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="00698-104">SYNTAX</span></span>

```
New-AzApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>] -Name <String>
 [-Description <String>] -ServiceUrl <String> -Path <String> -Protocols <PsApiManagementSchema[]>
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-OpenIdProviderId <String>]
 [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-ProductIds <String[]>] [-SubscriptionRequired]
 [-ApiVersionDescription <String>] [-ApiVersionSetId <String>] [-ApiVersion <String>] [-SourceApiId <String>]
 [-SourceApiRevision <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="00698-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="00698-105">DESCRIPTION</span></span>
<span data-ttu-id="00698-106">A **New-AzApiManagementApi** parancsmag létrehoz egy Azure API Management API-t.</span><span class="sxs-lookup"><span data-stu-id="00698-106">The **New-AzApiManagementApi** cmdlet creates an Azure API Management API.</span></span>

## <span data-ttu-id="00698-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="00698-107">EXAMPLES</span></span>

### <span data-ttu-id="00698-108">1. példa: API létrehozása</span><span class="sxs-lookup"><span data-stu-id="00698-108">Example 1: Create an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementApi -Context $ApiMgmtContext -Name "Echo api" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @("http", "https") -Path "testapi"
```

<span data-ttu-id="00698-109">Ez a parancs létrehoz egy EchoApi nevű API-t a megadott URL-címen.</span><span class="sxs-lookup"><span data-stu-id="00698-109">This command creates an API named EchoApi with the specified URL.</span></span>

### <span data-ttu-id="00698-110">2. példa: API létrehozása az összes művelet, címke, termék és házirend másolása a echo-api-ból és az ApiVersionSetbe</span><span class="sxs-lookup"><span data-stu-id="00698-110">Example 2: Create an API by copying all operation, Tags, Products and Policies from echo-api and into an ApiVersionSet</span></span>
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

<span data-ttu-id="00698-111">Ez a parancs létrehoz egy API-t az ApiVersionSetben, és a forrás Api-ból az összes műveletet, címkét és házirendet `echoapiv3` `xmsVersionSet` `echo-api` átmásolja.</span><span class="sxs-lookup"><span data-stu-id="00698-111">This command creates an API `echoapiv3` in ApiVersionSet `xmsVersionSet` and copies all operation, Tags and Policies from source Api `echo-api`.</span></span> <span data-ttu-id="00698-112">Felülbírálja a SubscriptionRequired, ServiceUrl, Path, Protocols</span><span class="sxs-lookup"><span data-stu-id="00698-112">It overrides the SubscriptionRequired, ServiceUrl, Path, Protocols</span></span>

### <span data-ttu-id="00698-113">3. példa</span><span class="sxs-lookup"><span data-stu-id="00698-113">Example 3</span></span>

<span data-ttu-id="00698-114">Létrehoz egy API-t.</span><span class="sxs-lookup"><span data-stu-id="00698-114">Creates an API.</span></span> <span data-ttu-id="00698-115">(automatikusan generált)</span><span class="sxs-lookup"><span data-stu-id="00698-115">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
New-AzApiManagementApi -ApiId '0001' -Context <PsApiManagementContext> -Name 'Echo api' -Path 'echov3' -Protocols Http -ServiceUrl 'https://contoso.com/apis/echo'
```

## <span data-ttu-id="00698-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="00698-116">PARAMETERS</span></span>

### <span data-ttu-id="00698-117">-ApiId</span><span class="sxs-lookup"><span data-stu-id="00698-117">-ApiId</span></span>
<span data-ttu-id="00698-118">A létrehozni szükséges API azonosítója.</span><span class="sxs-lookup"><span data-stu-id="00698-118">Specifies the ID of the API to create.</span></span>
<span data-ttu-id="00698-119">Ha nem adja meg ezt a paramétert, ez a parancsmag létrehoz egy azonosítót.</span><span class="sxs-lookup"><span data-stu-id="00698-119">If you do not specify this parameter, this cmdlet generates an ID for you.</span></span>

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

### <span data-ttu-id="00698-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="00698-120">-ApiVersion</span></span>
<span data-ttu-id="00698-121">A létrehozni szükséges Api API-verziója.</span><span class="sxs-lookup"><span data-stu-id="00698-121">Api Version of the Api to create.</span></span> <span data-ttu-id="00698-122">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="00698-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="00698-123">-ApiVersionDescription</span><span class="sxs-lookup"><span data-stu-id="00698-123">-ApiVersionDescription</span></span>
<span data-ttu-id="00698-124">Api verzióleírása.</span><span class="sxs-lookup"><span data-stu-id="00698-124">Api Version Description.</span></span> <span data-ttu-id="00698-125">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="00698-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="00698-126">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="00698-126">-ApiVersionSetId</span></span>
<span data-ttu-id="00698-127">A kapcsolódó Api-verziókészlet erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="00698-127">A resource identifier for the related Api Version Set.</span></span> <span data-ttu-id="00698-128">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="00698-128">This parameter is optional.</span></span>

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

### <span data-ttu-id="00698-129">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="00698-129">-AuthorizationScope</span></span>
<span data-ttu-id="00698-130">Az OAuth-műveletek hatókörét határozza meg.</span><span class="sxs-lookup"><span data-stu-id="00698-130">Specifies the OAuth operations scope.</span></span>
<span data-ttu-id="00698-131">Az alapértelmezett érték $Null.</span><span class="sxs-lookup"><span data-stu-id="00698-131">The default value is $Null.</span></span>

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

### <span data-ttu-id="00698-132">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="00698-132">-AuthorizationServerId</span></span>
<span data-ttu-id="00698-133">Az OAuth engedélyezési kiszolgálóazonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="00698-133">Specifies the OAuth authorization server ID.</span></span>
<span data-ttu-id="00698-134">Az alapértelmezett érték $Null.</span><span class="sxs-lookup"><span data-stu-id="00698-134">The default value is $Null.</span></span>
<span data-ttu-id="00698-135">Ha az *AuthorizationScope* paraméter meg van adva, meg kell adnia ezt a paramétert.</span><span class="sxs-lookup"><span data-stu-id="00698-135">You must specify this parameter if *AuthorizationScope* is specified.</span></span>

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

### <span data-ttu-id="00698-136">-BearerTokenSendingMethod</span><span class="sxs-lookup"><span data-stu-id="00698-136">-BearerTokenSendingMethod</span></span>
<span data-ttu-id="00698-137">OpenId engedélyezési kiszolgálói mechanizmus, amellyel hozzáférési jogkivonatot ad át az API-nak.</span><span class="sxs-lookup"><span data-stu-id="00698-137">OpenId authorization server mechanism by which access token is passed to the API.</span></span> <span data-ttu-id="00698-138">Lásd: http://tools.ietf.org/html/rfc6749#section-4 .</span><span class="sxs-lookup"><span data-stu-id="00698-138">Refer to http://tools.ietf.org/html/rfc6749#section-4.</span></span> <span data-ttu-id="00698-139">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="00698-139">This parameter is optional.</span></span> <span data-ttu-id="00698-140">Az alapértelmezett érték $null.</span><span class="sxs-lookup"><span data-stu-id="00698-140">Default value is $null.</span></span>

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

### <span data-ttu-id="00698-141">-Környezet</span><span class="sxs-lookup"><span data-stu-id="00698-141">-Context</span></span>
<span data-ttu-id="00698-142">Egy **PsApiManagementContext objektumot** ad meg.</span><span class="sxs-lookup"><span data-stu-id="00698-142">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="00698-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00698-143">-DefaultProfile</span></span>
<span data-ttu-id="00698-144">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="00698-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="00698-145">-Leírás</span><span class="sxs-lookup"><span data-stu-id="00698-145">-Description</span></span>
<span data-ttu-id="00698-146">Megadja a webes API leírását.</span><span class="sxs-lookup"><span data-stu-id="00698-146">Specifies a description for the web API.</span></span>

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

### <span data-ttu-id="00698-147">-Name</span><span class="sxs-lookup"><span data-stu-id="00698-147">-Name</span></span>
<span data-ttu-id="00698-148">A webes API nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="00698-148">Specifies the name of the web API.</span></span>
<span data-ttu-id="00698-149">Ez az API nyilvános neve, ahogyan a fejlesztői és rendszergazdai portálon megjelenik.</span><span class="sxs-lookup"><span data-stu-id="00698-149">This is the public name of the API as it appears on the developer and admin portals.</span></span>

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

### <span data-ttu-id="00698-150">-OpenIdProviderId</span><span class="sxs-lookup"><span data-stu-id="00698-150">-OpenIdProviderId</span></span>
<span data-ttu-id="00698-151">OpenId engedélyezési kiszolgáló azonosítója.</span><span class="sxs-lookup"><span data-stu-id="00698-151">OpenId authorization server identifier.</span></span> <span data-ttu-id="00698-152">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="00698-152">This parameter is optional.</span></span> <span data-ttu-id="00698-153">Az alapértelmezett érték $null.</span><span class="sxs-lookup"><span data-stu-id="00698-153">Default value is $null.</span></span> <span data-ttu-id="00698-154">Meg kell adni, ha a BearerTokenSendingMethods érték meg van adva.</span><span class="sxs-lookup"><span data-stu-id="00698-154">Must be specified if BearerTokenSendingMethods is specified.</span></span>

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

### <span data-ttu-id="00698-155">-Path</span><span class="sxs-lookup"><span data-stu-id="00698-155">-Path</span></span>
<span data-ttu-id="00698-156">A webes API elérési útját adja meg, amely az API nyilvános URL-címének utolsó része, és amely megfelel a felügyeleti portál Web API URL-utótag mezőjének.</span><span class="sxs-lookup"><span data-stu-id="00698-156">Specifies the web API path, which is the last part of the API's public URL and corresponds to the Web API URL suffix field in the admin portal.</span></span>
<span data-ttu-id="00698-157">Ezt az URL-címet használják az API-t használó ügyfelek arra, hogy kéréseket küldjenek a webszolgáltatásnak, és 1–400 karakter hosszúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="00698-157">This URL is used by API consumers to send requests to the web service, and must be one to 400 characters long.</span></span>
<span data-ttu-id="00698-158">Az alapértelmezett érték $Null.</span><span class="sxs-lookup"><span data-stu-id="00698-158">The default value is $Null.</span></span>

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

### <span data-ttu-id="00698-159">-ProductIds</span><span class="sxs-lookup"><span data-stu-id="00698-159">-ProductIds</span></span>
<span data-ttu-id="00698-160">Megadja az új API-hoz hozzáadandó termék-adatokat tartalmazó tömböt.</span><span class="sxs-lookup"><span data-stu-id="00698-160">Specifies an array of product IDs to which to add the new API.</span></span>

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

### <span data-ttu-id="00698-161">-Protocols</span><span class="sxs-lookup"><span data-stu-id="00698-161">-Protocols</span></span>
<span data-ttu-id="00698-162">A web API-protokollok tömbje.</span><span class="sxs-lookup"><span data-stu-id="00698-162">Specifies an array of web API protocols.</span></span>
<span data-ttu-id="00698-163">Érvényes értékek: http, https.</span><span class="sxs-lookup"><span data-stu-id="00698-163">Valid values are http, https.</span></span>
<span data-ttu-id="00698-164">Ezek azok a webes protokollok, amelyeken keresztül az API elérhetővé válik.</span><span class="sxs-lookup"><span data-stu-id="00698-164">These are the web protocols over which the API is made available.</span></span>
<span data-ttu-id="00698-165">Az alapértelmezett érték $Null.</span><span class="sxs-lookup"><span data-stu-id="00698-165">The default value is $Null.</span></span>

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

### <span data-ttu-id="00698-166">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="00698-166">-ServiceUrl</span></span>
<span data-ttu-id="00698-167">Annak a webszolgáltatásnak az URL-címe, amely elérhetővé teszi az API-t.</span><span class="sxs-lookup"><span data-stu-id="00698-167">Specifies the URL of the web service that exposes the API.</span></span>
<span data-ttu-id="00698-168">Ezt az URL-címet csak az Azure API Management használja, és nem teszi nyilvánosra.</span><span class="sxs-lookup"><span data-stu-id="00698-168">This URL is used only by Azure API Management, and is not made public.</span></span>
<span data-ttu-id="00698-169">Az URL-címnek 1–2000 karakter hosszúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="00698-169">The URL must be one to 2000 characters long.</span></span>

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

### <span data-ttu-id="00698-170">-SourceApiId</span><span class="sxs-lookup"><span data-stu-id="00698-170">-SourceApiId</span></span>
<span data-ttu-id="00698-171">A forrás API API-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="00698-171">Api identifier of the source API.</span></span> <span data-ttu-id="00698-172">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="00698-172">This parameter is optional.</span></span>

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

### <span data-ttu-id="00698-173">-SourceApiRevision</span><span class="sxs-lookup"><span data-stu-id="00698-173">-SourceApiRevision</span></span>
<span data-ttu-id="00698-174">A forrás API API-jának átdolgozása.</span><span class="sxs-lookup"><span data-stu-id="00698-174">Api Revision of the source API.</span></span> <span data-ttu-id="00698-175">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="00698-175">This parameter is optional.</span></span>

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

### <span data-ttu-id="00698-176">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="00698-176">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="00698-177">Az előfizetés kulcsfejlécének nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="00698-177">Specifies the subscription key header name.</span></span>
<span data-ttu-id="00698-178">Az alapértelmezett érték $Null.</span><span class="sxs-lookup"><span data-stu-id="00698-178">The default value is $Null.</span></span>

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

### <span data-ttu-id="00698-179">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="00698-179">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="00698-180">Az előfizetés kulcs lekérdezési karakterláncának paraméternevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="00698-180">Specifies the subscription key query string parameter name.</span></span>
<span data-ttu-id="00698-181">Az alapértelmezett érték $Null.</span><span class="sxs-lookup"><span data-stu-id="00698-181">The default value is $Null.</span></span>

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

### <span data-ttu-id="00698-182">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="00698-182">-SubscriptionRequired</span></span>
<span data-ttu-id="00698-183">Flag to enforce SubscriptionRequired for requests to the Api.</span><span class="sxs-lookup"><span data-stu-id="00698-183">Flag to enforce SubscriptionRequired for requests to the Api.</span></span> <span data-ttu-id="00698-184">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="00698-184">This parameter is optional.</span></span>

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

### <span data-ttu-id="00698-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00698-185">CommonParameters</span></span>
<span data-ttu-id="00698-186">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00698-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00698-187">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="00698-187">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00698-188">INPUTS</span><span class="sxs-lookup"><span data-stu-id="00698-188">INPUTS</span></span>

### <span data-ttu-id="00698-189">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="00698-189">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="00698-190">System.String</span><span class="sxs-lookup"><span data-stu-id="00698-190">System.String</span></span>

### <span data-ttu-id="00698-191">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span><span class="sxs-lookup"><span data-stu-id="00698-191">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="00698-192">System.String[]</span><span class="sxs-lookup"><span data-stu-id="00698-192">System.String[]</span></span>

## <span data-ttu-id="00698-193">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="00698-193">OUTPUTS</span></span>

### <span data-ttu-id="00698-194">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="00698-194">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="00698-195">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="00698-195">NOTES</span></span>

## <span data-ttu-id="00698-196">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="00698-196">RELATED LINKS</span></span>

[<span data-ttu-id="00698-197">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="00698-197">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="00698-198">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="00698-198">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="00698-199">Import-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="00698-199">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="00698-200">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="00698-200">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="00698-201">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="00698-201">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


