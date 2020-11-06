---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/set-azurermdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 8b91e1a68fc731476240021889cc80c9c4848357
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495419"
---
# <span data-ttu-id="6f8d2-101">Set-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="6f8d2-101">Set-AzureRmDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="6f8d2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6f8d2-102">SYNOPSIS</span></span>
<span data-ttu-id="6f8d2-103">Az integrációs futtatókörnyezet frissítése</span><span class="sxs-lookup"><span data-stu-id="6f8d2-103">Updates an integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6f8d2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6f8d2-104">SYNTAX</span></span>

### <span data-ttu-id="6f8d2-105">ByIntegrationRuntimeName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6f8d2-105">ByIntegrationRuntimeName (Default)</span></span>
```
Set-AzureRmDataFactoryV2IntegrationRuntime [-Type <String>] [-Description <String>] [-Location <String>]
 [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-SetupScriptContainerSasUri <String>] [-Edition <String>] [-MaxParallelExecutionsPerNode <Int32>]
 [-LicenseType <String>] [-AuthKey <SecureString>] [-Force] [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6f8d2-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="6f8d2-106">ByResourceId</span></span>
```
Set-AzureRmDataFactoryV2IntegrationRuntime [-Type <String>] [-Description <String>] [-Location <String>]
 [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-SetupScriptContainerSasUri <String>] [-Edition <String>] [-MaxParallelExecutionsPerNode <Int32>]
 [-LicenseType <String>] [-AuthKey <SecureString>] [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f8d2-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="6f8d2-107">ByIntegrationRuntimeObject</span></span>
```
Set-AzureRmDataFactoryV2IntegrationRuntime [-Type <String>] [-Description <String>] [-Location <String>]
 [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-SetupScriptContainerSasUri <String>] [-Edition <String>] [-MaxParallelExecutionsPerNode <Int32>]
 [-LicenseType <String>] [-AuthKey <SecureString>] [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f8d2-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="6f8d2-108">DESCRIPTION</span></span>
<span data-ttu-id="6f8d2-109">A Set-AzureRmDataFactoryV2IntegrationRuntime parancsmag meghatározott paraméterekkel frissíti az integrációs futtatókörnyezetet.</span><span class="sxs-lookup"><span data-stu-id="6f8d2-109">The Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet updates an integration runtime with specific parameters.</span></span>

## <span data-ttu-id="6f8d2-110">Példák</span><span class="sxs-lookup"><span data-stu-id="6f8d2-110">EXAMPLES</span></span>

### <span data-ttu-id="6f8d2-111">1. példa: az integrációs futtatókörnyezet frissítésének leírása.</span><span class="sxs-lookup"><span data-stu-id="6f8d2-111">Example 1: Update integration runtime description.</span></span>
```
PS C:\> Set-AzureRmDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' `
                                            -Description 'New description'

    Id                : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
    ResourceGroupName : rg-test-dfv2
    DataFactoryName   : test-df-eu2
    Name              : test-selfhost-ir
    Description       : New description
```

<span data-ttu-id="6f8d2-112">A parancsmag frissíti a "teszt-selfhost – IR" nevű integrációs futtatókörnyezet leírását.</span><span class="sxs-lookup"><span data-stu-id="6f8d2-112">The cmdlet updates the description of integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="6f8d2-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6f8d2-113">PARAMETERS</span></span>

### <span data-ttu-id="6f8d2-114">-AuthKey</span><span class="sxs-lookup"><span data-stu-id="6f8d2-114">-AuthKey</span></span>
<span data-ttu-id="6f8d2-115">Az önkiszolgáló integrációs futtatókörnyezet hitelesítési kulcsa.</span><span class="sxs-lookup"><span data-stu-id="6f8d2-115">The authentication key of the self-hosted integration runtime.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f8d2-116">-CatalogAdminCredential</span><span class="sxs-lookup"><span data-stu-id="6f8d2-116">-CatalogAdminCredential</span></span>
<span data-ttu-id="6f8d2-117">Az integrációs futtatókörnyezethez tartozó katalógus-adatbázis-rendszergazdai hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="6f8d2-117">The catalog database administrator credential of the integration runtime.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f8d2-118">-CatalogPricingTier</span><span class="sxs-lookup"><span data-stu-id="6f8d2-118">-CatalogPricingTier</span></span>
<span data-ttu-id="6f8d2-119">Az integrációs futtatókörnyezet katalógus-adatbázis árazási szintje.</span><span class="sxs-lookup"><span data-stu-id="6f8d2-119">The catalog database pricing tier of the integration runtime.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f8d2-120">-CatalogServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="6f8d2-120">-CatalogServerEndpoint</span></span>
<span data-ttu-id="6f8d2-121">Az integrációs futtatókörnyezet katalógus Database Server végpontja.</span><span class="sxs-lookup"><span data-stu-id="6f8d2-121">The catalog database server endpoint of the integration runtime.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f8d2-122">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="6f8d2-122">-DataFactoryName</span></span>
<span data-ttu-id="6f8d2-123">Az adatgyári név.</span><span class="sxs-lookup"><span data-stu-id="6f8d2-123">The data factory name.</span></span>

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

### <span data-ttu-id="6f8d2-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f8d2-124">-DefaultProfile</span></span>
<span data-ttu-id="6f8d2-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6f8d2-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6f8d2-126">-Leírás</span><span class="sxs-lookup"><span data-stu-id="6f8d2-126">-Description</span></span>
<span data-ttu-id="6f8d2-127">Az integrációs futtatókörnyezet leírása.</span><span class="sxs-lookup"><span data-stu-id="6f8d2-127">The integration runtime description.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f8d2-128">– Kiadás</span><span class="sxs-lookup"><span data-stu-id="6f8d2-128">-Edition</span></span>
<span data-ttu-id="6f8d2-129">Az SSIS-integrációs futásidejű verzió, amely a standard vagy a nagyvállalati lehet, az alapértelmezett érték a normál, ha nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="6f8d2-129">The edition for SSIS integration runtime which could be Standard or Enterprise, default is Standard if it is not specified.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Standard, Enterprise

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f8d2-130">-Force</span><span class="sxs-lookup"><span data-stu-id="6f8d2-130">-Force</span></span>
<span data-ttu-id="6f8d2-131">A parancsmag futtatása megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="6f8d2-131">Runs the cmdlet without prompting for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f8d2-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6f8d2-132">-InputObject</span></span>
<span data-ttu-id="6f8d2-133">Az integrációs futtatókörnyezet objektuma.</span><span class="sxs-lookup"><span data-stu-id="6f8d2-133">The integration runtime object.</span></span>

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

### <span data-ttu-id="6f8d2-134">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="6f8d2-134">-LicenseType</span></span>
<span data-ttu-id="6f8d2-135">Az SSIS-infravörös beállításhoz használni kívánt licenc típusa.</span><span class="sxs-lookup"><span data-stu-id="6f8d2-135">The license type that you want to select for the SSIS IR.</span></span> <span data-ttu-id="6f8d2-136">Két típus létezik: LicenseIncluded vagy BasePrice.</span><span class="sxs-lookup"><span data-stu-id="6f8d2-136">There are two types: LicenseIncluded or BasePrice.</span></span> <span data-ttu-id="6f8d2-137">Ha jogosult az Azure hibrid használati előnyeinek (AHUB) árazására, kérjük, válassza a BasePrice.</span><span class="sxs-lookup"><span data-stu-id="6f8d2-137">If you are qualified for the Azure Hybrid Use Benefit (AHUB) pricing, please select BasePrice.</span></span> <span data-ttu-id="6f8d2-138">Ha nem, akkor válassza a LicenseIncluded lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="6f8d2-138">If not, please select LicenseIncluded.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: LicenseIncluded, BasePrice

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f8d2-139">-Hely</span><span class="sxs-lookup"><span data-stu-id="6f8d2-139">-Location</span></span>
<span data-ttu-id="6f8d2-140">Az integrációs futtatókörnyezet helye.</span><span class="sxs-lookup"><span data-stu-id="6f8d2-140">The integration runtime location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f8d2-141">-MaxParallelExecutionsPerNode</span><span class="sxs-lookup"><span data-stu-id="6f8d2-141">-MaxParallelExecutionsPerNode</span></span>
<span data-ttu-id="6f8d2-142">A csomópontok maximális párhuzamos végrehajtásának száma egy felügyelt, dedikált integrációs futtatókörnyezet esetében.</span><span class="sxs-lookup"><span data-stu-id="6f8d2-142">Maximum parallel execution count per node for a managed dedicated integration runtime.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f8d2-143">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6f8d2-143">-Name</span></span>
<span data-ttu-id="6f8d2-144">Az integrációs futásidejű név.</span><span class="sxs-lookup"><span data-stu-id="6f8d2-144">The integration runtime name.</span></span>

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

### <span data-ttu-id="6f8d2-145">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="6f8d2-145">-NodeCount</span></span>
<span data-ttu-id="6f8d2-146">A fürtcsomópontok száma az integrációs futtatókörnyezetben.</span><span class="sxs-lookup"><span data-stu-id="6f8d2-146">Target nodes count of the integration runtime.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f8d2-147">-NodeSize</span><span class="sxs-lookup"><span data-stu-id="6f8d2-147">-NodeSize</span></span>
<span data-ttu-id="6f8d2-148">Az integrációs futtatókörnyezet csomópontjának mérete.</span><span class="sxs-lookup"><span data-stu-id="6f8d2-148">The integration runtime node size.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f8d2-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f8d2-149">-ResourceGroupName</span></span>
<span data-ttu-id="6f8d2-150">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="6f8d2-150">The resource group name.</span></span>

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

### <span data-ttu-id="6f8d2-151">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6f8d2-151">-ResourceId</span></span>
<span data-ttu-id="6f8d2-152">Az Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="6f8d2-152">The Azure resource ID.</span></span>

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

### <span data-ttu-id="6f8d2-153">-SetupScriptContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="6f8d2-153">-SetupScriptContainerSasUri</span></span>
<span data-ttu-id="6f8d2-154">Az egyéni beállítási parancsfájlt tartalmazó Azure Blob-tároló SAS-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="6f8d2-154">The SAS URI of the Azure blob container that contains the custom setup script.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f8d2-155">-Alhálózat</span><span class="sxs-lookup"><span data-stu-id="6f8d2-155">-Subnet</span></span>
<span data-ttu-id="6f8d2-156">Az alhálózat neve a VNet.</span><span class="sxs-lookup"><span data-stu-id="6f8d2-156">The name of the subnet in the VNet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SubnetName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f8d2-157">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="6f8d2-157">-Type</span></span>
<span data-ttu-id="6f8d2-158">Az integrációs futtatókörnyezet típusa.</span><span class="sxs-lookup"><span data-stu-id="6f8d2-158">The integration runtime type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Managed, SelfHosted

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f8d2-159">-VNetId</span><span class="sxs-lookup"><span data-stu-id="6f8d2-159">-VNetId</span></span>
<span data-ttu-id="6f8d2-160">Annak az VNet az azonosítója, amelyhez az integrációs futtatókörnyezet csatlakozik.</span><span class="sxs-lookup"><span data-stu-id="6f8d2-160">The ID of the VNet that the integration runtime joins.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f8d2-161">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6f8d2-161">-Confirm</span></span>
<span data-ttu-id="6f8d2-162">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6f8d2-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f8d2-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f8d2-163">-WhatIf</span></span>
<span data-ttu-id="6f8d2-164">Itt láthatja, hogy mi történik, ha a parancsmag fut, de nem futtatja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="6f8d2-164">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="6f8d2-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f8d2-165">CommonParameters</span></span>
<span data-ttu-id="6f8d2-166">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6f8d2-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f8d2-167">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f8d2-167">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f8d2-168">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6f8d2-168">INPUTS</span></span>

### <span data-ttu-id="6f8d2-169">System. String</span><span class="sxs-lookup"><span data-stu-id="6f8d2-169">System.String</span></span>
<span data-ttu-id="6f8d2-170">Microsoft. Azure. Command. DataFactoryV2. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="6f8d2-170">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="6f8d2-171">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6f8d2-171">OUTPUTS</span></span>

### <span data-ttu-id="6f8d2-172">Microsoft. Azure. Command. DataFactoryV2. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="6f8d2-172">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="6f8d2-173">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6f8d2-173">NOTES</span></span>

## <span data-ttu-id="6f8d2-174">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6f8d2-174">RELATED LINKS</span></span>

[<span data-ttu-id="6f8d2-175">Set-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="6f8d2-175">Set-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()
