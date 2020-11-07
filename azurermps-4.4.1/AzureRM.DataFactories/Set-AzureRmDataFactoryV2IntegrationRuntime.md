---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: ce842abf58dabb0bdd518f02e7030f3fb2feabc1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680585"
---
# <span data-ttu-id="cda88-101">Set-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="cda88-101">Set-AzureRmDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="cda88-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cda88-102">SYNOPSIS</span></span>
<span data-ttu-id="cda88-103">Az integrációs futtatókörnyezet frissítése</span><span class="sxs-lookup"><span data-stu-id="cda88-103">Updates an integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cda88-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cda88-104">SYNTAX</span></span>

### <span data-ttu-id="cda88-105">ByIntegrationRuntimeName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cda88-105">ByIntegrationRuntimeName (Default)</span></span>
```
Set-AzureRmDataFactoryV2IntegrationRuntime [-Type <String>] [-Description <String>] [-Location <String>]
 [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-Force] [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cda88-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="cda88-106">ByResourceId</span></span>
```
Set-AzureRmDataFactoryV2IntegrationRuntime [-Type <String>] [-Description <String>] [-Location <String>]
 [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cda88-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="cda88-107">ByIntegrationRuntimeObject</span></span>
```
Set-AzureRmDataFactoryV2IntegrationRuntime [-Type <String>] [-Description <String>] [-Location <String>]
 [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cda88-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="cda88-108">DESCRIPTION</span></span>
<span data-ttu-id="cda88-109">A Set-AzureRmDataFactoryV2IntegrationRuntime parancsmag meghatározott paraméterekkel frissíti az integrációs futtatókörnyezetet.</span><span class="sxs-lookup"><span data-stu-id="cda88-109">The Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet updates an integration runtime with specific parameters.</span></span>

## <span data-ttu-id="cda88-110">Példák</span><span class="sxs-lookup"><span data-stu-id="cda88-110">EXAMPLES</span></span>

### <span data-ttu-id="cda88-111">1. példa: az integrációs futtatókörnyezet frissítésének leírása.</span><span class="sxs-lookup"><span data-stu-id="cda88-111">Example 1: Update integration runtime description.</span></span>
```
PS C:\> Set-AzureRmDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' `
                                            -Description 'New description'

    Id                : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
    ResourceGroupName : rg-test-dfv2
    DataFactoryName   : test-df-eu2
    Name              : test-selfhost-ir
    Description       : New description
```

<span data-ttu-id="cda88-112">A parancsmag frissíti a "teszt-selfhost – IR" nevű integrációs futtatókörnyezet leírását.</span><span class="sxs-lookup"><span data-stu-id="cda88-112">The cmdlet updates the description of integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="cda88-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cda88-113">PARAMETERS</span></span>

### <span data-ttu-id="cda88-114">-CatalogAdminCredential</span><span class="sxs-lookup"><span data-stu-id="cda88-114">-CatalogAdminCredential</span></span>
<span data-ttu-id="cda88-115">Az integrációs futtatókörnyezethez tartozó katalógus-adatbázis-rendszergazdai hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="cda88-115">The catalog database administrator credential of the integration runtime.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cda88-116">-CatalogPricingTier</span><span class="sxs-lookup"><span data-stu-id="cda88-116">-CatalogPricingTier</span></span>
<span data-ttu-id="cda88-117">Az integrációs futtatókörnyezet katalógus-adatbázis árazási szintje.</span><span class="sxs-lookup"><span data-stu-id="cda88-117">The catalog database pricing tier of the integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cda88-118">-CatalogServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="cda88-118">-CatalogServerEndpoint</span></span>
<span data-ttu-id="cda88-119">Az integrációs futtatókörnyezet katalógus Database Server végpontja.</span><span class="sxs-lookup"><span data-stu-id="cda88-119">The catalog database server endpoint of the integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cda88-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="cda88-120">-Confirm</span></span>
<span data-ttu-id="cda88-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="cda88-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cda88-122">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="cda88-122">-DataFactoryName</span></span>
<span data-ttu-id="cda88-123">Az adatgyári név.</span><span class="sxs-lookup"><span data-stu-id="cda88-123">The data factory name.</span></span>

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

### <span data-ttu-id="cda88-124">-Leírás</span><span class="sxs-lookup"><span data-stu-id="cda88-124">-Description</span></span>
<span data-ttu-id="cda88-125">Az integrációs futtatókörnyezet leírása.</span><span class="sxs-lookup"><span data-stu-id="cda88-125">The integration runtime description.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cda88-126">-Force</span><span class="sxs-lookup"><span data-stu-id="cda88-126">-Force</span></span>
<span data-ttu-id="cda88-127">A parancsmag futtatása megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="cda88-127">Runs the cmdlet without prompting for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cda88-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cda88-128">-InputObject</span></span>
<span data-ttu-id="cda88-129">Az integrációs futtatókörnyezet objektuma.</span><span class="sxs-lookup"><span data-stu-id="cda88-129">The integration runtime object.</span></span>

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

### <span data-ttu-id="cda88-130">-Hely</span><span class="sxs-lookup"><span data-stu-id="cda88-130">-Location</span></span>
<span data-ttu-id="cda88-131">Az integrációs futtatókörnyezet helye.</span><span class="sxs-lookup"><span data-stu-id="cda88-131">The integration runtime location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cda88-132">-MaxParallelExecutionsPerNode</span><span class="sxs-lookup"><span data-stu-id="cda88-132">-MaxParallelExecutionsPerNode</span></span>
<span data-ttu-id="cda88-133">A csomópontok maximális párhuzamos végrehajtásának száma egy felügyelt, dedikált integrációs futtatókörnyezet esetében.</span><span class="sxs-lookup"><span data-stu-id="cda88-133">Maximum parallel execution count per node for a managed dedicated integration runtime.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cda88-134">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="cda88-134">-Name</span></span>
<span data-ttu-id="cda88-135">Az integrációs futásidejű név.</span><span class="sxs-lookup"><span data-stu-id="cda88-135">The integration runtime name.</span></span>

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

### <span data-ttu-id="cda88-136">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="cda88-136">-NodeCount</span></span>
<span data-ttu-id="cda88-137">A fürtcsomópontok száma az integrációs futtatókörnyezetben.</span><span class="sxs-lookup"><span data-stu-id="cda88-137">Target nodes count of the integration runtime.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cda88-138">-NodeSize</span><span class="sxs-lookup"><span data-stu-id="cda88-138">-NodeSize</span></span>
<span data-ttu-id="cda88-139">Az integrációs futtatókörnyezet csomópontjának mérete.</span><span class="sxs-lookup"><span data-stu-id="cda88-139">The integration runtime node size.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cda88-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cda88-140">-ResourceGroupName</span></span>
<span data-ttu-id="cda88-141">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="cda88-141">The resource group name.</span></span>

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

### <span data-ttu-id="cda88-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cda88-142">-ResourceId</span></span>
<span data-ttu-id="cda88-143">Az Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="cda88-143">The Azure resource ID.</span></span>

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

### <span data-ttu-id="cda88-144">-Alhálózat</span><span class="sxs-lookup"><span data-stu-id="cda88-144">-Subnet</span></span>
<span data-ttu-id="cda88-145">Az alhálózat neve a VNet.</span><span class="sxs-lookup"><span data-stu-id="cda88-145">The name of the subnet in the VNet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubnetName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cda88-146">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="cda88-146">-Type</span></span>
<span data-ttu-id="cda88-147">Az integrációs futtatókörnyezet típusa.</span><span class="sxs-lookup"><span data-stu-id="cda88-147">The integration runtime type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Managed, SelfHosted

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cda88-148">-VNetId</span><span class="sxs-lookup"><span data-stu-id="cda88-148">-VNetId</span></span>
<span data-ttu-id="cda88-149">Annak az VNet az azonosítója, amelyhez az integrációs futtatókörnyezet csatlakozik.</span><span class="sxs-lookup"><span data-stu-id="cda88-149">The ID of the VNet that the integration runtime joins.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cda88-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cda88-150">-WhatIf</span></span>
<span data-ttu-id="cda88-151">Itt láthatja, hogy mi történik, ha a parancsmag fut, de nem futtatja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="cda88-151">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="cda88-152">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cda88-152">-DefaultProfile</span></span>
<span data-ttu-id="cda88-153">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cda88-153">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cda88-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cda88-154">CommonParameters</span></span>
<span data-ttu-id="cda88-155">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cda88-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cda88-156">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cda88-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cda88-157">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cda88-157">INPUTS</span></span>

### <span data-ttu-id="cda88-158">System. String</span><span class="sxs-lookup"><span data-stu-id="cda88-158">System.String</span></span>
<span data-ttu-id="cda88-159">Microsoft. Azure. Command. DataFactoryV2. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="cda88-159">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="cda88-160">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cda88-160">OUTPUTS</span></span>

### <span data-ttu-id="cda88-161">Microsoft. Azure. Command. DataFactoryV2. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="cda88-161">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="cda88-162">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cda88-162">NOTES</span></span>

## <span data-ttu-id="cda88-163">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cda88-163">RELATED LINKS</span></span>

[<span data-ttu-id="cda88-164">Set-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="cda88-164">Set-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()
