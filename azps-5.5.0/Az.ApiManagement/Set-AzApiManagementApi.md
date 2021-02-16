---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 29CCF141-CC2F-4E11-8235-64025CFB5782
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApi.md
ms.openlocfilehash: 02a7a35f4498724266d4c352744169d733f5eeab
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205622"
---
# <span data-ttu-id="fc998-101">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="fc998-101">Set-AzApiManagementApi</span></span>

## <span data-ttu-id="fc998-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc998-102">SYNOPSIS</span></span>
<span data-ttu-id="fc998-103">Módosít egy API-t.</span><span class="sxs-lookup"><span data-stu-id="fc998-103">Modifies an API.</span></span>

## <span data-ttu-id="fc998-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="fc998-104">SYNTAX</span></span>

### <span data-ttu-id="fc998-105">ExpandedParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fc998-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-Name <String>]
 [-Description <String>] [-ServiceUrl <String>] [-Path <String>] [-Protocols <PsApiManagementSchema[]>]
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-OpenIdProviderId <String>]
 [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-SubscriptionRequired] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fc998-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="fc998-106">ByInputObject</span></span>
```
Set-AzApiManagementApi -InputObject <PsApiManagementApi> [-Name <String>] [-Description <String>]
 [-ServiceUrl <String>] [-Path <String>] [-Protocols <PsApiManagementSchema[]>]
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-OpenIdProviderId <String>]
 [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-SubscriptionRequired] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fc998-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="fc998-107">DESCRIPTION</span></span>
<span data-ttu-id="fc998-108">A **Set-AzApiManagementApi** parancsmag módosítja az Azure API Felügyeleti API-t.</span><span class="sxs-lookup"><span data-stu-id="fc998-108">The **Set-AzApiManagementApi** cmdlet modifies an Azure API Management API.</span></span>

## <span data-ttu-id="fc998-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="fc998-109">EXAMPLES</span></span>

### <span data-ttu-id="fc998-110">1. példa: API módosítása</span><span class="sxs-lookup"><span data-stu-id="fc998-110">Example 1: Modify an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementApi -Context $ApiMgmtContext -Name "EchoApi" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @('https') -Description "Responds with what was sent" -Path "echo"
```

### <span data-ttu-id="fc998-111">2. példa: API hozzáadása meglévő ApiVersionSethez</span><span class="sxs-lookup"><span data-stu-id="fc998-111">Example 2: Add an API to an existing ApiVersionSet</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$versionSet = New-AzApiManagementApiVersionSet -Context $context -Name "Echo API Version Set" -Scheme Segment -Description "version set sample"
PS C:\>$api = Get-AzApiManagementApi -Context $ApiMgmtContext -ApiId "echo-api"
PS C:\>$api.ApiVersionSetId = $versionSet.Id
PS C:\>$api.ApiVersion = "v1"
PS C:\>$api.ApiVersionSetDescription = $versionSet.Description
PS C:\>Set-AzApiManagementApi -InputObject $api -PassThru
```

<span data-ttu-id="fc998-112">Ez a példa hozzáad egy API-t egy meglévő API-verziókészlethez</span><span class="sxs-lookup"><span data-stu-id="fc998-112">This example adds an API to an existing API Version Set</span></span>

### <span data-ttu-id="fc998-113">3. példa: A Backend ServiceUrl módosítása arra a pontra, ahová az API mutat</span><span class="sxs-lookup"><span data-stu-id="fc998-113">Example 3: Change the Backend ServiceUrl where the API is pointing to</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$updatedApiServiceUrl = "http://newechoapi.cloudapp.net/updateapi"
PS C:\>$updatedApi = Set-AzApiManagementApi -Context $ApiMgmtContext -ApiId $echoApiId -ServiceUrl $updatedApiServiceUrl
```

<span data-ttu-id="fc998-114">Ebben a példában az a ServiceUrl `echo-api` frissül, amelyre mutat.</span><span class="sxs-lookup"><span data-stu-id="fc998-114">This example updates the ServiceUrl the `echo-api` is pointing to.</span></span>

## <span data-ttu-id="fc998-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fc998-115">PARAMETERS</span></span>

### <span data-ttu-id="fc998-116">-ApiId</span><span class="sxs-lookup"><span data-stu-id="fc998-116">-ApiId</span></span>
<span data-ttu-id="fc998-117">A módosítania kell az API azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="fc998-117">Specifies the ID of the API to modify.</span></span>

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

### <span data-ttu-id="fc998-118">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="fc998-118">-AuthorizationScope</span></span>
<span data-ttu-id="fc998-119">Az OAuth-műveletek hatókörét határozza meg.</span><span class="sxs-lookup"><span data-stu-id="fc998-119">Specifies the OAuth operations scope.</span></span>
<span data-ttu-id="fc998-120">Az alapértelmezett érték $Null.</span><span class="sxs-lookup"><span data-stu-id="fc998-120">The default value is $Null.</span></span>

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

### <span data-ttu-id="fc998-121">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="fc998-121">-AuthorizationServerId</span></span>
<span data-ttu-id="fc998-122">Az OAuth engedélyezési kiszolgáló azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="fc998-122">Specifies the OAuth authorization server identifier.</span></span>
<span data-ttu-id="fc998-123">Az alapértelmezett érték $Null.</span><span class="sxs-lookup"><span data-stu-id="fc998-123">The default value is $Null.</span></span>
<span data-ttu-id="fc998-124">Ha az *AuthorizationScope* paraméter meg van adva, meg kell adnia ezt a paramétert.</span><span class="sxs-lookup"><span data-stu-id="fc998-124">You must specify this parameter if *AuthorizationScope* is specified.</span></span>

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

### <span data-ttu-id="fc998-125">-BearerTokenSendingMethod</span><span class="sxs-lookup"><span data-stu-id="fc998-125">-BearerTokenSendingMethod</span></span>
<span data-ttu-id="fc998-126">OpenId engedélyezési kiszolgálói mechanizmus, amellyel hozzáférési jogkivonatot ad át az API-nak.</span><span class="sxs-lookup"><span data-stu-id="fc998-126">OpenId authorization server mechanism by which access token is passed to the API.</span></span> <span data-ttu-id="fc998-127">Lásd: http://tools.ietf.org/html/rfc6749#section-4 .</span><span class="sxs-lookup"><span data-stu-id="fc998-127">Refer to http://tools.ietf.org/html/rfc6749#section-4.</span></span> <span data-ttu-id="fc998-128">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="fc998-128">This parameter is optional.</span></span> <span data-ttu-id="fc998-129">Az alapértelmezett érték $null.</span><span class="sxs-lookup"><span data-stu-id="fc998-129">Default value is $null.</span></span>

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

### <span data-ttu-id="fc998-130">-Környezet</span><span class="sxs-lookup"><span data-stu-id="fc998-130">-Context</span></span>
<span data-ttu-id="fc998-131">Egy **PsApiManagementContext objektumot** ad meg.</span><span class="sxs-lookup"><span data-stu-id="fc998-131">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="fc998-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc998-132">-DefaultProfile</span></span>
<span data-ttu-id="fc998-133">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fc998-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fc998-134">-Leírás</span><span class="sxs-lookup"><span data-stu-id="fc998-134">-Description</span></span>
<span data-ttu-id="fc998-135">Megadja a webes API leírását.</span><span class="sxs-lookup"><span data-stu-id="fc998-135">Specifies a description for the web API.</span></span>

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

### <span data-ttu-id="fc998-136">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fc998-136">-InputObject</span></span>
<span data-ttu-id="fc998-137">A PsApiManagementApi példánya.</span><span class="sxs-lookup"><span data-stu-id="fc998-137">Instance of PsApiManagementApi.</span></span> <span data-ttu-id="fc998-138">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="fc998-138">This parameter is required.</span></span>

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

### <span data-ttu-id="fc998-139">-Name</span><span class="sxs-lookup"><span data-stu-id="fc998-139">-Name</span></span>
<span data-ttu-id="fc998-140">A webes API nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fc998-140">Specifies the name of the web API.</span></span>

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

### <span data-ttu-id="fc998-141">-OpenIdProviderId</span><span class="sxs-lookup"><span data-stu-id="fc998-141">-OpenIdProviderId</span></span>
<span data-ttu-id="fc998-142">OpenId engedélyezési kiszolgáló azonosítója.</span><span class="sxs-lookup"><span data-stu-id="fc998-142">OpenId authorization server identifier.</span></span> <span data-ttu-id="fc998-143">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="fc998-143">This parameter is optional.</span></span> <span data-ttu-id="fc998-144">Az alapértelmezett érték $null.</span><span class="sxs-lookup"><span data-stu-id="fc998-144">Default value is $null.</span></span> <span data-ttu-id="fc998-145">Meg kell adni, ha a BearerTokenSendingMethods érték meg van adva.</span><span class="sxs-lookup"><span data-stu-id="fc998-145">Must be specified if BearerTokenSendingMethods is specified.</span></span>

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

### <span data-ttu-id="fc998-146">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fc998-146">-PassThru</span></span>
<span data-ttu-id="fc998-147">passthru</span><span class="sxs-lookup"><span data-stu-id="fc998-147">passthru</span></span>

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

### <span data-ttu-id="fc998-148">-Path</span><span class="sxs-lookup"><span data-stu-id="fc998-148">-Path</span></span>
<span data-ttu-id="fc998-149">Megadja a webes API elérési útját, amely az API nyilvános URL-címének utolsó része.</span><span class="sxs-lookup"><span data-stu-id="fc998-149">Specifies the web API path, which is the last part of the API's public URL.</span></span>
<span data-ttu-id="fc998-150">Ezt az URL-címet használják az API-t használó ügyfelek arra, hogy kéréseket küldjenek a webszolgáltatásnak, és 1–400 karakter hosszúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="fc998-150">This URL is used by API consumers to send requests to the web service, and must be one to 400 characters long.</span></span>
<span data-ttu-id="fc998-151">Az alapértelmezett érték $Null.</span><span class="sxs-lookup"><span data-stu-id="fc998-151">The default value is $Null.</span></span>

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

### <span data-ttu-id="fc998-152">-Protocols</span><span class="sxs-lookup"><span data-stu-id="fc998-152">-Protocols</span></span>
<span data-ttu-id="fc998-153">A web API-protokollok tömbje.</span><span class="sxs-lookup"><span data-stu-id="fc998-153">Specifies an array of web API protocols.</span></span>
<span data-ttu-id="fc998-154">psdx_paramvalues http és https.</span><span class="sxs-lookup"><span data-stu-id="fc998-154">psdx_paramvalues http and https.</span></span>
<span data-ttu-id="fc998-155">Ezek azok a webes protokollok, amelyeken keresztül az API elérhetővé válik.</span><span class="sxs-lookup"><span data-stu-id="fc998-155">These are the web protocols over which the API is made available.</span></span>
<span data-ttu-id="fc998-156">Az alapértelmezett érték $Null.</span><span class="sxs-lookup"><span data-stu-id="fc998-156">The default value is $Null.</span></span>

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

### <span data-ttu-id="fc998-157">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="fc998-157">-ServiceUrl</span></span>
<span data-ttu-id="fc998-158">Annak a webszolgáltatásnak az URL-címe, amely elérhetővé teszi az API-t.</span><span class="sxs-lookup"><span data-stu-id="fc998-158">Specifies the URL of the web service that exposes the API.</span></span>
<span data-ttu-id="fc998-159">Ezt az URL-címet csak az Azure API Management használja, és nem teszi nyilvánosra.</span><span class="sxs-lookup"><span data-stu-id="fc998-159">This URL is used only by Azure API Management, and is not made public.</span></span>
<span data-ttu-id="fc998-160">Az URL-címnek 1–2000 karakter hosszúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="fc998-160">The URL must be one to 2000 characters long.</span></span>

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

### <span data-ttu-id="fc998-161">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="fc998-161">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="fc998-162">Az előfizetés kulcsfejlécének nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fc998-162">Specifies the name of the subscription key header.</span></span>
<span data-ttu-id="fc998-163">Az alapértelmezett érték $Null.</span><span class="sxs-lookup"><span data-stu-id="fc998-163">The default value is $Null.</span></span>

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

### <span data-ttu-id="fc998-164">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="fc998-164">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="fc998-165">Az előfizetés kulcslekérdezés karakterlánc paraméterének nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fc998-165">Specifies the name of the subscription key query string parameter.</span></span>
<span data-ttu-id="fc998-166">Az alapértelmezett érték $Null.</span><span class="sxs-lookup"><span data-stu-id="fc998-166">The default value is $Null.</span></span>

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

### <span data-ttu-id="fc998-167">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="fc998-167">-SubscriptionRequired</span></span>
<span data-ttu-id="fc998-168">Flag to enforce SubscriptionRequired for requests to the Api.</span><span class="sxs-lookup"><span data-stu-id="fc998-168">Flag to enforce SubscriptionRequired for requests to the Api.</span></span> <span data-ttu-id="fc998-169">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="fc998-169">This parameter is optional.</span></span>

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

### <span data-ttu-id="fc998-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc998-170">CommonParameters</span></span>
<span data-ttu-id="fc998-171">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc998-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc998-172">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fc998-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc998-173">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fc998-173">INPUTS</span></span>

### <span data-ttu-id="fc998-174">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="fc998-174">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="fc998-175">System.String</span><span class="sxs-lookup"><span data-stu-id="fc998-175">System.String</span></span>

### <span data-ttu-id="fc998-176">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="fc998-176">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

### <span data-ttu-id="fc998-177">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span><span class="sxs-lookup"><span data-stu-id="fc998-177">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="fc998-178">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="fc998-178">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="fc998-179">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fc998-179">OUTPUTS</span></span>

### <span data-ttu-id="fc998-180">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="fc998-180">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="fc998-181">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="fc998-181">NOTES</span></span>

## <span data-ttu-id="fc998-182">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fc998-182">RELATED LINKS</span></span>

[<span data-ttu-id="fc998-183">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="fc998-183">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="fc998-184">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="fc998-184">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="fc998-185">Import-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="fc998-185">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="fc998-186">New-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="fc998-186">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="fc998-187">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="fc998-187">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)


