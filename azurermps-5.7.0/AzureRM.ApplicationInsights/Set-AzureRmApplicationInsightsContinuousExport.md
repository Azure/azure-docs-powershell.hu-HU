---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/set-azurermapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Set-AzureRmApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Set-AzureRmApplicationInsightsContinuousExport.md
ms.openlocfilehash: 7b426f7f6b494c92d86a41217000b2d2335c7d91
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502640"
---
# <span data-ttu-id="178c4-101">Set-AzureRmApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="178c4-101">Set-AzureRmApplicationInsightsContinuousExport</span></span>

## <span data-ttu-id="178c4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="178c4-102">SYNOPSIS</span></span>
<span data-ttu-id="178c4-103">Folyamatos exportálási konfiguráció frissítése egy applciation-elemzést tartalmazó erőforrásban</span><span class="sxs-lookup"><span data-stu-id="178c4-103">Update a continuous export configuration in an applciation insights resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="178c4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="178c4-104">SYNTAX</span></span>

### <span data-ttu-id="178c4-105">ComponentNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="178c4-105">ComponentNameParameterSet (Default)</span></span>
```
Set-AzureRmApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String>
 -ExportId <String> -DocumentType <String[]> -StorageAccountId <String> -StorageLocation <String>
 -StorageSASUri <String> [-DisableConfiguration] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="178c4-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="178c4-106">ComponentObjectParameterSet</span></span>
```
Set-AzureRmApplicationInsightsContinuousExport [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 -ExportId <String> -DocumentType <String[]> -StorageAccountId <String> -StorageLocation <String>
 -StorageSASUri <String> [-DisableConfiguration] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="178c4-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="178c4-107">ResourceIdParameterSet</span></span>
```
Set-AzureRmApplicationInsightsContinuousExport [-ResourceId] <String> -ExportId <String>
 -DocumentType <String[]> -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String>
 [-DisableConfiguration] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="178c4-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="178c4-108">DESCRIPTION</span></span>
<span data-ttu-id="178c4-109">Folyamatos exportálási konfiguráció frissítése egy applciation-elemzést tartalmazó erőforrásban</span><span class="sxs-lookup"><span data-stu-id="178c4-109">Update a continuous export configuration in an applciation insights resource</span></span>

## <span data-ttu-id="178c4-110">Példák</span><span class="sxs-lookup"><span data-stu-id="178c4-110">EXAMPLES</span></span>

### <span data-ttu-id="178c4-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="178c4-111">Example 1</span></span>
```
PS C:\> $sastoken = New-AzureStorageContainerSASToken -Name testcontainer -Context $context -ExpiryTime (Get-Date).AddYears(50) -Permission w
PS C:\> $sasuri = "https://teststorageaccount.blob.core.windows.net/testcontainer" + $sastoken
PS C:\> Set-AzureRmApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test"
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

<span data-ttu-id="178c4-112">A "jlTFEiBg1rkDXOCIeJQ2mB2TxZg =" "teszt" "testgroup" erőforráscsoport "Request" ("Request") és a "trace" "testcontainer" ("teststorageaccount") tárolóba való exportálásához módosítsa a folyamatos exportálási konfigurációt. A SAS-tokennek érvényesnek kell lennie, és írási jogosultsággal kell rendelkeznie a tárolóhoz, máskülönben a folyamatos exportálási funkció nem működik.</span><span class="sxs-lookup"><span data-stu-id="178c4-112">Update continuous export configuration "jlTFEiBg1rkDXOCIeJQ2mB2TxZg=" of resource "test" in resource group "testgroup" to export "Request" and "Trace" documents to storage container "testcontainer" in "teststorageaccount".The SAS token have to be valid and have write permission to the container, otherwise continous export feature won't work.</span></span> <span data-ttu-id="178c4-113">Ha a SAS-token lejárt, a folyamatos exportálás funkció nem fog működni.</span><span class="sxs-lookup"><span data-stu-id="178c4-113">If SAS token expired, the continuous export feature will stop working.</span></span>

## <span data-ttu-id="178c4-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="178c4-114">PARAMETERS</span></span>

### <span data-ttu-id="178c4-115">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="178c4-115">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="178c4-116">Az alkalmazás betekintése összetevő-objektum.</span><span class="sxs-lookup"><span data-stu-id="178c4-116">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="178c4-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="178c4-117">-Confirm</span></span>
<span data-ttu-id="178c4-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="178c4-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="178c4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="178c4-119">-DefaultProfile</span></span>
<span data-ttu-id="178c4-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="178c4-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="178c4-121">-DisableConfiguration</span><span class="sxs-lookup"><span data-stu-id="178c4-121">-DisableConfiguration</span></span>
<span data-ttu-id="178c4-122">Tiltsa le a folyamatos exportálást.</span><span class="sxs-lookup"><span data-stu-id="178c4-122">Disable continuous export or not.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="178c4-123">-DocumentType</span><span class="sxs-lookup"><span data-stu-id="178c4-123">-DocumentType</span></span>
<span data-ttu-id="178c4-124">Az exportálni kívánt dokumentumtípusok.</span><span class="sxs-lookup"><span data-stu-id="178c4-124">Document types that need exported.</span></span>

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

### <span data-ttu-id="178c4-125">-ExportId</span><span class="sxs-lookup"><span data-stu-id="178c4-125">-ExportId</span></span>
<span data-ttu-id="178c4-126">Az alkalmazás betekintést nyújt a folyamatos exportálási azonosítóra.</span><span class="sxs-lookup"><span data-stu-id="178c4-126">Application Insights Continuous Export Id.</span></span>

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

### <span data-ttu-id="178c4-127">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="178c4-127">-Name</span></span>
<span data-ttu-id="178c4-128">Az alkalmazás betekintési összetevőjének neve.</span><span class="sxs-lookup"><span data-stu-id="178c4-128">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="178c4-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="178c4-129">-ResourceGroupName</span></span>
<span data-ttu-id="178c4-130">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="178c4-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="178c4-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="178c4-131">-ResourceId</span></span>
<span data-ttu-id="178c4-132">Az alkalmazás betekintési összetevőjének erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="178c4-132">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="178c4-133">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="178c4-133">-StorageAccountId</span></span>
<span data-ttu-id="178c4-134">Cél-tároló fiók azonosítója.</span><span class="sxs-lookup"><span data-stu-id="178c4-134">Destination Storage Account Id.</span></span>

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

### <span data-ttu-id="178c4-135">-StorageLocation</span><span class="sxs-lookup"><span data-stu-id="178c4-135">-StorageLocation</span></span>
<span data-ttu-id="178c4-136">Hely tárterületének azonosítója</span><span class="sxs-lookup"><span data-stu-id="178c4-136">Destination Storage Location Id.</span></span>

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

### <span data-ttu-id="178c4-137">-StorageSASUri</span><span class="sxs-lookup"><span data-stu-id="178c4-137">-StorageSASUri</span></span>
<span data-ttu-id="178c4-138">Destination Storage SAS URI.</span><span class="sxs-lookup"><span data-stu-id="178c4-138">Destination Storage SAS uri.</span></span>

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

### <span data-ttu-id="178c4-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="178c4-139">-WhatIf</span></span>
<span data-ttu-id="178c4-140">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="178c4-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="178c4-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="178c4-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="178c4-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="178c4-142">CommonParameters</span></span>
<span data-ttu-id="178c4-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="178c4-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="178c4-144">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="178c4-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="178c4-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="178c4-145">INPUTS</span></span>

### <span data-ttu-id="178c4-146">System. String</span><span class="sxs-lookup"><span data-stu-id="178c4-146">System.String</span></span>
<span data-ttu-id="178c4-147">System. string [] System. Boolean</span><span class="sxs-lookup"><span data-stu-id="178c4-147">System.String[] System.Boolean</span></span>

## <span data-ttu-id="178c4-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="178c4-148">OUTPUTS</span></span>

### <span data-ttu-id="178c4-149">Microsoft. Azure. Command. ApplicationInsights. models. PSExportConfiguration</span><span class="sxs-lookup"><span data-stu-id="178c4-149">Microsoft.Azure.Commands.ApplicationInsights.Models.PSExportConfiguration</span></span>

## <span data-ttu-id="178c4-150">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="178c4-150">NOTES</span></span>

## <span data-ttu-id="178c4-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="178c4-151">RELATED LINKS</span></span>

