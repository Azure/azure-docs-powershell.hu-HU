---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntimeMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntimeMetric.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 8912717f718bff7c669752e5e49c2796ee94b05b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680904"
---
# <span data-ttu-id="3f623-101">Get-AzureRmDataFactoryV2IntegrationRuntimeMetric</span><span class="sxs-lookup"><span data-stu-id="3f623-101">Get-AzureRmDataFactoryV2IntegrationRuntimeMetric</span></span>

## <span data-ttu-id="3f623-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3f623-102">SYNOPSIS</span></span>
<span data-ttu-id="3f623-103">Az integrációs futtatókörnyezet metrikus adatait kapja.</span><span class="sxs-lookup"><span data-stu-id="3f623-103">Gets metric data for an integration runtime.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3f623-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3f623-104">SYNTAX</span></span>

### <span data-ttu-id="3f623-105">ByIntegrationRuntimeName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3f623-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeMetric [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String>
```

### <span data-ttu-id="3f623-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="3f623-106">ByResourceId</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeMetric [-ResourceId] <String>
```

### <span data-ttu-id="3f623-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="3f623-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeMetric [-InputObject] <PSIntegrationRuntime>
```

## <span data-ttu-id="3f623-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="3f623-108">DESCRIPTION</span></span>
<span data-ttu-id="3f623-109">Az Get-AzureRmDataFactoryV2IntegrationRuntimeMetric parancsmag metrikus adatokat kap az adatfeldolgozó-integrációs futtatókörnyezetről.</span><span class="sxs-lookup"><span data-stu-id="3f623-109">The Get-AzureRmDataFactoryV2IntegrationRuntimeMetric cmdlet gets metric data about integration runtime in a data factory.</span></span>

## <span data-ttu-id="3f623-110">Példák</span><span class="sxs-lookup"><span data-stu-id="3f623-110">EXAMPLES</span></span>

### <span data-ttu-id="3f623-111">1. példa: az integrációs futtatókörnyezet metrikájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="3f623-111">Example 1: Get integration runtime metric</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2IntegrationRuntimeMetric -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'

IntegrationRuntimeName ResourceGroupName DataFactoryName   Nodes   
---------------------- ----------------- ---------------   -----   
test-selfhost-ir       rg-test-dfv2      test-df-eu2       {Node_1}
```

<span data-ttu-id="3f623-112">Ez a parancs metrikus adatokat jelenít meg a ' teszt-selfhost-IR ' nevű integrációs futtatókörnyezetről az "RG-teszt-dfv2" nevű erőforráscsoport előfizetésében, valamint a "teszt-DF-EU2" nevű adatfeldolgozót.</span><span class="sxs-lookup"><span data-stu-id="3f623-112">This command displays metric data about the integration runtime named 'test-selfhost-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

## <span data-ttu-id="3f623-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3f623-113">PARAMETERS</span></span>

### <span data-ttu-id="3f623-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="3f623-114">-DataFactoryName</span></span>
<span data-ttu-id="3f623-115">Az adatgyári név.</span><span class="sxs-lookup"><span data-stu-id="3f623-115">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f623-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3f623-116">-InputObject</span></span>
<span data-ttu-id="3f623-117">Az integrációs futtatókörnyezet objektuma.</span><span class="sxs-lookup"><span data-stu-id="3f623-117">The integration runtime object.</span></span>

```yaml
Type: PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3f623-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3f623-118">-Name</span></span>
<span data-ttu-id="3f623-119">Az integrációs futásidejű név.</span><span class="sxs-lookup"><span data-stu-id="3f623-119">The integration runtime name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f623-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f623-120">-ResourceGroupName</span></span>
<span data-ttu-id="3f623-121">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="3f623-121">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f623-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3f623-122">-ResourceId</span></span>
<span data-ttu-id="3f623-123">Az Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="3f623-123">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="3f623-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3f623-124">INPUTS</span></span>

### <span data-ttu-id="3f623-125">System. String</span><span class="sxs-lookup"><span data-stu-id="3f623-125">System.String</span></span>
<span data-ttu-id="3f623-126">Microsoft. Azure. Command. DataFactoryV2. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="3f623-126">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>


## <span data-ttu-id="3f623-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3f623-127">OUTPUTS</span></span>

### <span data-ttu-id="3f623-128">Microsoft. Azure. Command. DataFactoryV2. models. PSIntegrationRuntimeMetrics</span><span class="sxs-lookup"><span data-stu-id="3f623-128">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeMetrics</span></span>


## <span data-ttu-id="3f623-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3f623-129">NOTES</span></span>

## <span data-ttu-id="3f623-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3f623-130">RELATED LINKS</span></span>
[<span data-ttu-id="3f623-131">Get-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="3f623-131">Get-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()

