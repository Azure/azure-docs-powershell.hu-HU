---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/new-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackend.md
ms.openlocfilehash: ba528724bebfc6ce3400ead69a223e08f42663ef
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010949"
---
# <span data-ttu-id="8d0f2-101">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="8d0f2-101">New-AzApiManagementBackend</span></span>

## <span data-ttu-id="8d0f2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d0f2-102">SYNOPSIS</span></span>
<span data-ttu-id="8d0f2-103">Létrehoz egy új háttérendentitást.</span><span class="sxs-lookup"><span data-stu-id="8d0f2-103">Creates a new backend entity.</span></span>

## <span data-ttu-id="8d0f2-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8d0f2-104">SYNTAX</span></span>

```
New-AzApiManagementBackend -Context <PsApiManagementContext> [-BackendId <String>] -Protocol <String>
 -Url <String> [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>]
 [-ServiceFabricCluster <PsApiManagementServiceFabric>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8d0f2-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8d0f2-105">DESCRIPTION</span></span>
<span data-ttu-id="8d0f2-106">Létrehoz egy új háttérendentitást az Api Managementben.</span><span class="sxs-lookup"><span data-stu-id="8d0f2-106">Creates a new backend entity in Api Management.</span></span>

## <span data-ttu-id="8d0f2-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8d0f2-107">EXAMPLES</span></span>

### <span data-ttu-id="8d0f2-108">1. példa: A Backend 123 létrehozása egyszerű engedélyezési sémával</span><span class="sxs-lookup"><span data-stu-id="8d0f2-108">Example 1: Create Backend 123 with a Basic Authorization Scheme</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$credential = New-AzApiManagementBackendCredential -AuthorizationHeaderScheme basic -AuthorizationHeaderParameter opensesame -Query @{"sv" = @('xx', 'bb'); "sr" = @('cc')} -Header @{"x-my-1" = @('val1', 'val2')}

PS C:\>$backend = New-AzApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Credential $credential -Description "my backend"
```

<span data-ttu-id="8d0f2-109">Új backend létrehozása</span><span class="sxs-lookup"><span data-stu-id="8d0f2-109">Creates a new Backend</span></span>

## <span data-ttu-id="8d0f2-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8d0f2-110">PARAMETERS</span></span>

### <span data-ttu-id="8d0f2-111">-BackendId</span><span class="sxs-lookup"><span data-stu-id="8d0f2-111">-BackendId</span></span>
<span data-ttu-id="8d0f2-112">Az új háttér-háttér azonosítója.</span><span class="sxs-lookup"><span data-stu-id="8d0f2-112">Identifier of new backend.</span></span>
<span data-ttu-id="8d0f2-113">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="8d0f2-113">This parameter is optional.</span></span>
<span data-ttu-id="8d0f2-114">Ha nincs megadva, akkor a program létrehoz egy újat.</span><span class="sxs-lookup"><span data-stu-id="8d0f2-114">If not specified will be generated.</span></span>

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

### <span data-ttu-id="8d0f2-115">-Környezet</span><span class="sxs-lookup"><span data-stu-id="8d0f2-115">-Context</span></span>
<span data-ttu-id="8d0f2-116">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="8d0f2-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="8d0f2-117">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="8d0f2-117">This parameter is required.</span></span>

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

### <span data-ttu-id="8d0f2-118">-Hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="8d0f2-118">-Credential</span></span>
<span data-ttu-id="8d0f2-119">A háttéradatokkal való beszélgetéshez használt hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="8d0f2-119">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="8d0f2-120">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="8d0f2-120">This parameter is optional.</span></span>

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

### <span data-ttu-id="8d0f2-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d0f2-121">-DefaultProfile</span></span>
<span data-ttu-id="8d0f2-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8d0f2-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8d0f2-123">-Leírás</span><span class="sxs-lookup"><span data-stu-id="8d0f2-123">-Description</span></span>
<span data-ttu-id="8d0f2-124">Háttér leírása.</span><span class="sxs-lookup"><span data-stu-id="8d0f2-124">Backend Description.</span></span>
<span data-ttu-id="8d0f2-125">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="8d0f2-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="8d0f2-126">-Protocol</span><span class="sxs-lookup"><span data-stu-id="8d0f2-126">-Protocol</span></span>
<span data-ttu-id="8d0f2-127">Backend Communication protocol.</span><span class="sxs-lookup"><span data-stu-id="8d0f2-127">Backend Communication protocol.</span></span>
<span data-ttu-id="8d0f2-128">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="8d0f2-128">This parameter is required.</span></span>
<span data-ttu-id="8d0f2-129">Érvényes értékek: "http" és "soap".</span><span class="sxs-lookup"><span data-stu-id="8d0f2-129">Valid values are 'http' and 'soap'.</span></span>

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

### <span data-ttu-id="8d0f2-130">-Proxy</span><span class="sxs-lookup"><span data-stu-id="8d0f2-130">-Proxy</span></span>
<span data-ttu-id="8d0f2-131">A proxykiszolgáló adatai, amelyek a kérés backendbe való elküldése közben használatosak.</span><span class="sxs-lookup"><span data-stu-id="8d0f2-131">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="8d0f2-132">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="8d0f2-132">This parameter is optional.</span></span>

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

### <span data-ttu-id="8d0f2-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8d0f2-133">-ResourceId</span></span>
<span data-ttu-id="8d0f2-134">Az erőforrás felügyeleti uri-ja a külső rendszerben.</span><span class="sxs-lookup"><span data-stu-id="8d0f2-134">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="8d0f2-135">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="8d0f2-135">This parameter is optional.</span></span>
<span data-ttu-id="8d0f2-136">Ez az URL-cím lehet a logic appok, függvényalkalmazások vagy API-appok Arm Resource Id azonosítója.</span><span class="sxs-lookup"><span data-stu-id="8d0f2-136">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

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

### <span data-ttu-id="8d0f2-137">-ServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="8d0f2-137">-ServiceFabricCluster</span></span>
<span data-ttu-id="8d0f2-138">Service Fabric Cluster Backend details.</span><span class="sxs-lookup"><span data-stu-id="8d0f2-138">Service Fabric Cluster Backend details.</span></span> <span data-ttu-id="8d0f2-139">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="8d0f2-139">This parameter is optional.</span></span>

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

### <span data-ttu-id="8d0f2-140">-SkipCertificateChainValidation</span><span class="sxs-lookup"><span data-stu-id="8d0f2-140">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="8d0f2-141">Hogy kihagyja-e a tanúsítványlánc-ellenőrzést, amikor a backend-hez beszél.</span><span class="sxs-lookup"><span data-stu-id="8d0f2-141">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="8d0f2-142">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="8d0f2-142">This parameter is optional.</span></span>

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

### <span data-ttu-id="8d0f2-143">-SkipCertificateNameValidation</span><span class="sxs-lookup"><span data-stu-id="8d0f2-143">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="8d0f2-144">Kihagyhatja-e a Tanúsítványnév érvényesítése érvénybe lépését a backend-hez való beszélgetés során.</span><span class="sxs-lookup"><span data-stu-id="8d0f2-144">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="8d0f2-145">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="8d0f2-145">This parameter is optional.</span></span>

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

### <span data-ttu-id="8d0f2-146">-Title</span><span class="sxs-lookup"><span data-stu-id="8d0f2-146">-Title</span></span>
<span data-ttu-id="8d0f2-147">Háttércím.</span><span class="sxs-lookup"><span data-stu-id="8d0f2-147">Backend Title.</span></span>
<span data-ttu-id="8d0f2-148">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="8d0f2-148">This parameter is optional.</span></span>

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

### <span data-ttu-id="8d0f2-149">-Url</span><span class="sxs-lookup"><span data-stu-id="8d0f2-149">-Url</span></span>
<span data-ttu-id="8d0f2-150">A Backend futásidejű URL-címe.</span><span class="sxs-lookup"><span data-stu-id="8d0f2-150">Runtime Url for the Backend.</span></span>
<span data-ttu-id="8d0f2-151">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="8d0f2-151">This parameter is required.</span></span>

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

### <span data-ttu-id="8d0f2-152">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8d0f2-152">-Confirm</span></span>
<span data-ttu-id="8d0f2-153">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="8d0f2-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d0f2-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d0f2-154">-WhatIf</span></span>
<span data-ttu-id="8d0f2-155">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="8d0f2-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8d0f2-156">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8d0f2-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d0f2-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d0f2-157">CommonParameters</span></span>
<span data-ttu-id="8d0f2-158">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d0f2-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d0f2-159">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8d0f2-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d0f2-160">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8d0f2-160">INPUTS</span></span>

### <span data-ttu-id="8d0f2-161">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="8d0f2-161">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="8d0f2-162">System.String</span><span class="sxs-lookup"><span data-stu-id="8d0f2-162">System.String</span></span>

### <span data-ttu-id="8d0f2-163">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="8d0f2-163">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="8d0f2-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="8d0f2-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

### <span data-ttu-id="8d0f2-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="8d0f2-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

### <span data-ttu-id="8d0f2-166">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8d0f2-166">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span></span>

## <span data-ttu-id="8d0f2-167">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8d0f2-167">OUTPUTS</span></span>

### <span data-ttu-id="8d0f2-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="8d0f2-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="8d0f2-169">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8d0f2-169">NOTES</span></span>

## <span data-ttu-id="8d0f2-170">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8d0f2-170">RELATED LINKS</span></span>

[<span data-ttu-id="8d0f2-171">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="8d0f2-171">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend.md)

[<span data-ttu-id="8d0f2-172">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="8d0f2-172">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="8d0f2-173">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="8d0f2-173">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="8d0f2-174">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="8d0f2-174">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="8d0f2-175">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="8d0f2-175">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)

