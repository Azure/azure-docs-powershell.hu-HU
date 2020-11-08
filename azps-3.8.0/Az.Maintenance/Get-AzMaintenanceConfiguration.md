---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/get-azmaintenanceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzMaintenanceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzMaintenanceConfiguration.md
ms.openlocfilehash: d7bfd36c54d1a141a41d23ede168a64752e1fcd4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014224"
---
# <span data-ttu-id="2968a-101">Get-AzMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="2968a-101">Get-AzMaintenanceConfiguration</span></span>

## <span data-ttu-id="2968a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2968a-102">SYNOPSIS</span></span>
<span data-ttu-id="2968a-103">Karbantartási konfiguráció rekordjának beszerzése</span><span class="sxs-lookup"><span data-stu-id="2968a-103">Get Maintenance configuration record</span></span>

## <span data-ttu-id="2968a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2968a-104">SYNTAX</span></span>

```
Get-AzMaintenanceConfiguration [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2968a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2968a-105">DESCRIPTION</span></span>
<span data-ttu-id="2968a-106">Karbantartási konfiguráció rekordjának beszerzése</span><span class="sxs-lookup"><span data-stu-id="2968a-106">Get Maintenance configuration record</span></span>

## <span data-ttu-id="2968a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="2968a-107">EXAMPLES</span></span>

### <span data-ttu-id="2968a-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="2968a-108">Example 1</span></span>
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

<span data-ttu-id="2968a-109">Karbantartási konfiguráció rekordjának beszerzése</span><span class="sxs-lookup"><span data-stu-id="2968a-109">Get Maintenance configuration record</span></span>

## <span data-ttu-id="2968a-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2968a-110">PARAMETERS</span></span>

### <span data-ttu-id="2968a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2968a-111">-DefaultProfile</span></span>
<span data-ttu-id="2968a-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2968a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2968a-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2968a-113">-Name</span></span>
<span data-ttu-id="2968a-114">A karbantartás konfigurációja név.</span><span class="sxs-lookup"><span data-stu-id="2968a-114">The maintenance configuration Name.</span></span>

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

### <span data-ttu-id="2968a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2968a-115">-ResourceGroupName</span></span>
<span data-ttu-id="2968a-116">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="2968a-116">The resource Group Name.</span></span>

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

### <span data-ttu-id="2968a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2968a-117">CommonParameters</span></span>
<span data-ttu-id="2968a-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2968a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2968a-119">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="2968a-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2968a-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2968a-120">INPUTS</span></span>

### <span data-ttu-id="2968a-121">System. String</span><span class="sxs-lookup"><span data-stu-id="2968a-121">System.String</span></span>

## <span data-ttu-id="2968a-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2968a-122">OUTPUTS</span></span>

### <span data-ttu-id="2968a-123">Microsoft. Azure. commands. Maintenance. models. PSMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="2968a-123">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span></span>

## <span data-ttu-id="2968a-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2968a-124">NOTES</span></span>

## <span data-ttu-id="2968a-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2968a-125">RELATED LINKS</span></span>
