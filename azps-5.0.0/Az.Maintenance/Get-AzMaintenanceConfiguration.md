---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/get-azmaintenanceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzMaintenanceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzMaintenanceConfiguration.md
ms.openlocfilehash: d7bfd36c54d1a141a41d23ede168a64752e1fcd4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187356"
---
# <span data-ttu-id="e0310-101">Get-AzMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="e0310-101">Get-AzMaintenanceConfiguration</span></span>

## <span data-ttu-id="e0310-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e0310-102">SYNOPSIS</span></span>
<span data-ttu-id="e0310-103">Karbantartási konfiguráció rekordjának beszerzése</span><span class="sxs-lookup"><span data-stu-id="e0310-103">Get Maintenance configuration record</span></span>

## <span data-ttu-id="e0310-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e0310-104">SYNTAX</span></span>

```
Get-AzMaintenanceConfiguration [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e0310-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e0310-105">DESCRIPTION</span></span>
<span data-ttu-id="e0310-106">Karbantartási konfiguráció rekordjának beszerzése</span><span class="sxs-lookup"><span data-stu-id="e0310-106">Get Maintenance configuration record</span></span>

## <span data-ttu-id="e0310-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e0310-107">EXAMPLES</span></span>

### <span data-ttu-id="e0310-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e0310-108">Example 1</span></span>
```powershell
PS C:\> Get-AzMaintenanceConfiguration -ResourceGroupName smdtest -Name workervmscentralus


Location            : centralus
Tags                : {}
NamespaceProperty   :
ExtensionProperties : {}
MaintenanceScope    : Host
Id                  : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtest/providers/Microsoft.Maintenance/maintenanceConfigurations/workervmscentralus
Name                : workervmscentralus
Type                : Microsoft.Maintenance/maintenanceConfigurations
```

<span data-ttu-id="e0310-109">Karbantartási konfiguráció rekordjának beszerzése</span><span class="sxs-lookup"><span data-stu-id="e0310-109">Get Maintenance configuration record</span></span>

## <span data-ttu-id="e0310-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e0310-110">PARAMETERS</span></span>

### <span data-ttu-id="e0310-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0310-111">-DefaultProfile</span></span>
<span data-ttu-id="e0310-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e0310-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0310-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e0310-113">-Name</span></span>
<span data-ttu-id="e0310-114">A karbantartás konfigurációja név.</span><span class="sxs-lookup"><span data-stu-id="e0310-114">The maintenance configuration Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0310-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0310-115">-ResourceGroupName</span></span>
<span data-ttu-id="e0310-116">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="e0310-116">The resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0310-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0310-117">CommonParameters</span></span>
<span data-ttu-id="e0310-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e0310-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0310-119">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e0310-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0310-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e0310-120">INPUTS</span></span>

### <span data-ttu-id="e0310-121">System. String</span><span class="sxs-lookup"><span data-stu-id="e0310-121">System.String</span></span>

## <span data-ttu-id="e0310-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e0310-122">OUTPUTS</span></span>

### <span data-ttu-id="e0310-123">Microsoft. Azure. commands. Maintenance. models. PSMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="e0310-123">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span></span>

## <span data-ttu-id="e0310-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e0310-124">NOTES</span></span>

## <span data-ttu-id="e0310-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e0310-125">RELATED LINKS</span></span>
