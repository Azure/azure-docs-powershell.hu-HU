---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackend.md
ms.openlocfilehash: 1f78630f195fca7e08ed755dbaeb48e413c8f8d1
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100401006"
---
# <span data-ttu-id="7250d-101">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="7250d-101">New-AzApiManagementBackend</span></span>

## <span data-ttu-id="7250d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7250d-102">SYNOPSIS</span></span>
<span data-ttu-id="7250d-103">Létrehoz egy új háttérendentitást.</span><span class="sxs-lookup"><span data-stu-id="7250d-103">Creates a new backend entity.</span></span>

## <span data-ttu-id="7250d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7250d-104">SYNTAX</span></span>

```
New-AzApiManagementBackend -Context <PsApiManagementContext> [-BackendId <String>] -Protocol <String>
 -Url <String> [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>]
 [-ServiceFabricCluster <PsApiManagementServiceFabric>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7250d-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7250d-105">DESCRIPTION</span></span>
<span data-ttu-id="7250d-106">Létrehoz egy új háttérendentitást az Api Managementben.</span><span class="sxs-lookup"><span data-stu-id="7250d-106">Creates a new backend entity in Api Management.</span></span>

## <span data-ttu-id="7250d-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7250d-107">EXAMPLES</span></span>

### <span data-ttu-id="7250d-108">A Backend 123 létrehozása egyszerű engedélyezési sémával</span><span class="sxs-lookup"><span data-stu-id="7250d-108">Create Backend 123 with a Basic Authorization Scheme</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$credential = New-AzApiManagementBackendCredential -AuthorizationHeaderScheme basic -AuthorizationHeaderParameter opensesame -Query @{"sv" = @('xx', 'bb'); "sr" = @('cc')} -Header @{"x-my-1" = @('val1', 'val2')}

PS C:\>$backend = New-AzApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Credential $credential -Description "my backend"
```

<span data-ttu-id="7250d-109">Új backend létrehozása</span><span class="sxs-lookup"><span data-stu-id="7250d-109">Creates a new Backend</span></span>

## <span data-ttu-id="7250d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7250d-110">PARAMETERS</span></span>

### <span data-ttu-id="7250d-111">-BackendId</span><span class="sxs-lookup"><span data-stu-id="7250d-111">-BackendId</span></span>
<span data-ttu-id="7250d-112">Az új háttér-háttér azonosítója.</span><span class="sxs-lookup"><span data-stu-id="7250d-112">Identifier of new backend.</span></span>
<span data-ttu-id="7250d-113">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="7250d-113">This parameter is optional.</span></span>
<span data-ttu-id="7250d-114">Ha nincs megadva, akkor a program létrehoz egy újat.</span><span class="sxs-lookup"><span data-stu-id="7250d-114">If not specified will be generated.</span></span>

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

### <span data-ttu-id="7250d-115">-Környezet</span><span class="sxs-lookup"><span data-stu-id="7250d-115">-Context</span></span>
<span data-ttu-id="7250d-116">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="7250d-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="7250d-117">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="7250d-117">This parameter is required.</span></span>

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

### <span data-ttu-id="7250d-118">-Hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="7250d-118">-Credential</span></span>
<span data-ttu-id="7250d-119">A háttéradatokkal való beszélgetéshez használt hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="7250d-119">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="7250d-120">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="7250d-120">This parameter is optional.</span></span>

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

### <span data-ttu-id="7250d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7250d-121">-DefaultProfile</span></span>
<span data-ttu-id="7250d-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7250d-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7250d-123">-Leírás</span><span class="sxs-lookup"><span data-stu-id="7250d-123">-Description</span></span>
<span data-ttu-id="7250d-124">Háttér leírása.</span><span class="sxs-lookup"><span data-stu-id="7250d-124">Backend Description.</span></span>
<span data-ttu-id="7250d-125">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="7250d-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="7250d-126">-Protocol</span><span class="sxs-lookup"><span data-stu-id="7250d-126">-Protocol</span></span>
<span data-ttu-id="7250d-127">Backend Communication protocol.</span><span class="sxs-lookup"><span data-stu-id="7250d-127">Backend Communication protocol.</span></span>
<span data-ttu-id="7250d-128">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="7250d-128">This parameter is required.</span></span>
<span data-ttu-id="7250d-129">Érvényes értékek: "http" és "szappan".</span><span class="sxs-lookup"><span data-stu-id="7250d-129">Valid values are 'http' and 'soap'.</span></span>

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

### <span data-ttu-id="7250d-130">-Proxy</span><span class="sxs-lookup"><span data-stu-id="7250d-130">-Proxy</span></span>
<span data-ttu-id="7250d-131">A proxykiszolgáló adatai, amelyek a kérés backendbe való elküldése közben használatosak.</span><span class="sxs-lookup"><span data-stu-id="7250d-131">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="7250d-132">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="7250d-132">This parameter is optional.</span></span>

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

### <span data-ttu-id="7250d-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7250d-133">-ResourceId</span></span>
<span data-ttu-id="7250d-134">Az erőforrás felügyeleti uri-ja a külső rendszerben.</span><span class="sxs-lookup"><span data-stu-id="7250d-134">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="7250d-135">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="7250d-135">This parameter is optional.</span></span>
<span data-ttu-id="7250d-136">Ez az URL-cím lehet a logic appok, függvényalkalmazások vagy API-appok Arm Resource Id azonosítója.</span><span class="sxs-lookup"><span data-stu-id="7250d-136">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

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

### <span data-ttu-id="7250d-137">-ServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="7250d-137">-ServiceFabricCluster</span></span>
<span data-ttu-id="7250d-138">Service Fabric Cluster Backend details.</span><span class="sxs-lookup"><span data-stu-id="7250d-138">Service Fabric Cluster Backend details.</span></span> <span data-ttu-id="7250d-139">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="7250d-139">This parameter is optional.</span></span>

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

### <span data-ttu-id="7250d-140">-SkipCertificateChainValidation</span><span class="sxs-lookup"><span data-stu-id="7250d-140">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="7250d-141">Hogy kihagyja-e a tanúsítványlánc-ellenőrzést, amikor a backend-hez beszél.</span><span class="sxs-lookup"><span data-stu-id="7250d-141">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="7250d-142">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="7250d-142">This parameter is optional.</span></span>

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

### <span data-ttu-id="7250d-143">-SkipCertificateNameValidation</span><span class="sxs-lookup"><span data-stu-id="7250d-143">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="7250d-144">Kihagyhatja-e a Tanúsítványnév érvényesítése érvénybe lépését a backend-hez való beszélgetés során.</span><span class="sxs-lookup"><span data-stu-id="7250d-144">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="7250d-145">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="7250d-145">This parameter is optional.</span></span>

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

### <span data-ttu-id="7250d-146">-Title</span><span class="sxs-lookup"><span data-stu-id="7250d-146">-Title</span></span>
<span data-ttu-id="7250d-147">Háttércím.</span><span class="sxs-lookup"><span data-stu-id="7250d-147">Backend Title.</span></span>
<span data-ttu-id="7250d-148">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="7250d-148">This parameter is optional.</span></span>

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

### <span data-ttu-id="7250d-149">-Url</span><span class="sxs-lookup"><span data-stu-id="7250d-149">-Url</span></span>
<span data-ttu-id="7250d-150">A Backend futásidejű URL-címe.</span><span class="sxs-lookup"><span data-stu-id="7250d-150">Runtime Url for the Backend.</span></span>
<span data-ttu-id="7250d-151">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="7250d-151">This parameter is required.</span></span>

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

### <span data-ttu-id="7250d-152">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7250d-152">-Confirm</span></span>
<span data-ttu-id="7250d-153">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="7250d-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7250d-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7250d-154">-WhatIf</span></span>
<span data-ttu-id="7250d-155">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="7250d-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7250d-156">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7250d-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7250d-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7250d-157">CommonParameters</span></span>
<span data-ttu-id="7250d-158">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7250d-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7250d-159">További információt a about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7250d-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7250d-160">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7250d-160">INPUTS</span></span>

### <span data-ttu-id="7250d-161">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="7250d-161">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="7250d-162">System.String</span><span class="sxs-lookup"><span data-stu-id="7250d-162">System.String</span></span>

### <span data-ttu-id="7250d-163">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="7250d-163">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="7250d-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="7250d-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

### <span data-ttu-id="7250d-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="7250d-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

### <span data-ttu-id="7250d-166">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span><span class="sxs-lookup"><span data-stu-id="7250d-166">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span></span>

## <span data-ttu-id="7250d-167">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7250d-167">OUTPUTS</span></span>

### <span data-ttu-id="7250d-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="7250d-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="7250d-169">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7250d-169">NOTES</span></span>

## <span data-ttu-id="7250d-170">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7250d-170">RELATED LINKS</span></span>

[<span data-ttu-id="7250d-171">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="7250d-171">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend.md)

[<span data-ttu-id="7250d-172">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="7250d-172">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="7250d-173">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="7250d-173">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="7250d-174">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="7250d-174">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="7250d-175">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="7250d-175">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)

