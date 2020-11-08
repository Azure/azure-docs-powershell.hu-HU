---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratediscoveredserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateDiscoveredServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateDiscoveredServer.md
ms.openlocfilehash: 367d22f4cea200b59b63e3ddb39c1eaad749fc43
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195785"
---
# <span data-ttu-id="bc644-101">Get-AzMigrateDiscoveredServer</span><span class="sxs-lookup"><span data-stu-id="bc644-101">Get-AzMigrateDiscoveredServer</span></span>

## <span data-ttu-id="bc644-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bc644-102">SYNOPSIS</span></span>
<span data-ttu-id="bc644-103">Az összes felfedezett kiszolgáló beolvasása egy áttelepítési projektben.</span><span class="sxs-lookup"><span data-stu-id="bc644-103">Get All discovered servers in a migrate project.</span></span>

## <span data-ttu-id="bc644-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bc644-104">SYNTAX</span></span>

### <span data-ttu-id="bc644-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="bc644-105">List (Default)</span></span>
```
Get-AzMigrateDiscoveredServer -ProjectName <String> -ResourceGroupName <String> [-DisplayName <String>]
 [-SubscriptionId <String[]>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="bc644-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="bc644-106">Get</span></span>
```
Get-AzMigrateDiscoveredServer -Name <String> -ProjectName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="bc644-107">GetInSite</span><span class="sxs-lookup"><span data-stu-id="bc644-107">GetInSite</span></span>
```
Get-AzMigrateDiscoveredServer -ApplianceName <String> -Name <String> -ProjectName <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="bc644-108">ListInSite</span><span class="sxs-lookup"><span data-stu-id="bc644-108">ListInSite</span></span>
```
Get-AzMigrateDiscoveredServer -ApplianceName <String> -ProjectName <String> -ResourceGroupName <String>
 [-DisplayName <String>] [-SubscriptionId <String[]>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="bc644-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="bc644-109">DESCRIPTION</span></span>
<span data-ttu-id="bc644-110">Azure-áttelepítés beszerzése: a kiszolgáló parancsmagot beolvassa az összes kiszolgálót egy áttelepítési projektben.</span><span class="sxs-lookup"><span data-stu-id="bc644-110">Get Azure migrate server commandlet fetches all servers in a migrate project.</span></span>

## <span data-ttu-id="bc644-111">Példák</span><span class="sxs-lookup"><span data-stu-id="bc644-111">EXAMPLES</span></span>

### <span data-ttu-id="bc644-112">Példa 1: lista</span><span class="sxs-lookup"><span data-stu-id="bc644-112">Example 1: List</span></span>
```powershell
PS C:\> Get-AzMigrateDiscoveredServer -SubscriptionId xxx-xxx-xxx -ResourceGroupName julytest -ProjectName julytest

Name                                                                                                      Typeo…
----                                                                                                      ----o…
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029e62c-31d2-a6c3-5316-aa39f47c49fc Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029c180-1359-5e3c-3f56-05632aa4a37f Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029d80d-d014-72f3-8d05-d43ee49a023d Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029bd24-6d40-88dc-4f29-329596f9a50b Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_50292d97-2025-bfdf-1f07-86afa50d144f Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_50293685-fb73-0a89-204f-f79cb1f0061e Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029c9aa-3c8c-aba8-834e-1058bc457e5b Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029dabc-cc94-780f-76fd-e39acb0e9dce Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_50299579-fc18-4152-ade2-c4a57946f72b Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029cc18-efdc-7315-3b09-9d12a0f337e2 Microsoft.OffAzure/VMwareSites/machines

```

<span data-ttu-id="bc644-113">Az áttelepítési projekt összes kiszolgálójának beolvasása</span><span class="sxs-lookup"><span data-stu-id="bc644-113">Get All servers in a migrate project.</span></span>

### <span data-ttu-id="bc644-114">2. példa: Get</span><span class="sxs-lookup"><span data-stu-id="bc644-114">Example 2: Get</span></span>
```powershell
PS C:\> Get-AzMigrateDiscoveredServer -Name idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029e62c-31d2-a6c3-5316-aa39f47c49fc -SubscriptionId xxx-xxx-xxx -ResourceGroupName julytest -ProjectName julytest

Name                                                                                                      Typeo…
----                                                                                                      ----o…
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029e62c-31d2-a6c3-5316-aa39f47c49fc Microsoft.OffAzure/VMwareSites/machines

```

<span data-ttu-id="bc644-115">Kiszolgáló beszerzése egy áttelepítési projektben név szerint.</span><span class="sxs-lookup"><span data-stu-id="bc644-115">Get a server in a migrate project by name.</span></span>
<span data-ttu-id="bc644-116">A név a kiszolgáló egyedi Paramenter.</span><span class="sxs-lookup"><span data-stu-id="bc644-116">Name is a unique paramenter for a server.</span></span>

### <span data-ttu-id="bc644-117">3 Példa: lista egy készüléken</span><span class="sxs-lookup"><span data-stu-id="bc644-117">Example 3: List in an appliance</span></span>
```powershell
PS C:\> Get-AzMigrateDiscoveredServer  -ApplianceName BBVMwareAVS -SubscriptionId xxx-xxx-xxx -ResourceGroupName julytest -ProjectName julytest

Name                                                                                                      Typeo…
----                                                                                                      ----o…
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029e62c-31d2-a6c3-5316-aa39f47c49fc Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029c180-1359-5e3c-3f56-05632aa4a37f Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029d80d-d014-72f3-8d05-d43ee49a023d Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029bd24-6d40-88dc-4f29-329596f9a50b Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_50292d97-2025-bfdf-1f07-86afa50d144f Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_50293685-fb73-0a89-204f-f79cb1f0061e Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029c9aa-3c8c-aba8-834e-1058bc457e5b Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029dabc-cc94-780f-76fd-e39acb0e9dce Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_50299579-fc18-4152-ade2-c4a57946f72b Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029cc18-efdc-7315-3b09-9d12a0f337e2 Microsoft.OffAzure/VMwareSites/machines

```

<span data-ttu-id="bc644-118">A projektben lévő készülékek összes kiszolgálójának listázása.</span><span class="sxs-lookup"><span data-stu-id="bc644-118">List all servers for an appliance in a project.</span></span>

### <span data-ttu-id="bc644-119">4 példa: beolvasás egy készüléken</span><span class="sxs-lookup"><span data-stu-id="bc644-119">Example 4: Get in an appliance</span></span>
```powershell
PS C:\> Get-AzMigrateDiscoveredServer -Name idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029e62c-31d2-a6c3-5316-aa39f47c49fc -ApplianceName BBVMwareAVS -SubscriptionId xxx-xxx-xxx -ResourceGroupName julytest -ProjectName julytest

Name                                                                                                      Typeo…
----                                                                                                      ----o…
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029e62c-31d2-a6c3-5316-aa39f47c49fc Microsoft.OffAzure/VMwareSites/machines

```

<span data-ttu-id="bc644-120">Szerezzen be egy kiszolgálót a készülékhez a projektben.</span><span class="sxs-lookup"><span data-stu-id="bc644-120">Get a server for an appliance in a project.</span></span>
<span data-ttu-id="bc644-121">A név a kiszolgáló egyedi Paramenter.</span><span class="sxs-lookup"><span data-stu-id="bc644-121">Name is a unique paramenter for a server.</span></span>

### <span data-ttu-id="bc644-122">Példa 5: lista és szűrés megjelenítendő névvel</span><span class="sxs-lookup"><span data-stu-id="bc644-122">Example 5: List and filter by display name</span></span>
```powershell
PS C:\> Get-AzMigrateDiscoveredServer  -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -ProjectName BugBashAVSVMware -DisplayName Contoso | Format-Table DisplayName,Name,Type

DisplayName                   Name                                                                                  Type
-----------                   ----                                                                                  ----
Contoso-ConfigurationServer   10-150-8-52-b090bef3-b733-5e34-bc8f-eb6f2701432a_50098b08-5701-4c58-f6ad-1daf127a8ed9 Microsoft.OffAzure/VMwareSites/machines
Contoso-FrontTier1            10-150-8-52-b090bef3-b733-5e34-bc8f-eb6f2701432a_5009c31a-241a-8213-5627-4ea4af00df93 Microsoft.OffAzure/VMwareSites/machines
Contoso-MiddleTier1           10-150-8-52-b090bef3-b733-5e34-bc8f-eb6f2701432a_50097bb8-f32c-39d6-f475-5aaa6194f016 Microsoft.OffAzure/VMwareSites/machines
ContosoAppSrv2                10-150-8-52-b090bef3-b733-5e34-bc8f-eb6f2701432a_5009b455-1721-fa03-7ceb-8177cd2c5de6 Microsoft.OffAzure/VMwareSites/machines
ContosoCSASR                  10-150-8-52-b090bef3-b733-5e34-bc8f-eb6f2701432a_50096b80-7061-672c-8db0-07ee41212869 Microsoft.OffAzure/VMwareSites/machines
ContosoVMwareMigration2       10-150-8-52-b090bef3-b733-5e34-bc8f-eb6f2701432a_50099d31-71d5-2bd1-fada-8c4eba2f279a Microsoft.OffAzure/VMwareSites/machines
ContosoAppSrv1                10-150-8-52-b090bef3-b733-5e34-bc8f-eb6f2701432a_50097d3f-c1f6-9217-825c-936db54043df Microsoft.OffAzure/VMwareSites/machines

```

<span data-ttu-id="bc644-123">A kiszolgálók egy áttelepítési projektben és a megjelenítendő névvel rendelkező válaszok szűrése</span><span class="sxs-lookup"><span data-stu-id="bc644-123">List servers in a migrate project and filter responses with display name.</span></span>

### <span data-ttu-id="bc644-124">Példa 6: lista egy készüléken, és szűrés megjelenített névvel</span><span class="sxs-lookup"><span data-stu-id="bc644-124">Example 6: List in an appliance and filter by display name</span></span>
```powershell
PS C:\> PS /src/Migrate [Az.Migrate]> Get-AzMigrateDiscoveredServer  -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -ProjectName BugBashAVSVMware -ApplianceName BBVMwareAVS -DisplayName Contoso | Format-Table DisplayName,Name,Type

DisplayName                   Name                                                                                  Type
-----------                   ----                                                                                  ----
Contoso-ConfigurationServer   10-150-8-52-b090bef3-b733-5e34-bc8f-eb6f2701432a_50098b08-5701-4c58-f6ad-1daf127a8ed9 Microsoft.OffAzure/VMwareSites/machines
Contoso-FrontTier1            10-150-8-52-b090bef3-b733-5e34-bc8f-eb6f2701432a_5009c31a-241a-8213-5627-4ea4af00df93 Microsoft.OffAzure/VMwareSites/machines
Contoso-MiddleTier1           10-150-8-52-b090bef3-b733-5e34-bc8f-eb6f2701432a_50097bb8-f32c-39d6-f475-5aaa6194f016 Microsoft.OffAzure/VMwareSites/machines
ContosoAppSrv2                10-150-8-52-b090bef3-b733-5e34-bc8f-eb6f2701432a_5009b455-1721-fa03-7ceb-8177cd2c5de6 Microsoft.OffAzure/VMwareSites/machines
ContosoCSASR                  10-150-8-52-b090bef3-b733-5e34-bc8f-eb6f2701432a_50096b80-7061-672c-8db0-07ee41212869 Microsoft.OffAzure/VMwareSites/machines
ContosoVMwareMigration2       10-150-8-52-b090bef3-b733-5e34-bc8f-eb6f2701432a_50099d31-71d5-2bd1-fada-8c4eba2f279a Microsoft.OffAzure/VMwareSites/machines
ContosoAppSrv1                10-150-8-52-b090bef3-b733-5e34-bc8f-eb6f2701432a_50097d3f-c1f6-9217-825c-936db54043df Microsoft.OffAzure/VMwareSites/machines
Contoso-DataTier3             10-150-8-52-b090bef3-b733-5e34-bc8f-eb6f2701432a_500986e5-7720-471e-11d7-d4e8ae9edc45 Microsoft.OffAzure/VMwareSites/machines
```

<span data-ttu-id="bc644-125">Az áttelepítési projektben a készülékek listáját, valamint a megjelenítendő névvel rendelkező válaszokat szűrheti.</span><span class="sxs-lookup"><span data-stu-id="bc644-125">List servers for an appliance in a migrate project and filter responses with display name.</span></span>

## <span data-ttu-id="bc644-126">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bc644-126">PARAMETERS</span></span>

### <span data-ttu-id="bc644-127">-ApplianceName</span><span class="sxs-lookup"><span data-stu-id="bc644-127">-ApplianceName</span></span>
<span data-ttu-id="bc644-128">A készülék nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bc644-128">Specifies the appliance name.</span></span>
<span data-ttu-id="bc644-129">Ez a belső Térkép egy webhelyre mutat.</span><span class="sxs-lookup"><span data-stu-id="bc644-129">This internally maps to a site.</span></span>

```yaml
Type: System.String
Parameter Sets: GetInSite, ListInSite
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc644-130">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="bc644-130">-DisplayName</span></span>
<span data-ttu-id="bc644-131">A VMware Machine megjelenítendő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bc644-131">Specifies the VMware machine display name.</span></span>

```yaml
Type: System.String
Parameter Sets: List, ListInSite
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc644-132">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="bc644-132">-Name</span></span>
<span data-ttu-id="bc644-133">A VMware Machine nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bc644-133">Specifies the VMware machine name.</span></span>
<span data-ttu-id="bc644-134">Ez egy belső név.</span><span class="sxs-lookup"><span data-stu-id="bc644-134">This is an internal Name.</span></span>
<span data-ttu-id="bc644-135">Felhasználók esetében használja a megjelenítendő nevet.</span><span class="sxs-lookup"><span data-stu-id="bc644-135">For users, use display name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, GetInSite
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc644-136">-Projektnév</span><span class="sxs-lookup"><span data-stu-id="bc644-136">-ProjectName</span></span>
<span data-ttu-id="bc644-137">A projekt áttelepítési nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bc644-137">Specifies the migrate project name.</span></span>

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

### <span data-ttu-id="bc644-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc644-138">-ResourceGroupName</span></span>
<span data-ttu-id="bc644-139">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bc644-139">Specifies the resource group name.</span></span>

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

### <span data-ttu-id="bc644-140">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bc644-140">-SubscriptionId</span></span>
<span data-ttu-id="bc644-141">Az előfizetés azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="bc644-141">Specifies the subscription id.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc644-142">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="bc644-142">-Confirm</span></span>
<span data-ttu-id="bc644-143">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="bc644-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc644-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc644-144">-WhatIf</span></span>
<span data-ttu-id="bc644-145">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="bc644-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bc644-146">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bc644-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc644-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc644-147">CommonParameters</span></span>
<span data-ttu-id="bc644-148">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bc644-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc644-149">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="bc644-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc644-150">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bc644-150">INPUTS</span></span>

## <span data-ttu-id="bc644-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bc644-151">OUTPUTS</span></span>

### <span data-ttu-id="bc644-152">Microsoft. Azure. PowerShell. parancsmagok. áttelepítés. models. Api202001. IVMwareMachine</span><span class="sxs-lookup"><span data-stu-id="bc644-152">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api202001.IVMwareMachine</span></span>

## <span data-ttu-id="bc644-153">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bc644-153">NOTES</span></span>

<span data-ttu-id="bc644-154">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="bc644-154">ALIASES</span></span>

## <span data-ttu-id="bc644-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bc644-155">RELATED LINKS</span></span>
