---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackend.md
ms.openlocfilehash: c337e82c88c7fdbbc1f8a3663249126c9d92b19f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504639"
---
# <span data-ttu-id="60b7b-101">New-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="60b7b-101">New-AzureRmApiManagementBackend</span></span>

## <span data-ttu-id="60b7b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="60b7b-102">SYNOPSIS</span></span>
<span data-ttu-id="60b7b-103">Új backend-egyedet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="60b7b-103">Creates a new backend entity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="60b7b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="60b7b-104">SYNTAX</span></span>

```
New-AzureRmApiManagementBackend -Context <PsApiManagementContext> [-BackendId <String>] -Protocol <String>
 -Url <String> [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60b7b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="60b7b-105">DESCRIPTION</span></span>
<span data-ttu-id="60b7b-106">Új backend-entitás létrehozása az API-kezelésben.</span><span class="sxs-lookup"><span data-stu-id="60b7b-106">Creates a new backend entity in Api Management.</span></span>

## <span data-ttu-id="60b7b-107">Példák</span><span class="sxs-lookup"><span data-stu-id="60b7b-107">EXAMPLES</span></span>

### <span data-ttu-id="60b7b-108">A backend 123 létrehozása alapvető engedélyezési rendszerrel</span><span class="sxs-lookup"><span data-stu-id="60b7b-108">Create Backend 123 with a Basic Authorization Scheme</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$credential = New-AzureRmApiManagementBackendCredential -AuthorizationHeaderScheme basic -AuthorizationHeaderParameter opensesame -Query @{"sv" = @('xx', 'bb'); "sr" = @('cc')} -Header @{"x-my-1" = @('val1', 'val2')}

PS C:\>$backend = New-AzureRmApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Credential $credential -Description "my backend"
```

<span data-ttu-id="60b7b-109">Új backend létrehozása</span><span class="sxs-lookup"><span data-stu-id="60b7b-109">Creates a new Backend</span></span>

## <span data-ttu-id="60b7b-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="60b7b-110">PARAMETERS</span></span>

### <span data-ttu-id="60b7b-111">-BackendId</span><span class="sxs-lookup"><span data-stu-id="60b7b-111">-BackendId</span></span>
<span data-ttu-id="60b7b-112">Új backend-azonosító.</span><span class="sxs-lookup"><span data-stu-id="60b7b-112">Identifier of new backend.</span></span>
<span data-ttu-id="60b7b-113">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="60b7b-113">This parameter is optional.</span></span>
<span data-ttu-id="60b7b-114">Ha a program nem adja meg a megadott értéket.</span><span class="sxs-lookup"><span data-stu-id="60b7b-114">If not specified will be generated.</span></span>

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

### <span data-ttu-id="60b7b-115">-Környezet</span><span class="sxs-lookup"><span data-stu-id="60b7b-115">-Context</span></span>
<span data-ttu-id="60b7b-116">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="60b7b-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="60b7b-117">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="60b7b-117">This parameter is required.</span></span>

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

### <span data-ttu-id="60b7b-118">-Hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="60b7b-118">-Credential</span></span>
<span data-ttu-id="60b7b-119">Hitelesítő adatok, amelyeket a háttérben való beszélgetés során használni kell.</span><span class="sxs-lookup"><span data-stu-id="60b7b-119">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="60b7b-120">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="60b7b-120">This parameter is optional.</span></span>

```yaml
Type: PsApiManagementBackendCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60b7b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60b7b-121">-DefaultProfile</span></span>
<span data-ttu-id="60b7b-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="60b7b-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="60b7b-123">-Leírás</span><span class="sxs-lookup"><span data-stu-id="60b7b-123">-Description</span></span>
<span data-ttu-id="60b7b-124">A backend leírása.</span><span class="sxs-lookup"><span data-stu-id="60b7b-124">Backend Description.</span></span>
<span data-ttu-id="60b7b-125">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="60b7b-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="60b7b-126">-Protocol</span><span class="sxs-lookup"><span data-stu-id="60b7b-126">-Protocol</span></span>
<span data-ttu-id="60b7b-127">A backend kommunikációs protokollja.</span><span class="sxs-lookup"><span data-stu-id="60b7b-127">Backend Communication protocol.</span></span>
<span data-ttu-id="60b7b-128">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="60b7b-128">This parameter is required.</span></span>
<span data-ttu-id="60b7b-129">Az érvényes értékek a "http" és a "SOAP".</span><span class="sxs-lookup"><span data-stu-id="60b7b-129">Valid values are 'http' and 'soap'.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: http, soap

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60b7b-130">-Proxy</span><span class="sxs-lookup"><span data-stu-id="60b7b-130">-Proxy</span></span>
<span data-ttu-id="60b7b-131">A munkaablakba való küldéskor használandó proxykiszolgáló-adatok.</span><span class="sxs-lookup"><span data-stu-id="60b7b-131">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="60b7b-132">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="60b7b-132">This parameter is optional.</span></span>

```yaml
Type: PsApiManagementBackendProxy
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60b7b-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="60b7b-133">-ResourceId</span></span>
<span data-ttu-id="60b7b-134">Az erőforrás felügyeleti URI-ja külső rendszerben</span><span class="sxs-lookup"><span data-stu-id="60b7b-134">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="60b7b-135">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="60b7b-135">This parameter is optional.</span></span>
<span data-ttu-id="60b7b-136">Ez az URL-cím lehet a logikai alkalmazások, a függvények és az API-alkalmazások ARM erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="60b7b-136">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

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

### <span data-ttu-id="60b7b-137">-SkipCertificateChainValidation</span><span class="sxs-lookup"><span data-stu-id="60b7b-137">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="60b7b-138">Szeretné-e kihagyni a tanúsítványláncot az érvényesítést, ha a háttérrel beszél.</span><span class="sxs-lookup"><span data-stu-id="60b7b-138">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="60b7b-139">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="60b7b-139">This parameter is optional.</span></span>

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

### <span data-ttu-id="60b7b-140">-SkipCertificateNameValidation</span><span class="sxs-lookup"><span data-stu-id="60b7b-140">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="60b7b-141">Szeretné-e kihagyni a tanúsítvány nevének érvényesítését, amikor a háttérben beszél.</span><span class="sxs-lookup"><span data-stu-id="60b7b-141">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="60b7b-142">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="60b7b-142">This parameter is optional.</span></span>

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

### <span data-ttu-id="60b7b-143">-Cím</span><span class="sxs-lookup"><span data-stu-id="60b7b-143">-Title</span></span>
<span data-ttu-id="60b7b-144">A backend címe.</span><span class="sxs-lookup"><span data-stu-id="60b7b-144">Backend Title.</span></span>
<span data-ttu-id="60b7b-145">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="60b7b-145">This parameter is optional.</span></span>

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

### <span data-ttu-id="60b7b-146">-URL</span><span class="sxs-lookup"><span data-stu-id="60b7b-146">-Url</span></span>
<span data-ttu-id="60b7b-147">A backend futásidejű URL-címe.</span><span class="sxs-lookup"><span data-stu-id="60b7b-147">Runtime Url for the Backend.</span></span>
<span data-ttu-id="60b7b-148">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="60b7b-148">This parameter is required.</span></span>

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

### <span data-ttu-id="60b7b-149">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="60b7b-149">-Confirm</span></span>
<span data-ttu-id="60b7b-150">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="60b7b-150">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60b7b-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60b7b-151">-WhatIf</span></span>
<span data-ttu-id="60b7b-152">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="60b7b-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="60b7b-153">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="60b7b-153">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60b7b-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60b7b-154">CommonParameters</span></span>
<span data-ttu-id="60b7b-155">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="60b7b-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60b7b-156">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60b7b-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60b7b-157">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="60b7b-157">INPUTS</span></span>

### <span data-ttu-id="60b7b-158">Nincs</span><span class="sxs-lookup"><span data-stu-id="60b7b-158">None</span></span>
<span data-ttu-id="60b7b-159">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="60b7b-159">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="60b7b-160">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="60b7b-160">OUTPUTS</span></span>

### <span data-ttu-id="60b7b-161">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="60b7b-161">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="60b7b-162">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="60b7b-162">NOTES</span></span>

## <span data-ttu-id="60b7b-163">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="60b7b-163">RELATED LINKS</span></span>

[<span data-ttu-id="60b7b-164">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="60b7b-164">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="60b7b-165">Új – AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="60b7b-165">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="60b7b-166">Új – AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="60b7b-166">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="60b7b-167">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="60b7b-167">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)

[<span data-ttu-id="60b7b-168">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="60b7b-168">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)

