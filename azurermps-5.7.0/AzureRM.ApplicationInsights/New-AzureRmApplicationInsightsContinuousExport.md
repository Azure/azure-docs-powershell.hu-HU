---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/new-azurermapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/New-AzureRmApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/New-AzureRmApplicationInsightsContinuousExport.md
ms.openlocfilehash: 1e4dd5f65789751f9a28deb9e10c37221f45b97b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679301"
---
# <span data-ttu-id="caccb-101">New-AzureRmApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="caccb-101">New-AzureRmApplicationInsightsContinuousExport</span></span>

## <span data-ttu-id="caccb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="caccb-102">SYNOPSIS</span></span>
<span data-ttu-id="caccb-103">Új alkalmazás létrehozása – a folyamatos exportálási konfiguráció létrehozása egy alkalmazás-erőforráshoz</span><span class="sxs-lookup"><span data-stu-id="caccb-103">Create a new application insights continuous export configuration for an application insights resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="caccb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="caccb-104">SYNTAX</span></span>

### <span data-ttu-id="caccb-105">ComponentNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="caccb-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzureRmApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String>
 -DocumentType <String[]> -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="caccb-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="caccb-106">ComponentObjectParameterSet</span></span>
```
New-AzureRmApplicationInsightsContinuousExport [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 -DocumentType <String[]> -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="caccb-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="caccb-107">ResourceIdParameterSet</span></span>
```
New-AzureRmApplicationInsightsContinuousExport [-ResourceId] <String> -DocumentType <String[]>
 -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="caccb-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="caccb-108">DESCRIPTION</span></span>
<span data-ttu-id="caccb-109">Új alkalmazás létrehozása – a folyamatos exportálási konfiguráció létrehozása egy alkalmazás-erőforráshoz</span><span class="sxs-lookup"><span data-stu-id="caccb-109">Create a new application insights continuous export configuration for an application insights resource</span></span>

## <span data-ttu-id="caccb-110">Példák</span><span class="sxs-lookup"><span data-stu-id="caccb-110">EXAMPLES</span></span>

### <span data-ttu-id="caccb-111">Példa 1 új, folyamatos exportálási konfiguráció létrehozása az alkalmazásbeli betekintések erőforrásához</span><span class="sxs-lookup"><span data-stu-id="caccb-111">Example 1 Create a new continuous export configuration for an application insights resource</span></span>
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

<span data-ttu-id="caccb-112">Új alkalmazás létrehozása: a folyamatos exportálási konfiguráció exportálása a "Request" és a "trace" dokumentumtípusok "teststorageaccount" a "testgroup" erőforráscsoport "" testcontainer tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="caccb-112">Create a new application insights continuous export configuration to export "Request" and "Trace" document types to storage contain "testcontainer" in storage account "teststorageaccount" in resource group "testgroup".</span></span> <span data-ttu-id="caccb-113">A SAS-tokennek érvényesnek kell lennie, és írási jogosultsággal kell rendelkeznie a tárolóhoz, máskülönben a folyamatos exportálási funkció nem működik. Ha a SAS-token lejárt, a folyamatos exportálás funkció nem fog működni.</span><span class="sxs-lookup"><span data-stu-id="caccb-113">The SAS token have to be valid and have write permission to the container, otherwise continous export feature won't work.If SAS token expired, the continuous export feature will stop working.</span></span>

## <span data-ttu-id="caccb-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="caccb-114">PARAMETERS</span></span>

### <span data-ttu-id="caccb-115">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="caccb-115">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="caccb-116">Az alkalmazás betekintése összetevő-objektum.</span><span class="sxs-lookup"><span data-stu-id="caccb-116">Application Insights Component Object.</span></span>

```yaml
Type: PSApplicationInsightsComponent
Parameter Sets: ComponentObjectParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="caccb-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="caccb-117">-Confirm</span></span>
<span data-ttu-id="caccb-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="caccb-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="caccb-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="caccb-119">-DefaultProfile</span></span>
<span data-ttu-id="caccb-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="caccb-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="caccb-121">-DocumentType</span><span class="sxs-lookup"><span data-stu-id="caccb-121">-DocumentType</span></span>
<span data-ttu-id="caccb-122">Az exportálni kívánt dokumentumtípusok.</span><span class="sxs-lookup"><span data-stu-id="caccb-122">Document types that need exported.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 
Accepted values: Request, Exception, Custom Event, Trace, Metric, Page Load, Page View, Dependency, Availability, Performance Counter

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="caccb-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="caccb-123">-Name</span></span>
<span data-ttu-id="caccb-124">Összetevő neve</span><span class="sxs-lookup"><span data-stu-id="caccb-124">Component Name.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: ApplicationInsightsComponentName, ComponentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="caccb-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="caccb-125">-ResourceGroupName</span></span>
<span data-ttu-id="caccb-126">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="caccb-126">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="caccb-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="caccb-127">-ResourceId</span></span>
<span data-ttu-id="caccb-128">Az alkalmazás betekintési összetevőjének erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="caccb-128">Application Insights Component Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="caccb-129">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="caccb-129">-StorageAccountId</span></span>
<span data-ttu-id="caccb-130">Cél-tároló fiók azonosítója.</span><span class="sxs-lookup"><span data-stu-id="caccb-130">Destination Storage Account Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="caccb-131">-StorageLocation</span><span class="sxs-lookup"><span data-stu-id="caccb-131">-StorageLocation</span></span>
<span data-ttu-id="caccb-132">Hely tárterületének azonosítója</span><span class="sxs-lookup"><span data-stu-id="caccb-132">Destination Storage Location Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="caccb-133">-StorageSASUri</span><span class="sxs-lookup"><span data-stu-id="caccb-133">-StorageSASUri</span></span>
<span data-ttu-id="caccb-134">Destination Storage SAS URI.</span><span class="sxs-lookup"><span data-stu-id="caccb-134">Destination Storage SAS Uri.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="caccb-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="caccb-135">-WhatIf</span></span>
<span data-ttu-id="caccb-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="caccb-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="caccb-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="caccb-137">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="caccb-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="caccb-138">CommonParameters</span></span>
<span data-ttu-id="caccb-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="caccb-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="caccb-140">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="caccb-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="caccb-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="caccb-141">INPUTS</span></span>

### <span data-ttu-id="caccb-142">System. String</span><span class="sxs-lookup"><span data-stu-id="caccb-142">System.String</span></span>
<span data-ttu-id="caccb-143">System. string []</span><span class="sxs-lookup"><span data-stu-id="caccb-143">System.String[]</span></span>

## <span data-ttu-id="caccb-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="caccb-144">OUTPUTS</span></span>

### <span data-ttu-id="caccb-145">Microsoft. Azure. Command. ApplicationInsights. models. PSExportConfiguration</span><span class="sxs-lookup"><span data-stu-id="caccb-145">Microsoft.Azure.Commands.ApplicationInsights.Models.PSExportConfiguration</span></span>

## <span data-ttu-id="caccb-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="caccb-146">NOTES</span></span>

## <span data-ttu-id="caccb-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="caccb-147">RELATED LINKS</span></span>

