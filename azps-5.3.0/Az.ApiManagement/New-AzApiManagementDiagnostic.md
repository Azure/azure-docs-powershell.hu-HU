---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementDiagnostic.md
ms.openlocfilehash: f977b4dab003b3d1a1b83f1b81701a6089e1cefa
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98478817"
---
# <span data-ttu-id="5af33-101">New-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="5af33-101">New-AzApiManagementDiagnostic</span></span>

## <span data-ttu-id="5af33-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5af33-102">SYNOPSIS</span></span>
<span data-ttu-id="5af33-103">Új diagnosztika létrehozása globális vagy Api-hatókörben.</span><span class="sxs-lookup"><span data-stu-id="5af33-103">Creates a new diagnostics at the Global scope or Api Scope.</span></span>

## <span data-ttu-id="5af33-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5af33-104">SYNTAX</span></span>

```
New-AzApiManagementDiagnostic -Context <PsApiManagementContext> -LoggerId <String> [-DiagnosticId <String>]
 [-AlwaysLog <String>] [-ApiId <String>] [-SamplingSetting <PsApiManagementSamplingSetting>]
 [-FrontEndSetting <PsApiManagementPipelineDiagnosticSetting>]
 [-BackendSetting <PsApiManagementPipelineDiagnosticSetting>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5af33-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5af33-105">DESCRIPTION</span></span>
<span data-ttu-id="5af33-106">A **New-AzApiManagementDiagnostic** parancsmag létrehoz egy diagnosztikai entitást globális vagy adott Api-hatókörben.</span><span class="sxs-lookup"><span data-stu-id="5af33-106">The cmdlet **New-AzApiManagementDiagnostic** creates a diagnostic entity either at Global scope or specific Api scope.</span></span>

## <span data-ttu-id="5af33-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5af33-107">EXAMPLES</span></span>

### <span data-ttu-id="5af33-108">1. példa: Új globális hatókörű diagnosztikai eszköz létrehozása</span><span class="sxs-lookup"><span data-stu-id="5af33-108">Example 1: Create a new Global scope Diagnostic</span></span>
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

<span data-ttu-id="5af33-109">Ez a példa egy diagnosztikai entitást hoz létre a globális hatókörben.</span><span class="sxs-lookup"><span data-stu-id="5af33-109">This example create a diagnostic entity at the Global Scope.</span></span>

### <span data-ttu-id="5af33-110">2. példa: Diagnosztikai eszköz létrehozása az Api hatókörében</span><span class="sxs-lookup"><span data-stu-id="5af33-110">Example 2: Create a diagnostic at Api scope</span></span>
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

<span data-ttu-id="5af33-111">A fenti példa létrehoz egy diagnosztikát az API számára a fejléc és `httpbin` a 100 bájtos törzs `azuremonitor` naplózásához.</span><span class="sxs-lookup"><span data-stu-id="5af33-111">The example above create a diagnostic for the API `httpbin` to log the Header and 100 Bytes of Body to `azuremonitor` logger.</span></span>

## <span data-ttu-id="5af33-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5af33-112">PARAMETERS</span></span>

### <span data-ttu-id="5af33-113">-AlwaysLog</span><span class="sxs-lookup"><span data-stu-id="5af33-113">-AlwaysLog</span></span>
<span data-ttu-id="5af33-114">Meghatározza, hogy milyen típusú üzenetek ne alkalmazzanak mintavételezési beállításokat.</span><span class="sxs-lookup"><span data-stu-id="5af33-114">Specifies for what type of messages sampling settings should not apply.</span></span>
<span data-ttu-id="5af33-115">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="5af33-115">This parameter is optional.</span></span>

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

### <span data-ttu-id="5af33-116">-ApiId</span><span class="sxs-lookup"><span data-stu-id="5af33-116">-ApiId</span></span>
<span data-ttu-id="5af33-117">A meglévő API azonosítója.</span><span class="sxs-lookup"><span data-stu-id="5af33-117">Identifier of existing API.</span></span>
<span data-ttu-id="5af33-118">Ha meg van adva, az API-hatókör házirendet fog beállítani.</span><span class="sxs-lookup"><span data-stu-id="5af33-118">If specified will set API-scope policy.</span></span>
<span data-ttu-id="5af33-119">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="5af33-119">This parameters is required.</span></span>

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

### <span data-ttu-id="5af33-120">-BackendSetting</span><span class="sxs-lookup"><span data-stu-id="5af33-120">-BackendSetting</span></span>
<span data-ttu-id="5af33-121">A bejövő/kimenő http-üzenetek diagnosztikai beállítása a Háttérbe.</span><span class="sxs-lookup"><span data-stu-id="5af33-121">Diagnostic setting for incoming/outgoing Http Messages to the Backend.</span></span> <span data-ttu-id="5af33-122">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="5af33-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="5af33-123">-Környezet</span><span class="sxs-lookup"><span data-stu-id="5af33-123">-Context</span></span>
<span data-ttu-id="5af33-124">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="5af33-124">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="5af33-125">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="5af33-125">This parameter is required.</span></span>

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

### <span data-ttu-id="5af33-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5af33-126">-DefaultProfile</span></span>
<span data-ttu-id="5af33-127">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5af33-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5af33-128">-DiagnosticId</span><span class="sxs-lookup"><span data-stu-id="5af33-128">-DiagnosticId</span></span>
<span data-ttu-id="5af33-129">A diagnosztikai entitás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="5af33-129">Identifier of the diagnostics entity.</span></span>
<span data-ttu-id="5af33-130">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="5af33-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="5af33-131">-FrontEndSetting</span><span class="sxs-lookup"><span data-stu-id="5af33-131">-FrontEndSetting</span></span>
<span data-ttu-id="5af33-132">A bejövő/kimenő http-üzenetek diagnosztikai beállítása az átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="5af33-132">Diagnostic setting for incoming/outgoing Http Messages to the Gateway.</span></span> <span data-ttu-id="5af33-133">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="5af33-133">This parameter is optional.</span></span>

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

### <span data-ttu-id="5af33-134">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="5af33-134">-LoggerId</span></span>
<span data-ttu-id="5af33-135">Annak a naplózónak az azonosítója, akinek leküldéses diagnosztika szükséges.</span><span class="sxs-lookup"><span data-stu-id="5af33-135">Identifier of the logger to push diagnostics to.</span></span>
<span data-ttu-id="5af33-136">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="5af33-136">This parameter is required.</span></span>

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

### <span data-ttu-id="5af33-137">-SamplingSetting</span><span class="sxs-lookup"><span data-stu-id="5af33-137">-SamplingSetting</span></span>
<span data-ttu-id="5af33-138">A diagnosztikai eszköz mintavételezési beállítása.</span><span class="sxs-lookup"><span data-stu-id="5af33-138">Sampling Setting of the Diagnostic.</span></span>
<span data-ttu-id="5af33-139">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="5af33-139">This parameter is optional.</span></span>

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

### <span data-ttu-id="5af33-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5af33-140">-Confirm</span></span>
<span data-ttu-id="5af33-141">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="5af33-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5af33-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5af33-142">-WhatIf</span></span>
<span data-ttu-id="5af33-143">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="5af33-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5af33-144">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5af33-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5af33-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5af33-145">CommonParameters</span></span>
<span data-ttu-id="5af33-146">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5af33-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5af33-147">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5af33-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5af33-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5af33-148">INPUTS</span></span>

### <span data-ttu-id="5af33-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="5af33-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="5af33-150">System.String</span><span class="sxs-lookup"><span data-stu-id="5af33-150">System.String</span></span>

### <span data-ttu-id="5af33-151">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting</span><span class="sxs-lookup"><span data-stu-id="5af33-151">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting</span></span>

### <span data-ttu-id="5af33-152">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="5af33-152">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting</span></span>

## <span data-ttu-id="5af33-153">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5af33-153">OUTPUTS</span></span>

### <span data-ttu-id="5af33-154">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="5af33-154">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span></span>

## <span data-ttu-id="5af33-155">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5af33-155">NOTES</span></span>

## <span data-ttu-id="5af33-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5af33-156">RELATED LINKS</span></span>

[<span data-ttu-id="5af33-157">Get-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="5af33-157">Get-AzApiManagementDiagnostic</span></span>](./Get-AzApiManagementDiagnostic.md)

[<span data-ttu-id="5af33-158">Remove-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="5af33-158">Remove-AzApiManagementDiagnostic</span></span>](./Remove-AzApiManagementDiagnostic.md)

[<span data-ttu-id="5af33-159">Set-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="5af33-159">Set-AzApiManagementDiagnostic</span></span>](./Set-AzApiManagementDiagnostic.md)

[<span data-ttu-id="5af33-160">New-AzApiManagementHttpMessageDiagnostic</span><span class="sxs-lookup"><span data-stu-id="5af33-160">New-AzApiManagementHttpMessageDiagnostic</span></span>](./New-AzApiManagementHttpMessageDiagnostic.md)

[<span data-ttu-id="5af33-161">New-AzApiManagementSamplingSetting</span><span class="sxs-lookup"><span data-stu-id="5af33-161">New-AzApiManagementSamplingSetting</span></span>](./New-AzApiManagementHttpMessageDiagnostic.md)