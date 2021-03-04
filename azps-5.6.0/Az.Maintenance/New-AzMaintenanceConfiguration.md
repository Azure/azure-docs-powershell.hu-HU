---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/powershell/module/az.maintenance/new-azmaintenanceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzMaintenanceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzMaintenanceConfiguration.md
ms.openlocfilehash: ac264e048ea428ba68caa683eb6076074c9894b8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101935729"
---
# <span data-ttu-id="28313-101">New-AzMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="28313-101">New-AzMaintenanceConfiguration</span></span>

## <span data-ttu-id="28313-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="28313-102">SYNOPSIS</span></span>
<span data-ttu-id="28313-103">Konfigurációs rekord létrehozása vagy frissítése</span><span class="sxs-lookup"><span data-stu-id="28313-103">Create or Update configuration record</span></span>

## <span data-ttu-id="28313-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="28313-104">SYNTAX</span></span>

```
New-AzMaintenanceConfiguration [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Tag <Hashtable>] [-ExtensionProperty <Hashtable>] [-MaintenanceScope <String>] [-StartDateTime <String>]
 [-ExpirationDateTime <String>] [-Timezone <String>] [-Duration <TimeSpan>] [-Visibility <String>]
 [-RecurEvery <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="28313-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="28313-105">DESCRIPTION</span></span>
<span data-ttu-id="28313-106">Konfigurációs rekord létrehozása vagy frissítése</span><span class="sxs-lookup"><span data-stu-id="28313-106">Create or Update configuration record</span></span>

## <span data-ttu-id="28313-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="28313-107">EXAMPLES</span></span>

### <span data-ttu-id="28313-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="28313-108">Example 1</span></span>
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

<span data-ttu-id="28313-109">Karbantartási konfiguráció létrehozása a Host tartomány segítségével</span><span class="sxs-lookup"><span data-stu-id="28313-109">Create a maintenance configuration with scope Host</span></span>

## <span data-ttu-id="28313-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="28313-110">PARAMETERS</span></span>

### <span data-ttu-id="28313-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="28313-111">-AsJob</span></span>
<span data-ttu-id="28313-112">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="28313-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="28313-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28313-113">-DefaultProfile</span></span>
<span data-ttu-id="28313-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="28313-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28313-115">-Időtartam</span><span class="sxs-lookup"><span data-stu-id="28313-115">-Duration</span></span>
<span data-ttu-id="28313-116">Az időtartam</span><span class="sxs-lookup"><span data-stu-id="28313-116">The duration</span></span>


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

### <span data-ttu-id="28313-117">-ExpirationDateTime</span><span class="sxs-lookup"><span data-stu-id="28313-117">-ExpirationDateTime</span></span>
<span data-ttu-id="28313-118">The expirationDateTime of the schedule in format YYYY-MM-DD hh:mm</span><span class="sxs-lookup"><span data-stu-id="28313-118">The expirationDateTime of the schedule in format YYYY-MM-DD hh:mm</span></span>

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

### <span data-ttu-id="28313-119">-ExtensionProperty</span><span class="sxs-lookup"><span data-stu-id="28313-119">-ExtensionProperty</span></span>
<span data-ttu-id="28313-120">A Bővítmény tulajdonságai erőforrásonként.</span><span class="sxs-lookup"><span data-stu-id="28313-120">The Extension properties per resource.</span></span>

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

### <span data-ttu-id="28313-121">-Location</span><span class="sxs-lookup"><span data-stu-id="28313-121">-Location</span></span>
<span data-ttu-id="28313-122">A karbantartási konfigurációs hely.</span><span class="sxs-lookup"><span data-stu-id="28313-122">The maintenance configuration location.</span></span>

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

### <span data-ttu-id="28313-123">-MaintenanceScope</span><span class="sxs-lookup"><span data-stu-id="28313-123">-MaintenanceScope</span></span>
<span data-ttu-id="28313-124">A karbantartás hatóköre.</span><span class="sxs-lookup"><span data-stu-id="28313-124">The Maintenance Scope.</span></span>

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

### <span data-ttu-id="28313-125">-Name</span><span class="sxs-lookup"><span data-stu-id="28313-125">-Name</span></span>
<span data-ttu-id="28313-126">A karbantartási konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="28313-126">The maintenance configuration Name.</span></span>

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

### <span data-ttu-id="28313-127">-RecurEvery</span><span class="sxs-lookup"><span data-stu-id="28313-127">-RecurEvery</span></span>
<span data-ttu-id="28313-128">Az ütemezés ismétlődése</span><span class="sxs-lookup"><span data-stu-id="28313-128">The schedule recurrence</span></span>

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

### <span data-ttu-id="28313-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28313-129">-ResourceGroupName</span></span>
<span data-ttu-id="28313-130">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="28313-130">The resource Group Name.</span></span>

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

### <span data-ttu-id="28313-131">-StartDateTime</span><span class="sxs-lookup"><span data-stu-id="28313-131">-StartDateTime</span></span>
<span data-ttu-id="28313-132">The StartDateTime of the schedule in format YYYY-MM-DD hh:mm</span><span class="sxs-lookup"><span data-stu-id="28313-132">The StartDateTime of the schedule in format YYYY-MM-DD hh:mm</span></span>

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

### <span data-ttu-id="28313-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="28313-133">-Tag</span></span>
<span data-ttu-id="28313-134">A ARM címkék.</span><span class="sxs-lookup"><span data-stu-id="28313-134">The ARM Tags.</span></span>

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

### <span data-ttu-id="28313-135">-Timezone</span><span class="sxs-lookup"><span data-stu-id="28313-135">-Timezone</span></span>
<span data-ttu-id="28313-136">Az időzóna</span><span class="sxs-lookup"><span data-stu-id="28313-136">The timezone</span></span>

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

### <span data-ttu-id="28313-137">-Láthatóság</span><span class="sxs-lookup"><span data-stu-id="28313-137">-Visibility</span></span>
<span data-ttu-id="28313-138">A hatókör láthatósága</span><span class="sxs-lookup"><span data-stu-id="28313-138">The visibility of the scope</span></span>

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

### <span data-ttu-id="28313-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="28313-139">-Confirm</span></span>
<span data-ttu-id="28313-140">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="28313-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28313-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28313-141">-WhatIf</span></span>
<span data-ttu-id="28313-142">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="28313-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28313-143">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="28313-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28313-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28313-144">CommonParameters</span></span>
<span data-ttu-id="28313-145">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28313-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28313-146">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="28313-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28313-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="28313-147">INPUTS</span></span>

### <span data-ttu-id="28313-148">System.String</span><span class="sxs-lookup"><span data-stu-id="28313-148">System.String</span></span>

## <span data-ttu-id="28313-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="28313-149">OUTPUTS</span></span>

### <span data-ttu-id="28313-150">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="28313-150">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span></span>

## <span data-ttu-id="28313-151">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="28313-151">NOTES</span></span>

## <span data-ttu-id="28313-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="28313-152">RELATED LINKS</span></span>
