---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementDiagnostic.md
ms.openlocfilehash: c31c3d23e8e5ed160aff55a3599137454f1c638c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98367820"
---
# <span data-ttu-id="ec0c2-101">Get-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="ec0c2-101">Get-AzApiManagementDiagnostic</span></span>

## <span data-ttu-id="ec0c2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec0c2-102">SYNOPSIS</span></span>
<span data-ttu-id="ec0c2-103">A szolgáltatás vagy az Api szintjén konfigurált diagnosztikai adatok lekérte.</span><span class="sxs-lookup"><span data-stu-id="ec0c2-103">Get details of the Diagnostic configured at the service level or the Api Level.</span></span> <span data-ttu-id="ec0c2-104">A diagnosztika az Api Management átjárótól származó kérések és válaszok naplózására használható.</span><span class="sxs-lookup"><span data-stu-id="ec0c2-104">Diagnostics are used to log requests/responses from Api Management gateway.</span></span>

## <span data-ttu-id="ec0c2-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ec0c2-105">SYNTAX</span></span>

### <span data-ttu-id="ec0c2-106">ContextParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ec0c2-106">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementDiagnostic -Context <PsApiManagementContext> [-DiagnosticId <String>] [-ApiId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ec0c2-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ec0c2-107">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementDiagnostic -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ec0c2-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ec0c2-108">DESCRIPTION</span></span>
<span data-ttu-id="ec0c2-109">A **Get-AzApiManagementDiagnostic** adott hatókörben megkapja az Api-kezelési szolgáltatásban konfigurált diagnosztika részleteit.</span><span class="sxs-lookup"><span data-stu-id="ec0c2-109">The **Get-AzApiManagementDiagnostic** gets details of the diagnostics configured in the Api management service at a given scope.</span></span>

## <span data-ttu-id="ec0c2-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ec0c2-110">EXAMPLES</span></span>

### <span data-ttu-id="ec0c2-111">1. példa: A bérlői webhelyen konfigurált összes diagnosztikai beállítás lekérte.</span><span class="sxs-lookup"><span data-stu-id="ec0c2-111">Example 1: Get all the diagnostic configured at the tenant scope.</span></span>
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

<span data-ttu-id="ec0c2-112">Ez a parancs az Api Management szolgáltatásban konfigurált összes diagnosztika számára elérhető.</span><span class="sxs-lookup"><span data-stu-id="ec0c2-112">This command gets all the diagnostics configured in the Api Management service.</span></span>

### <span data-ttu-id="ec0c2-113">2. példa: Az Api hatókörében konfigurált összes diagnosztika lekérte</span><span class="sxs-lookup"><span data-stu-id="ec0c2-113">Example 2: Get all the diagnostics configured at the Api scope</span></span>
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

<span data-ttu-id="ec0c2-114">Ez a parancs az Api hatókörében konfigurált összes `echo-api` diagnosztikát lekérte</span><span class="sxs-lookup"><span data-stu-id="ec0c2-114">This command gets all the diagnostics configured at the `echo-api` Api scope</span></span>

### <span data-ttu-id="ec0c2-115">3. példa: Az API-hatókör diagnosztikai eszközének lekérte egy azonosítóval</span><span class="sxs-lookup"><span data-stu-id="ec0c2-115">Example 3: Get the API-scope diagnostic specified by an Id</span></span>
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

<span data-ttu-id="ec0c2-116">Ez a parancs az `applicationinsights` API-ban konfigurált diagnosztikát `echo-api` kapja.</span><span class="sxs-lookup"><span data-stu-id="ec0c2-116">This command gets the `applicationinsights` diagnostics configured in api `echo-api`.</span></span>

## <span data-ttu-id="ec0c2-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ec0c2-117">PARAMETERS</span></span>

### <span data-ttu-id="ec0c2-118">-ApiId</span><span class="sxs-lookup"><span data-stu-id="ec0c2-118">-ApiId</span></span>
<span data-ttu-id="ec0c2-119">A meglévő API azonosítója.</span><span class="sxs-lookup"><span data-stu-id="ec0c2-119">Identifier of existing API.</span></span>
<span data-ttu-id="ec0c2-120">Ha meg van adva, az API-hatókör diagnosztikát ad vissza.</span><span class="sxs-lookup"><span data-stu-id="ec0c2-120">If specified will return API-scope diagnostic.</span></span>
<span data-ttu-id="ec0c2-121">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="ec0c2-121">This parameters is required.</span></span>

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

### <span data-ttu-id="ec0c2-122">-Környezet</span><span class="sxs-lookup"><span data-stu-id="ec0c2-122">-Context</span></span>
<span data-ttu-id="ec0c2-123">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="ec0c2-123">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="ec0c2-124">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="ec0c2-124">This parameter is required.</span></span>

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

### <span data-ttu-id="ec0c2-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec0c2-125">-DefaultProfile</span></span>
<span data-ttu-id="ec0c2-126">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ec0c2-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec0c2-127">-DiagnosticId</span><span class="sxs-lookup"><span data-stu-id="ec0c2-127">-DiagnosticId</span></span>
<span data-ttu-id="ec0c2-128">A meglévő diagnosztikai eszköz azonosítója.</span><span class="sxs-lookup"><span data-stu-id="ec0c2-128">Identifier of existing diagnostic.</span></span>
<span data-ttu-id="ec0c2-129">Ha meg van adva, akkor a termék hatókörére vonatkozó házirendet ad vissza.</span><span class="sxs-lookup"><span data-stu-id="ec0c2-129">If specified will return product-scope policy.</span></span>
<span data-ttu-id="ec0c2-130">A paraméterek megadása nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="ec0c2-130">This parameters is optional.</span></span>

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

### <span data-ttu-id="ec0c2-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ec0c2-131">-ResourceId</span></span>
<span data-ttu-id="ec0c2-132">Diagnosztikai vagy API-diagnosztikai eszköz erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="ec0c2-132">Arm Resource Identifier of a Diagnostic or Api Diagnostic.</span></span> <span data-ttu-id="ec0c2-133">Ha meg van adva, az azonosító alapján próbálja megtalálni a diagnosztikai adatokat.</span><span class="sxs-lookup"><span data-stu-id="ec0c2-133">If specified will try to find diagnostic by the identifier.</span></span> <span data-ttu-id="ec0c2-134">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="ec0c2-134">This parameter is required.</span></span>

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

### <span data-ttu-id="ec0c2-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec0c2-135">CommonParameters</span></span>
<span data-ttu-id="ec0c2-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec0c2-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec0c2-137">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ec0c2-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec0c2-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ec0c2-138">INPUTS</span></span>

### <span data-ttu-id="ec0c2-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="ec0c2-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="ec0c2-140">System.String</span><span class="sxs-lookup"><span data-stu-id="ec0c2-140">System.String</span></span>

## <span data-ttu-id="ec0c2-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ec0c2-141">OUTPUTS</span></span>

### <span data-ttu-id="ec0c2-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="ec0c2-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span></span>

## <span data-ttu-id="ec0c2-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ec0c2-143">NOTES</span></span>

## <span data-ttu-id="ec0c2-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ec0c2-144">RELATED LINKS</span></span>
