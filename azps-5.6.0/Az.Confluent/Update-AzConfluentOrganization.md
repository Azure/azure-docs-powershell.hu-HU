---
external help file: ''
Module Name: Az.Confluent
online version: https://docs.microsoft.com/powershell/module/az.confluent/update-azconfluentorganization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Confluent/help/Update-AzConfluentOrganization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Confluent/help/Update-AzConfluentOrganization.md
ms.openlocfilehash: 7332d3154e87da2d9249dc16e3986efd636b737a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012565"
---
# <span data-ttu-id="0f79f-101">Update-AzConfluentOrganization</span><span class="sxs-lookup"><span data-stu-id="0f79f-101">Update-AzConfluentOrganization</span></span>

## <span data-ttu-id="0f79f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f79f-102">SYNOPSIS</span></span>
<span data-ttu-id="0f79f-103">Szervezeti erőforrás frissítése</span><span class="sxs-lookup"><span data-stu-id="0f79f-103">Update Organization resource</span></span>

## <span data-ttu-id="0f79f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0f79f-104">SYNTAX</span></span>

### <span data-ttu-id="0f79f-105">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0f79f-105">UpdateExpanded (Default)</span></span>
```
Update-AzConfluentOrganization -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="0f79f-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="0f79f-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzConfluentOrganization -InputObject <IConfluentIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0f79f-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0f79f-107">DESCRIPTION</span></span>
<span data-ttu-id="0f79f-108">Szervezeti erőforrás frissítése</span><span class="sxs-lookup"><span data-stu-id="0f79f-108">Update Organization resource</span></span>

## <span data-ttu-id="0f79f-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0f79f-109">EXAMPLES</span></span>

### <span data-ttu-id="0f79f-110">1. példa: Összefolyásos szervezet frissítése név szerint</span><span class="sxs-lookup"><span data-stu-id="0f79f-110">Example 1: Update a confluent organization by name</span></span>
```powershell
PS C:\> pdate-AzConfluentOrganization -ResourceGroupName azure-rg-test -Name confluentorg-02-pwsh -Tag @{"key01" = "value01"}

Location Name                 Type
-------- ----                 ----
eastus   confluentorg-02-pwsh Microsoft.Confluent/organizations
```

<span data-ttu-id="0f79f-111">Ez a parancs név szerint frissíti a összefolyásos szervezetet.</span><span class="sxs-lookup"><span data-stu-id="0f79f-111">This command updates a confluent organization by name.</span></span>

### <span data-ttu-id="0f79f-112">2. példa: Összefolyásos szervezet frissítése folyamat szerint</span><span class="sxs-lookup"><span data-stu-id="0f79f-112">Example 2: Update a confluent organization by pipeline</span></span>
```powershell
PS C:\> Get-AzConfluentOrganization -ResourceGroupName azure-rg-test -Name confluentorg-02-pwsh | Update-AzConfluentOrganization -Tag @{"key01" = "value01"; "key02"="value02"}

Location Name                 Type
-------- ----                 ----
eastus   confluentorg-02-pwsh Microsoft.Confluent/organizations
```

<span data-ttu-id="0f79f-113">Ez a parancs egy összefolyásos szervezetet folyamat szerint frissíti.</span><span class="sxs-lookup"><span data-stu-id="0f79f-113">This command updates a confluent organization by pipeline.</span></span>

## <span data-ttu-id="0f79f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0f79f-114">PARAMETERS</span></span>

### <span data-ttu-id="0f79f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f79f-115">-DefaultProfile</span></span>
<span data-ttu-id="0f79f-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0f79f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0f79f-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0f79f-117">-InputObject</span></span>
<span data-ttu-id="0f79f-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="0f79f-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.IConfluentIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0f79f-119">-Name</span><span class="sxs-lookup"><span data-stu-id="0f79f-119">-Name</span></span>
<span data-ttu-id="0f79f-120">Szervezet erőforrásneve</span><span class="sxs-lookup"><span data-stu-id="0f79f-120">Organization resource name</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: OrganizationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f79f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f79f-121">-ResourceGroupName</span></span>
<span data-ttu-id="0f79f-122">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="0f79f-122">Resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f79f-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0f79f-123">-SubscriptionId</span></span>
<span data-ttu-id="0f79f-124">Microsoft Azure-előfizetés azonosítója</span><span class="sxs-lookup"><span data-stu-id="0f79f-124">Microsoft Azure subscription id</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f79f-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="0f79f-125">-Tag</span></span>
<span data-ttu-id="0f79f-126">ARM hozzárendelése erőforráscímkékhez</span><span class="sxs-lookup"><span data-stu-id="0f79f-126">ARM resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f79f-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0f79f-127">-Confirm</span></span>
<span data-ttu-id="0f79f-128">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="0f79f-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f79f-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f79f-129">-WhatIf</span></span>
<span data-ttu-id="0f79f-130">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="0f79f-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f79f-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0f79f-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f79f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f79f-132">CommonParameters</span></span>
<span data-ttu-id="0f79f-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f79f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f79f-134">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0f79f-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f79f-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0f79f-135">INPUTS</span></span>

### <span data-ttu-id="0f79f-136">Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.IConfluentIdentity</span><span class="sxs-lookup"><span data-stu-id="0f79f-136">Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.IConfluentIdentity</span></span>

## <span data-ttu-id="0f79f-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0f79f-137">OUTPUTS</span></span>

### <span data-ttu-id="0f79f-138">Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.Api20200301.IOrganizationResource</span><span class="sxs-lookup"><span data-stu-id="0f79f-138">Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.Api20200301.IOrganizationResource</span></span>

## <span data-ttu-id="0f79f-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0f79f-139">NOTES</span></span>

<span data-ttu-id="0f79f-140">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="0f79f-140">ALIASES</span></span>

<span data-ttu-id="0f79f-141">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="0f79f-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0f79f-142">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="0f79f-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0f79f-143">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0f79f-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0f79f-144">INPUTOBJECT: <IConfluentIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="0f79f-144">INPUTOBJECT <IConfluentIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0f79f-145">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="0f79f-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0f79f-146">`[OrganizationName <String>]`: Szervezet erőforrásneve</span><span class="sxs-lookup"><span data-stu-id="0f79f-146">`[OrganizationName <String>]`: Organization resource name</span></span>
  - <span data-ttu-id="0f79f-147">`[ResourceGroupName <String>]`: Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="0f79f-147">`[ResourceGroupName <String>]`: Resource group name</span></span>
  - <span data-ttu-id="0f79f-148">`[SubscriptionId <String>]`: Microsoft Azure-előfizetés azonosítója</span><span class="sxs-lookup"><span data-stu-id="0f79f-148">`[SubscriptionId <String>]`: Microsoft Azure subscription id</span></span>

## <span data-ttu-id="0f79f-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0f79f-149">RELATED LINKS</span></span>

