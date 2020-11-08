---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementDiagnostic.md
ms.openlocfilehash: f3add9f35e56d4ba6d92b8438b970ddf8c682804
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013857"
---
# <span data-ttu-id="5f085-101">Set-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="5f085-101">Set-AzApiManagementDiagnostic</span></span>

## <span data-ttu-id="5f085-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5f085-102">SYNOPSIS</span></span>
<span data-ttu-id="5f085-103">API-kezelési diagnosztikai diagnosztikai művelet módosítása globális vagy API-hatókörben.</span><span class="sxs-lookup"><span data-stu-id="5f085-103">Modifies an API Management diagnostic at the Global or Api scope.</span></span>

## <span data-ttu-id="5f085-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5f085-104">SYNTAX</span></span>

### <span data-ttu-id="5f085-105">ExpandedParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5f085-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementDiagnostic -Context <PsApiManagementContext> -DiagnosticId <String> [-ApiId <String>]
 [-LoggerId <String>] [-AlwaysLog <String>] [-SamplingSetting <PsApiManagementSamplingSetting>]
 [-FrontEndSetting <PsApiManagementPipelineDiagnosticSetting>]
 [-BackendSetting <PsApiManagementPipelineDiagnosticSetting>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f085-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="5f085-106">ByInputObject</span></span>
```
Set-AzApiManagementDiagnostic -InputObject <PsApiManagementDiagnostic> [-LoggerId <String>]
 [-AlwaysLog <String>] [-SamplingSetting <PsApiManagementSamplingSetting>]
 [-FrontEndSetting <PsApiManagementPipelineDiagnosticSetting>]
 [-BackendSetting <PsApiManagementPipelineDiagnosticSetting>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f085-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="5f085-107">ByResourceId</span></span>
```
Set-AzApiManagementDiagnostic -ResourceId <String> [-LoggerId <String>] [-AlwaysLog <String>]
 [-SamplingSetting <PsApiManagementSamplingSetting>]
 [-FrontEndSetting <PsApiManagementPipelineDiagnosticSetting>]
 [-BackendSetting <PsApiManagementPipelineDiagnosticSetting>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5f085-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="5f085-108">DESCRIPTION</span></span>
<span data-ttu-id="5f085-109">A parancsmag **beállítása – AzApiManagementDiagnostic** frissíti a globális vagy API-hatókörben konfigurált diagnosztikát.</span><span class="sxs-lookup"><span data-stu-id="5f085-109">The cmdlet **Set-AzApiManagementDiagnostic** updates the diagnostics which is configured at the Global or Api Scope.</span></span>

## <span data-ttu-id="5f085-110">Példák</span><span class="sxs-lookup"><span data-stu-id="5f085-110">EXAMPLES</span></span>

### <span data-ttu-id="5f085-111">1. példa: a globális tartomány diagnosztikai beállításainak módosítása</span><span class="sxs-lookup"><span data-stu-id="5f085-111">Example 1: Modify a diagnostic at the Global scope</span></span>
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

<span data-ttu-id="5f085-112">Ez a parancs a megadott diagnosztikai mintavételi százalékot módosította az 100-ből 50%-ra.</span><span class="sxs-lookup"><span data-stu-id="5f085-112">This command modifies the specified diagnostic Sampling Percentage from 100 to 50%</span></span>

## <span data-ttu-id="5f085-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5f085-113">PARAMETERS</span></span>

### <span data-ttu-id="5f085-114">-AlwaysLog</span><span class="sxs-lookup"><span data-stu-id="5f085-114">-AlwaysLog</span></span>
<span data-ttu-id="5f085-115">Azt adja meg, hogy milyen típusú üzenetek mintavételi beállításai ne legyenek alkalmazhatók.</span><span class="sxs-lookup"><span data-stu-id="5f085-115">Specifies for what type of messages sampling settings should not apply.</span></span>
<span data-ttu-id="5f085-116">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="5f085-116">This parameter is optional.</span></span>

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

### <span data-ttu-id="5f085-117">-ApiId</span><span class="sxs-lookup"><span data-stu-id="5f085-117">-ApiId</span></span>
<span data-ttu-id="5f085-118">A meglévő API-azonosító.</span><span class="sxs-lookup"><span data-stu-id="5f085-118">Identifier of existing API.</span></span>
<span data-ttu-id="5f085-119">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="5f085-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="5f085-120">-BackendSetting</span><span class="sxs-lookup"><span data-stu-id="5f085-120">-BackendSetting</span></span>
<span data-ttu-id="5f085-121">Diagnosztikai beállítás a bejövő és kimenő http-üzenetekhez a Backendben.</span><span class="sxs-lookup"><span data-stu-id="5f085-121">Diagnostic setting for incoming/outgoing Http Messages to the Backend.</span></span> <span data-ttu-id="5f085-122">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="5f085-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="5f085-123">-Környezet</span><span class="sxs-lookup"><span data-stu-id="5f085-123">-Context</span></span>
<span data-ttu-id="5f085-124">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="5f085-124">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="5f085-125">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="5f085-125">This parameter is required.</span></span>

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

### <span data-ttu-id="5f085-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f085-126">-DefaultProfile</span></span>
<span data-ttu-id="5f085-127">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5f085-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5f085-128">-DiagnosticId</span><span class="sxs-lookup"><span data-stu-id="5f085-128">-DiagnosticId</span></span>
<span data-ttu-id="5f085-129">A meglévő diagnosztikai azonosító.</span><span class="sxs-lookup"><span data-stu-id="5f085-129">Identifier of existing Diagnostic.</span></span>
<span data-ttu-id="5f085-130">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="5f085-130">This parameter is required.</span></span>

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

### <span data-ttu-id="5f085-131">-FrontEndSetting</span><span class="sxs-lookup"><span data-stu-id="5f085-131">-FrontEndSetting</span></span>
<span data-ttu-id="5f085-132">Diagnosztikai beállítás a bejövő és kimenő http-üzenetekhez az átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="5f085-132">Diagnostic setting for incoming/outgoing Http Messages to the Gateway.</span></span> <span data-ttu-id="5f085-133">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="5f085-133">This parameter is optional.</span></span>

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

### <span data-ttu-id="5f085-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5f085-134">-InputObject</span></span>
<span data-ttu-id="5f085-135">A PsApiManagementDiagnostic példánya.</span><span class="sxs-lookup"><span data-stu-id="5f085-135">Instance of PsApiManagementDiagnostic.</span></span>
<span data-ttu-id="5f085-136">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="5f085-136">This parameter is required.</span></span>

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

### <span data-ttu-id="5f085-137">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="5f085-137">-LoggerId</span></span>
<span data-ttu-id="5f085-138">Az adatnaplózó azonosítója, amellyel lenyomja a diagnosztikát.</span><span class="sxs-lookup"><span data-stu-id="5f085-138">Identifier of the logger to push diagnostics to.</span></span>
<span data-ttu-id="5f085-139">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="5f085-139">This parameter is required.</span></span>

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

### <span data-ttu-id="5f085-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5f085-140">-PassThru</span></span>
<span data-ttu-id="5f085-141">Ha meg van adva, akkor a Microsoft. Azure. commands. ApiManagement. ServiceManagement. models. PsApiManagementDiagnostic típusa a set diagnosztikai beállítását jelenti.</span><span class="sxs-lookup"><span data-stu-id="5f085-141">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic type representing the set Diagnostic.</span></span>

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

### <span data-ttu-id="5f085-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5f085-142">-ResourceId</span></span>
<span data-ttu-id="5f085-143">Kar ResourceId diagnosztikai vagy API-diagnosztikai.</span><span class="sxs-lookup"><span data-stu-id="5f085-143">Arm ResourceId of Diagnostic or Api Diagnostic.</span></span> <span data-ttu-id="5f085-144">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="5f085-144">This parameter is required.</span></span>

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

### <span data-ttu-id="5f085-145">-SamplingSetting</span><span class="sxs-lookup"><span data-stu-id="5f085-145">-SamplingSetting</span></span>
<span data-ttu-id="5f085-146">A diagnosztikai környezet mintavételi beállításai</span><span class="sxs-lookup"><span data-stu-id="5f085-146">Sampling Setting of the Diagnostic.</span></span>
<span data-ttu-id="5f085-147">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="5f085-147">This parameter is optional.</span></span>

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

### <span data-ttu-id="5f085-148">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5f085-148">-Confirm</span></span>
<span data-ttu-id="5f085-149">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5f085-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5f085-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f085-150">-WhatIf</span></span>
<span data-ttu-id="5f085-151">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5f085-151">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5f085-152">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5f085-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5f085-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f085-153">CommonParameters</span></span>
<span data-ttu-id="5f085-154">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5f085-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f085-155">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="5f085-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f085-156">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5f085-156">INPUTS</span></span>

### <span data-ttu-id="5f085-157">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="5f085-157">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="5f085-158">System. String</span><span class="sxs-lookup"><span data-stu-id="5f085-158">System.String</span></span>

### <span data-ttu-id="5f085-159">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="5f085-159">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span></span>

### <span data-ttu-id="5f085-160">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementSamplingSetting</span><span class="sxs-lookup"><span data-stu-id="5f085-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting</span></span>

### <span data-ttu-id="5f085-161">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementPipelineDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="5f085-161">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting</span></span>

### <span data-ttu-id="5f085-162">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="5f085-162">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="5f085-163">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5f085-163">OUTPUTS</span></span>

### <span data-ttu-id="5f085-164">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="5f085-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span></span>

## <span data-ttu-id="5f085-165">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5f085-165">NOTES</span></span>

## <span data-ttu-id="5f085-166">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5f085-166">RELATED LINKS</span></span>
