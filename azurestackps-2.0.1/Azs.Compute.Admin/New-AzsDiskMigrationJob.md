---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/new-azsdiskmigrationjob
schema: 2.0.0
ms.openlocfilehash: c3fd190fb033a685bcb0d5087c544298681e47c5
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/24/2020
ms.locfileid: "94015370"
---
# <span data-ttu-id="c1d59-101">New-AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="c1d59-101">New-AzsDiskMigrationJob</span></span>

## <span data-ttu-id="c1d59-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c1d59-102">SYNOPSIS</span></span>


## <span data-ttu-id="c1d59-103">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c1d59-103">SYNTAX</span></span>

### <span data-ttu-id="c1d59-104">Volume (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c1d59-104">Volume (Default)</span></span>
```
New-AzsDiskMigrationJob -Name <String> -TargetScaleUnit <String> -TargetVolumeLabel <String> -Disks <IDisk[]>
 [-Location <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="c1d59-105">Megosztása</span><span class="sxs-lookup"><span data-stu-id="c1d59-105">Share</span></span>
```
New-AzsDiskMigrationJob -Name <String> -TargetShare <String> -Disks <IDisk[]> [-Location <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c1d59-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="c1d59-106">DESCRIPTION</span></span>


## <span data-ttu-id="c1d59-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c1d59-107">EXAMPLES</span></span>

### <span data-ttu-id="c1d59-108">Példa 1:</span><span class="sxs-lookup"><span data-stu-id="c1d59-108">Example 1:</span></span>
```powershell
PS C:\> $disks = Get-AzsDisk
PS C:\> New-AzsDiskMigrationJob -Name TestJob1 -TargetScaleUnit s-cluster -TargetVolumeLabel ObjStore_2 -Disks $disks

CreationTime : 2/26/2020 10:56:32 AM
EndTime      : 
Id           : /subscriptions/627fecef-520e-4c18-94e0-8f0665ba86a7/providers/Microsoft.Compute.Admin/locations/redmond/diskmigrationjobs/TestJob1
Location     : redmond
MigrationId  : TestJob1
Name         : redmond/TestJob1
StartTime    : 
Status       : Pending
Subtask      : {53ee3665-00e4-4c69-a067-524058905ead, d551734f-0370-4851-9704-c7cec80b34c5}
TargetShare  : \\SU1FileServer.s31r1801.masd.stbtest.microsoft.com\SU1_ObjStore_2
Type         : Microsoft.Compute.Admin/locations/diskmigrationjobs
```

<span data-ttu-id="c1d59-109">Hozzon létre áttelepítési feladatot a lemezek áttelepítéséhez a cél léptékű egységéhez és kötetéhez.</span><span class="sxs-lookup"><span data-stu-id="c1d59-109">Create a disk migration job to migrate disks to the target scale unit and volume.</span></span>

### <span data-ttu-id="c1d59-110">2. példa:</span><span class="sxs-lookup"><span data-stu-id="c1d59-110">Example 2:</span></span> 
```powershell
PS C:\> PS C:\> $disks = Get-AzsDisk
PS C:\> New-AzsDiskMigrationJob -Name TestJob2 -TargetShare \\SU1FileServer.s31r1801.masd.stbtest.microsoft.com\SU1_ObjStore_3 -Disks $disks
WARNING: TargetShare parameter will be deprecated in a future release, please use Volume instead.

CreationTime : 2/26/2020 11:02:48 AM
EndTime      : 
Id           : /subscriptions/627fecef-520e-4c18-94e0-8f0665ba86a7/providers/Microsoft.Compute.Admin/locations/redmond/diskmigrati
               onjobs/TestJob2
Location     : redmond
MigrationId  : TestJob2
Name         : redmond/TestJob2
StartTime    : 
Status       : Pending
Subtask      : {0cfd8d29-1ca4-42db-a490-9198814abc50, 89c9b15e-47c6-4321-a390-611fc190cfad}
TargetShare  : \\SU1FileServer.s31r1801.masd.stbtest.microsoft.com\SU1_ObjStore_3
Type         : Microsoft.Compute.Admin/locations/diskmigrationjobs-AzsDiskMigrationJob -Name TestJob1 -TargetScaleUnit s-cluster -TargetVolumeLabel ObjStore_2 -Disks $disks

```

<span data-ttu-id="c1d59-111">Hozzon létre áttelepítési feladatot a lemezek áttelepítéséhez a cél megosztásba.</span><span class="sxs-lookup"><span data-stu-id="c1d59-111">Create a disk migration job to migrate disks to the target share.</span></span>

## <span data-ttu-id="c1d59-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c1d59-112">PARAMETERS</span></span>

### <span data-ttu-id="c1d59-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1d59-113">-DefaultProfile</span></span>


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

### <span data-ttu-id="c1d59-114">-Lemezek</span><span class="sxs-lookup"><span data-stu-id="c1d59-114">-Disks</span></span>
<span data-ttu-id="c1d59-115">A kivitelezéshez lásd: jegyzetek szakasz a lemezek tulajdonságaihoz, és hozzon létre egy kivonatoló táblázatot.</span><span class="sxs-lookup"><span data-stu-id="c1d59-115">To construct, see NOTES section for DISKS properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180730Preview.IDisk[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="c1d59-116">-Hely</span><span class="sxs-lookup"><span data-stu-id="c1d59-116">-Location</span></span>


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

### <span data-ttu-id="c1d59-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c1d59-117">-Name</span></span>


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

### <span data-ttu-id="c1d59-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c1d59-118">-SubscriptionId</span></span>


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

### <span data-ttu-id="c1d59-119">-TargetScaleUnit</span><span class="sxs-lookup"><span data-stu-id="c1d59-119">-TargetScaleUnit</span></span>


```yaml
Type: System.String
Parameter Sets: Volume
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c1d59-120">-TargetShare</span><span class="sxs-lookup"><span data-stu-id="c1d59-120">-TargetShare</span></span>


```yaml
Type: System.String
Parameter Sets: Share
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c1d59-121">-TargetVolumeLabel</span><span class="sxs-lookup"><span data-stu-id="c1d59-121">-TargetVolumeLabel</span></span>


```yaml
Type: System.String
Parameter Sets: Volume
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c1d59-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c1d59-122">-Confirm</span></span>
<span data-ttu-id="c1d59-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c1d59-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1d59-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1d59-124">-WhatIf</span></span>
<span data-ttu-id="c1d59-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c1d59-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1d59-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c1d59-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1d59-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1d59-127">CommonParameters</span></span>
<span data-ttu-id="c1d59-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c1d59-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1d59-129">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c1d59-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1d59-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c1d59-130">INPUTS</span></span>

### <span data-ttu-id="c1d59-131">Microsoft. Azure. PowerShell. parancsmagok. ComputeAdmin. models. Api20180730Preview. IDisk []</span><span class="sxs-lookup"><span data-stu-id="c1d59-131">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180730Preview.IDisk[]</span></span>

## <span data-ttu-id="c1d59-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c1d59-132">OUTPUTS</span></span>

### <span data-ttu-id="c1d59-133">Microsoft. Azure. PowerShell. parancsmagok. ComputeAdmin. modellek. Api20180730Preview. IDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="c1d59-133">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180730Preview.IDiskMigrationJob</span></span>



### <span data-ttu-id="c1d59-134">Start-AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="c1d59-134">Start-AzsDiskMigrationJob</span></span>

## <span data-ttu-id="c1d59-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c1d59-135">NOTES</span></span>

<span data-ttu-id="c1d59-136">KOMPLEX paraméterek: az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="c1d59-136">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c1d59-137">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="c1d59-137">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="c1d59-138">LEMEZEK <IDisk [] >:</span><span class="sxs-lookup"><span data-stu-id="c1d59-138">DISKS <IDisk[]>:</span></span> 
  - <span data-ttu-id="c1d59-139">`[Location <String>]`: Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="c1d59-139">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="c1d59-140">`[DiskId <String>]`: A lemezvezérlő-azonosító.</span><span class="sxs-lookup"><span data-stu-id="c1d59-140">`[DiskId <String>]`: The disk id.</span></span>
  - <span data-ttu-id="c1d59-141">`[SharePath <String>]`: A Disk Share Path.</span><span class="sxs-lookup"><span data-stu-id="c1d59-141">`[SharePath <String>]`: The disk share path.</span></span>
  - <span data-ttu-id="c1d59-142">`[Status <DiskState?>]`: A lemez állapota.</span><span class="sxs-lookup"><span data-stu-id="c1d59-142">`[Status <DiskState?>]`: The disk status.</span></span>

## <span data-ttu-id="c1d59-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c1d59-143">RELATED LINKS</span></span>

