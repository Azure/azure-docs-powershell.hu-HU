---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackend.md
ms.openlocfilehash: 144830c2155379683c8568eda6e0d1bc021b38fb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498079"
---
# <span data-ttu-id="2c163-101">New-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="2c163-101">New-AzureRmApiManagementBackend</span></span>

## <span data-ttu-id="2c163-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2c163-102">SYNOPSIS</span></span>
<span data-ttu-id="2c163-103">Új backend-egyedet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="2c163-103">Creates a new backend entity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2c163-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2c163-104">SYNTAX</span></span>

```
New-AzureRmApiManagementBackend -Context <PsApiManagementContext> [-BackendId <String>] -Protocol <String>
 -Url <String> [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c163-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2c163-105">DESCRIPTION</span></span>
<span data-ttu-id="2c163-106">Új backend-entitás létrehozása az API-kezelésben.</span><span class="sxs-lookup"><span data-stu-id="2c163-106">Creates a new backend entity in Api Management.</span></span>

## <span data-ttu-id="2c163-107">Példák</span><span class="sxs-lookup"><span data-stu-id="2c163-107">EXAMPLES</span></span>

### <span data-ttu-id="2c163-108">A backend 123 létrehozása alapvető engedélyezési rendszerrel</span><span class="sxs-lookup"><span data-stu-id="2c163-108">Create Backend 123 with a Basic Authorization Scheme</span></span>
```
$credential = New-AzureRmApiManagementBackendCredential -AuthorizationHeaderScheme basic -AuthorizationHeaderParameter opensesame -Query @{"sv" = @('xx', 'bb'); "sr" = @('cc')} -Header @{"x-my-1" = @('val1', 'val2')}

$backend = New-AzureRmApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Credential $credential -Description "my backend"
```

<span data-ttu-id="2c163-109">Új backend létrehozása</span><span class="sxs-lookup"><span data-stu-id="2c163-109">Creates a new Backend</span></span>

## <span data-ttu-id="2c163-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2c163-110">PARAMETERS</span></span>

### <span data-ttu-id="2c163-111">-BackendId</span><span class="sxs-lookup"><span data-stu-id="2c163-111">-BackendId</span></span>
<span data-ttu-id="2c163-112">Új backend-azonosító.</span><span class="sxs-lookup"><span data-stu-id="2c163-112">Identifier of new backend.</span></span>
<span data-ttu-id="2c163-113">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="2c163-113">This parameter is optional.</span></span>
<span data-ttu-id="2c163-114">Ha a program nem adja meg a megadott értéket.</span><span class="sxs-lookup"><span data-stu-id="2c163-114">If not specified will be generated.</span></span>

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

### <span data-ttu-id="2c163-115">-Környezet</span><span class="sxs-lookup"><span data-stu-id="2c163-115">-Context</span></span>
<span data-ttu-id="2c163-116">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="2c163-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="2c163-117">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="2c163-117">This parameter is required.</span></span>

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

### <span data-ttu-id="2c163-118">-Hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="2c163-118">-Credential</span></span>
<span data-ttu-id="2c163-119">Hitelesítő adatok, amelyeket a háttérben való beszélgetés során használni kell.</span><span class="sxs-lookup"><span data-stu-id="2c163-119">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="2c163-120">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="2c163-120">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c163-121">-Leírás</span><span class="sxs-lookup"><span data-stu-id="2c163-121">-Description</span></span>
<span data-ttu-id="2c163-122">A backend leírása.</span><span class="sxs-lookup"><span data-stu-id="2c163-122">Backend Description.</span></span>
<span data-ttu-id="2c163-123">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="2c163-123">This parameter is optional.</span></span>

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

### <span data-ttu-id="2c163-124">-Protocol</span><span class="sxs-lookup"><span data-stu-id="2c163-124">-Protocol</span></span>
<span data-ttu-id="2c163-125">A backend kommunikációs protokollja.</span><span class="sxs-lookup"><span data-stu-id="2c163-125">Backend Communication protocol.</span></span>
<span data-ttu-id="2c163-126">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="2c163-126">This parameter is required.</span></span>
<span data-ttu-id="2c163-127">Az érvényes értékek a "http" és a "SOAP".</span><span class="sxs-lookup"><span data-stu-id="2c163-127">Valid values are 'http' and 'soap'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: http, soap

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c163-128">-Proxy</span><span class="sxs-lookup"><span data-stu-id="2c163-128">-Proxy</span></span>
<span data-ttu-id="2c163-129">A munkaablakba való küldéskor használandó proxykiszolgáló-adatok.</span><span class="sxs-lookup"><span data-stu-id="2c163-129">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="2c163-130">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="2c163-130">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c163-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2c163-131">-ResourceId</span></span>
<span data-ttu-id="2c163-132">Az erőforrás felügyeleti URI-ja külső rendszerben</span><span class="sxs-lookup"><span data-stu-id="2c163-132">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="2c163-133">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="2c163-133">This parameter is optional.</span></span>
<span data-ttu-id="2c163-134">Ez az URL-cím lehet a logikai alkalmazások, a függvények és az API-alkalmazások ARM erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="2c163-134">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

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

### <span data-ttu-id="2c163-135">-SkipCertificateChainValidation</span><span class="sxs-lookup"><span data-stu-id="2c163-135">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="2c163-136">Szeretné-e kihagyni a tanúsítványláncot az érvényesítést, ha a háttérrel beszél.</span><span class="sxs-lookup"><span data-stu-id="2c163-136">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="2c163-137">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="2c163-137">This parameter is optional.</span></span>

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

### <span data-ttu-id="2c163-138">-SkipCertificateNameValidation</span><span class="sxs-lookup"><span data-stu-id="2c163-138">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="2c163-139">Szeretné-e kihagyni a tanúsítvány nevének érvényesítését, amikor a háttérben beszél.</span><span class="sxs-lookup"><span data-stu-id="2c163-139">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="2c163-140">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="2c163-140">This parameter is optional.</span></span>

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

### <span data-ttu-id="2c163-141">-Cím</span><span class="sxs-lookup"><span data-stu-id="2c163-141">-Title</span></span>
<span data-ttu-id="2c163-142">A backend címe.</span><span class="sxs-lookup"><span data-stu-id="2c163-142">Backend Title.</span></span>
<span data-ttu-id="2c163-143">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="2c163-143">This parameter is optional.</span></span>

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

### <span data-ttu-id="2c163-144">-URL</span><span class="sxs-lookup"><span data-stu-id="2c163-144">-Url</span></span>
<span data-ttu-id="2c163-145">A backend futásidejű URL-címe.</span><span class="sxs-lookup"><span data-stu-id="2c163-145">Runtime Url for the Backend.</span></span>
<span data-ttu-id="2c163-146">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="2c163-146">This parameter is required.</span></span>

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

### <span data-ttu-id="2c163-147">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2c163-147">-Confirm</span></span>
<span data-ttu-id="2c163-148">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2c163-148">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c163-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c163-149">-WhatIf</span></span>
<span data-ttu-id="2c163-150">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2c163-150">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2c163-151">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2c163-151">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c163-152">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c163-152">-DefaultProfile</span></span>
<span data-ttu-id="2c163-153">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2c163-153">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2c163-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c163-154">CommonParameters</span></span>
<span data-ttu-id="2c163-155">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2c163-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c163-156">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c163-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c163-157">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2c163-157">INPUTS</span></span>

## <span data-ttu-id="2c163-158">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2c163-158">OUTPUTS</span></span>

### <span data-ttu-id="2c163-159">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="2c163-159">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="2c163-160">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2c163-160">NOTES</span></span>

## <span data-ttu-id="2c163-161">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2c163-161">RELATED LINKS</span></span>

[<span data-ttu-id="2c163-162">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="2c163-162">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="2c163-163">Új – AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="2c163-163">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="2c163-164">Új – AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="2c163-164">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="2c163-165">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="2c163-165">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)

[<span data-ttu-id="2c163-166">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="2c163-166">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)

