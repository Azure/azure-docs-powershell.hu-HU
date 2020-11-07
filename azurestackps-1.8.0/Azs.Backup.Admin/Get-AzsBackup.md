---
external help file: Azs.Backup.Admin-help.xml
Module Name: Azs.Backup.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: b51280387ad3eb29f05bee8876765a621e0d07c4
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2020
ms.locfileid: "93840389"
---
# <span data-ttu-id="b8bc7-101">Get-AzsBackup</span><span class="sxs-lookup"><span data-stu-id="b8bc7-101">Get-AzsBackup</span></span>

## <span data-ttu-id="b8bc7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b8bc7-102">SYNOPSIS</span></span>
<span data-ttu-id="b8bc7-103">A név alapján kapott hely biztonsági másolatát adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="b8bc7-103">Returns a backup from a location based on name.</span></span>

## <span data-ttu-id="b8bc7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b8bc7-104">SYNTAX</span></span>

### <span data-ttu-id="b8bc7-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b8bc7-105">List (Default)</span></span>
```
Get-AzsBackup [-Location <String>] [-ResourceGroupName <String>] [-Top <Int32>] [-Skip <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="b8bc7-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="b8bc7-106">Get</span></span>
```
Get-AzsBackup -Name <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="b8bc7-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="b8bc7-107">ResourceId</span></span>
```
Get-AzsBackup -ResourceId <String> [<CommonParameters>]
```

### <span data-ttu-id="b8bc7-108">ParentResource</span><span class="sxs-lookup"><span data-stu-id="b8bc7-108">ParentResource</span></span>
```
Get-AzsBackup -ParentResource <BackupLocation> [-Top <Int32>] [-Skip <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="b8bc7-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="b8bc7-109">DESCRIPTION</span></span>
<span data-ttu-id="b8bc7-110">A név alapján kapott hely biztonsági másolatát adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="b8bc7-110">Returns a backup from a location based on name.</span></span>

## <span data-ttu-id="b8bc7-111">Példák</span><span class="sxs-lookup"><span data-stu-id="b8bc7-111">EXAMPLES</span></span>

### <span data-ttu-id="b8bc7-112">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="b8bc7-112">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsBackup
```

<span data-ttu-id="b8bc7-113">Információkat kaphat az Azure sbout minden biztonsági mentéséről.</span><span class="sxs-lookup"><span data-stu-id="b8bc7-113">Get information sbout all Azure Stack backups.</span></span>

### <span data-ttu-id="b8bc7-114">--------------------------PÉLDA 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="b8bc7-114">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsBackup -Name 'backupName'
```

<span data-ttu-id="b8bc7-115">Információkat kaphat a megadott Azure-halom biztonsági mentéséhez.</span><span class="sxs-lookup"><span data-stu-id="b8bc7-115">Get information for the the specified Azure Stack backup.</span></span>

## <span data-ttu-id="b8bc7-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b8bc7-116">PARAMETERS</span></span>

### <span data-ttu-id="b8bc7-117">-Hely</span><span class="sxs-lookup"><span data-stu-id="b8bc7-117">-Location</span></span>
<span data-ttu-id="b8bc7-118">A hely biztonsági másolata</span><span class="sxs-lookup"><span data-stu-id="b8bc7-118">Location backed up.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8bc7-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b8bc7-119">-Name</span></span>
<span data-ttu-id="b8bc7-120">A biztonsági másolat neve.</span><span class="sxs-lookup"><span data-stu-id="b8bc7-120">Name of the backup.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8bc7-121">-ParentResource</span><span class="sxs-lookup"><span data-stu-id="b8bc7-121">-ParentResource</span></span>
<span data-ttu-id="b8bc7-122">A biztonsági mentési hely átadásakor a biztonsági másolatban található összes biztonsági mentés megjelenik.</span><span class="sxs-lookup"><span data-stu-id="b8bc7-122">Passing a backup location will return the list of all backups at that backup location.</span></span>

```yaml
Type: BackupLocation
Parameter Sets: ParentResource
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b8bc7-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8bc7-123">-ResourceGroupName</span></span>
<span data-ttu-id="b8bc7-124">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="b8bc7-124">Name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8bc7-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b8bc7-125">-ResourceId</span></span>
<span data-ttu-id="b8bc7-126">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="b8bc7-126">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8bc7-127">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="b8bc7-127">-Skip</span></span>
<span data-ttu-id="b8bc7-128">{{Fill skip Description}}</span><span class="sxs-lookup"><span data-stu-id="b8bc7-128">{{Fill Skip Description}}</span></span>

```yaml
Type: Int32
Parameter Sets: List, ParentResource
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8bc7-129">-Top</span><span class="sxs-lookup"><span data-stu-id="b8bc7-129">-Top</span></span>
<span data-ttu-id="b8bc7-130">{{Fill Top Description}}</span><span class="sxs-lookup"><span data-stu-id="b8bc7-130">{{Fill Top Description}}</span></span>

```yaml
Type: Int32
Parameter Sets: List, ParentResource
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8bc7-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8bc7-131">CommonParameters</span></span>
<span data-ttu-id="b8bc7-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b8bc7-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8bc7-133">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8bc7-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8bc7-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b8bc7-134">INPUTS</span></span>

## <span data-ttu-id="b8bc7-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b8bc7-135">OUTPUTS</span></span>

### <span data-ttu-id="b8bc7-136">Microsoft. AzureStack. Management. backup. admin. models. backup</span><span class="sxs-lookup"><span data-stu-id="b8bc7-136">Microsoft.AzureStack.Management.Backup.Admin.Models.Backup</span></span>

## <span data-ttu-id="b8bc7-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b8bc7-137">NOTES</span></span>

## <span data-ttu-id="b8bc7-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b8bc7-138">RELATED LINKS</span></span>

