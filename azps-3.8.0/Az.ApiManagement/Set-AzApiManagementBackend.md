---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementBackend.md
ms.openlocfilehash: 8631120178a256aa1ec5b817727f9362f6d8f076
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100407284"
---
# <span data-ttu-id="1d3a7-101">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="1d3a7-101">Set-AzApiManagementBackend</span></span>

## <span data-ttu-id="1d3a7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d3a7-102">SYNOPSIS</span></span>
<span data-ttu-id="1d3a7-103">Frissíti a backend-et.</span><span class="sxs-lookup"><span data-stu-id="1d3a7-103">Updates a Backend.</span></span>

## <span data-ttu-id="1d3a7-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="1d3a7-104">SYNTAX</span></span>

### <span data-ttu-id="1d3a7-105">ContextParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1d3a7-105">ContextParameterSet (Default)</span></span>
```
Set-AzApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-Protocol <String>]
 [-Url <String>] [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>]
 [-ServiceFabricCluster <PsApiManagementServiceFabric>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d3a7-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="1d3a7-106">ByInputObject</span></span>
```
Set-AzApiManagementBackend -InputObject <PsApiManagementBackend> [-Protocol <String>] [-Url <String>]
 [-ResourceId <String>] [-Title <String>] [-Description <String>] [-SkipCertificateChainValidation <Boolean>]
 [-SkipCertificateNameValidation <Boolean>] [-Credential <PsApiManagementBackendCredential>]
 [-Proxy <PsApiManagementBackendProxy>] [-ServiceFabricCluster <PsApiManagementServiceFabric>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1d3a7-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="1d3a7-107">DESCRIPTION</span></span>
<span data-ttu-id="1d3a7-108">Frissíti a meglévő háttért az Api-kezelésben.</span><span class="sxs-lookup"><span data-stu-id="1d3a7-108">Updates an existing backend in the Api Management.</span></span>

## <span data-ttu-id="1d3a7-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="1d3a7-109">EXAMPLES</span></span>

### <span data-ttu-id="1d3a7-110">A Backend 123 leírásának frissítése</span><span class="sxs-lookup"><span data-stu-id="1d3a7-110">Updates the Description of the Backend 123</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementBackend -Context $apimContext -BackendId 123 -Description "updated description" -PassThru
```

## <span data-ttu-id="1d3a7-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1d3a7-111">PARAMETERS</span></span>

### <span data-ttu-id="1d3a7-112">-BackendId</span><span class="sxs-lookup"><span data-stu-id="1d3a7-112">-BackendId</span></span>
<span data-ttu-id="1d3a7-113">Az új háttér-háttér azonosítója.</span><span class="sxs-lookup"><span data-stu-id="1d3a7-113">Identifier of new backend.</span></span>
<span data-ttu-id="1d3a7-114">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="1d3a7-114">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d3a7-115">-Környezet</span><span class="sxs-lookup"><span data-stu-id="1d3a7-115">-Context</span></span>
<span data-ttu-id="1d3a7-116">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="1d3a7-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="1d3a7-117">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="1d3a7-117">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1d3a7-118">-Hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="1d3a7-118">-Credential</span></span>
<span data-ttu-id="1d3a7-119">A háttéradatokkal való beszélgetéshez használt hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="1d3a7-119">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="1d3a7-120">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="1d3a7-120">This parameter is optional.</span></span>

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

### <span data-ttu-id="1d3a7-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d3a7-121">-DefaultProfile</span></span>
<span data-ttu-id="1d3a7-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1d3a7-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1d3a7-123">-Leírás</span><span class="sxs-lookup"><span data-stu-id="1d3a7-123">-Description</span></span>
<span data-ttu-id="1d3a7-124">Háttér leírása.</span><span class="sxs-lookup"><span data-stu-id="1d3a7-124">Backend Description.</span></span>
<span data-ttu-id="1d3a7-125">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="1d3a7-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="1d3a7-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1d3a7-126">-InputObject</span></span>
<span data-ttu-id="1d3a7-127">A PsApiManagementBackend példánya.</span><span class="sxs-lookup"><span data-stu-id="1d3a7-127">Instance of PsApiManagementBackend.</span></span> <span data-ttu-id="1d3a7-128">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="1d3a7-128">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1d3a7-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1d3a7-129">-PassThru</span></span>
<span data-ttu-id="1d3a7-130">Azt jelzi, hogy ez a parancsmag a  **PsApiManagementBackend** értéket adja vissza, amely módosítja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="1d3a7-130">Indicates that this cmdlet returns the  **PsApiManagementBackend** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="1d3a7-131">-Protocol</span><span class="sxs-lookup"><span data-stu-id="1d3a7-131">-Protocol</span></span>
<span data-ttu-id="1d3a7-132">Backend Communication protocol (http vagy soap).</span><span class="sxs-lookup"><span data-stu-id="1d3a7-132">Backend Communication protocol (http or soap).</span></span>
<span data-ttu-id="1d3a7-133">Ez a paraméter nem kötelező</span><span class="sxs-lookup"><span data-stu-id="1d3a7-133">This parameter is optional</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: http, soap

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d3a7-134">-Proxy</span><span class="sxs-lookup"><span data-stu-id="1d3a7-134">-Proxy</span></span>
<span data-ttu-id="1d3a7-135">A proxykiszolgáló adatai, amelyek a kérés backendbe való elküldése közben használatosak.</span><span class="sxs-lookup"><span data-stu-id="1d3a7-135">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="1d3a7-136">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="1d3a7-136">This parameter is optional.</span></span>

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

### <span data-ttu-id="1d3a7-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1d3a7-137">-ResourceId</span></span>
<span data-ttu-id="1d3a7-138">Az erőforrás felügyeleti uri-ja a külső rendszerben.</span><span class="sxs-lookup"><span data-stu-id="1d3a7-138">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="1d3a7-139">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="1d3a7-139">This parameter is optional.</span></span>
<span data-ttu-id="1d3a7-140">Ez az URL-cím lehet a logic appok, függvényalkalmazások vagy API-appok Arm Resource Id azonosítója.</span><span class="sxs-lookup"><span data-stu-id="1d3a7-140">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

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

### <span data-ttu-id="1d3a7-141">-ServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="1d3a7-141">-ServiceFabricCluster</span></span>
<span data-ttu-id="1d3a7-142">Service Fabric Cluster Backend details.</span><span class="sxs-lookup"><span data-stu-id="1d3a7-142">Service Fabric Cluster Backend details.</span></span> <span data-ttu-id="1d3a7-143">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="1d3a7-143">This parameter is optional.</span></span>

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

### <span data-ttu-id="1d3a7-144">-SkipCertificateChainValidation</span><span class="sxs-lookup"><span data-stu-id="1d3a7-144">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="1d3a7-145">Hogy kihagyja-e a tanúsítványlánc-ellenőrzést, amikor a backend-hez beszél.</span><span class="sxs-lookup"><span data-stu-id="1d3a7-145">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="1d3a7-146">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="1d3a7-146">This parameter is optional.</span></span>

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

### <span data-ttu-id="1d3a7-147">-SkipCertificateNameValidation</span><span class="sxs-lookup"><span data-stu-id="1d3a7-147">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="1d3a7-148">Kihagyhatja-e a Tanúsítványnév érvényesítése érvénybe lépését a backend-hez való beszélgetés során.</span><span class="sxs-lookup"><span data-stu-id="1d3a7-148">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="1d3a7-149">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="1d3a7-149">This parameter is optional.</span></span>

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

### <span data-ttu-id="1d3a7-150">-Title</span><span class="sxs-lookup"><span data-stu-id="1d3a7-150">-Title</span></span>
<span data-ttu-id="1d3a7-151">Háttércím.</span><span class="sxs-lookup"><span data-stu-id="1d3a7-151">Backend Title.</span></span>
<span data-ttu-id="1d3a7-152">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="1d3a7-152">This parameter is optional.</span></span>

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

### <span data-ttu-id="1d3a7-153">-Url</span><span class="sxs-lookup"><span data-stu-id="1d3a7-153">-Url</span></span>
<span data-ttu-id="1d3a7-154">A Backend futásidejű URL-címe.</span><span class="sxs-lookup"><span data-stu-id="1d3a7-154">Runtime Url for the Backend.</span></span>
<span data-ttu-id="1d3a7-155">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="1d3a7-155">This parameter is optional.</span></span>

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

### <span data-ttu-id="1d3a7-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1d3a7-156">-Confirm</span></span>
<span data-ttu-id="1d3a7-157">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="1d3a7-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d3a7-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d3a7-158">-WhatIf</span></span>
<span data-ttu-id="1d3a7-159">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="1d3a7-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1d3a7-160">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1d3a7-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d3a7-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d3a7-161">CommonParameters</span></span>
<span data-ttu-id="1d3a7-162">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d3a7-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d3a7-163">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1d3a7-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d3a7-164">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1d3a7-164">INPUTS</span></span>

### <span data-ttu-id="1d3a7-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="1d3a7-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="1d3a7-166">System.String</span><span class="sxs-lookup"><span data-stu-id="1d3a7-166">System.String</span></span>

### <span data-ttu-id="1d3a7-167">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="1d3a7-167">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="1d3a7-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="1d3a7-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

### <span data-ttu-id="1d3a7-169">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="1d3a7-169">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

### <span data-ttu-id="1d3a7-170">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span><span class="sxs-lookup"><span data-stu-id="1d3a7-170">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span></span>

### <span data-ttu-id="1d3a7-171">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="1d3a7-171">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="1d3a7-172">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1d3a7-172">OUTPUTS</span></span>

### <span data-ttu-id="1d3a7-173">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="1d3a7-173">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="1d3a7-174">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="1d3a7-174">NOTES</span></span>

## <span data-ttu-id="1d3a7-175">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1d3a7-175">RELATED LINKS</span></span>

[<span data-ttu-id="1d3a7-176">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="1d3a7-176">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend.md)

[<span data-ttu-id="1d3a7-177">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="1d3a7-177">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="1d3a7-178">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="1d3a7-178">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="1d3a7-179">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="1d3a7-179">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="1d3a7-180">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="1d3a7-180">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
