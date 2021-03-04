---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/invoke-azdatafactoryv2integrationruntimeupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade.md
ms.openlocfilehash: 941e820bb1c274a74cc52042b80cdf1b259a34b6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101930162"
---
# <span data-ttu-id="05839-101">Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade</span><span class="sxs-lookup"><span data-stu-id="05839-101">Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade</span></span>

## <span data-ttu-id="05839-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="05839-102">SYNOPSIS</span></span>
<span data-ttu-id="05839-103">Frissíti az önkiszolgáló integrációs futásiidőt.</span><span class="sxs-lookup"><span data-stu-id="05839-103">Upgrades self-hosted integration runtime.</span></span>

## <span data-ttu-id="05839-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="05839-104">SYNTAX</span></span>

### <span data-ttu-id="05839-105">ByIntegrationRuntimeName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="05839-105">ByIntegrationRuntimeName (Default)</span></span>
```
Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="05839-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="05839-106">ByResourceId</span></span>
```
Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05839-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="05839-107">ByIntegrationRuntimeObject</span></span>
```
Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="05839-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="05839-108">DESCRIPTION</span></span>
<span data-ttu-id="05839-109">Az **Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade** parancsmag frissíti az önkiszolgáló integrációs futásidejét, ha az új verzió elérhető.</span><span class="sxs-lookup"><span data-stu-id="05839-109">The **Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade** cmdlet upgrades self-hosted integration runtime if the new version is available.</span></span>

## <span data-ttu-id="05839-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="05839-110">EXAMPLES</span></span>

### <span data-ttu-id="05839-111">1. példa: Önkiszolgáló integrációs futási idő frissítése</span><span class="sxs-lookup"><span data-stu-id="05839-111">Example 1: Upgrades a self-hosted integration runtime</span></span>
```
PS C:\> Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'
```

<span data-ttu-id="05839-112">A parancsmag frissíti a "test-selfhost-ir" nevű önkiszolgáló integrációs futásiidőt a "test-df-eu2" data factoryban.</span><span class="sxs-lookup"><span data-stu-id="05839-112">The cmdlet upgrades self-hosted integration runtime named 'test-selfhost-ir' in data factory 'test-df-eu2'.</span></span>

## <span data-ttu-id="05839-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="05839-113">PARAMETERS</span></span>

### <span data-ttu-id="05839-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="05839-114">-DataFactoryName</span></span>
<span data-ttu-id="05839-115">Az adatüzem neve.</span><span class="sxs-lookup"><span data-stu-id="05839-115">The data factory name.</span></span>

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

### <span data-ttu-id="05839-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05839-116">-DefaultProfile</span></span>
<span data-ttu-id="05839-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="05839-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="05839-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="05839-118">-InputObject</span></span>
<span data-ttu-id="05839-119">Az integráció futásidejű objektuma.</span><span class="sxs-lookup"><span data-stu-id="05839-119">The integration runtime object.</span></span>

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

### <span data-ttu-id="05839-120">-Name</span><span class="sxs-lookup"><span data-stu-id="05839-120">-Name</span></span>
<span data-ttu-id="05839-121">Az integráció futásidejű neve.</span><span class="sxs-lookup"><span data-stu-id="05839-121">The integration runtime name.</span></span>

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

### <span data-ttu-id="05839-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05839-122">-ResourceGroupName</span></span>
<span data-ttu-id="05839-123">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="05839-123">The resource group name.</span></span>

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

### <span data-ttu-id="05839-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="05839-124">-ResourceId</span></span>
<span data-ttu-id="05839-125">Az Azure-erőforrásazonosító.</span><span class="sxs-lookup"><span data-stu-id="05839-125">The Azure resource ID.</span></span>

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

### <span data-ttu-id="05839-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="05839-126">-Confirm</span></span>
<span data-ttu-id="05839-127">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="05839-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05839-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05839-128">-WhatIf</span></span>
<span data-ttu-id="05839-129">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="05839-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05839-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="05839-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05839-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05839-131">CommonParameters</span></span>
<span data-ttu-id="05839-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05839-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05839-133">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05839-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05839-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="05839-134">INPUTS</span></span>

### <span data-ttu-id="05839-135">System.String</span><span class="sxs-lookup"><span data-stu-id="05839-135">System.String</span></span>

### <span data-ttu-id="05839-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="05839-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="05839-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="05839-137">OUTPUTS</span></span>

### <span data-ttu-id="05839-138">System.Void</span><span class="sxs-lookup"><span data-stu-id="05839-138">System.Void</span></span>

## <span data-ttu-id="05839-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="05839-139">NOTES</span></span>
<span data-ttu-id="05839-140">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, kezelő, adatok, faktorok, másolás, tevékenységek, integráció futásideje</span><span class="sxs-lookup"><span data-stu-id="05839-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="05839-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="05839-141">RELATED LINKS</span></span>

<span data-ttu-id="05839-142">[Set-AzDataFactoryV2IntegrationRuntime]() 
 [Get-AzDataFactoryV2IntegrationRuntime]()</span><span class="sxs-lookup"><span data-stu-id="05839-142">[Set-AzDataFactoryV2IntegrationRuntime]()
[Get-AzDataFactoryV2IntegrationRuntime]()</span></span>

