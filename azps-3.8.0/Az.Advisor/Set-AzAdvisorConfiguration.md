---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Advisor.dll-Help.xml
Module Name: Az.Advisor
online version: https://docs.microsoft.com/en-us/powershell/module/az.advisor/set-azadvisorConfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Set-AzAdvisorConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Set-AzAdvisorConfiguration.md
ms.openlocfilehash: bfd1677fa46a749b73206b02bb6585c4a529637f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011977"
---
# <span data-ttu-id="6ecf0-101">Set-AzAdvisorConfiguration</span><span class="sxs-lookup"><span data-stu-id="6ecf0-101">Set-AzAdvisorConfiguration</span></span>

## <span data-ttu-id="6ecf0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6ecf0-102">SYNOPSIS</span></span>
<span data-ttu-id="6ecf0-103">Frissítse vagy hozza létre az Azure Advisor konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="6ecf0-103">Updates or creates the Azure Advisor Configuration.</span></span>

## <span data-ttu-id="6ecf0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6ecf0-104">SYNTAX</span></span>

### <span data-ttu-id="6ecf0-105">InputObjectRgExcludeParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6ecf0-105">InputObjectRgExcludeParameterSet (Default)</span></span>
```
Set-AzAdvisorConfiguration [-Exclude] [[-ResourceGroupName] <String>]
 [[-InputObject] <PsAzureAdvisorConfigurationData>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ecf0-106">InputObjectLowCpuExcludeParameterSet</span><span class="sxs-lookup"><span data-stu-id="6ecf0-106">InputObjectLowCpuExcludeParameterSet</span></span> 
```
Set-AzAdvisorConfiguration [-Exclude] [-LowCpuThreshold] <Int32>
 [[-InputObject] <PsAzureAdvisorConfigurationData>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ecf0-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="6ecf0-107">DESCRIPTION</span></span>
<span data-ttu-id="6ecf0-108">Segítségével frissítheti az Azure Advisor konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="6ecf0-108">Used to update the configuration of the Azure Advisor.</span></span> <span data-ttu-id="6ecf0-109">Kétféle konfiguráció létezik: az előfizetési szint konfiguráció és a ResourceGroup-szint konfiguráció.</span><span class="sxs-lookup"><span data-stu-id="6ecf0-109">Two types of Configuration are present: Subscription level configuration and ResourceGroup level configuration.</span></span> 

<span data-ttu-id="6ecf0-110">Előfizetési szint beállítása: az előfizetéshez csak egy konfiguráció lehet az adott típushoz.</span><span class="sxs-lookup"><span data-stu-id="6ecf0-110">Subscription level configuration: There can be only one Configuration for this type for a subscription.</span></span> <span data-ttu-id="6ecf0-111">A LowCpuThreshold és a kihagyott tulajdonságok a parancsmag használatával frissíthetők.</span><span class="sxs-lookup"><span data-stu-id="6ecf0-111">LowCpuThreshold and Exclude properties can be updated using this cmdlet.</span></span>
<span data-ttu-id="6ecf0-112">ResourceGroup-szint beállítása: csak egy konfiguráció használható minden ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="6ecf0-112">ResourceGroup level configuration: There can be only one configuration for each ResourceGroup.</span></span> <span data-ttu-id="6ecf0-113">Ezzel a parancsmaggal csak az kizárható tulajdonságokat lehet frissíteni.</span><span class="sxs-lookup"><span data-stu-id="6ecf0-113">Only Exclude property can be updated using this cmdlet.</span></span>

## <span data-ttu-id="6ecf0-114">Példák</span><span class="sxs-lookup"><span data-stu-id="6ecf0-114">EXAMPLES</span></span>

###  <span data-ttu-id="6ecf0-115">Példa 1</span><span class="sxs-lookup"><span data-stu-id="6ecf0-115">Example 1</span></span>
```powershell
PS C:\> Set-AzAdvisorConfiguration -LowCpuThreshold 10
Id         : /subscriptions/{user_subscription}/resourceGroups/resourceGroupName1/providers/Microsoft.Advisor/configurations/{user_subscription}
Name       : {user_subscription}
Properties : additionalProperties : null
             exclude :  False
             lowCpuThreshold : 10

Type       : Microsoft.Advisor/Configurations
```

<span data-ttu-id="6ecf0-116">Frissíti az előfizetési szint konfigurációjának konfigurációját (lowCpuThreshold).</span><span class="sxs-lookup"><span data-stu-id="6ecf0-116">Updates the configuration(lowCpuThreshold) for subscription level Configuration.</span></span>

### <span data-ttu-id="6ecf0-117">2. példa</span><span class="sxs-lookup"><span data-stu-id="6ecf0-117">Example 2</span></span>
```powershell
PS C:\> Set-AzAdvisorConfiguration -LowCpuThreshold 15 -Exclude 
Id         : /subscriptions/{user_subscription}/resourceGroups/resourceGroupName1/providers/Microsoft.Advisor/configurations/{user_subscription}
Name       : {user_subscription}
Properties : additionalProperties : null
             exclude :  True
             lowCpuThreshold : 15

Type       : Microsoft.Advisor/Configurations
```

<span data-ttu-id="6ecf0-118">Frissíti az előfizetési szint konfigurációjának konfigurációját (lowCpuThreshold, kihagyása), és kizárja az ajánlás generálását.</span><span class="sxs-lookup"><span data-stu-id="6ecf0-118">Updates the configuration(lowCpuThreshold, exclude) for subscription level Configuration and excludes from the recommendation generation.</span></span>

### <span data-ttu-id="6ecf0-119">3. példa</span><span class="sxs-lookup"><span data-stu-id="6ecf0-119">Example 3</span></span>
```powershell
PS C:\> Set-AzAdvisorConfiguration -ResourceGroupName resourceGroupName1 -Exclude

Id         : /subscriptions/{user_subscription}/resourceGroups/resourceGroupName1/providers/Microsoft.Advisor/configurations/{user_subscription}-resourceGroupName1
Name       : {user_subscription}-resourceGroupName1
Properties : additionalProperties : null
             exclude :  True
             lowCpuThreshold : null

Type       : Microsoft.Advisor/Configurations
```

<span data-ttu-id="6ecf0-120">Frissíti a resourceGroupName1 kihagyott konfigurációt (kizár) az ajánlás generációjában.</span><span class="sxs-lookup"><span data-stu-id="6ecf0-120">Updates the configuration(exclude) for resourceGroupName1 to be excluded in the recommendation generation.</span></span>

### <span data-ttu-id="6ecf0-121">4. példa</span><span class="sxs-lookup"><span data-stu-id="6ecf0-121">Example 4</span></span>
```powershell
PS C:\> Get-AzAdvisorConfiguration | Set-AzAdvisorConfiguration -LowCpuThreshold 20
Id         : /subscriptions/{user_subscription}/resourceGroups/resourceGroupName1/providers/Microsoft.Advisor/configurations/{user_subscription}
Name       : {user_subscription}
Properties : additionalProperties : null
             exclude :  False
             lowCpuThreshold : 20

Type       : Microsoft.Advisor/Configurations
```

<span data-ttu-id="6ecf0-122">Frissíti a futószalagról átadott ajánlás konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="6ecf0-122">Updates the configuration for the given recommendation passed on from the pipeline.</span></span>

## <span data-ttu-id="6ecf0-123">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6ecf0-123">PARAMETERS</span></span>

### <span data-ttu-id="6ecf0-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6ecf0-124">-Confirm</span></span>
<span data-ttu-id="6ecf0-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6ecf0-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ecf0-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ecf0-126">-DefaultProfile</span></span>
<span data-ttu-id="6ecf0-127">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6ecf0-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ecf0-128">-Kizár</span><span class="sxs-lookup"><span data-stu-id="6ecf0-128">-Exclude</span></span>
<span data-ttu-id="6ecf0-129">Kizárhatja az ajánlás generációját.</span><span class="sxs-lookup"><span data-stu-id="6ecf0-129">Exclude from the recommendation generation.</span></span> <span data-ttu-id="6ecf0-130">Ha nem adja meg, hogy nincs-e kihagyva tulajdonság, a program FALSE értéket ad.</span><span class="sxs-lookup"><span data-stu-id="6ecf0-130">If not specified exclude property will be set to false.</span></span>

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

### <span data-ttu-id="6ecf0-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6ecf0-131">-InputObject</span></span>
<span data-ttu-id="6ecf0-132">Get-AzAdvisorConfiguration hívás által visszaadott PowerShell-objektum típusa: PsAzureAdvisorConfigurationData.</span><span class="sxs-lookup"><span data-stu-id="6ecf0-132">The powershell object type PsAzureAdvisorConfigurationData returned by Get-AzAdvisorConfiguration call.</span></span>

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

### <span data-ttu-id="6ecf0-133">-LowCpuThreshold</span><span class="sxs-lookup"><span data-stu-id="6ecf0-133">-LowCpuThreshold</span></span>
<span data-ttu-id="6ecf0-134">Az alacsony CPU-küszöb értékének értéke.</span><span class="sxs-lookup"><span data-stu-id="6ecf0-134">Value for Low Cpu threshold.</span></span>

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

### <span data-ttu-id="6ecf0-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ecf0-135">-ResourceGroupName</span></span>
<span data-ttu-id="6ecf0-136">A konfiguráció erőforráscsoport-neve.</span><span class="sxs-lookup"><span data-stu-id="6ecf0-136">Resource Group name for the configuration.</span></span>

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

### <span data-ttu-id="6ecf0-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ecf0-137">-WhatIf</span></span>
<span data-ttu-id="6ecf0-138">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6ecf0-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ecf0-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6ecf0-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ecf0-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ecf0-140">CommonParameters</span></span>
<span data-ttu-id="6ecf0-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6ecf0-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="6ecf0-142">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ecf0-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ecf0-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6ecf0-143">INPUTS</span></span>

### <span data-ttu-id="6ecf0-144">Microsoft. Azure. commands. Advisor. parancsmagok. models. PsAzureAdvisorConfigurationData</span><span class="sxs-lookup"><span data-stu-id="6ecf0-144">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorConfigurationData</span></span>

## <span data-ttu-id="6ecf0-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6ecf0-145">OUTPUTS</span></span>

### <span data-ttu-id="6ecf0-146">Microsoft. Azure. commands. Advisor. parancsmagok. models. PsAzureAdvisorConfigurationData</span><span class="sxs-lookup"><span data-stu-id="6ecf0-146">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorConfigurationData</span></span>

## <span data-ttu-id="6ecf0-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6ecf0-147">NOTES</span></span>

## <span data-ttu-id="6ecf0-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6ecf0-148">RELATED LINKS</span></span>
