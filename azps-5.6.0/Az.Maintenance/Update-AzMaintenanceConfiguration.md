---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/powershell/module/az.maintenance/update-azmaintenanceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Update-AzMaintenanceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Update-AzMaintenanceConfiguration.md
ms.openlocfilehash: d2131d542d845e065e1aae05a272b045ffa882f6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101935697"
---
# <span data-ttu-id="7846d-101">Update-AzMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="7846d-101">Update-AzMaintenanceConfiguration</span></span>

## <span data-ttu-id="7846d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7846d-102">SYNOPSIS</span></span>
<span data-ttu-id="7846d-103">Javításkonfigurációs rekord</span><span class="sxs-lookup"><span data-stu-id="7846d-103">Patch configuration record</span></span>

## <span data-ttu-id="7846d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7846d-104">SYNTAX</span></span>

```
Update-AzMaintenanceConfiguration [-ResourceGroupName] <String> [-Name] <String>
 [-Configuration] <PSMaintenanceConfiguration> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7846d-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7846d-105">DESCRIPTION</span></span>
<span data-ttu-id="7846d-106">Javításkarbantartás konfigurációs rekordja</span><span class="sxs-lookup"><span data-stu-id="7846d-106">Patch maintenance configuration record</span></span>

## <span data-ttu-id="7846d-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7846d-107">EXAMPLES</span></span>

### <span data-ttu-id="7846d-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="7846d-108">Example 1</span></span>
```powershell
PS C:\> Update-AzMaintenanceConfiguration -ResourceGroupName smdtest -Name workervmscentralus -Configuration $configuration


Location            : centralus
Tags                : {}
ExtensionProperties : {}
MaintenanceScope    : Host
Id                  : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtest/providers/Microsoft.Maintenance/maintenanceConfigurations/workervmscentralus
Name                : workervmscentralus
Type                : Microsoft.Maintenance/maintenanceConfigurations
```

<span data-ttu-id="7846d-109">Javításkarbantartás konfigurációs rekordja</span><span class="sxs-lookup"><span data-stu-id="7846d-109">Patch maintenance configuration record</span></span>

## <span data-ttu-id="7846d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7846d-110">PARAMETERS</span></span>

### <span data-ttu-id="7846d-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7846d-111">-AsJob</span></span>
<span data-ttu-id="7846d-112">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="7846d-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7846d-113">- Konfiguráció</span><span class="sxs-lookup"><span data-stu-id="7846d-113">-Configuration</span></span>
<span data-ttu-id="7846d-114">A frissíthető karbantartási konfiguráció.</span><span class="sxs-lookup"><span data-stu-id="7846d-114">The maintenance configuration to be updated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7846d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7846d-115">-DefaultProfile</span></span>
<span data-ttu-id="7846d-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7846d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7846d-117">-Name</span><span class="sxs-lookup"><span data-stu-id="7846d-117">-Name</span></span>
<span data-ttu-id="7846d-118">A karbantartási konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="7846d-118">The maintenance configuration Name.</span></span>

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

### <span data-ttu-id="7846d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7846d-119">-ResourceGroupName</span></span>
<span data-ttu-id="7846d-120">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="7846d-120">The resource Group Name.</span></span>

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

### <span data-ttu-id="7846d-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7846d-121">-Confirm</span></span>
<span data-ttu-id="7846d-122">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="7846d-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7846d-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7846d-123">-WhatIf</span></span>
<span data-ttu-id="7846d-124">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="7846d-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7846d-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7846d-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7846d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7846d-126">CommonParameters</span></span>
<span data-ttu-id="7846d-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7846d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7846d-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7846d-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7846d-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7846d-129">INPUTS</span></span>

### <span data-ttu-id="7846d-130">System.String</span><span class="sxs-lookup"><span data-stu-id="7846d-130">System.String</span></span>

### <span data-ttu-id="7846d-131">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="7846d-131">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span></span>

## <span data-ttu-id="7846d-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7846d-132">OUTPUTS</span></span>

### <span data-ttu-id="7846d-133">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="7846d-133">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span></span>

## <span data-ttu-id="7846d-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7846d-134">NOTES</span></span>

## <span data-ttu-id="7846d-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7846d-135">RELATED LINKS</span></span>
