---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 45B96AB0-ACE3-4754-B162-88027AC8CA41
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementAuthorizationServer.md
ms.openlocfilehash: 46530ce5fd72ea01abdd258feb9f7049bf9670a1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012260"
---
# <span data-ttu-id="1fc52-101">New-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="1fc52-101">New-AzApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="1fc52-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1fc52-102">SYNOPSIS</span></span>
<span data-ttu-id="1fc52-103">Engedélyezési kiszolgálót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="1fc52-103">Creates an authorization server.</span></span>

## <span data-ttu-id="1fc52-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1fc52-104">SYNTAX</span></span>

```
New-AzApiManagementAuthorizationServer -Context <PsApiManagementContext> [-ServerId <String>] -Name <String>
 [-Description <String>] -ClientRegistrationPageUrl <String> -AuthorizationEndpointUrl <String>
 -TokenEndpointUrl <String> -ClientId <String> [-ClientSecret <String>]
 [-AuthorizationRequestMethods <PsApiManagementAuthorizationRequestMethod[]>]
 -GrantTypes <PsApiManagementGrantType[]>
 -ClientAuthenticationMethods <PsApiManagementClientAuthenticationMethod[]> [-TokenBodyParameters <Hashtable>]
 [-SupportState <Boolean>] [-DefaultScope <String>]
 -AccessTokenSendingMethods <PsApiManagementAccessTokenSendingMethod[]> [-ResourceOwnerUsername <String>]
 [-ResourceOwnerPassword <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1fc52-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="1fc52-105">DESCRIPTION</span></span>
<span data-ttu-id="1fc52-106">A **New-AzApiManagementAuthorizationServer** parancsmag egy Azure API-kezelési engedélyezési kiszolgálót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="1fc52-106">The **New-AzApiManagementAuthorizationServer** cmdlet creates an Azure API Management authorization server.</span></span>

## <span data-ttu-id="1fc52-107">Példák</span><span class="sxs-lookup"><span data-stu-id="1fc52-107">EXAMPLES</span></span>

### <span data-ttu-id="1fc52-108">1. példa: engedélyezési kiszolgáló létrehozása</span><span class="sxs-lookup"><span data-stu-id="1fc52-108">Example 1: Create an authorization server</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementAuthorizationServer -Context $ApiMgmtContext -Name "Contoso OAuth2 server" -ClientRegistrationPageUrl "https://contoso/signup" -AuthorizationEndpointUrl "https://contoso/auth" -TokenEndpointUrl "https://contoso/token" -ClientId "clientid" -ClientSecret "e041ed1b660b4eadbad5a29d066e6e88" -AuthorizationRequestMethods @('Get', 'Post') -GrantTypes @( 'AuthorizationCode', 'Implicit', 'ResourceOwnerPassword', 'ClientCredentials') -ClientAuthenticationMethods @('Basic') -TokenBodyParameters @{'par1'='val1'; 'par2'='val2'} -AccessTokenSendingMethods @('AuthorizationHeader', 'Query') -ResourceOwnerUsername "ivan" -ResourceOwnerPassword "qwerty"
```

<span data-ttu-id="1fc52-109">Ez a parancs egy engedélyezési kiszolgálót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="1fc52-109">This command creates an authorization server.</span></span>

## <span data-ttu-id="1fc52-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1fc52-110">PARAMETERS</span></span>

### <span data-ttu-id="1fc52-111">-AccessTokenSendingMethods</span><span class="sxs-lookup"><span data-stu-id="1fc52-111">-AccessTokenSendingMethods</span></span>
<span data-ttu-id="1fc52-112">Az Access-tokenek küldésére szolgáló metódusok tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1fc52-112">Specifies an array of methods to send an access token.</span></span>
<span data-ttu-id="1fc52-113">psdx_paramvalues AuthorizationHeader és lekérdezés.</span><span class="sxs-lookup"><span data-stu-id="1fc52-113">psdx_paramvalues AuthorizationHeader and Query.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessTokenSendingMethod[]
Parameter Sets: (All)
Aliases:
Accepted values: AuthorizationHeader, Query

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1fc52-114">-AuthorizationEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="1fc52-114">-AuthorizationEndpointUrl</span></span>
<span data-ttu-id="1fc52-115">Megadja az engedélyezési végpontot az erőforrás-tulajdonosok hitelesítéséhez és az engedélyezési támogatás beszerzéséhez.</span><span class="sxs-lookup"><span data-stu-id="1fc52-115">Specifies the authorization endpoint to authenticate resource owners and obtain authorization grants.</span></span>

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

### <span data-ttu-id="1fc52-116">-AuthorizationRequestMethods</span><span class="sxs-lookup"><span data-stu-id="1fc52-116">-AuthorizationRequestMethods</span></span>
<span data-ttu-id="1fc52-117">Megadja az engedélyezési kérés módszereinek tömbjét.</span><span class="sxs-lookup"><span data-stu-id="1fc52-117">Specifies an array of authorization request methods.</span></span>
<span data-ttu-id="1fc52-118">Érvényes értékek: GET, POST.</span><span class="sxs-lookup"><span data-stu-id="1fc52-118">Valid values are: GET, POST.</span></span>
<span data-ttu-id="1fc52-119">Az alapértelmezett érték a beolvasás.</span><span class="sxs-lookup"><span data-stu-id="1fc52-119">The default value is GET.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAuthorizationRequestMethod[]
Parameter Sets: (All)
Aliases:
Accepted values: Get, Post, Head, Options, Trace, Put, Patch, Delete

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1fc52-120">-ClientAuthenticationMethods</span><span class="sxs-lookup"><span data-stu-id="1fc52-120">-ClientAuthenticationMethods</span></span>
<span data-ttu-id="1fc52-121">Az ügyfél-hitelesítési módszerek tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1fc52-121">Specifies an array of client authentication methods.</span></span>
<span data-ttu-id="1fc52-122">psdx_paramvalues egyszerű és a szövegtörzs.</span><span class="sxs-lookup"><span data-stu-id="1fc52-122">psdx_paramvalues Basic and Body.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementClientAuthenticationMethod[]
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Body

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1fc52-123">-ClientId</span><span class="sxs-lookup"><span data-stu-id="1fc52-123">-ClientId</span></span>
<span data-ttu-id="1fc52-124">Megadja az ügyfélalkalmazás fejlesztői konzoljának ügyfél-AZONOSÍTÓját.</span><span class="sxs-lookup"><span data-stu-id="1fc52-124">Specifies the client ID of the developer console that is the client application.</span></span>

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

### <span data-ttu-id="1fc52-125">-ClientRegistrationPageUrl</span><span class="sxs-lookup"><span data-stu-id="1fc52-125">-ClientRegistrationPageUrl</span></span>
<span data-ttu-id="1fc52-126">Az ügyfél regisztrációs végpontját adja meg az ügyfél regisztrálásához az engedélyezési kiszolgálóval, és ügyfél hitelesítő adatait kell beszereznie.</span><span class="sxs-lookup"><span data-stu-id="1fc52-126">Specifies the client registration endpoint to register clients with the authorization server and obtain client credentials.</span></span>

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

### <span data-ttu-id="1fc52-127">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="1fc52-127">-ClientSecret</span></span>
<span data-ttu-id="1fc52-128">Az ügyfélalkalmazás fejlesztői konzoljának ügyfél titkát adja meg.</span><span class="sxs-lookup"><span data-stu-id="1fc52-128">Specifies the client secret of developer console that is the client application.</span></span>

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

### <span data-ttu-id="1fc52-129">-Környezet</span><span class="sxs-lookup"><span data-stu-id="1fc52-129">-Context</span></span>
<span data-ttu-id="1fc52-130">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="1fc52-130">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="1fc52-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fc52-131">-DefaultProfile</span></span>
<span data-ttu-id="1fc52-132">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1fc52-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1fc52-133">-DefaultScope</span><span class="sxs-lookup"><span data-stu-id="1fc52-133">-DefaultScope</span></span>
<span data-ttu-id="1fc52-134">Az engedélyezési kiszolgáló alapértelmezett hatókörét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1fc52-134">Specifies the default scope for the authorization server.</span></span>

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

### <span data-ttu-id="1fc52-135">-Leírás</span><span class="sxs-lookup"><span data-stu-id="1fc52-135">-Description</span></span>
<span data-ttu-id="1fc52-136">Egy engedélyezési kiszolgáló leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="1fc52-136">Specifies a description for an authorization server.</span></span>

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

### <span data-ttu-id="1fc52-137">-GrantTypes</span><span class="sxs-lookup"><span data-stu-id="1fc52-137">-GrantTypes</span></span>
<span data-ttu-id="1fc52-138">Megadja a támogatási típusok tömbjét.</span><span class="sxs-lookup"><span data-stu-id="1fc52-138">Specifies an array of grant types.</span></span>
<span data-ttu-id="1fc52-139">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="1fc52-139">psdx_paramvalues</span></span>
- <span data-ttu-id="1fc52-140">AuthorizationCode</span><span class="sxs-lookup"><span data-stu-id="1fc52-140">AuthorizationCode</span></span>
- <span data-ttu-id="1fc52-141">ClientCredentials</span><span class="sxs-lookup"><span data-stu-id="1fc52-141">ClientCredentials</span></span> 
- <span data-ttu-id="1fc52-142">Implicit</span><span class="sxs-lookup"><span data-stu-id="1fc52-142">Implicit</span></span> 
- <span data-ttu-id="1fc52-143">ResourceOwnerPassword</span><span class="sxs-lookup"><span data-stu-id="1fc52-143">ResourceOwnerPassword</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGrantType[]
Parameter Sets: (All)
Aliases:
Accepted values: AuthorizationCode, Implicit, ResourceOwnerPassword, ClientCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1fc52-144">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1fc52-144">-Name</span></span>
<span data-ttu-id="1fc52-145">A létrehozandó engedélyezési kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1fc52-145">Specifies the name of the authorization server to create.</span></span>

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

### <span data-ttu-id="1fc52-146">-ResourceOwnerPassword</span><span class="sxs-lookup"><span data-stu-id="1fc52-146">-ResourceOwnerPassword</span></span>
<span data-ttu-id="1fc52-147">Az erőforrás tulajdonosi jelszavát adja meg.</span><span class="sxs-lookup"><span data-stu-id="1fc52-147">Specifies the resource owner password.</span></span>
<span data-ttu-id="1fc52-148">Meg kell adnia ezt a paramétert, ha a ResourceOwnerPassword a *GrantTypes* paraméter adja meg.</span><span class="sxs-lookup"><span data-stu-id="1fc52-148">You must specify this parameter is required if ResourceOwnerPassword is specified by the *GrantTypes* parameter.</span></span>

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

### <span data-ttu-id="1fc52-149">-ResourceOwnerUsername</span><span class="sxs-lookup"><span data-stu-id="1fc52-149">-ResourceOwnerUsername</span></span>
<span data-ttu-id="1fc52-150">Az erőforrás-tulajdonos felhasználónevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1fc52-150">Specifies the resource owner user name.</span></span>
<span data-ttu-id="1fc52-151">Ezt a paramétert akkor kell megadnia, ha a ResourceOwnerPassword a *GrantTypes* paraméter adja meg.</span><span class="sxs-lookup"><span data-stu-id="1fc52-151">You must specify this parameter if ResourceOwnerPassword is specified by the *GrantTypes* parameter.</span></span>

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

### <span data-ttu-id="1fc52-152">-ServerId</span><span class="sxs-lookup"><span data-stu-id="1fc52-152">-ServerId</span></span>
<span data-ttu-id="1fc52-153">A létrehozandó engedélyezési kiszolgáló AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="1fc52-153">Specifies the ID of the authorization server to create.</span></span>

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

### <span data-ttu-id="1fc52-154">-SupportState</span><span class="sxs-lookup"><span data-stu-id="1fc52-154">-SupportState</span></span>
<span data-ttu-id="1fc52-155">Azt jelzi, hogy támogatja-e az *állami* paramétereket.</span><span class="sxs-lookup"><span data-stu-id="1fc52-155">Indicates whether to support the *State* parameter.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1fc52-156">-TokenBodyParameters</span><span class="sxs-lookup"><span data-stu-id="1fc52-156">-TokenBodyParameters</span></span>
<span data-ttu-id="1fc52-157">Az **Application/x-www-Form-urlencoded** formátumban adja meg a szövegtörzs további paramétereit.</span><span class="sxs-lookup"><span data-stu-id="1fc52-157">Specifies additional body parameters using **application/x-www-form-urlencoded** format.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1fc52-158">-TokenEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="1fc52-158">-TokenEndpointUrl</span></span>
<span data-ttu-id="1fc52-159">Annak a jogkivonat-végpontnak az URL-címét adja meg, amely az ügyfelek által az engedélyezési vagy a frissítési tokenek megjelenítéséhez szükséges Exchange-hozzáférési tokenek beszerzéséhez használható.</span><span class="sxs-lookup"><span data-stu-id="1fc52-159">Specifies the token endpoint URL that is used by clients to obtain access tokens in exchange for presenting authorization grants or refresh tokens.</span></span>

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

### <span data-ttu-id="1fc52-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fc52-160">CommonParameters</span></span>
<span data-ttu-id="1fc52-161">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1fc52-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fc52-162">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="1fc52-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fc52-163">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1fc52-163">INPUTS</span></span>

### <span data-ttu-id="1fc52-164">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="1fc52-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="1fc52-165">System. String</span><span class="sxs-lookup"><span data-stu-id="1fc52-165">System.String</span></span>

### <span data-ttu-id="1fc52-166">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementAuthorizationRequestMethod []</span><span class="sxs-lookup"><span data-stu-id="1fc52-166">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAuthorizationRequestMethod[]</span></span>

### <span data-ttu-id="1fc52-167">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementGrantType []</span><span class="sxs-lookup"><span data-stu-id="1fc52-167">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGrantType[]</span></span>

### <span data-ttu-id="1fc52-168">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementClientAuthenticationMethod []</span><span class="sxs-lookup"><span data-stu-id="1fc52-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementClientAuthenticationMethod[]</span></span>

### <span data-ttu-id="1fc52-169">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="1fc52-169">System.Collections.Hashtable</span></span>

### <span data-ttu-id="1fc52-170">System. null ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="1fc52-170">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="1fc52-171">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementAccessTokenSendingMethod []</span><span class="sxs-lookup"><span data-stu-id="1fc52-171">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessTokenSendingMethod[]</span></span>

## <span data-ttu-id="1fc52-172">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1fc52-172">OUTPUTS</span></span>

### <span data-ttu-id="1fc52-173">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementOAuth2AuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="1fc52-173">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOAuth2AuthorizationServer</span></span>

## <span data-ttu-id="1fc52-174">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1fc52-174">NOTES</span></span>

## <span data-ttu-id="1fc52-175">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1fc52-175">RELATED LINKS</span></span>
