---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/en-us/powershell/module/az.hanaonazure/remove-azsapmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Remove-AzSapMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Remove-AzSapMonitor.md
ms.openlocfilehash: bcba06d87bce2f9ccc8016afc9f08dff75e29b1c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185341"
---
# <span data-ttu-id="352f0-101">Remove-AzSapMonitor</span><span class="sxs-lookup"><span data-stu-id="352f0-101">Remove-AzSapMonitor</span></span>

## <span data-ttu-id="352f0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="352f0-102">SYNOPSIS</span></span>
<span data-ttu-id="352f0-103">Egy SAP-monitor törlése a megadott előfizetéssel, erőforrás csoporttal és a monitor nevével</span><span class="sxs-lookup"><span data-stu-id="352f0-103">Deletes a SAP monitor with the specified subscription, resource group, and monitor name.</span></span>

## <span data-ttu-id="352f0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="352f0-104">SYNTAX</span></span>

### <span data-ttu-id="352f0-105">Delete (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="352f0-105">Delete (Default)</span></span>
```
Remove-AzSapMonitor -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="352f0-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="352f0-106">DeleteViaIdentity</span></span>
```
Remove-AzSapMonitor -InputObject <IHanaOnAzureIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="352f0-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="352f0-107">DESCRIPTION</span></span>
<span data-ttu-id="352f0-108">Egy SAP-monitor törlése a megadott előfizetéssel, erőforrás csoporttal és a monitor nevével</span><span class="sxs-lookup"><span data-stu-id="352f0-108">Deletes a SAP monitor with the specified subscription, resource group, and monitor name.</span></span>

## <span data-ttu-id="352f0-109">Példák</span><span class="sxs-lookup"><span data-stu-id="352f0-109">EXAMPLES</span></span>

### <span data-ttu-id="352f0-110">Példa 1: SAP-monitor eltávolítása név szerint</span><span class="sxs-lookup"><span data-stu-id="352f0-110">Example 1: Remove a SAP monitor by name</span></span>
```powershell
PS C:\> Remove-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-sapmonitor-t02

```

<span data-ttu-id="352f0-111">Ez a parancs eltávolít egy SAP-monitort név szerint.</span><span class="sxs-lookup"><span data-stu-id="352f0-111">This command removes a SAP monitor by name.</span></span>

### <span data-ttu-id="352f0-112">2. példa: SAP-monitor objektumból való eltávolítása</span><span class="sxs-lookup"><span data-stu-id="352f0-112">Example 2: Remove a SAP monitor by object</span></span>
```powershell
PS C:\> $sap = Get-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-sapmonitor-t01
PS C:\> Remove-AzSapMonitor -InputObject $sap

```

<span data-ttu-id="352f0-113">Ez a parancs eltávolít egy SAP-monitort objektum alapján.</span><span class="sxs-lookup"><span data-stu-id="352f0-113">This command removes a SAP monitor by object.</span></span>

## <span data-ttu-id="352f0-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="352f0-114">PARAMETERS</span></span>

### <span data-ttu-id="352f0-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="352f0-115">-AsJob</span></span>
<span data-ttu-id="352f0-116">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="352f0-116">Run the command as a job</span></span>

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

### <span data-ttu-id="352f0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="352f0-117">-DefaultProfile</span></span>
<span data-ttu-id="352f0-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="352f0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="352f0-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="352f0-119">-InputObject</span></span>
<span data-ttu-id="352f0-120">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="352f0-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="352f0-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="352f0-121">-Name</span></span>
<span data-ttu-id="352f0-122">Az SAP-figyelő erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="352f0-122">Name of the SAP monitor resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: SapMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="352f0-123">-Várva</span><span class="sxs-lookup"><span data-stu-id="352f0-123">-NoWait</span></span>
<span data-ttu-id="352f0-124">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="352f0-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="352f0-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="352f0-125">-PassThru</span></span>
<span data-ttu-id="352f0-126">Igaz érték visszaadása a parancs sikeressége után</span><span class="sxs-lookup"><span data-stu-id="352f0-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="352f0-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="352f0-127">-ResourceGroupName</span></span>
<span data-ttu-id="352f0-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="352f0-128">Name of the resource group.</span></span>

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

### <span data-ttu-id="352f0-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="352f0-129">-SubscriptionId</span></span>
<span data-ttu-id="352f0-130">Előfizetési azonosító, amely egyedileg azonosítja a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="352f0-130">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="352f0-131">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="352f0-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="352f0-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="352f0-132">-Confirm</span></span>
<span data-ttu-id="352f0-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="352f0-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="352f0-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="352f0-134">-WhatIf</span></span>
<span data-ttu-id="352f0-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="352f0-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="352f0-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="352f0-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="352f0-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="352f0-137">CommonParameters</span></span>
<span data-ttu-id="352f0-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="352f0-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="352f0-139">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="352f0-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="352f0-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="352f0-140">INPUTS</span></span>

### <span data-ttu-id="352f0-141">Microsoft. Azure. PowerShell. parancsmagok. HanaOnAzure. models. IHanaOnAzureIdentity</span><span class="sxs-lookup"><span data-stu-id="352f0-141">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span></span>

## <span data-ttu-id="352f0-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="352f0-142">OUTPUTS</span></span>

### <span data-ttu-id="352f0-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="352f0-143">System.Boolean</span></span>

## <span data-ttu-id="352f0-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="352f0-144">NOTES</span></span>

<span data-ttu-id="352f0-145">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="352f0-145">ALIASES</span></span>

<span data-ttu-id="352f0-146">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="352f0-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="352f0-147">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="352f0-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="352f0-148">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="352f0-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="352f0-149">INPUTOBJECT <IHanaOnAzureIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="352f0-149">INPUTOBJECT <IHanaOnAzureIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="352f0-150">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="352f0-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="352f0-151">`[Location <String>]`: A törölt boltozat helye.</span><span class="sxs-lookup"><span data-stu-id="352f0-151">`[Location <String>]`: The location of the deleted vault.</span></span>
  - <span data-ttu-id="352f0-152">`[OperationKind <AccessPolicyUpdateKind?>]`: A művelet neve</span><span class="sxs-lookup"><span data-stu-id="352f0-152">`[OperationKind <AccessPolicyUpdateKind?>]`: Name of the operation</span></span>
  - <span data-ttu-id="352f0-153">`[ProviderInstanceName <String>]`: A szolgáltató példányának neve.</span><span class="sxs-lookup"><span data-stu-id="352f0-153">`[ProviderInstanceName <String>]`: Name of the provider instance.</span></span>
  - <span data-ttu-id="352f0-154">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="352f0-154">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="352f0-155">`[ResourceName <String>]`: Az identitás-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="352f0-155">`[ResourceName <String>]`: The name of the identity resource.</span></span>
  - <span data-ttu-id="352f0-156">`[SapMonitorName <String>]`: Az SAP-figyelő erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="352f0-156">`[SapMonitorName <String>]`: Name of the SAP monitor resource.</span></span>
  - <span data-ttu-id="352f0-157">`[Scope <String>]`: Az erőforrás-szolgáltató hatóköre.</span><span class="sxs-lookup"><span data-stu-id="352f0-157">`[Scope <String>]`: The resource provider scope of the resource.</span></span> <span data-ttu-id="352f0-158">A fölérendelt erőforrás a felügyelt identitások segítségével meghosszabbodik.</span><span class="sxs-lookup"><span data-stu-id="352f0-158">Parent resource being extended by Managed Identities.</span></span>
  - <span data-ttu-id="352f0-159">`[SubscriptionId <String>]`: Az előfizetés azonosítója, amely egyedileg azonosítja a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="352f0-159">`[SubscriptionId <String>]`: Subscription ID which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="352f0-160">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="352f0-160">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="352f0-161">`[VaultName <String>]`: A boltozat neve</span><span class="sxs-lookup"><span data-stu-id="352f0-161">`[VaultName <String>]`: Name of the vault</span></span>

## <span data-ttu-id="352f0-162">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="352f0-162">RELATED LINKS</span></span>

