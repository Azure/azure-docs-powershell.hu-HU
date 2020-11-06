---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 664CF009-FC52-4F1B-933B-3DEBD05AC8C5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementApi.md
ms.openlocfilehash: 295551f9d4ddf751980ec81626e3714a37aa47a4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498084"
---
# <span data-ttu-id="075ca-101">New-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="075ca-101">New-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="075ca-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="075ca-102">SYNOPSIS</span></span>
<span data-ttu-id="075ca-103">API-t hoz létre.</span><span class="sxs-lookup"><span data-stu-id="075ca-103">Creates an API.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="075ca-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="075ca-104">SYNTAX</span></span>

```
New-AzureRmApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>] -Name <String>
 [-Description <String>] -ServiceUrl <String> -Path <String> -Protocols <PsApiManagementSchema[]>
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-ProductIds <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="075ca-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="075ca-105">DESCRIPTION</span></span>
<span data-ttu-id="075ca-106">A **New-AzureRmApiManagementApi** parancsmag egy Azure API-kezelési API-t hoz létre.</span><span class="sxs-lookup"><span data-stu-id="075ca-106">The **New-AzureRmApiManagementApi** cmdlet creates an Azure API Management API.</span></span>

## <span data-ttu-id="075ca-107">Példák</span><span class="sxs-lookup"><span data-stu-id="075ca-107">EXAMPLES</span></span>

### <span data-ttu-id="075ca-108">Példa 1: API létrehozása</span><span class="sxs-lookup"><span data-stu-id="075ca-108">Example 1: Create an API</span></span>
```
PS C:\>New-AzureRmApiManagementApi -Context $ApiMgmtContext -Name "Echo api" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @("http", "https") -Path "testapi"
```

<span data-ttu-id="075ca-109">A parancs létrehoz egy EchoApi nevű API-t a megadott URL-lel.</span><span class="sxs-lookup"><span data-stu-id="075ca-109">This command creates an API named EchoApi with the specified URL.</span></span>

## <span data-ttu-id="075ca-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="075ca-110">PARAMETERS</span></span>

### <span data-ttu-id="075ca-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="075ca-111">-ApiId</span></span>
<span data-ttu-id="075ca-112">A létrehozandó API AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="075ca-112">Specifies the ID of the API to create.</span></span>
<span data-ttu-id="075ca-113">Ha nem adja meg ezt a paramétert, ez a parancsmag azonosítót hoz létre Önnek.</span><span class="sxs-lookup"><span data-stu-id="075ca-113">If you do not specify this parameter, this cmdlet generates an ID for you.</span></span>

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

### <span data-ttu-id="075ca-114">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="075ca-114">-AuthorizationScope</span></span>
<span data-ttu-id="075ca-115">A OAuth-műveletek hatókörét adja meg.</span><span class="sxs-lookup"><span data-stu-id="075ca-115">Specifies the OAuth operations scope.</span></span>
<span data-ttu-id="075ca-116">Az alapértelmezett érték $Null.</span><span class="sxs-lookup"><span data-stu-id="075ca-116">The default value is $Null.</span></span>

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

### <span data-ttu-id="075ca-117">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="075ca-117">-AuthorizationServerId</span></span>
<span data-ttu-id="075ca-118">A OAuth-engedélyezési kiszolgáló AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="075ca-118">Specifies the OAuth authorization server ID.</span></span>
<span data-ttu-id="075ca-119">Az alapértelmezett érték $Null.</span><span class="sxs-lookup"><span data-stu-id="075ca-119">The default value is $Null.</span></span>
<span data-ttu-id="075ca-120">Ezt a paramétert akkor kell megadnia, ha a *AuthorizationScope* meg van adva.</span><span class="sxs-lookup"><span data-stu-id="075ca-120">You must specify this parameter if *AuthorizationScope* is specified.</span></span>

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

### <span data-ttu-id="075ca-121">-Környezet</span><span class="sxs-lookup"><span data-stu-id="075ca-121">-Context</span></span>
<span data-ttu-id="075ca-122">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="075ca-122">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="075ca-123">-Leírás</span><span class="sxs-lookup"><span data-stu-id="075ca-123">-Description</span></span>
<span data-ttu-id="075ca-124">A webes API leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="075ca-124">Specifies a description for the web API.</span></span>

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

### <span data-ttu-id="075ca-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="075ca-125">-Name</span></span>
<span data-ttu-id="075ca-126">A webes API nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="075ca-126">Specifies the name of the web API.</span></span>
<span data-ttu-id="075ca-127">Ez az API nyilvános neve a fejlesztői és a rendszergazdai portálon.</span><span class="sxs-lookup"><span data-stu-id="075ca-127">This is the public name of the API as it appears on the developer and admin portals.</span></span>

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

### <span data-ttu-id="075ca-128">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="075ca-128">-Path</span></span>
<span data-ttu-id="075ca-129">A webes API elérési útvonalát adja meg, amely az API nyilvános URL-címe utolsó része, és a felügyeleti portál webapi URL-utótag mezőjének felel meg.</span><span class="sxs-lookup"><span data-stu-id="075ca-129">Specifies the web API path, which is the last part of the API's public URL and corresponds to the Web API URL suffix field in the admin portal.</span></span>
<span data-ttu-id="075ca-130">Ezt az URL-címet használják az API-felhasználóknak a kérések webszolgáltatáshoz való küldéséhez, és egy-egy 400 karakter hosszúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="075ca-130">This URL is used by API consumers to send requests to the web service, and must be one to 400 characters long.</span></span>
<span data-ttu-id="075ca-131">Az alapértelmezett érték $Null.</span><span class="sxs-lookup"><span data-stu-id="075ca-131">The default value is $Null.</span></span>

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

### <span data-ttu-id="075ca-132">-Termékkód</span><span class="sxs-lookup"><span data-stu-id="075ca-132">-ProductIds</span></span>
<span data-ttu-id="075ca-133">Az új API hozzáadására szolgáló termékazonosítók tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="075ca-133">Specifies an array of product IDs to which to add the new API.</span></span>

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

### <span data-ttu-id="075ca-134">-Protokollok</span><span class="sxs-lookup"><span data-stu-id="075ca-134">-Protocols</span></span>
<span data-ttu-id="075ca-135">A webes API-protokollok tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="075ca-135">Specifies an array of web API protocols.</span></span>
<span data-ttu-id="075ca-136">Érvényes értékek: http, HTTPS.</span><span class="sxs-lookup"><span data-stu-id="075ca-136">Valid values are http, https.</span></span>
<span data-ttu-id="075ca-137">Ezek azok a webes protokollok, amelyek az API-t elérhetővé tették.</span><span class="sxs-lookup"><span data-stu-id="075ca-137">These are the web protocols over which the API is made available.</span></span>
<span data-ttu-id="075ca-138">Az alapértelmezett érték $Null.</span><span class="sxs-lookup"><span data-stu-id="075ca-138">The default value is $Null.</span></span>

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

### <span data-ttu-id="075ca-139">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="075ca-139">-ServiceUrl</span></span>
<span data-ttu-id="075ca-140">Annak a webszolgáltatásnak az URL-címe, amely kiteszi az API-t.</span><span class="sxs-lookup"><span data-stu-id="075ca-140">Specifies the URL of the web service that exposes the API.</span></span>
<span data-ttu-id="075ca-141">Ezt az URL-címet csak az Azure API-kezelés használja, és nem jelenik meg nyilvánosan.</span><span class="sxs-lookup"><span data-stu-id="075ca-141">This URL is used only by Azure API Management, and is not made public.</span></span>
<span data-ttu-id="075ca-142">Az URL-címnek egy 2000 karakter hosszúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="075ca-142">The URL must be one to 2000 characters long.</span></span>

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

### <span data-ttu-id="075ca-143">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="075ca-143">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="075ca-144">Az előfizetés kulcs fejlécének nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="075ca-144">Specifies the subscription key header name.</span></span>
<span data-ttu-id="075ca-145">Az alapértelmezett érték $Null.</span><span class="sxs-lookup"><span data-stu-id="075ca-145">The default value is $Null.</span></span>

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

### <span data-ttu-id="075ca-146">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="075ca-146">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="075ca-147">Az előfizetési kulcs lekérdezési karakterláncának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="075ca-147">Specifies the subscription key query string parameter name.</span></span>
<span data-ttu-id="075ca-148">Az alapértelmezett érték $Null.</span><span class="sxs-lookup"><span data-stu-id="075ca-148">The default value is $Null.</span></span>

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

### <span data-ttu-id="075ca-149">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="075ca-149">-DefaultProfile</span></span>
<span data-ttu-id="075ca-150">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="075ca-150">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="075ca-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="075ca-151">CommonParameters</span></span>
<span data-ttu-id="075ca-152">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="075ca-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="075ca-153">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="075ca-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="075ca-154">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="075ca-154">INPUTS</span></span>

## <span data-ttu-id="075ca-155">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="075ca-155">OUTPUTS</span></span>

### <span data-ttu-id="075ca-156">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="075ca-156">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="075ca-157">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="075ca-157">NOTES</span></span>

## <span data-ttu-id="075ca-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="075ca-158">RELATED LINKS</span></span>

[<span data-ttu-id="075ca-159">Exportálás – AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="075ca-159">Export-AzureRmApiManagementApi</span></span>](./Export-AzureRmApiManagementApi.md)

[<span data-ttu-id="075ca-160">Get-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="075ca-160">Get-AzureRmApiManagementApi</span></span>](./Get-AzureRmApiManagementApi.md)

[<span data-ttu-id="075ca-161">Importálás – AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="075ca-161">Import-AzureRmApiManagementApi</span></span>](./Import-AzureRmApiManagementApi.md)

[<span data-ttu-id="075ca-162">Remove-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="075ca-162">Remove-AzureRmApiManagementApi</span></span>](./Remove-AzureRmApiManagementApi.md)

[<span data-ttu-id="075ca-163">Set-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="075ca-163">Set-AzureRmApiManagementApi</span></span>](./Set-AzureRmApiManagementApi.md)


