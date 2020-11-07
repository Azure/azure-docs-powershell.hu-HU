---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/stop-azsdiskmigrationjob
schema: 2.0.0
ms.openlocfilehash: bb5c78d6c0ae29d415e02d3e78e79f963bc3315c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844846"
---
# <span data-ttu-id="57231-101">Stop-AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="57231-101">Stop-AzsDiskMigrationJob</span></span>

## <span data-ttu-id="57231-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="57231-102">SYNOPSIS</span></span>
<span data-ttu-id="57231-103">Áttelepítési feladat visszavonása</span><span class="sxs-lookup"><span data-stu-id="57231-103">Cancel a disk migration job.</span></span>

## <span data-ttu-id="57231-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="57231-104">SYNTAX</span></span>

```
Stop-AzsDiskMigrationJob -Name <String> [-Location <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="57231-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="57231-105">DESCRIPTION</span></span>
<span data-ttu-id="57231-106">Áttelepítési feladat visszavonása</span><span class="sxs-lookup"><span data-stu-id="57231-106">Cancel a disk migration job.</span></span>

## <span data-ttu-id="57231-107">Példák</span><span class="sxs-lookup"><span data-stu-id="57231-107">EXAMPLES</span></span>

### <span data-ttu-id="57231-108">Példa 1:</span><span class="sxs-lookup"><span data-stu-id="57231-108">Example 1:</span></span>
```powershell
PS C:\> Stop-AzsDiskMigrationJob -Name TestJob

CreationTime : 2/26/2020 11:06:40 AM
EndTime      : 2/26/2020 11:07:24 AM
Id           : /subscriptions/627fecef-520e-4c18-94e0-8f0665ba86a7/providers/Microsoft.Compute.Admin/locations/redmond/diskmigrati
               onjobs/TestJob
Location     : redmond
MigrationId  : TestJob
Name         : redmond/TestJob
StartTime    : 2/26/2020 11:06:40 AM
Status       : Canceled
Subtask      : {47774498-6bc7-4ce2-98ca-738739ded2fc, b09ac623-f71d-480c-98bc-88fa3f603f2c}
TargetShare  : \\SU1FileServer.s31r1801.masd.stbtest.microsoft.com\SU1_ObjStore_4
Type         : Microsoft.Compute.Admin/locations/diskmigrationjobs
```

<span data-ttu-id="57231-109">Felügyelt áttelepítési feladat visszavonása</span><span class="sxs-lookup"><span data-stu-id="57231-109">Cancel a managed disk migration job.</span></span>

## <span data-ttu-id="57231-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="57231-110">PARAMETERS</span></span>

### <span data-ttu-id="57231-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57231-111">-DefaultProfile</span></span>
<span data-ttu-id="57231-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="57231-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="57231-113">-Hely</span><span class="sxs-lookup"><span data-stu-id="57231-113">-Location</span></span>
<span data-ttu-id="57231-114">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="57231-114">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="57231-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="57231-115">-Name</span></span>
<span data-ttu-id="57231-116">Az áttelepítési feladat GUID-neve.</span><span class="sxs-lookup"><span data-stu-id="57231-116">The migration job guid name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MigrationId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="57231-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="57231-117">-SubscriptionId</span></span>
<span data-ttu-id="57231-118">A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="57231-118">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="57231-119">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="57231-119">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="57231-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="57231-120">-Confirm</span></span>
<span data-ttu-id="57231-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="57231-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57231-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57231-122">-WhatIf</span></span>
<span data-ttu-id="57231-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="57231-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57231-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="57231-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57231-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57231-125">CommonParameters</span></span>
<span data-ttu-id="57231-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="57231-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57231-127">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="57231-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57231-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="57231-128">INPUTS</span></span>

## <span data-ttu-id="57231-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="57231-129">OUTPUTS</span></span>

### <span data-ttu-id="57231-130">Microsoft. Azure. PowerShell. parancsmagok. ComputeAdmin. modellek. Api20180730Preview. IDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="57231-130">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180730Preview.IDiskMigrationJob</span></span>



## <span data-ttu-id="57231-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="57231-131">NOTES</span></span>

## <span data-ttu-id="57231-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="57231-132">RELATED LINKS</span></span>

