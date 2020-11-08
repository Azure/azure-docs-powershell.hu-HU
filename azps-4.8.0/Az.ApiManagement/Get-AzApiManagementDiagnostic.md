---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementDiagnostic.md
ms.openlocfilehash: c31c3d23e8e5ed160aff55a3599137454f1c638c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94185109"
---
# <span data-ttu-id="e8571-101">Get-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="e8571-101">Get-AzApiManagementDiagnostic</span></span>

## <span data-ttu-id="e8571-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e8571-102">SYNOPSIS</span></span>
<span data-ttu-id="e8571-103">A szolgáltatás szintjén vagy az API szintjén konfigurált diagnosztikai adatok részletes ismertetése.</span><span class="sxs-lookup"><span data-stu-id="e8571-103">Get details of the Diagnostic configured at the service level or the Api Level.</span></span> <span data-ttu-id="e8571-104">A diagnosztika az API-kezelési átjárótól érkező kérések és válaszok naplózására szolgál.</span><span class="sxs-lookup"><span data-stu-id="e8571-104">Diagnostics are used to log requests/responses from Api Management gateway.</span></span>

## <span data-ttu-id="e8571-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e8571-105">SYNTAX</span></span>

### <span data-ttu-id="e8571-106">ContextParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e8571-106">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementDiagnostic -Context <PsApiManagementContext> [-DiagnosticId <String>] [-ApiId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e8571-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e8571-107">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementDiagnostic -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e8571-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="e8571-108">DESCRIPTION</span></span>
<span data-ttu-id="e8571-109">A **Get-AzApiManagementDiagnostic** az API-kezelési szolgáltatásban megadott keresési diagnosztikai szolgáltatás részleteit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="e8571-109">The **Get-AzApiManagementDiagnostic** gets details of the diagnostics configured in the Api management service at a given scope.</span></span>

## <span data-ttu-id="e8571-110">Példák</span><span class="sxs-lookup"><span data-stu-id="e8571-110">EXAMPLES</span></span>

### <span data-ttu-id="e8571-111">Példa 1: a bérlői hatókörben konfigurált összes diagnosztikai elem beszerzése.</span><span class="sxs-lookup"><span data-stu-id="e8571-111">Example 1: Get all the diagnostic configured at the tenant scope.</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementDiagnostic -Context $apimContext

DiagnosticId                 : applicationinsights
ApiId                        :
AlwaysLog                    : allErrors
LoggerId                     : backendapisachinc
EnableHttpCorrelationHeaders : True
SamplingSetting              : Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting
FrontendSetting              :
BackendSetting               :
Id                           : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/diagnostics/applicationinsights
ResourceGroupName            : Api-Default-WestUS
ServiceName                  : contoso

DiagnosticId                 : azuremonitor
ApiId                        :
AlwaysLog                    :
LoggerId                     : azuremonitor
EnableHttpCorrelationHeaders :
SamplingSetting              : Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting
FrontendSetting              :
BackendSetting               : 
Id                           : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/diagnostics/azuremonitor
ResourceGroupName            : Api-Default-WestUS
ServiceName                  : contoso
```

<span data-ttu-id="e8571-112">Ez a parancs beilleszti az API-kezelési szolgáltatásban beállított összes diagnosztikát.</span><span class="sxs-lookup"><span data-stu-id="e8571-112">This command gets all the diagnostics configured in the Api Management service.</span></span>

### <span data-ttu-id="e8571-113">2. példa: az API-hatókörben konfigurált összes diagnosztika beszerzése</span><span class="sxs-lookup"><span data-stu-id="e8571-113">Example 2: Get all the diagnostics configured at the Api scope</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementDiagnostic -Context $apimContext -ApiId "echo-api"

DiagnosticId                 : applicationinsights
ApiId                        : echo-api
AlwaysLog                    : allErrors
LoggerId                     : backendapisachinc
EnableHttpCorrelationHeaders : True
SamplingSetting              : Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting
FrontendSetting              : Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting
BackendSetting               : Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting
Id                           : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/diagnostics/applicationinsights
ResourceGroupName            : Api-Default-WestUS
ServiceName                  : contoso
```

<span data-ttu-id="e8571-114">Ez a parancs az API-hatókörben konfigurált összes diagnosztikát bekerül `echo-api`</span><span class="sxs-lookup"><span data-stu-id="e8571-114">This command gets all the diagnostics configured at the `echo-api` Api scope</span></span>

### <span data-ttu-id="e8571-115">3. példa: az API-tartomány diagnosztikai azonosítójának beszerzése</span><span class="sxs-lookup"><span data-stu-id="e8571-115">Example 3: Get the API-scope diagnostic specified by an Id</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementDiagnostic -Context $apimContext -ApiId "echo-api" -DiagnosticId "applicationinsights"

DiagnosticId                 : applicationinsights
ApiId                        : echo-api
AlwaysLog                    : allErrors
LoggerId                     : backendapisachinc
EnableHttpCorrelationHeaders : True
SamplingSetting              : Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting
FrontendSetting              :
BackendSetting               :
Id                           : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/diagnostics/applicationinsights
ResourceGroupName            : Api-Default-WestUS
ServiceName                  : contoso
```

<span data-ttu-id="e8571-116">Ez a parancs az `applicationinsights` API-ban konfigurált diagnosztikát kapja `echo-api` .</span><span class="sxs-lookup"><span data-stu-id="e8571-116">This command gets the `applicationinsights` diagnostics configured in api `echo-api`.</span></span>

## <span data-ttu-id="e8571-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e8571-117">PARAMETERS</span></span>

### <span data-ttu-id="e8571-118">-ApiId</span><span class="sxs-lookup"><span data-stu-id="e8571-118">-ApiId</span></span>
<span data-ttu-id="e8571-119">A meglévő API-azonosító.</span><span class="sxs-lookup"><span data-stu-id="e8571-119">Identifier of existing API.</span></span>
<span data-ttu-id="e8571-120">Ha meg van adva, akkor az API-hatókör diagnosztikai funkcióját adja vissza.</span><span class="sxs-lookup"><span data-stu-id="e8571-120">If specified will return API-scope diagnostic.</span></span>
<span data-ttu-id="e8571-121">Ehhez a paraméterekre van szükség.</span><span class="sxs-lookup"><span data-stu-id="e8571-121">This parameters is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8571-122">-Környezet</span><span class="sxs-lookup"><span data-stu-id="e8571-122">-Context</span></span>
<span data-ttu-id="e8571-123">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="e8571-123">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="e8571-124">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="e8571-124">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e8571-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8571-125">-DefaultProfile</span></span>
<span data-ttu-id="e8571-126">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e8571-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8571-127">-DiagnosticId</span><span class="sxs-lookup"><span data-stu-id="e8571-127">-DiagnosticId</span></span>
<span data-ttu-id="e8571-128">A meglévő diagnosztikai azonosító.</span><span class="sxs-lookup"><span data-stu-id="e8571-128">Identifier of existing diagnostic.</span></span>
<span data-ttu-id="e8571-129">Ha meg van adva a termékek hatókörét visszaadó házirend.</span><span class="sxs-lookup"><span data-stu-id="e8571-129">If specified will return product-scope policy.</span></span>
<span data-ttu-id="e8571-130">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="e8571-130">This parameters is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8571-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e8571-131">-ResourceId</span></span>
<span data-ttu-id="e8571-132">A diagnosztikai vagy API-diagnosztikai diagnosztikai vagy API-diagnosztikai erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="e8571-132">Arm Resource Identifier of a Diagnostic or Api Diagnostic.</span></span> <span data-ttu-id="e8571-133">Ha meg van adva, a program megpróbálja diagnosztikai lehetőséget keresni az azonosítóval.</span><span class="sxs-lookup"><span data-stu-id="e8571-133">If specified will try to find diagnostic by the identifier.</span></span> <span data-ttu-id="e8571-134">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="e8571-134">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8571-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8571-135">CommonParameters</span></span>
<span data-ttu-id="e8571-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e8571-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8571-137">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e8571-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8571-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e8571-138">INPUTS</span></span>

### <span data-ttu-id="e8571-139">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="e8571-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e8571-140">System. String</span><span class="sxs-lookup"><span data-stu-id="e8571-140">System.String</span></span>

## <span data-ttu-id="e8571-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e8571-141">OUTPUTS</span></span>

### <span data-ttu-id="e8571-142">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="e8571-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span></span>

## <span data-ttu-id="e8571-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e8571-143">NOTES</span></span>

## <span data-ttu-id="e8571-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e8571-144">RELATED LINKS</span></span>
