---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azdiagnosticsettingcategory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDiagnosticSettingCategory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDiagnosticSettingCategory.md
ms.openlocfilehash: 29c65ef5f5ec3b2b54fb883da706ddc9a38e1d4d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100147410"
---
# <span data-ttu-id="e4100-101">Get-AzDiagnosticSettingCategory</span><span class="sxs-lookup"><span data-stu-id="e4100-101">Get-AzDiagnosticSettingCategory</span></span>

## <span data-ttu-id="e4100-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e4100-102">SYNOPSIS</span></span>
<span data-ttu-id="e4100-103">Szerezze be vagy sorolja fel az Azure-erőforrás támogatott diagnosztikai beállításkategóriáját.</span><span class="sxs-lookup"><span data-stu-id="e4100-103">Get or list supported diagnostic setting category for Azure resource.</span></span>

## <span data-ttu-id="e4100-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e4100-104">SYNTAX</span></span>

```
Get-AzDiagnosticSettingCategory -TargetResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e4100-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e4100-105">DESCRIPTION</span></span>
<span data-ttu-id="e4100-106">Szerezze be vagy sorolja fel az Azure-erőforrás támogatott diagnosztikai beállításkategóriáját.</span><span class="sxs-lookup"><span data-stu-id="e4100-106">Get or list supported diagnostic setting category for Azure resource.</span></span>

## <span data-ttu-id="e4100-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e4100-107">EXAMPLES</span></span>

### <span data-ttu-id="e4100-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="e4100-108">Example 1</span></span>
```powershell
PS C:\> Get-AzDiagnosticSettingCategory -TargetResourceId /subscriptions/XXXXXXXXXXXX/resourceGroups/XXXXXXXX/providers/Microsoft.Network/virtualNetworks/XXXXXXXX
Id           : /subscriptions/XXXXXXXXXXXX/resourceGroups/XXXXXXXX/providers/Microsoft.Network/virtualNetworks/XXXXXXXX/providers/microsoft.insights/diagnosticSettingsCategories/VMProtectionAlerts
Name         : VMProtectionAlerts
Type         : microsoft.insights/diagnosticSettingsCategories
CategoryType : Logs

Id           : /subscriptions/XXXXXXXXXXXX/resourceGroups/XXXXXXXX/providers/Microsoft.Network/virtualNetworks/XXXXXXXX/providers/microsoft.insights/diagnosticSettingsCategories/AllMetrics
Name         : AllMetrics
Type         : microsoft.insights/diagnosticSettingsCategories
CategoryType : Metrics
```

<span data-ttu-id="e4100-109">A támogatott diagnosztikai beállítások kategóriái a virtuális hálózathoz.</span><span class="sxs-lookup"><span data-stu-id="e4100-109">Get supported diagnostic setting categories for virtual network.</span></span>

## <span data-ttu-id="e4100-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e4100-110">PARAMETERS</span></span>

### <span data-ttu-id="e4100-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4100-111">-DefaultProfile</span></span>
<span data-ttu-id="e4100-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e4100-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e4100-113">-Name</span><span class="sxs-lookup"><span data-stu-id="e4100-113">-Name</span></span>
<span data-ttu-id="e4100-114">A diagnosztikai beállítások kategóriájának neve</span><span class="sxs-lookup"><span data-stu-id="e4100-114">Name of diagnostic setting category</span></span>

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

### <span data-ttu-id="e4100-115">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="e4100-115">-TargetResourceId</span></span>
<span data-ttu-id="e4100-116">Célerőforrás azonosítója</span><span class="sxs-lookup"><span data-stu-id="e4100-116">Target resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4100-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4100-117">CommonParameters</span></span>
<span data-ttu-id="e4100-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4100-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4100-119">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e4100-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4100-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e4100-120">INPUTS</span></span>

### <span data-ttu-id="e4100-121">System.String</span><span class="sxs-lookup"><span data-stu-id="e4100-121">System.String</span></span>

## <span data-ttu-id="e4100-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e4100-122">OUTPUTS</span></span>

### <span data-ttu-id="e4100-123">Microsoft.Azure.Commands.Insights.OutputClasses.PSDiagnosticSettingCategory</span><span class="sxs-lookup"><span data-stu-id="e4100-123">Microsoft.Azure.Commands.Insights.OutputClasses.PSDiagnosticSettingCategory</span></span>

## <span data-ttu-id="e4100-124">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e4100-124">NOTES</span></span>

## <span data-ttu-id="e4100-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e4100-125">RELATED LINKS</span></span>
