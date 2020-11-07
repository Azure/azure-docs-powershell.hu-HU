---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/set-azapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsContinuousExport.md
ms.openlocfilehash: 04976e85104c702bb129882e942864f9a5b201ae
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671653"
---
# <span data-ttu-id="467e9-101">Set-AzApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="467e9-101">Set-AzApplicationInsightsContinuousExport</span></span>

## <span data-ttu-id="467e9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="467e9-102">SYNOPSIS</span></span>
<span data-ttu-id="467e9-103">Folyamatos exportálási konfiguráció frissítése egy applciation-elemzést tartalmazó erőforrásban</span><span class="sxs-lookup"><span data-stu-id="467e9-103">Update a continuous export configuration in an applciation insights resource</span></span>

## <span data-ttu-id="467e9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="467e9-104">SYNTAX</span></span>

### <span data-ttu-id="467e9-105">ComponentNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="467e9-105">ComponentNameParameterSet (Default)</span></span>
```
Set-AzApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String> -ExportId <String>
 -DocumentType <String[]> -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String>
 [-DisableConfiguration] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="467e9-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="467e9-106">ComponentObjectParameterSet</span></span>
```
Set-AzApplicationInsightsContinuousExport [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 -ExportId <String> -DocumentType <String[]> -StorageAccountId <String> -StorageLocation <String>
 -StorageSASUri <String> [-DisableConfiguration] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="467e9-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="467e9-107">ResourceIdParameterSet</span></span>
```
Set-AzApplicationInsightsContinuousExport [-ResourceId] <String> -ExportId <String> -DocumentType <String[]>
 -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String> [-DisableConfiguration]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="467e9-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="467e9-108">DESCRIPTION</span></span>
<span data-ttu-id="467e9-109">Folyamatos exportálási konfiguráció frissítése egy applciation-elemzést tartalmazó erőforrásban</span><span class="sxs-lookup"><span data-stu-id="467e9-109">Update a continuous export configuration in an applciation insights resource</span></span>

## <span data-ttu-id="467e9-110">Példák</span><span class="sxs-lookup"><span data-stu-id="467e9-110">EXAMPLES</span></span>

### <span data-ttu-id="467e9-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="467e9-111">Example 1</span></span>
```
PS C:\> $sastoken = New-AzStorageContainerSASToken -Name testcontainer -Context $context -ExpiryTime (Get-Date).AddYears(50) -Permission w
PS C:\> $sasuri = "https://teststorageaccount.blob.core.windows.net/testcontainer" + $sastoken
PS C:\> Set-AzApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test"
 -DocumentTypes "Request","Trace" -ExportId "jlTFEiBg1rkDXOCIeJQ2mB2TxZg=" -DestinationStorageAccountId "/subscriptions/50359d91-7b9d-4823-85af-eb298a61ba96/resourceGroups/testgroup/providers/Microsoft.Storage/storageAccounts/teststorageaccount" -DestinationStorageLocationId sourcecentralus
 -DestinationStorageSASUri $sasuri

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

<span data-ttu-id="467e9-112">A "jlTFEiBg1rkDXOCIeJQ2mB2TxZg =" "teszt" "testgroup" erőforráscsoport "Request" ("Request") és a "trace" "testcontainer" ("teststorageaccount") tárolóba való exportálásához módosítsa a folyamatos exportálási konfigurációt. A SAS-tokennek érvényesnek kell lennie, és írási jogosultsággal kell rendelkeznie a tárolóhoz, máskülönben a folyamatos exportálási funkció nem működik.</span><span class="sxs-lookup"><span data-stu-id="467e9-112">Update continuous export configuration "jlTFEiBg1rkDXOCIeJQ2mB2TxZg=" of resource "test" in resource group "testgroup" to export "Request" and "Trace" documents to storage container "testcontainer" in "teststorageaccount".The SAS token have to be valid and have write permission to the container, otherwise continous export feature won't work.</span></span> <span data-ttu-id="467e9-113">Ha a SAS-token lejárt, a folyamatos exportálás funkció nem fog működni.</span><span class="sxs-lookup"><span data-stu-id="467e9-113">If SAS token expired, the continuous export feature will stop working.</span></span>

## <span data-ttu-id="467e9-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="467e9-114">PARAMETERS</span></span>

### <span data-ttu-id="467e9-115">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="467e9-115">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="467e9-116">Az alkalmazás betekintése összetevő-objektum.</span><span class="sxs-lookup"><span data-stu-id="467e9-116">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="467e9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="467e9-117">-DefaultProfile</span></span>
<span data-ttu-id="467e9-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="467e9-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="467e9-119">-DisableConfiguration</span><span class="sxs-lookup"><span data-stu-id="467e9-119">-DisableConfiguration</span></span>
<span data-ttu-id="467e9-120">Tiltsa le a folyamatos exportálást.</span><span class="sxs-lookup"><span data-stu-id="467e9-120">Disable continuous export or not.</span></span>

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

### <span data-ttu-id="467e9-121">-DocumentType</span><span class="sxs-lookup"><span data-stu-id="467e9-121">-DocumentType</span></span>
<span data-ttu-id="467e9-122">Az exportálni kívánt dokumentumtípusok.</span><span class="sxs-lookup"><span data-stu-id="467e9-122">Document types that need exported.</span></span>

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

### <span data-ttu-id="467e9-123">-ExportId</span><span class="sxs-lookup"><span data-stu-id="467e9-123">-ExportId</span></span>
<span data-ttu-id="467e9-124">Az alkalmazás betekintést nyújt a folyamatos exportálási azonosítóra.</span><span class="sxs-lookup"><span data-stu-id="467e9-124">Application Insights Continuous Export Id.</span></span>

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

### <span data-ttu-id="467e9-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="467e9-125">-Name</span></span>
<span data-ttu-id="467e9-126">Az alkalmazás betekintési összetevőjének neve.</span><span class="sxs-lookup"><span data-stu-id="467e9-126">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="467e9-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="467e9-127">-ResourceGroupName</span></span>
<span data-ttu-id="467e9-128">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="467e9-128">Resource Group Name.</span></span>

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

### <span data-ttu-id="467e9-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="467e9-129">-ResourceId</span></span>
<span data-ttu-id="467e9-130">Az alkalmazás betekintési összetevőjének erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="467e9-130">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="467e9-131">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="467e9-131">-StorageAccountId</span></span>
<span data-ttu-id="467e9-132">Cél-tároló fiók azonosítója.</span><span class="sxs-lookup"><span data-stu-id="467e9-132">Destination Storage Account Id.</span></span>

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

### <span data-ttu-id="467e9-133">-StorageLocation</span><span class="sxs-lookup"><span data-stu-id="467e9-133">-StorageLocation</span></span>
<span data-ttu-id="467e9-134">Hely tárterületének azonosítója</span><span class="sxs-lookup"><span data-stu-id="467e9-134">Destination Storage Location Id.</span></span>

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

### <span data-ttu-id="467e9-135">-StorageSASUri</span><span class="sxs-lookup"><span data-stu-id="467e9-135">-StorageSASUri</span></span>
<span data-ttu-id="467e9-136">Destination Storage SAS URI.</span><span class="sxs-lookup"><span data-stu-id="467e9-136">Destination Storage SAS uri.</span></span>

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

### <span data-ttu-id="467e9-137">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="467e9-137">-Confirm</span></span>
<span data-ttu-id="467e9-138">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="467e9-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="467e9-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="467e9-139">-WhatIf</span></span>
<span data-ttu-id="467e9-140">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="467e9-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="467e9-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="467e9-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="467e9-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="467e9-142">CommonParameters</span></span>
<span data-ttu-id="467e9-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="467e9-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="467e9-144">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="467e9-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="467e9-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="467e9-145">INPUTS</span></span>

### <span data-ttu-id="467e9-146">Microsoft. Azure. Command. ApplicationInsights. models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="467e9-146">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="467e9-147">System. String</span><span class="sxs-lookup"><span data-stu-id="467e9-147">System.String</span></span>

## <span data-ttu-id="467e9-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="467e9-148">OUTPUTS</span></span>

### <span data-ttu-id="467e9-149">Microsoft. Azure. Command. ApplicationInsights. models. PSExportConfiguration</span><span class="sxs-lookup"><span data-stu-id="467e9-149">Microsoft.Azure.Commands.ApplicationInsights.Models.PSExportConfiguration</span></span>

## <span data-ttu-id="467e9-150">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="467e9-150">NOTES</span></span>

## <span data-ttu-id="467e9-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="467e9-151">RELATED LINKS</span></span>
