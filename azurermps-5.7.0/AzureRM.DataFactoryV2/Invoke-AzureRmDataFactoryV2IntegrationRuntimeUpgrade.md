---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/invoke-azurermdatafactoryv2integrationruntimeupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Invoke-AzureRmDataFactoryV2IntegrationRuntimeUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Invoke-AzureRmDataFactoryV2IntegrationRuntimeUpgrade.md
ms.openlocfilehash: 312ef369e6d191dd96f85a293345d8fa155468b9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494538"
---
# <span data-ttu-id="c36ea-101">Invoke-AzureRmDataFactoryV2IntegrationRuntimeUpgrade</span><span class="sxs-lookup"><span data-stu-id="c36ea-101">Invoke-AzureRmDataFactoryV2IntegrationRuntimeUpgrade</span></span>

## <span data-ttu-id="c36ea-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c36ea-102">SYNOPSIS</span></span>
<span data-ttu-id="c36ea-103">Önkiszolgáló integrációs futtatókörnyezet frissítése</span><span class="sxs-lookup"><span data-stu-id="c36ea-103">Upgrades self-hosted integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c36ea-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c36ea-104">SYNTAX</span></span>

### <span data-ttu-id="c36ea-105">ByIntegrationRuntimeName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c36ea-105">ByIntegrationRuntimeName (Default)</span></span>
```
Invoke-AzureRmDataFactoryV2IntegrationRuntimeUpgrade [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c36ea-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="c36ea-106">ByResourceId</span></span>
```
Invoke-AzureRmDataFactoryV2IntegrationRuntimeUpgrade [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c36ea-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="c36ea-107">ByIntegrationRuntimeObject</span></span>
```
Invoke-AzureRmDataFactoryV2IntegrationRuntimeUpgrade [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c36ea-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="c36ea-108">DESCRIPTION</span></span>
<span data-ttu-id="c36ea-109">A **meghívó-AzureRmDataFactoryV2IntegrationRuntimeUpgrade** parancsmag az önálló integrációs futtatókörnyezetet frissíti, ha az új verzió elérhető.</span><span class="sxs-lookup"><span data-stu-id="c36ea-109">The **Invoke-AzureRmDataFactoryV2IntegrationRuntimeUpgrade** cmdlet upgrades self-hosted integration runtime if the new version is available.</span></span>

## <span data-ttu-id="c36ea-110">Példák</span><span class="sxs-lookup"><span data-stu-id="c36ea-110">EXAMPLES</span></span>

### <span data-ttu-id="c36ea-111">1. példa: egy önállóan üzemeltetett integrációs futtatókörnyezet frissítése</span><span class="sxs-lookup"><span data-stu-id="c36ea-111">Example 1: Upgrades a self-hosted integration runtime</span></span>
```
PS C:\> Invoke-AzureRmDataFactoryV2IntegrationRuntimeUpgrade -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'
```

<span data-ttu-id="c36ea-112">A parancsmag a "teszt-selfhost-IR" nevű "tesztelt-DF-EU2" adatkezelési futtatókörnyezetet frissíti.</span><span class="sxs-lookup"><span data-stu-id="c36ea-112">The cmdlet upgrades self-hosted integration runtime named 'test-selfhost-ir' in data factory 'test-df-eu2'.</span></span>

## <span data-ttu-id="c36ea-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c36ea-113">PARAMETERS</span></span>

### <span data-ttu-id="c36ea-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="c36ea-114">-DataFactoryName</span></span>
<span data-ttu-id="c36ea-115">Az adatgyári név.</span><span class="sxs-lookup"><span data-stu-id="c36ea-115">The data factory name.</span></span>

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

### <span data-ttu-id="c36ea-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c36ea-116">-DefaultProfile</span></span>
<span data-ttu-id="c36ea-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c36ea-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c36ea-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c36ea-118">-InputObject</span></span>
<span data-ttu-id="c36ea-119">Az integrációs futtatókörnyezet objektuma.</span><span class="sxs-lookup"><span data-stu-id="c36ea-119">The integration runtime object.</span></span>

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

### <span data-ttu-id="c36ea-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c36ea-120">-Name</span></span>
<span data-ttu-id="c36ea-121">Az integrációs futásidejű név.</span><span class="sxs-lookup"><span data-stu-id="c36ea-121">The integration runtime name.</span></span>

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

### <span data-ttu-id="c36ea-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c36ea-122">-ResourceGroupName</span></span>
<span data-ttu-id="c36ea-123">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="c36ea-123">The resource group name.</span></span>

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

### <span data-ttu-id="c36ea-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c36ea-124">-ResourceId</span></span>
<span data-ttu-id="c36ea-125">Az Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="c36ea-125">The Azure resource ID.</span></span>

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

### <span data-ttu-id="c36ea-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c36ea-126">-Confirm</span></span>
<span data-ttu-id="c36ea-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c36ea-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c36ea-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c36ea-128">-WhatIf</span></span>
<span data-ttu-id="c36ea-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c36ea-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c36ea-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c36ea-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c36ea-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c36ea-131">CommonParameters</span></span>
<span data-ttu-id="c36ea-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c36ea-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c36ea-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c36ea-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c36ea-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c36ea-134">INPUTS</span></span>

### <span data-ttu-id="c36ea-135">System. String</span><span class="sxs-lookup"><span data-stu-id="c36ea-135">System.String</span></span>
<span data-ttu-id="c36ea-136">Microsoft. Azure. Command. DataFactoryV2. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="c36ea-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="c36ea-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c36ea-137">OUTPUTS</span></span>

### <span data-ttu-id="c36ea-138">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="c36ea-138">System.Object</span></span>

## <span data-ttu-id="c36ea-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c36ea-139">NOTES</span></span>
<span data-ttu-id="c36ea-140">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak, másolás, tevékenységek, integrációs futtatókörnyezet</span><span class="sxs-lookup"><span data-stu-id="c36ea-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="c36ea-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c36ea-141">RELATED LINKS</span></span>

<span data-ttu-id="c36ea-142">[Set-AzureRmDataFactoryV2IntegrationRuntime]() 
 [Get-AzureRmDataFactoryV2IntegrationRuntime]()</span><span class="sxs-lookup"><span data-stu-id="c36ea-142">[Set-AzureRmDataFactoryV2IntegrationRuntime]()
[Get-AzureRmDataFactoryV2IntegrationRuntime]()</span></span>

