---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 664CF009-FC52-4F1B-933B-3DEBD05AC8C5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementApi.md
ms.openlocfilehash: 2601635bb3fc9ac1f6886adcb2cbb971a3cf0d63
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679632"
---
# <span data-ttu-id="aa045-101">New-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="aa045-101">New-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="aa045-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="aa045-102">SYNOPSIS</span></span>
<span data-ttu-id="aa045-103">API-t hoz létre.</span><span class="sxs-lookup"><span data-stu-id="aa045-103">Creates an API.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aa045-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="aa045-104">SYNTAX</span></span>

```
New-AzureRmApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>] -Name <String>
 [-Description <String>] -ServiceUrl <String> -Path <String> -Protocols <PsApiManagementSchema[]>
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-ProductIds <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="aa045-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="aa045-105">DESCRIPTION</span></span>
<span data-ttu-id="aa045-106">A **New-AzureRmApiManagementApi** parancsmag egy Azure API-kezelési API-t hoz létre.</span><span class="sxs-lookup"><span data-stu-id="aa045-106">The **New-AzureRmApiManagementApi** cmdlet creates an Azure API Management API.</span></span>

## <span data-ttu-id="aa045-107">Példák</span><span class="sxs-lookup"><span data-stu-id="aa045-107">EXAMPLES</span></span>

### <span data-ttu-id="aa045-108">Példa 1: API létrehozása</span><span class="sxs-lookup"><span data-stu-id="aa045-108">Example 1: Create an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementApi -Context $ApiMgmtContext -Name "Echo api" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @("http", "https") -Path "testapi"
```

<span data-ttu-id="aa045-109">A parancs létrehoz egy EchoApi nevű API-t a megadott URL-lel.</span><span class="sxs-lookup"><span data-stu-id="aa045-109">This command creates an API named EchoApi with the specified URL.</span></span>

## <span data-ttu-id="aa045-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="aa045-110">PARAMETERS</span></span>

### <span data-ttu-id="aa045-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="aa045-111">-ApiId</span></span>
<span data-ttu-id="aa045-112">A létrehozandó API AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="aa045-112">Specifies the ID of the API to create.</span></span>
<span data-ttu-id="aa045-113">Ha nem adja meg ezt a paramétert, ez a parancsmag azonosítót hoz létre Önnek.</span><span class="sxs-lookup"><span data-stu-id="aa045-113">If you do not specify this parameter, this cmdlet generates an ID for you.</span></span>

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

### <span data-ttu-id="aa045-114">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="aa045-114">-AuthorizationScope</span></span>
<span data-ttu-id="aa045-115">A OAuth-műveletek hatókörét adja meg.</span><span class="sxs-lookup"><span data-stu-id="aa045-115">Specifies the OAuth operations scope.</span></span>
<span data-ttu-id="aa045-116">Az alapértelmezett érték $Null.</span><span class="sxs-lookup"><span data-stu-id="aa045-116">The default value is $Null.</span></span>

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

### <span data-ttu-id="aa045-117">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="aa045-117">-AuthorizationServerId</span></span>
<span data-ttu-id="aa045-118">A OAuth-engedélyezési kiszolgáló AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="aa045-118">Specifies the OAuth authorization server ID.</span></span>
<span data-ttu-id="aa045-119">Az alapértelmezett érték $Null.</span><span class="sxs-lookup"><span data-stu-id="aa045-119">The default value is $Null.</span></span>
<span data-ttu-id="aa045-120">Ezt a paramétert akkor kell megadnia, ha a *AuthorizationScope* meg van adva.</span><span class="sxs-lookup"><span data-stu-id="aa045-120">You must specify this parameter if *AuthorizationScope* is specified.</span></span>

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

### <span data-ttu-id="aa045-121">-Környezet</span><span class="sxs-lookup"><span data-stu-id="aa045-121">-Context</span></span>
<span data-ttu-id="aa045-122">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="aa045-122">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="aa045-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa045-123">-DefaultProfile</span></span>
<span data-ttu-id="aa045-124">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="aa045-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aa045-125">-Leírás</span><span class="sxs-lookup"><span data-stu-id="aa045-125">-Description</span></span>
<span data-ttu-id="aa045-126">A webes API leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="aa045-126">Specifies a description for the web API.</span></span>

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

### <span data-ttu-id="aa045-127">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="aa045-127">-Name</span></span>
<span data-ttu-id="aa045-128">A webes API nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="aa045-128">Specifies the name of the web API.</span></span>
<span data-ttu-id="aa045-129">Ez az API nyilvános neve a fejlesztői és a rendszergazdai portálon.</span><span class="sxs-lookup"><span data-stu-id="aa045-129">This is the public name of the API as it appears on the developer and admin portals.</span></span>

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

### <span data-ttu-id="aa045-130">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="aa045-130">-Path</span></span>
<span data-ttu-id="aa045-131">A webes API elérési útvonalát adja meg, amely az API nyilvános URL-címe utolsó része, és a felügyeleti portál webapi URL-utótag mezőjének felel meg.</span><span class="sxs-lookup"><span data-stu-id="aa045-131">Specifies the web API path, which is the last part of the API's public URL and corresponds to the Web API URL suffix field in the admin portal.</span></span>
<span data-ttu-id="aa045-132">Ezt az URL-címet használják az API-felhasználóknak a kérések webszolgáltatáshoz való küldéséhez, és egy-egy 400 karakter hosszúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="aa045-132">This URL is used by API consumers to send requests to the web service, and must be one to 400 characters long.</span></span>
<span data-ttu-id="aa045-133">Az alapértelmezett érték $Null.</span><span class="sxs-lookup"><span data-stu-id="aa045-133">The default value is $Null.</span></span>

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

### <span data-ttu-id="aa045-134">-Termékkód</span><span class="sxs-lookup"><span data-stu-id="aa045-134">-ProductIds</span></span>
<span data-ttu-id="aa045-135">Az új API hozzáadására szolgáló termékazonosítók tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="aa045-135">Specifies an array of product IDs to which to add the new API.</span></span>

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

### <span data-ttu-id="aa045-136">-Protokollok</span><span class="sxs-lookup"><span data-stu-id="aa045-136">-Protocols</span></span>
<span data-ttu-id="aa045-137">A webes API-protokollok tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="aa045-137">Specifies an array of web API protocols.</span></span>
<span data-ttu-id="aa045-138">Érvényes értékek: http, HTTPS.</span><span class="sxs-lookup"><span data-stu-id="aa045-138">Valid values are http, https.</span></span>
<span data-ttu-id="aa045-139">Ezek azok a webes protokollok, amelyek az API-t elérhetővé tették.</span><span class="sxs-lookup"><span data-stu-id="aa045-139">These are the web protocols over which the API is made available.</span></span>
<span data-ttu-id="aa045-140">Az alapértelmezett érték $Null.</span><span class="sxs-lookup"><span data-stu-id="aa045-140">The default value is $Null.</span></span>

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

### <span data-ttu-id="aa045-141">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="aa045-141">-ServiceUrl</span></span>
<span data-ttu-id="aa045-142">Annak a webszolgáltatásnak az URL-címe, amely kiteszi az API-t.</span><span class="sxs-lookup"><span data-stu-id="aa045-142">Specifies the URL of the web service that exposes the API.</span></span>
<span data-ttu-id="aa045-143">Ezt az URL-címet csak az Azure API-kezelés használja, és nem jelenik meg nyilvánosan.</span><span class="sxs-lookup"><span data-stu-id="aa045-143">This URL is used only by Azure API Management, and is not made public.</span></span>
<span data-ttu-id="aa045-144">Az URL-címnek egy 2000 karakter hosszúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="aa045-144">The URL must be one to 2000 characters long.</span></span>

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

### <span data-ttu-id="aa045-145">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="aa045-145">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="aa045-146">Az előfizetés kulcs fejlécének nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="aa045-146">Specifies the subscription key header name.</span></span>
<span data-ttu-id="aa045-147">Az alapértelmezett érték $Null.</span><span class="sxs-lookup"><span data-stu-id="aa045-147">The default value is $Null.</span></span>

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

### <span data-ttu-id="aa045-148">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="aa045-148">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="aa045-149">Az előfizetési kulcs lekérdezési karakterláncának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="aa045-149">Specifies the subscription key query string parameter name.</span></span>
<span data-ttu-id="aa045-150">Az alapértelmezett érték $Null.</span><span class="sxs-lookup"><span data-stu-id="aa045-150">The default value is $Null.</span></span>

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

### <span data-ttu-id="aa045-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa045-151">CommonParameters</span></span>
<span data-ttu-id="aa045-152">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="aa045-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa045-153">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa045-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa045-154">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="aa045-154">INPUTS</span></span>

### <span data-ttu-id="aa045-155">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="aa045-155">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="aa045-156">System. String</span><span class="sxs-lookup"><span data-stu-id="aa045-156">System.String</span></span>

### <span data-ttu-id="aa045-157">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementSchema []</span><span class="sxs-lookup"><span data-stu-id="aa045-157">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="aa045-158">System. string []</span><span class="sxs-lookup"><span data-stu-id="aa045-158">System.String[]</span></span>

## <span data-ttu-id="aa045-159">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="aa045-159">OUTPUTS</span></span>

### <span data-ttu-id="aa045-160">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="aa045-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="aa045-161">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="aa045-161">NOTES</span></span>

## <span data-ttu-id="aa045-162">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="aa045-162">RELATED LINKS</span></span>

[<span data-ttu-id="aa045-163">Exportálás – AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="aa045-163">Export-AzureRmApiManagementApi</span></span>](./Export-AzureRmApiManagementApi.md)

[<span data-ttu-id="aa045-164">Get-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="aa045-164">Get-AzureRmApiManagementApi</span></span>](./Get-AzureRmApiManagementApi.md)

[<span data-ttu-id="aa045-165">Importálás – AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="aa045-165">Import-AzureRmApiManagementApi</span></span>](./Import-AzureRmApiManagementApi.md)

[<span data-ttu-id="aa045-166">Remove-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="aa045-166">Remove-AzureRmApiManagementApi</span></span>](./Remove-AzureRmApiManagementApi.md)

[<span data-ttu-id="aa045-167">Set-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="aa045-167">Set-AzureRmApiManagementApi</span></span>](./Set-AzureRmApiManagementApi.md)


