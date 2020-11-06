---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 45B96AB0-ACE3-4754-B162-88027AC8CA41
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementAuthorizationServer.md
ms.openlocfilehash: 636391b427702b1b66dff284f8a16264bf1b1f12
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494222"
---
# <span data-ttu-id="d06b9-101">New-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="d06b9-101">New-AzureRmApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="d06b9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d06b9-102">SYNOPSIS</span></span>
<span data-ttu-id="d06b9-103">Engedélyezési kiszolgálót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="d06b9-103">Creates an authorization server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d06b9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d06b9-104">SYNTAX</span></span>

```
New-AzureRmApiManagementAuthorizationServer -Context <PsApiManagementContext> [-ServerId <String>]
 -Name <String> [-Description <String>] -ClientRegistrationPageUrl <String> -AuthorizationEndpointUrl <String>
 -TokenEndpointUrl <String> -ClientId <String> [-ClientSecret <String>]
 [-AuthorizationRequestMethods <PsApiManagementAuthorizationRequestMethod[]>]
 -GrantTypes <PsApiManagementGrantType[]>
 -ClientAuthenticationMethods <PsApiManagementClientAuthenticationMethod[]> [-TokenBodyParameters <Hashtable>]
 [-SupportState <Boolean>] [-DefaultScope <String>]
 -AccessTokenSendingMethods <PsApiManagementAccessTokenSendingMethod[]> [-ResourceOwnerUsername <String>]
 [-ResourceOwnerPassword <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d06b9-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d06b9-105">DESCRIPTION</span></span>
<span data-ttu-id="d06b9-106">A **New-AzureRmApiManagementAuthorizationServer** parancsmag egy Azure API-kezelési engedélyezési kiszolgálót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="d06b9-106">The **New-AzureRmApiManagementAuthorizationServer** cmdlet creates an Azure API Management authorization server.</span></span>

## <span data-ttu-id="d06b9-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d06b9-107">EXAMPLES</span></span>

### <span data-ttu-id="d06b9-108">1. példa: engedélyezési kiszolgáló létrehozása</span><span class="sxs-lookup"><span data-stu-id="d06b9-108">Example 1: Create an authorization server</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementAuthrizarionServer -Context $ApiMgmtContext -Name "Contoso OAuth2 server" -ClientRegistrationPageUrl "https://contoso/signup" -AuthorizationEndpointUrl "https://contoso/auth" -TokenEndpointUrl "https://contoso/token" -ClientId "clientid" -ClientSecret "e041ed1b660b4eadbad5a29d066e6e88" -AuthorizationRequestMethods @('Get', 'Post') -GrantTypes @( 'AuthorizationCode', 'Implicit', 'ResourceOwnerPassword', 'ClientCredentials') -ClientAuthenticationMethods @('Basic') -TokenBodyParameters @{'par1'='val1'; 'par2'='val2'} -AccessTokenSendingMethods @('AuthorizationHeader', 'Query') -ResourceOwnerUsername "ivan" -ResourceOwnerPassword "qwerty"
```

<span data-ttu-id="d06b9-109">Ez a parancs egy engedélyezési kiszolgálót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="d06b9-109">This command creates an authorization server.</span></span>

## <span data-ttu-id="d06b9-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d06b9-110">PARAMETERS</span></span>

### <span data-ttu-id="d06b9-111">-AccessTokenSendingMethods</span><span class="sxs-lookup"><span data-stu-id="d06b9-111">-AccessTokenSendingMethods</span></span>
<span data-ttu-id="d06b9-112">Az Access-tokenek küldésére szolgáló metódusok tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d06b9-112">Specifies an array of methods to send an access token.</span></span>
<span data-ttu-id="d06b9-113">psdx_paramvalues AuthorizationHeader és lekérdezés.</span><span class="sxs-lookup"><span data-stu-id="d06b9-113">psdx_paramvalues AuthorizationHeader and Query.</span></span>

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

### <span data-ttu-id="d06b9-114">-AuthorizationEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="d06b9-114">-AuthorizationEndpointUrl</span></span>
<span data-ttu-id="d06b9-115">Megadja az engedélyezési végpontot az erőforrás-tulajdonosok hitelesítéséhez és az engedélyezési támogatás beszerzéséhez.</span><span class="sxs-lookup"><span data-stu-id="d06b9-115">Specifies the authorization endpoint to authenticate resource owners and obtain authorization grants.</span></span>

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

### <span data-ttu-id="d06b9-116">-AuthorizationRequestMethods</span><span class="sxs-lookup"><span data-stu-id="d06b9-116">-AuthorizationRequestMethods</span></span>
<span data-ttu-id="d06b9-117">Megadja az engedélyezési kérés módszereinek tömbjét.</span><span class="sxs-lookup"><span data-stu-id="d06b9-117">Specifies an array of authorization request methods.</span></span>
<span data-ttu-id="d06b9-118">Érvényes értékek: GET, POST.</span><span class="sxs-lookup"><span data-stu-id="d06b9-118">Valid values are: GET, POST.</span></span>
<span data-ttu-id="d06b9-119">Az alapértelmezett érték a beolvasás.</span><span class="sxs-lookup"><span data-stu-id="d06b9-119">The default value is GET.</span></span>

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

### <span data-ttu-id="d06b9-120">-ClientAuthenticationMethods</span><span class="sxs-lookup"><span data-stu-id="d06b9-120">-ClientAuthenticationMethods</span></span>
<span data-ttu-id="d06b9-121">Az ügyfél-hitelesítési módszerek tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d06b9-121">Specifies an array of client authentication methods.</span></span>
<span data-ttu-id="d06b9-122">psdx_paramvalues egyszerű és a szövegtörzs.</span><span class="sxs-lookup"><span data-stu-id="d06b9-122">psdx_paramvalues Basic and Body.</span></span>

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

### <span data-ttu-id="d06b9-123">-ClientId</span><span class="sxs-lookup"><span data-stu-id="d06b9-123">-ClientId</span></span>
<span data-ttu-id="d06b9-124">Megadja az ügyfélalkalmazás fejlesztői konzoljának ügyfél-AZONOSÍTÓját.</span><span class="sxs-lookup"><span data-stu-id="d06b9-124">Specifies the client ID of the developer console that is the client application.</span></span>

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

### <span data-ttu-id="d06b9-125">-ClientRegistrationPageUrl</span><span class="sxs-lookup"><span data-stu-id="d06b9-125">-ClientRegistrationPageUrl</span></span>
<span data-ttu-id="d06b9-126">Az ügyfél regisztrációs végpontját adja meg az ügyfél regisztrálásához az engedélyezési kiszolgálóval, és ügyfél hitelesítő adatait kell beszereznie.</span><span class="sxs-lookup"><span data-stu-id="d06b9-126">Specifies the client registration endpoint to register clients with the authorization server and obtain client credentials.</span></span>

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

### <span data-ttu-id="d06b9-127">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="d06b9-127">-ClientSecret</span></span>
<span data-ttu-id="d06b9-128">Az ügyfélalkalmazás fejlesztői konzoljának ügyfél titkát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d06b9-128">Specifies the client secret of developer console that is the client application.</span></span>

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

### <span data-ttu-id="d06b9-129">-Környezet</span><span class="sxs-lookup"><span data-stu-id="d06b9-129">-Context</span></span>
<span data-ttu-id="d06b9-130">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="d06b9-130">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="d06b9-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d06b9-131">-DefaultProfile</span></span>
<span data-ttu-id="d06b9-132">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d06b9-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d06b9-133">-DefaultScope</span><span class="sxs-lookup"><span data-stu-id="d06b9-133">-DefaultScope</span></span>
<span data-ttu-id="d06b9-134">Az engedélyezési kiszolgáló alapértelmezett hatókörét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d06b9-134">Specifies the default scope for the authorization server.</span></span>

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

### <span data-ttu-id="d06b9-135">-Leírás</span><span class="sxs-lookup"><span data-stu-id="d06b9-135">-Description</span></span>
<span data-ttu-id="d06b9-136">Egy engedélyezési kiszolgáló leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="d06b9-136">Specifies a description for an authorization server.</span></span>

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

### <span data-ttu-id="d06b9-137">-GrantTypes</span><span class="sxs-lookup"><span data-stu-id="d06b9-137">-GrantTypes</span></span>
<span data-ttu-id="d06b9-138">Megadja a támogatási típusok tömbjét.</span><span class="sxs-lookup"><span data-stu-id="d06b9-138">Specifies an array of grant types.</span></span>
<span data-ttu-id="d06b9-139">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="d06b9-139">psdx_paramvalues</span></span>
- <span data-ttu-id="d06b9-140">AuthorizationCode</span><span class="sxs-lookup"><span data-stu-id="d06b9-140">AuthorizationCode</span></span>
- <span data-ttu-id="d06b9-141">ClientCredentials</span><span class="sxs-lookup"><span data-stu-id="d06b9-141">ClientCredentials</span></span> 
- <span data-ttu-id="d06b9-142">Implicit</span><span class="sxs-lookup"><span data-stu-id="d06b9-142">Implicit</span></span> 
- <span data-ttu-id="d06b9-143">ResourceOwnerPassword</span><span class="sxs-lookup"><span data-stu-id="d06b9-143">ResourceOwnerPassword</span></span>

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

### <span data-ttu-id="d06b9-144">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d06b9-144">-Name</span></span>
<span data-ttu-id="d06b9-145">A létrehozandó engedélyezési kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d06b9-145">Specifies the name of the authorization server to create.</span></span>

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

### <span data-ttu-id="d06b9-146">-ResourceOwnerPassword</span><span class="sxs-lookup"><span data-stu-id="d06b9-146">-ResourceOwnerPassword</span></span>
<span data-ttu-id="d06b9-147">Az erőforrás tulajdonosi jelszavát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d06b9-147">Specifies the resource owner password.</span></span>
<span data-ttu-id="d06b9-148">Meg kell adnia ezt a paramétert, ha a ResourceOwnerPassword a *GrantTypes* paraméter adja meg.</span><span class="sxs-lookup"><span data-stu-id="d06b9-148">You must specify this parameter is required if ResourceOwnerPassword is specified by the *GrantTypes* parameter.</span></span>

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

### <span data-ttu-id="d06b9-149">-ResourceOwnerUsername</span><span class="sxs-lookup"><span data-stu-id="d06b9-149">-ResourceOwnerUsername</span></span>
<span data-ttu-id="d06b9-150">Az erőforrás-tulajdonos felhasználónevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d06b9-150">Specifies the resource owner user name.</span></span>
<span data-ttu-id="d06b9-151">Ezt a paramétert akkor kell megadnia, ha a ResourceOwnerPassword a *GrantTypes* paraméter adja meg.</span><span class="sxs-lookup"><span data-stu-id="d06b9-151">You must specify this parameter if ResourceOwnerPassword is specified by the *GrantTypes* parameter.</span></span>

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

### <span data-ttu-id="d06b9-152">-ServerId</span><span class="sxs-lookup"><span data-stu-id="d06b9-152">-ServerId</span></span>
<span data-ttu-id="d06b9-153">A létrehozandó engedélyezési kiszolgáló AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d06b9-153">Specifies the ID of the authorization server to create.</span></span>

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

### <span data-ttu-id="d06b9-154">-SupportState</span><span class="sxs-lookup"><span data-stu-id="d06b9-154">-SupportState</span></span>
<span data-ttu-id="d06b9-155">Azt jelzi, hogy támogatja-e az *állami* paramétereket.</span><span class="sxs-lookup"><span data-stu-id="d06b9-155">Indicates whether to support the *State* parameter.</span></span>

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

### <span data-ttu-id="d06b9-156">-TokenBodyParameters</span><span class="sxs-lookup"><span data-stu-id="d06b9-156">-TokenBodyParameters</span></span>
<span data-ttu-id="d06b9-157">Az **Application/x-www-Form-urlencoded** formátumban adja meg a szövegtörzs további paramétereit.</span><span class="sxs-lookup"><span data-stu-id="d06b9-157">Specifies additional body parameters using **application/x-www-form-urlencoded** format.</span></span>

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

### <span data-ttu-id="d06b9-158">-TokenEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="d06b9-158">-TokenEndpointUrl</span></span>
<span data-ttu-id="d06b9-159">Annak a jogkivonat-végpontnak az URL-címét adja meg, amely az ügyfelek által az engedélyezési vagy a frissítési tokenek megjelenítéséhez szükséges Exchange-hozzáférési tokenek beszerzéséhez használható.</span><span class="sxs-lookup"><span data-stu-id="d06b9-159">Specifies the token endpoint URL that is used by clients to obtain access tokens in exchange for presenting authorization grants or refresh tokens.</span></span>

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

### <span data-ttu-id="d06b9-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d06b9-160">CommonParameters</span></span>
<span data-ttu-id="d06b9-161">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d06b9-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d06b9-162">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d06b9-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d06b9-163">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d06b9-163">INPUTS</span></span>

### <span data-ttu-id="d06b9-164">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="d06b9-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="d06b9-165">System. String</span><span class="sxs-lookup"><span data-stu-id="d06b9-165">System.String</span></span>

### <span data-ttu-id="d06b9-166">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementAuthorizationRequestMethod []</span><span class="sxs-lookup"><span data-stu-id="d06b9-166">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAuthorizationRequestMethod[]</span></span>

### <span data-ttu-id="d06b9-167">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementGrantType []</span><span class="sxs-lookup"><span data-stu-id="d06b9-167">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGrantType[]</span></span>

### <span data-ttu-id="d06b9-168">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementClientAuthenticationMethod []</span><span class="sxs-lookup"><span data-stu-id="d06b9-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementClientAuthenticationMethod[]</span></span>

### <span data-ttu-id="d06b9-169">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="d06b9-169">System.Collections.Hashtable</span></span>

### <span data-ttu-id="d06b9-170">System. null ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="d06b9-170">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="d06b9-171">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementAccessTokenSendingMethod []</span><span class="sxs-lookup"><span data-stu-id="d06b9-171">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessTokenSendingMethod[]</span></span>

## <span data-ttu-id="d06b9-172">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d06b9-172">OUTPUTS</span></span>

### <span data-ttu-id="d06b9-173">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementOAuth2AuthrozationServer</span><span class="sxs-lookup"><span data-stu-id="d06b9-173">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOAuth2AuthrozationServer</span></span>

## <span data-ttu-id="d06b9-174">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d06b9-174">NOTES</span></span>

## <span data-ttu-id="d06b9-175">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d06b9-175">RELATED LINKS</span></span>
