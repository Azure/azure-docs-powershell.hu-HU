---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementDiagnostic.md
ms.openlocfilehash: c646e7f39b5149803161bfc7b97ed64b5517dd9e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024245"
---
# <span data-ttu-id="96b14-101">Set-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="96b14-101">Set-AzApiManagementDiagnostic</span></span>

## <span data-ttu-id="96b14-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="96b14-102">SYNOPSIS</span></span>
<span data-ttu-id="96b14-103">API-kezelési diagnosztikai diagnosztikai művelet módosítása globális vagy API-hatókörben.</span><span class="sxs-lookup"><span data-stu-id="96b14-103">Modifies an API Management diagnostic at the Global or Api scope.</span></span>

## <span data-ttu-id="96b14-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="96b14-104">SYNTAX</span></span>

### <span data-ttu-id="96b14-105">ExpandedParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="96b14-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementDiagnostic -Context <PsApiManagementContext> -DiagnosticId <String> [-ApiId <String>]
 [-LoggerId <String>] [-AlwaysLog <String>] [-SamplingSetting <PsApiManagementSamplingSetting>]
 [-FrontEndSetting <PsApiManagementPipelineDiagnosticSetting>]
 [-BackendSetting <PsApiManagementPipelineDiagnosticSetting>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96b14-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="96b14-106">ByInputObject</span></span>
```
Set-AzApiManagementDiagnostic -InputObject <PsApiManagementDiagnostic> [-LoggerId <String>]
 [-AlwaysLog <String>] [-SamplingSetting <PsApiManagementSamplingSetting>]
 [-FrontEndSetting <PsApiManagementPipelineDiagnosticSetting>]
 [-BackendSetting <PsApiManagementPipelineDiagnosticSetting>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96b14-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="96b14-107">ByResourceId</span></span>
```
Set-AzApiManagementDiagnostic -ResourceId <String> [-LoggerId <String>] [-AlwaysLog <String>]
 [-SamplingSetting <PsApiManagementSamplingSetting>]
 [-FrontEndSetting <PsApiManagementPipelineDiagnosticSetting>]
 [-BackendSetting <PsApiManagementPipelineDiagnosticSetting>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="96b14-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="96b14-108">DESCRIPTION</span></span>
<span data-ttu-id="96b14-109">A parancsmag **beállítása – AzApiManagementDiagnostic** frissíti a globális vagy API-hatókörben konfigurált diagnosztikát.</span><span class="sxs-lookup"><span data-stu-id="96b14-109">The cmdlet **Set-AzApiManagementDiagnostic** updates the diagnostics which is configured at the Global or Api Scope.</span></span>

## <span data-ttu-id="96b14-110">Példák</span><span class="sxs-lookup"><span data-stu-id="96b14-110">EXAMPLES</span></span>

### <span data-ttu-id="96b14-111">1. példa: a globális tartomány diagnosztikai beállításainak módosítása</span><span class="sxs-lookup"><span data-stu-id="96b14-111">Example 1: Modify a diagnostic at the Global scope</span></span>
```powershell
PS c:\> $context =New-AzApiManagementContext -ResourceGroupName Api-Default-WestUS -ServiceName contoso
PS c:\> $diagnostic=Get-AzApiManagementDiagnostic -Context $context -DiagnosticId "applicationinsights"
PS c:\> $diagnostic

DiagnosticId      : applicationinsights
AlwaysLog         : allErrors
LoggerId          : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/loggers/backendapisachinc
Sampling          : Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting
Frontend          :
Backend           :
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/diagnostics/applicationinsights
ResourceGroupName : Api-Default-WestUS
ServiceName       : contoso


PS c:\> $diagnostic.Sampling

SamplingType Percentage
------------ ----------
fixed               100

PS c:\> $diagnostic.Sampling.Percentage = 50
PS c:\> $diagnostic.Sampling

SamplingType Percentage
------------ ----------
fixed                50

PS c:\> Set-AzApiManagementDiagnostic -InputObject $diagnostic
```

<span data-ttu-id="96b14-112">Ez a parancs a megadott diagnosztikai mintavételi százalékot módosította az 100-ből 50%-ra.</span><span class="sxs-lookup"><span data-stu-id="96b14-112">This command modifies the specified diagnostic Sampling Percentage from 100 to 50%</span></span>

### <span data-ttu-id="96b14-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="96b14-113">Example 2</span></span>

<span data-ttu-id="96b14-114">API-kezelési diagnosztikai diagnosztikai művelet módosítása globális vagy API-hatókörben.</span><span class="sxs-lookup"><span data-stu-id="96b14-114">Modifies an API Management diagnostic at the Global or Api scope.</span></span> <span data-ttu-id="96b14-115">autogenerated</span><span class="sxs-lookup"><span data-stu-id="96b14-115">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzApiManagementDiagnostic -AlwaysLog allErrors -ApiId '0001' -Context <PsApiManagementContext> -DiagnosticId 'applicationinsights' -LoggerId 'Logger123' -SamplingSetting <PsApiManagementSamplingSetting>
```

## <span data-ttu-id="96b14-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="96b14-116">PARAMETERS</span></span>

### <span data-ttu-id="96b14-117">-AlwaysLog</span><span class="sxs-lookup"><span data-stu-id="96b14-117">-AlwaysLog</span></span>
<span data-ttu-id="96b14-118">Azt adja meg, hogy milyen típusú üzenetek mintavételi beállításai ne legyenek alkalmazhatók.</span><span class="sxs-lookup"><span data-stu-id="96b14-118">Specifies for what type of messages sampling settings should not apply.</span></span>
<span data-ttu-id="96b14-119">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="96b14-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="96b14-120">-ApiId</span><span class="sxs-lookup"><span data-stu-id="96b14-120">-ApiId</span></span>
<span data-ttu-id="96b14-121">A meglévő API-azonosító.</span><span class="sxs-lookup"><span data-stu-id="96b14-121">Identifier of existing API.</span></span>
<span data-ttu-id="96b14-122">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="96b14-122">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96b14-123">-BackendSetting</span><span class="sxs-lookup"><span data-stu-id="96b14-123">-BackendSetting</span></span>
<span data-ttu-id="96b14-124">Diagnosztikai beállítás a bejövő és kimenő http-üzenetekhez a Backendben.</span><span class="sxs-lookup"><span data-stu-id="96b14-124">Diagnostic setting for incoming/outgoing Http Messages to the Backend.</span></span> <span data-ttu-id="96b14-125">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="96b14-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="96b14-126">-Környezet</span><span class="sxs-lookup"><span data-stu-id="96b14-126">-Context</span></span>
<span data-ttu-id="96b14-127">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="96b14-127">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="96b14-128">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="96b14-128">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="96b14-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96b14-129">-DefaultProfile</span></span>
<span data-ttu-id="96b14-130">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="96b14-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="96b14-131">-DiagnosticId</span><span class="sxs-lookup"><span data-stu-id="96b14-131">-DiagnosticId</span></span>
<span data-ttu-id="96b14-132">A meglévő diagnosztikai azonosító.</span><span class="sxs-lookup"><span data-stu-id="96b14-132">Identifier of existing Diagnostic.</span></span>
<span data-ttu-id="96b14-133">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="96b14-133">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96b14-134">-FrontEndSetting</span><span class="sxs-lookup"><span data-stu-id="96b14-134">-FrontEndSetting</span></span>
<span data-ttu-id="96b14-135">Diagnosztikai beállítás a bejövő és kimenő http-üzenetekhez az átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="96b14-135">Diagnostic setting for incoming/outgoing Http Messages to the Gateway.</span></span> <span data-ttu-id="96b14-136">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="96b14-136">This parameter is optional.</span></span>

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

### <span data-ttu-id="96b14-137">-InputObject</span><span class="sxs-lookup"><span data-stu-id="96b14-137">-InputObject</span></span>
<span data-ttu-id="96b14-138">A PsApiManagementDiagnostic példánya.</span><span class="sxs-lookup"><span data-stu-id="96b14-138">Instance of PsApiManagementDiagnostic.</span></span>
<span data-ttu-id="96b14-139">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="96b14-139">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="96b14-140">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="96b14-140">-LoggerId</span></span>
<span data-ttu-id="96b14-141">Az adatnaplózó azonosítója, amellyel lenyomja a diagnosztikát.</span><span class="sxs-lookup"><span data-stu-id="96b14-141">Identifier of the logger to push diagnostics to.</span></span>
<span data-ttu-id="96b14-142">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="96b14-142">This parameter is required.</span></span>

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

### <span data-ttu-id="96b14-143">-PassThru</span><span class="sxs-lookup"><span data-stu-id="96b14-143">-PassThru</span></span>
<span data-ttu-id="96b14-144">Ha meg van adva, akkor a Microsoft. Azure. commands. ApiManagement. ServiceManagement. models. PsApiManagementDiagnostic típusa a set diagnosztikai beállítását jelenti.</span><span class="sxs-lookup"><span data-stu-id="96b14-144">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic type representing the set Diagnostic.</span></span>

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

### <span data-ttu-id="96b14-145">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="96b14-145">-ResourceId</span></span>
<span data-ttu-id="96b14-146">Kar ResourceId diagnosztikai vagy API-diagnosztikai.</span><span class="sxs-lookup"><span data-stu-id="96b14-146">Arm ResourceId of Diagnostic or Api Diagnostic.</span></span> <span data-ttu-id="96b14-147">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="96b14-147">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96b14-148">-SamplingSetting</span><span class="sxs-lookup"><span data-stu-id="96b14-148">-SamplingSetting</span></span>
<span data-ttu-id="96b14-149">A diagnosztikai környezet mintavételi beállításai</span><span class="sxs-lookup"><span data-stu-id="96b14-149">Sampling Setting of the Diagnostic.</span></span>
<span data-ttu-id="96b14-150">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="96b14-150">This parameter is optional.</span></span>

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

### <span data-ttu-id="96b14-151">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="96b14-151">-Confirm</span></span>
<span data-ttu-id="96b14-152">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="96b14-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96b14-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96b14-153">-WhatIf</span></span>
<span data-ttu-id="96b14-154">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="96b14-154">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="96b14-155">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="96b14-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96b14-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96b14-156">CommonParameters</span></span>
<span data-ttu-id="96b14-157">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="96b14-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96b14-158">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="96b14-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96b14-159">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="96b14-159">INPUTS</span></span>

### <span data-ttu-id="96b14-160">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="96b14-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="96b14-161">System. String</span><span class="sxs-lookup"><span data-stu-id="96b14-161">System.String</span></span>

### <span data-ttu-id="96b14-162">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="96b14-162">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span></span>

### <span data-ttu-id="96b14-163">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementSamplingSetting</span><span class="sxs-lookup"><span data-stu-id="96b14-163">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting</span></span>

### <span data-ttu-id="96b14-164">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementPipelineDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="96b14-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting</span></span>

### <span data-ttu-id="96b14-165">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="96b14-165">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="96b14-166">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="96b14-166">OUTPUTS</span></span>

### <span data-ttu-id="96b14-167">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="96b14-167">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span></span>

## <span data-ttu-id="96b14-168">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="96b14-168">NOTES</span></span>

## <span data-ttu-id="96b14-169">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="96b14-169">RELATED LINKS</span></span>
