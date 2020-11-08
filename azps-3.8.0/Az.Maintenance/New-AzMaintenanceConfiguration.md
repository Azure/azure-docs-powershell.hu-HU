---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/new-azmaintenanceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzMaintenanceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzMaintenanceConfiguration.md
ms.openlocfilehash: eb51fe99a1dbfdd5838fcd4fd5de93a5d7fb36e3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014220"
---
# <span data-ttu-id="3b770-101">New-AzMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="3b770-101">New-AzMaintenanceConfiguration</span></span>

## <span data-ttu-id="3b770-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3b770-102">SYNOPSIS</span></span>
<span data-ttu-id="3b770-103">Konfigurációs rekord létrehozása vagy frissítése</span><span class="sxs-lookup"><span data-stu-id="3b770-103">Create or Update configuration record</span></span>

## <span data-ttu-id="3b770-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3b770-104">SYNTAX</span></span>

```
New-AzMaintenanceConfiguration [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Tag <Hashtable>] [-ExtensionProperty <Hashtable>] [-MaintenanceScope <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b770-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3b770-105">DESCRIPTION</span></span>
<span data-ttu-id="3b770-106">Konfigurációs rekord létrehozása vagy frissítése</span><span class="sxs-lookup"><span data-stu-id="3b770-106">Create or Update configuration record</span></span>

## <span data-ttu-id="3b770-107">Példák</span><span class="sxs-lookup"><span data-stu-id="3b770-107">EXAMPLES</span></span>

### <span data-ttu-id="3b770-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="3b770-108">Example 1</span></span>
```powershell
PS C:\> New-AzMaintenanceConfiguration -ResourceGroupName smdtest -Name workervmscentralus -MaintenanceScope Host -Location centralus


Location            : centralus
Tags                : {}
ExtensionProperties : {}
MaintenanceScope    : Host
Id                  : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtest/providers/Microsoft.Maintenance/maintenanceConfigurations/workervmscentralus
Name                : workervmscentralus
Type                : Microsoft.Maintenance/maintenanceConfigurations
```

<span data-ttu-id="3b770-109">Karbantartási konfiguráció létrehozása a hatókör-állomással</span><span class="sxs-lookup"><span data-stu-id="3b770-109">Create a maintenance configuration with scope Host</span></span>

## <span data-ttu-id="3b770-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3b770-110">PARAMETERS</span></span>

### <span data-ttu-id="3b770-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3b770-111">-AsJob</span></span>
<span data-ttu-id="3b770-112">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="3b770-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3b770-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b770-113">-DefaultProfile</span></span>
<span data-ttu-id="3b770-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3b770-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3b770-115">-ExtensionProperty</span><span class="sxs-lookup"><span data-stu-id="3b770-115">-ExtensionProperty</span></span>
<span data-ttu-id="3b770-116">A kiterjesztés tulajdonságai erőforrás szerint</span><span class="sxs-lookup"><span data-stu-id="3b770-116">The Extension properties per resource.</span></span>

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

### <span data-ttu-id="3b770-117">-Hely</span><span class="sxs-lookup"><span data-stu-id="3b770-117">-Location</span></span>
<span data-ttu-id="3b770-118">A karbantartási konfiguráció helye.</span><span class="sxs-lookup"><span data-stu-id="3b770-118">The maintenance configuration location.</span></span>

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

### <span data-ttu-id="3b770-119">-MaintenanceScope</span><span class="sxs-lookup"><span data-stu-id="3b770-119">-MaintenanceScope</span></span>
<span data-ttu-id="3b770-120">A karbantartás hatóköre.</span><span class="sxs-lookup"><span data-stu-id="3b770-120">The Maintenance Scope.</span></span>

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

### <span data-ttu-id="3b770-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3b770-121">-Name</span></span>
<span data-ttu-id="3b770-122">A karbantartás konfigurációja név.</span><span class="sxs-lookup"><span data-stu-id="3b770-122">The maintenance configuration Name.</span></span>

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

### <span data-ttu-id="3b770-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b770-123">-ResourceGroupName</span></span>
<span data-ttu-id="3b770-124">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="3b770-124">The resource Group Name.</span></span>

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

### <span data-ttu-id="3b770-125">-Címke</span><span class="sxs-lookup"><span data-stu-id="3b770-125">-Tag</span></span>
<span data-ttu-id="3b770-126">A kar címkéi.</span><span class="sxs-lookup"><span data-stu-id="3b770-126">The ARM Tags.</span></span>

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

### <span data-ttu-id="3b770-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3b770-127">-Confirm</span></span>
<span data-ttu-id="3b770-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3b770-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b770-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b770-129">-WhatIf</span></span>
<span data-ttu-id="3b770-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3b770-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b770-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3b770-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b770-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b770-132">CommonParameters</span></span>
<span data-ttu-id="3b770-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3b770-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b770-134">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="3b770-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b770-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3b770-135">INPUTS</span></span>

### <span data-ttu-id="3b770-136">System. String</span><span class="sxs-lookup"><span data-stu-id="3b770-136">System.String</span></span>

## <span data-ttu-id="3b770-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3b770-137">OUTPUTS</span></span>

### <span data-ttu-id="3b770-138">Microsoft. Azure. commands. Maintenance. models. PSMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="3b770-138">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span></span>

## <span data-ttu-id="3b770-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3b770-139">NOTES</span></span>

## <span data-ttu-id="3b770-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3b770-140">RELATED LINKS</span></span>
