---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/remove-azconnectedmachine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Remove-AzConnectedMachine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Remove-AzConnectedMachine.md
ms.openlocfilehash: e8988f5dd6e2e37cc98c31ceab244693eae1941e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194448"
---
# <span data-ttu-id="ebea0-101">Remove-AzConnectedMachine</span><span class="sxs-lookup"><span data-stu-id="ebea0-101">Remove-AzConnectedMachine</span></span>

## <span data-ttu-id="ebea0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ebea0-102">SYNOPSIS</span></span>
<span data-ttu-id="ebea0-103">A hibrid gép identitásának eltávolítására szolgáló művelet az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="ebea0-103">The operation to remove a hybrid machine identity in Azure.</span></span>

## <span data-ttu-id="ebea0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ebea0-104">SYNTAX</span></span>

### <span data-ttu-id="ebea0-105">Delete (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ebea0-105">Delete (Default)</span></span>
```
Remove-AzConnectedMachine -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ebea0-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="ebea0-106">DeleteViaIdentity</span></span>
```
Remove-AzConnectedMachine -InputObject <IConnectedMachineIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ebea0-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="ebea0-107">DESCRIPTION</span></span>
<span data-ttu-id="ebea0-108">A hibrid gép identitásának eltávolítására szolgáló művelet az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="ebea0-108">The operation to remove a hybrid machine identity in Azure.</span></span>

## <span data-ttu-id="ebea0-109">Példák</span><span class="sxs-lookup"><span data-stu-id="ebea0-109">EXAMPLES</span></span>

### <span data-ttu-id="ebea0-110">1. példa: csatlakoztatott gép eltávolítása</span><span class="sxs-lookup"><span data-stu-id="ebea0-110">Example 1: Remove a connected machine</span></span>
```powershell
PS C:\> Remove-AzConnectedMachine -Name myMachine -ResourceGroupName myRG

```

<span data-ttu-id="ebea0-111">A csatlakoztatott gép törlése</span><span class="sxs-lookup"><span data-stu-id="ebea0-111">Deletes the connected machine.</span></span>

### <span data-ttu-id="ebea0-112">2. példa: a csatlakoztatott gépek eltávolítása a csővezetéken keresztül</span><span class="sxs-lookup"><span data-stu-id="ebea0-112">Example 2: Remove connected machines via the pipeline</span></span>
```powershell
PS C:\> Get-AzConnectedMachine -ResourceGroupName contoso-connected-machines | Remove-AzConnectedMachine

```

<span data-ttu-id="ebea0-113">Eltávolítja az erőforrás csoport összes számítógépét `contoso-connected-machines` .</span><span class="sxs-lookup"><span data-stu-id="ebea0-113">Removes all machines in the `contoso-connected-machines` resource group.</span></span>

## <span data-ttu-id="ebea0-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ebea0-114">PARAMETERS</span></span>

### <span data-ttu-id="ebea0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebea0-115">-DefaultProfile</span></span>
<span data-ttu-id="ebea0-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ebea0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ebea0-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ebea0-117">-InputObject</span></span>
<span data-ttu-id="ebea0-118">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ebea0-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ebea0-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ebea0-119">-Name</span></span>
<span data-ttu-id="ebea0-120">A hibrid gép neve.</span><span class="sxs-lookup"><span data-stu-id="ebea0-120">The name of the hybrid machine.</span></span>

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

### <span data-ttu-id="ebea0-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ebea0-121">-PassThru</span></span>
<span data-ttu-id="ebea0-122">Igaz érték visszaadása a parancs sikeressége után</span><span class="sxs-lookup"><span data-stu-id="ebea0-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="ebea0-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ebea0-123">-ResourceGroupName</span></span>
<span data-ttu-id="ebea0-124">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="ebea0-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="ebea0-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ebea0-125">-SubscriptionId</span></span>
<span data-ttu-id="ebea0-126">Az előfizetési hitelesítő adatok, amelyek egyedileg azonosíthatják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="ebea0-126">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="ebea0-127">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="ebea0-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="ebea0-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ebea0-128">-Confirm</span></span>
<span data-ttu-id="ebea0-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ebea0-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ebea0-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ebea0-130">-WhatIf</span></span>
<span data-ttu-id="ebea0-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ebea0-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ebea0-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ebea0-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ebea0-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebea0-133">CommonParameters</span></span>
<span data-ttu-id="ebea0-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ebea0-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebea0-135">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ebea0-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebea0-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ebea0-136">INPUTS</span></span>

### <span data-ttu-id="ebea0-137">Microsoft. Azure. PowerShell. parancsmagok. ConnectedMachine. models. IConnectedMachineIdentity</span><span class="sxs-lookup"><span data-stu-id="ebea0-137">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity</span></span>

## <span data-ttu-id="ebea0-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ebea0-138">OUTPUTS</span></span>

### <span data-ttu-id="ebea0-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ebea0-139">System.Boolean</span></span>

## <span data-ttu-id="ebea0-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ebea0-140">NOTES</span></span>

<span data-ttu-id="ebea0-141">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="ebea0-141">ALIASES</span></span>

<span data-ttu-id="ebea0-142">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="ebea0-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ebea0-143">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="ebea0-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ebea0-144">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="ebea0-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ebea0-145">INPUTOBJECT <IConnectedMachineIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="ebea0-145">INPUTOBJECT <IConnectedMachineIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ebea0-146">`[ExtensionName <String>]`: A gép mellékének neve.</span><span class="sxs-lookup"><span data-stu-id="ebea0-146">`[ExtensionName <String>]`: The name of the machine extension.</span></span>
  - <span data-ttu-id="ebea0-147">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="ebea0-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ebea0-148">`[Name <String>]`: A hibrid gép neve.</span><span class="sxs-lookup"><span data-stu-id="ebea0-148">`[Name <String>]`: The name of the hybrid machine.</span></span>
  - <span data-ttu-id="ebea0-149">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="ebea0-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="ebea0-150">`[SubscriptionId <String>]`: Az előfizetési hitelesítő adatok, amelyek egyedileg azonosíthatják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="ebea0-150">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="ebea0-151">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="ebea0-151">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="ebea0-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ebea0-152">RELATED LINKS</span></span>

