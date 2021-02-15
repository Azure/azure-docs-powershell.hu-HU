---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/set-azapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsContinuousExport.md
ms.openlocfilehash: fef34358855666d0f407c72831b2973ce95cc7e9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100168482"
---
# <span data-ttu-id="60fb4-101">Set-AzApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="60fb4-101">Set-AzApplicationInsightsContinuousExport</span></span>

## <span data-ttu-id="60fb4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="60fb4-102">SYNOPSIS</span></span>
<span data-ttu-id="60fb4-103">Folyamatos exportálási konfiguráció frissítése alkalmazásstatékony erőforrásban</span><span class="sxs-lookup"><span data-stu-id="60fb4-103">Update a continuous export configuration in an application insights resource</span></span>

## <span data-ttu-id="60fb4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="60fb4-104">SYNTAX</span></span>

### <span data-ttu-id="60fb4-105">ComponentNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="60fb4-105">ComponentNameParameterSet (Default)</span></span>
```
Set-AzApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String> -ExportId <String>
 -DocumentType <String[]> -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String>
 [-DisableConfiguration] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60fb4-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="60fb4-106">ComponentObjectParameterSet</span></span>
```
Set-AzApplicationInsightsContinuousExport [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 -ExportId <String> -DocumentType <String[]> -StorageAccountId <String> -StorageLocation <String>
 -StorageSASUri <String> [-DisableConfiguration] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60fb4-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="60fb4-107">ResourceIdParameterSet</span></span>
```
Set-AzApplicationInsightsContinuousExport [-ResourceId] <String> -ExportId <String> -DocumentType <String[]>
 -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String> [-DisableConfiguration]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60fb4-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="60fb4-108">DESCRIPTION</span></span>
<span data-ttu-id="60fb4-109">Folyamatos exportálási konfiguráció frissítése alkalmazásstatékony erőforrásban</span><span class="sxs-lookup"><span data-stu-id="60fb4-109">Update a continuous export configuration in an application insights resource</span></span>

## <span data-ttu-id="60fb4-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="60fb4-110">EXAMPLES</span></span>

### <span data-ttu-id="60fb4-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="60fb4-111">Example 1</span></span>
```
PS C:\> $sastoken = New-AzStorageContainerSASToken -Name testcontainer -Context $context -ExpiryTime (Get-Date).AddYears(50) -Permission w
PS C:\> $sasuri = "https://teststorageaccount.blob.core.windows.net/testcontainer" + $sastoken
PS C:\> Set-AzApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test"
 -DocumentTypes "Request","Trace" -ExportId "jlTFEiBg1rkDXOCIeJQ2mB2TxZg=" -StorageAccountId "/subscriptions/50359d91-7b9d-4823-85af-eb298a61ba96/resourceGroups/testgroup/providers/Microsoft.Storage/storageAccounts/teststorageaccount" -StorageLocation sourcecentralus
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

<span data-ttu-id="60fb4-112">Frissítse a "testgroup" erőforráscsoport "tesztcsoport" erőforráscsoportjában a "tesztcsoport" "jlTFEiBg1rkDXOCIeJQ2mB2TxZg=" folyamatos exportálási konfigurációját, és exportálja a "Request" és a "Trace" dokumentumokat a "testcontainer" tárolóba a "testtorageaccount" csoportban. Az SAS-jogkivonatnak érvényesnek és írási engedéllyel kell rendelkeznie a tárolóhoz, ellenkező esetben a folyamatos exportálási funkció nem fog működni.</span><span class="sxs-lookup"><span data-stu-id="60fb4-112">Update continuous export configuration "jlTFEiBg1rkDXOCIeJQ2mB2TxZg=" of resource "test" in resource group "testgroup" to export "Request" and "Trace" documents to storage container "testcontainer" in "teststorageaccount".The SAS token have to be valid and have write permission to the container, otherwise continuous export feature won't work.</span></span> <span data-ttu-id="60fb4-113">Ha lejárt az SAS-jogkivonat, a folyamatos exportálási funkció leáll.</span><span class="sxs-lookup"><span data-stu-id="60fb4-113">If SAS token expired, the continuous export feature will stop working.</span></span>

## <span data-ttu-id="60fb4-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="60fb4-114">PARAMETERS</span></span>

### <span data-ttu-id="60fb4-115">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="60fb4-115">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="60fb4-116">Application Insights összetevő-objektum.</span><span class="sxs-lookup"><span data-stu-id="60fb4-116">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="60fb4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60fb4-117">-DefaultProfile</span></span>
<span data-ttu-id="60fb4-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="60fb4-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="60fb4-119">-DisableConfiguration</span><span class="sxs-lookup"><span data-stu-id="60fb4-119">-DisableConfiguration</span></span>
<span data-ttu-id="60fb4-120">Tiltsa le a folyamatos exportálást.</span><span class="sxs-lookup"><span data-stu-id="60fb4-120">Disable continuous export or not.</span></span>

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

### <span data-ttu-id="60fb4-121">-DocumentType</span><span class="sxs-lookup"><span data-stu-id="60fb4-121">-DocumentType</span></span>
<span data-ttu-id="60fb4-122">Exportálni szükséges dokumentumtípusok.</span><span class="sxs-lookup"><span data-stu-id="60fb4-122">Document types that need exported.</span></span>

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

### <span data-ttu-id="60fb4-123">-ExportId</span><span class="sxs-lookup"><span data-stu-id="60fb4-123">-ExportId</span></span>
<span data-ttu-id="60fb4-124">Application Insights folyamatos exportálási azonosító.</span><span class="sxs-lookup"><span data-stu-id="60fb4-124">Application Insights Continuous Export Id.</span></span>

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

### <span data-ttu-id="60fb4-125">-Name</span><span class="sxs-lookup"><span data-stu-id="60fb4-125">-Name</span></span>
<span data-ttu-id="60fb4-126">Application Insights összetevő neve.</span><span class="sxs-lookup"><span data-stu-id="60fb4-126">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="60fb4-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60fb4-127">-ResourceGroupName</span></span>
<span data-ttu-id="60fb4-128">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="60fb4-128">Resource Group Name.</span></span>

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

### <span data-ttu-id="60fb4-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="60fb4-129">-ResourceId</span></span>
<span data-ttu-id="60fb4-130">Application Insights összetevő erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="60fb4-130">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="60fb4-131">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="60fb4-131">-StorageAccountId</span></span>
<span data-ttu-id="60fb4-132">Céltárolófiók azonosítója.</span><span class="sxs-lookup"><span data-stu-id="60fb4-132">Destination Storage Account Id.</span></span>

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

### <span data-ttu-id="60fb4-133">-StorageLocation</span><span class="sxs-lookup"><span data-stu-id="60fb4-133">-StorageLocation</span></span>
<span data-ttu-id="60fb4-134">Célhely helyének azonosítója.</span><span class="sxs-lookup"><span data-stu-id="60fb4-134">Destination Storage Location Id.</span></span>

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

### <span data-ttu-id="60fb4-135">-StorageSASUri</span><span class="sxs-lookup"><span data-stu-id="60fb4-135">-StorageSASUri</span></span>
<span data-ttu-id="60fb4-136">Destination Storage SAS uri.</span><span class="sxs-lookup"><span data-stu-id="60fb4-136">Destination Storage SAS uri.</span></span>

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

### <span data-ttu-id="60fb4-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="60fb4-137">-Confirm</span></span>
<span data-ttu-id="60fb4-138">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="60fb4-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60fb4-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60fb4-139">-WhatIf</span></span>
<span data-ttu-id="60fb4-140">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="60fb4-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="60fb4-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="60fb4-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60fb4-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60fb4-142">CommonParameters</span></span>
<span data-ttu-id="60fb4-143">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60fb4-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60fb4-144">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60fb4-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60fb4-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="60fb4-145">INPUTS</span></span>

### <span data-ttu-id="60fb4-146">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="60fb4-146">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="60fb4-147">System.String</span><span class="sxs-lookup"><span data-stu-id="60fb4-147">System.String</span></span>

## <span data-ttu-id="60fb4-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="60fb4-148">OUTPUTS</span></span>

### <span data-ttu-id="60fb4-149">Microsoft.Azure.Commands.ApplicationInsights.Models.PSExportConfiguration</span><span class="sxs-lookup"><span data-stu-id="60fb4-149">Microsoft.Azure.Commands.ApplicationInsights.Models.PSExportConfiguration</span></span>

## <span data-ttu-id="60fb4-150">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="60fb4-150">NOTES</span></span>

## <span data-ttu-id="60fb4-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="60fb4-151">RELATED LINKS</span></span>
