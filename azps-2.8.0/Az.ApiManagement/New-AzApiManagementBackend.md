---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackend.md
ms.openlocfilehash: 5caef678df0aef88f4655c031d53e995920d0379
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668064"
---
# <span data-ttu-id="48a63-101">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="48a63-101">New-AzApiManagementBackend</span></span>

## <span data-ttu-id="48a63-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="48a63-102">SYNOPSIS</span></span>
<span data-ttu-id="48a63-103">Új backend-egyedet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="48a63-103">Creates a new backend entity.</span></span>

## <span data-ttu-id="48a63-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="48a63-104">SYNTAX</span></span>

```
New-AzApiManagementBackend -Context <PsApiManagementContext> [-BackendId <String>] -Protocol <String>
 -Url <String> [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>]
 [-ServiceFabricCluster <PsApiManagementServiceFabric>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="48a63-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="48a63-105">DESCRIPTION</span></span>
<span data-ttu-id="48a63-106">Új backend-entitás létrehozása az API-kezelésben.</span><span class="sxs-lookup"><span data-stu-id="48a63-106">Creates a new backend entity in Api Management.</span></span>

## <span data-ttu-id="48a63-107">Példák</span><span class="sxs-lookup"><span data-stu-id="48a63-107">EXAMPLES</span></span>

### <span data-ttu-id="48a63-108">A backend 123 létrehozása alapvető engedélyezési rendszerrel</span><span class="sxs-lookup"><span data-stu-id="48a63-108">Create Backend 123 with a Basic Authorization Scheme</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$credential = New-AzApiManagementBackendCredential -AuthorizationHeaderScheme basic -AuthorizationHeaderParameter opensesame -Query @{"sv" = @('xx', 'bb'); "sr" = @('cc')} -Header @{"x-my-1" = @('val1', 'val2')}

PS C:\>$backend = New-AzApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Credential $credential -Description "my backend"
```

<span data-ttu-id="48a63-109">Új backend létrehozása</span><span class="sxs-lookup"><span data-stu-id="48a63-109">Creates a new Backend</span></span>

## <span data-ttu-id="48a63-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="48a63-110">PARAMETERS</span></span>

### <span data-ttu-id="48a63-111">-BackendId</span><span class="sxs-lookup"><span data-stu-id="48a63-111">-BackendId</span></span>
<span data-ttu-id="48a63-112">Új backend-azonosító.</span><span class="sxs-lookup"><span data-stu-id="48a63-112">Identifier of new backend.</span></span>
<span data-ttu-id="48a63-113">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="48a63-113">This parameter is optional.</span></span>
<span data-ttu-id="48a63-114">Ha a program nem adja meg a megadott értéket.</span><span class="sxs-lookup"><span data-stu-id="48a63-114">If not specified will be generated.</span></span>

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

### <span data-ttu-id="48a63-115">-Környezet</span><span class="sxs-lookup"><span data-stu-id="48a63-115">-Context</span></span>
<span data-ttu-id="48a63-116">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="48a63-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="48a63-117">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="48a63-117">This parameter is required.</span></span>

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

### <span data-ttu-id="48a63-118">-Hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="48a63-118">-Credential</span></span>
<span data-ttu-id="48a63-119">Hitelesítő adatok, amelyeket a háttérben való beszélgetés során használni kell.</span><span class="sxs-lookup"><span data-stu-id="48a63-119">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="48a63-120">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="48a63-120">This parameter is optional.</span></span>

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

### <span data-ttu-id="48a63-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48a63-121">-DefaultProfile</span></span>
<span data-ttu-id="48a63-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="48a63-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="48a63-123">-Leírás</span><span class="sxs-lookup"><span data-stu-id="48a63-123">-Description</span></span>
<span data-ttu-id="48a63-124">A backend leírása.</span><span class="sxs-lookup"><span data-stu-id="48a63-124">Backend Description.</span></span>
<span data-ttu-id="48a63-125">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="48a63-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="48a63-126">-Protocol</span><span class="sxs-lookup"><span data-stu-id="48a63-126">-Protocol</span></span>
<span data-ttu-id="48a63-127">A backend kommunikációs protokollja.</span><span class="sxs-lookup"><span data-stu-id="48a63-127">Backend Communication protocol.</span></span>
<span data-ttu-id="48a63-128">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="48a63-128">This parameter is required.</span></span>
<span data-ttu-id="48a63-129">Az érvényes értékek a "http" és a "SOAP".</span><span class="sxs-lookup"><span data-stu-id="48a63-129">Valid values are 'http' and 'soap'.</span></span>

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

### <span data-ttu-id="48a63-130">-Proxy</span><span class="sxs-lookup"><span data-stu-id="48a63-130">-Proxy</span></span>
<span data-ttu-id="48a63-131">A munkaablakba való küldéskor használandó proxykiszolgáló-adatok.</span><span class="sxs-lookup"><span data-stu-id="48a63-131">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="48a63-132">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="48a63-132">This parameter is optional.</span></span>

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

### <span data-ttu-id="48a63-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="48a63-133">-ResourceId</span></span>
<span data-ttu-id="48a63-134">Az erőforrás felügyeleti URI-ja külső rendszerben</span><span class="sxs-lookup"><span data-stu-id="48a63-134">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="48a63-135">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="48a63-135">This parameter is optional.</span></span>
<span data-ttu-id="48a63-136">Ez az URL-cím lehet a logikai alkalmazások, a függvények és az API-alkalmazások ARM erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="48a63-136">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

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

### <span data-ttu-id="48a63-137">-ServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="48a63-137">-ServiceFabricCluster</span></span>
<span data-ttu-id="48a63-138">A Service Fabric cluster backend részletei.</span><span class="sxs-lookup"><span data-stu-id="48a63-138">Service Fabric Cluster Backend details.</span></span> <span data-ttu-id="48a63-139">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="48a63-139">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48a63-140">-SkipCertificateChainValidation</span><span class="sxs-lookup"><span data-stu-id="48a63-140">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="48a63-141">Szeretné-e kihagyni a tanúsítványláncot az érvényesítést, ha a háttérrel beszél.</span><span class="sxs-lookup"><span data-stu-id="48a63-141">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="48a63-142">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="48a63-142">This parameter is optional.</span></span>

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

### <span data-ttu-id="48a63-143">-SkipCertificateNameValidation</span><span class="sxs-lookup"><span data-stu-id="48a63-143">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="48a63-144">Szeretné-e kihagyni a tanúsítvány nevének érvényesítését, amikor a háttérben beszél.</span><span class="sxs-lookup"><span data-stu-id="48a63-144">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="48a63-145">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="48a63-145">This parameter is optional.</span></span>

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

### <span data-ttu-id="48a63-146">-Cím</span><span class="sxs-lookup"><span data-stu-id="48a63-146">-Title</span></span>
<span data-ttu-id="48a63-147">A backend címe.</span><span class="sxs-lookup"><span data-stu-id="48a63-147">Backend Title.</span></span>
<span data-ttu-id="48a63-148">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="48a63-148">This parameter is optional.</span></span>

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

### <span data-ttu-id="48a63-149">-URL</span><span class="sxs-lookup"><span data-stu-id="48a63-149">-Url</span></span>
<span data-ttu-id="48a63-150">A backend futásidejű URL-címe.</span><span class="sxs-lookup"><span data-stu-id="48a63-150">Runtime Url for the Backend.</span></span>
<span data-ttu-id="48a63-151">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="48a63-151">This parameter is required.</span></span>

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

### <span data-ttu-id="48a63-152">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="48a63-152">-Confirm</span></span>
<span data-ttu-id="48a63-153">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="48a63-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48a63-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48a63-154">-WhatIf</span></span>
<span data-ttu-id="48a63-155">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="48a63-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="48a63-156">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="48a63-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48a63-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48a63-157">CommonParameters</span></span>
<span data-ttu-id="48a63-158">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="48a63-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48a63-159">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="48a63-159">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48a63-160">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="48a63-160">INPUTS</span></span>

### <span data-ttu-id="48a63-161">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="48a63-161">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="48a63-162">System. String</span><span class="sxs-lookup"><span data-stu-id="48a63-162">System.String</span></span>

### <span data-ttu-id="48a63-163">System. null ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="48a63-163">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="48a63-164">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="48a63-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

### <span data-ttu-id="48a63-165">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="48a63-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

### <span data-ttu-id="48a63-166">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementServiceFabric</span><span class="sxs-lookup"><span data-stu-id="48a63-166">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span></span>

## <span data-ttu-id="48a63-167">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="48a63-167">OUTPUTS</span></span>

### <span data-ttu-id="48a63-168">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="48a63-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="48a63-169">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="48a63-169">NOTES</span></span>

## <span data-ttu-id="48a63-170">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="48a63-170">RELATED LINKS</span></span>

[<span data-ttu-id="48a63-171">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="48a63-171">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend)

[<span data-ttu-id="48a63-172">Új – AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="48a63-172">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="48a63-173">Új – AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="48a63-173">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="48a63-174">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="48a63-174">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="48a63-175">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="48a63-175">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)

