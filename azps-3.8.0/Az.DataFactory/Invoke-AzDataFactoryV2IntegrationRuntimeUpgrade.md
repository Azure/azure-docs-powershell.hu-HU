---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/invoke-azdatafactoryv2integrationruntimeupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade.md
ms.openlocfilehash: c7ffe4348d11658da6e7c9caeccaa14f17a6329b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93847261"
---
# <span data-ttu-id="69af9-101">Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade</span><span class="sxs-lookup"><span data-stu-id="69af9-101">Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade</span></span>

## <span data-ttu-id="69af9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="69af9-102">SYNOPSIS</span></span>
<span data-ttu-id="69af9-103">Önkiszolgáló integrációs futtatókörnyezet frissítése</span><span class="sxs-lookup"><span data-stu-id="69af9-103">Upgrades self-hosted integration runtime.</span></span>

## <span data-ttu-id="69af9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="69af9-104">SYNTAX</span></span>

### <span data-ttu-id="69af9-105">ByIntegrationRuntimeName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="69af9-105">ByIntegrationRuntimeName (Default)</span></span>
```
Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="69af9-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="69af9-106">ByResourceId</span></span>
```
Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69af9-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="69af9-107">ByIntegrationRuntimeObject</span></span>
```
Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69af9-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="69af9-108">DESCRIPTION</span></span>
<span data-ttu-id="69af9-109">A **meghívó-AzDataFactoryV2IntegrationRuntimeUpgrade** parancsmag az önálló integrációs futtatókörnyezetet frissíti, ha az új verzió elérhető.</span><span class="sxs-lookup"><span data-stu-id="69af9-109">The **Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade** cmdlet upgrades self-hosted integration runtime if the new version is available.</span></span>

## <span data-ttu-id="69af9-110">Példák</span><span class="sxs-lookup"><span data-stu-id="69af9-110">EXAMPLES</span></span>

### <span data-ttu-id="69af9-111">1. példa: egy önállóan üzemeltetett integrációs futtatókörnyezet frissítése</span><span class="sxs-lookup"><span data-stu-id="69af9-111">Example 1: Upgrades a self-hosted integration runtime</span></span>
```
PS C:\> Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'
```

<span data-ttu-id="69af9-112">A parancsmag a "teszt-selfhost-IR" nevű "tesztelt-DF-EU2" adatkezelési futtatókörnyezetet frissíti.</span><span class="sxs-lookup"><span data-stu-id="69af9-112">The cmdlet upgrades self-hosted integration runtime named 'test-selfhost-ir' in data factory 'test-df-eu2'.</span></span>

## <span data-ttu-id="69af9-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="69af9-113">PARAMETERS</span></span>

### <span data-ttu-id="69af9-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="69af9-114">-DataFactoryName</span></span>
<span data-ttu-id="69af9-115">Az adatgyári név.</span><span class="sxs-lookup"><span data-stu-id="69af9-115">The data factory name.</span></span>

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

### <span data-ttu-id="69af9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69af9-116">-DefaultProfile</span></span>
<span data-ttu-id="69af9-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="69af9-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="69af9-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="69af9-118">-InputObject</span></span>
<span data-ttu-id="69af9-119">Az integrációs futtatókörnyezet objektuma.</span><span class="sxs-lookup"><span data-stu-id="69af9-119">The integration runtime object.</span></span>

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

### <span data-ttu-id="69af9-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="69af9-120">-Name</span></span>
<span data-ttu-id="69af9-121">Az integrációs futásidejű név.</span><span class="sxs-lookup"><span data-stu-id="69af9-121">The integration runtime name.</span></span>

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

### <span data-ttu-id="69af9-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69af9-122">-ResourceGroupName</span></span>
<span data-ttu-id="69af9-123">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="69af9-123">The resource group name.</span></span>

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

### <span data-ttu-id="69af9-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="69af9-124">-ResourceId</span></span>
<span data-ttu-id="69af9-125">Az Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="69af9-125">The Azure resource ID.</span></span>

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

### <span data-ttu-id="69af9-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="69af9-126">-Confirm</span></span>
<span data-ttu-id="69af9-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="69af9-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69af9-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69af9-128">-WhatIf</span></span>
<span data-ttu-id="69af9-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="69af9-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69af9-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="69af9-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69af9-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69af9-131">CommonParameters</span></span>
<span data-ttu-id="69af9-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="69af9-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69af9-133">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69af9-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69af9-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="69af9-134">INPUTS</span></span>

### <span data-ttu-id="69af9-135">System. String</span><span class="sxs-lookup"><span data-stu-id="69af9-135">System.String</span></span>

### <span data-ttu-id="69af9-136">Microsoft. Azure. Command. DataFactoryV2. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="69af9-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="69af9-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="69af9-137">OUTPUTS</span></span>

### <span data-ttu-id="69af9-138">System. Void</span><span class="sxs-lookup"><span data-stu-id="69af9-138">System.Void</span></span>

## <span data-ttu-id="69af9-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="69af9-139">NOTES</span></span>
<span data-ttu-id="69af9-140">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak, másolás, tevékenységek, integrációs futtatókörnyezet</span><span class="sxs-lookup"><span data-stu-id="69af9-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="69af9-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="69af9-141">RELATED LINKS</span></span>

<span data-ttu-id="69af9-142">[Set-AzDataFactoryV2IntegrationRuntime]() 
 [Get-AzDataFactoryV2IntegrationRuntime]()</span><span class="sxs-lookup"><span data-stu-id="69af9-142">[Set-AzDataFactoryV2IntegrationRuntime]()
[Get-AzDataFactoryV2IntegrationRuntime]()</span></span>

