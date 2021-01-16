---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.appconfiguration/new-azappconfigurationstorekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/New-AzAppConfigurationStoreKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/New-AzAppConfigurationStoreKey.md
ms.openlocfilehash: 922bc6f596611638c0ea7d27304e6ea3f0d62eeb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98322541"
---
# <span data-ttu-id="b0c56-101">New-AzAppConfigurationStoreKey</span><span class="sxs-lookup"><span data-stu-id="b0c56-101">New-AzAppConfigurationStoreKey</span></span>

## <span data-ttu-id="b0c56-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0c56-102">SYNOPSIS</span></span>
<span data-ttu-id="b0c56-103">A megadott konfigurációs tároló hozzáférési kulcsának újragenerálása.</span><span class="sxs-lookup"><span data-stu-id="b0c56-103">Regenerates an access key for the specified configuration store.</span></span>

## <span data-ttu-id="b0c56-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b0c56-104">SYNTAX</span></span>

### <span data-ttu-id="b0c56-105">RegenerateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b0c56-105">RegenerateExpanded (Default)</span></span>
```
New-AzAppConfigurationStoreKey -Name <String> -ResourceGroupName <String> -Id <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b0c56-106">RegenerateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="b0c56-106">RegenerateViaIdentityExpanded</span></span>
```
New-AzAppConfigurationStoreKey -InputObject <IAppConfigurationIdentity> -Id <String>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b0c56-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b0c56-107">DESCRIPTION</span></span>
<span data-ttu-id="b0c56-108">A megadott konfigurációs tároló hozzáférési kulcsának újragenerálása.</span><span class="sxs-lookup"><span data-stu-id="b0c56-108">Regenerates an access key for the specified configuration store.</span></span>

## <span data-ttu-id="b0c56-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b0c56-109">EXAMPLES</span></span>

### <span data-ttu-id="b0c56-110">1. példa: Az appkonfigurációs áruház kulcsának újragenerálása</span><span class="sxs-lookup"><span data-stu-id="b0c56-110">Example 1: Regenerate key of an app configuration store</span></span>
```powershell
PS C:\> $keys= Get-AzAppConfigurationStoreKey -Name appconfig-test01 -ResourceGroupName azpwsh-manual-test
PS C:\> New-AzAppConfigurationStoreKey -Name appconfig-test01 -ResourceGroupName azpwsh-manual-test -Id $keys[0].id

ConnectionString                                                                                                                     LastModified        Name      ReadOnly Value
----------------                                                                                                                     ------------        ----      -------- -----
Endpoint=https://appconfig-test01.azconfig.io;Id=09pv-l0-s0:opFCQMC6+9485xJgN5Ws;Secret=GcoE9e9t7GLRNJ910M46IrbHO/Vg0tt4HujRdsaCoTY= 5/8/2020 5:47:15 AM Secondary False    GcoE9e9t7GLRNJ910M46IrbHO/Vg0tt4HujRdsaCoTY=
```

<span data-ttu-id="b0c56-111">Ez a parancs újragenerálja egy alkalmazáskonfigurációs áruház kulcsát.</span><span class="sxs-lookup"><span data-stu-id="b0c56-111">This command regenerate key of an app configuration store.</span></span>

### <span data-ttu-id="b0c56-112">2. példa: Az appkonfigurációs tárolók kulcsának újragenerálása objektum szerint</span><span class="sxs-lookup"><span data-stu-id="b0c56-112">Example 2: Regenerate key of an app configuration store by object</span></span>
```powershell
PS C:\> $app= New-AzAppConfigurationStore -Name appconfig-test10 -ResourceGroupName azpwsh-manual-test
PS C:\> $keys= Get-AzAppConfigurationStoreKey -Name appconfig-test01 -ResourceGroupName azpwsh-manual-test
PS C:\> New-AzAppConfigurationStoreKey -InputObject $app -Id $keys[0].id
ConnectionString                                                                                                                     LastModified        Name      ReadOnly Value
----------------                                                                                                                     ------------        ----      -------- -----
Endpoint=https://appconfig-test01.azconfig.io;Id=09pv-l0-s0:opFCQMC6+9485xJgN5Ws;Secret=GcoE9e9t7GLRNJ910M46IrbHO/Vg0tt4HujRdsaCoTY= 5/8/2020 5:47:15 AM Secondary False    GcoE9e9t7GLRNJ910M46IrbHO/Vg0tt4HujRdsaCoTY=
```

<span data-ttu-id="b0c56-113">Ez a parancs objektum szerint újragenerálja az alkalmazáskonfigurációs tárolók kulcsát.</span><span class="sxs-lookup"><span data-stu-id="b0c56-113">This command regenerate key of an app configuration store by object.</span></span>

## <span data-ttu-id="b0c56-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b0c56-114">PARAMETERS</span></span>

### <span data-ttu-id="b0c56-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0c56-115">-DefaultProfile</span></span>
<span data-ttu-id="b0c56-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b0c56-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0c56-117">-Id</span><span class="sxs-lookup"><span data-stu-id="b0c56-117">-Id</span></span>
<span data-ttu-id="b0c56-118">Az újragenerálni megfelelő kulcs azonosítója.</span><span class="sxs-lookup"><span data-stu-id="b0c56-118">The id of the key to regenerate.</span></span>

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

### <span data-ttu-id="b0c56-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b0c56-119">-InputObject</span></span>
<span data-ttu-id="b0c56-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="b0c56-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b0c56-121">-Name</span><span class="sxs-lookup"><span data-stu-id="b0c56-121">-Name</span></span>
<span data-ttu-id="b0c56-122">A konfigurációs tároló neve.</span><span class="sxs-lookup"><span data-stu-id="b0c56-122">The name of the configuration store.</span></span>

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

### <span data-ttu-id="b0c56-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0c56-123">-ResourceGroupName</span></span>
<span data-ttu-id="b0c56-124">Annak az erőforráscsoportnak a neve, amelyhez a tároló beállításjegyzék tartozik.</span><span class="sxs-lookup"><span data-stu-id="b0c56-124">The name of the resource group to which the container registry belongs.</span></span>

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

### <span data-ttu-id="b0c56-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b0c56-125">-SubscriptionId</span></span>
<span data-ttu-id="b0c56-126">A Microsoft Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="b0c56-126">The Microsoft Azure subscription ID.</span></span>

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

### <span data-ttu-id="b0c56-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b0c56-127">-Confirm</span></span>
<span data-ttu-id="b0c56-128">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="b0c56-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0c56-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0c56-129">-WhatIf</span></span>
<span data-ttu-id="b0c56-130">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="b0c56-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b0c56-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b0c56-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0c56-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0c56-132">CommonParameters</span></span>
<span data-ttu-id="b0c56-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0c56-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0c56-134">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b0c56-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0c56-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b0c56-135">INPUTS</span></span>

### <span data-ttu-id="b0c56-136">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity</span><span class="sxs-lookup"><span data-stu-id="b0c56-136">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity</span></span>

## <span data-ttu-id="b0c56-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b0c56-137">OUTPUTS</span></span>

### <span data-ttu-id="b0c56-138">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IApiKey</span><span class="sxs-lookup"><span data-stu-id="b0c56-138">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IApiKey</span></span>

## <span data-ttu-id="b0c56-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b0c56-139">NOTES</span></span>

<span data-ttu-id="b0c56-140">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="b0c56-140">ALIASES</span></span>

<span data-ttu-id="b0c56-141">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="b0c56-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b0c56-142">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="b0c56-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b0c56-143">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b0c56-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b0c56-144">INPUTOBJECT: <IAppConfigurationIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="b0c56-144">INPUTOBJECT <IAppConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b0c56-145">`[ConfigStoreName <String>]`: A konfigurációs tároló neve.</span><span class="sxs-lookup"><span data-stu-id="b0c56-145">`[ConfigStoreName <String>]`: The name of the configuration store.</span></span>
  - <span data-ttu-id="b0c56-146">`[GroupName <String>]`: A privát csatolású erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="b0c56-146">`[GroupName <String>]`: The name of the private link resource group.</span></span>
  - <span data-ttu-id="b0c56-147">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="b0c56-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b0c56-148">`[PrivateEndpointConnectionName <String>]`: Private endpoint connection name</span><span class="sxs-lookup"><span data-stu-id="b0c56-148">`[PrivateEndpointConnectionName <String>]`: Private endpoint connection name</span></span>
  - <span data-ttu-id="b0c56-149">`[ResourceGroupName <String>]`: Annak az erőforráscsoportnak a neve, amelyhez a tároló beállításjegyzék tartozik.</span><span class="sxs-lookup"><span data-stu-id="b0c56-149">`[ResourceGroupName <String>]`: The name of the resource group to which the container registry belongs.</span></span>
  - <span data-ttu-id="b0c56-150">`[SubscriptionId <String>]`: A Microsoft Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="b0c56-150">`[SubscriptionId <String>]`: The Microsoft Azure subscription ID.</span></span>

## <span data-ttu-id="b0c56-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b0c56-151">RELATED LINKS</span></span>

