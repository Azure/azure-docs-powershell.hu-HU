---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/get-azdatafactoryv2integrationruntimemetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeMetric.md
ms.openlocfilehash: 12810756f1ebe3e3bf345519d981b660f4c61aa6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101930241"
---
# <span data-ttu-id="717ad-101">Get-AzDataFactoryV2IntegrationRuntimeMetric</span><span class="sxs-lookup"><span data-stu-id="717ad-101">Get-AzDataFactoryV2IntegrationRuntimeMetric</span></span>

## <span data-ttu-id="717ad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="717ad-102">SYNOPSIS</span></span>
<span data-ttu-id="717ad-103">Az integrációs futásidejű metrikus adatokat kapja.</span><span class="sxs-lookup"><span data-stu-id="717ad-103">Gets metric data for an integration runtime.</span></span> 

## <span data-ttu-id="717ad-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="717ad-104">SYNTAX</span></span>

### <span data-ttu-id="717ad-105">ByIntegrationRuntimeName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="717ad-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeMetric [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="717ad-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="717ad-106">ByResourceId</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeMetric [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="717ad-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="717ad-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeMetric [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="717ad-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="717ad-108">DESCRIPTION</span></span>
<span data-ttu-id="717ad-109">A Get-AzDataFactoryV2IntegrationRuntimeMetric parancsmag metrikus adatokat kap az integráció futásidejére vonatkozó adatokhoz egy adat factoryban.</span><span class="sxs-lookup"><span data-stu-id="717ad-109">The Get-AzDataFactoryV2IntegrationRuntimeMetric cmdlet gets metric data about integration runtime in a data factory.</span></span>

## <span data-ttu-id="717ad-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="717ad-110">EXAMPLES</span></span>

### <span data-ttu-id="717ad-111">1. példa: Integráció futásidejű mutatója</span><span class="sxs-lookup"><span data-stu-id="717ad-111">Example 1: Get integration runtime metric</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntimeMetric -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'

IntegrationRuntimeName ResourceGroupName DataFactoryName   Nodes   
---------------------- ----------------- ---------------   -----   
test-selfhost-ir       rg-test-dfv2      test-df-eu2       {Node_1}
```

<span data-ttu-id="717ad-112">Ez a parancs a "rg-test-dfv2" nevű erőforráscsoport és a "test-df-eu2" nevű adatüzemellátó erőforráscsoporthoz a "test-selfhost-ir" nevű integrációs futásidő metrikus adatait jeleníti meg az előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="717ad-112">This command displays metric data about the integration runtime named 'test-selfhost-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

## <span data-ttu-id="717ad-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="717ad-113">PARAMETERS</span></span>

### <span data-ttu-id="717ad-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="717ad-114">-DataFactoryName</span></span>
<span data-ttu-id="717ad-115">Az adatüzem neve.</span><span class="sxs-lookup"><span data-stu-id="717ad-115">The data factory name.</span></span>

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

### <span data-ttu-id="717ad-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="717ad-116">-DefaultProfile</span></span>
<span data-ttu-id="717ad-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="717ad-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="717ad-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="717ad-118">-InputObject</span></span>
<span data-ttu-id="717ad-119">Az integráció futásidejű objektuma.</span><span class="sxs-lookup"><span data-stu-id="717ad-119">The integration runtime object.</span></span>

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

### <span data-ttu-id="717ad-120">-Name</span><span class="sxs-lookup"><span data-stu-id="717ad-120">-Name</span></span>
<span data-ttu-id="717ad-121">Az integráció futásidejű neve.</span><span class="sxs-lookup"><span data-stu-id="717ad-121">The integration runtime name.</span></span>

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

### <span data-ttu-id="717ad-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="717ad-122">-ResourceGroupName</span></span>
<span data-ttu-id="717ad-123">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="717ad-123">The resource group name.</span></span>

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

### <span data-ttu-id="717ad-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="717ad-124">-ResourceId</span></span>
<span data-ttu-id="717ad-125">Az Azure-erőforrásazonosító.</span><span class="sxs-lookup"><span data-stu-id="717ad-125">The Azure resource ID.</span></span>

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

### <span data-ttu-id="717ad-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="717ad-126">CommonParameters</span></span>
<span data-ttu-id="717ad-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="717ad-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="717ad-128">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="717ad-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="717ad-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="717ad-129">INPUTS</span></span>

### <span data-ttu-id="717ad-130">System.String</span><span class="sxs-lookup"><span data-stu-id="717ad-130">System.String</span></span>

### <span data-ttu-id="717ad-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="717ad-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="717ad-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="717ad-132">OUTPUTS</span></span>

### <span data-ttu-id="717ad-133">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeMetrics</span><span class="sxs-lookup"><span data-stu-id="717ad-133">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeMetrics</span></span>

## <span data-ttu-id="717ad-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="717ad-134">NOTES</span></span>

## <span data-ttu-id="717ad-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="717ad-135">RELATED LINKS</span></span>

[<span data-ttu-id="717ad-136">Get-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="717ad-136">Get-AzDataFactoryV2IntegrationRuntime</span></span>]()

