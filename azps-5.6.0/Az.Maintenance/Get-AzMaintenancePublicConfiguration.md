---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/powershell/module/az.maintenance/get-azmaintenancepublicconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzMaintenancePublicConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzMaintenancePublicConfiguration.md
ms.openlocfilehash: a4625d48086064fb59b5f2faee78357380f6a323
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001238"
---
# <span data-ttu-id="959c6-101">Get-AzMaintenancePublicConfiguration</span><span class="sxs-lookup"><span data-stu-id="959c6-101">Get-AzMaintenancePublicConfiguration</span></span>

## <span data-ttu-id="959c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="959c6-102">SYNOPSIS</span></span>
<span data-ttu-id="959c6-103">A Nyilvános karbantartás konfigurációs rekordjának lekérte</span><span class="sxs-lookup"><span data-stu-id="959c6-103">Get Public Maintenance Configuration record</span></span>

## <span data-ttu-id="959c6-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="959c6-104">SYNTAX</span></span>

```
Get-AzMaintenancePublicConfiguration [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="959c6-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="959c6-105">DESCRIPTION</span></span>
<span data-ttu-id="959c6-106">A Nyilvános karbantartás konfigurációs rekordjának lekérte</span><span class="sxs-lookup"><span data-stu-id="959c6-106">Get Public Maintenance Configuration record</span></span>

## <span data-ttu-id="959c6-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="959c6-107">EXAMPLES</span></span>

### <span data-ttu-id="959c6-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="959c6-108">Example 1</span></span>
```powershell
PS C:\> Get-AzMaintenancePublicConfiguration -ResourceGroupName smdtest -Name workervmscentralus


Location            : centralus
Tags                : {}
NamespaceProperty   :
ExtensionProperties : {"publicMaintenanceConfigurationId" : "workervmscentralus"}
StartDateTime       : 2020-08-01 00:00
ExpirationDateTime  : 2021-08-04 00:00
TimeZone            : Pacific Standard Time
RecurEvery          : Day
Duration            : 05:00
MaintenanceScope    : SQLDB
Visibility          : Public
Id                  : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtest/providers/Microsoft.Maintenance/publicMaintenanceConfigurations/workervmscentralus
Name                : workervmscentralus
Type                : Microsoft.Maintenance/publicMaintenanceConfigurations
```

<span data-ttu-id="959c6-109">A Nyilvános karbantartás konfigurációs rekordjának lekérte</span><span class="sxs-lookup"><span data-stu-id="959c6-109">Get Public Maintenance configuration record</span></span>

## <span data-ttu-id="959c6-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="959c6-110">PARAMETERS</span></span>

### <span data-ttu-id="959c6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="959c6-111">-DefaultProfile</span></span>
<span data-ttu-id="959c6-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="959c6-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="959c6-113">-Name</span><span class="sxs-lookup"><span data-stu-id="959c6-113">-Name</span></span>
<span data-ttu-id="959c6-114">A nyilvános karbantartási konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="959c6-114">The public maintenance configuration Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="959c6-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="959c6-115">-ResourceGroupName</span></span>
<span data-ttu-id="959c6-116">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="959c6-116">The resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="959c6-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="959c6-117">CommonParameters</span></span>
<span data-ttu-id="959c6-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="959c6-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="959c6-119">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="959c6-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="959c6-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="959c6-120">INPUTS</span></span>

### <span data-ttu-id="959c6-121">System.String</span><span class="sxs-lookup"><span data-stu-id="959c6-121">System.String</span></span>

## <span data-ttu-id="959c6-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="959c6-122">OUTPUTS</span></span>

### <span data-ttu-id="959c6-123">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="959c6-123">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span></span>

## <span data-ttu-id="959c6-124">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="959c6-124">NOTES</span></span>

## <span data-ttu-id="959c6-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="959c6-125">RELATED LINKS</span></span>
