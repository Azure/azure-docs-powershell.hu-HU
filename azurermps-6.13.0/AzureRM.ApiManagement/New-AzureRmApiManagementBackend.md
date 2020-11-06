---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackend.md
ms.openlocfilehash: 46e0a864bcedd8ac0c23761545f5480eaa4a093a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494221"
---
# <span data-ttu-id="ea419-101">New-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="ea419-101">New-AzureRmApiManagementBackend</span></span>

## <span data-ttu-id="ea419-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ea419-102">SYNOPSIS</span></span>
<span data-ttu-id="ea419-103">Új backend-egyedet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="ea419-103">Creates a new backend entity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ea419-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ea419-104">SYNTAX</span></span>

```
New-AzureRmApiManagementBackend -Context <PsApiManagementContext> [-BackendId <String>] -Protocol <String>
 -Url <String> [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>]
 [-ServiceFabricCluster <PsApiManagementServiceFabric>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea419-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ea419-105">DESCRIPTION</span></span>
<span data-ttu-id="ea419-106">Új backend-entitás létrehozása az API-kezelésben.</span><span class="sxs-lookup"><span data-stu-id="ea419-106">Creates a new backend entity in Api Management.</span></span>

## <span data-ttu-id="ea419-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ea419-107">EXAMPLES</span></span>

### <span data-ttu-id="ea419-108">A backend 123 létrehozása alapvető engedélyezési rendszerrel</span><span class="sxs-lookup"><span data-stu-id="ea419-108">Create Backend 123 with a Basic Authorization Scheme</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$credential = New-AzureRmApiManagementBackendCredential -AuthorizationHeaderScheme basic -AuthorizationHeaderParameter opensesame -Query @{"sv" = @('xx', 'bb'); "sr" = @('cc')} -Header @{"x-my-1" = @('val1', 'val2')}

PS C:\>$backend = New-AzureRmApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Credential $credential -Description "my backend"
```

<span data-ttu-id="ea419-109">Új backend létrehozása</span><span class="sxs-lookup"><span data-stu-id="ea419-109">Creates a new Backend</span></span>

## <span data-ttu-id="ea419-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ea419-110">PARAMETERS</span></span>

### <span data-ttu-id="ea419-111">-BackendId</span><span class="sxs-lookup"><span data-stu-id="ea419-111">-BackendId</span></span>
<span data-ttu-id="ea419-112">Új backend-azonosító.</span><span class="sxs-lookup"><span data-stu-id="ea419-112">Identifier of new backend.</span></span>
<span data-ttu-id="ea419-113">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="ea419-113">This parameter is optional.</span></span>
<span data-ttu-id="ea419-114">Ha a program nem adja meg a megadott értéket.</span><span class="sxs-lookup"><span data-stu-id="ea419-114">If not specified will be generated.</span></span>

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

### <span data-ttu-id="ea419-115">-Környezet</span><span class="sxs-lookup"><span data-stu-id="ea419-115">-Context</span></span>
<span data-ttu-id="ea419-116">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="ea419-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="ea419-117">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="ea419-117">This parameter is required.</span></span>

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

### <span data-ttu-id="ea419-118">-Hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="ea419-118">-Credential</span></span>
<span data-ttu-id="ea419-119">Hitelesítő adatok, amelyeket a háttérben való beszélgetés során használni kell.</span><span class="sxs-lookup"><span data-stu-id="ea419-119">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="ea419-120">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="ea419-120">This parameter is optional.</span></span>

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

### <span data-ttu-id="ea419-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea419-121">-DefaultProfile</span></span>
<span data-ttu-id="ea419-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ea419-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ea419-123">-Leírás</span><span class="sxs-lookup"><span data-stu-id="ea419-123">-Description</span></span>
<span data-ttu-id="ea419-124">A backend leírása.</span><span class="sxs-lookup"><span data-stu-id="ea419-124">Backend Description.</span></span>
<span data-ttu-id="ea419-125">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="ea419-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="ea419-126">-Protocol</span><span class="sxs-lookup"><span data-stu-id="ea419-126">-Protocol</span></span>
<span data-ttu-id="ea419-127">A backend kommunikációs protokollja.</span><span class="sxs-lookup"><span data-stu-id="ea419-127">Backend Communication protocol.</span></span>
<span data-ttu-id="ea419-128">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="ea419-128">This parameter is required.</span></span>
<span data-ttu-id="ea419-129">Az érvényes értékek a "http" és a "SOAP".</span><span class="sxs-lookup"><span data-stu-id="ea419-129">Valid values are 'http' and 'soap'.</span></span>

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

### <span data-ttu-id="ea419-130">-Proxy</span><span class="sxs-lookup"><span data-stu-id="ea419-130">-Proxy</span></span>
<span data-ttu-id="ea419-131">A munkaablakba való küldéskor használandó proxykiszolgáló-adatok.</span><span class="sxs-lookup"><span data-stu-id="ea419-131">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="ea419-132">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="ea419-132">This parameter is optional.</span></span>

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

### <span data-ttu-id="ea419-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ea419-133">-ResourceId</span></span>
<span data-ttu-id="ea419-134">Az erőforrás felügyeleti URI-ja külső rendszerben</span><span class="sxs-lookup"><span data-stu-id="ea419-134">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="ea419-135">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="ea419-135">This parameter is optional.</span></span>
<span data-ttu-id="ea419-136">Ez az URL-cím lehet a logikai alkalmazások, a függvények és az API-alkalmazások ARM erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="ea419-136">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

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

### <span data-ttu-id="ea419-137">-ServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="ea419-137">-ServiceFabricCluster</span></span>
<span data-ttu-id="ea419-138">A Service Fabric cluster backend részletei.</span><span class="sxs-lookup"><span data-stu-id="ea419-138">Service Fabric Cluster Backend details.</span></span> <span data-ttu-id="ea419-139">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="ea419-139">This parameter is optional.</span></span>

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

### <span data-ttu-id="ea419-140">-SkipCertificateChainValidation</span><span class="sxs-lookup"><span data-stu-id="ea419-140">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="ea419-141">Szeretné-e kihagyni a tanúsítványláncot az érvényesítést, ha a háttérrel beszél.</span><span class="sxs-lookup"><span data-stu-id="ea419-141">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="ea419-142">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="ea419-142">This parameter is optional.</span></span>

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

### <span data-ttu-id="ea419-143">-SkipCertificateNameValidation</span><span class="sxs-lookup"><span data-stu-id="ea419-143">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="ea419-144">Szeretné-e kihagyni a tanúsítvány nevének érvényesítését, amikor a háttérben beszél.</span><span class="sxs-lookup"><span data-stu-id="ea419-144">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="ea419-145">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="ea419-145">This parameter is optional.</span></span>

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

### <span data-ttu-id="ea419-146">-Cím</span><span class="sxs-lookup"><span data-stu-id="ea419-146">-Title</span></span>
<span data-ttu-id="ea419-147">A backend címe.</span><span class="sxs-lookup"><span data-stu-id="ea419-147">Backend Title.</span></span>
<span data-ttu-id="ea419-148">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="ea419-148">This parameter is optional.</span></span>

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

### <span data-ttu-id="ea419-149">-URL</span><span class="sxs-lookup"><span data-stu-id="ea419-149">-Url</span></span>
<span data-ttu-id="ea419-150">A backend futásidejű URL-címe.</span><span class="sxs-lookup"><span data-stu-id="ea419-150">Runtime Url for the Backend.</span></span>
<span data-ttu-id="ea419-151">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="ea419-151">This parameter is required.</span></span>

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

### <span data-ttu-id="ea419-152">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ea419-152">-Confirm</span></span>
<span data-ttu-id="ea419-153">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ea419-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea419-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea419-154">-WhatIf</span></span>
<span data-ttu-id="ea419-155">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ea419-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ea419-156">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ea419-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea419-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea419-157">CommonParameters</span></span>
<span data-ttu-id="ea419-158">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ea419-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea419-159">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea419-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea419-160">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ea419-160">INPUTS</span></span>

### <span data-ttu-id="ea419-161">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="ea419-161">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="ea419-162">System. String</span><span class="sxs-lookup"><span data-stu-id="ea419-162">System.String</span></span>

### <span data-ttu-id="ea419-163">System. null ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="ea419-163">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="ea419-164">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="ea419-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

### <span data-ttu-id="ea419-165">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="ea419-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

### <span data-ttu-id="ea419-166">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ea419-166">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span></span>

## <span data-ttu-id="ea419-167">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ea419-167">OUTPUTS</span></span>

### <span data-ttu-id="ea419-168">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="ea419-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="ea419-169">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ea419-169">NOTES</span></span>

## <span data-ttu-id="ea419-170">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ea419-170">RELATED LINKS</span></span>

[<span data-ttu-id="ea419-171">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="ea419-171">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="ea419-172">Új – AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="ea419-172">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="ea419-173">Új – AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="ea419-173">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="ea419-174">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="ea419-174">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)

[<span data-ttu-id="ea419-175">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="ea419-175">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)

