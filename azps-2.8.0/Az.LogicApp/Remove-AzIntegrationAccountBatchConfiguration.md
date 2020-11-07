---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccountbatchconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountBatchConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountBatchConfiguration.md
ms.openlocfilehash: e2c4f3f399bd4bcd472ae04c6ca2234c2d2b26d2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666033"
---
# <span data-ttu-id="5ed0f-101">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="5ed0f-101">Remove-AzIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="5ed0f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5ed0f-102">SYNOPSIS</span></span>
<span data-ttu-id="5ed0f-103">Eltávolítja az integrációs fiók kötegének konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="5ed0f-103">Removes an integration account batch configuration.</span></span>

## <span data-ttu-id="5ed0f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5ed0f-104">SYNTAX</span></span>

### <span data-ttu-id="5ed0f-105">ByIntegrationAccount (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5ed0f-105">ByIntegrationAccount (Default)</span></span>
```
Remove-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ed0f-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="5ed0f-106">ByInputObject</span></span>
```
Remove-AzIntegrationAccountBatchConfiguration -InputObject <PSIntegrationAccountBatchConfiguration> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ed0f-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="5ed0f-107">ByResourceId</span></span>
```
Remove-AzIntegrationAccountBatchConfiguration -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ed0f-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="5ed0f-108">DESCRIPTION</span></span>
<span data-ttu-id="5ed0f-109">A **Remove-AzIntegrationAccountBatchConfiguration** parancsmag az integrációs fiókból távolítja el a köteg-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="5ed0f-109">The **Remove-AzIntegrationAccountBatchConfiguration** cmdlet removes a batch configuration from an integration account.</span></span>

## <span data-ttu-id="5ed0f-110">Példák</span><span class="sxs-lookup"><span data-stu-id="5ed0f-110">EXAMPLES</span></span>

### <span data-ttu-id="5ed0f-111">Példa 1: kötegfájl-konfiguráció eltávolítása paraméterek alapján</span><span class="sxs-lookup"><span data-stu-id="5ed0f-111">Example 1: Remove a batch configuration by parameters</span></span>
```powershell
PS C:\> Remove-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig"
```

<span data-ttu-id="5ed0f-112">Eltávolítja a "sampleBatchConfig" nevű köteg-konfigurációt az "sampleIntegrationAccount" integrációs fiókjában.</span><span class="sxs-lookup"><span data-stu-id="5ed0f-112">Removes the batch configuration named "sampleBatchConfig" located in the integration account "sampleIntegrationAccount".</span></span>

## <span data-ttu-id="5ed0f-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5ed0f-113">PARAMETERS</span></span>

### <span data-ttu-id="5ed0f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ed0f-114">-DefaultProfile</span></span>
<span data-ttu-id="5ed0f-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5ed0f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ed0f-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5ed0f-116">-InputObject</span></span>
<span data-ttu-id="5ed0f-117">Az integrációs fiók kötegének konfigurációja.</span><span class="sxs-lookup"><span data-stu-id="5ed0f-117">An integration account batch configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5ed0f-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5ed0f-118">-Name</span></span>
<span data-ttu-id="5ed0f-119">Az integrációs fiók kötegének neve.</span><span class="sxs-lookup"><span data-stu-id="5ed0f-119">The integration account batch configuration name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccount
Aliases: BatchConfigurationName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ed0f-120">-ParentName</span><span class="sxs-lookup"><span data-stu-id="5ed0f-120">-ParentName</span></span>
<span data-ttu-id="5ed0f-121">Az integrációs fiók neve.</span><span class="sxs-lookup"><span data-stu-id="5ed0f-121">The integration account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccount
Aliases: IntegrationAccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ed0f-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5ed0f-122">-PassThru</span></span>
<span data-ttu-id="5ed0f-123">Adja meg, hogy a parancs sikeres volt-e.</span><span class="sxs-lookup"><span data-stu-id="5ed0f-123">Return whether the command was successful or not.</span></span>

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

### <span data-ttu-id="5ed0f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ed0f-124">-ResourceGroupName</span></span>
<span data-ttu-id="5ed0f-125">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="5ed0f-125">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccount
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ed0f-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5ed0f-126">-ResourceId</span></span>
<span data-ttu-id="5ed0f-127">Az integrációs fiók kötegének konfigurációs erőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="5ed0f-127">The integration account batch configuration resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ed0f-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5ed0f-128">-Confirm</span></span>
<span data-ttu-id="5ed0f-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5ed0f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ed0f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ed0f-130">-WhatIf</span></span>
<span data-ttu-id="5ed0f-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5ed0f-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5ed0f-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5ed0f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ed0f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ed0f-133">CommonParameters</span></span>
<span data-ttu-id="5ed0f-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5ed0f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ed0f-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ed0f-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ed0f-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5ed0f-136">INPUTS</span></span>

### <span data-ttu-id="5ed0f-137">Microsoft. Azure. Command. LogicApp. models. PSIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="5ed0f-137">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span></span>

### <span data-ttu-id="5ed0f-138">System. String</span><span class="sxs-lookup"><span data-stu-id="5ed0f-138">System.String</span></span>

## <span data-ttu-id="5ed0f-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5ed0f-139">OUTPUTS</span></span>

### <span data-ttu-id="5ed0f-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5ed0f-140">System.Boolean</span></span>

## <span data-ttu-id="5ed0f-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5ed0f-141">NOTES</span></span>

## <span data-ttu-id="5ed0f-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5ed0f-142">RELATED LINKS</span></span>
