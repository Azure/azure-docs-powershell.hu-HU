---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 29CCF141-CC2F-4E11-8235-64025CFB5782
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementApi.md
ms.openlocfilehash: 6ab29738f181f6fece9d3b4cd679496a9add9bc5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499100"
---
# <span data-ttu-id="2b1ec-101">Set-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="2b1ec-101">Set-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="2b1ec-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2b1ec-102">SYNOPSIS</span></span>
<span data-ttu-id="2b1ec-103">Módosítja az API-t.</span><span class="sxs-lookup"><span data-stu-id="2b1ec-103">Modifies an API.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2b1ec-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2b1ec-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementApi -Context <PsApiManagementContext> -ApiId <String> -Name <String>
 [-Description <String>] -ServiceUrl <String> [-Path <String>] -Protocols <PsApiManagementSchema[]>
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2b1ec-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2b1ec-105">DESCRIPTION</span></span>
<span data-ttu-id="2b1ec-106">A **set-AzureRmApiManagementApi** parancsmag módosította az Azure API-kezelési API-t.</span><span class="sxs-lookup"><span data-stu-id="2b1ec-106">The **Set-AzureRmApiManagementApi** cmdlet modifies an Azure API Management API.</span></span>

## <span data-ttu-id="2b1ec-107">Példák</span><span class="sxs-lookup"><span data-stu-id="2b1ec-107">EXAMPLES</span></span>

### <span data-ttu-id="2b1ec-108">Példa 1 API módosítása</span><span class="sxs-lookup"><span data-stu-id="2b1ec-108">Example 1 Modify an API</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementApi -Context $ApiMgmtContext -Name "EchoApi" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @('https') -Description "Responds with what was sent" -Path "echo"
```

## <span data-ttu-id="2b1ec-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2b1ec-109">PARAMETERS</span></span>

### <span data-ttu-id="2b1ec-110">-ApiId</span><span class="sxs-lookup"><span data-stu-id="2b1ec-110">-ApiId</span></span>
<span data-ttu-id="2b1ec-111">A módosítandó API AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="2b1ec-111">Specifies the ID of the API to modify.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b1ec-112">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="2b1ec-112">-AuthorizationScope</span></span>
<span data-ttu-id="2b1ec-113">A OAuth-műveletek hatókörét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2b1ec-113">Specifies the OAuth operations scope.</span></span>
<span data-ttu-id="2b1ec-114">Az alapértelmezett érték $Null.</span><span class="sxs-lookup"><span data-stu-id="2b1ec-114">The default value is $Null.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b1ec-115">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="2b1ec-115">-AuthorizationServerId</span></span>
<span data-ttu-id="2b1ec-116">A OAuth-engedélyezési kiszolgáló azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="2b1ec-116">Specifies the OAuth authorization server identifier.</span></span>
<span data-ttu-id="2b1ec-117">Az alapértelmezett érték $Null.</span><span class="sxs-lookup"><span data-stu-id="2b1ec-117">The default value is $Null.</span></span>
<span data-ttu-id="2b1ec-118">Ezt a paramétert akkor kell megadnia, ha a *AuthorizationScope* meg van adva.</span><span class="sxs-lookup"><span data-stu-id="2b1ec-118">You must specify this parameter if *AuthorizationScope* is specified.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b1ec-119">-Környezet</span><span class="sxs-lookup"><span data-stu-id="2b1ec-119">-Context</span></span>
<span data-ttu-id="2b1ec-120">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="2b1ec-120">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b1ec-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b1ec-121">-DefaultProfile</span></span>
<span data-ttu-id="2b1ec-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2b1ec-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b1ec-123">-Leírás</span><span class="sxs-lookup"><span data-stu-id="2b1ec-123">-Description</span></span>
<span data-ttu-id="2b1ec-124">A webes API leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="2b1ec-124">Specifies a description for the web API.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b1ec-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2b1ec-125">-Name</span></span>
<span data-ttu-id="2b1ec-126">A webes API nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2b1ec-126">Specifies the name of the web API.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b1ec-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2b1ec-127">-PassThru</span></span>
<span data-ttu-id="2b1ec-128">passthru</span><span class="sxs-lookup"><span data-stu-id="2b1ec-128">passthru</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b1ec-129">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="2b1ec-129">-Path</span></span>
<span data-ttu-id="2b1ec-130">A webes API elérési útvonalát adja meg, amely az API nyilvános URL-címe utolsó része.</span><span class="sxs-lookup"><span data-stu-id="2b1ec-130">Specifies the web API path, which is the last part of the API's public URL.</span></span>
<span data-ttu-id="2b1ec-131">Ezt az URL-címet használják az API-felhasználóknak a kérések webszolgáltatáshoz való küldéséhez, és egy-egy 400 karakter hosszúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="2b1ec-131">This URL is used by API consumers to send requests to the web service, and must be one to 400 characters long.</span></span>
<span data-ttu-id="2b1ec-132">Az alapértelmezett érték $Null.</span><span class="sxs-lookup"><span data-stu-id="2b1ec-132">The default value is $Null.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b1ec-133">-Protokollok</span><span class="sxs-lookup"><span data-stu-id="2b1ec-133">-Protocols</span></span>
<span data-ttu-id="2b1ec-134">A webes API-protokollok tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2b1ec-134">Specifies an array of web API protocols.</span></span>
<span data-ttu-id="2b1ec-135">http-és HTTPS-psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="2b1ec-135">psdx_paramvalues http and https.</span></span>
<span data-ttu-id="2b1ec-136">Ezek azok a webes protokollok, amelyek az API-t elérhetővé tették.</span><span class="sxs-lookup"><span data-stu-id="2b1ec-136">These are the web protocols over which the API is made available.</span></span>
<span data-ttu-id="2b1ec-137">Az alapértelmezett érték $Null.</span><span class="sxs-lookup"><span data-stu-id="2b1ec-137">The default value is $Null.</span></span>

```yaml
Type: PsApiManagementSchema[]
Parameter Sets: (All)
Aliases: 
Accepted values: Http, Https

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b1ec-138">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="2b1ec-138">-ServiceUrl</span></span>
<span data-ttu-id="2b1ec-139">Annak a webszolgáltatásnak az URL-címe, amely kiteszi az API-t.</span><span class="sxs-lookup"><span data-stu-id="2b1ec-139">Specifies the URL of the web service that exposes the API.</span></span>
<span data-ttu-id="2b1ec-140">Ezt az URL-címet csak az Azure API-kezelés használja, és nem jelenik meg nyilvánosan.</span><span class="sxs-lookup"><span data-stu-id="2b1ec-140">This URL is used only by Azure API Management, and is not made public.</span></span>
<span data-ttu-id="2b1ec-141">Az URL-címnek egy 2000 karakter hosszúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="2b1ec-141">The URL must be one to 2000 characters long.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b1ec-142">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="2b1ec-142">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="2b1ec-143">Az előfizetési kulcs fejlécének nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2b1ec-143">Specifies the name of the subscription key header.</span></span>
<span data-ttu-id="2b1ec-144">Az alapértelmezett érték $Null.</span><span class="sxs-lookup"><span data-stu-id="2b1ec-144">The default value is $Null.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b1ec-145">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="2b1ec-145">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="2b1ec-146">Az előfizetési kulcs lekérdezési karakterlánc paraméterének a nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2b1ec-146">Specifies the name of the subscription key query string parameter.</span></span>
<span data-ttu-id="2b1ec-147">Az alapértelmezett érték $Null.</span><span class="sxs-lookup"><span data-stu-id="2b1ec-147">The default value is $Null.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b1ec-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b1ec-148">CommonParameters</span></span>
<span data-ttu-id="2b1ec-149">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2b1ec-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b1ec-150">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b1ec-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b1ec-151">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2b1ec-151">INPUTS</span></span>

### <span data-ttu-id="2b1ec-152">Nincs</span><span class="sxs-lookup"><span data-stu-id="2b1ec-152">None</span></span>
<span data-ttu-id="2b1ec-153">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="2b1ec-153">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2b1ec-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2b1ec-154">OUTPUTS</span></span>

### <span data-ttu-id="2b1ec-155">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="2b1ec-155">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="2b1ec-156">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2b1ec-156">NOTES</span></span>

## <span data-ttu-id="2b1ec-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2b1ec-157">RELATED LINKS</span></span>

[<span data-ttu-id="2b1ec-158">Exportálás – AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="2b1ec-158">Export-AzureRmApiManagementApi</span></span>](./Export-AzureRmApiManagementApi.md)

[<span data-ttu-id="2b1ec-159">Get-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="2b1ec-159">Get-AzureRmApiManagementApi</span></span>](./Get-AzureRmApiManagementApi.md)

[<span data-ttu-id="2b1ec-160">Importálás – AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="2b1ec-160">Import-AzureRmApiManagementApi</span></span>](./Import-AzureRmApiManagementApi.md)

[<span data-ttu-id="2b1ec-161">Új – AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="2b1ec-161">New-AzureRmApiManagementApi</span></span>](./New-AzureRmApiManagementApi.md)

[<span data-ttu-id="2b1ec-162">Remove-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="2b1ec-162">Remove-AzureRmApiManagementApi</span></span>](./Remove-AzureRmApiManagementApi.md)


