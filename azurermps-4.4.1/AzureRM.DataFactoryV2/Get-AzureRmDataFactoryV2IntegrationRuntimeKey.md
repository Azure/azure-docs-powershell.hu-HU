---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntimeKey.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 42ccd34e299439d3288a8a587ce9d62abe198847
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505099"
---
# <span data-ttu-id="9e0a2-101">Get-AzureRmDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="9e0a2-101">Get-AzureRmDataFactoryV2IntegrationRuntimeKey</span></span>

## <span data-ttu-id="9e0a2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9e0a2-102">SYNOPSIS</span></span>
<span data-ttu-id="9e0a2-103">Egy önállóan működtetett integrációs futásidejű kulcsokat kap.</span><span class="sxs-lookup"><span data-stu-id="9e0a2-103">Gets keys for a self-hosted integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9e0a2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9e0a2-104">SYNTAX</span></span>

### <span data-ttu-id="9e0a2-105">ByIntegrationRuntimeName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9e0a2-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeKey [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String>
```

### <span data-ttu-id="9e0a2-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="9e0a2-106">ByResourceId</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeKey [-ResourceId] <String>
```

### <span data-ttu-id="9e0a2-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="9e0a2-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeKey [-InputObject] <PSIntegrationRuntime>
```

## <span data-ttu-id="9e0a2-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="9e0a2-108">DESCRIPTION</span></span>
<span data-ttu-id="9e0a2-109">Beolvashatja az integrációs futtatókörnyezet kulcsait.</span><span class="sxs-lookup"><span data-stu-id="9e0a2-109">Get keys for an integration runtime.</span></span> <span data-ttu-id="9e0a2-110">A kulcsok az integrációs futásidejű csomópontok regisztrálására szolgálnak.</span><span class="sxs-lookup"><span data-stu-id="9e0a2-110">The keys are used to register an integration runtime node.</span></span>

## <span data-ttu-id="9e0a2-111">Példák</span><span class="sxs-lookup"><span data-stu-id="9e0a2-111">EXAMPLES</span></span>

### <span data-ttu-id="9e0a2-112">Példa 1: integrációs futásidejű kulcsok beszerzése</span><span class="sxs-lookup"><span data-stu-id="9e0a2-112">Example 1: Get integration runtime keys</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2IntegrationRuntimeKey -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'

AuthKey1                                                 AuthKey2
--------                                                 --------
IR@89895504-f647-48fd-8dd3-42fa556d67e3******            IR@89895504-f647-48fd-8dd3-42fa556d67e3****
```

<span data-ttu-id="9e0a2-113">A parancsmag a ' teszt-selfhost-IR ' nevű integrációs futásidejű kulcsait keresi meg.</span><span class="sxs-lookup"><span data-stu-id="9e0a2-113">The cmdlet retrieves keys for an integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="9e0a2-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9e0a2-114">PARAMETERS</span></span>

### <span data-ttu-id="9e0a2-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="9e0a2-115">-DataFactoryName</span></span>
<span data-ttu-id="9e0a2-116">Az adatgyári név.</span><span class="sxs-lookup"><span data-stu-id="9e0a2-116">The data factory name.</span></span>

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

### <span data-ttu-id="9e0a2-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9e0a2-117">-InputObject</span></span>
<span data-ttu-id="9e0a2-118">Az integrációs futtatókörnyezet objektuma.</span><span class="sxs-lookup"><span data-stu-id="9e0a2-118">The integration runtime object.</span></span>

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

### <span data-ttu-id="9e0a2-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9e0a2-119">-Name</span></span>
<span data-ttu-id="9e0a2-120">Az integrációs futásidejű név.</span><span class="sxs-lookup"><span data-stu-id="9e0a2-120">The integration runtime name.</span></span>

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

### <span data-ttu-id="9e0a2-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e0a2-121">-ResourceGroupName</span></span>
<span data-ttu-id="9e0a2-122">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="9e0a2-122">The resource group name.</span></span>

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

### <span data-ttu-id="9e0a2-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9e0a2-123">-ResourceId</span></span>
<span data-ttu-id="9e0a2-124">Az Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="9e0a2-124">The Azure resource ID.</span></span>

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

## <span data-ttu-id="9e0a2-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9e0a2-125">INPUTS</span></span>

### <span data-ttu-id="9e0a2-126">System. String</span><span class="sxs-lookup"><span data-stu-id="9e0a2-126">System.String</span></span>
<span data-ttu-id="9e0a2-127">Microsoft. Azure. Command. DataFactoryV2. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="9e0a2-127">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span> 


## <span data-ttu-id="9e0a2-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9e0a2-128">OUTPUTS</span></span>

### <span data-ttu-id="9e0a2-129">Microsoft. Azure. Command. DataFactoryV2. models. PSIntegrationRuntimeKeys</span><span class="sxs-lookup"><span data-stu-id="9e0a2-129">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeKeys</span></span>


## <span data-ttu-id="9e0a2-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9e0a2-130">NOTES</span></span>

## <span data-ttu-id="9e0a2-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9e0a2-131">RELATED LINKS</span></span>
[<span data-ttu-id="9e0a2-132">Új – AzureRmDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="9e0a2-132">New-AzureRmDataFactoryV2IntegrationRuntimeKey</span></span>]()
