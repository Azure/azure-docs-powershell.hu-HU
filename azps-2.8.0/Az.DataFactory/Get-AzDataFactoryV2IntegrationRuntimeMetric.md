---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2integrationruntimemetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeMetric.md
ms.openlocfilehash: 2f8887fa1e7839b3752d13c580460032ddc87026
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667057"
---
# <span data-ttu-id="0ff4a-101">Get-AzDataFactoryV2IntegrationRuntimeMetric</span><span class="sxs-lookup"><span data-stu-id="0ff4a-101">Get-AzDataFactoryV2IntegrationRuntimeMetric</span></span>

## <span data-ttu-id="0ff4a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0ff4a-102">SYNOPSIS</span></span>
<span data-ttu-id="0ff4a-103">Az integrációs futtatókörnyezet metrikus adatait kapja.</span><span class="sxs-lookup"><span data-stu-id="0ff4a-103">Gets metric data for an integration runtime.</span></span> 

## <span data-ttu-id="0ff4a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0ff4a-104">SYNTAX</span></span>

### <span data-ttu-id="0ff4a-105">ByIntegrationRuntimeName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0ff4a-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeMetric [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0ff4a-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="0ff4a-106">ByResourceId</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeMetric [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0ff4a-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="0ff4a-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeMetric [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0ff4a-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="0ff4a-108">DESCRIPTION</span></span>
<span data-ttu-id="0ff4a-109">Az Get-AzDataFactoryV2IntegrationRuntimeMetric parancsmag metrikus adatokat kap az adatfeldolgozó-integrációs futtatókörnyezetről.</span><span class="sxs-lookup"><span data-stu-id="0ff4a-109">The Get-AzDataFactoryV2IntegrationRuntimeMetric cmdlet gets metric data about integration runtime in a data factory.</span></span>

## <span data-ttu-id="0ff4a-110">Példák</span><span class="sxs-lookup"><span data-stu-id="0ff4a-110">EXAMPLES</span></span>

### <span data-ttu-id="0ff4a-111">1. példa: az integrációs futtatókörnyezet metrikájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="0ff4a-111">Example 1: Get integration runtime metric</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntimeMetric -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'

IntegrationRuntimeName ResourceGroupName DataFactoryName   Nodes   
---------------------- ----------------- ---------------   -----   
test-selfhost-ir       rg-test-dfv2      test-df-eu2       {Node_1}
```

<span data-ttu-id="0ff4a-112">Ez a parancs metrikus adatokat jelenít meg a ' teszt-selfhost-IR ' nevű integrációs futtatókörnyezetről az "RG-teszt-dfv2" nevű erőforráscsoport előfizetésében, valamint a "teszt-DF-EU2" nevű adatfeldolgozót.</span><span class="sxs-lookup"><span data-stu-id="0ff4a-112">This command displays metric data about the integration runtime named 'test-selfhost-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

## <span data-ttu-id="0ff4a-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0ff4a-113">PARAMETERS</span></span>

### <span data-ttu-id="0ff4a-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="0ff4a-114">-DataFactoryName</span></span>
<span data-ttu-id="0ff4a-115">Az adatgyári név.</span><span class="sxs-lookup"><span data-stu-id="0ff4a-115">The data factory name.</span></span>

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

### <span data-ttu-id="0ff4a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ff4a-116">-DefaultProfile</span></span>
<span data-ttu-id="0ff4a-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0ff4a-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0ff4a-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0ff4a-118">-InputObject</span></span>
<span data-ttu-id="0ff4a-119">Az integrációs futtatókörnyezet objektuma.</span><span class="sxs-lookup"><span data-stu-id="0ff4a-119">The integration runtime object.</span></span>

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

### <span data-ttu-id="0ff4a-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0ff4a-120">-Name</span></span>
<span data-ttu-id="0ff4a-121">Az integrációs futásidejű név.</span><span class="sxs-lookup"><span data-stu-id="0ff4a-121">The integration runtime name.</span></span>

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

### <span data-ttu-id="0ff4a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ff4a-122">-ResourceGroupName</span></span>
<span data-ttu-id="0ff4a-123">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="0ff4a-123">The resource group name.</span></span>

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

### <span data-ttu-id="0ff4a-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0ff4a-124">-ResourceId</span></span>
<span data-ttu-id="0ff4a-125">Az Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="0ff4a-125">The Azure resource ID.</span></span>

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

### <span data-ttu-id="0ff4a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ff4a-126">CommonParameters</span></span>
<span data-ttu-id="0ff4a-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0ff4a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ff4a-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ff4a-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ff4a-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0ff4a-129">INPUTS</span></span>

### <span data-ttu-id="0ff4a-130">System. String</span><span class="sxs-lookup"><span data-stu-id="0ff4a-130">System.String</span></span>

### <span data-ttu-id="0ff4a-131">Microsoft. Azure. Command. DataFactoryV2. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="0ff4a-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="0ff4a-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0ff4a-132">OUTPUTS</span></span>

### <span data-ttu-id="0ff4a-133">Microsoft. Azure. Command. DataFactoryV2. models. PSIntegrationRuntimeMetrics</span><span class="sxs-lookup"><span data-stu-id="0ff4a-133">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeMetrics</span></span>

## <span data-ttu-id="0ff4a-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0ff4a-134">NOTES</span></span>

## <span data-ttu-id="0ff4a-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0ff4a-135">RELATED LINKS</span></span>

[<span data-ttu-id="0ff4a-136">Get-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="0ff4a-136">Get-AzDataFactoryV2IntegrationRuntime</span></span>]()

