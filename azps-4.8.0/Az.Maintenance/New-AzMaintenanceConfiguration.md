---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/new-azmaintenanceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzMaintenanceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzMaintenanceConfiguration.md
ms.openlocfilehash: bc2932f91bd2f7361d98ebbe6516ae8bec1513cc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181640"
---
# <span data-ttu-id="64532-101">New-AzMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="64532-101">New-AzMaintenanceConfiguration</span></span>

## <span data-ttu-id="64532-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="64532-102">SYNOPSIS</span></span>
<span data-ttu-id="64532-103">Konfigurációs rekord létrehozása vagy frissítése</span><span class="sxs-lookup"><span data-stu-id="64532-103">Create or Update configuration record</span></span>

## <span data-ttu-id="64532-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="64532-104">SYNTAX</span></span>

```
New-AzMaintenanceConfiguration [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Tag <Hashtable>] [-ExtensionProperty <Hashtable>] [-MaintenanceScope <String>] [-StartDateTime <String>]
 [-ExpirationDateTime <String>] [-Timezone <String>] [-Duration <TimeSpan>] [-Visibility <String>]
 [-RecurEvery <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="64532-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="64532-105">DESCRIPTION</span></span>
<span data-ttu-id="64532-106">Konfigurációs rekord létrehozása vagy frissítése</span><span class="sxs-lookup"><span data-stu-id="64532-106">Create or Update configuration record</span></span>

## <span data-ttu-id="64532-107">Példák</span><span class="sxs-lookup"><span data-stu-id="64532-107">EXAMPLES</span></span>

### <span data-ttu-id="64532-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="64532-108">Example 1</span></span>
```powershell
PS C:\> New-AzMaintenanceConfiguration -ResourceGroupName smdtest -Name workervmscentralus -MaintenanceScope Host -Location centralus -StartDateTime 2020-08-01 00:00 -ExpirationDateTime 2021-08-04 00:00 -TimeZone Pacific Standard Time -Duration 05:00 -RecurEvery Day


Location            : centralus
Tags                : {}
ExtensionProperties : {}
MaintenanceScope    : Host
StartDateTime       : 2020-08-01 00:00
ExpirationDateTime  : 2021-08-04 00:00
TimeZone            : Pacific Standard Time
RecurEvery          : Day
Duration            : 05:00
MaintenanceScope    : Host
Visibility          : Custom
Id                  : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtest/providers/Microsoft.Maintenance/maintenanceConfigurations/workervmscentralus
Name                : workervmscentralus
Type                : Microsoft.Maintenance/maintenanceConfigurations
```

<span data-ttu-id="64532-109">Karbantartási konfiguráció létrehozása a hatókör-állomással</span><span class="sxs-lookup"><span data-stu-id="64532-109">Create a maintenance configuration with scope Host</span></span>

## <span data-ttu-id="64532-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="64532-110">PARAMETERS</span></span>

### <span data-ttu-id="64532-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="64532-111">-AsJob</span></span>
<span data-ttu-id="64532-112">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="64532-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="64532-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64532-113">-DefaultProfile</span></span>
<span data-ttu-id="64532-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="64532-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64532-115">-Időtartam</span><span class="sxs-lookup"><span data-stu-id="64532-115">-Duration</span></span>
<span data-ttu-id="64532-116">Az időtartam</span><span class="sxs-lookup"><span data-stu-id="64532-116">The duration</span></span>


```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64532-117">-ExpirationDateTime</span><span class="sxs-lookup"><span data-stu-id="64532-117">-ExpirationDateTime</span></span>
<span data-ttu-id="64532-118">Az ütemterv expirationDateTime éééé-hh-nn óó: PP formátumban</span><span class="sxs-lookup"><span data-stu-id="64532-118">The expirationDateTime of the schedule in format YYYY-MM-DD hh:mm</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64532-119">-ExtensionProperty</span><span class="sxs-lookup"><span data-stu-id="64532-119">-ExtensionProperty</span></span>
<span data-ttu-id="64532-120">A kiterjesztés tulajdonságai erőforrás szerint</span><span class="sxs-lookup"><span data-stu-id="64532-120">The Extension properties per resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64532-121">-Hely</span><span class="sxs-lookup"><span data-stu-id="64532-121">-Location</span></span>
<span data-ttu-id="64532-122">A karbantartási konfiguráció helye.</span><span class="sxs-lookup"><span data-stu-id="64532-122">The maintenance configuration location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64532-123">-MaintenanceScope</span><span class="sxs-lookup"><span data-stu-id="64532-123">-MaintenanceScope</span></span>
<span data-ttu-id="64532-124">A karbantartás hatóköre.</span><span class="sxs-lookup"><span data-stu-id="64532-124">The Maintenance Scope.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64532-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="64532-125">-Name</span></span>
<span data-ttu-id="64532-126">A karbantartás konfigurációja név.</span><span class="sxs-lookup"><span data-stu-id="64532-126">The maintenance configuration Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64532-127">-RecurEvery</span><span class="sxs-lookup"><span data-stu-id="64532-127">-RecurEvery</span></span>
<span data-ttu-id="64532-128">Az ütemezés ismétlődése</span><span class="sxs-lookup"><span data-stu-id="64532-128">The schedule recurrence</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64532-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64532-129">-ResourceGroupName</span></span>
<span data-ttu-id="64532-130">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="64532-130">The resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64532-131">-StartDateTime</span><span class="sxs-lookup"><span data-stu-id="64532-131">-StartDateTime</span></span>
<span data-ttu-id="64532-132">Az ütemterv StartDateTime éééé-hh-nn óó: PP formátumban</span><span class="sxs-lookup"><span data-stu-id="64532-132">The StartDateTime of the schedule in format YYYY-MM-DD hh:mm</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64532-133">-Címke</span><span class="sxs-lookup"><span data-stu-id="64532-133">-Tag</span></span>
<span data-ttu-id="64532-134">A kar címkéi.</span><span class="sxs-lookup"><span data-stu-id="64532-134">The ARM Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64532-135">-Időzóna</span><span class="sxs-lookup"><span data-stu-id="64532-135">-Timezone</span></span>
<span data-ttu-id="64532-136">Az időzóna</span><span class="sxs-lookup"><span data-stu-id="64532-136">The timezone</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64532-137">-Láthatóság</span><span class="sxs-lookup"><span data-stu-id="64532-137">-Visibility</span></span>
<span data-ttu-id="64532-138">A hatókör láthatósága</span><span class="sxs-lookup"><span data-stu-id="64532-138">The visibility of the scope</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64532-139">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="64532-139">-Confirm</span></span>
<span data-ttu-id="64532-140">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="64532-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64532-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64532-141">-WhatIf</span></span>
<span data-ttu-id="64532-142">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="64532-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64532-143">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="64532-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64532-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64532-144">CommonParameters</span></span>
<span data-ttu-id="64532-145">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="64532-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64532-146">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="64532-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64532-147">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="64532-147">INPUTS</span></span>

### <span data-ttu-id="64532-148">System. String</span><span class="sxs-lookup"><span data-stu-id="64532-148">System.String</span></span>

## <span data-ttu-id="64532-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="64532-149">OUTPUTS</span></span>

### <span data-ttu-id="64532-150">Microsoft. Azure. commands. Maintenance. models. PSMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="64532-150">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span></span>

## <span data-ttu-id="64532-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="64532-151">NOTES</span></span>

## <span data-ttu-id="64532-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="64532-152">RELATED LINKS</span></span>
