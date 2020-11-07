---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementBackend.md
ms.openlocfilehash: 85545777f5a76f3f75e81648a009ffcdcad8ab30
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679989"
---
# <span data-ttu-id="9c336-101">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="9c336-101">Set-AzureRmApiManagementBackend</span></span>

## <span data-ttu-id="9c336-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9c336-102">SYNOPSIS</span></span>
<span data-ttu-id="9c336-103">A backend frissítése</span><span class="sxs-lookup"><span data-stu-id="9c336-103">Updates a Backend.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9c336-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9c336-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-Protocol <String>]
 [-Url <String>] [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9c336-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9c336-105">DESCRIPTION</span></span>
<span data-ttu-id="9c336-106">Egy meglévő backend frissítése az API-kezelésben.</span><span class="sxs-lookup"><span data-stu-id="9c336-106">Updates an existing backend in the Api Management.</span></span>

## <span data-ttu-id="9c336-107">Példák</span><span class="sxs-lookup"><span data-stu-id="9c336-107">EXAMPLES</span></span>

### <span data-ttu-id="9c336-108">A backend 123 leírásának frissítése</span><span class="sxs-lookup"><span data-stu-id="9c336-108">Updates the Description of the Backend 123</span></span>
```
Set-AzureRmApiManagementBackend -Context $apimContext -BackendId 123 -Description "updated description" -PassThru
```

## <span data-ttu-id="9c336-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9c336-109">PARAMETERS</span></span>

### <span data-ttu-id="9c336-110">-BackendId</span><span class="sxs-lookup"><span data-stu-id="9c336-110">-BackendId</span></span>
<span data-ttu-id="9c336-111">Új backend-azonosító.</span><span class="sxs-lookup"><span data-stu-id="9c336-111">Identifier of new backend.</span></span>
<span data-ttu-id="9c336-112">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="9c336-112">This parameter is required.</span></span>

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

### <span data-ttu-id="9c336-113">-Környezet</span><span class="sxs-lookup"><span data-stu-id="9c336-113">-Context</span></span>
<span data-ttu-id="9c336-114">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="9c336-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="9c336-115">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="9c336-115">This parameter is required.</span></span>

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

### <span data-ttu-id="9c336-116">-Hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="9c336-116">-Credential</span></span>
<span data-ttu-id="9c336-117">Hitelesítő adatok, amelyeket a háttérben való beszélgetés során használni kell.</span><span class="sxs-lookup"><span data-stu-id="9c336-117">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="9c336-118">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="9c336-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="9c336-119">-Leírás</span><span class="sxs-lookup"><span data-stu-id="9c336-119">-Description</span></span>
<span data-ttu-id="9c336-120">A backend leírása.</span><span class="sxs-lookup"><span data-stu-id="9c336-120">Backend Description.</span></span>
<span data-ttu-id="9c336-121">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="9c336-121">This parameter is optional.</span></span>

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

### <span data-ttu-id="9c336-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9c336-122">-PassThru</span></span>
<span data-ttu-id="9c336-123">Jelzi, hogy ez a parancsmag a parancsmag által módosított  **PsApiManagementBackend** adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="9c336-123">Indicates that this cmdlet returns the  **PsApiManagementBackend** that this cmdlet modifies.</span></span>


```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c336-124">-Protocol</span><span class="sxs-lookup"><span data-stu-id="9c336-124">-Protocol</span></span>
<span data-ttu-id="9c336-125">Backend kommunikációs protokoll (http vagy SOAP).</span><span class="sxs-lookup"><span data-stu-id="9c336-125">Backend Communication protocol (http or soap).</span></span>
<span data-ttu-id="9c336-126">Ez a paraméter nem kötelező</span><span class="sxs-lookup"><span data-stu-id="9c336-126">This parameter is optional</span></span>

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

### <span data-ttu-id="9c336-127">-Proxy</span><span class="sxs-lookup"><span data-stu-id="9c336-127">-Proxy</span></span>
<span data-ttu-id="9c336-128">A munkaablakba való küldéskor használandó proxykiszolgáló-adatok.</span><span class="sxs-lookup"><span data-stu-id="9c336-128">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="9c336-129">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="9c336-129">This parameter is optional.</span></span>

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

### <span data-ttu-id="9c336-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9c336-130">-ResourceId</span></span>
<span data-ttu-id="9c336-131">Az erőforrás felügyeleti URI-ja külső rendszerben</span><span class="sxs-lookup"><span data-stu-id="9c336-131">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="9c336-132">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="9c336-132">This parameter is optional.</span></span>
<span data-ttu-id="9c336-133">Ez az URL-cím lehet a logikai alkalmazások, a függvények és az API-alkalmazások ARM erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="9c336-133">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

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

### <span data-ttu-id="9c336-134">-SkipCertificateChainValidation</span><span class="sxs-lookup"><span data-stu-id="9c336-134">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="9c336-135">Szeretné-e kihagyni a tanúsítványláncot az érvényesítést, ha a háttérrel beszél.</span><span class="sxs-lookup"><span data-stu-id="9c336-135">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="9c336-136">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="9c336-136">This parameter is optional.</span></span>

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

### <span data-ttu-id="9c336-137">-SkipCertificateNameValidation</span><span class="sxs-lookup"><span data-stu-id="9c336-137">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="9c336-138">Szeretné-e kihagyni a tanúsítvány nevének érvényesítését, amikor a háttérben beszél.</span><span class="sxs-lookup"><span data-stu-id="9c336-138">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="9c336-139">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="9c336-139">This parameter is optional.</span></span>

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

### <span data-ttu-id="9c336-140">-Cím</span><span class="sxs-lookup"><span data-stu-id="9c336-140">-Title</span></span>
<span data-ttu-id="9c336-141">A backend címe.</span><span class="sxs-lookup"><span data-stu-id="9c336-141">Backend Title.</span></span>
<span data-ttu-id="9c336-142">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="9c336-142">This parameter is optional.</span></span>

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

### <span data-ttu-id="9c336-143">-URL</span><span class="sxs-lookup"><span data-stu-id="9c336-143">-Url</span></span>
<span data-ttu-id="9c336-144">A backend futásidejű URL-címe.</span><span class="sxs-lookup"><span data-stu-id="9c336-144">Runtime Url for the Backend.</span></span>
<span data-ttu-id="9c336-145">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="9c336-145">This parameter is optional.</span></span>

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

### <span data-ttu-id="9c336-146">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9c336-146">-Confirm</span></span>
<span data-ttu-id="9c336-147">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9c336-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c336-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c336-148">-WhatIf</span></span>
<span data-ttu-id="9c336-149">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9c336-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9c336-150">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9c336-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c336-151">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c336-151">-DefaultProfile</span></span>
<span data-ttu-id="9c336-152">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9c336-152">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9c336-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c336-153">CommonParameters</span></span>
<span data-ttu-id="9c336-154">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9c336-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c336-155">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c336-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c336-156">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9c336-156">INPUTS</span></span>

## <span data-ttu-id="9c336-157">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9c336-157">OUTPUTS</span></span>

### <span data-ttu-id="9c336-158">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="9c336-158">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="9c336-159">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9c336-159">NOTES</span></span>

## <span data-ttu-id="9c336-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9c336-160">RELATED LINKS</span></span>

[<span data-ttu-id="9c336-161">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="9c336-161">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="9c336-162">Új – AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="9c336-162">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="9c336-163">Új – AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="9c336-163">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="9c336-164">Új – AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="9c336-164">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="9c336-165">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="9c336-165">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)
