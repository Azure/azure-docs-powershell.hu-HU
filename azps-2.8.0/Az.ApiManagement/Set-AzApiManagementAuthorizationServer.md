---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 93005775-3AB9-43C5-B353-45B82124ADB7
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementAuthorizationServer.md
ms.openlocfilehash: 696db55822242e124f006be233a9c8a8605a360d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667946"
---
# <span data-ttu-id="aafe5-101">Set-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="aafe5-101">Set-AzApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="aafe5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="aafe5-102">SYNOPSIS</span></span>
<span data-ttu-id="aafe5-103">Módosítja az engedélyezési kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="aafe5-103">Modifies an authorization server.</span></span>

## <span data-ttu-id="aafe5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="aafe5-104">SYNTAX</span></span>

```
Set-AzApiManagementAuthorizationServer -Context <PsApiManagementContext> -ServerId <String> -Name <String>
 [-Description <String>] -ClientRegistrationPageUrl <String> -AuthorizationEndpointUrl <String>
 -TokenEndpointUrl <String> -ClientId <String> [-ClientSecret <String>]
 [-AuthorizationRequestMethods <PsApiManagementAuthorizationRequestMethod[]>]
 -GrantTypes <PsApiManagementGrantType[]>
 -ClientAuthenticationMethods <PsApiManagementClientAuthenticationMethod[]> [-TokenBodyParameters <Hashtable>]
 [-SupportState <Boolean>] [-DefaultScope <String>]
 -AccessTokenSendingMethods <PsApiManagementAccessTokenSendingMethod[]> [-ResourceOwnerUsername <String>]
 [-ResourceOwnerPassword <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aafe5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="aafe5-105">DESCRIPTION</span></span>
<span data-ttu-id="aafe5-106">A **set-AzApiManagementAuthorizationServer** parancsmag az Azure API-kezelés engedélyezési kiszolgálójának adatait módosítja.</span><span class="sxs-lookup"><span data-stu-id="aafe5-106">The **Set-AzApiManagementAuthorizationServer** cmdlet modifies Azure API Management authorization server details.</span></span>

## <span data-ttu-id="aafe5-107">Példák</span><span class="sxs-lookup"><span data-stu-id="aafe5-107">EXAMPLES</span></span>

### <span data-ttu-id="aafe5-108">Példa 1: engedélyezési kiszolgáló módosítása</span><span class="sxs-lookup"><span data-stu-id="aafe5-108">Example 1: Modify an authorization server</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementAuthorizationServer -Context $ApiMgmtContext -ServerId 0123456789 -Name "Contoso OAuth2 server" -ClientRegistrationPageUrl "https://contoso/signupv2" -AuthorizationEndpointUrl "https://contoso/authv2" -TokenEndpointUrl "https://contoso/tokenv2" -ClientId "clientid" -ClientSecret "e041ed1b660b4eadbad5a29d066e6e88" -AuthorizationRequestMethods @('Get') -GrantTypes @( 'AuthorizationCode', 'Implicit', 'ClientCredentials') -ClientAuthenticationMethods @('Basic') -TokenBodyParameters @{'par1'='val1'} -AccessTokenSendingMethods @('AuthorizationHeader')
```

<span data-ttu-id="aafe5-109">Ez a parancs módosítja a megadott API-kezelési engedélyezési kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="aafe5-109">This command modifies the specified API Management authorization server.</span></span>

## <span data-ttu-id="aafe5-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="aafe5-110">PARAMETERS</span></span>

### <span data-ttu-id="aafe5-111">-AccessTokenSendingMethods</span><span class="sxs-lookup"><span data-stu-id="aafe5-111">-AccessTokenSendingMethods</span></span>
<span data-ttu-id="aafe5-112">Az Access-tokenek küldésére szolgáló metódusok tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="aafe5-112">Specifies an array of methods to send an access token.</span></span>
<span data-ttu-id="aafe5-113">psdx_paramvalues AuthorizationHeader és lekérdezés.</span><span class="sxs-lookup"><span data-stu-id="aafe5-113">psdx_paramvalues AuthorizationHeader and Query.</span></span>

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

### <span data-ttu-id="aafe5-114">-AuthorizationEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="aafe5-114">-AuthorizationEndpointUrl</span></span>
<span data-ttu-id="aafe5-115">Megadja az engedélyezési végpontot az erőforrás-tulajdonosok hitelesítéséhez és az engedélyezési támogatás beszerzéséhez.</span><span class="sxs-lookup"><span data-stu-id="aafe5-115">Specifies the authorization endpoint to authenticate resource owners and obtain authorization grants.</span></span>

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

### <span data-ttu-id="aafe5-116">-AuthorizationRequestMethods</span><span class="sxs-lookup"><span data-stu-id="aafe5-116">-AuthorizationRequestMethods</span></span>
<span data-ttu-id="aafe5-117">Megadja az engedélyezési kérés módszereinek tömbjét.</span><span class="sxs-lookup"><span data-stu-id="aafe5-117">Specifies an array of authorization request methods.</span></span>
<span data-ttu-id="aafe5-118">psdx_paramvalues beolvasás és közzététel.</span><span class="sxs-lookup"><span data-stu-id="aafe5-118">psdx_paramvalues GET and POST.</span></span>
<span data-ttu-id="aafe5-119">Az alapértelmezett érték a beolvasás.</span><span class="sxs-lookup"><span data-stu-id="aafe5-119">The default value is GET.</span></span>

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

### <span data-ttu-id="aafe5-120">-ClientAuthenticationMethods</span><span class="sxs-lookup"><span data-stu-id="aafe5-120">-ClientAuthenticationMethods</span></span>
<span data-ttu-id="aafe5-121">Az ügyfél-hitelesítési módszerek tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="aafe5-121">Specifies an array of client authentication methods.</span></span>
<span data-ttu-id="aafe5-122">psdx_paramvalues egyszerű és a szövegtörzs.</span><span class="sxs-lookup"><span data-stu-id="aafe5-122">psdx_paramvalues Basic and Body.</span></span>

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

### <span data-ttu-id="aafe5-123">-ClientId</span><span class="sxs-lookup"><span data-stu-id="aafe5-123">-ClientId</span></span>
<span data-ttu-id="aafe5-124">Megadja az ügyfélalkalmazás fejlesztői konzoljának ügyfél-AZONOSÍTÓját.</span><span class="sxs-lookup"><span data-stu-id="aafe5-124">Specifies the client ID of the developer console that is the client application.</span></span>

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

### <span data-ttu-id="aafe5-125">-ClientRegistrationPageUrl</span><span class="sxs-lookup"><span data-stu-id="aafe5-125">-ClientRegistrationPageUrl</span></span>
<span data-ttu-id="aafe5-126">Az ügyfél regisztrációs végpontját adja meg az ügyfél regisztrálásához az engedélyezési kiszolgálóval, és ügyfél hitelesítő adatait kell beszereznie.</span><span class="sxs-lookup"><span data-stu-id="aafe5-126">Specifies the client registration endpoint to register clients with the authorization server and obtain client credentials.</span></span>

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

### <span data-ttu-id="aafe5-127">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="aafe5-127">-ClientSecret</span></span>
<span data-ttu-id="aafe5-128">Az ügyfélalkalmazás fejlesztői konzoljának az ügyfél titkát adja meg.</span><span class="sxs-lookup"><span data-stu-id="aafe5-128">Specifies the client secret of the developer console that is the client application.</span></span>

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

### <span data-ttu-id="aafe5-129">-Környezet</span><span class="sxs-lookup"><span data-stu-id="aafe5-129">-Context</span></span>
<span data-ttu-id="aafe5-130">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="aafe5-130">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="aafe5-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aafe5-131">-DefaultProfile</span></span>
<span data-ttu-id="aafe5-132">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="aafe5-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aafe5-133">-DefaultScope</span><span class="sxs-lookup"><span data-stu-id="aafe5-133">-DefaultScope</span></span>
<span data-ttu-id="aafe5-134">Az engedélyezési kiszolgáló alapértelmezett hatókörét adja meg.</span><span class="sxs-lookup"><span data-stu-id="aafe5-134">Specifies the default scope for the authorization server.</span></span>

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

### <span data-ttu-id="aafe5-135">-Leírás</span><span class="sxs-lookup"><span data-stu-id="aafe5-135">-Description</span></span>
<span data-ttu-id="aafe5-136">Egy engedélyezési kiszolgáló leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="aafe5-136">Specifies a description for an authorization server.</span></span>

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

### <span data-ttu-id="aafe5-137">-GrantTypes</span><span class="sxs-lookup"><span data-stu-id="aafe5-137">-GrantTypes</span></span>
<span data-ttu-id="aafe5-138">Megadja a támogatási típusok tömbjét.</span><span class="sxs-lookup"><span data-stu-id="aafe5-138">Specifies an array of grant types.</span></span>
<span data-ttu-id="aafe5-139">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="aafe5-139">psdx_paramvalues</span></span>
- <span data-ttu-id="aafe5-140">AuthorizationCode</span><span class="sxs-lookup"><span data-stu-id="aafe5-140">AuthorizationCode</span></span>
- <span data-ttu-id="aafe5-141">ClientCredentials</span><span class="sxs-lookup"><span data-stu-id="aafe5-141">ClientCredentials</span></span> 
- <span data-ttu-id="aafe5-142">Implicit</span><span class="sxs-lookup"><span data-stu-id="aafe5-142">Implicit</span></span> 
- <span data-ttu-id="aafe5-143">ResourceOwnerPassword</span><span class="sxs-lookup"><span data-stu-id="aafe5-143">ResourceOwnerPassword</span></span>

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

### <span data-ttu-id="aafe5-144">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="aafe5-144">-Name</span></span>
<span data-ttu-id="aafe5-145">A módosítani kívánt engedélyezési kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="aafe5-145">Specifies the name of the authorization server to modify.</span></span>

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

### <span data-ttu-id="aafe5-146">-PassThru</span><span class="sxs-lookup"><span data-stu-id="aafe5-146">-PassThru</span></span>
<span data-ttu-id="aafe5-147">passthru</span><span class="sxs-lookup"><span data-stu-id="aafe5-147">passthru</span></span>

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

### <span data-ttu-id="aafe5-148">-ResourceOwnerPassword</span><span class="sxs-lookup"><span data-stu-id="aafe5-148">-ResourceOwnerPassword</span></span>
<span data-ttu-id="aafe5-149">Az erőforrás tulajdonosi jelszavát adja meg.</span><span class="sxs-lookup"><span data-stu-id="aafe5-149">Specifies the resource owner password.</span></span>
<span data-ttu-id="aafe5-150">Ezt a paramétert akkor kell megadnia, ha a ResourceOwnerPassword a *GrantTypes* paraméter adja meg.</span><span class="sxs-lookup"><span data-stu-id="aafe5-150">You must specify this parameter if ResourceOwnerPassword is specified by the *GrantTypes* parameter.</span></span>

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

### <span data-ttu-id="aafe5-151">-ResourceOwnerUsername</span><span class="sxs-lookup"><span data-stu-id="aafe5-151">-ResourceOwnerUsername</span></span>
<span data-ttu-id="aafe5-152">Az erőforrás-tulajdonos felhasználónevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="aafe5-152">Specifies the resource owner user name.</span></span>
<span data-ttu-id="aafe5-153">Ezt a paramétert akkor kell megadnia, ha a ResourceOwnerPassword a *GrantTypes* paraméter adja meg.</span><span class="sxs-lookup"><span data-stu-id="aafe5-153">You must specify this parameter if ResourceOwnerPassword is specified by the *GrantTypes* parameter.</span></span>

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

### <span data-ttu-id="aafe5-154">-ServerId</span><span class="sxs-lookup"><span data-stu-id="aafe5-154">-ServerId</span></span>
<span data-ttu-id="aafe5-155">A módosítani kívánt engedélyezési kiszolgáló AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="aafe5-155">Specifies the ID of the authorization server to modify.</span></span>

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

### <span data-ttu-id="aafe5-156">-SupportState</span><span class="sxs-lookup"><span data-stu-id="aafe5-156">-SupportState</span></span>
<span data-ttu-id="aafe5-157">Azt jelzi, hogy támogatja-e az *állami* paramétereket.</span><span class="sxs-lookup"><span data-stu-id="aafe5-157">Indicates whether to support the *State* parameter.</span></span>

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

### <span data-ttu-id="aafe5-158">-TokenBodyParameters</span><span class="sxs-lookup"><span data-stu-id="aafe5-158">-TokenBodyParameters</span></span>
<span data-ttu-id="aafe5-159">Az Application/x-www-Form-urlencoded formátumban adja meg a szövegtörzs további paramétereit.</span><span class="sxs-lookup"><span data-stu-id="aafe5-159">Specifies additional body parameters using application/x-www-form-urlencoded format.</span></span>

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

### <span data-ttu-id="aafe5-160">-TokenEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="aafe5-160">-TokenEndpointUrl</span></span>
<span data-ttu-id="aafe5-161">Annak a jogkivonat-végpontnak a meghatározása, amellyel az ügyfelek megkapják az Access-tokenek engedélyezési vagy frissítési tokenek megjelenítését az Exchange-ben.</span><span class="sxs-lookup"><span data-stu-id="aafe5-161">Specifies the token endpoint for clients to obtain access tokens in exchange for presenting authorization grants or refresh tokens.</span></span>

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

### <span data-ttu-id="aafe5-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aafe5-162">CommonParameters</span></span>
<span data-ttu-id="aafe5-163">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="aafe5-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aafe5-164">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="aafe5-164">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aafe5-165">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="aafe5-165">INPUTS</span></span>

### <span data-ttu-id="aafe5-166">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="aafe5-166">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="aafe5-167">System. String</span><span class="sxs-lookup"><span data-stu-id="aafe5-167">System.String</span></span>

### <span data-ttu-id="aafe5-168">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementAuthorizationRequestMethod []</span><span class="sxs-lookup"><span data-stu-id="aafe5-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAuthorizationRequestMethod[]</span></span>

### <span data-ttu-id="aafe5-169">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementGrantType []</span><span class="sxs-lookup"><span data-stu-id="aafe5-169">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGrantType[]</span></span>

### <span data-ttu-id="aafe5-170">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementClientAuthenticationMethod []</span><span class="sxs-lookup"><span data-stu-id="aafe5-170">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementClientAuthenticationMethod[]</span></span>

### <span data-ttu-id="aafe5-171">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="aafe5-171">System.Collections.Hashtable</span></span>

### <span data-ttu-id="aafe5-172">System. null ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="aafe5-172">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="aafe5-173">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementAccessTokenSendingMethod []</span><span class="sxs-lookup"><span data-stu-id="aafe5-173">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessTokenSendingMethod[]</span></span>

### <span data-ttu-id="aafe5-174">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="aafe5-174">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="aafe5-175">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="aafe5-175">OUTPUTS</span></span>

### <span data-ttu-id="aafe5-176">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementOAuth2AuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="aafe5-176">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOAuth2AuthorizationServer</span></span>

## <span data-ttu-id="aafe5-177">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="aafe5-177">NOTES</span></span>

## <span data-ttu-id="aafe5-178">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="aafe5-178">RELATED LINKS</span></span>

[<span data-ttu-id="aafe5-179">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="aafe5-179">Get-AzApiManagementAuthorizationServer</span></span>](./Get-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="aafe5-180">Új – AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="aafe5-180">New-AzApiManagementAuthorizationServer</span></span>](./New-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="aafe5-181">Remove-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="aafe5-181">Remove-AzApiManagementAuthorizationServer</span></span>](./Remove-AzApiManagementAuthorizationServer.md)


