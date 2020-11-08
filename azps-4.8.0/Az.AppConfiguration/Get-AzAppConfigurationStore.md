---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.appconfiguration/get-azappconfigurationstore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Get-AzAppConfigurationStore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Get-AzAppConfigurationStore.md
ms.openlocfilehash: 88847cbb128f5545a235eb2c5c02043231ff1078
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94017985"
---
# <span data-ttu-id="7a5d0-101">Get-AzAppConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="7a5d0-101">Get-AzAppConfigurationStore</span></span>

## <span data-ttu-id="7a5d0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7a5d0-102">SYNOPSIS</span></span>
<span data-ttu-id="7a5d0-103">Beolvashatja vagy listázhatja az App konfigurációs tárolóit.</span><span class="sxs-lookup"><span data-stu-id="7a5d0-103">Get or list app configuration stores.</span></span>

## <span data-ttu-id="7a5d0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7a5d0-104">SYNTAX</span></span>

### <span data-ttu-id="7a5d0-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7a5d0-105">List (Default)</span></span>
```
Get-AzAppConfigurationStore [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="7a5d0-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="7a5d0-106">Get</span></span>
```
Get-AzAppConfigurationStore -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="7a5d0-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="7a5d0-107">GetViaIdentity</span></span>
```
Get-AzAppConfigurationStore -InputObject <IAppConfigurationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="7a5d0-108">Lista1</span><span class="sxs-lookup"><span data-stu-id="7a5d0-108">List1</span></span>
```
Get-AzAppConfigurationStore -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="7a5d0-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="7a5d0-109">DESCRIPTION</span></span>
<span data-ttu-id="7a5d0-110">Beolvashatja vagy listázhatja az App konfigurációs tárolóit.</span><span class="sxs-lookup"><span data-stu-id="7a5d0-110">Get or list app configuration stores.</span></span>

## <span data-ttu-id="7a5d0-111">Példák</span><span class="sxs-lookup"><span data-stu-id="7a5d0-111">EXAMPLES</span></span>

### <span data-ttu-id="7a5d0-112">Példa 1: az App minden konfigurációs áruházának listázása az előfizetés alatt</span><span class="sxs-lookup"><span data-stu-id="7a5d0-112">Example 1: List all app configuration stores under a subscription</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore

Location Name               Type
-------- ----               ----
eastus   appconfig-test01   Microsoft.AppConfiguration/configurationStores
eastus   contoso-app-config Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="7a5d0-113">Ez a parancs felsorolja az összes app-konfigurációs üzletet az előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="7a5d0-113">This command lists all app configuration stores under a subscription.</span></span>

### <span data-ttu-id="7a5d0-114">2. példa: az App minden konfigurációs tárolójának listázása egy erőforráscsoport alatt</span><span class="sxs-lookup"><span data-stu-id="7a5d0-114">Example 2: List all app configuration stores under a resource group</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test

Location Name             Type
-------- ----             ----
eastus   appconfig-test01 Microsoft.AppConfiguration/configurationStores
eastus   appconfig-test02 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="7a5d0-115">Ez a parancs felsorolja az összes app-konfigurációs üzletet egy erőforráscsoport alatt.</span><span class="sxs-lookup"><span data-stu-id="7a5d0-115">This command lists all app configuration stores under a resource group.</span></span>

### <span data-ttu-id="7a5d0-116">3. példa: alkalmazás konfigurációs tárolójának beszerzése név alapján</span><span class="sxs-lookup"><span data-stu-id="7a5d0-116">Example 3: Get an app configuration store by name</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test -Name appconfig-test01

Location Name             Type
-------- ----             ----
eastus   appconfig-test01 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="7a5d0-117">Ez a parancs név szerint kapja meg az App Configuration Store áruházát.</span><span class="sxs-lookup"><span data-stu-id="7a5d0-117">This command gets an app configuration store by name.</span></span>

### <span data-ttu-id="7a5d0-118">Példa 4: alkalmazás-konfigurációs tároló beszerzése csővezetéken</span><span class="sxs-lookup"><span data-stu-id="7a5d0-118">Example 4: Get an app configuration store by pipeline</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test -Name appconfig-test01 | Get-AzAppConfigurationStore

Location Name             Type
-------- ----             ----
eastus   appconfig-test01 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="7a5d0-119">Ez a parancs csővezetéken keresztüli alkalmazás-konfiguráció áruházba kerül.</span><span class="sxs-lookup"><span data-stu-id="7a5d0-119">This command gets an app configuration store by pipeline.</span></span>

## <span data-ttu-id="7a5d0-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7a5d0-120">PARAMETERS</span></span>

### <span data-ttu-id="7a5d0-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a5d0-121">-DefaultProfile</span></span>
<span data-ttu-id="7a5d0-122">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7a5d0-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a5d0-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7a5d0-123">-InputObject</span></span>
<span data-ttu-id="7a5d0-124">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="7a5d0-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7a5d0-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7a5d0-125">-Name</span></span>
<span data-ttu-id="7a5d0-126">A konfigurációs tároló neve.</span><span class="sxs-lookup"><span data-stu-id="7a5d0-126">The name of the configuration store.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a5d0-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a5d0-127">-ResourceGroupName</span></span>
<span data-ttu-id="7a5d0-128">Annak az erőforráscsoportnek a neve, amelyhez a tároló beállításjegyzéke tartozik.</span><span class="sxs-lookup"><span data-stu-id="7a5d0-128">The name of the resource group to which the container registry belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a5d0-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7a5d0-129">-SubscriptionId</span></span>
<span data-ttu-id="7a5d0-130">A Microsoft Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="7a5d0-130">The Microsoft Azure subscription ID.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a5d0-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a5d0-131">CommonParameters</span></span>
<span data-ttu-id="7a5d0-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7a5d0-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a5d0-133">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="7a5d0-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a5d0-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7a5d0-134">INPUTS</span></span>

### <span data-ttu-id="7a5d0-135">Microsoft. Azure. PowerShell. parancsmagok. AppConfiguration. models. IAppConfigurationIdentity</span><span class="sxs-lookup"><span data-stu-id="7a5d0-135">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity</span></span>

## <span data-ttu-id="7a5d0-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7a5d0-136">OUTPUTS</span></span>

### <span data-ttu-id="7a5d0-137">Microsoft. Azure. PowerShell. parancsmagok. AppConfiguration. modellek. Api20200601. IConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="7a5d0-137">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IConfigurationStore</span></span>

## <span data-ttu-id="7a5d0-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7a5d0-138">NOTES</span></span>

<span data-ttu-id="7a5d0-139">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="7a5d0-139">ALIASES</span></span>

<span data-ttu-id="7a5d0-140">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="7a5d0-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7a5d0-141">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="7a5d0-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7a5d0-142">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="7a5d0-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7a5d0-143">INPUTOBJECT <IAppConfigurationIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="7a5d0-143">INPUTOBJECT <IAppConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7a5d0-144">`[ConfigStoreName <String>]`: A konfigurációs tároló neve.</span><span class="sxs-lookup"><span data-stu-id="7a5d0-144">`[ConfigStoreName <String>]`: The name of the configuration store.</span></span>
  - <span data-ttu-id="7a5d0-145">`[GroupName <String>]`: A magánjellegű kapcsolat erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="7a5d0-145">`[GroupName <String>]`: The name of the private link resource group.</span></span>
  - <span data-ttu-id="7a5d0-146">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="7a5d0-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7a5d0-147">`[PrivateEndpointConnectionName <String>]`: Privát végpont-kapcsolat neve</span><span class="sxs-lookup"><span data-stu-id="7a5d0-147">`[PrivateEndpointConnectionName <String>]`: Private endpoint connection name</span></span>
  - <span data-ttu-id="7a5d0-148">`[ResourceGroupName <String>]`: Annak az erőforráscsoport-csoportnak a neve, amelyhez a tároló beállításjegyzéke tartozik.</span><span class="sxs-lookup"><span data-stu-id="7a5d0-148">`[ResourceGroupName <String>]`: The name of the resource group to which the container registry belongs.</span></span>
  - <span data-ttu-id="7a5d0-149">`[SubscriptionId <String>]`: A Microsoft Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="7a5d0-149">`[SubscriptionId <String>]`: The Microsoft Azure subscription ID.</span></span>

## <span data-ttu-id="7a5d0-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7a5d0-150">RELATED LINKS</span></span>

