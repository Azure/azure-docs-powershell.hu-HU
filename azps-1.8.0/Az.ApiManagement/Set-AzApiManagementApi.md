---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 29CCF141-CC2F-4E11-8235-64025CFB5782
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApi.md
ms.openlocfilehash: 190dfb075e16b6b7eaaa0cb6fafd0145b3211654
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836929"
---
# <span data-ttu-id="dca9d-101">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="dca9d-101">Set-AzApiManagementApi</span></span>

## <span data-ttu-id="dca9d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="dca9d-102">SYNOPSIS</span></span>
<span data-ttu-id="dca9d-103">Módosítja az API-t.</span><span class="sxs-lookup"><span data-stu-id="dca9d-103">Modifies an API.</span></span>

## <span data-ttu-id="dca9d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="dca9d-104">SYNTAX</span></span>

### <span data-ttu-id="dca9d-105">ExpandedParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="dca9d-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> -Name <String> [-Description <String>]
 -ServiceUrl <String> [-Path <String>] -Protocols <PsApiManagementSchema[]> [-AuthorizationServerId <String>]
 [-AuthorizationScope <String>] [-SubscriptionKeyHeaderName <String>] [-SubscriptionKeyQueryParamName <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dca9d-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="dca9d-106">ByInputObject</span></span>
```
Set-AzApiManagementApi -InputObject <PsApiManagementApi> -Name <String> [-Description <String>]
 -ServiceUrl <String> [-Path <String>] -Protocols <PsApiManagementSchema[]> [-AuthorizationServerId <String>]
 [-AuthorizationScope <String>] [-SubscriptionKeyHeaderName <String>] [-SubscriptionKeyQueryParamName <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dca9d-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="dca9d-107">DESCRIPTION</span></span>
<span data-ttu-id="dca9d-108">A **set-AzApiManagementApi** parancsmag módosította az Azure API-kezelési API-t.</span><span class="sxs-lookup"><span data-stu-id="dca9d-108">The **Set-AzApiManagementApi** cmdlet modifies an Azure API Management API.</span></span>

## <span data-ttu-id="dca9d-109">Példák</span><span class="sxs-lookup"><span data-stu-id="dca9d-109">EXAMPLES</span></span>

### <span data-ttu-id="dca9d-110">Példa 1 API módosítása</span><span class="sxs-lookup"><span data-stu-id="dca9d-110">Example 1 Modify an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementApi -Context $ApiMgmtContext -Name "EchoApi" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @('https') -Description "Responds with what was sent" -Path "echo"
```

## <span data-ttu-id="dca9d-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="dca9d-111">PARAMETERS</span></span>

### <span data-ttu-id="dca9d-112">-ApiId</span><span class="sxs-lookup"><span data-stu-id="dca9d-112">-ApiId</span></span>
<span data-ttu-id="dca9d-113">A módosítandó API AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="dca9d-113">Specifies the ID of the API to modify.</span></span>

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

### <span data-ttu-id="dca9d-114">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="dca9d-114">-AuthorizationScope</span></span>
<span data-ttu-id="dca9d-115">A OAuth-műveletek hatókörét adja meg.</span><span class="sxs-lookup"><span data-stu-id="dca9d-115">Specifies the OAuth operations scope.</span></span>
<span data-ttu-id="dca9d-116">Az alapértelmezett érték $Null.</span><span class="sxs-lookup"><span data-stu-id="dca9d-116">The default value is $Null.</span></span>

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

### <span data-ttu-id="dca9d-117">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="dca9d-117">-AuthorizationServerId</span></span>
<span data-ttu-id="dca9d-118">A OAuth-engedélyezési kiszolgáló azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="dca9d-118">Specifies the OAuth authorization server identifier.</span></span>
<span data-ttu-id="dca9d-119">Az alapértelmezett érték $Null.</span><span class="sxs-lookup"><span data-stu-id="dca9d-119">The default value is $Null.</span></span>
<span data-ttu-id="dca9d-120">Ezt a paramétert akkor kell megadnia, ha a *AuthorizationScope* meg van adva.</span><span class="sxs-lookup"><span data-stu-id="dca9d-120">You must specify this parameter if *AuthorizationScope* is specified.</span></span>

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

### <span data-ttu-id="dca9d-121">-Környezet</span><span class="sxs-lookup"><span data-stu-id="dca9d-121">-Context</span></span>
<span data-ttu-id="dca9d-122">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="dca9d-122">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="dca9d-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dca9d-123">-DefaultProfile</span></span>
<span data-ttu-id="dca9d-124">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="dca9d-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dca9d-125">-Leírás</span><span class="sxs-lookup"><span data-stu-id="dca9d-125">-Description</span></span>
<span data-ttu-id="dca9d-126">A webes API leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="dca9d-126">Specifies a description for the web API.</span></span>

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

### <span data-ttu-id="dca9d-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dca9d-127">-InputObject</span></span>
<span data-ttu-id="dca9d-128">A PsApiManagementApi példánya.</span><span class="sxs-lookup"><span data-stu-id="dca9d-128">Instance of PsApiManagementApi.</span></span> <span data-ttu-id="dca9d-129">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="dca9d-129">This parameter is required.</span></span>

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

### <span data-ttu-id="dca9d-130">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="dca9d-130">-Name</span></span>
<span data-ttu-id="dca9d-131">A webes API nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="dca9d-131">Specifies the name of the web API.</span></span>

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

### <span data-ttu-id="dca9d-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dca9d-132">-PassThru</span></span>
<span data-ttu-id="dca9d-133">passthru</span><span class="sxs-lookup"><span data-stu-id="dca9d-133">passthru</span></span>

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

### <span data-ttu-id="dca9d-134">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="dca9d-134">-Path</span></span>
<span data-ttu-id="dca9d-135">A webes API elérési útvonalát adja meg, amely az API nyilvános URL-címe utolsó része.</span><span class="sxs-lookup"><span data-stu-id="dca9d-135">Specifies the web API path, which is the last part of the API's public URL.</span></span>
<span data-ttu-id="dca9d-136">Ezt az URL-címet használják az API-felhasználóknak a kérések webszolgáltatáshoz való küldéséhez, és egy-egy 400 karakter hosszúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="dca9d-136">This URL is used by API consumers to send requests to the web service, and must be one to 400 characters long.</span></span>
<span data-ttu-id="dca9d-137">Az alapértelmezett érték $Null.</span><span class="sxs-lookup"><span data-stu-id="dca9d-137">The default value is $Null.</span></span>

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

### <span data-ttu-id="dca9d-138">-Protokollok</span><span class="sxs-lookup"><span data-stu-id="dca9d-138">-Protocols</span></span>
<span data-ttu-id="dca9d-139">A webes API-protokollok tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="dca9d-139">Specifies an array of web API protocols.</span></span>
<span data-ttu-id="dca9d-140">http-és HTTPS-psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="dca9d-140">psdx_paramvalues http and https.</span></span>
<span data-ttu-id="dca9d-141">Ezek azok a webes protokollok, amelyek az API-t elérhetővé tették.</span><span class="sxs-lookup"><span data-stu-id="dca9d-141">These are the web protocols over which the API is made available.</span></span>
<span data-ttu-id="dca9d-142">Az alapértelmezett érték $Null.</span><span class="sxs-lookup"><span data-stu-id="dca9d-142">The default value is $Null.</span></span>

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

### <span data-ttu-id="dca9d-143">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="dca9d-143">-ServiceUrl</span></span>
<span data-ttu-id="dca9d-144">Annak a webszolgáltatásnak az URL-címe, amely kiteszi az API-t.</span><span class="sxs-lookup"><span data-stu-id="dca9d-144">Specifies the URL of the web service that exposes the API.</span></span>
<span data-ttu-id="dca9d-145">Ezt az URL-címet csak az Azure API-kezelés használja, és nem jelenik meg nyilvánosan.</span><span class="sxs-lookup"><span data-stu-id="dca9d-145">This URL is used only by Azure API Management, and is not made public.</span></span>
<span data-ttu-id="dca9d-146">Az URL-címnek egy 2000 karakter hosszúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="dca9d-146">The URL must be one to 2000 characters long.</span></span>

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

### <span data-ttu-id="dca9d-147">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="dca9d-147">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="dca9d-148">Az előfizetési kulcs fejlécének nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="dca9d-148">Specifies the name of the subscription key header.</span></span>
<span data-ttu-id="dca9d-149">Az alapértelmezett érték $Null.</span><span class="sxs-lookup"><span data-stu-id="dca9d-149">The default value is $Null.</span></span>

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

### <span data-ttu-id="dca9d-150">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="dca9d-150">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="dca9d-151">Az előfizetési kulcs lekérdezési karakterlánc paraméterének a nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="dca9d-151">Specifies the name of the subscription key query string parameter.</span></span>
<span data-ttu-id="dca9d-152">Az alapértelmezett érték $Null.</span><span class="sxs-lookup"><span data-stu-id="dca9d-152">The default value is $Null.</span></span>

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

### <span data-ttu-id="dca9d-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dca9d-153">CommonParameters</span></span>
<span data-ttu-id="dca9d-154">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="dca9d-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dca9d-155">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dca9d-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dca9d-156">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="dca9d-156">INPUTS</span></span>

### <span data-ttu-id="dca9d-157">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="dca9d-157">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="dca9d-158">System. String</span><span class="sxs-lookup"><span data-stu-id="dca9d-158">System.String</span></span>

### <span data-ttu-id="dca9d-159">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="dca9d-159">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

### <span data-ttu-id="dca9d-160">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementSchema []</span><span class="sxs-lookup"><span data-stu-id="dca9d-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="dca9d-161">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="dca9d-161">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="dca9d-162">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dca9d-162">OUTPUTS</span></span>

### <span data-ttu-id="dca9d-163">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="dca9d-163">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="dca9d-164">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="dca9d-164">NOTES</span></span>

## <span data-ttu-id="dca9d-165">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dca9d-165">RELATED LINKS</span></span>

[<span data-ttu-id="dca9d-166">Exportálás – AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="dca9d-166">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="dca9d-167">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="dca9d-167">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="dca9d-168">Importálás – AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="dca9d-168">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="dca9d-169">Új – AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="dca9d-169">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="dca9d-170">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="dca9d-170">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)


