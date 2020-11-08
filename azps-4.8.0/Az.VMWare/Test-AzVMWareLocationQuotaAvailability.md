---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/test-azvmwarelocationquotaavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Test-AzVMWareLocationQuotaAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Test-AzVMWareLocationQuotaAvailability.md
ms.openlocfilehash: 9cb677ff172c986f18c7c11c00e0f8d7e0bbf5bf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182458"
---
# <span data-ttu-id="6ce5a-101">Test-AzVMWareLocationQuotaAvailability</span><span class="sxs-lookup"><span data-stu-id="6ce5a-101">Test-AzVMWareLocationQuotaAvailability</span></span>

## <span data-ttu-id="6ce5a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6ce5a-102">SYNOPSIS</span></span>
<span data-ttu-id="6ce5a-103">Visszaadott kvóta az előfizetéshez régiónként</span><span class="sxs-lookup"><span data-stu-id="6ce5a-103">Return quota for subscription by region</span></span>

## <span data-ttu-id="6ce5a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6ce5a-104">SYNTAX</span></span>

### <span data-ttu-id="6ce5a-105">Ellenőrzés (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6ce5a-105">Check (Default)</span></span>
```
Test-AzVMWareLocationQuotaAvailability -Location <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6ce5a-106">CheckViaIdentity</span><span class="sxs-lookup"><span data-stu-id="6ce5a-106">CheckViaIdentity</span></span>
```
Test-AzVMWareLocationQuotaAvailability -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6ce5a-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="6ce5a-107">DESCRIPTION</span></span>
<span data-ttu-id="6ce5a-108">Visszaadott kvóta az előfizetéshez régiónként</span><span class="sxs-lookup"><span data-stu-id="6ce5a-108">Return quota for subscription by region</span></span>

## <span data-ttu-id="6ce5a-109">Példák</span><span class="sxs-lookup"><span data-stu-id="6ce5a-109">EXAMPLES</span></span>

### <span data-ttu-id="6ce5a-110">Példa 1: a kvóta elérhetőségének ellenőrzése</span><span class="sxs-lookup"><span data-stu-id="6ce5a-110">Example 1: Check quota availability</span></span>
```powershell
PS C:\> Test-AzVMWareLocationQuotaAvailability -Location eastus

Enabled
-------
Disabled
```

<span data-ttu-id="6ce5a-111">A kvóta elérhetőségének ellenőrzése</span><span class="sxs-lookup"><span data-stu-id="6ce5a-111">Check quota availability</span></span>

## <span data-ttu-id="6ce5a-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6ce5a-112">PARAMETERS</span></span>

### <span data-ttu-id="6ce5a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ce5a-113">-DefaultProfile</span></span>
<span data-ttu-id="6ce5a-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6ce5a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ce5a-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6ce5a-115">-InputObject</span></span>
<span data-ttu-id="6ce5a-116">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="6ce5a-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity
Parameter Sets: CheckViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6ce5a-117">-Hely</span><span class="sxs-lookup"><span data-stu-id="6ce5a-117">-Location</span></span>
<span data-ttu-id="6ce5a-118">Azure Region (Azure)</span><span class="sxs-lookup"><span data-stu-id="6ce5a-118">Azure region</span></span>

```yaml
Type: System.String
Parameter Sets: Check
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ce5a-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6ce5a-119">-SubscriptionId</span></span>
<span data-ttu-id="6ce5a-120">A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="6ce5a-120">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Check
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ce5a-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6ce5a-121">-Confirm</span></span>
<span data-ttu-id="6ce5a-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6ce5a-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ce5a-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ce5a-123">-WhatIf</span></span>
<span data-ttu-id="6ce5a-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6ce5a-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ce5a-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6ce5a-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ce5a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ce5a-126">CommonParameters</span></span>
<span data-ttu-id="6ce5a-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6ce5a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ce5a-128">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="6ce5a-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ce5a-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6ce5a-129">INPUTS</span></span>

### <span data-ttu-id="6ce5a-130">Microsoft. Azure. PowerShell. parancsmagok. VMWare. models. IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="6ce5a-130">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="6ce5a-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6ce5a-131">OUTPUTS</span></span>

### <span data-ttu-id="6ce5a-132">Microsoft. Azure. PowerShell. parancsmagok. VMWare. models. Api20200320. IQuota</span><span class="sxs-lookup"><span data-stu-id="6ce5a-132">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IQuota</span></span>

## <span data-ttu-id="6ce5a-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6ce5a-133">NOTES</span></span>

<span data-ttu-id="6ce5a-134">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="6ce5a-134">ALIASES</span></span>

<span data-ttu-id="6ce5a-135">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="6ce5a-135">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6ce5a-136">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="6ce5a-136">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6ce5a-137">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="6ce5a-137">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6ce5a-138">INPUTOBJECT <IVMWareIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="6ce5a-138">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6ce5a-139">`[AuthorizationName <String>]`: A ExpressRoute-áramkör engedélyezésének neve a privát felhőben</span><span class="sxs-lookup"><span data-stu-id="6ce5a-139">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="6ce5a-140">`[ClusterName <String>]`: A fürt neve a privát felhőben</span><span class="sxs-lookup"><span data-stu-id="6ce5a-140">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="6ce5a-141">`[HcxEnterpriseSiteName <String>]`: A HCX Enterprise webhely neve a privát felhőben</span><span class="sxs-lookup"><span data-stu-id="6ce5a-141">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="6ce5a-142">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="6ce5a-142">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6ce5a-143">`[Location <String>]`: Azure region</span><span class="sxs-lookup"><span data-stu-id="6ce5a-143">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="6ce5a-144">`[PrivateCloudName <String>]`: A privát felhő neve</span><span class="sxs-lookup"><span data-stu-id="6ce5a-144">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="6ce5a-145">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="6ce5a-145">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="6ce5a-146">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="6ce5a-146">The name is case insensitive.</span></span>
  - <span data-ttu-id="6ce5a-147">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="6ce5a-147">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="6ce5a-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6ce5a-148">RELATED LINKS</span></span>

