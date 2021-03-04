---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/get-azmigratediscoveredserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateDiscoveredServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateDiscoveredServer.md
ms.openlocfilehash: 79a61ea316247fe3d76f5ad0b202d30037cb839c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101934097"
---
# <span data-ttu-id="90423-101">Get-AzMigrateDiscoveredServer</span><span class="sxs-lookup"><span data-stu-id="90423-101">Get-AzMigrateDiscoveredServer</span></span>

## <span data-ttu-id="90423-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="90423-102">SYNOPSIS</span></span>
<span data-ttu-id="90423-103">Szerezze be az összes felfedezett kiszolgálót egy áttelepítési projektben.</span><span class="sxs-lookup"><span data-stu-id="90423-103">Get All discovered servers in a migrate project.</span></span>

## <span data-ttu-id="90423-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="90423-104">SYNTAX</span></span>

### <span data-ttu-id="90423-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="90423-105">List (Default)</span></span>
```
Get-AzMigrateDiscoveredServer -ProjectName <String> -ResourceGroupName <String> [-DisplayName <String>]
 [-SubscriptionId <String[]>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="90423-106">Bej.le</span><span class="sxs-lookup"><span data-stu-id="90423-106">Get</span></span>
```
Get-AzMigrateDiscoveredServer -Name <String> -ProjectName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="90423-107">GetInSite</span><span class="sxs-lookup"><span data-stu-id="90423-107">GetInSite</span></span>
```
Get-AzMigrateDiscoveredServer -ApplianceName <String> -Name <String> -ProjectName <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="90423-108">ListInSite</span><span class="sxs-lookup"><span data-stu-id="90423-108">ListInSite</span></span>
```
Get-AzMigrateDiscoveredServer -ApplianceName <String> -ProjectName <String> -ResourceGroupName <String>
 [-DisplayName <String>] [-SubscriptionId <String[]>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="90423-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="90423-109">DESCRIPTION</span></span>
<span data-ttu-id="90423-110">A kiszolgálói parancsmag azure-áttelepítése a projekt összes kiszolgálóját lehívja.</span><span class="sxs-lookup"><span data-stu-id="90423-110">Get Azure migrate server commandlet fetches all servers in a migrate project.</span></span>

## <span data-ttu-id="90423-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="90423-111">EXAMPLES</span></span>

### <span data-ttu-id="90423-112">1. példa: Lista</span><span class="sxs-lookup"><span data-stu-id="90423-112">Example 1: List</span></span>
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

<span data-ttu-id="90423-113">Szerezze be az összes kiszolgálót egy áttelepítési projektbe.</span><span class="sxs-lookup"><span data-stu-id="90423-113">Get All servers in a migrate project.</span></span>

### <span data-ttu-id="90423-114">2. példa: Get</span><span class="sxs-lookup"><span data-stu-id="90423-114">Example 2: Get</span></span>
```powershell
PS C:\> Get-AzMigrateDiscoveredServer -Name idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029e62c-31d2-a6c3-5316-aa39f47c49fc -SubscriptionId xxx-xxx-xxx -ResourceGroupName julytest -ProjectName julytest

Name                                                                                                      Typeo…
----                                                                                                      ----o…
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029e62c-31d2-a6c3-5316-aa39f47c49fc Microsoft.OffAzure/VMwareSites/machines

```

<span data-ttu-id="90423-115">Kiszolgáló létrehozása projekt áttelepítéséhez név szerint.</span><span class="sxs-lookup"><span data-stu-id="90423-115">Get a server in a migrate project by name.</span></span>
<span data-ttu-id="90423-116">A név a kiszolgáló egyedi paramétere.</span><span class="sxs-lookup"><span data-stu-id="90423-116">Name is a unique paramenter for a server.</span></span>

### <span data-ttu-id="90423-117">3. példa: Lista egy készülékben</span><span class="sxs-lookup"><span data-stu-id="90423-117">Example 3: List in an appliance</span></span>
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

<span data-ttu-id="90423-118">List all servers for an berendezés in a project.</span><span class="sxs-lookup"><span data-stu-id="90423-118">List all servers for an appliance in a project.</span></span>

### <span data-ttu-id="90423-119">4. példa: Készülék használata</span><span class="sxs-lookup"><span data-stu-id="90423-119">Example 4: Get in an appliance</span></span>
```powershell
PS C:\> Get-AzMigrateDiscoveredServer -Name idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029e62c-31d2-a6c3-5316-aa39f47c49fc -ApplianceName BBVMwareAVS -SubscriptionId xxx-xxx-xxx -ResourceGroupName julytest -ProjectName julytest

Name                                                                                                      Typeo…
----                                                                                                      ----o…
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029e62c-31d2-a6c3-5316-aa39f47c49fc Microsoft.OffAzure/VMwareSites/machines

```

<span data-ttu-id="90423-120">Kiszolgálót kell szereznie egy berendezéshez egy projektben.</span><span class="sxs-lookup"><span data-stu-id="90423-120">Get a server for an appliance in a project.</span></span>
<span data-ttu-id="90423-121">A név a kiszolgáló egyedi paramétere.</span><span class="sxs-lookup"><span data-stu-id="90423-121">Name is a unique paramenter for a server.</span></span>

### <span data-ttu-id="90423-122">5. példa: Lista és szűrés megjelenítendő név alapján</span><span class="sxs-lookup"><span data-stu-id="90423-122">Example 5: List and filter by display name</span></span>
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

<span data-ttu-id="90423-123">List servers in a migrate project and filter responses with display name.</span><span class="sxs-lookup"><span data-stu-id="90423-123">List servers in a migrate project and filter responses with display name.</span></span>

### <span data-ttu-id="90423-124">6. példa: Lista egy készülékben, és szűrés megjelenítendő név alapján</span><span class="sxs-lookup"><span data-stu-id="90423-124">Example 6: List in an appliance and filter by display name</span></span>
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

<span data-ttu-id="90423-125">List servers for an berendezés in a mirate project and filter responses with display name.</span><span class="sxs-lookup"><span data-stu-id="90423-125">List servers for an appliance in a migrate project and filter responses with display name.</span></span>

## <span data-ttu-id="90423-126">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="90423-126">PARAMETERS</span></span>

### <span data-ttu-id="90423-127">-Gépnév</span><span class="sxs-lookup"><span data-stu-id="90423-127">-ApplianceName</span></span>
<span data-ttu-id="90423-128">A készülék nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="90423-128">Specifies the appliance name.</span></span>
<span data-ttu-id="90423-129">Ez belsőleg egy webhelyhez van leképezve.</span><span class="sxs-lookup"><span data-stu-id="90423-129">This internally maps to a site.</span></span>

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

### <span data-ttu-id="90423-130">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="90423-130">-DisplayName</span></span>
<span data-ttu-id="90423-131">A VMware-számítógép megjelenítendő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="90423-131">Specifies the VMware machine display name.</span></span>

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

### <span data-ttu-id="90423-132">-Name</span><span class="sxs-lookup"><span data-stu-id="90423-132">-Name</span></span>
<span data-ttu-id="90423-133">A VMware számítógép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="90423-133">Specifies the VMware machine name.</span></span>
<span data-ttu-id="90423-134">Ez egy belső név.</span><span class="sxs-lookup"><span data-stu-id="90423-134">This is an internal Name.</span></span>
<span data-ttu-id="90423-135">A felhasználóknak használja a megjelenítendő nevet.</span><span class="sxs-lookup"><span data-stu-id="90423-135">For users, use display name.</span></span>

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

### <span data-ttu-id="90423-136">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="90423-136">-ProjectName</span></span>
<span data-ttu-id="90423-137">A projekt nevét határozza meg.</span><span class="sxs-lookup"><span data-stu-id="90423-137">Specifies the migrate project name.</span></span>

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

### <span data-ttu-id="90423-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90423-138">-ResourceGroupName</span></span>
<span data-ttu-id="90423-139">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="90423-139">Specifies the resource group name.</span></span>

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

### <span data-ttu-id="90423-140">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="90423-140">-SubscriptionId</span></span>
<span data-ttu-id="90423-141">Az előfizetés azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="90423-141">Specifies the subscription id.</span></span>

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

### <span data-ttu-id="90423-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="90423-142">-Confirm</span></span>
<span data-ttu-id="90423-143">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="90423-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90423-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90423-144">-WhatIf</span></span>
<span data-ttu-id="90423-145">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="90423-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90423-146">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="90423-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90423-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90423-147">CommonParameters</span></span>
<span data-ttu-id="90423-148">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90423-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90423-149">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="90423-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90423-150">INPUTS</span><span class="sxs-lookup"><span data-stu-id="90423-150">INPUTS</span></span>

## <span data-ttu-id="90423-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="90423-151">OUTPUTS</span></span>

### <span data-ttu-id="90423-152">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api202001.IVMwareMachine</span><span class="sxs-lookup"><span data-stu-id="90423-152">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api202001.IVMwareMachine</span></span>

## <span data-ttu-id="90423-153">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="90423-153">NOTES</span></span>

<span data-ttu-id="90423-154">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="90423-154">ALIASES</span></span>

## <span data-ttu-id="90423-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="90423-155">RELATED LINKS</span></span>

