---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryv2integrationruntimemetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntimeMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntimeMetric.md
ms.openlocfilehash: 07c5b03b3d5717115238e3cd66b9f80925b51537
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499631"
---
# <span data-ttu-id="fea70-101">Get-AzureRmDataFactoryV2IntegrationRuntimeMetric</span><span class="sxs-lookup"><span data-stu-id="fea70-101">Get-AzureRmDataFactoryV2IntegrationRuntimeMetric</span></span>

## <span data-ttu-id="fea70-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fea70-102">SYNOPSIS</span></span>
<span data-ttu-id="fea70-103">Az integrációs futtatókörnyezet metrikus adatait kapja.</span><span class="sxs-lookup"><span data-stu-id="fea70-103">Gets metric data for an integration runtime.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fea70-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fea70-104">SYNTAX</span></span>

### <span data-ttu-id="fea70-105">ByIntegrationRuntimeName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fea70-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeMetric [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fea70-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="fea70-106">ByResourceId</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeMetric [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fea70-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="fea70-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeMetric [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fea70-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="fea70-108">DESCRIPTION</span></span>
<span data-ttu-id="fea70-109">Az Get-AzureRmDataFactoryV2IntegrationRuntimeMetric parancsmag metrikus adatokat kap az adatfeldolgozó-integrációs futtatókörnyezetről.</span><span class="sxs-lookup"><span data-stu-id="fea70-109">The Get-AzureRmDataFactoryV2IntegrationRuntimeMetric cmdlet gets metric data about integration runtime in a data factory.</span></span>

## <span data-ttu-id="fea70-110">Példák</span><span class="sxs-lookup"><span data-stu-id="fea70-110">EXAMPLES</span></span>

### <span data-ttu-id="fea70-111">1. példa: az integrációs futtatókörnyezet metrikájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="fea70-111">Example 1: Get integration runtime metric</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2IntegrationRuntimeMetric -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'

IntegrationRuntimeName ResourceGroupName DataFactoryName   Nodes   
---------------------- ----------------- ---------------   -----   
test-selfhost-ir       rg-test-dfv2      test-df-eu2       {Node_1}
```

<span data-ttu-id="fea70-112">Ez a parancs metrikus adatokat jelenít meg a ' teszt-selfhost-IR ' nevű integrációs futtatókörnyezetről az "RG-teszt-dfv2" nevű erőforráscsoport előfizetésében, valamint a "teszt-DF-EU2" nevű adatfeldolgozót.</span><span class="sxs-lookup"><span data-stu-id="fea70-112">This command displays metric data about the integration runtime named 'test-selfhost-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

## <span data-ttu-id="fea70-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fea70-113">PARAMETERS</span></span>

### <span data-ttu-id="fea70-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="fea70-114">-DataFactoryName</span></span>
<span data-ttu-id="fea70-115">Az adatgyári név.</span><span class="sxs-lookup"><span data-stu-id="fea70-115">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fea70-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fea70-116">-DefaultProfile</span></span>
<span data-ttu-id="fea70-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fea70-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fea70-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fea70-118">-InputObject</span></span>
<span data-ttu-id="fea70-119">Az integrációs futtatókörnyezet objektuma.</span><span class="sxs-lookup"><span data-stu-id="fea70-119">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fea70-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="fea70-120">-Name</span></span>
<span data-ttu-id="fea70-121">Az integrációs futásidejű név.</span><span class="sxs-lookup"><span data-stu-id="fea70-121">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fea70-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fea70-122">-ResourceGroupName</span></span>
<span data-ttu-id="fea70-123">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="fea70-123">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fea70-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fea70-124">-ResourceId</span></span>
<span data-ttu-id="fea70-125">Az Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="fea70-125">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fea70-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fea70-126">CommonParameters</span></span>
<span data-ttu-id="fea70-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fea70-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fea70-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fea70-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fea70-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fea70-129">INPUTS</span></span>

### <span data-ttu-id="fea70-130">System. String</span><span class="sxs-lookup"><span data-stu-id="fea70-130">System.String</span></span>

### <span data-ttu-id="fea70-131">Microsoft. Azure. Command. DataFactoryV2. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="fea70-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>
<span data-ttu-id="fea70-132">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="fea70-132">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="fea70-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fea70-133">OUTPUTS</span></span>

### <span data-ttu-id="fea70-134">Microsoft. Azure. Command. DataFactoryV2. models. PSIntegrationRuntimeMetrics</span><span class="sxs-lookup"><span data-stu-id="fea70-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeMetrics</span></span>

## <span data-ttu-id="fea70-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fea70-135">NOTES</span></span>

## <span data-ttu-id="fea70-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fea70-136">RELATED LINKS</span></span>

[<span data-ttu-id="fea70-137">Get-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="fea70-137">Get-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()

