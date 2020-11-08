---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementBackend.md
ms.openlocfilehash: 30947e52e5a7afaa8bf2890b95f48f6bb6f36bce
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013859"
---
# <span data-ttu-id="1d35d-101">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="1d35d-101">Set-AzApiManagementBackend</span></span>

## <span data-ttu-id="1d35d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1d35d-102">SYNOPSIS</span></span>
<span data-ttu-id="1d35d-103">A backend frissítése</span><span class="sxs-lookup"><span data-stu-id="1d35d-103">Updates a Backend.</span></span>

## <span data-ttu-id="1d35d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1d35d-104">SYNTAX</span></span>

### <span data-ttu-id="1d35d-105">ContextParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1d35d-105">ContextParameterSet (Default)</span></span>
```
Set-AzApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-Protocol <String>]
 [-Url <String>] [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>]
 [-ServiceFabricCluster <PsApiManagementServiceFabric>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d35d-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="1d35d-106">ByInputObject</span></span>
```
Set-AzApiManagementBackend -InputObject <PsApiManagementBackend> [-Protocol <String>] [-Url <String>]
 [-ResourceId <String>] [-Title <String>] [-Description <String>] [-SkipCertificateChainValidation <Boolean>]
 [-SkipCertificateNameValidation <Boolean>] [-Credential <PsApiManagementBackendCredential>]
 [-Proxy <PsApiManagementBackendProxy>] [-ServiceFabricCluster <PsApiManagementServiceFabric>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1d35d-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="1d35d-107">DESCRIPTION</span></span>
<span data-ttu-id="1d35d-108">Egy meglévő backend frissítése az API-kezelésben.</span><span class="sxs-lookup"><span data-stu-id="1d35d-108">Updates an existing backend in the Api Management.</span></span>

## <span data-ttu-id="1d35d-109">Példák</span><span class="sxs-lookup"><span data-stu-id="1d35d-109">EXAMPLES</span></span>

### <span data-ttu-id="1d35d-110">A backend 123 leírásának frissítése</span><span class="sxs-lookup"><span data-stu-id="1d35d-110">Updates the Description of the Backend 123</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementBackend -Context $apimContext -BackendId 123 -Description "updated description" -PassThru
```

## <span data-ttu-id="1d35d-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1d35d-111">PARAMETERS</span></span>

### <span data-ttu-id="1d35d-112">-BackendId</span><span class="sxs-lookup"><span data-stu-id="1d35d-112">-BackendId</span></span>
<span data-ttu-id="1d35d-113">Új backend-azonosító.</span><span class="sxs-lookup"><span data-stu-id="1d35d-113">Identifier of new backend.</span></span>
<span data-ttu-id="1d35d-114">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="1d35d-114">This parameter is required.</span></span>

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

### <span data-ttu-id="1d35d-115">-Környezet</span><span class="sxs-lookup"><span data-stu-id="1d35d-115">-Context</span></span>
<span data-ttu-id="1d35d-116">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="1d35d-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="1d35d-117">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="1d35d-117">This parameter is required.</span></span>

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

### <span data-ttu-id="1d35d-118">-Hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="1d35d-118">-Credential</span></span>
<span data-ttu-id="1d35d-119">Hitelesítő adatok, amelyeket a háttérben való beszélgetés során használni kell.</span><span class="sxs-lookup"><span data-stu-id="1d35d-119">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="1d35d-120">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="1d35d-120">This parameter is optional.</span></span>

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

### <span data-ttu-id="1d35d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d35d-121">-DefaultProfile</span></span>
<span data-ttu-id="1d35d-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1d35d-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1d35d-123">-Leírás</span><span class="sxs-lookup"><span data-stu-id="1d35d-123">-Description</span></span>
<span data-ttu-id="1d35d-124">A backend leírása.</span><span class="sxs-lookup"><span data-stu-id="1d35d-124">Backend Description.</span></span>
<span data-ttu-id="1d35d-125">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="1d35d-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="1d35d-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1d35d-126">-InputObject</span></span>
<span data-ttu-id="1d35d-127">A PsApiManagementBackend példánya.</span><span class="sxs-lookup"><span data-stu-id="1d35d-127">Instance of PsApiManagementBackend.</span></span> <span data-ttu-id="1d35d-128">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="1d35d-128">This parameter is required.</span></span>

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

### <span data-ttu-id="1d35d-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1d35d-129">-PassThru</span></span>
<span data-ttu-id="1d35d-130">Jelzi, hogy ez a parancsmag a parancsmag által módosított  **PsApiManagementBackend** adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="1d35d-130">Indicates that this cmdlet returns the  **PsApiManagementBackend** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="1d35d-131">-Protocol</span><span class="sxs-lookup"><span data-stu-id="1d35d-131">-Protocol</span></span>
<span data-ttu-id="1d35d-132">Backend kommunikációs protokoll (http vagy SOAP).</span><span class="sxs-lookup"><span data-stu-id="1d35d-132">Backend Communication protocol (http or soap).</span></span>
<span data-ttu-id="1d35d-133">Ez a paraméter nem kötelező</span><span class="sxs-lookup"><span data-stu-id="1d35d-133">This parameter is optional</span></span>

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

### <span data-ttu-id="1d35d-134">-Proxy</span><span class="sxs-lookup"><span data-stu-id="1d35d-134">-Proxy</span></span>
<span data-ttu-id="1d35d-135">A munkaablakba való küldéskor használandó proxykiszolgáló-adatok.</span><span class="sxs-lookup"><span data-stu-id="1d35d-135">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="1d35d-136">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="1d35d-136">This parameter is optional.</span></span>

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

### <span data-ttu-id="1d35d-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1d35d-137">-ResourceId</span></span>
<span data-ttu-id="1d35d-138">Az erőforrás felügyeleti URI-ja külső rendszerben</span><span class="sxs-lookup"><span data-stu-id="1d35d-138">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="1d35d-139">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="1d35d-139">This parameter is optional.</span></span>
<span data-ttu-id="1d35d-140">Ez az URL-cím lehet a logikai alkalmazások, a függvények és az API-alkalmazások ARM erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="1d35d-140">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

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

### <span data-ttu-id="1d35d-141">-ServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="1d35d-141">-ServiceFabricCluster</span></span>
<span data-ttu-id="1d35d-142">A Service Fabric cluster backend részletei.</span><span class="sxs-lookup"><span data-stu-id="1d35d-142">Service Fabric Cluster Backend details.</span></span> <span data-ttu-id="1d35d-143">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="1d35d-143">This parameter is optional.</span></span>

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

### <span data-ttu-id="1d35d-144">-SkipCertificateChainValidation</span><span class="sxs-lookup"><span data-stu-id="1d35d-144">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="1d35d-145">Szeretné-e kihagyni a tanúsítványláncot az érvényesítést, ha a háttérrel beszél.</span><span class="sxs-lookup"><span data-stu-id="1d35d-145">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="1d35d-146">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="1d35d-146">This parameter is optional.</span></span>

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

### <span data-ttu-id="1d35d-147">-SkipCertificateNameValidation</span><span class="sxs-lookup"><span data-stu-id="1d35d-147">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="1d35d-148">Szeretné-e kihagyni a tanúsítvány nevének érvényesítését, amikor a háttérben beszél.</span><span class="sxs-lookup"><span data-stu-id="1d35d-148">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="1d35d-149">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="1d35d-149">This parameter is optional.</span></span>

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

### <span data-ttu-id="1d35d-150">-Cím</span><span class="sxs-lookup"><span data-stu-id="1d35d-150">-Title</span></span>
<span data-ttu-id="1d35d-151">A backend címe.</span><span class="sxs-lookup"><span data-stu-id="1d35d-151">Backend Title.</span></span>
<span data-ttu-id="1d35d-152">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="1d35d-152">This parameter is optional.</span></span>

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

### <span data-ttu-id="1d35d-153">-URL</span><span class="sxs-lookup"><span data-stu-id="1d35d-153">-Url</span></span>
<span data-ttu-id="1d35d-154">A backend futásidejű URL-címe.</span><span class="sxs-lookup"><span data-stu-id="1d35d-154">Runtime Url for the Backend.</span></span>
<span data-ttu-id="1d35d-155">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="1d35d-155">This parameter is optional.</span></span>

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

### <span data-ttu-id="1d35d-156">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="1d35d-156">-Confirm</span></span>
<span data-ttu-id="1d35d-157">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1d35d-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d35d-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d35d-158">-WhatIf</span></span>
<span data-ttu-id="1d35d-159">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="1d35d-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1d35d-160">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1d35d-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d35d-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d35d-161">CommonParameters</span></span>
<span data-ttu-id="1d35d-162">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1d35d-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d35d-163">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="1d35d-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d35d-164">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1d35d-164">INPUTS</span></span>

### <span data-ttu-id="1d35d-165">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="1d35d-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="1d35d-166">System. String</span><span class="sxs-lookup"><span data-stu-id="1d35d-166">System.String</span></span>

### <span data-ttu-id="1d35d-167">System. null ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="1d35d-167">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="1d35d-168">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="1d35d-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

### <span data-ttu-id="1d35d-169">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="1d35d-169">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

### <span data-ttu-id="1d35d-170">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementServiceFabric</span><span class="sxs-lookup"><span data-stu-id="1d35d-170">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span></span>

### <span data-ttu-id="1d35d-171">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="1d35d-171">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="1d35d-172">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1d35d-172">OUTPUTS</span></span>

### <span data-ttu-id="1d35d-173">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="1d35d-173">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="1d35d-174">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1d35d-174">NOTES</span></span>

## <span data-ttu-id="1d35d-175">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1d35d-175">RELATED LINKS</span></span>

[<span data-ttu-id="1d35d-176">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="1d35d-176">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend)

[<span data-ttu-id="1d35d-177">Új – AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="1d35d-177">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="1d35d-178">Új – AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="1d35d-178">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="1d35d-179">Új – AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="1d35d-179">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="1d35d-180">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="1d35d-180">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
