---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/powershell/module/az.logicapp/remove-azintegrationaccountbatchconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountBatchConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountBatchConfiguration.md
ms.openlocfilehash: 24c5f3b93b2be446eed4e5b81e1e69bf2116aa8b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101923601"
---
# <span data-ttu-id="8b271-101">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="8b271-101">Remove-AzIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="8b271-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b271-102">SYNOPSIS</span></span>
<span data-ttu-id="8b271-103">Eltávolítja az integrációs fiók kötegkonfigurációját.</span><span class="sxs-lookup"><span data-stu-id="8b271-103">Removes an integration account batch configuration.</span></span>

## <span data-ttu-id="8b271-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8b271-104">SYNTAX</span></span>

### <span data-ttu-id="8b271-105">ByIntegrationAccount (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8b271-105">ByIntegrationAccount (Default)</span></span>
```
Remove-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b271-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="8b271-106">ByInputObject</span></span>
```
Remove-AzIntegrationAccountBatchConfiguration -InputObject <PSIntegrationAccountBatchConfiguration> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b271-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="8b271-107">ByResourceId</span></span>
```
Remove-AzIntegrationAccountBatchConfiguration -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b271-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8b271-108">DESCRIPTION</span></span>
<span data-ttu-id="8b271-109">A **Remove-AzIntegrationAccountBatchConfiguration** parancsmag eltávolít egy kötegkonfigurációt egy integrációs fiókból.</span><span class="sxs-lookup"><span data-stu-id="8b271-109">The **Remove-AzIntegrationAccountBatchConfiguration** cmdlet removes a batch configuration from an integration account.</span></span>

## <span data-ttu-id="8b271-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8b271-110">EXAMPLES</span></span>

### <span data-ttu-id="8b271-111">1. példa: Köteg-konfiguráció eltávolítása paraméterek alapján</span><span class="sxs-lookup"><span data-stu-id="8b271-111">Example 1: Remove a batch configuration by parameters</span></span>
```powershell
PS C:\> Remove-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig"
```

<span data-ttu-id="8b271-112">Eltávolítja a "sampleBatchConfig" nevű kötegkonfigurációt, amely a "sampleIntegrationAccount" integrációs fiókban található.</span><span class="sxs-lookup"><span data-stu-id="8b271-112">Removes the batch configuration named "sampleBatchConfig" located in the integration account "sampleIntegrationAccount".</span></span>

## <span data-ttu-id="8b271-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8b271-113">PARAMETERS</span></span>

### <span data-ttu-id="8b271-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b271-114">-DefaultProfile</span></span>
<span data-ttu-id="8b271-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8b271-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8b271-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8b271-116">-InputObject</span></span>
<span data-ttu-id="8b271-117">Egy integrációs fiók kötegkonfigurációja.</span><span class="sxs-lookup"><span data-stu-id="8b271-117">An integration account batch configuration.</span></span>

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

### <span data-ttu-id="8b271-118">-Name</span><span class="sxs-lookup"><span data-stu-id="8b271-118">-Name</span></span>
<span data-ttu-id="8b271-119">Az integrációs fiók kötegkonfigurációs neve.</span><span class="sxs-lookup"><span data-stu-id="8b271-119">The integration account batch configuration name.</span></span>

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

### <span data-ttu-id="8b271-120">-ParentName</span><span class="sxs-lookup"><span data-stu-id="8b271-120">-ParentName</span></span>
<span data-ttu-id="8b271-121">Az integrációs fiók neve.</span><span class="sxs-lookup"><span data-stu-id="8b271-121">The integration account name.</span></span>

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

### <span data-ttu-id="8b271-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8b271-122">-PassThru</span></span>
<span data-ttu-id="8b271-123">Adja vissza, hogy a parancs sikeres volt-e.</span><span class="sxs-lookup"><span data-stu-id="8b271-123">Return whether the command was successful or not.</span></span>

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

### <span data-ttu-id="8b271-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b271-124">-ResourceGroupName</span></span>
<span data-ttu-id="8b271-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="8b271-125">The resource group name.</span></span>

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

### <span data-ttu-id="8b271-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8b271-126">-ResourceId</span></span>
<span data-ttu-id="8b271-127">Az integrációs fiók köteg konfigurációs erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="8b271-127">The integration account batch configuration resource id.</span></span>

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

### <span data-ttu-id="8b271-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8b271-128">-Confirm</span></span>
<span data-ttu-id="8b271-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="8b271-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b271-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b271-130">-WhatIf</span></span>
<span data-ttu-id="8b271-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="8b271-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8b271-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8b271-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b271-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b271-133">CommonParameters</span></span>
<span data-ttu-id="8b271-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b271-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b271-135">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b271-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b271-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8b271-136">INPUTS</span></span>

### <span data-ttu-id="8b271-137">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="8b271-137">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span></span>

### <span data-ttu-id="8b271-138">System.String</span><span class="sxs-lookup"><span data-stu-id="8b271-138">System.String</span></span>

## <span data-ttu-id="8b271-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8b271-139">OUTPUTS</span></span>

### <span data-ttu-id="8b271-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8b271-140">System.Boolean</span></span>

## <span data-ttu-id="8b271-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8b271-141">NOTES</span></span>

## <span data-ttu-id="8b271-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8b271-142">RELATED LINKS</span></span>
