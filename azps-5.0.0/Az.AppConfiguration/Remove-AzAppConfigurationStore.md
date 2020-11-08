---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.appconfiguration/remove-azappconfigurationstore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Remove-AzAppConfigurationStore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Remove-AzAppConfigurationStore.md
ms.openlocfilehash: b0939a4baa498532a3b519875183e6d1d12945a7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186445"
---
# <span data-ttu-id="83825-101">Remove-AzAppConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="83825-101">Remove-AzAppConfigurationStore</span></span>

## <span data-ttu-id="83825-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="83825-102">SYNOPSIS</span></span>
<span data-ttu-id="83825-103">Törli a konfigurációs tárolót.</span><span class="sxs-lookup"><span data-stu-id="83825-103">Deletes a configuration store.</span></span>

## <span data-ttu-id="83825-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="83825-104">SYNTAX</span></span>

### <span data-ttu-id="83825-105">Delete (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="83825-105">Delete (Default)</span></span>
```
Remove-AzAppConfigurationStore -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="83825-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="83825-106">DeleteViaIdentity</span></span>
```
Remove-AzAppConfigurationStore -InputObject <IAppConfigurationIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="83825-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="83825-107">DESCRIPTION</span></span>
<span data-ttu-id="83825-108">Törli a konfigurációs tárolót.</span><span class="sxs-lookup"><span data-stu-id="83825-108">Deletes a configuration store.</span></span>

## <span data-ttu-id="83825-109">Példák</span><span class="sxs-lookup"><span data-stu-id="83825-109">EXAMPLES</span></span>

### <span data-ttu-id="83825-110">1. példa: alkalmazás-konfigurációs tároló eltávolítása</span><span class="sxs-lookup"><span data-stu-id="83825-110">Example 1: Remove an app configuration store</span></span>
```powershell
PS C:\> Remove-AzAppConfigurationStore -Name appconfig-test03 -ResourceGroupName lucas-manual-test

```

<span data-ttu-id="83825-111">Ez a parancs eltávolítja az App Configuration Store áruházát.</span><span class="sxs-lookup"><span data-stu-id="83825-111">This command removes an app configuration store.</span></span>

### <span data-ttu-id="83825-112">2. példa: alkalmazás-konfigurációs áruház eltávolítása</span><span class="sxs-lookup"><span data-stu-id="83825-112">Example 2: Remove an app configuration store</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore -Name appconfig-test02 -ResourceGroupName lucas-manual-test | Remove-AzAppConfigurationStore

```

<span data-ttu-id="83825-113">Ez a parancs eltávolítja az App Configuration Store áruházát.</span><span class="sxs-lookup"><span data-stu-id="83825-113">This command removes an app configuration store.</span></span>

## <span data-ttu-id="83825-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="83825-114">PARAMETERS</span></span>

### <span data-ttu-id="83825-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="83825-115">-AsJob</span></span>
<span data-ttu-id="83825-116">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="83825-116">Run the command as a job</span></span>

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

### <span data-ttu-id="83825-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83825-117">-DefaultProfile</span></span>
<span data-ttu-id="83825-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="83825-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="83825-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="83825-119">-InputObject</span></span>
<span data-ttu-id="83825-120">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="83825-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="83825-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="83825-121">-Name</span></span>
<span data-ttu-id="83825-122">A konfigurációs tároló neve.</span><span class="sxs-lookup"><span data-stu-id="83825-122">The name of the configuration store.</span></span>

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

### <span data-ttu-id="83825-123">-Várva</span><span class="sxs-lookup"><span data-stu-id="83825-123">-NoWait</span></span>
<span data-ttu-id="83825-124">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="83825-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="83825-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="83825-125">-PassThru</span></span>
<span data-ttu-id="83825-126">Igaz érték visszaadása a parancs sikeressége után</span><span class="sxs-lookup"><span data-stu-id="83825-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="83825-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83825-127">-ResourceGroupName</span></span>
<span data-ttu-id="83825-128">Annak az erőforráscsoportnek a neve, amelyhez a tároló beállításjegyzéke tartozik.</span><span class="sxs-lookup"><span data-stu-id="83825-128">The name of the resource group to which the container registry belongs.</span></span>

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

### <span data-ttu-id="83825-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="83825-129">-SubscriptionId</span></span>
<span data-ttu-id="83825-130">A Microsoft Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="83825-130">The Microsoft Azure subscription ID.</span></span>

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

### <span data-ttu-id="83825-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="83825-131">-Confirm</span></span>
<span data-ttu-id="83825-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="83825-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83825-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83825-133">-WhatIf</span></span>
<span data-ttu-id="83825-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="83825-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83825-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="83825-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83825-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83825-136">CommonParameters</span></span>
<span data-ttu-id="83825-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="83825-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83825-138">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="83825-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83825-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="83825-139">INPUTS</span></span>

### <span data-ttu-id="83825-140">Microsoft. Azure. PowerShell. parancsmagok. AppConfiguration. models. IAppConfigurationIdentity</span><span class="sxs-lookup"><span data-stu-id="83825-140">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity</span></span>

## <span data-ttu-id="83825-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="83825-141">OUTPUTS</span></span>

### <span data-ttu-id="83825-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="83825-142">System.Boolean</span></span>

## <span data-ttu-id="83825-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="83825-143">NOTES</span></span>

<span data-ttu-id="83825-144">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="83825-144">ALIASES</span></span>

<span data-ttu-id="83825-145">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="83825-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="83825-146">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="83825-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="83825-147">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="83825-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="83825-148">INPUTOBJECT <IAppConfigurationIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="83825-148">INPUTOBJECT <IAppConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="83825-149">`[ConfigStoreName <String>]`: A konfigurációs tároló neve.</span><span class="sxs-lookup"><span data-stu-id="83825-149">`[ConfigStoreName <String>]`: The name of the configuration store.</span></span>
  - <span data-ttu-id="83825-150">`[GroupName <String>]`: A magánjellegű kapcsolat erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="83825-150">`[GroupName <String>]`: The name of the private link resource group.</span></span>
  - <span data-ttu-id="83825-151">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="83825-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="83825-152">`[PrivateEndpointConnectionName <String>]`: Privát végpont-kapcsolat neve</span><span class="sxs-lookup"><span data-stu-id="83825-152">`[PrivateEndpointConnectionName <String>]`: Private endpoint connection name</span></span>
  - <span data-ttu-id="83825-153">`[ResourceGroupName <String>]`: Annak az erőforráscsoport-csoportnak a neve, amelyhez a tároló beállításjegyzéke tartozik.</span><span class="sxs-lookup"><span data-stu-id="83825-153">`[ResourceGroupName <String>]`: The name of the resource group to which the container registry belongs.</span></span>
  - <span data-ttu-id="83825-154">`[SubscriptionId <String>]`: A Microsoft Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="83825-154">`[SubscriptionId <String>]`: The Microsoft Azure subscription ID.</span></span>

## <span data-ttu-id="83825-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="83825-155">RELATED LINKS</span></span>

