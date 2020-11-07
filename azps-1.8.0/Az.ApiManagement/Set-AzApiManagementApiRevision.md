---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementapirevision
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiRevision.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiRevision.md
ms.openlocfilehash: 8b2e29da3c3f6140cbab422e74d09656c921c16c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836924"
---
# <span data-ttu-id="20aa5-101">Set-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="20aa5-101">Set-AzApiManagementApiRevision</span></span>

## <span data-ttu-id="20aa5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="20aa5-102">SYNOPSIS</span></span>
<span data-ttu-id="20aa5-103">API-módosítás módosítása</span><span class="sxs-lookup"><span data-stu-id="20aa5-103">Modifies an API Revision</span></span>

## <span data-ttu-id="20aa5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="20aa5-104">SYNTAX</span></span>

### <span data-ttu-id="20aa5-105">ExpandedParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="20aa5-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementApiRevision -ApiRevision <String> -Context <PsApiManagementContext> -ApiId <String>
 -Name <String> [-Description <String>] -ServiceUrl <String> [-Path <String>]
 -Protocols <PsApiManagementSchema[]> [-AuthorizationServerId <String>] [-AuthorizationScope <String>]
 [-SubscriptionKeyHeaderName <String>] [-SubscriptionKeyQueryParamName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20aa5-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="20aa5-106">ByInputObject</span></span>
```
Set-AzApiManagementApiRevision -InputObject <PsApiManagementApi> -Name <String> [-Description <String>]
 -ServiceUrl <String> [-Path <String>] -Protocols <PsApiManagementSchema[]> [-AuthorizationServerId <String>]
 [-AuthorizationScope <String>] [-SubscriptionKeyHeaderName <String>] [-SubscriptionKeyQueryParamName <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="20aa5-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="20aa5-107">DESCRIPTION</span></span>
<span data-ttu-id="20aa5-108">A **set-AzApiManagementApiRevision** parancsmag egy Azure API-kezelési API-módosítást módosít.</span><span class="sxs-lookup"><span data-stu-id="20aa5-108">The **Set-AzApiManagementApiRevision** cmdlet modifies an Azure API Management API Revision.</span></span>

## <span data-ttu-id="20aa5-109">Példák</span><span class="sxs-lookup"><span data-stu-id="20aa5-109">EXAMPLES</span></span>

### <span data-ttu-id="20aa5-110">Példa 1 API-módosítás módosítása</span><span class="sxs-lookup"><span data-stu-id="20aa5-110">Example 1 Modify an API Revision</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementApiRevision -Context $ApiMgmtContext -ApiId "echo-api" -ApiRevision "2" -Name "EchoApi" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @('https') -Description "Responds with what was sent" -Path "echo"
```

<span data-ttu-id="20aa5-111">A parancsmag frissíti az `2` API `echo-api` új leírását, protokollját és elérési útját.</span><span class="sxs-lookup"><span data-stu-id="20aa5-111">The cmdlet updates the `2` revision of the API `echo-api` with a new description, protocol and path.</span></span>

## <span data-ttu-id="20aa5-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="20aa5-112">PARAMETERS</span></span>

### <span data-ttu-id="20aa5-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="20aa5-113">-ApiId</span></span>
<span data-ttu-id="20aa5-114">A meglévő API-azonosító.</span><span class="sxs-lookup"><span data-stu-id="20aa5-114">Identifier of existing API.</span></span>
<span data-ttu-id="20aa5-115">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="20aa5-115">This parameter is required.</span></span>

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

### <span data-ttu-id="20aa5-116">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="20aa5-116">-ApiRevision</span></span>
<span data-ttu-id="20aa5-117">A meglévő API-verzió verziószámának azonosítója</span><span class="sxs-lookup"><span data-stu-id="20aa5-117">Identifier of existing API Revision.</span></span> <span data-ttu-id="20aa5-118">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="20aa5-118">This parameter is required.</span></span>

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

### <span data-ttu-id="20aa5-119">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="20aa5-119">-AuthorizationScope</span></span>
<span data-ttu-id="20aa5-120">OAuth-műveletek hatóköre</span><span class="sxs-lookup"><span data-stu-id="20aa5-120">OAuth operations scope.</span></span>
<span data-ttu-id="20aa5-121">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="20aa5-121">This parameter is optional.</span></span>
<span data-ttu-id="20aa5-122">Az alapértelmezett érték $null.</span><span class="sxs-lookup"><span data-stu-id="20aa5-122">Default value is $null.</span></span>

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

### <span data-ttu-id="20aa5-123">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="20aa5-123">-AuthorizationServerId</span></span>
<span data-ttu-id="20aa5-124">OAuth-engedélyezési kiszolgáló azonosítója</span><span class="sxs-lookup"><span data-stu-id="20aa5-124">OAuth authorization server identifier.</span></span>
<span data-ttu-id="20aa5-125">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="20aa5-125">This parameter is optional.</span></span>
<span data-ttu-id="20aa5-126">Az alapértelmezett érték $null.</span><span class="sxs-lookup"><span data-stu-id="20aa5-126">Default value is $null.</span></span>
<span data-ttu-id="20aa5-127">Meg kell adni, ha a AuthorizationScope meg van adva.</span><span class="sxs-lookup"><span data-stu-id="20aa5-127">Must be specified if AuthorizationScope specified.</span></span>

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

### <span data-ttu-id="20aa5-128">-Környezet</span><span class="sxs-lookup"><span data-stu-id="20aa5-128">-Context</span></span>
<span data-ttu-id="20aa5-129">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="20aa5-129">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="20aa5-130">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="20aa5-130">This parameter is required.</span></span>

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

### <span data-ttu-id="20aa5-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20aa5-131">-DefaultProfile</span></span>
<span data-ttu-id="20aa5-132">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="20aa5-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20aa5-133">-Leírás</span><span class="sxs-lookup"><span data-stu-id="20aa5-133">-Description</span></span>
<span data-ttu-id="20aa5-134">Webes API leírása.</span><span class="sxs-lookup"><span data-stu-id="20aa5-134">Web API description.</span></span>
<span data-ttu-id="20aa5-135">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="20aa5-135">This parameter is optional.</span></span>

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

### <span data-ttu-id="20aa5-136">-InputObject</span><span class="sxs-lookup"><span data-stu-id="20aa5-136">-InputObject</span></span>
<span data-ttu-id="20aa5-137">A PsApiManagementApi példánya.</span><span class="sxs-lookup"><span data-stu-id="20aa5-137">Instance of PsApiManagementApi.</span></span> <span data-ttu-id="20aa5-138">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="20aa5-138">This parameter is required.</span></span>

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

### <span data-ttu-id="20aa5-139">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="20aa5-139">-Name</span></span>
<span data-ttu-id="20aa5-140">Web API-név.</span><span class="sxs-lookup"><span data-stu-id="20aa5-140">Web API name.</span></span>
<span data-ttu-id="20aa5-141">Az API-t a fejlesztői és a felügyeleti portálokon megjelenő nyilvános név.</span><span class="sxs-lookup"><span data-stu-id="20aa5-141">Public name of the API as it would appear on the developer and admin portals.</span></span>
<span data-ttu-id="20aa5-142">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="20aa5-142">This parameter is required.</span></span>

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

### <span data-ttu-id="20aa5-143">-PassThru</span><span class="sxs-lookup"><span data-stu-id="20aa5-143">-PassThru</span></span>
<span data-ttu-id="20aa5-144">Ha meg van adva, akkor a Microsoft. Azure. commands. ApiManagement. ServiceManagement. models. PsApiManagementApi típusa a set API-t jelképezi.</span><span class="sxs-lookup"><span data-stu-id="20aa5-144">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi type representing the set API.</span></span>

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

### <span data-ttu-id="20aa5-145">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="20aa5-145">-Path</span></span>
<span data-ttu-id="20aa5-146">Web API-elérési út.</span><span class="sxs-lookup"><span data-stu-id="20aa5-146">Web API Path.</span></span>
<span data-ttu-id="20aa5-147">Az API nyilvános URL-címének utolsó része.</span><span class="sxs-lookup"><span data-stu-id="20aa5-147">Last part of the API's public URL.</span></span>
<span data-ttu-id="20aa5-148">Ezt az URL-címet az API-felhasználók fogják használni a webszolgáltatásra irányuló kérések elküldéséhez.</span><span class="sxs-lookup"><span data-stu-id="20aa5-148">This URL will be used by API consumers for sending requests to the web service.</span></span>
<span data-ttu-id="20aa5-149">1 – 400 karakter hosszúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="20aa5-149">Must be 1 to 400 characters long.</span></span>
<span data-ttu-id="20aa5-150">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="20aa5-150">This parameter is optional.</span></span>
<span data-ttu-id="20aa5-151">Az alapértelmezett érték $null.</span><span class="sxs-lookup"><span data-stu-id="20aa5-151">Default value is $null.</span></span>

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

### <span data-ttu-id="20aa5-152">-Protokollok</span><span class="sxs-lookup"><span data-stu-id="20aa5-152">-Protocols</span></span>
<span data-ttu-id="20aa5-153">Webes API-protokollok (http, HTTPS).</span><span class="sxs-lookup"><span data-stu-id="20aa5-153">Web API protocols (http, https).</span></span>
<span data-ttu-id="20aa5-154">Azok a protokollok, amelyek az API-t elérhetővé tették.</span><span class="sxs-lookup"><span data-stu-id="20aa5-154">Protocols over which API is made available.</span></span>
<span data-ttu-id="20aa5-155">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="20aa5-155">This parameter is required.</span></span>
<span data-ttu-id="20aa5-156">Az alapértelmezett érték $null.</span><span class="sxs-lookup"><span data-stu-id="20aa5-156">Default value is $null.</span></span>

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

### <span data-ttu-id="20aa5-157">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="20aa5-157">-ServiceUrl</span></span>
<span data-ttu-id="20aa5-158">A webszolgáltatás URL-címe kiteszi az API-t.</span><span class="sxs-lookup"><span data-stu-id="20aa5-158">A URL of the web service exposing the API.</span></span>
<span data-ttu-id="20aa5-159">Ezt az URL-címet csak az Azure API-kezelés fogja használni, és ezek nem lesznek nyilvánosan elérhetők.</span><span class="sxs-lookup"><span data-stu-id="20aa5-159">This URL will be used by Azure API Management only, and will not be made public.</span></span>
<span data-ttu-id="20aa5-160">1 – 2000 karakter hosszúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="20aa5-160">Must be 1 to 2000 characters long.</span></span>
<span data-ttu-id="20aa5-161">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="20aa5-161">This parameter is required.</span></span>

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

### <span data-ttu-id="20aa5-162">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="20aa5-162">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="20aa5-163">Az előfizetés kulcs fejlécének neve.</span><span class="sxs-lookup"><span data-stu-id="20aa5-163">Subscription key header name.</span></span>
<span data-ttu-id="20aa5-164">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="20aa5-164">This parameter is optional.</span></span>
<span data-ttu-id="20aa5-165">Az alapértelmezett érték $null.</span><span class="sxs-lookup"><span data-stu-id="20aa5-165">Default value is $null.</span></span>

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

### <span data-ttu-id="20aa5-166">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="20aa5-166">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="20aa5-167">Az előfizetés kulcs lekérdezése karakterlánc paraméterének neve.</span><span class="sxs-lookup"><span data-stu-id="20aa5-167">Subscription key query string parameter name.</span></span>
<span data-ttu-id="20aa5-168">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="20aa5-168">This parameter is optional.</span></span>
<span data-ttu-id="20aa5-169">Az alapértelmezett érték $null.</span><span class="sxs-lookup"><span data-stu-id="20aa5-169">Default value is $null.</span></span>

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

### <span data-ttu-id="20aa5-170">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="20aa5-170">-Confirm</span></span>
<span data-ttu-id="20aa5-171">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="20aa5-171">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20aa5-172">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20aa5-172">-WhatIf</span></span>
<span data-ttu-id="20aa5-173">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="20aa5-173">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="20aa5-174">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="20aa5-174">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20aa5-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20aa5-175">CommonParameters</span></span>
<span data-ttu-id="20aa5-176">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="20aa5-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20aa5-177">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20aa5-177">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20aa5-178">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="20aa5-178">INPUTS</span></span>

### <span data-ttu-id="20aa5-179">System. String</span><span class="sxs-lookup"><span data-stu-id="20aa5-179">System.String</span></span>

### <span data-ttu-id="20aa5-180">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="20aa5-180">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="20aa5-181">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="20aa5-181">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

### <span data-ttu-id="20aa5-182">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementSchema []</span><span class="sxs-lookup"><span data-stu-id="20aa5-182">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="20aa5-183">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="20aa5-183">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="20aa5-184">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="20aa5-184">OUTPUTS</span></span>

### <span data-ttu-id="20aa5-185">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="20aa5-185">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="20aa5-186">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="20aa5-186">NOTES</span></span>

## <span data-ttu-id="20aa5-187">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="20aa5-187">RELATED LINKS</span></span>

[<span data-ttu-id="20aa5-188">Get-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="20aa5-188">Get-AzApiManagementApiRevision</span></span>](./Get-AzApiManagementApiRevision.md)

[<span data-ttu-id="20aa5-189">Új – AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="20aa5-189">New-AzApiManagementApiRevision</span></span>](./New-AzApiManagementApiRevision.md)

[<span data-ttu-id="20aa5-190">Remove-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="20aa5-190">Remove-AzApiManagementApiRevision</span></span>](./Remove-AzApiManagementApiRevision.md)