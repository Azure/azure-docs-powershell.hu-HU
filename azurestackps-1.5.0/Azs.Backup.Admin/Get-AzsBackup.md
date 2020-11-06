---
external help file: Azs.Backup.Admin-help.xml
Module Name: Azs.Backup.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: fb306ed03cb9ab1f06209345474b2ef196d9e1d8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491504"
---
# <span data-ttu-id="5a30c-101">Get-AzsBackup</span><span class="sxs-lookup"><span data-stu-id="5a30c-101">Get-AzsBackup</span></span>

## <span data-ttu-id="5a30c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5a30c-102">SYNOPSIS</span></span>
<span data-ttu-id="5a30c-103">A név alapján kapott hely biztonsági másolatát adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="5a30c-103">Returns a backup from a location based on name.</span></span>

## <span data-ttu-id="5a30c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5a30c-104">SYNTAX</span></span>

### <span data-ttu-id="5a30c-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5a30c-105">List (Default)</span></span>
```
Get-AzsBackup [-Location <String>] [-ResourceGroupName <String>] [-Top <Int32>] [-Skip <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="5a30c-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="5a30c-106">Get</span></span>
```
Get-AzsBackup -Name <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="5a30c-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="5a30c-107">ResourceId</span></span>
```
Get-AzsBackup -ResourceId <String> [<CommonParameters>]
```

### <span data-ttu-id="5a30c-108">ParentResource</span><span class="sxs-lookup"><span data-stu-id="5a30c-108">ParentResource</span></span>
```
Get-AzsBackup -ParentResource <BackupLocation> [-Top <Int32>] [-Skip <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="5a30c-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="5a30c-109">DESCRIPTION</span></span>
<span data-ttu-id="5a30c-110">A név alapján kapott hely biztonsági másolatát adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="5a30c-110">Returns a backup from a location based on name.</span></span>

## <span data-ttu-id="5a30c-111">Példák</span><span class="sxs-lookup"><span data-stu-id="5a30c-111">EXAMPLES</span></span>

### <span data-ttu-id="5a30c-112">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="5a30c-112">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsBackup
```

<span data-ttu-id="5a30c-113">Információkat kaphat az Azure-halom biztonsági másolatáról.</span><span class="sxs-lookup"><span data-stu-id="5a30c-113">Get information about all Azure Stack backups.</span></span>

### <span data-ttu-id="5a30c-114">--------------------------PÉLDA 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="5a30c-114">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsBackup -Name 'backupName'
```

<span data-ttu-id="5a30c-115">Információkat kaphat a megadott Azure-halom biztonsági mentéséhez.</span><span class="sxs-lookup"><span data-stu-id="5a30c-115">Get information for the specified Azure Stack backup.</span></span>

## <span data-ttu-id="5a30c-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5a30c-116">PARAMETERS</span></span>

### <span data-ttu-id="5a30c-117">-Hely</span><span class="sxs-lookup"><span data-stu-id="5a30c-117">-Location</span></span>
<span data-ttu-id="5a30c-118">A hely biztonsági másolata</span><span class="sxs-lookup"><span data-stu-id="5a30c-118">Location backed up.</span></span>

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

### <span data-ttu-id="5a30c-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5a30c-119">-Name</span></span>
<span data-ttu-id="5a30c-120">A biztonsági másolat neve.</span><span class="sxs-lookup"><span data-stu-id="5a30c-120">Name of the backup.</span></span>

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

### <span data-ttu-id="5a30c-121">-ParentResource</span><span class="sxs-lookup"><span data-stu-id="5a30c-121">-ParentResource</span></span>
<span data-ttu-id="5a30c-122">A biztonsági mentési hely átadásakor a biztonsági másolatban található összes biztonsági mentés megjelenik.</span><span class="sxs-lookup"><span data-stu-id="5a30c-122">Passing a backup location will return the list of all backups at that backup location.</span></span>

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

### <span data-ttu-id="5a30c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a30c-123">-ResourceGroupName</span></span>
<span data-ttu-id="5a30c-124">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="5a30c-124">Name of the resource group.</span></span>

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

### <span data-ttu-id="5a30c-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5a30c-125">-ResourceId</span></span>
<span data-ttu-id="5a30c-126">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="5a30c-126">The resource id.</span></span>

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

### <span data-ttu-id="5a30c-127">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="5a30c-127">-Skip</span></span>
<span data-ttu-id="5a30c-128">Az első N elem kihagyása a paraméterben megadott értékkel.</span><span class="sxs-lookup"><span data-stu-id="5a30c-128">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="5a30c-129">-Top</span><span class="sxs-lookup"><span data-stu-id="5a30c-129">-Top</span></span>
<span data-ttu-id="5a30c-130">A paraméterben megadott módon adja vissza a legfelső N-elemeket.</span><span class="sxs-lookup"><span data-stu-id="5a30c-130">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="5a30c-131">A-kihagyás paraméter után érvényes.</span><span class="sxs-lookup"><span data-stu-id="5a30c-131">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="5a30c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a30c-132">CommonParameters</span></span>
<span data-ttu-id="5a30c-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5a30c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a30c-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a30c-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a30c-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5a30c-135">INPUTS</span></span>

## <span data-ttu-id="5a30c-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5a30c-136">OUTPUTS</span></span>

### <span data-ttu-id="5a30c-137">Microsoft. AzureStack. Management. backup. admin. models. backup</span><span class="sxs-lookup"><span data-stu-id="5a30c-137">Microsoft.AzureStack.Management.Backup.Admin.Models.Backup</span></span>

## <span data-ttu-id="5a30c-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5a30c-138">NOTES</span></span>

## <span data-ttu-id="5a30c-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5a30c-139">RELATED LINKS</span></span>

