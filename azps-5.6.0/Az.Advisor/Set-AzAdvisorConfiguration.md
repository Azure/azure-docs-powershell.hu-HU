---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Advisor.dll-Help.xml
Module Name: Az.Advisor
online version: https://docs.microsoft.com/powershell/module/az.advisor/set-azadvisorConfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Set-AzAdvisorConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Set-AzAdvisorConfiguration.md
ms.openlocfilehash: 550b9d11cd2f5b0cadb13d76809faa2ac34dc426
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101926113"
---
# <span data-ttu-id="18a0d-101">Set-AzAdvisorConfiguration</span><span class="sxs-lookup"><span data-stu-id="18a0d-101">Set-AzAdvisorConfiguration</span></span>

## <span data-ttu-id="18a0d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="18a0d-102">SYNOPSIS</span></span>
<span data-ttu-id="18a0d-103">Frissíti vagy létrehozza az Azure Advisor-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="18a0d-103">Updates or creates the Azure Advisor Configuration.</span></span>

## <span data-ttu-id="18a0d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="18a0d-104">SYNTAX</span></span>

### <span data-ttu-id="18a0d-105">InputObjectRgExcludeParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="18a0d-105">InputObjectRgExcludeParameterSet (Default)</span></span>
```
Set-AzAdvisorConfiguration [-Exclude] [[-ResourceGroupName] <String>]
 [[-InputObject] <PsAzureAdvisorConfigurationData>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18a0d-106">InputObjectLowCpuExcludeParameterSet</span><span class="sxs-lookup"><span data-stu-id="18a0d-106">InputObjectLowCpuExcludeParameterSet</span></span> 
```
Set-AzAdvisorConfiguration [-Exclude] [-LowCpuThreshold] <Int32>
 [[-InputObject] <PsAzureAdvisorConfigurationData>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="18a0d-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="18a0d-107">DESCRIPTION</span></span>
<span data-ttu-id="18a0d-108">Az Azure Advisor konfigurációjának frissítésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="18a0d-108">Used to update the configuration of the Azure Advisor.</span></span> <span data-ttu-id="18a0d-109">Két konfigurációtípus van jelen: Előfizetési szintű konfiguráció és Erőforráscsoport szintű konfiguráció.</span><span class="sxs-lookup"><span data-stu-id="18a0d-109">Two types of Configuration are present: Subscription level configuration and ResourceGroup level configuration.</span></span> 

<span data-ttu-id="18a0d-110">Előfizetési szintű konfiguráció: Ehhez a típushoz csak egy konfiguráció lehet egy előfizetéshez.</span><span class="sxs-lookup"><span data-stu-id="18a0d-110">Subscription level configuration: There can be only one Configuration for this type for a subscription.</span></span> <span data-ttu-id="18a0d-111">Ezzel a parancsmaggal frissítheti a LowCpuThreshold és a Exclude tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="18a0d-111">LowCpuThreshold and Exclude properties can be updated using this cmdlet.</span></span>
<span data-ttu-id="18a0d-112">Erőforráscsoport szintű konfiguráció: Minden Erőforráscsoporthoz csak egy konfiguráció lehet.</span><span class="sxs-lookup"><span data-stu-id="18a0d-112">ResourceGroup level configuration: There can be only one configuration for each ResourceGroup.</span></span> <span data-ttu-id="18a0d-113">Ezzel a parancsmagot használva csak az Exclude tulajdonság frissíthető.</span><span class="sxs-lookup"><span data-stu-id="18a0d-113">Only Exclude property can be updated using this cmdlet.</span></span>

## <span data-ttu-id="18a0d-114">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="18a0d-114">EXAMPLES</span></span>

###  <span data-ttu-id="18a0d-115">1. példa</span><span class="sxs-lookup"><span data-stu-id="18a0d-115">Example 1</span></span>
```powershell
PS C:\> Set-AzAdvisorConfiguration -LowCpuThreshold 10
Id         : /subscriptions/{user_subscription}/resourceGroups/resourceGroupName1/providers/Microsoft.Advisor/configurations/{user_subscription}
Name       : {user_subscription}
Properties : additionalProperties : null
             exclude :  False
             lowCpuThreshold : 10

Type       : Microsoft.Advisor/Configurations
```

<span data-ttu-id="18a0d-116">Frissíti az előfizetési szintű konfiguráció (lowCpuThreshold) konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="18a0d-116">Updates the configuration(lowCpuThreshold) for subscription level Configuration.</span></span>

### <span data-ttu-id="18a0d-117">2. példa</span><span class="sxs-lookup"><span data-stu-id="18a0d-117">Example 2</span></span>
```powershell
PS C:\> Set-AzAdvisorConfiguration -LowCpuThreshold 15 -Exclude 
Id         : /subscriptions/{user_subscription}/resourceGroups/resourceGroupName1/providers/Microsoft.Advisor/configurations/{user_subscription}
Name       : {user_subscription}
Properties : additionalProperties : null
             exclude :  True
             lowCpuThreshold : 15

Type       : Microsoft.Advisor/Configurations
```

<span data-ttu-id="18a0d-118">Frissíti az előfizetési szintű konfiguráció konfigurációját (lowCpuThreshold, exclude) és nem tartalmazza az ajánlott konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="18a0d-118">Updates the configuration(lowCpuThreshold, exclude) for subscription level Configuration and excludes from the recommendation generation.</span></span>

### <span data-ttu-id="18a0d-119">3. példa</span><span class="sxs-lookup"><span data-stu-id="18a0d-119">Example 3</span></span>
```powershell
PS C:\> Set-AzAdvisorConfiguration -ResourceGroupName resourceGroupName1 -Exclude

Id         : /subscriptions/{user_subscription}/resourceGroups/resourceGroupName1/providers/Microsoft.Advisor/configurations/{user_subscription}-resourceGroupName1
Name       : {user_subscription}-resourceGroupName1
Properties : additionalProperties : null
             exclude :  True
             lowCpuThreshold : null

Type       : Microsoft.Advisor/Configurations
```

<span data-ttu-id="18a0d-120">Frissíti az erőforrásGroupName1 konfigurációját (kizárását) ahhoz, hogy ne legyen elérhető az ajánlott frissítésben.</span><span class="sxs-lookup"><span data-stu-id="18a0d-120">Updates the configuration(exclude) for resourceGroupName1 to be excluded in the recommendation generation.</span></span>

### <span data-ttu-id="18a0d-121">4. példa</span><span class="sxs-lookup"><span data-stu-id="18a0d-121">Example 4</span></span>
```powershell
PS C:\> Get-AzAdvisorConfiguration | Set-AzAdvisorConfiguration -LowCpuThreshold 20
Id         : /subscriptions/{user_subscription}/resourceGroups/resourceGroupName1/providers/Microsoft.Advisor/configurations/{user_subscription}
Name       : {user_subscription}
Properties : additionalProperties : null
             exclude :  False
             lowCpuThreshold : 20

Type       : Microsoft.Advisor/Configurations
```

<span data-ttu-id="18a0d-122">Frissíti a folyamatból átadott adott javaslat konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="18a0d-122">Updates the configuration for the given recommendation passed on from the pipeline.</span></span>

## <span data-ttu-id="18a0d-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="18a0d-123">PARAMETERS</span></span>

### <span data-ttu-id="18a0d-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="18a0d-124">-Confirm</span></span>
<span data-ttu-id="18a0d-125">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="18a0d-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="18a0d-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18a0d-126">-DefaultProfile</span></span>
<span data-ttu-id="18a0d-127">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="18a0d-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="18a0d-128">-Exclude</span><span class="sxs-lookup"><span data-stu-id="18a0d-128">-Exclude</span></span>
<span data-ttu-id="18a0d-129">Zárja ki az ajánlottak generálásból.</span><span class="sxs-lookup"><span data-stu-id="18a0d-129">Exclude from the recommendation generation.</span></span> <span data-ttu-id="18a0d-130">Ha nincs megadva a exclude tulajdonság, akkor a tulajdonság hamisra lesz állítva.</span><span class="sxs-lookup"><span data-stu-id="18a0d-130">If not specified exclude property will be set to false.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18a0d-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="18a0d-131">-InputObject</span></span>
<span data-ttu-id="18a0d-132">A hívás által visszaadott PsAzureAdvisorConfigurationData powershellGet-AzAdvisorConfiguration objektumtípus.</span><span class="sxs-lookup"><span data-stu-id="18a0d-132">The powershell object type PsAzureAdvisorConfigurationData returned by Get-AzAdvisorConfiguration call.</span></span>

```yaml
Type: PsAzureAdvisorConfigurationData
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="18a0d-133">-LowCpuThreshold</span><span class="sxs-lookup"><span data-stu-id="18a0d-133">-LowCpuThreshold</span></span>
<span data-ttu-id="18a0d-134">Az alacsony processzorküszöb értéke.</span><span class="sxs-lookup"><span data-stu-id="18a0d-134">Value for Low Cpu threshold.</span></span>

```yaml
Type: Int32
Parameter Sets: InputObjectLowCpuExcludeParameterSet
Aliases:
Accepted values: 0, 5, 10, 15, 20

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18a0d-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18a0d-135">-ResourceGroupName</span></span>
<span data-ttu-id="18a0d-136">A konfiguráció erőforráscsoportjának neve.</span><span class="sxs-lookup"><span data-stu-id="18a0d-136">Resource Group name for the configuration.</span></span>

```yaml
Type: String
Parameter Sets: InputObjectRgExcludeParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18a0d-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18a0d-137">-WhatIf</span></span>
<span data-ttu-id="18a0d-138">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="18a0d-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="18a0d-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="18a0d-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="18a0d-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18a0d-140">CommonParameters</span></span>
<span data-ttu-id="18a0d-141">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18a0d-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="18a0d-142">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18a0d-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18a0d-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="18a0d-143">INPUTS</span></span>

### <span data-ttu-id="18a0d-144">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorConfigurationData</span><span class="sxs-lookup"><span data-stu-id="18a0d-144">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorConfigurationData</span></span>

## <span data-ttu-id="18a0d-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="18a0d-145">OUTPUTS</span></span>

### <span data-ttu-id="18a0d-146">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorConfigurationData</span><span class="sxs-lookup"><span data-stu-id="18a0d-146">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorConfigurationData</span></span>

## <span data-ttu-id="18a0d-147">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="18a0d-147">NOTES</span></span>

## <span data-ttu-id="18a0d-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="18a0d-148">RELATED LINKS</span></span>
