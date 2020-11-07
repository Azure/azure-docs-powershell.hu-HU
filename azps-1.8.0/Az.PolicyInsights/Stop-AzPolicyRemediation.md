---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/stop-azpolicyremediation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Stop-AzPolicyRemediation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Stop-AzPolicyRemediation.md
ms.openlocfilehash: 2630b438fa9c5aaa691422be2da2d32e08112fba
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669822"
---
# <span data-ttu-id="36d90-101">Stop-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="36d90-101">Stop-AzPolicyRemediation</span></span>

## <span data-ttu-id="36d90-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="36d90-102">SYNOPSIS</span></span>
<span data-ttu-id="36d90-103">Visszavonja a folyamatban lévő házirend-szervizelést.</span><span class="sxs-lookup"><span data-stu-id="36d90-103">Cancels an in-progress policy remediation.</span></span>

## <span data-ttu-id="36d90-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="36d90-104">SYNTAX</span></span>

### <span data-ttu-id="36d90-105">ByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="36d90-105">ByName (Default)</span></span>
```
Stop-AzPolicyRemediation -Name <String> [-Scope <String>] [-ManagementGroupName <String>]
 [-ResourceGroupName <String>] [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36d90-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="36d90-106">ByResourceId</span></span>
```
Stop-AzPolicyRemediation -ResourceId <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36d90-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="36d90-107">ByInputObject</span></span>
```
Stop-AzPolicyRemediation -InputObject <PSRemediation> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36d90-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="36d90-108">DESCRIPTION</span></span>
<span data-ttu-id="36d90-109">A **stop-AzPolicyRemediation** parancsmag megszünteti a folyamatban lévő házirend-szervizelést.</span><span class="sxs-lookup"><span data-stu-id="36d90-109">The **Stop-AzPolicyRemediation** cmdlet cancels an in-progress policy remediation.</span></span> <span data-ttu-id="36d90-110">Az aktív üzembe állítások törlődnek, és a rendszer nem hoz létre új központi telepítőket.</span><span class="sxs-lookup"><span data-stu-id="36d90-110">Active deployments will be canceled and no new deployments will be created.</span></span>

## <span data-ttu-id="36d90-111">Példák</span><span class="sxs-lookup"><span data-stu-id="36d90-111">EXAMPLES</span></span>

### <span data-ttu-id="36d90-112">Példa 1: házirend-szervizelés megszüntetése az erőforráscsoport hatókörében</span><span class="sxs-lookup"><span data-stu-id="36d90-112">Example 1: Cancel a policy remediation at resource group scope</span></span>
```
PS C:\> Stop-AzPolicyRemediation -ResourceGroupName "myRG" -Name "remediation1"
```

<span data-ttu-id="36d90-113">Ez a parancs a "myRG" erőforráscsoport "remediation1" nevű szervizelését törli.</span><span class="sxs-lookup"><span data-stu-id="36d90-113">This command cancels the remediation named 'remediation1' in resource group 'myRG'.</span></span>

### <span data-ttu-id="36d90-114">2. példa: a kezelési csoport lemondása csővezetéken keresztüli szervizelésének lemondása</span><span class="sxs-lookup"><span data-stu-id="36d90-114">Example 2: Cancel a management group remediation via piping</span></span>
```
PS C:\> $remediation = Get-AzPolicyRemediation -ManagementGroupName "mg1" -Name "remediation1"
PS C:\> $remediation | Stop-AzPolicyRemediation
```

<span data-ttu-id="36d90-115">Ez a parancs lemondja a "remediation1" nevű "mg1" felügyeleti csoportban található "" nevű szervizelést.</span><span class="sxs-lookup"><span data-stu-id="36d90-115">This command cancels the remediation named 'remediation1' in management group 'mg1'.</span></span>

## <span data-ttu-id="36d90-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="36d90-116">PARAMETERS</span></span>

### <span data-ttu-id="36d90-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="36d90-117">-AsJob</span></span>
<span data-ttu-id="36d90-118">Futtassa a parancsmagot a háttérben.</span><span class="sxs-lookup"><span data-stu-id="36d90-118">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="36d90-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36d90-119">-DefaultProfile</span></span>
<span data-ttu-id="36d90-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="36d90-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36d90-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="36d90-121">-InputObject</span></span>
<span data-ttu-id="36d90-122">A Szervizelési objektum.</span><span class="sxs-lookup"><span data-stu-id="36d90-122">The Remediation object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="36d90-123">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="36d90-123">-ManagementGroupName</span></span>
<span data-ttu-id="36d90-124">Felügyeleti csoport azonosítója</span><span class="sxs-lookup"><span data-stu-id="36d90-124">Management group ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36d90-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="36d90-125">-Name</span></span>
<span data-ttu-id="36d90-126">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="36d90-126">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36d90-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="36d90-127">-PassThru</span></span>
<span data-ttu-id="36d90-128">Igaz érték visszaadása, ha a parancs sikeresen befejeződött.</span><span class="sxs-lookup"><span data-stu-id="36d90-128">Return True if the command completes successfully.</span></span>

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

### <span data-ttu-id="36d90-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36d90-129">-ResourceGroupName</span></span>
<span data-ttu-id="36d90-130">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="36d90-130">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36d90-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="36d90-131">-ResourceId</span></span>
<span data-ttu-id="36d90-132">Erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="36d90-132">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36d90-133">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="36d90-133">-Scope</span></span>
<span data-ttu-id="36d90-134">Az erőforrás hatóköre.</span><span class="sxs-lookup"><span data-stu-id="36d90-134">Scope of the resource.</span></span>
<span data-ttu-id="36d90-135">Pl.</span><span class="sxs-lookup"><span data-stu-id="36d90-135">E.g.</span></span>
<span data-ttu-id="36d90-136">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span><span class="sxs-lookup"><span data-stu-id="36d90-136">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36d90-137">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="36d90-137">-Confirm</span></span>
<span data-ttu-id="36d90-138">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="36d90-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36d90-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36d90-139">-WhatIf</span></span>
<span data-ttu-id="36d90-140">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="36d90-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36d90-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="36d90-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36d90-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36d90-142">CommonParameters</span></span>
<span data-ttu-id="36d90-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="36d90-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36d90-144">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36d90-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36d90-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="36d90-145">INPUTS</span></span>

### <span data-ttu-id="36d90-146">System. String</span><span class="sxs-lookup"><span data-stu-id="36d90-146">System.String</span></span>

### <span data-ttu-id="36d90-147">Microsoft. Azure. Command. PolicyInsights. models. remediáció. PSRemediation</span><span class="sxs-lookup"><span data-stu-id="36d90-147">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span></span>

## <span data-ttu-id="36d90-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="36d90-148">OUTPUTS</span></span>

### <span data-ttu-id="36d90-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="36d90-149">System.Boolean</span></span>

## <span data-ttu-id="36d90-150">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="36d90-150">NOTES</span></span>

## <span data-ttu-id="36d90-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="36d90-151">RELATED LINKS</span></span>
