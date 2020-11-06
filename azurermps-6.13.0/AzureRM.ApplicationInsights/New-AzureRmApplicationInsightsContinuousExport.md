---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/new-azurermapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/New-AzureRmApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/New-AzureRmApplicationInsightsContinuousExport.md
ms.openlocfilehash: 73aa26491a86b0eba01adb3898dba803f1ecf0eb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494207"
---
# <span data-ttu-id="014d2-101">New-AzureRmApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="014d2-101">New-AzureRmApplicationInsightsContinuousExport</span></span>

## <span data-ttu-id="014d2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="014d2-102">SYNOPSIS</span></span>
<span data-ttu-id="014d2-103">Új alkalmazás létrehozása – a folyamatos exportálási konfiguráció létrehozása egy alkalmazás-erőforráshoz</span><span class="sxs-lookup"><span data-stu-id="014d2-103">Create a new application insights continuous export configuration for an application insights resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="014d2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="014d2-104">SYNTAX</span></span>

### <span data-ttu-id="014d2-105">ComponentNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="014d2-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzureRmApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String>
 -DocumentType <String[]> -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="014d2-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="014d2-106">ComponentObjectParameterSet</span></span>
```
New-AzureRmApplicationInsightsContinuousExport [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 -DocumentType <String[]> -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="014d2-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="014d2-107">ResourceIdParameterSet</span></span>
```
New-AzureRmApplicationInsightsContinuousExport [-ResourceId] <String> -DocumentType <String[]>
 -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="014d2-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="014d2-108">DESCRIPTION</span></span>
<span data-ttu-id="014d2-109">Új alkalmazás létrehozása – a folyamatos exportálási konfiguráció létrehozása egy alkalmazás-erőforráshoz</span><span class="sxs-lookup"><span data-stu-id="014d2-109">Create a new application insights continuous export configuration for an application insights resource</span></span>

## <span data-ttu-id="014d2-110">Példák</span><span class="sxs-lookup"><span data-stu-id="014d2-110">EXAMPLES</span></span>

### <span data-ttu-id="014d2-111">Példa 1 új, folyamatos exportálási konfiguráció létrehozása az alkalmazásbeli betekintések erőforrásához</span><span class="sxs-lookup"><span data-stu-id="014d2-111">Example 1 Create a new continuous export configuration for an application insights resource</span></span>
```
PS C:\> $sastoken = New-AzureStorageContainerSASToken -Name testcontainer -Context $context -ExpiryTime (Get-Date).AddYears(50) -Permission w
PS C:\> $sasuri = "https://teststorageaccount.blob.core.windows.net/testcontainer" + $sastoken
PS C:\> New-AzureRmApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test"
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

<span data-ttu-id="014d2-112">Új alkalmazás létrehozása: a folyamatos exportálási konfiguráció exportálása a "Request" és a "trace" dokumentumtípusok "teststorageaccount" a "testgroup" erőforráscsoport "" testcontainer tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="014d2-112">Create a new application insights continuous export configuration to export "Request" and "Trace" document types to storage contain "testcontainer" in storage account "teststorageaccount" in resource group "testgroup".</span></span> <span data-ttu-id="014d2-113">A SAS-tokennek érvényesnek kell lennie, és írási jogosultsággal kell rendelkeznie a tárolóhoz, máskülönben a folyamatos exportálási funkció nem működik. Ha a SAS-token lejárt, a folyamatos exportálás funkció nem fog működni.</span><span class="sxs-lookup"><span data-stu-id="014d2-113">The SAS token have to be valid and have write permission to the container, otherwise continous export feature won't work.If SAS token expired, the continuous export feature will stop working.</span></span>

## <span data-ttu-id="014d2-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="014d2-114">PARAMETERS</span></span>

### <span data-ttu-id="014d2-115">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="014d2-115">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="014d2-116">Az alkalmazás betekintése összetevő-objektum.</span><span class="sxs-lookup"><span data-stu-id="014d2-116">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="014d2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="014d2-117">-DefaultProfile</span></span>
<span data-ttu-id="014d2-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="014d2-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="014d2-119">-DocumentType</span><span class="sxs-lookup"><span data-stu-id="014d2-119">-DocumentType</span></span>
<span data-ttu-id="014d2-120">Az exportálni kívánt dokumentumtípusok.</span><span class="sxs-lookup"><span data-stu-id="014d2-120">Document types that need exported.</span></span>

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

### <span data-ttu-id="014d2-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="014d2-121">-Name</span></span>
<span data-ttu-id="014d2-122">Összetevő neve</span><span class="sxs-lookup"><span data-stu-id="014d2-122">Component Name.</span></span>

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

### <span data-ttu-id="014d2-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="014d2-123">-ResourceGroupName</span></span>
<span data-ttu-id="014d2-124">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="014d2-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="014d2-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="014d2-125">-ResourceId</span></span>
<span data-ttu-id="014d2-126">Az alkalmazás betekintési összetevőjének erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="014d2-126">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="014d2-127">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="014d2-127">-StorageAccountId</span></span>
<span data-ttu-id="014d2-128">Cél-tároló fiók azonosítója.</span><span class="sxs-lookup"><span data-stu-id="014d2-128">Destination Storage Account Id.</span></span>

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

### <span data-ttu-id="014d2-129">-StorageLocation</span><span class="sxs-lookup"><span data-stu-id="014d2-129">-StorageLocation</span></span>
<span data-ttu-id="014d2-130">Hely tárterületének azonosítója</span><span class="sxs-lookup"><span data-stu-id="014d2-130">Destination Storage Location Id.</span></span>

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

### <span data-ttu-id="014d2-131">-StorageSASUri</span><span class="sxs-lookup"><span data-stu-id="014d2-131">-StorageSASUri</span></span>
<span data-ttu-id="014d2-132">Destination Storage SAS URI.</span><span class="sxs-lookup"><span data-stu-id="014d2-132">Destination Storage SAS Uri.</span></span>

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

### <span data-ttu-id="014d2-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="014d2-133">-Confirm</span></span>
<span data-ttu-id="014d2-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="014d2-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="014d2-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="014d2-135">-WhatIf</span></span>
<span data-ttu-id="014d2-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="014d2-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="014d2-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="014d2-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="014d2-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="014d2-138">CommonParameters</span></span>
<span data-ttu-id="014d2-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="014d2-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="014d2-140">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="014d2-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="014d2-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="014d2-141">INPUTS</span></span>

### <span data-ttu-id="014d2-142">Microsoft. Azure. Command. ApplicationInsights. models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="014d2-142">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>
<span data-ttu-id="014d2-143">Paraméterek: ApplicationInsightsComponent (ByValue)</span><span class="sxs-lookup"><span data-stu-id="014d2-143">Parameters: ApplicationInsightsComponent (ByValue)</span></span>

### <span data-ttu-id="014d2-144">System. String</span><span class="sxs-lookup"><span data-stu-id="014d2-144">System.String</span></span>

## <span data-ttu-id="014d2-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="014d2-145">OUTPUTS</span></span>

### <span data-ttu-id="014d2-146">Microsoft. Azure. Command. ApplicationInsights. models. PSExportConfiguration</span><span class="sxs-lookup"><span data-stu-id="014d2-146">Microsoft.Azure.Commands.ApplicationInsights.Models.PSExportConfiguration</span></span>

## <span data-ttu-id="014d2-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="014d2-147">NOTES</span></span>

## <span data-ttu-id="014d2-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="014d2-148">RELATED LINKS</span></span>
