---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/update-azmaintenanceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Update-AzMaintenanceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Update-AzMaintenanceConfiguration.md
ms.openlocfilehash: ed6f94944f00cd138d3140c2bd69029a98ea9f15
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187349"
---
# <span data-ttu-id="de9e2-101">Update-AzMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="de9e2-101">Update-AzMaintenanceConfiguration</span></span>

## <span data-ttu-id="de9e2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="de9e2-102">SYNOPSIS</span></span>
<span data-ttu-id="de9e2-103">A javítások konfigurációs rekordja</span><span class="sxs-lookup"><span data-stu-id="de9e2-103">Patch configuration record</span></span>

## <span data-ttu-id="de9e2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="de9e2-104">SYNTAX</span></span>

```
Update-AzMaintenanceConfiguration [-ResourceGroupName] <String> [-Name] <String>
 [-Configuration] <PSMaintenanceConfiguration> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="de9e2-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="de9e2-105">DESCRIPTION</span></span>
<span data-ttu-id="de9e2-106">Javítás-karbantartási konfigurációs rekord</span><span class="sxs-lookup"><span data-stu-id="de9e2-106">Patch maintenance configuration record</span></span>

## <span data-ttu-id="de9e2-107">Példák</span><span class="sxs-lookup"><span data-stu-id="de9e2-107">EXAMPLES</span></span>

### <span data-ttu-id="de9e2-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="de9e2-108">Example 1</span></span>
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

<span data-ttu-id="de9e2-109">Javítás-karbantartási konfigurációs rekord</span><span class="sxs-lookup"><span data-stu-id="de9e2-109">Patch maintenance configuration record</span></span>

## <span data-ttu-id="de9e2-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="de9e2-110">PARAMETERS</span></span>

### <span data-ttu-id="de9e2-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="de9e2-111">-AsJob</span></span>
<span data-ttu-id="de9e2-112">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="de9e2-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="de9e2-113">-Configuration</span><span class="sxs-lookup"><span data-stu-id="de9e2-113">-Configuration</span></span>
<span data-ttu-id="de9e2-114">A frissítendő karbantartási konfiguráció.</span><span class="sxs-lookup"><span data-stu-id="de9e2-114">The maintenance configuration to be updated.</span></span>

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

### <span data-ttu-id="de9e2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de9e2-115">-DefaultProfile</span></span>
<span data-ttu-id="de9e2-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="de9e2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de9e2-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="de9e2-117">-Name</span></span>
<span data-ttu-id="de9e2-118">A karbantartás konfigurációja név.</span><span class="sxs-lookup"><span data-stu-id="de9e2-118">The maintenance configuration Name.</span></span>

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

### <span data-ttu-id="de9e2-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de9e2-119">-ResourceGroupName</span></span>
<span data-ttu-id="de9e2-120">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="de9e2-120">The resource Group Name.</span></span>

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

### <span data-ttu-id="de9e2-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="de9e2-121">-Confirm</span></span>
<span data-ttu-id="de9e2-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="de9e2-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de9e2-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de9e2-123">-WhatIf</span></span>
<span data-ttu-id="de9e2-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="de9e2-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de9e2-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="de9e2-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de9e2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de9e2-126">CommonParameters</span></span>
<span data-ttu-id="de9e2-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="de9e2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de9e2-128">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="de9e2-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de9e2-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="de9e2-129">INPUTS</span></span>

### <span data-ttu-id="de9e2-130">System. String</span><span class="sxs-lookup"><span data-stu-id="de9e2-130">System.String</span></span>

### <span data-ttu-id="de9e2-131">Microsoft. Azure. commands. Maintenance. models. PSMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="de9e2-131">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span></span>

## <span data-ttu-id="de9e2-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="de9e2-132">OUTPUTS</span></span>

### <span data-ttu-id="de9e2-133">Microsoft. Azure. commands. Maintenance. models. PSMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="de9e2-133">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span></span>

## <span data-ttu-id="de9e2-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="de9e2-134">NOTES</span></span>

## <span data-ttu-id="de9e2-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="de9e2-135">RELATED LINKS</span></span>