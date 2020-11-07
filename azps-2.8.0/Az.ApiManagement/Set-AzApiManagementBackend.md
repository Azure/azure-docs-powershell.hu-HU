---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementBackend.md
ms.openlocfilehash: f5cf0d9f80b15f178cb701b4474fa5dc13d957eb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667944"
---
# <span data-ttu-id="12ce4-101">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="12ce4-101">Set-AzApiManagementBackend</span></span>

## <span data-ttu-id="12ce4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="12ce4-102">SYNOPSIS</span></span>
<span data-ttu-id="12ce4-103">A backend frissítése</span><span class="sxs-lookup"><span data-stu-id="12ce4-103">Updates a Backend.</span></span>

## <span data-ttu-id="12ce4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="12ce4-104">SYNTAX</span></span>

### <span data-ttu-id="12ce4-105">ContextParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="12ce4-105">ContextParameterSet (Default)</span></span>
```
Set-AzApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-Protocol <String>]
 [-Url <String>] [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>]
 [-ServiceFabricCluster <PsApiManagementServiceFabric>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12ce4-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="12ce4-106">ByInputObject</span></span>
```
Set-AzApiManagementBackend -InputObject <PsApiManagementBackend> [-Protocol <String>] [-Url <String>]
 [-ResourceId <String>] [-Title <String>] [-Description <String>] [-SkipCertificateChainValidation <Boolean>]
 [-SkipCertificateNameValidation <Boolean>] [-Credential <PsApiManagementBackendCredential>]
 [-Proxy <PsApiManagementBackendProxy>] [-ServiceFabricCluster <PsApiManagementServiceFabric>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12ce4-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="12ce4-107">DESCRIPTION</span></span>
<span data-ttu-id="12ce4-108">Egy meglévő backend frissítése az API-kezelésben.</span><span class="sxs-lookup"><span data-stu-id="12ce4-108">Updates an existing backend in the Api Management.</span></span>

## <span data-ttu-id="12ce4-109">Példák</span><span class="sxs-lookup"><span data-stu-id="12ce4-109">EXAMPLES</span></span>

### <span data-ttu-id="12ce4-110">A backend 123 leírásának frissítése</span><span class="sxs-lookup"><span data-stu-id="12ce4-110">Updates the Description of the Backend 123</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementBackend -Context $apimContext -BackendId 123 -Description "updated description" -PassThru
```

## <span data-ttu-id="12ce4-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="12ce4-111">PARAMETERS</span></span>

### <span data-ttu-id="12ce4-112">-BackendId</span><span class="sxs-lookup"><span data-stu-id="12ce4-112">-BackendId</span></span>
<span data-ttu-id="12ce4-113">Új backend-azonosító.</span><span class="sxs-lookup"><span data-stu-id="12ce4-113">Identifier of new backend.</span></span>
<span data-ttu-id="12ce4-114">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="12ce4-114">This parameter is required.</span></span>

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

### <span data-ttu-id="12ce4-115">-Környezet</span><span class="sxs-lookup"><span data-stu-id="12ce4-115">-Context</span></span>
<span data-ttu-id="12ce4-116">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="12ce4-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="12ce4-117">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="12ce4-117">This parameter is required.</span></span>

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

### <span data-ttu-id="12ce4-118">-Hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="12ce4-118">-Credential</span></span>
<span data-ttu-id="12ce4-119">Hitelesítő adatok, amelyeket a háttérben való beszélgetés során használni kell.</span><span class="sxs-lookup"><span data-stu-id="12ce4-119">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="12ce4-120">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="12ce4-120">This parameter is optional.</span></span>

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

### <span data-ttu-id="12ce4-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12ce4-121">-DefaultProfile</span></span>
<span data-ttu-id="12ce4-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="12ce4-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="12ce4-123">-Leírás</span><span class="sxs-lookup"><span data-stu-id="12ce4-123">-Description</span></span>
<span data-ttu-id="12ce4-124">A backend leírása.</span><span class="sxs-lookup"><span data-stu-id="12ce4-124">Backend Description.</span></span>
<span data-ttu-id="12ce4-125">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="12ce4-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="12ce4-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="12ce4-126">-InputObject</span></span>
<span data-ttu-id="12ce4-127">A PsApiManagementBackend példánya.</span><span class="sxs-lookup"><span data-stu-id="12ce4-127">Instance of PsApiManagementBackend.</span></span> <span data-ttu-id="12ce4-128">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="12ce4-128">This parameter is required.</span></span>

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

### <span data-ttu-id="12ce4-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="12ce4-129">-PassThru</span></span>
<span data-ttu-id="12ce4-130">Jelzi, hogy ez a parancsmag a parancsmag által módosított  **PsApiManagementBackend** adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="12ce4-130">Indicates that this cmdlet returns the  **PsApiManagementBackend** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="12ce4-131">-Protocol</span><span class="sxs-lookup"><span data-stu-id="12ce4-131">-Protocol</span></span>
<span data-ttu-id="12ce4-132">Backend kommunikációs protokoll (http vagy SOAP).</span><span class="sxs-lookup"><span data-stu-id="12ce4-132">Backend Communication protocol (http or soap).</span></span>
<span data-ttu-id="12ce4-133">Ez a paraméter nem kötelező</span><span class="sxs-lookup"><span data-stu-id="12ce4-133">This parameter is optional</span></span>

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

### <span data-ttu-id="12ce4-134">-Proxy</span><span class="sxs-lookup"><span data-stu-id="12ce4-134">-Proxy</span></span>
<span data-ttu-id="12ce4-135">A munkaablakba való küldéskor használandó proxykiszolgáló-adatok.</span><span class="sxs-lookup"><span data-stu-id="12ce4-135">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="12ce4-136">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="12ce4-136">This parameter is optional.</span></span>

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

### <span data-ttu-id="12ce4-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="12ce4-137">-ResourceId</span></span>
<span data-ttu-id="12ce4-138">Az erőforrás felügyeleti URI-ja külső rendszerben</span><span class="sxs-lookup"><span data-stu-id="12ce4-138">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="12ce4-139">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="12ce4-139">This parameter is optional.</span></span>
<span data-ttu-id="12ce4-140">Ez az URL-cím lehet a logikai alkalmazások, a függvények és az API-alkalmazások ARM erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="12ce4-140">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

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

### <span data-ttu-id="12ce4-141">-ServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="12ce4-141">-ServiceFabricCluster</span></span>
<span data-ttu-id="12ce4-142">A Service Fabric cluster backend részletei.</span><span class="sxs-lookup"><span data-stu-id="12ce4-142">Service Fabric Cluster Backend details.</span></span> <span data-ttu-id="12ce4-143">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="12ce4-143">This parameter is optional.</span></span>

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

### <span data-ttu-id="12ce4-144">-SkipCertificateChainValidation</span><span class="sxs-lookup"><span data-stu-id="12ce4-144">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="12ce4-145">Szeretné-e kihagyni a tanúsítványláncot az érvényesítést, ha a háttérrel beszél.</span><span class="sxs-lookup"><span data-stu-id="12ce4-145">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="12ce4-146">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="12ce4-146">This parameter is optional.</span></span>

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

### <span data-ttu-id="12ce4-147">-SkipCertificateNameValidation</span><span class="sxs-lookup"><span data-stu-id="12ce4-147">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="12ce4-148">Szeretné-e kihagyni a tanúsítvány nevének érvényesítését, amikor a háttérben beszél.</span><span class="sxs-lookup"><span data-stu-id="12ce4-148">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="12ce4-149">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="12ce4-149">This parameter is optional.</span></span>

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

### <span data-ttu-id="12ce4-150">-Cím</span><span class="sxs-lookup"><span data-stu-id="12ce4-150">-Title</span></span>
<span data-ttu-id="12ce4-151">A backend címe.</span><span class="sxs-lookup"><span data-stu-id="12ce4-151">Backend Title.</span></span>
<span data-ttu-id="12ce4-152">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="12ce4-152">This parameter is optional.</span></span>

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

### <span data-ttu-id="12ce4-153">-URL</span><span class="sxs-lookup"><span data-stu-id="12ce4-153">-Url</span></span>
<span data-ttu-id="12ce4-154">A backend futásidejű URL-címe.</span><span class="sxs-lookup"><span data-stu-id="12ce4-154">Runtime Url for the Backend.</span></span>
<span data-ttu-id="12ce4-155">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="12ce4-155">This parameter is optional.</span></span>

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

### <span data-ttu-id="12ce4-156">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="12ce4-156">-Confirm</span></span>
<span data-ttu-id="12ce4-157">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="12ce4-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12ce4-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12ce4-158">-WhatIf</span></span>
<span data-ttu-id="12ce4-159">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="12ce4-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="12ce4-160">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="12ce4-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12ce4-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12ce4-161">CommonParameters</span></span>
<span data-ttu-id="12ce4-162">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="12ce4-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12ce4-163">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="12ce4-163">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12ce4-164">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="12ce4-164">INPUTS</span></span>

### <span data-ttu-id="12ce4-165">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="12ce4-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="12ce4-166">System. String</span><span class="sxs-lookup"><span data-stu-id="12ce4-166">System.String</span></span>

### <span data-ttu-id="12ce4-167">System. null ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="12ce4-167">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="12ce4-168">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="12ce4-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

### <span data-ttu-id="12ce4-169">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="12ce4-169">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

### <span data-ttu-id="12ce4-170">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementServiceFabric</span><span class="sxs-lookup"><span data-stu-id="12ce4-170">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span></span>

### <span data-ttu-id="12ce4-171">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="12ce4-171">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="12ce4-172">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="12ce4-172">OUTPUTS</span></span>

### <span data-ttu-id="12ce4-173">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="12ce4-173">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="12ce4-174">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="12ce4-174">NOTES</span></span>

## <span data-ttu-id="12ce4-175">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="12ce4-175">RELATED LINKS</span></span>

[<span data-ttu-id="12ce4-176">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="12ce4-176">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend)

[<span data-ttu-id="12ce4-177">Új – AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="12ce4-177">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="12ce4-178">Új – AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="12ce4-178">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="12ce4-179">Új – AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="12ce4-179">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="12ce4-180">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="12ce4-180">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
