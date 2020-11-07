---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 93005775-3AB9-43C5-B353-45B82124ADB7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementAuthorizationServer.md
ms.openlocfilehash: ed7043746aa5ce59e733737acf8da61bdb44b0a1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679991"
---
# <span data-ttu-id="5f39b-101">Set-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="5f39b-101">Set-AzureRmApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="5f39b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5f39b-102">SYNOPSIS</span></span>
<span data-ttu-id="5f39b-103">Módosítja az engedélyezési kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="5f39b-103">Modifies an authorization server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5f39b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5f39b-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementAuthorizationServer -Context <PsApiManagementContext> -ServerId <String> -Name <String>
 [-Description <String>] -ClientRegistrationPageUrl <String> -AuthorizationEndpointUrl <String>
 -TokenEndpointUrl <String> -ClientId <String> [-ClientSecret <String>]
 [-AuthorizationRequestMethods <PsApiManagementAuthorizationRequestMethod[]>]
 -GrantTypes <PsApiManagementGrantType[]>
 -ClientAuthenticationMethods <PsApiManagementClientAuthenticationMethod[]> [-TokenBodyParameters <Hashtable>]
 [-SupportState <Boolean>] [-DefaultScope <String>]
 -AccessTokenSendingMethods <PsApiManagementAccessTokenSendingMethod[]> [-ResourceOwnerUsername <String>]
 [-ResourceOwnerPassword <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5f39b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="5f39b-105">DESCRIPTION</span></span>
<span data-ttu-id="5f39b-106">A **set-AzureRmApiManagementAuthorizationServer** parancsmag az Azure API-kezelés engedélyezési kiszolgálójának adatait módosítja.</span><span class="sxs-lookup"><span data-stu-id="5f39b-106">The **Set-AzureRmApiManagementAuthorizationServer** cmdlet modifies Azure API Management authorization server details.</span></span>

## <span data-ttu-id="5f39b-107">Példák</span><span class="sxs-lookup"><span data-stu-id="5f39b-107">EXAMPLES</span></span>

### <span data-ttu-id="5f39b-108">Példa 1: engedélyezési kiszolgáló módosítása</span><span class="sxs-lookup"><span data-stu-id="5f39b-108">Example 1: Modify an authorization server</span></span>
```
PS C:\>Set-AzureRmApiManagementAuthrizarionServer -Context $ApiMgmtContext -ServerId 0123456789 -Name "Contoso OAuth2 server" -ClientRegistrationPageUrl "https://contoso/signupv2" -AuthorizationEndpointUrl "https://contoso/authv2" -TokenEndpointUrl "https://contoso/tokenv2" -ClientId "clientid" -ClientSecret "e041ed1b660b4eadbad5a29d066e6e88" -AuthorizationRequestMethods @('Get') -GrantTypes @( 'AuthorizationCode', 'Implicit', 'ClientCredentials') -ClientAuthenticationMethods @('Basic') -TokenBodyParameters @{'par1'='val1'} -AccessTokenSendingMethods @('AuthorizationHeader')
```

<span data-ttu-id="5f39b-109">Ez a parancs módosítja a megadott API-kezelési engedélyezési kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="5f39b-109">This command modifies the specified API Management authorization server.</span></span>

## <span data-ttu-id="5f39b-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5f39b-110">PARAMETERS</span></span>

### <span data-ttu-id="5f39b-111">-AccessTokenSendingMethods</span><span class="sxs-lookup"><span data-stu-id="5f39b-111">-AccessTokenSendingMethods</span></span>
<span data-ttu-id="5f39b-112">Az Access-tokenek küldésére szolgáló metódusok tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5f39b-112">Specifies an array of methods to send an access token.</span></span>
<span data-ttu-id="5f39b-113">psdx_paramvalues AuthorizationHeader és lekérdezés.</span><span class="sxs-lookup"><span data-stu-id="5f39b-113">psdx_paramvalues AuthorizationHeader and Query.</span></span>

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

### <span data-ttu-id="5f39b-114">-AuthorizationEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="5f39b-114">-AuthorizationEndpointUrl</span></span>
<span data-ttu-id="5f39b-115">Megadja az engedélyezési végpontot az erőforrás-tulajdonosok hitelesítéséhez és az engedélyezési támogatás beszerzéséhez.</span><span class="sxs-lookup"><span data-stu-id="5f39b-115">Specifies the authorization endpoint to authenticate resource owners and obtain authorization grants.</span></span>

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

### <span data-ttu-id="5f39b-116">-AuthorizationRequestMethods</span><span class="sxs-lookup"><span data-stu-id="5f39b-116">-AuthorizationRequestMethods</span></span>
<span data-ttu-id="5f39b-117">Megadja az engedélyezési kérés módszereinek tömbjét.</span><span class="sxs-lookup"><span data-stu-id="5f39b-117">Specifies an array of authorization request methods.</span></span>
<span data-ttu-id="5f39b-118">psdx_paramvalues beolvasás és közzététel.</span><span class="sxs-lookup"><span data-stu-id="5f39b-118">psdx_paramvalues GET and POST.</span></span>
<span data-ttu-id="5f39b-119">Az alapértelmezett érték a beolvasás.</span><span class="sxs-lookup"><span data-stu-id="5f39b-119">The default value is GET.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAuthorizationRequestMethod[]
Parameter Sets: (All)
Aliases: 
Accepted values: Get, Post

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f39b-120">-ClientAuthenticationMethods</span><span class="sxs-lookup"><span data-stu-id="5f39b-120">-ClientAuthenticationMethods</span></span>
<span data-ttu-id="5f39b-121">Az ügyfél-hitelesítési módszerek tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5f39b-121">Specifies an array of client authentication methods.</span></span>
<span data-ttu-id="5f39b-122">psdx_paramvalues egyszerű és a szövegtörzs.</span><span class="sxs-lookup"><span data-stu-id="5f39b-122">psdx_paramvalues Basic and Body.</span></span>

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

### <span data-ttu-id="5f39b-123">-ClientId</span><span class="sxs-lookup"><span data-stu-id="5f39b-123">-ClientId</span></span>
<span data-ttu-id="5f39b-124">Megadja az ügyfélalkalmazás fejlesztői konzoljának ügyfél-AZONOSÍTÓját.</span><span class="sxs-lookup"><span data-stu-id="5f39b-124">Specifies the client ID of the developer console that is the client application.</span></span>

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

### <span data-ttu-id="5f39b-125">-ClientRegistrationPageUrl</span><span class="sxs-lookup"><span data-stu-id="5f39b-125">-ClientRegistrationPageUrl</span></span>
<span data-ttu-id="5f39b-126">Az ügyfél regisztrációs végpontját adja meg az ügyfél regisztrálásához az engedélyezési kiszolgálóval, és ügyfél hitelesítő adatait kell beszereznie.</span><span class="sxs-lookup"><span data-stu-id="5f39b-126">Specifies the client registration endpoint to register clients with the authorization server and obtain client credentials.</span></span>

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

### <span data-ttu-id="5f39b-127">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="5f39b-127">-ClientSecret</span></span>
<span data-ttu-id="5f39b-128">Az ügyfélalkalmazás fejlesztői konzoljának az ügyfél titkát adja meg.</span><span class="sxs-lookup"><span data-stu-id="5f39b-128">Specifies the client secret of the developer console that is the client application.</span></span>

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

### <span data-ttu-id="5f39b-129">-Környezet</span><span class="sxs-lookup"><span data-stu-id="5f39b-129">-Context</span></span>
<span data-ttu-id="5f39b-130">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="5f39b-130">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="5f39b-131">-DefaultScope</span><span class="sxs-lookup"><span data-stu-id="5f39b-131">-DefaultScope</span></span>
<span data-ttu-id="5f39b-132">Az engedélyezési kiszolgáló alapértelmezett hatókörét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5f39b-132">Specifies the default scope for the authorization server.</span></span>

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

### <span data-ttu-id="5f39b-133">-Leírás</span><span class="sxs-lookup"><span data-stu-id="5f39b-133">-Description</span></span>
<span data-ttu-id="5f39b-134">Egy engedélyezési kiszolgáló leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="5f39b-134">Specifies a description for an authorization server.</span></span>

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

### <span data-ttu-id="5f39b-135">-GrantTypes</span><span class="sxs-lookup"><span data-stu-id="5f39b-135">-GrantTypes</span></span>
<span data-ttu-id="5f39b-136">Megadja a támogatási típusok tömbjét.</span><span class="sxs-lookup"><span data-stu-id="5f39b-136">Specifies an array of grant types.</span></span>
<span data-ttu-id="5f39b-137">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="5f39b-137">psdx_paramvalues</span></span>

- <span data-ttu-id="5f39b-138">AuthorizationCode</span><span class="sxs-lookup"><span data-stu-id="5f39b-138">AuthorizationCode</span></span>
- <span data-ttu-id="5f39b-139">ClientCredentials</span><span class="sxs-lookup"><span data-stu-id="5f39b-139">ClientCredentials</span></span> 
- <span data-ttu-id="5f39b-140">Implicit</span><span class="sxs-lookup"><span data-stu-id="5f39b-140">Implicit</span></span> 
- <span data-ttu-id="5f39b-141">ResourceOwnerPassword</span><span class="sxs-lookup"><span data-stu-id="5f39b-141">ResourceOwnerPassword</span></span>

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

### <span data-ttu-id="5f39b-142">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5f39b-142">-Name</span></span>
<span data-ttu-id="5f39b-143">A módosítani kívánt engedélyezési kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5f39b-143">Specifies the name of the authorization server to modify.</span></span>

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

### <span data-ttu-id="5f39b-144">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5f39b-144">-PassThru</span></span>
<span data-ttu-id="5f39b-145">passthru</span><span class="sxs-lookup"><span data-stu-id="5f39b-145">passthru</span></span>

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

### <span data-ttu-id="5f39b-146">-ResourceOwnerPassword</span><span class="sxs-lookup"><span data-stu-id="5f39b-146">-ResourceOwnerPassword</span></span>
<span data-ttu-id="5f39b-147">Az erőforrás tulajdonosi jelszavát adja meg.</span><span class="sxs-lookup"><span data-stu-id="5f39b-147">Specifies the resource owner password.</span></span>
<span data-ttu-id="5f39b-148">Ezt a paramétert akkor kell megadnia, ha a ResourceOwnerPassword a *GrantTypes* paraméter adja meg.</span><span class="sxs-lookup"><span data-stu-id="5f39b-148">You must specify this parameter if ResourceOwnerPassword is specified by the *GrantTypes* parameter.</span></span>

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

### <span data-ttu-id="5f39b-149">-ResourceOwnerUsername</span><span class="sxs-lookup"><span data-stu-id="5f39b-149">-ResourceOwnerUsername</span></span>
<span data-ttu-id="5f39b-150">Az erőforrás-tulajdonos felhasználónevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5f39b-150">Specifies the resource owner user name.</span></span>
<span data-ttu-id="5f39b-151">Ezt a paramétert akkor kell megadnia, ha a ResourceOwnerPassword a *GrantTypes* paraméter adja meg.</span><span class="sxs-lookup"><span data-stu-id="5f39b-151">You must specify this parameter if ResourceOwnerPassword is specified by the *GrantTypes* parameter.</span></span>

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

### <span data-ttu-id="5f39b-152">-ServerId</span><span class="sxs-lookup"><span data-stu-id="5f39b-152">-ServerId</span></span>
<span data-ttu-id="5f39b-153">A módosítani kívánt engedélyezési kiszolgáló AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="5f39b-153">Specifies the ID of the authorization server to modify.</span></span>

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

### <span data-ttu-id="5f39b-154">-SupportState</span><span class="sxs-lookup"><span data-stu-id="5f39b-154">-SupportState</span></span>
<span data-ttu-id="5f39b-155">Azt jelzi, hogy támogatja-e az *állami* paramétereket.</span><span class="sxs-lookup"><span data-stu-id="5f39b-155">Indicates whether to support the *State* parameter.</span></span>

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

### <span data-ttu-id="5f39b-156">-TokenBodyParameters</span><span class="sxs-lookup"><span data-stu-id="5f39b-156">-TokenBodyParameters</span></span>
<span data-ttu-id="5f39b-157">Az Application/x-www-Form-urlencoded formátumban adja meg a szövegtörzs további paramétereit.</span><span class="sxs-lookup"><span data-stu-id="5f39b-157">Specifies additional body parameters using application/x-www-form-urlencoded format.</span></span>

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

### <span data-ttu-id="5f39b-158">-TokenEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="5f39b-158">-TokenEndpointUrl</span></span>
<span data-ttu-id="5f39b-159">Annak a jogkivonat-végpontnak a meghatározása, amellyel az ügyfelek megkapják az Access-tokenek engedélyezési vagy frissítési tokenek megjelenítését az Exchange-ben.</span><span class="sxs-lookup"><span data-stu-id="5f39b-159">Specifies the token endpoint for clients to obtain access tokens in exchange for presenting authorization grants or refresh tokens.</span></span>

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

### <span data-ttu-id="5f39b-160">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f39b-160">-DefaultProfile</span></span>
<span data-ttu-id="5f39b-161">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5f39b-161">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5f39b-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f39b-162">CommonParameters</span></span>
<span data-ttu-id="5f39b-163">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5f39b-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f39b-164">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f39b-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f39b-165">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5f39b-165">INPUTS</span></span>

## <span data-ttu-id="5f39b-166">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5f39b-166">OUTPUTS</span></span>

### <span data-ttu-id="5f39b-167">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementOAuth2AuthrozationServer</span><span class="sxs-lookup"><span data-stu-id="5f39b-167">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOAuth2AuthrozationServer</span></span>

## <span data-ttu-id="5f39b-168">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5f39b-168">NOTES</span></span>

## <span data-ttu-id="5f39b-169">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5f39b-169">RELATED LINKS</span></span>

[<span data-ttu-id="5f39b-170">Get-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="5f39b-170">Get-AzureRmApiManagementAuthorizationServer</span></span>](./Get-AzureRmApiManagementAuthorizationServer.md)

[<span data-ttu-id="5f39b-171">Új – AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="5f39b-171">New-AzureRmApiManagementAuthorizationServer</span></span>](./New-AzureRmApiManagementAuthorizationServer.md)

[<span data-ttu-id="5f39b-172">Remove-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="5f39b-172">Remove-AzureRmApiManagementAuthorizationServer</span></span>](./Remove-AzureRmApiManagementAuthorizationServer.md)


