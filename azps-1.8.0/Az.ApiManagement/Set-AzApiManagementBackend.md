---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementBackend.md
ms.openlocfilehash: 0ac89ed099029fbbabe90e07da7ba9c204449db9
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100400739"
---
# <span data-ttu-id="4a1df-101">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="4a1df-101">Set-AzApiManagementBackend</span></span>

## <span data-ttu-id="4a1df-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4a1df-102">SYNOPSIS</span></span>
<span data-ttu-id="4a1df-103">Frissíti a backend-et.</span><span class="sxs-lookup"><span data-stu-id="4a1df-103">Updates a Backend.</span></span>

## <span data-ttu-id="4a1df-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="4a1df-104">SYNTAX</span></span>

```
Set-AzApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-Protocol <String>]
 [-Url <String>] [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>]
 [-ServiceFabricCluster <PsApiManagementServiceFabric>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4a1df-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="4a1df-105">DESCRIPTION</span></span>
<span data-ttu-id="4a1df-106">Frissíti a meglévő háttért az Api-kezelésben.</span><span class="sxs-lookup"><span data-stu-id="4a1df-106">Updates an existing backend in the Api Management.</span></span>

## <span data-ttu-id="4a1df-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="4a1df-107">EXAMPLES</span></span>

### <span data-ttu-id="4a1df-108">A Backend 123 leírásának frissítése</span><span class="sxs-lookup"><span data-stu-id="4a1df-108">Updates the Description of the Backend 123</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementBackend -Context $apimContext -BackendId 123 -Description "updated description" -PassThru
```

## <span data-ttu-id="4a1df-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4a1df-109">PARAMETERS</span></span>

### <span data-ttu-id="4a1df-110">-BackendId</span><span class="sxs-lookup"><span data-stu-id="4a1df-110">-BackendId</span></span>
<span data-ttu-id="4a1df-111">Az új háttér-háttér azonosítója.</span><span class="sxs-lookup"><span data-stu-id="4a1df-111">Identifier of new backend.</span></span>
<span data-ttu-id="4a1df-112">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="4a1df-112">This parameter is required.</span></span>

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

### <span data-ttu-id="4a1df-113">-Környezet</span><span class="sxs-lookup"><span data-stu-id="4a1df-113">-Context</span></span>
<span data-ttu-id="4a1df-114">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="4a1df-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="4a1df-115">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="4a1df-115">This parameter is required.</span></span>

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

### <span data-ttu-id="4a1df-116">-Hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="4a1df-116">-Credential</span></span>
<span data-ttu-id="4a1df-117">A háttéradatokkal való beszélgetéshez használt hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="4a1df-117">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="4a1df-118">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="4a1df-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="4a1df-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a1df-119">-DefaultProfile</span></span>
<span data-ttu-id="4a1df-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4a1df-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4a1df-121">-Leírás</span><span class="sxs-lookup"><span data-stu-id="4a1df-121">-Description</span></span>
<span data-ttu-id="4a1df-122">Háttér leírása.</span><span class="sxs-lookup"><span data-stu-id="4a1df-122">Backend Description.</span></span>
<span data-ttu-id="4a1df-123">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="4a1df-123">This parameter is optional.</span></span>

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

### <span data-ttu-id="4a1df-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4a1df-124">-PassThru</span></span>
<span data-ttu-id="4a1df-125">Azt jelzi, hogy ez a parancsmag a  **PsApiManagementBackend** értéket adja vissza, amely módosítja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="4a1df-125">Indicates that this cmdlet returns the  **PsApiManagementBackend** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="4a1df-126">-Protocol</span><span class="sxs-lookup"><span data-stu-id="4a1df-126">-Protocol</span></span>
<span data-ttu-id="4a1df-127">Backend Communication protocol (http vagy soap).</span><span class="sxs-lookup"><span data-stu-id="4a1df-127">Backend Communication protocol (http or soap).</span></span>
<span data-ttu-id="4a1df-128">Ez a paraméter nem kötelező</span><span class="sxs-lookup"><span data-stu-id="4a1df-128">This parameter is optional</span></span>

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

### <span data-ttu-id="4a1df-129">-Proxy</span><span class="sxs-lookup"><span data-stu-id="4a1df-129">-Proxy</span></span>
<span data-ttu-id="4a1df-130">A proxykiszolgáló adatai, amelyek a kérés backendbe való elküldése közben használatosak.</span><span class="sxs-lookup"><span data-stu-id="4a1df-130">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="4a1df-131">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="4a1df-131">This parameter is optional.</span></span>

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

### <span data-ttu-id="4a1df-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4a1df-132">-ResourceId</span></span>
<span data-ttu-id="4a1df-133">Az erőforrás felügyeleti uri-ja a külső rendszerben.</span><span class="sxs-lookup"><span data-stu-id="4a1df-133">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="4a1df-134">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="4a1df-134">This parameter is optional.</span></span>
<span data-ttu-id="4a1df-135">Ez az URL-cím lehet a logic appok, függvényalkalmazások vagy API-appok Arm Resource Id azonosítója.</span><span class="sxs-lookup"><span data-stu-id="4a1df-135">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

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

### <span data-ttu-id="4a1df-136">-ServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="4a1df-136">-ServiceFabricCluster</span></span>
<span data-ttu-id="4a1df-137">Service Fabric Cluster Backend details.</span><span class="sxs-lookup"><span data-stu-id="4a1df-137">Service Fabric Cluster Backend details.</span></span> <span data-ttu-id="4a1df-138">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="4a1df-138">This parameter is optional.</span></span>

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

### <span data-ttu-id="4a1df-139">-SkipCertificateChainValidation</span><span class="sxs-lookup"><span data-stu-id="4a1df-139">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="4a1df-140">Hogy kihagyja-e a tanúsítványlánc-ellenőrzést, amikor a backend-hez beszél.</span><span class="sxs-lookup"><span data-stu-id="4a1df-140">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="4a1df-141">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="4a1df-141">This parameter is optional.</span></span>

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

### <span data-ttu-id="4a1df-142">-SkipCertificateNameValidation</span><span class="sxs-lookup"><span data-stu-id="4a1df-142">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="4a1df-143">Kihagyhatja-e a Tanúsítványnév érvényesítése érvénybe lépését a backend-hez való beszélgetés során.</span><span class="sxs-lookup"><span data-stu-id="4a1df-143">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="4a1df-144">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="4a1df-144">This parameter is optional.</span></span>

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

### <span data-ttu-id="4a1df-145">-Title</span><span class="sxs-lookup"><span data-stu-id="4a1df-145">-Title</span></span>
<span data-ttu-id="4a1df-146">Háttércím.</span><span class="sxs-lookup"><span data-stu-id="4a1df-146">Backend Title.</span></span>
<span data-ttu-id="4a1df-147">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="4a1df-147">This parameter is optional.</span></span>

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

### <span data-ttu-id="4a1df-148">-Url</span><span class="sxs-lookup"><span data-stu-id="4a1df-148">-Url</span></span>
<span data-ttu-id="4a1df-149">A Backend futásidejű URL-címe.</span><span class="sxs-lookup"><span data-stu-id="4a1df-149">Runtime Url for the Backend.</span></span>
<span data-ttu-id="4a1df-150">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="4a1df-150">This parameter is optional.</span></span>

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

### <span data-ttu-id="4a1df-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4a1df-151">-Confirm</span></span>
<span data-ttu-id="4a1df-152">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="4a1df-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a1df-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a1df-153">-WhatIf</span></span>
<span data-ttu-id="4a1df-154">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="4a1df-154">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4a1df-155">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4a1df-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a1df-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a1df-156">CommonParameters</span></span>
<span data-ttu-id="4a1df-157">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a1df-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a1df-158">További információt a about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a1df-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a1df-159">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4a1df-159">INPUTS</span></span>

### <span data-ttu-id="4a1df-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="4a1df-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="4a1df-161">System.String</span><span class="sxs-lookup"><span data-stu-id="4a1df-161">System.String</span></span>

### <span data-ttu-id="4a1df-162">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="4a1df-162">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="4a1df-163">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="4a1df-163">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

### <span data-ttu-id="4a1df-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="4a1df-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

### <span data-ttu-id="4a1df-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span><span class="sxs-lookup"><span data-stu-id="4a1df-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span></span>

### <span data-ttu-id="4a1df-166">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="4a1df-166">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="4a1df-167">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4a1df-167">OUTPUTS</span></span>

### <span data-ttu-id="4a1df-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="4a1df-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="4a1df-169">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="4a1df-169">NOTES</span></span>

## <span data-ttu-id="4a1df-170">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4a1df-170">RELATED LINKS</span></span>

[<span data-ttu-id="4a1df-171">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="4a1df-171">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend.md)

[<span data-ttu-id="4a1df-172">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="4a1df-172">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="4a1df-173">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="4a1df-173">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="4a1df-174">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="4a1df-174">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="4a1df-175">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="4a1df-175">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
