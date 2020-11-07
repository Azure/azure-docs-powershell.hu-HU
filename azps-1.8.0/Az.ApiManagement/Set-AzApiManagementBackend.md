---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementBackend.md
ms.openlocfilehash: ce27a151ebb6d778ed647fb81909c44c11edbf8e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836918"
---
# <span data-ttu-id="98ef4-101">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="98ef4-101">Set-AzApiManagementBackend</span></span>

## <span data-ttu-id="98ef4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="98ef4-102">SYNOPSIS</span></span>
<span data-ttu-id="98ef4-103">A backend frissítése</span><span class="sxs-lookup"><span data-stu-id="98ef4-103">Updates a Backend.</span></span>

## <span data-ttu-id="98ef4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="98ef4-104">SYNTAX</span></span>

```
Set-AzApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-Protocol <String>]
 [-Url <String>] [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>]
 [-ServiceFabricCluster <PsApiManagementServiceFabric>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="98ef4-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="98ef4-105">DESCRIPTION</span></span>
<span data-ttu-id="98ef4-106">Egy meglévő backend frissítése az API-kezelésben.</span><span class="sxs-lookup"><span data-stu-id="98ef4-106">Updates an existing backend in the Api Management.</span></span>

## <span data-ttu-id="98ef4-107">Példák</span><span class="sxs-lookup"><span data-stu-id="98ef4-107">EXAMPLES</span></span>

### <span data-ttu-id="98ef4-108">A backend 123 leírásának frissítése</span><span class="sxs-lookup"><span data-stu-id="98ef4-108">Updates the Description of the Backend 123</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementBackend -Context $apimContext -BackendId 123 -Description "updated description" -PassThru
```

## <span data-ttu-id="98ef4-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="98ef4-109">PARAMETERS</span></span>

### <span data-ttu-id="98ef4-110">-BackendId</span><span class="sxs-lookup"><span data-stu-id="98ef4-110">-BackendId</span></span>
<span data-ttu-id="98ef4-111">Új backend-azonosító.</span><span class="sxs-lookup"><span data-stu-id="98ef4-111">Identifier of new backend.</span></span>
<span data-ttu-id="98ef4-112">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="98ef4-112">This parameter is required.</span></span>

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

### <span data-ttu-id="98ef4-113">-Környezet</span><span class="sxs-lookup"><span data-stu-id="98ef4-113">-Context</span></span>
<span data-ttu-id="98ef4-114">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="98ef4-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="98ef4-115">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="98ef4-115">This parameter is required.</span></span>

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

### <span data-ttu-id="98ef4-116">-Hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="98ef4-116">-Credential</span></span>
<span data-ttu-id="98ef4-117">Hitelesítő adatok, amelyeket a háttérben való beszélgetés során használni kell.</span><span class="sxs-lookup"><span data-stu-id="98ef4-117">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="98ef4-118">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="98ef4-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="98ef4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98ef4-119">-DefaultProfile</span></span>
<span data-ttu-id="98ef4-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="98ef4-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="98ef4-121">-Leírás</span><span class="sxs-lookup"><span data-stu-id="98ef4-121">-Description</span></span>
<span data-ttu-id="98ef4-122">A backend leírása.</span><span class="sxs-lookup"><span data-stu-id="98ef4-122">Backend Description.</span></span>
<span data-ttu-id="98ef4-123">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="98ef4-123">This parameter is optional.</span></span>

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

### <span data-ttu-id="98ef4-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="98ef4-124">-PassThru</span></span>
<span data-ttu-id="98ef4-125">Jelzi, hogy ez a parancsmag a parancsmag által módosított  **PsApiManagementBackend** adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="98ef4-125">Indicates that this cmdlet returns the  **PsApiManagementBackend** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="98ef4-126">-Protocol</span><span class="sxs-lookup"><span data-stu-id="98ef4-126">-Protocol</span></span>
<span data-ttu-id="98ef4-127">Backend kommunikációs protokoll (http vagy SOAP).</span><span class="sxs-lookup"><span data-stu-id="98ef4-127">Backend Communication protocol (http or soap).</span></span>
<span data-ttu-id="98ef4-128">Ez a paraméter nem kötelező</span><span class="sxs-lookup"><span data-stu-id="98ef4-128">This parameter is optional</span></span>

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

### <span data-ttu-id="98ef4-129">-Proxy</span><span class="sxs-lookup"><span data-stu-id="98ef4-129">-Proxy</span></span>
<span data-ttu-id="98ef4-130">A munkaablakba való küldéskor használandó proxykiszolgáló-adatok.</span><span class="sxs-lookup"><span data-stu-id="98ef4-130">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="98ef4-131">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="98ef4-131">This parameter is optional.</span></span>

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

### <span data-ttu-id="98ef4-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="98ef4-132">-ResourceId</span></span>
<span data-ttu-id="98ef4-133">Az erőforrás felügyeleti URI-ja külső rendszerben</span><span class="sxs-lookup"><span data-stu-id="98ef4-133">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="98ef4-134">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="98ef4-134">This parameter is optional.</span></span>
<span data-ttu-id="98ef4-135">Ez az URL-cím lehet a logikai alkalmazások, a függvények és az API-alkalmazások ARM erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="98ef4-135">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

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

### <span data-ttu-id="98ef4-136">-ServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="98ef4-136">-ServiceFabricCluster</span></span>
<span data-ttu-id="98ef4-137">A Service Fabric cluster backend részletei.</span><span class="sxs-lookup"><span data-stu-id="98ef4-137">Service Fabric Cluster Backend details.</span></span> <span data-ttu-id="98ef4-138">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="98ef4-138">This parameter is optional.</span></span>

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

### <span data-ttu-id="98ef4-139">-SkipCertificateChainValidation</span><span class="sxs-lookup"><span data-stu-id="98ef4-139">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="98ef4-140">Szeretné-e kihagyni a tanúsítványláncot az érvényesítést, ha a háttérrel beszél.</span><span class="sxs-lookup"><span data-stu-id="98ef4-140">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="98ef4-141">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="98ef4-141">This parameter is optional.</span></span>

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

### <span data-ttu-id="98ef4-142">-SkipCertificateNameValidation</span><span class="sxs-lookup"><span data-stu-id="98ef4-142">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="98ef4-143">Szeretné-e kihagyni a tanúsítvány nevének érvényesítését, amikor a háttérben beszél.</span><span class="sxs-lookup"><span data-stu-id="98ef4-143">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="98ef4-144">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="98ef4-144">This parameter is optional.</span></span>

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

### <span data-ttu-id="98ef4-145">-Cím</span><span class="sxs-lookup"><span data-stu-id="98ef4-145">-Title</span></span>
<span data-ttu-id="98ef4-146">A backend címe.</span><span class="sxs-lookup"><span data-stu-id="98ef4-146">Backend Title.</span></span>
<span data-ttu-id="98ef4-147">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="98ef4-147">This parameter is optional.</span></span>

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

### <span data-ttu-id="98ef4-148">-URL</span><span class="sxs-lookup"><span data-stu-id="98ef4-148">-Url</span></span>
<span data-ttu-id="98ef4-149">A backend futásidejű URL-címe.</span><span class="sxs-lookup"><span data-stu-id="98ef4-149">Runtime Url for the Backend.</span></span>
<span data-ttu-id="98ef4-150">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="98ef4-150">This parameter is optional.</span></span>

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

### <span data-ttu-id="98ef4-151">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="98ef4-151">-Confirm</span></span>
<span data-ttu-id="98ef4-152">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="98ef4-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98ef4-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98ef4-153">-WhatIf</span></span>
<span data-ttu-id="98ef4-154">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="98ef4-154">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="98ef4-155">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="98ef4-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98ef4-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98ef4-156">CommonParameters</span></span>
<span data-ttu-id="98ef4-157">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="98ef4-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98ef4-158">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98ef4-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98ef4-159">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="98ef4-159">INPUTS</span></span>

### <span data-ttu-id="98ef4-160">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="98ef4-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="98ef4-161">System. String</span><span class="sxs-lookup"><span data-stu-id="98ef4-161">System.String</span></span>

### <span data-ttu-id="98ef4-162">System. null ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="98ef4-162">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="98ef4-163">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="98ef4-163">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

### <span data-ttu-id="98ef4-164">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="98ef4-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

### <span data-ttu-id="98ef4-165">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementServiceFabric</span><span class="sxs-lookup"><span data-stu-id="98ef4-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span></span>

### <span data-ttu-id="98ef4-166">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="98ef4-166">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="98ef4-167">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="98ef4-167">OUTPUTS</span></span>

### <span data-ttu-id="98ef4-168">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="98ef4-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="98ef4-169">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="98ef4-169">NOTES</span></span>

## <span data-ttu-id="98ef4-170">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="98ef4-170">RELATED LINKS</span></span>

[<span data-ttu-id="98ef4-171">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="98ef4-171">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend)

[<span data-ttu-id="98ef4-172">Új – AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="98ef4-172">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="98ef4-173">Új – AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="98ef4-173">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="98ef4-174">Új – AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="98ef4-174">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="98ef4-175">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="98ef4-175">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
