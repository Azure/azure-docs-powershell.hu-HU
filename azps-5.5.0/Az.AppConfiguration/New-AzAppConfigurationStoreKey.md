---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.appconfiguration/new-azappconfigurationstorekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/New-AzAppConfigurationStoreKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/New-AzAppConfigurationStoreKey.md
ms.openlocfilehash: 922bc6f596611638c0ea7d27304e6ea3f0d62eeb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100149531"
---
# <span data-ttu-id="d8d73-101">New-AzAppConfigurationStoreKey</span><span class="sxs-lookup"><span data-stu-id="d8d73-101">New-AzAppConfigurationStoreKey</span></span>

## <span data-ttu-id="d8d73-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8d73-102">SYNOPSIS</span></span>
<span data-ttu-id="d8d73-103">A megadott konfigurációs tároló hozzáférési kulcsának újragenerálása.</span><span class="sxs-lookup"><span data-stu-id="d8d73-103">Regenerates an access key for the specified configuration store.</span></span>

## <span data-ttu-id="d8d73-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d8d73-104">SYNTAX</span></span>

### <span data-ttu-id="d8d73-105">RegenerateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d8d73-105">RegenerateExpanded (Default)</span></span>
```
New-AzAppConfigurationStoreKey -Name <String> -ResourceGroupName <String> -Id <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d8d73-106">RegenerateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="d8d73-106">RegenerateViaIdentityExpanded</span></span>
```
New-AzAppConfigurationStoreKey -InputObject <IAppConfigurationIdentity> -Id <String>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d8d73-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d8d73-107">DESCRIPTION</span></span>
<span data-ttu-id="d8d73-108">A megadott konfigurációs tároló hozzáférési kulcsának újragenerálása.</span><span class="sxs-lookup"><span data-stu-id="d8d73-108">Regenerates an access key for the specified configuration store.</span></span>

## <span data-ttu-id="d8d73-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d8d73-109">EXAMPLES</span></span>

### <span data-ttu-id="d8d73-110">1. példa: Az appkonfigurációs áruház kulcsának újragenerálása</span><span class="sxs-lookup"><span data-stu-id="d8d73-110">Example 1: Regenerate key of an app configuration store</span></span>
```powershell
PS C:\> $keys= Get-AzAppConfigurationStoreKey -Name appconfig-test01 -ResourceGroupName azpwsh-manual-test
PS C:\> New-AzAppConfigurationStoreKey -Name appconfig-test01 -ResourceGroupName azpwsh-manual-test -Id $keys[0].id

ConnectionString                                                                                                                     LastModified        Name      ReadOnly Value
----------------                                                                                                                     ------------        ----      -------- -----
Endpoint=https://appconfig-test01.azconfig.io;Id=09pv-l0-s0:opFCQMC6+9485xJgN5Ws;Secret=GcoE9e9t7GLRNJ910M46IrbHO/Vg0tt4HujRdsaCoTY= 5/8/2020 5:47:15 AM Secondary False    GcoE9e9t7GLRNJ910M46IrbHO/Vg0tt4HujRdsaCoTY=
```

<span data-ttu-id="d8d73-111">Ez a parancs újragenerálja egy alkalmazáskonfigurációs áruház kulcsát.</span><span class="sxs-lookup"><span data-stu-id="d8d73-111">This command regenerate key of an app configuration store.</span></span>

### <span data-ttu-id="d8d73-112">2. példa: Az appkonfigurációs tárolók kulcsának újragenerálása objektum szerint</span><span class="sxs-lookup"><span data-stu-id="d8d73-112">Example 2: Regenerate key of an app configuration store by object</span></span>
```powershell
PS C:\> $app= New-AzAppConfigurationStore -Name appconfig-test10 -ResourceGroupName azpwsh-manual-test
PS C:\> $keys= Get-AzAppConfigurationStoreKey -Name appconfig-test01 -ResourceGroupName azpwsh-manual-test
PS C:\> New-AzAppConfigurationStoreKey -InputObject $app -Id $keys[0].id
ConnectionString                                                                                                                     LastModified        Name      ReadOnly Value
----------------                                                                                                                     ------------        ----      -------- -----
Endpoint=https://appconfig-test01.azconfig.io;Id=09pv-l0-s0:opFCQMC6+9485xJgN5Ws;Secret=GcoE9e9t7GLRNJ910M46IrbHO/Vg0tt4HujRdsaCoTY= 5/8/2020 5:47:15 AM Secondary False    GcoE9e9t7GLRNJ910M46IrbHO/Vg0tt4HujRdsaCoTY=
```

<span data-ttu-id="d8d73-113">Ez a parancs objektum szerint újragenerálja az alkalmazáskonfigurációs tárolók kulcsát.</span><span class="sxs-lookup"><span data-stu-id="d8d73-113">This command regenerate key of an app configuration store by object.</span></span>

## <span data-ttu-id="d8d73-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d8d73-114">PARAMETERS</span></span>

### <span data-ttu-id="d8d73-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8d73-115">-DefaultProfile</span></span>
<span data-ttu-id="d8d73-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d8d73-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8d73-117">-Id</span><span class="sxs-lookup"><span data-stu-id="d8d73-117">-Id</span></span>
<span data-ttu-id="d8d73-118">Az újragenerálni megfelelő kulcs azonosítója.</span><span class="sxs-lookup"><span data-stu-id="d8d73-118">The id of the key to regenerate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8d73-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d8d73-119">-InputObject</span></span>
<span data-ttu-id="d8d73-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="d8d73-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity
Parameter Sets: RegenerateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d8d73-121">-Name</span><span class="sxs-lookup"><span data-stu-id="d8d73-121">-Name</span></span>
<span data-ttu-id="d8d73-122">A konfigurációs tároló neve.</span><span class="sxs-lookup"><span data-stu-id="d8d73-122">The name of the configuration store.</span></span>

```yaml
Type: System.String
Parameter Sets: RegenerateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8d73-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8d73-123">-ResourceGroupName</span></span>
<span data-ttu-id="d8d73-124">Annak az erőforráscsoportnak a neve, amelyhez a tároló beállításjegyzék tartozik.</span><span class="sxs-lookup"><span data-stu-id="d8d73-124">The name of the resource group to which the container registry belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: RegenerateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8d73-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d8d73-125">-SubscriptionId</span></span>
<span data-ttu-id="d8d73-126">A Microsoft Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="d8d73-126">The Microsoft Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: RegenerateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8d73-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d8d73-127">-Confirm</span></span>
<span data-ttu-id="d8d73-128">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d8d73-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8d73-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8d73-129">-WhatIf</span></span>
<span data-ttu-id="d8d73-130">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="d8d73-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8d73-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d8d73-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8d73-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8d73-132">CommonParameters</span></span>
<span data-ttu-id="d8d73-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8d73-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8d73-134">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d8d73-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8d73-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d8d73-135">INPUTS</span></span>

### <span data-ttu-id="d8d73-136">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity</span><span class="sxs-lookup"><span data-stu-id="d8d73-136">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity</span></span>

## <span data-ttu-id="d8d73-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d8d73-137">OUTPUTS</span></span>

### <span data-ttu-id="d8d73-138">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IApiKey</span><span class="sxs-lookup"><span data-stu-id="d8d73-138">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IApiKey</span></span>

## <span data-ttu-id="d8d73-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d8d73-139">NOTES</span></span>

<span data-ttu-id="d8d73-140">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="d8d73-140">ALIASES</span></span>

<span data-ttu-id="d8d73-141">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="d8d73-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d8d73-142">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="d8d73-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d8d73-143">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d8d73-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d8d73-144">INPUTOBJECT: <IAppConfigurationIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="d8d73-144">INPUTOBJECT <IAppConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d8d73-145">`[ConfigStoreName <String>]`: A konfigurációs tároló neve.</span><span class="sxs-lookup"><span data-stu-id="d8d73-145">`[ConfigStoreName <String>]`: The name of the configuration store.</span></span>
  - <span data-ttu-id="d8d73-146">`[GroupName <String>]`: A privát csatolású erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="d8d73-146">`[GroupName <String>]`: The name of the private link resource group.</span></span>
  - <span data-ttu-id="d8d73-147">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="d8d73-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d8d73-148">`[PrivateEndpointConnectionName <String>]`: Private endpoint connection name</span><span class="sxs-lookup"><span data-stu-id="d8d73-148">`[PrivateEndpointConnectionName <String>]`: Private endpoint connection name</span></span>
  - <span data-ttu-id="d8d73-149">`[ResourceGroupName <String>]`: Annak az erőforráscsoportnak a neve, amelyhez a tároló beállításjegyzék tartozik.</span><span class="sxs-lookup"><span data-stu-id="d8d73-149">`[ResourceGroupName <String>]`: The name of the resource group to which the container registry belongs.</span></span>
  - <span data-ttu-id="d8d73-150">`[SubscriptionId <String>]`: A Microsoft Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="d8d73-150">`[SubscriptionId <String>]`: The Microsoft Azure subscription ID.</span></span>

## <span data-ttu-id="d8d73-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d8d73-151">RELATED LINKS</span></span>

