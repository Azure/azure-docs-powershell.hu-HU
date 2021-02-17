---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/stop-azpolicyremediation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Stop-AzPolicyRemediation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Stop-AzPolicyRemediation.md
ms.openlocfilehash: 9dfb3ff2f50df7a858ab8194ec86fa312501dcff
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100169442"
---
# <span data-ttu-id="fb59e-101">Stop-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="fb59e-101">Stop-AzPolicyRemediation</span></span>

## <span data-ttu-id="fb59e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb59e-102">SYNOPSIS</span></span>
<span data-ttu-id="fb59e-103">Megszakítja a folyamatban lévő házirendek szervizelését.</span><span class="sxs-lookup"><span data-stu-id="fb59e-103">Cancels an in-progress policy remediation.</span></span>

## <span data-ttu-id="fb59e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="fb59e-104">SYNTAX</span></span>

### <span data-ttu-id="fb59e-105">ByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fb59e-105">ByName (Default)</span></span>
```
Stop-AzPolicyRemediation -Name <String> [-Scope <String>] [-ManagementGroupName <String>]
 [-ResourceGroupName <String>] [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb59e-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="fb59e-106">ByResourceId</span></span>
```
Stop-AzPolicyRemediation -ResourceId <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb59e-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="fb59e-107">ByInputObject</span></span>
```
Stop-AzPolicyRemediation -InputObject <PSRemediation> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb59e-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="fb59e-108">DESCRIPTION</span></span>
<span data-ttu-id="fb59e-109">A **Stop-AzPolicyRemediation** parancsmag megszakítja a folyamatban lévő házirendek szervizelését.</span><span class="sxs-lookup"><span data-stu-id="fb59e-109">The **Stop-AzPolicyRemediation** cmdlet cancels an in-progress policy remediation.</span></span> <span data-ttu-id="fb59e-110">Az aktív telepítéseket a rendszer megszakítja, és nem jön létre új telepítés.</span><span class="sxs-lookup"><span data-stu-id="fb59e-110">Active deployments will be canceled and no new deployments will be created.</span></span>

## <span data-ttu-id="fb59e-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="fb59e-111">EXAMPLES</span></span>

### <span data-ttu-id="fb59e-112">1. példa: Házirend-szervizelés megszakítása az erőforráscsoport hatókörében</span><span class="sxs-lookup"><span data-stu-id="fb59e-112">Example 1: Cancel a policy remediation at resource group scope</span></span>
```
PS C:\> Stop-AzPolicyRemediation -ResourceGroupName "myRG" -Name "remediation1"
```

<span data-ttu-id="fb59e-113">Ez a parancs megszakítja a "szervizelés1" nevű szervizelést a "myRG" erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="fb59e-113">This command cancels the remediation named 'remediation1' in resource group 'myRG'.</span></span>

### <span data-ttu-id="fb59e-114">2. példa: Felügyeleti csoport szervizelésének megszakítása pipával</span><span class="sxs-lookup"><span data-stu-id="fb59e-114">Example 2: Cancel a management group remediation via piping</span></span>
```
PS C:\> $remediation = Get-AzPolicyRemediation -ManagementGroupName "mg1" -Name "remediation1"
PS C:\> $remediation | Stop-AzPolicyRemediation
```

<span data-ttu-id="fb59e-115">Ez a parancs megszakítja a "remediation1" (szervizelés1) nevű szervizelést a "1" felügyeleti csoportban.</span><span class="sxs-lookup"><span data-stu-id="fb59e-115">This command cancels the remediation named 'remediation1' in management group 'mg1'.</span></span>

## <span data-ttu-id="fb59e-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fb59e-116">PARAMETERS</span></span>

### <span data-ttu-id="fb59e-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fb59e-117">-AsJob</span></span>
<span data-ttu-id="fb59e-118">Futtassa a parancsmagot a háttérben.</span><span class="sxs-lookup"><span data-stu-id="fb59e-118">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="fb59e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb59e-119">-DefaultProfile</span></span>
<span data-ttu-id="fb59e-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fb59e-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb59e-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fb59e-121">-InputObject</span></span>
<span data-ttu-id="fb59e-122">A Szervizelés objektum.</span><span class="sxs-lookup"><span data-stu-id="fb59e-122">The Remediation object.</span></span>

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

### <span data-ttu-id="fb59e-123">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="fb59e-123">-ManagementGroupName</span></span>
<span data-ttu-id="fb59e-124">Felügyeleti csoport azonosítója.</span><span class="sxs-lookup"><span data-stu-id="fb59e-124">Management group ID.</span></span>

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

### <span data-ttu-id="fb59e-125">-Name</span><span class="sxs-lookup"><span data-stu-id="fb59e-125">-Name</span></span>
<span data-ttu-id="fb59e-126">Erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="fb59e-126">Resource name.</span></span>

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

### <span data-ttu-id="fb59e-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fb59e-127">-PassThru</span></span>
<span data-ttu-id="fb59e-128">Igaz érték visszaadva, ha a parancs sikeresen befejeződött.</span><span class="sxs-lookup"><span data-stu-id="fb59e-128">Return True if the command completes successfully.</span></span>

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

### <span data-ttu-id="fb59e-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb59e-129">-ResourceGroupName</span></span>
<span data-ttu-id="fb59e-130">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="fb59e-130">Resource group name.</span></span>

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

### <span data-ttu-id="fb59e-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fb59e-131">-ResourceId</span></span>
<span data-ttu-id="fb59e-132">Erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="fb59e-132">Resource ID.</span></span>

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

### <span data-ttu-id="fb59e-133">-Scope</span><span class="sxs-lookup"><span data-stu-id="fb59e-133">-Scope</span></span>
<span data-ttu-id="fb59e-134">Az erőforrás hatóköre.</span><span class="sxs-lookup"><span data-stu-id="fb59e-134">Scope of the resource.</span></span>
<span data-ttu-id="fb59e-135">Például:</span><span class="sxs-lookup"><span data-stu-id="fb59e-135">E.g.</span></span>
<span data-ttu-id="fb59e-136">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span><span class="sxs-lookup"><span data-stu-id="fb59e-136">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span></span>

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

### <span data-ttu-id="fb59e-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fb59e-137">-Confirm</span></span>
<span data-ttu-id="fb59e-138">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="fb59e-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb59e-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb59e-139">-WhatIf</span></span>
<span data-ttu-id="fb59e-140">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="fb59e-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb59e-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fb59e-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb59e-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb59e-142">CommonParameters</span></span>
<span data-ttu-id="fb59e-143">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb59e-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb59e-144">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fb59e-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb59e-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fb59e-145">INPUTS</span></span>

### <span data-ttu-id="fb59e-146">System.String</span><span class="sxs-lookup"><span data-stu-id="fb59e-146">System.String</span></span>

### <span data-ttu-id="fb59e-147">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span><span class="sxs-lookup"><span data-stu-id="fb59e-147">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span></span>

## <span data-ttu-id="fb59e-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fb59e-148">OUTPUTS</span></span>

### <span data-ttu-id="fb59e-149">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fb59e-149">System.Boolean</span></span>

## <span data-ttu-id="fb59e-150">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="fb59e-150">NOTES</span></span>

## <span data-ttu-id="fb59e-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fb59e-151">RELATED LINKS</span></span>
