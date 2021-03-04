---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/set-azapimanagementdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementDiagnostic.md
ms.openlocfilehash: c9cb592713f7a24739651d36855fdf595ffc7eeb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925329"
---
# <span data-ttu-id="8e8a5-101">Set-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="8e8a5-101">Set-AzApiManagementDiagnostic</span></span>

## <span data-ttu-id="8e8a5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e8a5-102">SYNOPSIS</span></span>
<span data-ttu-id="8e8a5-103">Módosítja az API-kezelés diagnosztikai eszközét a globális vagy az API-hatókörben.</span><span class="sxs-lookup"><span data-stu-id="8e8a5-103">Modifies an API Management diagnostic at the Global or Api scope.</span></span>

## <span data-ttu-id="8e8a5-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8e8a5-104">SYNTAX</span></span>

### <span data-ttu-id="8e8a5-105">ExpandedParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8e8a5-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementDiagnostic -Context <PsApiManagementContext> -DiagnosticId <String> [-ApiId <String>]
 [-LoggerId <String>] [-AlwaysLog <String>] [-SamplingSetting <PsApiManagementSamplingSetting>]
 [-FrontEndSetting <PsApiManagementPipelineDiagnosticSetting>]
 [-BackendSetting <PsApiManagementPipelineDiagnosticSetting>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e8a5-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="8e8a5-106">ByInputObject</span></span>
```
Set-AzApiManagementDiagnostic -InputObject <PsApiManagementDiagnostic> [-LoggerId <String>]
 [-AlwaysLog <String>] [-SamplingSetting <PsApiManagementSamplingSetting>]
 [-FrontEndSetting <PsApiManagementPipelineDiagnosticSetting>]
 [-BackendSetting <PsApiManagementPipelineDiagnosticSetting>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e8a5-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="8e8a5-107">ByResourceId</span></span>
```
Set-AzApiManagementDiagnostic -ResourceId <String> [-LoggerId <String>] [-AlwaysLog <String>]
 [-SamplingSetting <PsApiManagementSamplingSetting>]
 [-FrontEndSetting <PsApiManagementPipelineDiagnosticSetting>]
 [-BackendSetting <PsApiManagementPipelineDiagnosticSetting>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e8a5-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8e8a5-108">DESCRIPTION</span></span>
<span data-ttu-id="8e8a5-109">A **Set-AzApiManagementDiagnostic** parancsmag frissíti a globális vagy API-hatókörben konfigurált diagnosztikát.</span><span class="sxs-lookup"><span data-stu-id="8e8a5-109">The cmdlet **Set-AzApiManagementDiagnostic** updates the diagnostics which is configured at the Global or Api Scope.</span></span>

## <span data-ttu-id="8e8a5-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8e8a5-110">EXAMPLES</span></span>

### <span data-ttu-id="8e8a5-111">1. példa: Diagnosztikai hiba módosítása a globális hatókörben</span><span class="sxs-lookup"><span data-stu-id="8e8a5-111">Example 1: Modify a diagnostic at the Global scope</span></span>
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

<span data-ttu-id="8e8a5-112">Ez a parancs módosítja a megadott diagnosztikai mintavételezési százalékos értéket 100-ról 50%-ra</span><span class="sxs-lookup"><span data-stu-id="8e8a5-112">This command modifies the specified diagnostic Sampling Percentage from 100 to 50%</span></span>

### <span data-ttu-id="8e8a5-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="8e8a5-113">Example 2</span></span>

<span data-ttu-id="8e8a5-114">Módosítja az API-kezelés diagnosztikai eszközét a globális vagy az API-hatókörben.</span><span class="sxs-lookup"><span data-stu-id="8e8a5-114">Modifies an API Management diagnostic at the Global or Api scope.</span></span> <span data-ttu-id="8e8a5-115">(automatikusan generált)</span><span class="sxs-lookup"><span data-stu-id="8e8a5-115">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzApiManagementDiagnostic -AlwaysLog allErrors -ApiId '0001' -Context <PsApiManagementContext> -DiagnosticId 'applicationinsights' -LoggerId 'Logger123' -SamplingSetting <PsApiManagementSamplingSetting>
```

## <span data-ttu-id="8e8a5-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8e8a5-116">PARAMETERS</span></span>

### <span data-ttu-id="8e8a5-117">-AlwaysLog</span><span class="sxs-lookup"><span data-stu-id="8e8a5-117">-AlwaysLog</span></span>
<span data-ttu-id="8e8a5-118">Meghatározza, hogy milyen típusú üzenetek ne alkalmazzanak mintavételezési beállításokat.</span><span class="sxs-lookup"><span data-stu-id="8e8a5-118">Specifies for what type of messages sampling settings should not apply.</span></span>
<span data-ttu-id="8e8a5-119">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="8e8a5-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="8e8a5-120">-ApiId</span><span class="sxs-lookup"><span data-stu-id="8e8a5-120">-ApiId</span></span>
<span data-ttu-id="8e8a5-121">A meglévő API azonosítója.</span><span class="sxs-lookup"><span data-stu-id="8e8a5-121">Identifier of existing API.</span></span>
<span data-ttu-id="8e8a5-122">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="8e8a5-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="8e8a5-123">-BackendSetting</span><span class="sxs-lookup"><span data-stu-id="8e8a5-123">-BackendSetting</span></span>
<span data-ttu-id="8e8a5-124">Diagnosztikai beállítás a bejövő/kimenő http-üzenetekhez a Háttérbe.</span><span class="sxs-lookup"><span data-stu-id="8e8a5-124">Diagnostic setting for incoming/outgoing Http Messages to the Backend.</span></span> <span data-ttu-id="8e8a5-125">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="8e8a5-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="8e8a5-126">-Környezet</span><span class="sxs-lookup"><span data-stu-id="8e8a5-126">-Context</span></span>
<span data-ttu-id="8e8a5-127">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="8e8a5-127">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="8e8a5-128">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="8e8a5-128">This parameter is required.</span></span>

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

### <span data-ttu-id="8e8a5-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e8a5-129">-DefaultProfile</span></span>
<span data-ttu-id="8e8a5-130">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8e8a5-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e8a5-131">-DiagnosticId</span><span class="sxs-lookup"><span data-stu-id="8e8a5-131">-DiagnosticId</span></span>
<span data-ttu-id="8e8a5-132">A meglévő diagnosztikai azonosító.</span><span class="sxs-lookup"><span data-stu-id="8e8a5-132">Identifier of existing Diagnostic.</span></span>
<span data-ttu-id="8e8a5-133">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="8e8a5-133">This parameter is required.</span></span>

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

### <span data-ttu-id="8e8a5-134">-FrontEndSetting</span><span class="sxs-lookup"><span data-stu-id="8e8a5-134">-FrontEndSetting</span></span>
<span data-ttu-id="8e8a5-135">A bejövő/kimenő http-üzenetek diagnosztikai beállítása az átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="8e8a5-135">Diagnostic setting for incoming/outgoing Http Messages to the Gateway.</span></span> <span data-ttu-id="8e8a5-136">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="8e8a5-136">This parameter is optional.</span></span>

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

### <span data-ttu-id="8e8a5-137">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8e8a5-137">-InputObject</span></span>
<span data-ttu-id="8e8a5-138">A PsApiManagementDiagnostic példánya.</span><span class="sxs-lookup"><span data-stu-id="8e8a5-138">Instance of PsApiManagementDiagnostic.</span></span>
<span data-ttu-id="8e8a5-139">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="8e8a5-139">This parameter is required.</span></span>

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

### <span data-ttu-id="8e8a5-140">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="8e8a5-140">-LoggerId</span></span>
<span data-ttu-id="8e8a5-141">Annak a naplózónak az azonosítója, akinek leküldéses diagnosztika szükséges.</span><span class="sxs-lookup"><span data-stu-id="8e8a5-141">Identifier of the logger to push diagnostics to.</span></span>
<span data-ttu-id="8e8a5-142">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="8e8a5-142">This parameter is required.</span></span>

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

### <span data-ttu-id="8e8a5-143">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8e8a5-143">-PassThru</span></span>
<span data-ttu-id="8e8a5-144">Ha ez a beállítás meg van adva, akkor a Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic típus képviseli a halmaz diagnosztikai eszközét.</span><span class="sxs-lookup"><span data-stu-id="8e8a5-144">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic type representing the set Diagnostic.</span></span>

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

### <span data-ttu-id="8e8a5-145">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8e8a5-145">-ResourceId</span></span>
<span data-ttu-id="8e8a5-146">Arm ResourceId of Diagnostic vagy Api Diagnostic.</span><span class="sxs-lookup"><span data-stu-id="8e8a5-146">Arm ResourceId of Diagnostic or Api Diagnostic.</span></span> <span data-ttu-id="8e8a5-147">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="8e8a5-147">This parameter is required.</span></span>

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

### <span data-ttu-id="8e8a5-148">-SamplingSetting</span><span class="sxs-lookup"><span data-stu-id="8e8a5-148">-SamplingSetting</span></span>
<span data-ttu-id="8e8a5-149">A diagnosztikai eszköz mintavételezése.</span><span class="sxs-lookup"><span data-stu-id="8e8a5-149">Sampling Setting of the Diagnostic.</span></span>
<span data-ttu-id="8e8a5-150">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="8e8a5-150">This parameter is optional.</span></span>

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

### <span data-ttu-id="8e8a5-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8e8a5-151">-Confirm</span></span>
<span data-ttu-id="8e8a5-152">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="8e8a5-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e8a5-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e8a5-153">-WhatIf</span></span>
<span data-ttu-id="8e8a5-154">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="8e8a5-154">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8e8a5-155">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8e8a5-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e8a5-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e8a5-156">CommonParameters</span></span>
<span data-ttu-id="8e8a5-157">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e8a5-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e8a5-158">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8e8a5-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e8a5-159">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8e8a5-159">INPUTS</span></span>

### <span data-ttu-id="8e8a5-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="8e8a5-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="8e8a5-161">System.String</span><span class="sxs-lookup"><span data-stu-id="8e8a5-161">System.String</span></span>

### <span data-ttu-id="8e8a5-162">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="8e8a5-162">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span></span>

### <span data-ttu-id="8e8a5-163">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting</span><span class="sxs-lookup"><span data-stu-id="8e8a5-163">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting</span></span>

### <span data-ttu-id="8e8a5-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="8e8a5-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting</span></span>

### <span data-ttu-id="8e8a5-165">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="8e8a5-165">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="8e8a5-166">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8e8a5-166">OUTPUTS</span></span>

### <span data-ttu-id="8e8a5-167">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="8e8a5-167">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span></span>

## <span data-ttu-id="8e8a5-168">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8e8a5-168">NOTES</span></span>

## <span data-ttu-id="8e8a5-169">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8e8a5-169">RELATED LINKS</span></span>
