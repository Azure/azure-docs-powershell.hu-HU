---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 29CCF141-CC2F-4E11-8235-64025CFB5782
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApi.md
ms.openlocfilehash: 02a7a35f4498724266d4c352744169d733f5eeab
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024947"
---
# <span data-ttu-id="5033d-101">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="5033d-101">Set-AzApiManagementApi</span></span>

## <span data-ttu-id="5033d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5033d-102">SYNOPSIS</span></span>
<span data-ttu-id="5033d-103">Módosítja az API-t.</span><span class="sxs-lookup"><span data-stu-id="5033d-103">Modifies an API.</span></span>

## <span data-ttu-id="5033d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5033d-104">SYNTAX</span></span>

### <span data-ttu-id="5033d-105">ExpandedParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5033d-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-Name <String>]
 [-Description <String>] [-ServiceUrl <String>] [-Path <String>] [-Protocols <PsApiManagementSchema[]>]
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-OpenIdProviderId <String>]
 [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-SubscriptionRequired] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5033d-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="5033d-106">ByInputObject</span></span>
```
Set-AzApiManagementApi -InputObject <PsApiManagementApi> [-Name <String>] [-Description <String>]
 [-ServiceUrl <String>] [-Path <String>] [-Protocols <PsApiManagementSchema[]>]
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-OpenIdProviderId <String>]
 [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-SubscriptionRequired] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5033d-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="5033d-107">DESCRIPTION</span></span>
<span data-ttu-id="5033d-108">A **set-AzApiManagementApi** parancsmag módosította az Azure API-kezelési API-t.</span><span class="sxs-lookup"><span data-stu-id="5033d-108">The **Set-AzApiManagementApi** cmdlet modifies an Azure API Management API.</span></span>

## <span data-ttu-id="5033d-109">Példák</span><span class="sxs-lookup"><span data-stu-id="5033d-109">EXAMPLES</span></span>

### <span data-ttu-id="5033d-110">Példa 1: API módosítása</span><span class="sxs-lookup"><span data-stu-id="5033d-110">Example 1: Modify an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementApi -Context $ApiMgmtContext -Name "EchoApi" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @('https') -Description "Responds with what was sent" -Path "echo"
```

### <span data-ttu-id="5033d-111">2. példa: API hozzáadása meglévő ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="5033d-111">Example 2: Add an API to an existing ApiVersionSet</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$versionSet = New-AzApiManagementApiVersionSet -Context $context -Name "Echo API Version Set" -Scheme Segment -Description "version set sample"
PS C:\>$api = Get-AzApiManagementApi -Context $ApiMgmtContext -ApiId "echo-api"
PS C:\>$api.ApiVersionSetId = $versionSet.Id
PS C:\>$api.ApiVersion = "v1"
PS C:\>$api.ApiVersionSetDescription = $versionSet.Description
PS C:\>Set-AzApiManagementApi -InputObject $api -PassThru
```

<span data-ttu-id="5033d-112">Ez a példa egy API-t ad hozzá egy meglévő API-verzióhoz.</span><span class="sxs-lookup"><span data-stu-id="5033d-112">This example adds an API to an existing API Version Set</span></span>

### <span data-ttu-id="5033d-113">3. példa: a backend ServiceUrl megváltoztatása, ahol az API mutat</span><span class="sxs-lookup"><span data-stu-id="5033d-113">Example 3: Change the Backend ServiceUrl where the API is pointing to</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$updatedApiServiceUrl = "http://newechoapi.cloudapp.net/updateapi"
PS C:\>$updatedApi = Set-AzApiManagementApi -Context $ApiMgmtContext -ApiId $echoApiId -ServiceUrl $updatedApiServiceUrl
```

<span data-ttu-id="5033d-114">Ebben a példában a ServiceUrl frissíti a `echo-api` mutatót.</span><span class="sxs-lookup"><span data-stu-id="5033d-114">This example updates the ServiceUrl the `echo-api` is pointing to.</span></span>

## <span data-ttu-id="5033d-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5033d-115">PARAMETERS</span></span>

### <span data-ttu-id="5033d-116">-ApiId</span><span class="sxs-lookup"><span data-stu-id="5033d-116">-ApiId</span></span>
<span data-ttu-id="5033d-117">A módosítandó API AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="5033d-117">Specifies the ID of the API to modify.</span></span>

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

### <span data-ttu-id="5033d-118">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="5033d-118">-AuthorizationScope</span></span>
<span data-ttu-id="5033d-119">A OAuth-műveletek hatókörét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5033d-119">Specifies the OAuth operations scope.</span></span>
<span data-ttu-id="5033d-120">Az alapértelmezett érték $Null.</span><span class="sxs-lookup"><span data-stu-id="5033d-120">The default value is $Null.</span></span>

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

### <span data-ttu-id="5033d-121">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="5033d-121">-AuthorizationServerId</span></span>
<span data-ttu-id="5033d-122">A OAuth-engedélyezési kiszolgáló azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="5033d-122">Specifies the OAuth authorization server identifier.</span></span>
<span data-ttu-id="5033d-123">Az alapértelmezett érték $Null.</span><span class="sxs-lookup"><span data-stu-id="5033d-123">The default value is $Null.</span></span>
<span data-ttu-id="5033d-124">Ezt a paramétert akkor kell megadnia, ha a *AuthorizationScope* meg van adva.</span><span class="sxs-lookup"><span data-stu-id="5033d-124">You must specify this parameter if *AuthorizationScope* is specified.</span></span>

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

### <span data-ttu-id="5033d-125">-BearerTokenSendingMethod</span><span class="sxs-lookup"><span data-stu-id="5033d-125">-BearerTokenSendingMethod</span></span>
<span data-ttu-id="5033d-126">Az OpenId engedélyezési kiszolgáló mechanizmusa, amellyel az Access-tokent átadták az API-nek.</span><span class="sxs-lookup"><span data-stu-id="5033d-126">OpenId authorization server mechanism by which access token is passed to the API.</span></span> <span data-ttu-id="5033d-127">Lásd: http://tools.ietf.org/html/rfc6749#section-4 .</span><span class="sxs-lookup"><span data-stu-id="5033d-127">Refer to http://tools.ietf.org/html/rfc6749#section-4.</span></span> <span data-ttu-id="5033d-128">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="5033d-128">This parameter is optional.</span></span> <span data-ttu-id="5033d-129">Az alapértelmezett érték $null.</span><span class="sxs-lookup"><span data-stu-id="5033d-129">Default value is $null.</span></span>

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

### <span data-ttu-id="5033d-130">-Környezet</span><span class="sxs-lookup"><span data-stu-id="5033d-130">-Context</span></span>
<span data-ttu-id="5033d-131">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="5033d-131">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="5033d-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5033d-132">-DefaultProfile</span></span>
<span data-ttu-id="5033d-133">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5033d-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5033d-134">-Leírás</span><span class="sxs-lookup"><span data-stu-id="5033d-134">-Description</span></span>
<span data-ttu-id="5033d-135">A webes API leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="5033d-135">Specifies a description for the web API.</span></span>

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

### <span data-ttu-id="5033d-136">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5033d-136">-InputObject</span></span>
<span data-ttu-id="5033d-137">A PsApiManagementApi példánya.</span><span class="sxs-lookup"><span data-stu-id="5033d-137">Instance of PsApiManagementApi.</span></span> <span data-ttu-id="5033d-138">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="5033d-138">This parameter is required.</span></span>

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

### <span data-ttu-id="5033d-139">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5033d-139">-Name</span></span>
<span data-ttu-id="5033d-140">A webes API nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5033d-140">Specifies the name of the web API.</span></span>

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

### <span data-ttu-id="5033d-141">-OpenIdProviderId</span><span class="sxs-lookup"><span data-stu-id="5033d-141">-OpenIdProviderId</span></span>
<span data-ttu-id="5033d-142">OpenId engedélyezési kiszolgáló azonosítója</span><span class="sxs-lookup"><span data-stu-id="5033d-142">OpenId authorization server identifier.</span></span> <span data-ttu-id="5033d-143">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="5033d-143">This parameter is optional.</span></span> <span data-ttu-id="5033d-144">Az alapértelmezett érték $null.</span><span class="sxs-lookup"><span data-stu-id="5033d-144">Default value is $null.</span></span> <span data-ttu-id="5033d-145">Meg kell adni, ha a BearerTokenSendingMethods meg van adva.</span><span class="sxs-lookup"><span data-stu-id="5033d-145">Must be specified if BearerTokenSendingMethods is specified.</span></span>

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

### <span data-ttu-id="5033d-146">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5033d-146">-PassThru</span></span>
<span data-ttu-id="5033d-147">passthru</span><span class="sxs-lookup"><span data-stu-id="5033d-147">passthru</span></span>

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

### <span data-ttu-id="5033d-148">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="5033d-148">-Path</span></span>
<span data-ttu-id="5033d-149">A webes API elérési útvonalát adja meg, amely az API nyilvános URL-címe utolsó része.</span><span class="sxs-lookup"><span data-stu-id="5033d-149">Specifies the web API path, which is the last part of the API's public URL.</span></span>
<span data-ttu-id="5033d-150">Ezt az URL-címet használják az API-felhasználóknak a kérések webszolgáltatáshoz való küldéséhez, és egy-egy 400 karakter hosszúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="5033d-150">This URL is used by API consumers to send requests to the web service, and must be one to 400 characters long.</span></span>
<span data-ttu-id="5033d-151">Az alapértelmezett érték $Null.</span><span class="sxs-lookup"><span data-stu-id="5033d-151">The default value is $Null.</span></span>

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

### <span data-ttu-id="5033d-152">-Protokollok</span><span class="sxs-lookup"><span data-stu-id="5033d-152">-Protocols</span></span>
<span data-ttu-id="5033d-153">A webes API-protokollok tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5033d-153">Specifies an array of web API protocols.</span></span>
<span data-ttu-id="5033d-154">http-és HTTPS-psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="5033d-154">psdx_paramvalues http and https.</span></span>
<span data-ttu-id="5033d-155">Ezek azok a webes protokollok, amelyek az API-t elérhetővé tették.</span><span class="sxs-lookup"><span data-stu-id="5033d-155">These are the web protocols over which the API is made available.</span></span>
<span data-ttu-id="5033d-156">Az alapértelmezett érték $Null.</span><span class="sxs-lookup"><span data-stu-id="5033d-156">The default value is $Null.</span></span>

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

### <span data-ttu-id="5033d-157">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="5033d-157">-ServiceUrl</span></span>
<span data-ttu-id="5033d-158">Annak a webszolgáltatásnak az URL-címe, amely kiteszi az API-t.</span><span class="sxs-lookup"><span data-stu-id="5033d-158">Specifies the URL of the web service that exposes the API.</span></span>
<span data-ttu-id="5033d-159">Ezt az URL-címet csak az Azure API-kezelés használja, és nem jelenik meg nyilvánosan.</span><span class="sxs-lookup"><span data-stu-id="5033d-159">This URL is used only by Azure API Management, and is not made public.</span></span>
<span data-ttu-id="5033d-160">Az URL-címnek egy 2000 karakter hosszúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="5033d-160">The URL must be one to 2000 characters long.</span></span>

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

### <span data-ttu-id="5033d-161">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="5033d-161">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="5033d-162">Az előfizetési kulcs fejlécének nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5033d-162">Specifies the name of the subscription key header.</span></span>
<span data-ttu-id="5033d-163">Az alapértelmezett érték $Null.</span><span class="sxs-lookup"><span data-stu-id="5033d-163">The default value is $Null.</span></span>

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

### <span data-ttu-id="5033d-164">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="5033d-164">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="5033d-165">Az előfizetési kulcs lekérdezési karakterlánc paraméterének a nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5033d-165">Specifies the name of the subscription key query string parameter.</span></span>
<span data-ttu-id="5033d-166">Az alapértelmezett érték $Null.</span><span class="sxs-lookup"><span data-stu-id="5033d-166">The default value is $Null.</span></span>

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

### <span data-ttu-id="5033d-167">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="5033d-167">-SubscriptionRequired</span></span>
<span data-ttu-id="5033d-168">Megjelölés az API-SubscriptionRequired vonatkozó kérelmek érvényesítéséhez.</span><span class="sxs-lookup"><span data-stu-id="5033d-168">Flag to enforce SubscriptionRequired for requests to the Api.</span></span> <span data-ttu-id="5033d-169">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="5033d-169">This parameter is optional.</span></span>

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

### <span data-ttu-id="5033d-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5033d-170">CommonParameters</span></span>
<span data-ttu-id="5033d-171">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5033d-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5033d-172">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="5033d-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5033d-173">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5033d-173">INPUTS</span></span>

### <span data-ttu-id="5033d-174">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="5033d-174">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="5033d-175">System. String</span><span class="sxs-lookup"><span data-stu-id="5033d-175">System.String</span></span>

### <span data-ttu-id="5033d-176">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="5033d-176">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

### <span data-ttu-id="5033d-177">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementSchema []</span><span class="sxs-lookup"><span data-stu-id="5033d-177">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="5033d-178">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="5033d-178">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="5033d-179">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5033d-179">OUTPUTS</span></span>

### <span data-ttu-id="5033d-180">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="5033d-180">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="5033d-181">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5033d-181">NOTES</span></span>

## <span data-ttu-id="5033d-182">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5033d-182">RELATED LINKS</span></span>

[<span data-ttu-id="5033d-183">Exportálás – AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="5033d-183">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="5033d-184">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="5033d-184">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="5033d-185">Importálás – AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="5033d-185">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="5033d-186">Új – AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="5033d-186">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="5033d-187">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="5033d-187">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)


