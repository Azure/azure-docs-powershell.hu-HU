---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementBackend.md
ms.openlocfilehash: 52e159ae0f9d1b94b316394ddefe04f0bd8aa1c8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492063"
---
# <span data-ttu-id="693df-101">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="693df-101">Set-AzureRmApiManagementBackend</span></span>

## <span data-ttu-id="693df-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="693df-102">SYNOPSIS</span></span>
<span data-ttu-id="693df-103">A backend frissítése</span><span class="sxs-lookup"><span data-stu-id="693df-103">Updates a Backend.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="693df-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="693df-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-Protocol <String>]
 [-Url <String>] [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>]
 [-ServiceFabricCluster <PsApiManagementServiceFabric>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="693df-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="693df-105">DESCRIPTION</span></span>
<span data-ttu-id="693df-106">Egy meglévő backend frissítése az API-kezelésben.</span><span class="sxs-lookup"><span data-stu-id="693df-106">Updates an existing backend in the Api Management.</span></span>

## <span data-ttu-id="693df-107">Példák</span><span class="sxs-lookup"><span data-stu-id="693df-107">EXAMPLES</span></span>

### <span data-ttu-id="693df-108">A backend 123 leírásának frissítése</span><span class="sxs-lookup"><span data-stu-id="693df-108">Updates the Description of the Backend 123</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementBackend -Context $apimContext -BackendId 123 -Description "updated description" -PassThru
```

## <span data-ttu-id="693df-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="693df-109">PARAMETERS</span></span>

### <span data-ttu-id="693df-110">-BackendId</span><span class="sxs-lookup"><span data-stu-id="693df-110">-BackendId</span></span>
<span data-ttu-id="693df-111">Új backend-azonosító.</span><span class="sxs-lookup"><span data-stu-id="693df-111">Identifier of new backend.</span></span>
<span data-ttu-id="693df-112">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="693df-112">This parameter is required.</span></span>

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

### <span data-ttu-id="693df-113">-Környezet</span><span class="sxs-lookup"><span data-stu-id="693df-113">-Context</span></span>
<span data-ttu-id="693df-114">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="693df-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="693df-115">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="693df-115">This parameter is required.</span></span>

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

### <span data-ttu-id="693df-116">-Hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="693df-116">-Credential</span></span>
<span data-ttu-id="693df-117">Hitelesítő adatok, amelyeket a háttérben való beszélgetés során használni kell.</span><span class="sxs-lookup"><span data-stu-id="693df-117">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="693df-118">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="693df-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="693df-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="693df-119">-DefaultProfile</span></span>
<span data-ttu-id="693df-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="693df-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="693df-121">-Leírás</span><span class="sxs-lookup"><span data-stu-id="693df-121">-Description</span></span>
<span data-ttu-id="693df-122">A backend leírása.</span><span class="sxs-lookup"><span data-stu-id="693df-122">Backend Description.</span></span>
<span data-ttu-id="693df-123">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="693df-123">This parameter is optional.</span></span>

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

### <span data-ttu-id="693df-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="693df-124">-PassThru</span></span>
<span data-ttu-id="693df-125">Jelzi, hogy ez a parancsmag a parancsmag által módosított  **PsApiManagementBackend** adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="693df-125">Indicates that this cmdlet returns the  **PsApiManagementBackend** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="693df-126">-Protocol</span><span class="sxs-lookup"><span data-stu-id="693df-126">-Protocol</span></span>
<span data-ttu-id="693df-127">Backend kommunikációs protokoll (http vagy SOAP).</span><span class="sxs-lookup"><span data-stu-id="693df-127">Backend Communication protocol (http or soap).</span></span>
<span data-ttu-id="693df-128">Ez a paraméter nem kötelező</span><span class="sxs-lookup"><span data-stu-id="693df-128">This parameter is optional</span></span>

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

### <span data-ttu-id="693df-129">-Proxy</span><span class="sxs-lookup"><span data-stu-id="693df-129">-Proxy</span></span>
<span data-ttu-id="693df-130">A munkaablakba való küldéskor használandó proxykiszolgáló-adatok.</span><span class="sxs-lookup"><span data-stu-id="693df-130">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="693df-131">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="693df-131">This parameter is optional.</span></span>

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

### <span data-ttu-id="693df-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="693df-132">-ResourceId</span></span>
<span data-ttu-id="693df-133">Az erőforrás felügyeleti URI-ja külső rendszerben</span><span class="sxs-lookup"><span data-stu-id="693df-133">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="693df-134">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="693df-134">This parameter is optional.</span></span>
<span data-ttu-id="693df-135">Ez az URL-cím lehet a logikai alkalmazások, a függvények és az API-alkalmazások ARM erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="693df-135">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

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

### <span data-ttu-id="693df-136">-ServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="693df-136">-ServiceFabricCluster</span></span>
<span data-ttu-id="693df-137">A Service Fabric cluster backend részletei.</span><span class="sxs-lookup"><span data-stu-id="693df-137">Service Fabric Cluster Backend details.</span></span> <span data-ttu-id="693df-138">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="693df-138">This parameter is optional.</span></span>

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

### <span data-ttu-id="693df-139">-SkipCertificateChainValidation</span><span class="sxs-lookup"><span data-stu-id="693df-139">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="693df-140">Szeretné-e kihagyni a tanúsítványláncot az érvényesítést, ha a háttérrel beszél.</span><span class="sxs-lookup"><span data-stu-id="693df-140">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="693df-141">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="693df-141">This parameter is optional.</span></span>

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

### <span data-ttu-id="693df-142">-SkipCertificateNameValidation</span><span class="sxs-lookup"><span data-stu-id="693df-142">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="693df-143">Szeretné-e kihagyni a tanúsítvány nevének érvényesítését, amikor a háttérben beszél.</span><span class="sxs-lookup"><span data-stu-id="693df-143">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="693df-144">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="693df-144">This parameter is optional.</span></span>

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

### <span data-ttu-id="693df-145">-Cím</span><span class="sxs-lookup"><span data-stu-id="693df-145">-Title</span></span>
<span data-ttu-id="693df-146">A backend címe.</span><span class="sxs-lookup"><span data-stu-id="693df-146">Backend Title.</span></span>
<span data-ttu-id="693df-147">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="693df-147">This parameter is optional.</span></span>

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

### <span data-ttu-id="693df-148">-URL</span><span class="sxs-lookup"><span data-stu-id="693df-148">-Url</span></span>
<span data-ttu-id="693df-149">A backend futásidejű URL-címe.</span><span class="sxs-lookup"><span data-stu-id="693df-149">Runtime Url for the Backend.</span></span>
<span data-ttu-id="693df-150">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="693df-150">This parameter is optional.</span></span>

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

### <span data-ttu-id="693df-151">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="693df-151">-Confirm</span></span>
<span data-ttu-id="693df-152">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="693df-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="693df-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="693df-153">-WhatIf</span></span>
<span data-ttu-id="693df-154">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="693df-154">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="693df-155">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="693df-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="693df-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="693df-156">CommonParameters</span></span>
<span data-ttu-id="693df-157">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="693df-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="693df-158">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="693df-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="693df-159">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="693df-159">INPUTS</span></span>

### <span data-ttu-id="693df-160">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="693df-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="693df-161">System. String</span><span class="sxs-lookup"><span data-stu-id="693df-161">System.String</span></span>

### <span data-ttu-id="693df-162">System. null ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="693df-162">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="693df-163">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="693df-163">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

### <span data-ttu-id="693df-164">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="693df-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

### <span data-ttu-id="693df-165">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementServiceFabric</span><span class="sxs-lookup"><span data-stu-id="693df-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span></span>

### <span data-ttu-id="693df-166">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="693df-166">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="693df-167">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="693df-167">OUTPUTS</span></span>

### <span data-ttu-id="693df-168">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="693df-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="693df-169">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="693df-169">NOTES</span></span>

## <span data-ttu-id="693df-170">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="693df-170">RELATED LINKS</span></span>

[<span data-ttu-id="693df-171">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="693df-171">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="693df-172">Új – AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="693df-172">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="693df-173">Új – AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="693df-173">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="693df-174">Új – AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="693df-174">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="693df-175">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="693df-175">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)
