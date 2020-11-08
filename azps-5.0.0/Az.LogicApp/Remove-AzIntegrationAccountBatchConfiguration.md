---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccountbatchconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountBatchConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountBatchConfiguration.md
ms.openlocfilehash: 848ce0e0c5608271f1f8facb955aad2df95b6a0a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195840"
---
# <span data-ttu-id="110d6-101">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="110d6-101">Remove-AzIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="110d6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="110d6-102">SYNOPSIS</span></span>
<span data-ttu-id="110d6-103">Eltávolítja az integrációs fiók kötegének konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="110d6-103">Removes an integration account batch configuration.</span></span>

## <span data-ttu-id="110d6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="110d6-104">SYNTAX</span></span>

### <span data-ttu-id="110d6-105">ByIntegrationAccount (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="110d6-105">ByIntegrationAccount (Default)</span></span>
```
Remove-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="110d6-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="110d6-106">ByInputObject</span></span>
```
Remove-AzIntegrationAccountBatchConfiguration -InputObject <PSIntegrationAccountBatchConfiguration> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="110d6-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="110d6-107">ByResourceId</span></span>
```
Remove-AzIntegrationAccountBatchConfiguration -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="110d6-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="110d6-108">DESCRIPTION</span></span>
<span data-ttu-id="110d6-109">A **Remove-AzIntegrationAccountBatchConfiguration** parancsmag az integrációs fiókból távolítja el a köteg-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="110d6-109">The **Remove-AzIntegrationAccountBatchConfiguration** cmdlet removes a batch configuration from an integration account.</span></span>

## <span data-ttu-id="110d6-110">Példák</span><span class="sxs-lookup"><span data-stu-id="110d6-110">EXAMPLES</span></span>

### <span data-ttu-id="110d6-111">Példa 1: kötegfájl-konfiguráció eltávolítása paraméterek alapján</span><span class="sxs-lookup"><span data-stu-id="110d6-111">Example 1: Remove a batch configuration by parameters</span></span>
```powershell
PS C:\> Remove-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig"
```

<span data-ttu-id="110d6-112">Eltávolítja a "sampleBatchConfig" nevű köteg-konfigurációt az "sampleIntegrationAccount" integrációs fiókjában.</span><span class="sxs-lookup"><span data-stu-id="110d6-112">Removes the batch configuration named "sampleBatchConfig" located in the integration account "sampleIntegrationAccount".</span></span>

## <span data-ttu-id="110d6-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="110d6-113">PARAMETERS</span></span>

### <span data-ttu-id="110d6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="110d6-114">-DefaultProfile</span></span>
<span data-ttu-id="110d6-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="110d6-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="110d6-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="110d6-116">-InputObject</span></span>
<span data-ttu-id="110d6-117">Az integrációs fiók kötegének konfigurációja.</span><span class="sxs-lookup"><span data-stu-id="110d6-117">An integration account batch configuration.</span></span>

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

### <span data-ttu-id="110d6-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="110d6-118">-Name</span></span>
<span data-ttu-id="110d6-119">Az integrációs fiók kötegének neve.</span><span class="sxs-lookup"><span data-stu-id="110d6-119">The integration account batch configuration name.</span></span>

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

### <span data-ttu-id="110d6-120">-ParentName</span><span class="sxs-lookup"><span data-stu-id="110d6-120">-ParentName</span></span>
<span data-ttu-id="110d6-121">Az integrációs fiók neve.</span><span class="sxs-lookup"><span data-stu-id="110d6-121">The integration account name.</span></span>

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

### <span data-ttu-id="110d6-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="110d6-122">-PassThru</span></span>
<span data-ttu-id="110d6-123">Adja meg, hogy a parancs sikeres volt-e.</span><span class="sxs-lookup"><span data-stu-id="110d6-123">Return whether the command was successful or not.</span></span>

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

### <span data-ttu-id="110d6-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="110d6-124">-ResourceGroupName</span></span>
<span data-ttu-id="110d6-125">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="110d6-125">The resource group name.</span></span>

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

### <span data-ttu-id="110d6-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="110d6-126">-ResourceId</span></span>
<span data-ttu-id="110d6-127">Az integrációs fiók kötegének konfigurációs erőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="110d6-127">The integration account batch configuration resource id.</span></span>

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

### <span data-ttu-id="110d6-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="110d6-128">-Confirm</span></span>
<span data-ttu-id="110d6-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="110d6-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="110d6-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="110d6-130">-WhatIf</span></span>
<span data-ttu-id="110d6-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="110d6-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="110d6-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="110d6-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="110d6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="110d6-133">CommonParameters</span></span>
<span data-ttu-id="110d6-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="110d6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="110d6-135">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="110d6-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="110d6-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="110d6-136">INPUTS</span></span>

### <span data-ttu-id="110d6-137">Microsoft. Azure. Command. LogicApp. models. PSIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="110d6-137">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span></span>

### <span data-ttu-id="110d6-138">System. String</span><span class="sxs-lookup"><span data-stu-id="110d6-138">System.String</span></span>

## <span data-ttu-id="110d6-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="110d6-139">OUTPUTS</span></span>

### <span data-ttu-id="110d6-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="110d6-140">System.Boolean</span></span>

## <span data-ttu-id="110d6-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="110d6-141">NOTES</span></span>

## <span data-ttu-id="110d6-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="110d6-142">RELATED LINKS</span></span>
