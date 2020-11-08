---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/new-azapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsightsContinuousExport.md
ms.openlocfilehash: 97994eb9898f5eca3e8f7f3015e2ce96845d5c24
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024231"
---
# <span data-ttu-id="2c4e7-101">New-AzApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="2c4e7-101">New-AzApplicationInsightsContinuousExport</span></span>

## <span data-ttu-id="2c4e7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2c4e7-102">SYNOPSIS</span></span>
<span data-ttu-id="2c4e7-103">Új alkalmazás létrehozása – a folyamatos exportálási konfiguráció létrehozása egy alkalmazás-erőforráshoz</span><span class="sxs-lookup"><span data-stu-id="2c4e7-103">Create a new application insights continuous export configuration for an application insights resource</span></span>

## <span data-ttu-id="2c4e7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2c4e7-104">SYNTAX</span></span>

### <span data-ttu-id="2c4e7-105">ComponentNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2c4e7-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String>
 -DocumentType <String[]> -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c4e7-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2c4e7-106">ComponentObjectParameterSet</span></span>
```
New-AzApplicationInsightsContinuousExport [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 -DocumentType <String[]> -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c4e7-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2c4e7-107">ResourceIdParameterSet</span></span>
```
New-AzApplicationInsightsContinuousExport [-ResourceId] <String> -DocumentType <String[]>
 -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c4e7-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="2c4e7-108">DESCRIPTION</span></span>
<span data-ttu-id="2c4e7-109">Új alkalmazás létrehozása – a folyamatos exportálási konfiguráció létrehozása egy alkalmazás-erőforráshoz</span><span class="sxs-lookup"><span data-stu-id="2c4e7-109">Create a new application insights continuous export configuration for an application insights resource</span></span>

## <span data-ttu-id="2c4e7-110">Példák</span><span class="sxs-lookup"><span data-stu-id="2c4e7-110">EXAMPLES</span></span>

### <span data-ttu-id="2c4e7-111">Példa 1 új, folyamatos exportálási konfiguráció létrehozása az alkalmazásbeli betekintések erőforrásához</span><span class="sxs-lookup"><span data-stu-id="2c4e7-111">Example 1 Create a new continuous export configuration for an application insights resource</span></span>
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

<span data-ttu-id="2c4e7-112">Új alkalmazás létrehozása: a folyamatos exportálási konfiguráció exportálása a "Request" és a "trace" dokumentumtípusok "teststorageaccount" a "testgroup" erőforráscsoport "" testcontainer tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="2c4e7-112">Create a new application insights continuous export configuration to export "Request" and "Trace" document types to storage contain "testcontainer" in storage account "teststorageaccount" in resource group "testgroup".</span></span> <span data-ttu-id="2c4e7-113">A SAS-tokennek érvényesnek kell lennie, és írási engedéllyel kell rendelkeznie a tárolóhoz, máskülönben a folyamatos exportálási funkció nem működik. Ha a SAS-token lejárt, a folyamatos exportálás funkció nem fog működni.</span><span class="sxs-lookup"><span data-stu-id="2c4e7-113">The SAS token have to be valid and have write permission to the container, otherwise continuous export feature won't work.If SAS token expired, the continuous export feature will stop working.</span></span>

## <span data-ttu-id="2c4e7-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2c4e7-114">PARAMETERS</span></span>

### <span data-ttu-id="2c4e7-115">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="2c4e7-115">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="2c4e7-116">Az alkalmazás betekintése összetevő-objektum.</span><span class="sxs-lookup"><span data-stu-id="2c4e7-116">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="2c4e7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c4e7-117">-DefaultProfile</span></span>
<span data-ttu-id="2c4e7-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2c4e7-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2c4e7-119">-DocumentType</span><span class="sxs-lookup"><span data-stu-id="2c4e7-119">-DocumentType</span></span>
<span data-ttu-id="2c4e7-120">Az exportálni kívánt dokumentumtípusok.</span><span class="sxs-lookup"><span data-stu-id="2c4e7-120">Document types that need exported.</span></span>

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

### <span data-ttu-id="2c4e7-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2c4e7-121">-Name</span></span>
<span data-ttu-id="2c4e7-122">Összetevő neve</span><span class="sxs-lookup"><span data-stu-id="2c4e7-122">Component Name.</span></span>

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

### <span data-ttu-id="2c4e7-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c4e7-123">-ResourceGroupName</span></span>
<span data-ttu-id="2c4e7-124">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="2c4e7-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="2c4e7-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2c4e7-125">-ResourceId</span></span>
<span data-ttu-id="2c4e7-126">Az alkalmazás betekintési összetevőjének erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="2c4e7-126">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="2c4e7-127">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="2c4e7-127">-StorageAccountId</span></span>
<span data-ttu-id="2c4e7-128">Cél-tároló fiók azonosítója.</span><span class="sxs-lookup"><span data-stu-id="2c4e7-128">Destination Storage Account Id.</span></span>

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

### <span data-ttu-id="2c4e7-129">-StorageLocation</span><span class="sxs-lookup"><span data-stu-id="2c4e7-129">-StorageLocation</span></span>
<span data-ttu-id="2c4e7-130">Hely tárterületének azonosítója</span><span class="sxs-lookup"><span data-stu-id="2c4e7-130">Destination Storage Location Id.</span></span>

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

### <span data-ttu-id="2c4e7-131">-StorageSASUri</span><span class="sxs-lookup"><span data-stu-id="2c4e7-131">-StorageSASUri</span></span>
<span data-ttu-id="2c4e7-132">Destination Storage SAS URI.</span><span class="sxs-lookup"><span data-stu-id="2c4e7-132">Destination Storage SAS Uri.</span></span>

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

### <span data-ttu-id="2c4e7-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2c4e7-133">-Confirm</span></span>
<span data-ttu-id="2c4e7-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2c4e7-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c4e7-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c4e7-135">-WhatIf</span></span>
<span data-ttu-id="2c4e7-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2c4e7-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2c4e7-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2c4e7-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c4e7-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c4e7-138">CommonParameters</span></span>
<span data-ttu-id="2c4e7-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2c4e7-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c4e7-140">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c4e7-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c4e7-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2c4e7-141">INPUTS</span></span>

### <span data-ttu-id="2c4e7-142">Microsoft. Azure. Command. ApplicationInsights. models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="2c4e7-142">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="2c4e7-143">System. String</span><span class="sxs-lookup"><span data-stu-id="2c4e7-143">System.String</span></span>

## <span data-ttu-id="2c4e7-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2c4e7-144">OUTPUTS</span></span>

### <span data-ttu-id="2c4e7-145">Microsoft. Azure. Command. ApplicationInsights. models. PSExportConfiguration</span><span class="sxs-lookup"><span data-stu-id="2c4e7-145">Microsoft.Azure.Commands.ApplicationInsights.Models.PSExportConfiguration</span></span>

## <span data-ttu-id="2c4e7-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2c4e7-146">NOTES</span></span>

## <span data-ttu-id="2c4e7-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2c4e7-147">RELATED LINKS</span></span>
