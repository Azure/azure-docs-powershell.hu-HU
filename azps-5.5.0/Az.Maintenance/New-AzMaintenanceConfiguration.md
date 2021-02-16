---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/new-azmaintenanceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzMaintenanceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzMaintenanceConfiguration.md
ms.openlocfilehash: bc2932f91bd2f7361d98ebbe6516ae8bec1513cc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100157514"
---
# <span data-ttu-id="5cf8e-101">New-AzMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="5cf8e-101">New-AzMaintenanceConfiguration</span></span>

## <span data-ttu-id="5cf8e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5cf8e-102">SYNOPSIS</span></span>
<span data-ttu-id="5cf8e-103">Konfigurációs rekord létrehozása vagy frissítése</span><span class="sxs-lookup"><span data-stu-id="5cf8e-103">Create or Update configuration record</span></span>

## <span data-ttu-id="5cf8e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5cf8e-104">SYNTAX</span></span>

```
New-AzMaintenanceConfiguration [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Tag <Hashtable>] [-ExtensionProperty <Hashtable>] [-MaintenanceScope <String>] [-StartDateTime <String>]
 [-ExpirationDateTime <String>] [-Timezone <String>] [-Duration <TimeSpan>] [-Visibility <String>]
 [-RecurEvery <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5cf8e-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5cf8e-105">DESCRIPTION</span></span>
<span data-ttu-id="5cf8e-106">Konfigurációs rekord létrehozása vagy frissítése</span><span class="sxs-lookup"><span data-stu-id="5cf8e-106">Create or Update configuration record</span></span>

## <span data-ttu-id="5cf8e-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5cf8e-107">EXAMPLES</span></span>

### <span data-ttu-id="5cf8e-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="5cf8e-108">Example 1</span></span>
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

<span data-ttu-id="5cf8e-109">Karbantartási konfiguráció létrehozása a Host tartomány segítségével</span><span class="sxs-lookup"><span data-stu-id="5cf8e-109">Create a maintenance configuration with scope Host</span></span>

## <span data-ttu-id="5cf8e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5cf8e-110">PARAMETERS</span></span>

### <span data-ttu-id="5cf8e-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5cf8e-111">-AsJob</span></span>
<span data-ttu-id="5cf8e-112">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="5cf8e-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5cf8e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cf8e-113">-DefaultProfile</span></span>
<span data-ttu-id="5cf8e-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5cf8e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5cf8e-115">-Időtartam</span><span class="sxs-lookup"><span data-stu-id="5cf8e-115">-Duration</span></span>
<span data-ttu-id="5cf8e-116">Az időtartam</span><span class="sxs-lookup"><span data-stu-id="5cf8e-116">The duration</span></span>


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

### <span data-ttu-id="5cf8e-117">-ExpirationDateTime</span><span class="sxs-lookup"><span data-stu-id="5cf8e-117">-ExpirationDateTime</span></span>
<span data-ttu-id="5cf8e-118">The expirationDateTime of the schedule in format YYYY-MM-DD hh:mm</span><span class="sxs-lookup"><span data-stu-id="5cf8e-118">The expirationDateTime of the schedule in format YYYY-MM-DD hh:mm</span></span>

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

### <span data-ttu-id="5cf8e-119">-ExtensionProperty</span><span class="sxs-lookup"><span data-stu-id="5cf8e-119">-ExtensionProperty</span></span>
<span data-ttu-id="5cf8e-120">A Bővítmény tulajdonságai erőforrásonként.</span><span class="sxs-lookup"><span data-stu-id="5cf8e-120">The Extension properties per resource.</span></span>

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

### <span data-ttu-id="5cf8e-121">-Location</span><span class="sxs-lookup"><span data-stu-id="5cf8e-121">-Location</span></span>
<span data-ttu-id="5cf8e-122">A karbantartási konfigurációs hely.</span><span class="sxs-lookup"><span data-stu-id="5cf8e-122">The maintenance configuration location.</span></span>

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

### <span data-ttu-id="5cf8e-123">-MaintenanceScope</span><span class="sxs-lookup"><span data-stu-id="5cf8e-123">-MaintenanceScope</span></span>
<span data-ttu-id="5cf8e-124">A karbantartás hatóköre.</span><span class="sxs-lookup"><span data-stu-id="5cf8e-124">The Maintenance Scope.</span></span>

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

### <span data-ttu-id="5cf8e-125">-Name</span><span class="sxs-lookup"><span data-stu-id="5cf8e-125">-Name</span></span>
<span data-ttu-id="5cf8e-126">A karbantartási konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="5cf8e-126">The maintenance configuration Name.</span></span>

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

### <span data-ttu-id="5cf8e-127">-RecurEvery</span><span class="sxs-lookup"><span data-stu-id="5cf8e-127">-RecurEvery</span></span>
<span data-ttu-id="5cf8e-128">Az ütemezés ismétlődése</span><span class="sxs-lookup"><span data-stu-id="5cf8e-128">The schedule recurrence</span></span>

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

### <span data-ttu-id="5cf8e-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5cf8e-129">-ResourceGroupName</span></span>
<span data-ttu-id="5cf8e-130">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="5cf8e-130">The resource Group Name.</span></span>

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

### <span data-ttu-id="5cf8e-131">-StartDateTime</span><span class="sxs-lookup"><span data-stu-id="5cf8e-131">-StartDateTime</span></span>
<span data-ttu-id="5cf8e-132">The StartDateTime of the schedule in format YYYY-MM-DD hh:mm</span><span class="sxs-lookup"><span data-stu-id="5cf8e-132">The StartDateTime of the schedule in format YYYY-MM-DD hh:mm</span></span>

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

### <span data-ttu-id="5cf8e-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="5cf8e-133">-Tag</span></span>
<span data-ttu-id="5cf8e-134">A ARM címkék.</span><span class="sxs-lookup"><span data-stu-id="5cf8e-134">The ARM Tags.</span></span>

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

### <span data-ttu-id="5cf8e-135">-Timezone</span><span class="sxs-lookup"><span data-stu-id="5cf8e-135">-Timezone</span></span>
<span data-ttu-id="5cf8e-136">Az időzóna</span><span class="sxs-lookup"><span data-stu-id="5cf8e-136">The timezone</span></span>

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

### <span data-ttu-id="5cf8e-137">-Láthatóság</span><span class="sxs-lookup"><span data-stu-id="5cf8e-137">-Visibility</span></span>
<span data-ttu-id="5cf8e-138">A hatókör láthatósága</span><span class="sxs-lookup"><span data-stu-id="5cf8e-138">The visibility of the scope</span></span>

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

### <span data-ttu-id="5cf8e-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5cf8e-139">-Confirm</span></span>
<span data-ttu-id="5cf8e-140">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="5cf8e-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5cf8e-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5cf8e-141">-WhatIf</span></span>
<span data-ttu-id="5cf8e-142">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="5cf8e-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5cf8e-143">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5cf8e-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5cf8e-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cf8e-144">CommonParameters</span></span>
<span data-ttu-id="5cf8e-145">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5cf8e-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cf8e-146">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5cf8e-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cf8e-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5cf8e-147">INPUTS</span></span>

### <span data-ttu-id="5cf8e-148">System.String</span><span class="sxs-lookup"><span data-stu-id="5cf8e-148">System.String</span></span>

## <span data-ttu-id="5cf8e-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5cf8e-149">OUTPUTS</span></span>

### <span data-ttu-id="5cf8e-150">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="5cf8e-150">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span></span>

## <span data-ttu-id="5cf8e-151">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5cf8e-151">NOTES</span></span>

## <span data-ttu-id="5cf8e-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5cf8e-152">RELATED LINKS</span></span>
