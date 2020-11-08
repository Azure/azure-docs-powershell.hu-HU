---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/get-azmaintenancepublicconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzMaintenancePublicConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzMaintenancePublicConfiguration.md
ms.openlocfilehash: 8df9e8145e1acb03c0351f30565da2d9a8ed4a9d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181647"
---
# <span data-ttu-id="dbf17-101">Get-AzMaintenancePublicConfiguration</span><span class="sxs-lookup"><span data-stu-id="dbf17-101">Get-AzMaintenancePublicConfiguration</span></span>

## <span data-ttu-id="dbf17-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="dbf17-102">SYNOPSIS</span></span>
<span data-ttu-id="dbf17-103">Nyilvános karbantartási konfiguráció rekordjának beszerzése</span><span class="sxs-lookup"><span data-stu-id="dbf17-103">Get Public Maintenance Configuration record</span></span>

## <span data-ttu-id="dbf17-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="dbf17-104">SYNTAX</span></span>

```
Get-AzMaintenancePublicConfiguration [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dbf17-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="dbf17-105">DESCRIPTION</span></span>
<span data-ttu-id="dbf17-106">Nyilvános karbantartási konfiguráció rekordjának beszerzése</span><span class="sxs-lookup"><span data-stu-id="dbf17-106">Get Public Maintenance Configuration record</span></span>

## <span data-ttu-id="dbf17-107">Példák</span><span class="sxs-lookup"><span data-stu-id="dbf17-107">EXAMPLES</span></span>

### <span data-ttu-id="dbf17-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="dbf17-108">Example 1</span></span>
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

<span data-ttu-id="dbf17-109">Nyilvános karbantartási konfiguráció rekordjának beszerzése</span><span class="sxs-lookup"><span data-stu-id="dbf17-109">Get Public Maintenance configuration record</span></span>

## <span data-ttu-id="dbf17-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="dbf17-110">PARAMETERS</span></span>

### <span data-ttu-id="dbf17-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbf17-111">-DefaultProfile</span></span>
<span data-ttu-id="dbf17-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="dbf17-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dbf17-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="dbf17-113">-Name</span></span>
<span data-ttu-id="dbf17-114">A nyilvános karbantartás konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="dbf17-114">The public maintenance configuration Name.</span></span>

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

### <span data-ttu-id="dbf17-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dbf17-115">-ResourceGroupName</span></span>
<span data-ttu-id="dbf17-116">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="dbf17-116">The resource Group Name.</span></span>

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

### <span data-ttu-id="dbf17-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbf17-117">CommonParameters</span></span>
<span data-ttu-id="dbf17-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="dbf17-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbf17-119">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="dbf17-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbf17-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="dbf17-120">INPUTS</span></span>

### <span data-ttu-id="dbf17-121">System. String</span><span class="sxs-lookup"><span data-stu-id="dbf17-121">System.String</span></span>

## <span data-ttu-id="dbf17-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dbf17-122">OUTPUTS</span></span>

### <span data-ttu-id="dbf17-123">Microsoft. Azure. commands. Maintenance. models. PSMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="dbf17-123">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span></span>

## <span data-ttu-id="dbf17-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="dbf17-124">NOTES</span></span>

## <span data-ttu-id="dbf17-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dbf17-125">RELATED LINKS</span></span>
