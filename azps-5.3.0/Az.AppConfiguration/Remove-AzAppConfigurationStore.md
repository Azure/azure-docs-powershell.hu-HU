---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.appconfiguration/remove-azappconfigurationstore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Remove-AzAppConfigurationStore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Remove-AzAppConfigurationStore.md
ms.openlocfilehash: b0939a4baa498532a3b519875183e6d1d12945a7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98381442"
---
# <span data-ttu-id="dc0a7-101">Remove-AzAppConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="dc0a7-101">Remove-AzAppConfigurationStore</span></span>

## <span data-ttu-id="dc0a7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dc0a7-102">SYNOPSIS</span></span>
<span data-ttu-id="dc0a7-103">Törli a konfigurációs tárolót.</span><span class="sxs-lookup"><span data-stu-id="dc0a7-103">Deletes a configuration store.</span></span>

## <span data-ttu-id="dc0a7-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="dc0a7-104">SYNTAX</span></span>

### <span data-ttu-id="dc0a7-105">Törlés (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="dc0a7-105">Delete (Default)</span></span>
```
Remove-AzAppConfigurationStore -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="dc0a7-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="dc0a7-106">DeleteViaIdentity</span></span>
```
Remove-AzAppConfigurationStore -InputObject <IAppConfigurationIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="dc0a7-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="dc0a7-107">DESCRIPTION</span></span>
<span data-ttu-id="dc0a7-108">Törli a konfigurációs tárolót.</span><span class="sxs-lookup"><span data-stu-id="dc0a7-108">Deletes a configuration store.</span></span>

## <span data-ttu-id="dc0a7-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="dc0a7-109">EXAMPLES</span></span>

### <span data-ttu-id="dc0a7-110">1. példa: Alkalmazáskonfigurációs áruház eltávolítása</span><span class="sxs-lookup"><span data-stu-id="dc0a7-110">Example 1: Remove an app configuration store</span></span>
```powershell
PS C:\> Remove-AzAppConfigurationStore -Name appconfig-test03 -ResourceGroupName lucas-manual-test

```

<span data-ttu-id="dc0a7-111">Ez a parancs eltávolítja az alkalmazáskonfigurációs áruházat.</span><span class="sxs-lookup"><span data-stu-id="dc0a7-111">This command removes an app configuration store.</span></span>

### <span data-ttu-id="dc0a7-112">2. példa: Alkalmazáskonfigurációs áruház eltávolítása</span><span class="sxs-lookup"><span data-stu-id="dc0a7-112">Example 2: Remove an app configuration store</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore -Name appconfig-test02 -ResourceGroupName lucas-manual-test | Remove-AzAppConfigurationStore

```

<span data-ttu-id="dc0a7-113">Ez a parancs eltávolítja az alkalmazáskonfigurációs áruházat.</span><span class="sxs-lookup"><span data-stu-id="dc0a7-113">This command removes an app configuration store.</span></span>

## <span data-ttu-id="dc0a7-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dc0a7-114">PARAMETERS</span></span>

### <span data-ttu-id="dc0a7-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dc0a7-115">-AsJob</span></span>
<span data-ttu-id="dc0a7-116">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="dc0a7-116">Run the command as a job</span></span>

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

### <span data-ttu-id="dc0a7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc0a7-117">-DefaultProfile</span></span>
<span data-ttu-id="dc0a7-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="dc0a7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc0a7-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dc0a7-119">-InputObject</span></span>
<span data-ttu-id="dc0a7-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="dc0a7-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dc0a7-121">-Name</span><span class="sxs-lookup"><span data-stu-id="dc0a7-121">-Name</span></span>
<span data-ttu-id="dc0a7-122">A konfigurációs tároló neve.</span><span class="sxs-lookup"><span data-stu-id="dc0a7-122">The name of the configuration store.</span></span>

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

### <span data-ttu-id="dc0a7-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="dc0a7-123">-NoWait</span></span>
<span data-ttu-id="dc0a7-124">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="dc0a7-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="dc0a7-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dc0a7-125">-PassThru</span></span>
<span data-ttu-id="dc0a7-126">Igaz értéket ad vissza, ha a parancs sikeres</span><span class="sxs-lookup"><span data-stu-id="dc0a7-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="dc0a7-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc0a7-127">-ResourceGroupName</span></span>
<span data-ttu-id="dc0a7-128">Annak az erőforráscsoportnak a neve, amelyhez a tároló beállításjegyzék tartozik.</span><span class="sxs-lookup"><span data-stu-id="dc0a7-128">The name of the resource group to which the container registry belongs.</span></span>

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

### <span data-ttu-id="dc0a7-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="dc0a7-129">-SubscriptionId</span></span>
<span data-ttu-id="dc0a7-130">A Microsoft Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="dc0a7-130">The Microsoft Azure subscription ID.</span></span>

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

### <span data-ttu-id="dc0a7-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dc0a7-131">-Confirm</span></span>
<span data-ttu-id="dc0a7-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="dc0a7-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc0a7-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc0a7-133">-WhatIf</span></span>
<span data-ttu-id="dc0a7-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="dc0a7-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dc0a7-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="dc0a7-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc0a7-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc0a7-136">CommonParameters</span></span>
<span data-ttu-id="dc0a7-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc0a7-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc0a7-138">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dc0a7-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc0a7-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dc0a7-139">INPUTS</span></span>

### <span data-ttu-id="dc0a7-140">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity</span><span class="sxs-lookup"><span data-stu-id="dc0a7-140">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity</span></span>

## <span data-ttu-id="dc0a7-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dc0a7-141">OUTPUTS</span></span>

### <span data-ttu-id="dc0a7-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="dc0a7-142">System.Boolean</span></span>

## <span data-ttu-id="dc0a7-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="dc0a7-143">NOTES</span></span>

<span data-ttu-id="dc0a7-144">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="dc0a7-144">ALIASES</span></span>

<span data-ttu-id="dc0a7-145">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="dc0a7-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="dc0a7-146">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="dc0a7-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="dc0a7-147">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="dc0a7-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="dc0a7-148">INPUTOBJECT: <IAppConfigurationIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="dc0a7-148">INPUTOBJECT <IAppConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="dc0a7-149">`[ConfigStoreName <String>]`: A konfigurációs tároló neve.</span><span class="sxs-lookup"><span data-stu-id="dc0a7-149">`[ConfigStoreName <String>]`: The name of the configuration store.</span></span>
  - <span data-ttu-id="dc0a7-150">`[GroupName <String>]`: A privát csatolású erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="dc0a7-150">`[GroupName <String>]`: The name of the private link resource group.</span></span>
  - <span data-ttu-id="dc0a7-151">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="dc0a7-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="dc0a7-152">`[PrivateEndpointConnectionName <String>]`: Private endpoint connection name</span><span class="sxs-lookup"><span data-stu-id="dc0a7-152">`[PrivateEndpointConnectionName <String>]`: Private endpoint connection name</span></span>
  - <span data-ttu-id="dc0a7-153">`[ResourceGroupName <String>]`: Annak az erőforráscsoportnak a neve, amelyhez a tároló beállításjegyzék tartozik.</span><span class="sxs-lookup"><span data-stu-id="dc0a7-153">`[ResourceGroupName <String>]`: The name of the resource group to which the container registry belongs.</span></span>
  - <span data-ttu-id="dc0a7-154">`[SubscriptionId <String>]`: A Microsoft Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="dc0a7-154">`[SubscriptionId <String>]`: The Microsoft Azure subscription ID.</span></span>

## <span data-ttu-id="dc0a7-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dc0a7-155">RELATED LINKS</span></span>

