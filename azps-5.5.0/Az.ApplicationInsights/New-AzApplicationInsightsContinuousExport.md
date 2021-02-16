---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/new-azapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsightsContinuousExport.md
ms.openlocfilehash: 97994eb9898f5eca3e8f7f3015e2ce96845d5c24
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100149506"
---
# <span data-ttu-id="3a8c3-101">New-AzApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="3a8c3-101">New-AzApplicationInsightsContinuousExport</span></span>

## <span data-ttu-id="3a8c3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a8c3-102">SYNOPSIS</span></span>
<span data-ttu-id="3a8c3-103">Új alkalmazás-betekintések folyamatos exportálási konfigurációjának létrehozása alkalmazásstatékony erőforrásokhoz</span><span class="sxs-lookup"><span data-stu-id="3a8c3-103">Create a new application insights continuous export configuration for an application insights resource</span></span>

## <span data-ttu-id="3a8c3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="3a8c3-104">SYNTAX</span></span>

### <span data-ttu-id="3a8c3-105">ComponentNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3a8c3-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String>
 -DocumentType <String[]> -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a8c3-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3a8c3-106">ComponentObjectParameterSet</span></span>
```
New-AzApplicationInsightsContinuousExport [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 -DocumentType <String[]> -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a8c3-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3a8c3-107">ResourceIdParameterSet</span></span>
```
New-AzApplicationInsightsContinuousExport [-ResourceId] <String> -DocumentType <String[]>
 -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a8c3-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="3a8c3-108">DESCRIPTION</span></span>
<span data-ttu-id="3a8c3-109">Új alkalmazásstatikációk folyamatos exportálási konfigurációjának létrehozása alkalmazásstatékony erőforrásokhoz</span><span class="sxs-lookup"><span data-stu-id="3a8c3-109">Create a new application insights continuous export configuration for an application insights resource</span></span>

## <span data-ttu-id="3a8c3-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="3a8c3-110">EXAMPLES</span></span>

### <span data-ttu-id="3a8c3-111">1. példa: Új folyamatos exportálási konfiguráció létrehozása alkalmazásstatékony erőforráshoz</span><span class="sxs-lookup"><span data-stu-id="3a8c3-111">Example 1 Create a new continuous export configuration for an application insights resource</span></span>
```
PS C:\> $sastoken = New-AzStorageContainerSASToken -Name testcontainer -Context $context -ExpiryTime (Get-Date).AddYears(50) -Permission w
PS C:\> $sasuri = "https://teststorageaccount.blob.core.windows.net/testcontainer" + $sastoken
PS C:\> New-AzApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test"
 -DocumentType "Request","Trace", "Custom Event" -StorageAccountId "/subscriptions/50359d91-7b9d-4823-85af-eb298a61ba96/resourceGroups/testgroup/providers/Microsoft.Storage/storageAccounts/teststorageaccount" -StorageLocation sourcecentralus
 -StorageSASUri $sasuri

ExportId                         : jlTFEiBg1rkDXOCIeJQ2mB2TxZg=
StorageName                      : teststorageaccount
ContainerName                    : testcontainer
DocumentTypes                    : Request, Custom Event, Trace
DestinationStorageSubscriptionId : 50359d91-7b9d-4823-85af-eb298a61ba96
DestinationStorageLocationId     : sourcecentralus
DestinationStorageAccountId      : /subscriptions/50359d91-7b9d-4823-85af-eb298a61ba96/resourceGroups/testgroup/providers/Microsoft.Storage/storageAccounts/teststorageaccount
IsEnabled                        : True
ExportStatus                     : Preparing
LastSuccessTime                  :
```

<span data-ttu-id="3a8c3-112">Hozzon létre egy új alkalmazáselemzési folyamatos exportálási konfigurációt a "Request" és a "Trace" (Kérés) és a "Trace" (Dokumentumtípusok nyomon követésének) exportálásához, hogy a "testcontainer" tárolófiók "testtorageaccount" "testgroup" erőforráscsoportjában "testcontainer" tárolóhelyet tartalmazzanak.</span><span class="sxs-lookup"><span data-stu-id="3a8c3-112">Create a new application insights continuous export configuration to export "Request" and "Trace" document types to storage contain "testcontainer" in storage account "teststorageaccount" in resource group "testgroup".</span></span> <span data-ttu-id="3a8c3-113">Az SAS-jogkivonatnak érvényesnek és írási engedéllyel kell rendelkeznie a tárolóhoz, ellenkező esetben a folyamatos exportálási funkció nem fog működni. Ha lejárt az SAS-jogkivonat, a folyamatos exportálási funkció leáll.</span><span class="sxs-lookup"><span data-stu-id="3a8c3-113">The SAS token have to be valid and have write permission to the container, otherwise continuous export feature won't work.If SAS token expired, the continuous export feature will stop working.</span></span>

## <span data-ttu-id="3a8c3-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3a8c3-114">PARAMETERS</span></span>

### <span data-ttu-id="3a8c3-115">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="3a8c3-115">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="3a8c3-116">Application Insights összetevő-objektum.</span><span class="sxs-lookup"><span data-stu-id="3a8c3-116">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="3a8c3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a8c3-117">-DefaultProfile</span></span>
<span data-ttu-id="3a8c3-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3a8c3-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3a8c3-119">-DocumentType</span><span class="sxs-lookup"><span data-stu-id="3a8c3-119">-DocumentType</span></span>
<span data-ttu-id="3a8c3-120">Exportálni szükséges dokumentumtípusok.</span><span class="sxs-lookup"><span data-stu-id="3a8c3-120">Document types that need exported.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: Request, Exception, Custom Event, Trace, Metric, Page Load, Page View, Dependency, Availability, Performance Counter

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a8c3-121">-Name</span><span class="sxs-lookup"><span data-stu-id="3a8c3-121">-Name</span></span>
<span data-ttu-id="3a8c3-122">Összetevő neve.</span><span class="sxs-lookup"><span data-stu-id="3a8c3-122">Component Name.</span></span>

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

### <span data-ttu-id="3a8c3-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a8c3-123">-ResourceGroupName</span></span>
<span data-ttu-id="3a8c3-124">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="3a8c3-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="3a8c3-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3a8c3-125">-ResourceId</span></span>
<span data-ttu-id="3a8c3-126">Application Insights összetevő erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="3a8c3-126">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="3a8c3-127">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="3a8c3-127">-StorageAccountId</span></span>
<span data-ttu-id="3a8c3-128">Céltárolófiók azonosítója.</span><span class="sxs-lookup"><span data-stu-id="3a8c3-128">Destination Storage Account Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a8c3-129">-StorageLocation</span><span class="sxs-lookup"><span data-stu-id="3a8c3-129">-StorageLocation</span></span>
<span data-ttu-id="3a8c3-130">Célhely helyének azonosítója.</span><span class="sxs-lookup"><span data-stu-id="3a8c3-130">Destination Storage Location Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a8c3-131">-StorageSASUri</span><span class="sxs-lookup"><span data-stu-id="3a8c3-131">-StorageSASUri</span></span>
<span data-ttu-id="3a8c3-132">Destination Storage SAS Uri.</span><span class="sxs-lookup"><span data-stu-id="3a8c3-132">Destination Storage SAS Uri.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a8c3-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3a8c3-133">-Confirm</span></span>
<span data-ttu-id="3a8c3-134">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="3a8c3-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a8c3-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a8c3-135">-WhatIf</span></span>
<span data-ttu-id="3a8c3-136">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="3a8c3-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3a8c3-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3a8c3-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a8c3-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a8c3-138">CommonParameters</span></span>
<span data-ttu-id="3a8c3-139">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a8c3-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a8c3-140">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a8c3-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a8c3-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3a8c3-141">INPUTS</span></span>

### <span data-ttu-id="3a8c3-142">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="3a8c3-142">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="3a8c3-143">System.String</span><span class="sxs-lookup"><span data-stu-id="3a8c3-143">System.String</span></span>

## <span data-ttu-id="3a8c3-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3a8c3-144">OUTPUTS</span></span>

### <span data-ttu-id="3a8c3-145">Microsoft.Azure.Commands.ApplicationInsights.Models.PSExportConfiguration</span><span class="sxs-lookup"><span data-stu-id="3a8c3-145">Microsoft.Azure.Commands.ApplicationInsights.Models.PSExportConfiguration</span></span>

## <span data-ttu-id="3a8c3-146">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="3a8c3-146">NOTES</span></span>

## <span data-ttu-id="3a8c3-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3a8c3-147">RELATED LINKS</span></span>
