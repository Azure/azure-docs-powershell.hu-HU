---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/get-azmaintenanceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzMaintenanceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzMaintenanceConfiguration.md
ms.openlocfilehash: d7bfd36c54d1a141a41d23ede168a64752e1fcd4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181651"
---
# <span data-ttu-id="37a5f-101">Get-AzMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="37a5f-101">Get-AzMaintenanceConfiguration</span></span>

## <span data-ttu-id="37a5f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="37a5f-102">SYNOPSIS</span></span>
<span data-ttu-id="37a5f-103">Karbantartási konfiguráció rekordjának beszerzése</span><span class="sxs-lookup"><span data-stu-id="37a5f-103">Get Maintenance configuration record</span></span>

## <span data-ttu-id="37a5f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="37a5f-104">SYNTAX</span></span>

```
Get-AzMaintenanceConfiguration [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="37a5f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="37a5f-105">DESCRIPTION</span></span>
<span data-ttu-id="37a5f-106">Karbantartási konfiguráció rekordjának beszerzése</span><span class="sxs-lookup"><span data-stu-id="37a5f-106">Get Maintenance configuration record</span></span>

## <span data-ttu-id="37a5f-107">Példák</span><span class="sxs-lookup"><span data-stu-id="37a5f-107">EXAMPLES</span></span>

### <span data-ttu-id="37a5f-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="37a5f-108">Example 1</span></span>
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

<span data-ttu-id="37a5f-109">Karbantartási konfiguráció rekordjának beszerzése</span><span class="sxs-lookup"><span data-stu-id="37a5f-109">Get Maintenance configuration record</span></span>

## <span data-ttu-id="37a5f-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="37a5f-110">PARAMETERS</span></span>

### <span data-ttu-id="37a5f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37a5f-111">-DefaultProfile</span></span>
<span data-ttu-id="37a5f-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="37a5f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37a5f-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="37a5f-113">-Name</span></span>
<span data-ttu-id="37a5f-114">A karbantartás konfigurációja név.</span><span class="sxs-lookup"><span data-stu-id="37a5f-114">The maintenance configuration Name.</span></span>

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

### <span data-ttu-id="37a5f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37a5f-115">-ResourceGroupName</span></span>
<span data-ttu-id="37a5f-116">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="37a5f-116">The resource Group Name.</span></span>

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

### <span data-ttu-id="37a5f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37a5f-117">CommonParameters</span></span>
<span data-ttu-id="37a5f-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="37a5f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37a5f-119">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="37a5f-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37a5f-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="37a5f-120">INPUTS</span></span>

### <span data-ttu-id="37a5f-121">System. String</span><span class="sxs-lookup"><span data-stu-id="37a5f-121">System.String</span></span>

## <span data-ttu-id="37a5f-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="37a5f-122">OUTPUTS</span></span>

### <span data-ttu-id="37a5f-123">Microsoft. Azure. commands. Maintenance. models. PSMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="37a5f-123">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span></span>

## <span data-ttu-id="37a5f-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="37a5f-124">NOTES</span></span>

## <span data-ttu-id="37a5f-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="37a5f-125">RELATED LINKS</span></span>
