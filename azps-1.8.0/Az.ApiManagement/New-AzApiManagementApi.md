---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 664CF009-FC52-4F1B-933B-3DEBD05AC8C5
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApi.md
ms.openlocfilehash: 43793ef7d1d3f9a4e5e63687e1eaf785d237e86b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93665650"
---
# <span data-ttu-id="79b0c-101">New-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="79b0c-101">New-AzApiManagementApi</span></span>

## <span data-ttu-id="79b0c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="79b0c-102">SYNOPSIS</span></span>
<span data-ttu-id="79b0c-103">API-t hoz létre.</span><span class="sxs-lookup"><span data-stu-id="79b0c-103">Creates an API.</span></span>

## <span data-ttu-id="79b0c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="79b0c-104">SYNTAX</span></span>

```
New-AzApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>] -Name <String>
 [-Description <String>] -ServiceUrl <String> -Path <String> -Protocols <PsApiManagementSchema[]>
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-ProductIds <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="79b0c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="79b0c-105">DESCRIPTION</span></span>
<span data-ttu-id="79b0c-106">A **New-AzApiManagementApi** parancsmag egy Azure API-kezelési API-t hoz létre.</span><span class="sxs-lookup"><span data-stu-id="79b0c-106">The **New-AzApiManagementApi** cmdlet creates an Azure API Management API.</span></span>

## <span data-ttu-id="79b0c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="79b0c-107">EXAMPLES</span></span>

### <span data-ttu-id="79b0c-108">Példa 1: API létrehozása</span><span class="sxs-lookup"><span data-stu-id="79b0c-108">Example 1: Create an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementApi -Context $ApiMgmtContext -Name "Echo api" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @("http", "https") -Path "testapi"
```

<span data-ttu-id="79b0c-109">A parancs létrehoz egy EchoApi nevű API-t a megadott URL-lel.</span><span class="sxs-lookup"><span data-stu-id="79b0c-109">This command creates an API named EchoApi with the specified URL.</span></span>

## <span data-ttu-id="79b0c-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="79b0c-110">PARAMETERS</span></span>

### <span data-ttu-id="79b0c-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="79b0c-111">-ApiId</span></span>
<span data-ttu-id="79b0c-112">A létrehozandó API AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="79b0c-112">Specifies the ID of the API to create.</span></span>
<span data-ttu-id="79b0c-113">Ha nem adja meg ezt a paramétert, ez a parancsmag azonosítót hoz létre Önnek.</span><span class="sxs-lookup"><span data-stu-id="79b0c-113">If you do not specify this parameter, this cmdlet generates an ID for you.</span></span>

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

### <span data-ttu-id="79b0c-114">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="79b0c-114">-AuthorizationScope</span></span>
<span data-ttu-id="79b0c-115">A OAuth-műveletek hatókörét adja meg.</span><span class="sxs-lookup"><span data-stu-id="79b0c-115">Specifies the OAuth operations scope.</span></span>
<span data-ttu-id="79b0c-116">Az alapértelmezett érték $Null.</span><span class="sxs-lookup"><span data-stu-id="79b0c-116">The default value is $Null.</span></span>

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

### <span data-ttu-id="79b0c-117">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="79b0c-117">-AuthorizationServerId</span></span>
<span data-ttu-id="79b0c-118">A OAuth-engedélyezési kiszolgáló AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="79b0c-118">Specifies the OAuth authorization server ID.</span></span>
<span data-ttu-id="79b0c-119">Az alapértelmezett érték $Null.</span><span class="sxs-lookup"><span data-stu-id="79b0c-119">The default value is $Null.</span></span>
<span data-ttu-id="79b0c-120">Ezt a paramétert akkor kell megadnia, ha a *AuthorizationScope* meg van adva.</span><span class="sxs-lookup"><span data-stu-id="79b0c-120">You must specify this parameter if *AuthorizationScope* is specified.</span></span>

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

### <span data-ttu-id="79b0c-121">-Környezet</span><span class="sxs-lookup"><span data-stu-id="79b0c-121">-Context</span></span>
<span data-ttu-id="79b0c-122">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="79b0c-122">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79b0c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79b0c-123">-DefaultProfile</span></span>
<span data-ttu-id="79b0c-124">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="79b0c-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="79b0c-125">-Leírás</span><span class="sxs-lookup"><span data-stu-id="79b0c-125">-Description</span></span>
<span data-ttu-id="79b0c-126">A webes API leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="79b0c-126">Specifies a description for the web API.</span></span>

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

### <span data-ttu-id="79b0c-127">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="79b0c-127">-Name</span></span>
<span data-ttu-id="79b0c-128">A webes API nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="79b0c-128">Specifies the name of the web API.</span></span>
<span data-ttu-id="79b0c-129">Ez az API nyilvános neve a fejlesztői és a rendszergazdai portálon.</span><span class="sxs-lookup"><span data-stu-id="79b0c-129">This is the public name of the API as it appears on the developer and admin portals.</span></span>

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

### <span data-ttu-id="79b0c-130">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="79b0c-130">-Path</span></span>
<span data-ttu-id="79b0c-131">A webes API elérési útvonalát adja meg, amely az API nyilvános URL-címe utolsó része, és a felügyeleti portál webapi URL-utótag mezőjének felel meg.</span><span class="sxs-lookup"><span data-stu-id="79b0c-131">Specifies the web API path, which is the last part of the API's public URL and corresponds to the Web API URL suffix field in the admin portal.</span></span>
<span data-ttu-id="79b0c-132">Ezt az URL-címet használják az API-felhasználóknak a kérések webszolgáltatáshoz való küldéséhez, és egy-egy 400 karakter hosszúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="79b0c-132">This URL is used by API consumers to send requests to the web service, and must be one to 400 characters long.</span></span>
<span data-ttu-id="79b0c-133">Az alapértelmezett érték $Null.</span><span class="sxs-lookup"><span data-stu-id="79b0c-133">The default value is $Null.</span></span>

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

### <span data-ttu-id="79b0c-134">-Termékkód</span><span class="sxs-lookup"><span data-stu-id="79b0c-134">-ProductIds</span></span>
<span data-ttu-id="79b0c-135">Az új API hozzáadására szolgáló termékazonosítók tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="79b0c-135">Specifies an array of product IDs to which to add the new API.</span></span>

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

### <span data-ttu-id="79b0c-136">-Protokollok</span><span class="sxs-lookup"><span data-stu-id="79b0c-136">-Protocols</span></span>
<span data-ttu-id="79b0c-137">A webes API-protokollok tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="79b0c-137">Specifies an array of web API protocols.</span></span>
<span data-ttu-id="79b0c-138">Érvényes értékek: http, HTTPS.</span><span class="sxs-lookup"><span data-stu-id="79b0c-138">Valid values are http, https.</span></span>
<span data-ttu-id="79b0c-139">Ezek azok a webes protokollok, amelyek az API-t elérhetővé tették.</span><span class="sxs-lookup"><span data-stu-id="79b0c-139">These are the web protocols over which the API is made available.</span></span>
<span data-ttu-id="79b0c-140">Az alapértelmezett érték $Null.</span><span class="sxs-lookup"><span data-stu-id="79b0c-140">The default value is $Null.</span></span>

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

### <span data-ttu-id="79b0c-141">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="79b0c-141">-ServiceUrl</span></span>
<span data-ttu-id="79b0c-142">Annak a webszolgáltatásnak az URL-címe, amely kiteszi az API-t.</span><span class="sxs-lookup"><span data-stu-id="79b0c-142">Specifies the URL of the web service that exposes the API.</span></span>
<span data-ttu-id="79b0c-143">Ezt az URL-címet csak az Azure API-kezelés használja, és nem jelenik meg nyilvánosan.</span><span class="sxs-lookup"><span data-stu-id="79b0c-143">This URL is used only by Azure API Management, and is not made public.</span></span>
<span data-ttu-id="79b0c-144">Az URL-címnek egy 2000 karakter hosszúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="79b0c-144">The URL must be one to 2000 characters long.</span></span>

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

### <span data-ttu-id="79b0c-145">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="79b0c-145">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="79b0c-146">Az előfizetés kulcs fejlécének nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="79b0c-146">Specifies the subscription key header name.</span></span>
<span data-ttu-id="79b0c-147">Az alapértelmezett érték $Null.</span><span class="sxs-lookup"><span data-stu-id="79b0c-147">The default value is $Null.</span></span>

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

### <span data-ttu-id="79b0c-148">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="79b0c-148">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="79b0c-149">Az előfizetési kulcs lekérdezési karakterláncának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="79b0c-149">Specifies the subscription key query string parameter name.</span></span>
<span data-ttu-id="79b0c-150">Az alapértelmezett érték $Null.</span><span class="sxs-lookup"><span data-stu-id="79b0c-150">The default value is $Null.</span></span>

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

### <span data-ttu-id="79b0c-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79b0c-151">CommonParameters</span></span>
<span data-ttu-id="79b0c-152">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="79b0c-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79b0c-153">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79b0c-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79b0c-154">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="79b0c-154">INPUTS</span></span>

### <span data-ttu-id="79b0c-155">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="79b0c-155">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="79b0c-156">System. String</span><span class="sxs-lookup"><span data-stu-id="79b0c-156">System.String</span></span>

### <span data-ttu-id="79b0c-157">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementSchema []</span><span class="sxs-lookup"><span data-stu-id="79b0c-157">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="79b0c-158">System. string []</span><span class="sxs-lookup"><span data-stu-id="79b0c-158">System.String[]</span></span>

## <span data-ttu-id="79b0c-159">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="79b0c-159">OUTPUTS</span></span>

### <span data-ttu-id="79b0c-160">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="79b0c-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="79b0c-161">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="79b0c-161">NOTES</span></span>

## <span data-ttu-id="79b0c-162">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="79b0c-162">RELATED LINKS</span></span>

[<span data-ttu-id="79b0c-163">Exportálás – AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="79b0c-163">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="79b0c-164">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="79b0c-164">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="79b0c-165">Importálás – AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="79b0c-165">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="79b0c-166">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="79b0c-166">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="79b0c-167">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="79b0c-167">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


