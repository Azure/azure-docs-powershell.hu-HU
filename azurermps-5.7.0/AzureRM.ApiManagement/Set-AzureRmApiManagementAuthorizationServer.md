---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 93005775-3AB9-43C5-B353-45B82124ADB7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementAuthorizationServer.md
ms.openlocfilehash: 6424ad453d7e2ee3c4933127cc58e6d3e1193e76
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503124"
---
# <span data-ttu-id="40c66-101">Set-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="40c66-101">Set-AzureRmApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="40c66-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="40c66-102">SYNOPSIS</span></span>
<span data-ttu-id="40c66-103">Módosítja az engedélyezési kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="40c66-103">Modifies an authorization server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="40c66-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="40c66-104">SYNTAX</span></span>

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

## <span data-ttu-id="40c66-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="40c66-105">DESCRIPTION</span></span>
<span data-ttu-id="40c66-106">A **set-AzureRmApiManagementAuthorizationServer** parancsmag az Azure API-kezelés engedélyezési kiszolgálójának adatait módosítja.</span><span class="sxs-lookup"><span data-stu-id="40c66-106">The **Set-AzureRmApiManagementAuthorizationServer** cmdlet modifies Azure API Management authorization server details.</span></span>

## <span data-ttu-id="40c66-107">Példák</span><span class="sxs-lookup"><span data-stu-id="40c66-107">EXAMPLES</span></span>

### <span data-ttu-id="40c66-108">Példa 1: engedélyezési kiszolgáló módosítása</span><span class="sxs-lookup"><span data-stu-id="40c66-108">Example 1: Modify an authorization server</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementAuthrizarionServer -Context $ApiMgmtContext -ServerId 0123456789 -Name "Contoso OAuth2 server" -ClientRegistrationPageUrl "https://contoso/signupv2" -AuthorizationEndpointUrl "https://contoso/authv2" -TokenEndpointUrl "https://contoso/tokenv2" -ClientId "clientid" -ClientSecret "e041ed1b660b4eadbad5a29d066e6e88" -AuthorizationRequestMethods @('Get') -GrantTypes @( 'AuthorizationCode', 'Implicit', 'ClientCredentials') -ClientAuthenticationMethods @('Basic') -TokenBodyParameters @{'par1'='val1'} -AccessTokenSendingMethods @('AuthorizationHeader')
```

<span data-ttu-id="40c66-109">Ez a parancs módosítja a megadott API-kezelési engedélyezési kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="40c66-109">This command modifies the specified API Management authorization server.</span></span>

## <span data-ttu-id="40c66-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="40c66-110">PARAMETERS</span></span>

### <span data-ttu-id="40c66-111">-AccessTokenSendingMethods</span><span class="sxs-lookup"><span data-stu-id="40c66-111">-AccessTokenSendingMethods</span></span>
<span data-ttu-id="40c66-112">Az Access-tokenek küldésére szolgáló metódusok tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="40c66-112">Specifies an array of methods to send an access token.</span></span>
<span data-ttu-id="40c66-113">psdx_paramvalues AuthorizationHeader és lekérdezés.</span><span class="sxs-lookup"><span data-stu-id="40c66-113">psdx_paramvalues AuthorizationHeader and Query.</span></span>

```yaml
Type: PsApiManagementAccessTokenSendingMethod[]
Parameter Sets: (All)
Aliases: 
Accepted values: AuthorizationHeader, Query

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40c66-114">-AuthorizationEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="40c66-114">-AuthorizationEndpointUrl</span></span>
<span data-ttu-id="40c66-115">Megadja az engedélyezési végpontot az erőforrás-tulajdonosok hitelesítéséhez és az engedélyezési támogatás beszerzéséhez.</span><span class="sxs-lookup"><span data-stu-id="40c66-115">Specifies the authorization endpoint to authenticate resource owners and obtain authorization grants.</span></span>

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

### <span data-ttu-id="40c66-116">-AuthorizationRequestMethods</span><span class="sxs-lookup"><span data-stu-id="40c66-116">-AuthorizationRequestMethods</span></span>
<span data-ttu-id="40c66-117">Megadja az engedélyezési kérés módszereinek tömbjét.</span><span class="sxs-lookup"><span data-stu-id="40c66-117">Specifies an array of authorization request methods.</span></span>
<span data-ttu-id="40c66-118">psdx_paramvalues beolvasás és közzététel.</span><span class="sxs-lookup"><span data-stu-id="40c66-118">psdx_paramvalues GET and POST.</span></span>
<span data-ttu-id="40c66-119">Az alapértelmezett érték a beolvasás.</span><span class="sxs-lookup"><span data-stu-id="40c66-119">The default value is GET.</span></span>

```yaml
Type: PsApiManagementAuthorizationRequestMethod[]
Parameter Sets: (All)
Aliases: 
Accepted values: Get, Post

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40c66-120">-ClientAuthenticationMethods</span><span class="sxs-lookup"><span data-stu-id="40c66-120">-ClientAuthenticationMethods</span></span>
<span data-ttu-id="40c66-121">Az ügyfél-hitelesítési módszerek tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="40c66-121">Specifies an array of client authentication methods.</span></span>
<span data-ttu-id="40c66-122">psdx_paramvalues egyszerű és a szövegtörzs.</span><span class="sxs-lookup"><span data-stu-id="40c66-122">psdx_paramvalues Basic and Body.</span></span>

```yaml
Type: PsApiManagementClientAuthenticationMethod[]
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Body

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40c66-123">-ClientId</span><span class="sxs-lookup"><span data-stu-id="40c66-123">-ClientId</span></span>
<span data-ttu-id="40c66-124">Megadja az ügyfélalkalmazás fejlesztői konzoljának ügyfél-AZONOSÍTÓját.</span><span class="sxs-lookup"><span data-stu-id="40c66-124">Specifies the client ID of the developer console that is the client application.</span></span>

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

### <span data-ttu-id="40c66-125">-ClientRegistrationPageUrl</span><span class="sxs-lookup"><span data-stu-id="40c66-125">-ClientRegistrationPageUrl</span></span>
<span data-ttu-id="40c66-126">Az ügyfél regisztrációs végpontját adja meg az ügyfél regisztrálásához az engedélyezési kiszolgálóval, és ügyfél hitelesítő adatait kell beszereznie.</span><span class="sxs-lookup"><span data-stu-id="40c66-126">Specifies the client registration endpoint to register clients with the authorization server and obtain client credentials.</span></span>

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

### <span data-ttu-id="40c66-127">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="40c66-127">-ClientSecret</span></span>
<span data-ttu-id="40c66-128">Az ügyfélalkalmazás fejlesztői konzoljának az ügyfél titkát adja meg.</span><span class="sxs-lookup"><span data-stu-id="40c66-128">Specifies the client secret of the developer console that is the client application.</span></span>

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

### <span data-ttu-id="40c66-129">-Környezet</span><span class="sxs-lookup"><span data-stu-id="40c66-129">-Context</span></span>
<span data-ttu-id="40c66-130">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="40c66-130">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="40c66-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40c66-131">-DefaultProfile</span></span>
<span data-ttu-id="40c66-132">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="40c66-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="40c66-133">-DefaultScope</span><span class="sxs-lookup"><span data-stu-id="40c66-133">-DefaultScope</span></span>
<span data-ttu-id="40c66-134">Az engedélyezési kiszolgáló alapértelmezett hatókörét adja meg.</span><span class="sxs-lookup"><span data-stu-id="40c66-134">Specifies the default scope for the authorization server.</span></span>

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

### <span data-ttu-id="40c66-135">-Leírás</span><span class="sxs-lookup"><span data-stu-id="40c66-135">-Description</span></span>
<span data-ttu-id="40c66-136">Egy engedélyezési kiszolgáló leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="40c66-136">Specifies a description for an authorization server.</span></span>

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

### <span data-ttu-id="40c66-137">-GrantTypes</span><span class="sxs-lookup"><span data-stu-id="40c66-137">-GrantTypes</span></span>
<span data-ttu-id="40c66-138">Megadja a támogatási típusok tömbjét.</span><span class="sxs-lookup"><span data-stu-id="40c66-138">Specifies an array of grant types.</span></span>
<span data-ttu-id="40c66-139">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="40c66-139">psdx_paramvalues</span></span>

- <span data-ttu-id="40c66-140">AuthorizationCode</span><span class="sxs-lookup"><span data-stu-id="40c66-140">AuthorizationCode</span></span>
- <span data-ttu-id="40c66-141">ClientCredentials</span><span class="sxs-lookup"><span data-stu-id="40c66-141">ClientCredentials</span></span> 
- <span data-ttu-id="40c66-142">Implicit</span><span class="sxs-lookup"><span data-stu-id="40c66-142">Implicit</span></span> 
- <span data-ttu-id="40c66-143">ResourceOwnerPassword</span><span class="sxs-lookup"><span data-stu-id="40c66-143">ResourceOwnerPassword</span></span>

```yaml
Type: PsApiManagementGrantType[]
Parameter Sets: (All)
Aliases: 
Accepted values: AuthorizationCode, Implicit, ResourceOwnerPassword, ClientCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40c66-144">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="40c66-144">-Name</span></span>
<span data-ttu-id="40c66-145">A módosítani kívánt engedélyezési kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="40c66-145">Specifies the name of the authorization server to modify.</span></span>

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

### <span data-ttu-id="40c66-146">-PassThru</span><span class="sxs-lookup"><span data-stu-id="40c66-146">-PassThru</span></span>
<span data-ttu-id="40c66-147">passthru</span><span class="sxs-lookup"><span data-stu-id="40c66-147">passthru</span></span>

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

### <span data-ttu-id="40c66-148">-ResourceOwnerPassword</span><span class="sxs-lookup"><span data-stu-id="40c66-148">-ResourceOwnerPassword</span></span>
<span data-ttu-id="40c66-149">Az erőforrás tulajdonosi jelszavát adja meg.</span><span class="sxs-lookup"><span data-stu-id="40c66-149">Specifies the resource owner password.</span></span>
<span data-ttu-id="40c66-150">Ezt a paramétert akkor kell megadnia, ha a ResourceOwnerPassword a *GrantTypes* paraméter adja meg.</span><span class="sxs-lookup"><span data-stu-id="40c66-150">You must specify this parameter if ResourceOwnerPassword is specified by the *GrantTypes* parameter.</span></span>

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

### <span data-ttu-id="40c66-151">-ResourceOwnerUsername</span><span class="sxs-lookup"><span data-stu-id="40c66-151">-ResourceOwnerUsername</span></span>
<span data-ttu-id="40c66-152">Az erőforrás-tulajdonos felhasználónevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="40c66-152">Specifies the resource owner user name.</span></span>
<span data-ttu-id="40c66-153">Ezt a paramétert akkor kell megadnia, ha a ResourceOwnerPassword a *GrantTypes* paraméter adja meg.</span><span class="sxs-lookup"><span data-stu-id="40c66-153">You must specify this parameter if ResourceOwnerPassword is specified by the *GrantTypes* parameter.</span></span>

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

### <span data-ttu-id="40c66-154">-ServerId</span><span class="sxs-lookup"><span data-stu-id="40c66-154">-ServerId</span></span>
<span data-ttu-id="40c66-155">A módosítani kívánt engedélyezési kiszolgáló AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="40c66-155">Specifies the ID of the authorization server to modify.</span></span>

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

### <span data-ttu-id="40c66-156">-SupportState</span><span class="sxs-lookup"><span data-stu-id="40c66-156">-SupportState</span></span>
<span data-ttu-id="40c66-157">Azt jelzi, hogy támogatja-e az *állami* paramétereket.</span><span class="sxs-lookup"><span data-stu-id="40c66-157">Indicates whether to support the *State* parameter.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40c66-158">-TokenBodyParameters</span><span class="sxs-lookup"><span data-stu-id="40c66-158">-TokenBodyParameters</span></span>
<span data-ttu-id="40c66-159">Az Application/x-www-Form-urlencoded formátumban adja meg a szövegtörzs további paramétereit.</span><span class="sxs-lookup"><span data-stu-id="40c66-159">Specifies additional body parameters using application/x-www-form-urlencoded format.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40c66-160">-TokenEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="40c66-160">-TokenEndpointUrl</span></span>
<span data-ttu-id="40c66-161">Annak a jogkivonat-végpontnak a meghatározása, amellyel az ügyfelek megkapják az Access-tokenek engedélyezési vagy frissítési tokenek megjelenítését az Exchange-ben.</span><span class="sxs-lookup"><span data-stu-id="40c66-161">Specifies the token endpoint for clients to obtain access tokens in exchange for presenting authorization grants or refresh tokens.</span></span>

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

### <span data-ttu-id="40c66-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40c66-162">CommonParameters</span></span>
<span data-ttu-id="40c66-163">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="40c66-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40c66-164">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40c66-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40c66-165">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="40c66-165">INPUTS</span></span>

### <span data-ttu-id="40c66-166">Nincs</span><span class="sxs-lookup"><span data-stu-id="40c66-166">None</span></span>
<span data-ttu-id="40c66-167">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="40c66-167">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="40c66-168">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="40c66-168">OUTPUTS</span></span>

### <span data-ttu-id="40c66-169">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementOAuth2AuthrozationServer</span><span class="sxs-lookup"><span data-stu-id="40c66-169">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOAuth2AuthrozationServer</span></span>

## <span data-ttu-id="40c66-170">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="40c66-170">NOTES</span></span>

## <span data-ttu-id="40c66-171">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="40c66-171">RELATED LINKS</span></span>

[<span data-ttu-id="40c66-172">Get-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="40c66-172">Get-AzureRmApiManagementAuthorizationServer</span></span>](./Get-AzureRmApiManagementAuthorizationServer.md)

[<span data-ttu-id="40c66-173">Új – AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="40c66-173">New-AzureRmApiManagementAuthorizationServer</span></span>](./New-AzureRmApiManagementAuthorizationServer.md)

[<span data-ttu-id="40c66-174">Remove-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="40c66-174">Remove-AzureRmApiManagementAuthorizationServer</span></span>](./Remove-AzureRmApiManagementAuthorizationServer.md)


