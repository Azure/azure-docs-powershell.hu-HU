---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementapirevision
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementApiRevision.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementApiRevision.md
ms.openlocfilehash: fe709b560c790ad010469bf2f0a2043231124138
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501228"
---
# <span data-ttu-id="5afb0-101">Set-AzureRmApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="5afb0-101">Set-AzureRmApiManagementApiRevision</span></span>

## <span data-ttu-id="5afb0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5afb0-102">SYNOPSIS</span></span>
<span data-ttu-id="5afb0-103">API-módosítás módosítása</span><span class="sxs-lookup"><span data-stu-id="5afb0-103">Modifies an API Revision</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5afb0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5afb0-104">SYNTAX</span></span>

### <span data-ttu-id="5afb0-105">ExpandedParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5afb0-105">ExpandedParameter (Default)</span></span>
```
Set-AzureRmApiManagementApiRevision -ApiRevision <String> -Context <PsApiManagementContext> -ApiId <String>
 -Name <String> [-Description <String>] -ServiceUrl <String> [-Path <String>]
 -Protocols <PsApiManagementSchema[]> [-AuthorizationServerId <String>] [-AuthorizationScope <String>]
 [-SubscriptionKeyHeaderName <String>] [-SubscriptionKeyQueryParamName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5afb0-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="5afb0-106">ByInputObject</span></span>
```
Set-AzureRmApiManagementApiRevision -InputObject <PsApiManagementApi> -Name <String> [-Description <String>]
 -ServiceUrl <String> [-Path <String>] -Protocols <PsApiManagementSchema[]> [-AuthorizationServerId <String>]
 [-AuthorizationScope <String>] [-SubscriptionKeyHeaderName <String>] [-SubscriptionKeyQueryParamName <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5afb0-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="5afb0-107">DESCRIPTION</span></span>
<span data-ttu-id="5afb0-108">A **set-AzureRmApiManagementApiRevision** parancsmag egy Azure API-kezelési API-módosítást módosít.</span><span class="sxs-lookup"><span data-stu-id="5afb0-108">The **Set-AzureRmApiManagementApiRevision** cmdlet modifies an Azure API Management API Revision.</span></span>

## <span data-ttu-id="5afb0-109">Példák</span><span class="sxs-lookup"><span data-stu-id="5afb0-109">EXAMPLES</span></span>

### <span data-ttu-id="5afb0-110">Példa 1 API-módosítás módosítása</span><span class="sxs-lookup"><span data-stu-id="5afb0-110">Example 1 Modify an API Revision</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementApiRevision -Context $ApiMgmtContext -ApiId "echo-api" -ApiRevision "2" -Name "EchoApi" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @('https') -Description "Responds with what was sent" -Path "echo"
```

<span data-ttu-id="5afb0-111">A parancsmag frissíti az `2` API `echo-api` új leírását, protokollját és elérési útját.</span><span class="sxs-lookup"><span data-stu-id="5afb0-111">The cmdlet updates the `2` revision of the API `echo-api` with a new description, protocol and path.</span></span>

## <span data-ttu-id="5afb0-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5afb0-112">PARAMETERS</span></span>

### <span data-ttu-id="5afb0-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="5afb0-113">-ApiId</span></span>
<span data-ttu-id="5afb0-114">A meglévő API-azonosító.</span><span class="sxs-lookup"><span data-stu-id="5afb0-114">Identifier of existing API.</span></span>
<span data-ttu-id="5afb0-115">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="5afb0-115">This parameter is required.</span></span>

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

### <span data-ttu-id="5afb0-116">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="5afb0-116">-ApiRevision</span></span>
<span data-ttu-id="5afb0-117">A meglévő API-verzió verziószámának azonosítója</span><span class="sxs-lookup"><span data-stu-id="5afb0-117">Identifier of existing API Revision.</span></span> <span data-ttu-id="5afb0-118">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="5afb0-118">This parameter is required.</span></span>

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

### <span data-ttu-id="5afb0-119">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="5afb0-119">-AuthorizationScope</span></span>
<span data-ttu-id="5afb0-120">OAuth-műveletek hatóköre</span><span class="sxs-lookup"><span data-stu-id="5afb0-120">OAuth operations scope.</span></span>
<span data-ttu-id="5afb0-121">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="5afb0-121">This parameter is optional.</span></span>
<span data-ttu-id="5afb0-122">Az alapértelmezett érték $null.</span><span class="sxs-lookup"><span data-stu-id="5afb0-122">Default value is $null.</span></span>

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

### <span data-ttu-id="5afb0-123">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="5afb0-123">-AuthorizationServerId</span></span>
<span data-ttu-id="5afb0-124">OAuth-engedélyezési kiszolgáló azonosítója</span><span class="sxs-lookup"><span data-stu-id="5afb0-124">OAuth authorization server identifier.</span></span>
<span data-ttu-id="5afb0-125">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="5afb0-125">This parameter is optional.</span></span>
<span data-ttu-id="5afb0-126">Az alapértelmezett érték $null.</span><span class="sxs-lookup"><span data-stu-id="5afb0-126">Default value is $null.</span></span>
<span data-ttu-id="5afb0-127">Meg kell adni, ha a AuthorizationScope meg van adva.</span><span class="sxs-lookup"><span data-stu-id="5afb0-127">Must be specified if AuthorizationScope specified.</span></span>

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

### <span data-ttu-id="5afb0-128">-Környezet</span><span class="sxs-lookup"><span data-stu-id="5afb0-128">-Context</span></span>
<span data-ttu-id="5afb0-129">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="5afb0-129">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="5afb0-130">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="5afb0-130">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5afb0-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5afb0-131">-DefaultProfile</span></span>
<span data-ttu-id="5afb0-132">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5afb0-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5afb0-133">-Leírás</span><span class="sxs-lookup"><span data-stu-id="5afb0-133">-Description</span></span>
<span data-ttu-id="5afb0-134">Webes API leírása.</span><span class="sxs-lookup"><span data-stu-id="5afb0-134">Web API description.</span></span>
<span data-ttu-id="5afb0-135">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="5afb0-135">This parameter is optional.</span></span>

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

### <span data-ttu-id="5afb0-136">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5afb0-136">-InputObject</span></span>
<span data-ttu-id="5afb0-137">A PsApiManagementApi példánya.</span><span class="sxs-lookup"><span data-stu-id="5afb0-137">Instance of PsApiManagementApi.</span></span> <span data-ttu-id="5afb0-138">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="5afb0-138">This parameter is required.</span></span>

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

### <span data-ttu-id="5afb0-139">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5afb0-139">-Name</span></span>
<span data-ttu-id="5afb0-140">Web API-név.</span><span class="sxs-lookup"><span data-stu-id="5afb0-140">Web API name.</span></span>
<span data-ttu-id="5afb0-141">Az API-t a fejlesztői és a felügyeleti portálokon megjelenő nyilvános név.</span><span class="sxs-lookup"><span data-stu-id="5afb0-141">Public name of the API as it would appear on the developer and admin portals.</span></span>
<span data-ttu-id="5afb0-142">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="5afb0-142">This parameter is required.</span></span>

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

### <span data-ttu-id="5afb0-143">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5afb0-143">-PassThru</span></span>
<span data-ttu-id="5afb0-144">Ha meg van adva, akkor a Microsoft. Azure. commands. ApiManagement. ServiceManagement. models. PsApiManagementApi típusa a set API-t jelképezi.</span><span class="sxs-lookup"><span data-stu-id="5afb0-144">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi type representing the set API.</span></span>

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

### <span data-ttu-id="5afb0-145">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="5afb0-145">-Path</span></span>
<span data-ttu-id="5afb0-146">Web API-elérési út.</span><span class="sxs-lookup"><span data-stu-id="5afb0-146">Web API Path.</span></span>
<span data-ttu-id="5afb0-147">Az API nyilvános URL-címének utolsó része.</span><span class="sxs-lookup"><span data-stu-id="5afb0-147">Last part of the API's public URL.</span></span>
<span data-ttu-id="5afb0-148">Ezt az URL-címet az API-felhasználók fogják használni a webszolgáltatásra irányuló kérések elküldéséhez.</span><span class="sxs-lookup"><span data-stu-id="5afb0-148">This URL will be used by API consumers for sending requests to the web service.</span></span>
<span data-ttu-id="5afb0-149">1 – 400 karakter hosszúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="5afb0-149">Must be 1 to 400 characters long.</span></span>
<span data-ttu-id="5afb0-150">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="5afb0-150">This parameter is optional.</span></span>
<span data-ttu-id="5afb0-151">Az alapértelmezett érték $null.</span><span class="sxs-lookup"><span data-stu-id="5afb0-151">Default value is $null.</span></span>

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

### <span data-ttu-id="5afb0-152">-Protokollok</span><span class="sxs-lookup"><span data-stu-id="5afb0-152">-Protocols</span></span>
<span data-ttu-id="5afb0-153">Webes API-protokollok (http, HTTPS).</span><span class="sxs-lookup"><span data-stu-id="5afb0-153">Web API protocols (http, https).</span></span>
<span data-ttu-id="5afb0-154">Azok a protokollok, amelyek az API-t elérhetővé tették.</span><span class="sxs-lookup"><span data-stu-id="5afb0-154">Protocols over which API is made available.</span></span>
<span data-ttu-id="5afb0-155">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="5afb0-155">This parameter is required.</span></span>
<span data-ttu-id="5afb0-156">Az alapértelmezett érték $null.</span><span class="sxs-lookup"><span data-stu-id="5afb0-156">Default value is $null.</span></span>

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

### <span data-ttu-id="5afb0-157">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="5afb0-157">-ServiceUrl</span></span>
<span data-ttu-id="5afb0-158">A webszolgáltatás URL-címe kiteszi az API-t.</span><span class="sxs-lookup"><span data-stu-id="5afb0-158">A URL of the web service exposing the API.</span></span>
<span data-ttu-id="5afb0-159">Ezt az URL-címet csak az Azure API-kezelés fogja használni, és ezek nem lesznek nyilvánosan elérhetők.</span><span class="sxs-lookup"><span data-stu-id="5afb0-159">This URL will be used by Azure API Management only, and will not be made public.</span></span>
<span data-ttu-id="5afb0-160">1 – 2000 karakter hosszúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="5afb0-160">Must be 1 to 2000 characters long.</span></span>
<span data-ttu-id="5afb0-161">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="5afb0-161">This parameter is required.</span></span>

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

### <span data-ttu-id="5afb0-162">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="5afb0-162">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="5afb0-163">Az előfizetés kulcs fejlécének neve.</span><span class="sxs-lookup"><span data-stu-id="5afb0-163">Subscription key header name.</span></span>
<span data-ttu-id="5afb0-164">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="5afb0-164">This parameter is optional.</span></span>
<span data-ttu-id="5afb0-165">Az alapértelmezett érték $null.</span><span class="sxs-lookup"><span data-stu-id="5afb0-165">Default value is $null.</span></span>

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

### <span data-ttu-id="5afb0-166">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="5afb0-166">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="5afb0-167">Az előfizetés kulcs lekérdezése karakterlánc paraméterének neve.</span><span class="sxs-lookup"><span data-stu-id="5afb0-167">Subscription key query string parameter name.</span></span>
<span data-ttu-id="5afb0-168">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="5afb0-168">This parameter is optional.</span></span>
<span data-ttu-id="5afb0-169">Az alapértelmezett érték $null.</span><span class="sxs-lookup"><span data-stu-id="5afb0-169">Default value is $null.</span></span>

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

### <span data-ttu-id="5afb0-170">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5afb0-170">-Confirm</span></span>
<span data-ttu-id="5afb0-171">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5afb0-171">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5afb0-172">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5afb0-172">-WhatIf</span></span>
<span data-ttu-id="5afb0-173">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5afb0-173">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5afb0-174">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5afb0-174">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5afb0-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5afb0-175">CommonParameters</span></span>
<span data-ttu-id="5afb0-176">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5afb0-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5afb0-177">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5afb0-177">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5afb0-178">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5afb0-178">INPUTS</span></span>

### <span data-ttu-id="5afb0-179">System. String</span><span class="sxs-lookup"><span data-stu-id="5afb0-179">System.String</span></span>

### <span data-ttu-id="5afb0-180">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="5afb0-180">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="5afb0-181">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="5afb0-181">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>
<span data-ttu-id="5afb0-182">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="5afb0-182">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="5afb0-183">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementSchema []</span><span class="sxs-lookup"><span data-stu-id="5afb0-183">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="5afb0-184">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="5afb0-184">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="5afb0-185">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5afb0-185">OUTPUTS</span></span>

### <span data-ttu-id="5afb0-186">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="5afb0-186">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="5afb0-187">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5afb0-187">NOTES</span></span>

## <span data-ttu-id="5afb0-188">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5afb0-188">RELATED LINKS</span></span>

[<span data-ttu-id="5afb0-189">Get-AzureRmApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="5afb0-189">Get-AzureRmApiManagementApiRevision</span></span>](./Get-AzureRmApiManagementApiRevision.md)

[<span data-ttu-id="5afb0-190">Új – AzureRmApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="5afb0-190">New-AzureRmApiManagementApiRevision</span></span>](./New-AzureRmApiManagementApiRevision.md)

[<span data-ttu-id="5afb0-191">Remove-AzureRmApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="5afb0-191">Remove-AzureRmApiManagementApiRevision</span></span>](./Remove-AzureRmApiManagementApiRevision.md)
