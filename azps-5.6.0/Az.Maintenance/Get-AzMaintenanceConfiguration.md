---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/powershell/module/az.maintenance/get-azmaintenanceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzMaintenanceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzMaintenanceConfiguration.md
ms.openlocfilehash: 6939cde26695cb4273d776437c3697c03d426db3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101934930"
---
# <span data-ttu-id="db46d-101">Get-AzMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="db46d-101">Get-AzMaintenanceConfiguration</span></span>

## <span data-ttu-id="db46d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="db46d-102">SYNOPSIS</span></span>
<span data-ttu-id="db46d-103">A Karbantartás konfigurációs rekord lekérte</span><span class="sxs-lookup"><span data-stu-id="db46d-103">Get Maintenance configuration record</span></span>

## <span data-ttu-id="db46d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="db46d-104">SYNTAX</span></span>

```
Get-AzMaintenanceConfiguration [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="db46d-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="db46d-105">DESCRIPTION</span></span>
<span data-ttu-id="db46d-106">A Karbantartás konfigurációs rekord lekérte</span><span class="sxs-lookup"><span data-stu-id="db46d-106">Get Maintenance configuration record</span></span>

## <span data-ttu-id="db46d-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="db46d-107">EXAMPLES</span></span>

### <span data-ttu-id="db46d-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="db46d-108">Example 1</span></span>
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

<span data-ttu-id="db46d-109">A Karbantartás konfigurációs rekord lekérte</span><span class="sxs-lookup"><span data-stu-id="db46d-109">Get Maintenance configuration record</span></span>

## <span data-ttu-id="db46d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="db46d-110">PARAMETERS</span></span>

### <span data-ttu-id="db46d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db46d-111">-DefaultProfile</span></span>
<span data-ttu-id="db46d-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="db46d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db46d-113">-Name</span><span class="sxs-lookup"><span data-stu-id="db46d-113">-Name</span></span>
<span data-ttu-id="db46d-114">A karbantartási konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="db46d-114">The maintenance configuration Name.</span></span>

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

### <span data-ttu-id="db46d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db46d-115">-ResourceGroupName</span></span>
<span data-ttu-id="db46d-116">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="db46d-116">The resource Group Name.</span></span>

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

### <span data-ttu-id="db46d-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db46d-117">CommonParameters</span></span>
<span data-ttu-id="db46d-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db46d-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db46d-119">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="db46d-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db46d-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="db46d-120">INPUTS</span></span>

### <span data-ttu-id="db46d-121">System.String</span><span class="sxs-lookup"><span data-stu-id="db46d-121">System.String</span></span>

## <span data-ttu-id="db46d-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="db46d-122">OUTPUTS</span></span>

### <span data-ttu-id="db46d-123">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="db46d-123">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span></span>

## <span data-ttu-id="db46d-124">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="db46d-124">NOTES</span></span>

## <span data-ttu-id="db46d-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="db46d-125">RELATED LINKS</span></span>
