---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/remove-azconnectedmachineextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Remove-AzConnectedMachineExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Remove-AzConnectedMachineExtension.md
ms.openlocfilehash: ee746fd2f9a35415e4efd3c2f8aaba803d182beb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194445"
---
# <span data-ttu-id="9db86-101">Remove-AzConnectedMachineExtension</span><span class="sxs-lookup"><span data-stu-id="9db86-101">Remove-AzConnectedMachineExtension</span></span>

## <span data-ttu-id="9db86-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9db86-102">SYNOPSIS</span></span>
<span data-ttu-id="9db86-103">A bővítmény törlésére szolgáló művelet.</span><span class="sxs-lookup"><span data-stu-id="9db86-103">The operation to delete the extension.</span></span>

## <span data-ttu-id="9db86-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9db86-104">SYNTAX</span></span>

### <span data-ttu-id="9db86-105">Delete (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9db86-105">Delete (Default)</span></span>
```
Remove-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="9db86-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="9db86-106">DeleteViaIdentity</span></span>
```
Remove-AzConnectedMachineExtension -InputObject <IConnectedMachineIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9db86-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="9db86-107">DESCRIPTION</span></span>
<span data-ttu-id="9db86-108">A bővítmény törlésére szolgáló művelet.</span><span class="sxs-lookup"><span data-stu-id="9db86-108">The operation to delete the extension.</span></span>

## <span data-ttu-id="9db86-109">Példák</span><span class="sxs-lookup"><span data-stu-id="9db86-109">EXAMPLES</span></span>

### <span data-ttu-id="9db86-110">1. példa: számítógép-kiterjesztés eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="9db86-110">Example 1: Remove a machine extension.</span></span>
```powershell
PS C:\> Remove-AzConnectedMachineExtension -MachineName myMachine -ResourceGroupName myRG -Name custom

```

<span data-ttu-id="9db86-111">Törli a számítógépen a bővítményt.</span><span class="sxs-lookup"><span data-stu-id="9db86-111">Deletes the extension on the machine.</span></span>

### <span data-ttu-id="9db86-112">2. példa: a kiterjesztés eltávolítása a csővezetéken keresztül</span><span class="sxs-lookup"><span data-stu-id="9db86-112">Example 2: Remove extension via the pipeline</span></span>
```powershell
PS C:\> Get-AzConnectedMachineExtension -ResourceGroupName contoso-connected-machines -MachineName myMachine | Remove-AzConnectedMachineExtension

```

<span data-ttu-id="9db86-113">Eltávolítja az összes kiterjesztést a megadott gépen.</span><span class="sxs-lookup"><span data-stu-id="9db86-113">Removes all extensions in the specified machine.</span></span>

## <span data-ttu-id="9db86-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9db86-114">PARAMETERS</span></span>

### <span data-ttu-id="9db86-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9db86-115">-AsJob</span></span>
<span data-ttu-id="9db86-116">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="9db86-116">Run the command as a job</span></span>

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

### <span data-ttu-id="9db86-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9db86-117">-DefaultProfile</span></span>
<span data-ttu-id="9db86-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9db86-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9db86-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9db86-119">-InputObject</span></span>
<span data-ttu-id="9db86-120">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="9db86-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="9db86-121">-Számítógépnév</span><span class="sxs-lookup"><span data-stu-id="9db86-121">-MachineName</span></span>
<span data-ttu-id="9db86-122">Annak a gépnek a neve, ahol a kiterjesztést törölni kell.</span><span class="sxs-lookup"><span data-stu-id="9db86-122">The name of the machine where the extension should be deleted.</span></span>

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

### <span data-ttu-id="9db86-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9db86-123">-Name</span></span>
<span data-ttu-id="9db86-124">A gép mellékének neve.</span><span class="sxs-lookup"><span data-stu-id="9db86-124">The name of the machine extension.</span></span>

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

### <span data-ttu-id="9db86-125">-Várva</span><span class="sxs-lookup"><span data-stu-id="9db86-125">-NoWait</span></span>
<span data-ttu-id="9db86-126">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="9db86-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="9db86-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9db86-127">-PassThru</span></span>
<span data-ttu-id="9db86-128">Igaz érték visszaadása a parancs sikeressége után</span><span class="sxs-lookup"><span data-stu-id="9db86-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="9db86-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9db86-129">-ResourceGroupName</span></span>
<span data-ttu-id="9db86-130">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="9db86-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="9db86-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9db86-131">-SubscriptionId</span></span>
<span data-ttu-id="9db86-132">Az előfizetési hitelesítő adatok, amelyek egyedileg azonosíthatják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="9db86-132">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="9db86-133">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="9db86-133">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="9db86-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9db86-134">-Confirm</span></span>
<span data-ttu-id="9db86-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9db86-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9db86-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9db86-136">-WhatIf</span></span>
<span data-ttu-id="9db86-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9db86-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9db86-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9db86-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9db86-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9db86-139">CommonParameters</span></span>
<span data-ttu-id="9db86-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9db86-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9db86-141">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="9db86-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9db86-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9db86-142">INPUTS</span></span>

### <span data-ttu-id="9db86-143">Microsoft. Azure. PowerShell. parancsmagok. ConnectedMachine. models. IConnectedMachineIdentity</span><span class="sxs-lookup"><span data-stu-id="9db86-143">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity</span></span>

## <span data-ttu-id="9db86-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9db86-144">OUTPUTS</span></span>

### <span data-ttu-id="9db86-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9db86-145">System.Boolean</span></span>

## <span data-ttu-id="9db86-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9db86-146">NOTES</span></span>

<span data-ttu-id="9db86-147">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="9db86-147">ALIASES</span></span>

<span data-ttu-id="9db86-148">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="9db86-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9db86-149">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="9db86-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9db86-150">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="9db86-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9db86-151">INPUTOBJECT <IConnectedMachineIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="9db86-151">INPUTOBJECT <IConnectedMachineIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9db86-152">`[ExtensionName <String>]`: A gép mellékének neve.</span><span class="sxs-lookup"><span data-stu-id="9db86-152">`[ExtensionName <String>]`: The name of the machine extension.</span></span>
  - <span data-ttu-id="9db86-153">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="9db86-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9db86-154">`[Name <String>]`: A hibrid gép neve.</span><span class="sxs-lookup"><span data-stu-id="9db86-154">`[Name <String>]`: The name of the hybrid machine.</span></span>
  - <span data-ttu-id="9db86-155">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="9db86-155">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="9db86-156">`[SubscriptionId <String>]`: Az előfizetési hitelesítő adatok, amelyek egyedileg azonosíthatják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="9db86-156">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="9db86-157">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="9db86-157">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="9db86-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9db86-158">RELATED LINKS</span></span>

