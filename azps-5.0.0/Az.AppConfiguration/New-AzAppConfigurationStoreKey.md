---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.appconfiguration/new-azappconfigurationstorekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/New-AzAppConfigurationStoreKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/New-AzAppConfigurationStoreKey.md
ms.openlocfilehash: 922bc6f596611638c0ea7d27304e6ea3f0d62eeb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186448"
---
# <span data-ttu-id="cf904-101">New-AzAppConfigurationStoreKey</span><span class="sxs-lookup"><span data-stu-id="cf904-101">New-AzAppConfigurationStoreKey</span></span>

## <span data-ttu-id="cf904-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cf904-102">SYNOPSIS</span></span>
<span data-ttu-id="cf904-103">Újra létrehoz egy Access-kulcsot a megadott konfigurációs tárolóhoz.</span><span class="sxs-lookup"><span data-stu-id="cf904-103">Regenerates an access key for the specified configuration store.</span></span>

## <span data-ttu-id="cf904-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cf904-104">SYNTAX</span></span>

### <span data-ttu-id="cf904-105">RegenerateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cf904-105">RegenerateExpanded (Default)</span></span>
```
New-AzAppConfigurationStoreKey -Name <String> -ResourceGroupName <String> -Id <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="cf904-106">RegenerateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="cf904-106">RegenerateViaIdentityExpanded</span></span>
```
New-AzAppConfigurationStoreKey -InputObject <IAppConfigurationIdentity> -Id <String>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="cf904-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="cf904-107">DESCRIPTION</span></span>
<span data-ttu-id="cf904-108">Újra létrehoz egy Access-kulcsot a megadott konfigurációs tárolóhoz.</span><span class="sxs-lookup"><span data-stu-id="cf904-108">Regenerates an access key for the specified configuration store.</span></span>

## <span data-ttu-id="cf904-109">Példák</span><span class="sxs-lookup"><span data-stu-id="cf904-109">EXAMPLES</span></span>

### <span data-ttu-id="cf904-110">1. példa: egy app konfigurációs áruház kulcsának újragenerálása</span><span class="sxs-lookup"><span data-stu-id="cf904-110">Example 1: Regenerate key of an app configuration store</span></span>
```powershell
PS C:\> $keys= Get-AzAppConfigurationStoreKey -Name appconfig-test01 -ResourceGroupName azpwsh-manual-test
PS C:\> New-AzAppConfigurationStoreKey -Name appconfig-test01 -ResourceGroupName azpwsh-manual-test -Id $keys[0].id

ConnectionString                                                                                                                     LastModified        Name      ReadOnly Value
----------------                                                                                                                     ------------        ----      -------- -----
Endpoint=https://appconfig-test01.azconfig.io;Id=09pv-l0-s0:opFCQMC6+9485xJgN5Ws;Secret=GcoE9e9t7GLRNJ910M46IrbHO/Vg0tt4HujRdsaCoTY= 5/8/2020 5:47:15 AM Secondary False    GcoE9e9t7GLRNJ910M46IrbHO/Vg0tt4HujRdsaCoTY=
```

<span data-ttu-id="cf904-111">Ez a parancs újra létrehoz egy app konfigurációs áruház kulcsát.</span><span class="sxs-lookup"><span data-stu-id="cf904-111">This command regenerate key of an app configuration store.</span></span>

### <span data-ttu-id="cf904-112">2. példa: az App Configuration Store objektumának újragenerálása objektum szerint</span><span class="sxs-lookup"><span data-stu-id="cf904-112">Example 2: Regenerate key of an app configuration store by object</span></span>
```powershell
PS C:\> $app= New-AzAppConfigurationStore -Name appconfig-test10 -ResourceGroupName azpwsh-manual-test
PS C:\> $keys= Get-AzAppConfigurationStoreKey -Name appconfig-test01 -ResourceGroupName azpwsh-manual-test
PS C:\> New-AzAppConfigurationStoreKey -InputObject $app -Id $keys[0].id
ConnectionString                                                                                                                     LastModified        Name      ReadOnly Value
----------------                                                                                                                     ------------        ----      -------- -----
Endpoint=https://appconfig-test01.azconfig.io;Id=09pv-l0-s0:opFCQMC6+9485xJgN5Ws;Secret=GcoE9e9t7GLRNJ910M46IrbHO/Vg0tt4HujRdsaCoTY= 5/8/2020 5:47:15 AM Secondary False    GcoE9e9t7GLRNJ910M46IrbHO/Vg0tt4HujRdsaCoTY=
```

<span data-ttu-id="cf904-113">Ezzel a paranccsal létrehozhatja az App Configuration Store objektumának kulcsát.</span><span class="sxs-lookup"><span data-stu-id="cf904-113">This command regenerate key of an app configuration store by object.</span></span>

## <span data-ttu-id="cf904-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cf904-114">PARAMETERS</span></span>

### <span data-ttu-id="cf904-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf904-115">-DefaultProfile</span></span>
<span data-ttu-id="cf904-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cf904-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf904-117">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="cf904-117">-Id</span></span>
<span data-ttu-id="cf904-118">Az újragenerálni kívánt kulcs azonosítója.</span><span class="sxs-lookup"><span data-stu-id="cf904-118">The id of the key to regenerate.</span></span>

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

### <span data-ttu-id="cf904-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cf904-119">-InputObject</span></span>
<span data-ttu-id="cf904-120">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="cf904-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="cf904-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="cf904-121">-Name</span></span>
<span data-ttu-id="cf904-122">A konfigurációs tároló neve.</span><span class="sxs-lookup"><span data-stu-id="cf904-122">The name of the configuration store.</span></span>

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

### <span data-ttu-id="cf904-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf904-123">-ResourceGroupName</span></span>
<span data-ttu-id="cf904-124">Annak az erőforráscsoportnek a neve, amelyhez a tároló beállításjegyzéke tartozik.</span><span class="sxs-lookup"><span data-stu-id="cf904-124">The name of the resource group to which the container registry belongs.</span></span>

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

### <span data-ttu-id="cf904-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cf904-125">-SubscriptionId</span></span>
<span data-ttu-id="cf904-126">A Microsoft Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="cf904-126">The Microsoft Azure subscription ID.</span></span>

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

### <span data-ttu-id="cf904-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="cf904-127">-Confirm</span></span>
<span data-ttu-id="cf904-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="cf904-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf904-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf904-129">-WhatIf</span></span>
<span data-ttu-id="cf904-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="cf904-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cf904-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cf904-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf904-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf904-132">CommonParameters</span></span>
<span data-ttu-id="cf904-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cf904-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf904-134">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="cf904-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf904-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cf904-135">INPUTS</span></span>

### <span data-ttu-id="cf904-136">Microsoft. Azure. PowerShell. parancsmagok. AppConfiguration. models. IAppConfigurationIdentity</span><span class="sxs-lookup"><span data-stu-id="cf904-136">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity</span></span>

## <span data-ttu-id="cf904-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cf904-137">OUTPUTS</span></span>

### <span data-ttu-id="cf904-138">Microsoft. Azure. PowerShell. parancsmagok. AppConfiguration. modellek. Api20200601. IApiKey</span><span class="sxs-lookup"><span data-stu-id="cf904-138">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IApiKey</span></span>

## <span data-ttu-id="cf904-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cf904-139">NOTES</span></span>

<span data-ttu-id="cf904-140">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="cf904-140">ALIASES</span></span>

<span data-ttu-id="cf904-141">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="cf904-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="cf904-142">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="cf904-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cf904-143">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="cf904-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="cf904-144">INPUTOBJECT <IAppConfigurationIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="cf904-144">INPUTOBJECT <IAppConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="cf904-145">`[ConfigStoreName <String>]`: A konfigurációs tároló neve.</span><span class="sxs-lookup"><span data-stu-id="cf904-145">`[ConfigStoreName <String>]`: The name of the configuration store.</span></span>
  - <span data-ttu-id="cf904-146">`[GroupName <String>]`: A magánjellegű kapcsolat erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="cf904-146">`[GroupName <String>]`: The name of the private link resource group.</span></span>
  - <span data-ttu-id="cf904-147">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="cf904-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="cf904-148">`[PrivateEndpointConnectionName <String>]`: Privát végpont-kapcsolat neve</span><span class="sxs-lookup"><span data-stu-id="cf904-148">`[PrivateEndpointConnectionName <String>]`: Private endpoint connection name</span></span>
  - <span data-ttu-id="cf904-149">`[ResourceGroupName <String>]`: Annak az erőforráscsoport-csoportnak a neve, amelyhez a tároló beállításjegyzéke tartozik.</span><span class="sxs-lookup"><span data-stu-id="cf904-149">`[ResourceGroupName <String>]`: The name of the resource group to which the container registry belongs.</span></span>
  - <span data-ttu-id="cf904-150">`[SubscriptionId <String>]`: A Microsoft Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="cf904-150">`[SubscriptionId <String>]`: The Microsoft Azure subscription ID.</span></span>

## <span data-ttu-id="cf904-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cf904-151">RELATED LINKS</span></span>
