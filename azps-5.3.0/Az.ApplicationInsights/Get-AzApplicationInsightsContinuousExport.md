---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/get-azapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsightsContinuousExport.md
ms.openlocfilehash: d5711e6bca9b0579b456e4d2b0c5f915b4ad6fe0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98381399"
---
# <span data-ttu-id="07fc1-101">Get-AzApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="07fc1-101">Get-AzApplicationInsightsContinuousExport</span></span>

## <span data-ttu-id="07fc1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07fc1-102">SYNOPSIS</span></span>
<span data-ttu-id="07fc1-103">Alkalmazásstatikációk folyamatos exportálási konfigurációjának lekérte egy alkalmazásstatékony erőforráshoz</span><span class="sxs-lookup"><span data-stu-id="07fc1-103">Get application insights continuous export configuration for an application insights resource</span></span>

## <span data-ttu-id="07fc1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="07fc1-104">SYNTAX</span></span>

### <span data-ttu-id="07fc1-105">ComponentNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="07fc1-105">ComponentNameParameterSet (Default)</span></span>
```
Get-AzApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String> [[-ExportId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="07fc1-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="07fc1-106">ComponentObjectParameterSet</span></span>
```
Get-AzApplicationInsightsContinuousExport [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [[-ExportId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="07fc1-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="07fc1-107">ResourceIdParameterSet</span></span>
```
Get-AzApplicationInsightsContinuousExport [-ResourceId] <String> [[-ExportId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="07fc1-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="07fc1-108">DESCRIPTION</span></span>
<span data-ttu-id="07fc1-109">Alkalmazásstatikációk folyamatos exportálási konfigurációjának lekérte egy alkalmazásstatékony erőforráshoz</span><span class="sxs-lookup"><span data-stu-id="07fc1-109">Get application insights continuous export configuration for an application insights resource</span></span>

## <span data-ttu-id="07fc1-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="07fc1-110">EXAMPLES</span></span>

### <span data-ttu-id="07fc1-111">1. példa: Folyamatos exportálás alkalmazáselemzési erőforráshoz</span><span class="sxs-lookup"><span data-stu-id="07fc1-111">Example 1 Get continuous export for an application insights resource</span></span>
```
PS C:\> Get-AzApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test"

ExportId                     DocumentTypes                ExportStatus DestinationStorageAccountId
--------                     -------------                ------------ ---------------------------
ZJrfffySPdtG3ESn3iRxVIEFuNY= Request, Performance Counter Preparing    /subscriptions/{subid}...
```

<span data-ttu-id="07fc1-112">Alkalmazásstatikációk folyamatos exportálási konfigurációja a "teszt" nevű erőforráshoz a "tesztcsoport" erőforráscsoportban</span><span class="sxs-lookup"><span data-stu-id="07fc1-112">Get application insights continuous export configurations for resource named "test" in resource group "testgroup"</span></span>

### <span data-ttu-id="07fc1-113">2. példa: Folyamatos exportálás alkalmazáselemzési erőforráshoz</span><span class="sxs-lookup"><span data-stu-id="07fc1-113">Example 2 Get continuous export for an application insights resource</span></span>
```
PS C:\> Get-AzApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test" -ExportId "ZJrfffySPdtG3ESn3iRxVIEFuNY="

ExportId                         : ZJrfffySPdtG3ESn3iRxVIEFuNY=
StorageName                      : targetaccount
ContainerName                    : continuousexport
DocumentTypes                    : Request, Performance Counter
DestinationStorageSubscriptionId : {subid}
DestinationStorageLocationId     : eastus
DestinationStorageAccountId      : /subscriptions/{subid}/resourceGroups/targetstorage/providers/Microsoft.Storage/storageAccounts/targetaccount
IsEnabled                        : True
ExportStatus                     : Preparing
LastSuccessTime                  :
```

<span data-ttu-id="07fc1-114">Az "ZJrfffySPdtG3ESn3iRxVIEFuNY=" nevű exportálási azonosítóval folyamatos exportálási konfigurációt kaphat az "teszt" nevű erőforráshoz a "tesztcsoport" erőforráscsoportban</span><span class="sxs-lookup"><span data-stu-id="07fc1-114">Get application insights continuous export configuration with export id "ZJrfffySPdtG3ESn3iRxVIEFuNY=" for resource named "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="07fc1-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="07fc1-115">PARAMETERS</span></span>

### <span data-ttu-id="07fc1-116">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="07fc1-116">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="07fc1-117">Application Insights összetevő-objektum.</span><span class="sxs-lookup"><span data-stu-id="07fc1-117">Application Insights Component Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent
Parameter Sets: ComponentObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="07fc1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07fc1-118">-DefaultProfile</span></span>
<span data-ttu-id="07fc1-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="07fc1-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="07fc1-120">-ExportId</span><span class="sxs-lookup"><span data-stu-id="07fc1-120">-ExportId</span></span>
<span data-ttu-id="07fc1-121">Application Insights folyamatos exportálási azonosító.</span><span class="sxs-lookup"><span data-stu-id="07fc1-121">Application Insights Continuous Export Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07fc1-122">-Name</span><span class="sxs-lookup"><span data-stu-id="07fc1-122">-Name</span></span>
<span data-ttu-id="07fc1-123">Application Insights összetevő neve.</span><span class="sxs-lookup"><span data-stu-id="07fc1-123">Application Insights Component Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases: ApplicationInsightsComponentName, ComponentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07fc1-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07fc1-124">-ResourceGroupName</span></span>
<span data-ttu-id="07fc1-125">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="07fc1-125">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07fc1-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="07fc1-126">-ResourceId</span></span>
<span data-ttu-id="07fc1-127">Application Insights összetevő erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="07fc1-127">Application Insights Component Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07fc1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07fc1-128">CommonParameters</span></span>
<span data-ttu-id="07fc1-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07fc1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07fc1-130">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07fc1-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07fc1-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="07fc1-131">INPUTS</span></span>

### <span data-ttu-id="07fc1-132">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="07fc1-132">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="07fc1-133">System.String</span><span class="sxs-lookup"><span data-stu-id="07fc1-133">System.String</span></span>

## <span data-ttu-id="07fc1-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="07fc1-134">OUTPUTS</span></span>

### <span data-ttu-id="07fc1-135">Microsoft.Azure.Commands.ApplicationInsights.Models.PSExportConfiguration</span><span class="sxs-lookup"><span data-stu-id="07fc1-135">Microsoft.Azure.Commands.ApplicationInsights.Models.PSExportConfiguration</span></span>

## <span data-ttu-id="07fc1-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="07fc1-136">NOTES</span></span>

## <span data-ttu-id="07fc1-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="07fc1-137">RELATED LINKS</span></span>
