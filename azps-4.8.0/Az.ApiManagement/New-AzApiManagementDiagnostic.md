---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementDiagnostic.md
ms.openlocfilehash: f977b4dab003b3d1a1b83f1b81701a6089e1cefa
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024946"
---
# <span data-ttu-id="585fa-101">New-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="585fa-101">New-AzApiManagementDiagnostic</span></span>

## <span data-ttu-id="585fa-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="585fa-102">SYNOPSIS</span></span>
<span data-ttu-id="585fa-103">Új diagnosztikát hoz létre a globális hatókörben vagy az API-tartományban.</span><span class="sxs-lookup"><span data-stu-id="585fa-103">Creates a new diagnostics at the Global scope or Api Scope.</span></span>

## <span data-ttu-id="585fa-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="585fa-104">SYNTAX</span></span>

```
New-AzApiManagementDiagnostic -Context <PsApiManagementContext> -LoggerId <String> [-DiagnosticId <String>]
 [-AlwaysLog <String>] [-ApiId <String>] [-SamplingSetting <PsApiManagementSamplingSetting>]
 [-FrontEndSetting <PsApiManagementPipelineDiagnosticSetting>]
 [-BackendSetting <PsApiManagementPipelineDiagnosticSetting>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="585fa-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="585fa-105">DESCRIPTION</span></span>
<span data-ttu-id="585fa-106">A **New-AzApiManagementDiagnostic** parancsmag létrehoz egy diagnosztikai entitást globális hatókörben vagy adott API-hatókörben.</span><span class="sxs-lookup"><span data-stu-id="585fa-106">The cmdlet **New-AzApiManagementDiagnostic** creates a diagnostic entity either at Global scope or specific Api scope.</span></span>

## <span data-ttu-id="585fa-107">Példák</span><span class="sxs-lookup"><span data-stu-id="585fa-107">EXAMPLES</span></span>

### <span data-ttu-id="585fa-108">Példa 1: új globális hatókör-diagnosztika létrehozása</span><span class="sxs-lookup"><span data-stu-id="585fa-108">Example 1: Create a new Global scope Diagnostic</span></span>
```powershell
PS D:\github\azure-powershell> $context = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS D:\github\azure-powershell> $logger = Get-AzApiManagementLogger -Context $context -LoggerId "backendapisachinc"
PS D:\github\azure-powershell> $samplingsetting = New-AzApiManagementSamplingSetting -SamplingType fixed -SamplingPercentage 100
PS D:\github\azure-powershell> New-AzApiManagementDiagnostic -LoggerId $logger.LoggerId -Context $context -AlwaysLog allErrors -SamplingSetting $samplingSetting  -DiagnosticId "applicationinsights"

DiagnosticId                 : applicationinsights
ApiId                        :
AlwaysLog                    : allErrors
LoggerId                     : backendapisachinc
EnableHttpCorrelationHeaders : True
SamplingSetting              : Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting
FrontendSetting              :
BackendSetting               :
Id                           : /subscriptions/subid/resourceGroups/Api-Default-WestUs/providers/Microsoft.ApiManagement/service/contoso/diagnostics/applicationinsights
ResourceGroupName            : Api-Default-WestUs
ServiceName                  : contoso
```

<span data-ttu-id="585fa-109">Ebben a példában egy diagnosztikai entitást hoz létre globális hatókörben.</span><span class="sxs-lookup"><span data-stu-id="585fa-109">This example create a diagnostic entity at the Global Scope.</span></span>

### <span data-ttu-id="585fa-110">2. példa: diagnosztikai API-hatókör létrehozása</span><span class="sxs-lookup"><span data-stu-id="585fa-110">Example 2: Create a diagnostic at Api scope</span></span>
```powershell
PS D:\github\azure-powershell> $context = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS D:\github\azure-powershell> $logger = Get-AzApiManagementLogger -Context $context -LoggerId azuremonitor
PS D:\github\azure-powershell> $samplingsetting = New-AzApiManagementSamplingSetting -SamplingType fixed -SamplingPercentage 100
PS D:\github\azure-powershell> $httpMessageDiagnostic = New-AzApiManagementHttpMessageDiagnostic -HeadersToLog 'Content-Type', 'User-Agent' -BodyBytesToLog 100
PS D:\github\azure-powershell> $pipelineDiagnostic = New-AzApiManagementPipelineDiagnosticSetting -Request $httpMessageDiagnostic -Response $httpMessageDiagnostic
PS D:\github\azure-powershell> New-AzApiManagementDiagnostic -LoggerId $logger.LoggerId -Context $context -ApiId httpbin -AlwaysLog allErrors -SamplingSetting $samplingsetting -FrontEndSetting $pipelineDiagnostic -BackendSetting $pipelineDiagnostic -DiagnosticId azuremonitor

DiagnosticId                 : azuremonitor
ApiId                        : httpbin
AlwaysLog                    : allErrors
LoggerId                     : azuremonitor
EnableHttpCorrelationHeaders :
SamplingSetting              : Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting
FrontendSetting              : Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting
BackendSetting               : Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting
Id                           : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/apis/httpbin/diagnostics/azuremonitor      
ResourceGroupName            : Api-Default-WestUS
ServiceName                  : contoso
```

<span data-ttu-id="585fa-111">A fenti példa létrehoz egy diagnosztikai felületet az API `httpbin` -hoz, és naplózni az élőfejet és az 100 bájtot `azuremonitor` naplózó szervezetnek.</span><span class="sxs-lookup"><span data-stu-id="585fa-111">The example above create a diagnostic for the API `httpbin` to log the Header and 100 Bytes of Body to `azuremonitor` logger.</span></span>

## <span data-ttu-id="585fa-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="585fa-112">PARAMETERS</span></span>

### <span data-ttu-id="585fa-113">-AlwaysLog</span><span class="sxs-lookup"><span data-stu-id="585fa-113">-AlwaysLog</span></span>
<span data-ttu-id="585fa-114">Azt adja meg, hogy milyen típusú üzenetek mintavételi beállításai ne legyenek alkalmazhatók.</span><span class="sxs-lookup"><span data-stu-id="585fa-114">Specifies for what type of messages sampling settings should not apply.</span></span>
<span data-ttu-id="585fa-115">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="585fa-115">This parameter is optional.</span></span>

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

### <span data-ttu-id="585fa-116">-ApiId</span><span class="sxs-lookup"><span data-stu-id="585fa-116">-ApiId</span></span>
<span data-ttu-id="585fa-117">A meglévő API-azonosító.</span><span class="sxs-lookup"><span data-stu-id="585fa-117">Identifier of existing API.</span></span>
<span data-ttu-id="585fa-118">Ha meg van adva a program API-hatóköri házirend beállítása.</span><span class="sxs-lookup"><span data-stu-id="585fa-118">If specified will set API-scope policy.</span></span>
<span data-ttu-id="585fa-119">Ehhez a paraméterekre van szükség.</span><span class="sxs-lookup"><span data-stu-id="585fa-119">This parameters is required.</span></span>

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

### <span data-ttu-id="585fa-120">-BackendSetting</span><span class="sxs-lookup"><span data-stu-id="585fa-120">-BackendSetting</span></span>
<span data-ttu-id="585fa-121">Diagnosztikai beállítás a bejövő és kimenő http-üzenetekhez a Backendben.</span><span class="sxs-lookup"><span data-stu-id="585fa-121">Diagnostic setting for incoming/outgoing Http Messages to the Backend.</span></span> <span data-ttu-id="585fa-122">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="585fa-122">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="585fa-123">-Környezet</span><span class="sxs-lookup"><span data-stu-id="585fa-123">-Context</span></span>
<span data-ttu-id="585fa-124">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="585fa-124">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="585fa-125">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="585fa-125">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="585fa-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="585fa-126">-DefaultProfile</span></span>
<span data-ttu-id="585fa-127">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="585fa-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="585fa-128">-DiagnosticId</span><span class="sxs-lookup"><span data-stu-id="585fa-128">-DiagnosticId</span></span>
<span data-ttu-id="585fa-129">A diagnosztikai entitás azonosítója</span><span class="sxs-lookup"><span data-stu-id="585fa-129">Identifier of the diagnostics entity.</span></span>
<span data-ttu-id="585fa-130">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="585fa-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="585fa-131">-FrontEndSetting</span><span class="sxs-lookup"><span data-stu-id="585fa-131">-FrontEndSetting</span></span>
<span data-ttu-id="585fa-132">Diagnosztikai beállítás a bejövő és kimenő http-üzenetekhez az átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="585fa-132">Diagnostic setting for incoming/outgoing Http Messages to the Gateway.</span></span> <span data-ttu-id="585fa-133">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="585fa-133">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="585fa-134">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="585fa-134">-LoggerId</span></span>
<span data-ttu-id="585fa-135">Az adatnaplózó azonosítója, amellyel lenyomja a diagnosztikát.</span><span class="sxs-lookup"><span data-stu-id="585fa-135">Identifier of the logger to push diagnostics to.</span></span>
<span data-ttu-id="585fa-136">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="585fa-136">This parameter is required.</span></span>

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

### <span data-ttu-id="585fa-137">-SamplingSetting</span><span class="sxs-lookup"><span data-stu-id="585fa-137">-SamplingSetting</span></span>
<span data-ttu-id="585fa-138">A diagnosztikai környezet mintavételi beállításai</span><span class="sxs-lookup"><span data-stu-id="585fa-138">Sampling Setting of the Diagnostic.</span></span>
<span data-ttu-id="585fa-139">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="585fa-139">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="585fa-140">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="585fa-140">-Confirm</span></span>
<span data-ttu-id="585fa-141">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="585fa-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="585fa-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="585fa-142">-WhatIf</span></span>
<span data-ttu-id="585fa-143">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="585fa-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="585fa-144">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="585fa-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="585fa-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="585fa-145">CommonParameters</span></span>
<span data-ttu-id="585fa-146">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="585fa-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="585fa-147">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="585fa-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="585fa-148">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="585fa-148">INPUTS</span></span>

### <span data-ttu-id="585fa-149">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="585fa-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="585fa-150">System. String</span><span class="sxs-lookup"><span data-stu-id="585fa-150">System.String</span></span>

### <span data-ttu-id="585fa-151">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementSamplingSetting</span><span class="sxs-lookup"><span data-stu-id="585fa-151">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting</span></span>

### <span data-ttu-id="585fa-152">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementPipelineDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="585fa-152">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting</span></span>

## <span data-ttu-id="585fa-153">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="585fa-153">OUTPUTS</span></span>

### <span data-ttu-id="585fa-154">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="585fa-154">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span></span>

## <span data-ttu-id="585fa-155">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="585fa-155">NOTES</span></span>

## <span data-ttu-id="585fa-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="585fa-156">RELATED LINKS</span></span>

[<span data-ttu-id="585fa-157">Get-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="585fa-157">Get-AzApiManagementDiagnostic</span></span>](./Get-AzApiManagementDiagnostic.md)

[<span data-ttu-id="585fa-158">Remove-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="585fa-158">Remove-AzApiManagementDiagnostic</span></span>](./Remove-AzApiManagementDiagnostic.md)

[<span data-ttu-id="585fa-159">Set-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="585fa-159">Set-AzApiManagementDiagnostic</span></span>](./Set-AzApiManagementDiagnostic.md)

[<span data-ttu-id="585fa-160">Új – AzApiManagementHttpMessageDiagnostic</span><span class="sxs-lookup"><span data-stu-id="585fa-160">New-AzApiManagementHttpMessageDiagnostic</span></span>](./New-AzApiManagementHttpMessageDiagnostic.md)

[<span data-ttu-id="585fa-161">Új – AzApiManagementSamplingSetting</span><span class="sxs-lookup"><span data-stu-id="585fa-161">New-AzApiManagementSamplingSetting</span></span>](./New-AzApiManagementHttpMessageDiagnostic.md)