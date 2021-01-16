---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2integrationruntimemetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeMetric.md
ms.openlocfilehash: 9b82d302bba1c2f51de3748fb9c335dd0db2699d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98333701"
---
# <span data-ttu-id="71d57-101">Get-AzDataFactoryV2IntegrationRuntimeMetric</span><span class="sxs-lookup"><span data-stu-id="71d57-101">Get-AzDataFactoryV2IntegrationRuntimeMetric</span></span>

## <span data-ttu-id="71d57-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="71d57-102">SYNOPSIS</span></span>
<span data-ttu-id="71d57-103">Az integrációs futásidejű metrikus adatokat kapja.</span><span class="sxs-lookup"><span data-stu-id="71d57-103">Gets metric data for an integration runtime.</span></span> 

## <span data-ttu-id="71d57-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="71d57-104">SYNTAX</span></span>

### <span data-ttu-id="71d57-105">ByIntegrationRuntimeName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="71d57-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeMetric [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="71d57-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="71d57-106">ByResourceId</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeMetric [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="71d57-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="71d57-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeMetric [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="71d57-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="71d57-108">DESCRIPTION</span></span>
<span data-ttu-id="71d57-109">A Get-AzDataFactoryV2IntegrationRuntimeMetric parancsmag metrikus adatokat kap az integráció futásidejére vonatkozó adatokról egy adat factoryban.</span><span class="sxs-lookup"><span data-stu-id="71d57-109">The Get-AzDataFactoryV2IntegrationRuntimeMetric cmdlet gets metric data about integration runtime in a data factory.</span></span>

## <span data-ttu-id="71d57-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="71d57-110">EXAMPLES</span></span>

### <span data-ttu-id="71d57-111">1. példa: Integráció futásidejű mutatója</span><span class="sxs-lookup"><span data-stu-id="71d57-111">Example 1: Get integration runtime metric</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntimeMetric -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'

IntegrationRuntimeName ResourceGroupName DataFactoryName   Nodes   
---------------------- ----------------- ---------------   -----   
test-selfhost-ir       rg-test-dfv2      test-df-eu2       {Node_1}
```

<span data-ttu-id="71d57-112">Ez a parancs az "rg-test-dfv2" nevű erőforráscsoport és a "test-df-eu2" nevű adatüzemeltöltési csoport "test-selfhost-ir" nevű integrációs futásidejére vonatkozó metrikus adatokat jeleníti meg az előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="71d57-112">This command displays metric data about the integration runtime named 'test-selfhost-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

## <span data-ttu-id="71d57-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="71d57-113">PARAMETERS</span></span>

### <span data-ttu-id="71d57-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="71d57-114">-DataFactoryName</span></span>
<span data-ttu-id="71d57-115">Az adatüzem neve.</span><span class="sxs-lookup"><span data-stu-id="71d57-115">The data factory name.</span></span>

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

### <span data-ttu-id="71d57-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71d57-116">-DefaultProfile</span></span>
<span data-ttu-id="71d57-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="71d57-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="71d57-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="71d57-118">-InputObject</span></span>
<span data-ttu-id="71d57-119">Az integráció futásidejű objektuma.</span><span class="sxs-lookup"><span data-stu-id="71d57-119">The integration runtime object.</span></span>

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

### <span data-ttu-id="71d57-120">-Name</span><span class="sxs-lookup"><span data-stu-id="71d57-120">-Name</span></span>
<span data-ttu-id="71d57-121">Az integráció futásidejű neve.</span><span class="sxs-lookup"><span data-stu-id="71d57-121">The integration runtime name.</span></span>

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

### <span data-ttu-id="71d57-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71d57-122">-ResourceGroupName</span></span>
<span data-ttu-id="71d57-123">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="71d57-123">The resource group name.</span></span>

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

### <span data-ttu-id="71d57-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="71d57-124">-ResourceId</span></span>
<span data-ttu-id="71d57-125">Az Azure-erőforrásazonosító.</span><span class="sxs-lookup"><span data-stu-id="71d57-125">The Azure resource ID.</span></span>

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

### <span data-ttu-id="71d57-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71d57-126">CommonParameters</span></span>
<span data-ttu-id="71d57-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71d57-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71d57-128">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71d57-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71d57-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="71d57-129">INPUTS</span></span>

### <span data-ttu-id="71d57-130">System.String</span><span class="sxs-lookup"><span data-stu-id="71d57-130">System.String</span></span>

### <span data-ttu-id="71d57-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="71d57-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="71d57-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="71d57-132">OUTPUTS</span></span>

### <span data-ttu-id="71d57-133">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeMetrics</span><span class="sxs-lookup"><span data-stu-id="71d57-133">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeMetrics</span></span>

## <span data-ttu-id="71d57-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="71d57-134">NOTES</span></span>

## <span data-ttu-id="71d57-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="71d57-135">RELATED LINKS</span></span>

[<span data-ttu-id="71d57-136">Get-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="71d57-136">Get-AzDataFactoryV2IntegrationRuntime</span></span>]()

