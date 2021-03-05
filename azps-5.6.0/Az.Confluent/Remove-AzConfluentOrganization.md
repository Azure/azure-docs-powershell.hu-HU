---
external help file: ''
Module Name: Az.Confluent
online version: https://docs.microsoft.com/powershell/module/az.confluent/remove-azconfluentorganization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Confluent/help/Remove-AzConfluentOrganization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Confluent/help/Remove-AzConfluentOrganization.md
ms.openlocfilehash: d35de003bd4822758fd75c7dbbcf616ebecbbccb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012550"
---
# <span data-ttu-id="a51f1-101">Remove-AzConfluentOrganization</span><span class="sxs-lookup"><span data-stu-id="a51f1-101">Remove-AzConfluentOrganization</span></span>

## <span data-ttu-id="a51f1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a51f1-102">SYNOPSIS</span></span>
<span data-ttu-id="a51f1-103">Szervezeti erőforrás törlése</span><span class="sxs-lookup"><span data-stu-id="a51f1-103">Delete Organization resource</span></span>

## <span data-ttu-id="a51f1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a51f1-104">SYNTAX</span></span>

### <span data-ttu-id="a51f1-105">Törlés (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a51f1-105">Delete (Default)</span></span>
```
Remove-AzConfluentOrganization -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a51f1-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a51f1-106">DeleteViaIdentity</span></span>
```
Remove-AzConfluentOrganization -InputObject <IConfluentIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a51f1-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a51f1-107">DESCRIPTION</span></span>
<span data-ttu-id="a51f1-108">Szervezeti erőforrás törlése</span><span class="sxs-lookup"><span data-stu-id="a51f1-108">Delete Organization resource</span></span>

## <span data-ttu-id="a51f1-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a51f1-109">EXAMPLES</span></span>

### <span data-ttu-id="a51f1-110">1. példa: Összefolyásos szervezet eltávolítása név szerint</span><span class="sxs-lookup"><span data-stu-id="a51f1-110">Example 1: Remove a confluent organization by name</span></span>
```powershell
PS C:\> Remove-AzConfluentOrganization -ResourceGroupName azure-rg-test -Name confluentorg-01-portal

```

<span data-ttu-id="a51f1-111">Ez a parancs eltávolítja a összefolyásos szervezetet név szerint</span><span class="sxs-lookup"><span data-stu-id="a51f1-111">This command removes a confluent organization by name</span></span>

### <span data-ttu-id="a51f1-112">2. példa: Összefolyásos szervezet eltávolítása folyamat szerint</span><span class="sxs-lookup"><span data-stu-id="a51f1-112">Example 2: Remove a confluent organization by pipeline</span></span>
```powershell
PS C:\>  Get-AzConfluentOrganization -ResourceGroupName azure-rg-test -Name confluentorg-02-pwsh | Remove-AzConfluentOrganization

```

<span data-ttu-id="a51f1-113">Ez a parancs egy folyamat szerint eltávolítja a összefolyásos szervezetet.</span><span class="sxs-lookup"><span data-stu-id="a51f1-113">This command removes a confluent organization by pipeline.</span></span>

## <span data-ttu-id="a51f1-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a51f1-114">PARAMETERS</span></span>

### <span data-ttu-id="a51f1-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a51f1-115">-AsJob</span></span>
<span data-ttu-id="a51f1-116">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="a51f1-116">Run the command as a job</span></span>

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

### <span data-ttu-id="a51f1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a51f1-117">-DefaultProfile</span></span>
<span data-ttu-id="a51f1-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a51f1-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a51f1-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a51f1-119">-InputObject</span></span>
<span data-ttu-id="a51f1-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="a51f1-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.IConfluentIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a51f1-121">-Name</span><span class="sxs-lookup"><span data-stu-id="a51f1-121">-Name</span></span>
<span data-ttu-id="a51f1-122">Szervezet erőforrásneve</span><span class="sxs-lookup"><span data-stu-id="a51f1-122">Organization resource name</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: OrganizationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a51f1-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="a51f1-123">-NoWait</span></span>
<span data-ttu-id="a51f1-124">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="a51f1-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="a51f1-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a51f1-125">-PassThru</span></span>
<span data-ttu-id="a51f1-126">Igaz értéket ad vissza, ha a parancs sikeres</span><span class="sxs-lookup"><span data-stu-id="a51f1-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="a51f1-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a51f1-127">-ResourceGroupName</span></span>
<span data-ttu-id="a51f1-128">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="a51f1-128">Resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a51f1-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a51f1-129">-SubscriptionId</span></span>
<span data-ttu-id="a51f1-130">Microsoft Azure-előfizetés azonosítója</span><span class="sxs-lookup"><span data-stu-id="a51f1-130">Microsoft Azure subscription id</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a51f1-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a51f1-131">-Confirm</span></span>
<span data-ttu-id="a51f1-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="a51f1-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a51f1-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a51f1-133">-WhatIf</span></span>
<span data-ttu-id="a51f1-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="a51f1-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a51f1-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a51f1-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a51f1-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a51f1-136">CommonParameters</span></span>
<span data-ttu-id="a51f1-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a51f1-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a51f1-138">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a51f1-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a51f1-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a51f1-139">INPUTS</span></span>

### <span data-ttu-id="a51f1-140">Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.IConfluentIdentity</span><span class="sxs-lookup"><span data-stu-id="a51f1-140">Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.IConfluentIdentity</span></span>

## <span data-ttu-id="a51f1-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a51f1-141">OUTPUTS</span></span>

### <span data-ttu-id="a51f1-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a51f1-142">System.Boolean</span></span>

## <span data-ttu-id="a51f1-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a51f1-143">NOTES</span></span>

<span data-ttu-id="a51f1-144">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="a51f1-144">ALIASES</span></span>

<span data-ttu-id="a51f1-145">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="a51f1-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a51f1-146">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="a51f1-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a51f1-147">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a51f1-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a51f1-148">INPUTOBJECT: <IConfluentIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="a51f1-148">INPUTOBJECT <IConfluentIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a51f1-149">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="a51f1-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a51f1-150">`[OrganizationName <String>]`: Szervezet erőforrásneve</span><span class="sxs-lookup"><span data-stu-id="a51f1-150">`[OrganizationName <String>]`: Organization resource name</span></span>
  - <span data-ttu-id="a51f1-151">`[ResourceGroupName <String>]`: Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="a51f1-151">`[ResourceGroupName <String>]`: Resource group name</span></span>
  - <span data-ttu-id="a51f1-152">`[SubscriptionId <String>]`: Microsoft Azure-előfizetés azonosítója</span><span class="sxs-lookup"><span data-stu-id="a51f1-152">`[SubscriptionId <String>]`: Microsoft Azure subscription id</span></span>

## <span data-ttu-id="a51f1-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a51f1-153">RELATED LINKS</span></span>

