---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/powershell/module/az.appconfiguration/get-azappconfigurationstore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Get-AzAppConfigurationStore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Get-AzAppConfigurationStore.md
ms.openlocfilehash: e7f7c1f7493123793a32163b4e8f37bec8706e10
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101942730"
---
# <span data-ttu-id="b529e-101">Get-AzAppConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="b529e-101">Get-AzAppConfigurationStore</span></span>

## <span data-ttu-id="b529e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b529e-102">SYNOPSIS</span></span>
<span data-ttu-id="b529e-103">Alkalmazáskonfigurációs áruházak letöltése vagy listába sorolja.</span><span class="sxs-lookup"><span data-stu-id="b529e-103">Get or list app configuration stores.</span></span>

## <span data-ttu-id="b529e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b529e-104">SYNTAX</span></span>

### <span data-ttu-id="b529e-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b529e-105">List (Default)</span></span>
```
Get-AzAppConfigurationStore [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b529e-106">Bej.le</span><span class="sxs-lookup"><span data-stu-id="b529e-106">Get</span></span>
```
Get-AzAppConfigurationStore -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b529e-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b529e-107">GetViaIdentity</span></span>
```
Get-AzAppConfigurationStore -InputObject <IAppConfigurationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="b529e-108">Lista1</span><span class="sxs-lookup"><span data-stu-id="b529e-108">List1</span></span>
```
Get-AzAppConfigurationStore -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="b529e-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b529e-109">DESCRIPTION</span></span>
<span data-ttu-id="b529e-110">Alkalmazáskonfigurációs áruházak letöltése vagy listába sorolja.</span><span class="sxs-lookup"><span data-stu-id="b529e-110">Get or list app configuration stores.</span></span>

## <span data-ttu-id="b529e-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b529e-111">EXAMPLES</span></span>

### <span data-ttu-id="b529e-112">1. példa: Az összes alkalmazáskonfigurációs áruház felsorolása egy előfizetés alatt</span><span class="sxs-lookup"><span data-stu-id="b529e-112">Example 1: List all app configuration stores under a subscription</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore

Location Name               Type
-------- ----               ----
eastus   appconfig-test01   Microsoft.AppConfiguration/configurationStores
eastus   contoso-app-config Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="b529e-113">Ez a parancs felsorolja az előfizetés alatt található összes alkalmazáskonfigurációs tárolót.</span><span class="sxs-lookup"><span data-stu-id="b529e-113">This command lists all app configuration stores under a subscription.</span></span>

### <span data-ttu-id="b529e-114">2. példa: Egy erőforráscsoport összes alkalmazáskonfigurációs tárolójának felsorolása</span><span class="sxs-lookup"><span data-stu-id="b529e-114">Example 2: List all app configuration stores under a resource group</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test

Location Name             Type
-------- ----             ----
eastus   appconfig-test01 Microsoft.AppConfiguration/configurationStores
eastus   appconfig-test02 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="b529e-115">Ez a parancs felsorolja az erőforráscsoport összes alkalmazáskonfigurációs tárolóját.</span><span class="sxs-lookup"><span data-stu-id="b529e-115">This command lists all app configuration stores under a resource group.</span></span>

### <span data-ttu-id="b529e-116">3. példa: Alkalmazáskonfigurációs áruház letöltése név szerint</span><span class="sxs-lookup"><span data-stu-id="b529e-116">Example 3: Get an app configuration store by name</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test -Name appconfig-test01

Location Name             Type
-------- ----             ----
eastus   appconfig-test01 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="b529e-117">Ez a parancs név szerint kap egy alkalmazáskonfigurációs tárolót.</span><span class="sxs-lookup"><span data-stu-id="b529e-117">This command gets an app configuration store by name.</span></span>

### <span data-ttu-id="b529e-118">4. példa: Alkalmazáskonfigurációs áruház lekérte folyamat szerint</span><span class="sxs-lookup"><span data-stu-id="b529e-118">Example 4: Get an app configuration store by pipeline</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test -Name appconfig-test01 | Get-AzAppConfigurationStore

Location Name             Type
-------- ----             ----
eastus   appconfig-test01 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="b529e-119">Ez a parancs egy alkalmazáskonfigurációs tárolót kap folyamat szerint.</span><span class="sxs-lookup"><span data-stu-id="b529e-119">This command gets an app configuration store by pipeline.</span></span>

## <span data-ttu-id="b529e-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b529e-120">PARAMETERS</span></span>

### <span data-ttu-id="b529e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b529e-121">-DefaultProfile</span></span>
<span data-ttu-id="b529e-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b529e-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b529e-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b529e-123">-InputObject</span></span>
<span data-ttu-id="b529e-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="b529e-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b529e-125">-Name</span><span class="sxs-lookup"><span data-stu-id="b529e-125">-Name</span></span>
<span data-ttu-id="b529e-126">A konfigurációs tároló neve.</span><span class="sxs-lookup"><span data-stu-id="b529e-126">The name of the configuration store.</span></span>

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

### <span data-ttu-id="b529e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b529e-127">-ResourceGroupName</span></span>
<span data-ttu-id="b529e-128">Annak az erőforráscsoportnak a neve, amelyhez a tároló beállításjegyzék tartozik.</span><span class="sxs-lookup"><span data-stu-id="b529e-128">The name of the resource group to which the container registry belongs.</span></span>

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

### <span data-ttu-id="b529e-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b529e-129">-SubscriptionId</span></span>
<span data-ttu-id="b529e-130">A Microsoft Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="b529e-130">The Microsoft Azure subscription ID.</span></span>

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

### <span data-ttu-id="b529e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b529e-131">CommonParameters</span></span>
<span data-ttu-id="b529e-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b529e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b529e-133">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b529e-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b529e-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b529e-134">INPUTS</span></span>

### <span data-ttu-id="b529e-135">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity</span><span class="sxs-lookup"><span data-stu-id="b529e-135">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity</span></span>

## <span data-ttu-id="b529e-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b529e-136">OUTPUTS</span></span>

### <span data-ttu-id="b529e-137">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="b529e-137">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IConfigurationStore</span></span>

## <span data-ttu-id="b529e-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b529e-138">NOTES</span></span>

<span data-ttu-id="b529e-139">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="b529e-139">ALIASES</span></span>

<span data-ttu-id="b529e-140">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="b529e-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b529e-141">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="b529e-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b529e-142">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b529e-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b529e-143">INPUTOBJECT: <IAppConfigurationIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="b529e-143">INPUTOBJECT <IAppConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b529e-144">`[ConfigStoreName <String>]`: A konfigurációs tároló neve.</span><span class="sxs-lookup"><span data-stu-id="b529e-144">`[ConfigStoreName <String>]`: The name of the configuration store.</span></span>
  - <span data-ttu-id="b529e-145">`[GroupName <String>]`: A privát csatolású erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="b529e-145">`[GroupName <String>]`: The name of the private link resource group.</span></span>
  - <span data-ttu-id="b529e-146">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="b529e-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b529e-147">`[PrivateEndpointConnectionName <String>]`: Private endpoint connection name</span><span class="sxs-lookup"><span data-stu-id="b529e-147">`[PrivateEndpointConnectionName <String>]`: Private endpoint connection name</span></span>
  - <span data-ttu-id="b529e-148">`[ResourceGroupName <String>]`: Annak az erőforráscsoportnak a neve, amelyhez a tároló beállításjegyzék tartozik.</span><span class="sxs-lookup"><span data-stu-id="b529e-148">`[ResourceGroupName <String>]`: The name of the resource group to which the container registry belongs.</span></span>
  - <span data-ttu-id="b529e-149">`[SubscriptionId <String>]`: A Microsoft Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="b529e-149">`[SubscriptionId <String>]`: The Microsoft Azure subscription ID.</span></span>

## <span data-ttu-id="b529e-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b529e-150">RELATED LINKS</span></span>

