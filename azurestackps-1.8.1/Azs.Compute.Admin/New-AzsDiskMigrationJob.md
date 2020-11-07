---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: db6eff0b0b0e0698c42dd7905cd3e5f7879345e1
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93840579"
---
# <span data-ttu-id="71e31-101">New-AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="71e31-101">New-AzsDiskMigrationJob</span></span>

## <span data-ttu-id="71e31-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="71e31-102">SYNOPSIS</span></span>
<span data-ttu-id="71e31-103">Felügyelt áttelepítési feladatot indít át a távtárolású lemezek áttelepítéséhez a megadott célhelyre.</span><span class="sxs-lookup"><span data-stu-id="71e31-103">Starts a managed disk migration job to migrate managed disks to the specified destination share.</span></span>

## <span data-ttu-id="71e31-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="71e31-104">SYNTAX</span></span>

```
New-AzsDiskMigrationJob [-Disks] <Disk[]> [-TargetShare] <String> [[-Location] <String>] [-Name] <String>
 [<CommonParameters>]
```

## <span data-ttu-id="71e31-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="71e31-105">DESCRIPTION</span></span>
<span data-ttu-id="71e31-106">Lemezvezérlő-áttelepítési feladat létrehozása</span><span class="sxs-lookup"><span data-stu-id="71e31-106">Create a disk migration job.</span></span>

## <span data-ttu-id="71e31-107">Példák</span><span class="sxs-lookup"><span data-stu-id="71e31-107">EXAMPLES</span></span>

### <span data-ttu-id="71e31-108">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="71e31-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsDiskMigrationJob -Name "MyMigrationJob" -Disks $disks -location local -TargetShare "\\SU1FileServer.azurestack.local\SU1_ObjStore"
```

<span data-ttu-id="71e31-109">Felügyelt áttelepítési feladat indítása az első 20 lemezen</span><span class="sxs-lookup"><span data-stu-id="71e31-109">Start a managed disk migration job for the first 20 disks</span></span>

## <span data-ttu-id="71e31-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="71e31-110">PARAMETERS</span></span>

### <span data-ttu-id="71e31-111">-Lemezek</span><span class="sxs-lookup"><span data-stu-id="71e31-111">-Disks</span></span>
<span data-ttu-id="71e31-112">A lemezek listájának paraméterei.</span><span class="sxs-lookup"><span data-stu-id="71e31-112">The parameters of disk list.</span></span>

```yaml
Type: Disk[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71e31-113">-Hely</span><span class="sxs-lookup"><span data-stu-id="71e31-113">-Location</span></span>
<span data-ttu-id="71e31-114">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="71e31-114">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71e31-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="71e31-115">-Name</span></span>
<span data-ttu-id="71e31-116">Az áttelepítési feladat GUID-neve.</span><span class="sxs-lookup"><span data-stu-id="71e31-116">The migration job guid name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: MigrationId

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71e31-117">-TargetShare</span><span class="sxs-lookup"><span data-stu-id="71e31-117">-TargetShare</span></span>
<span data-ttu-id="71e31-118">A cél megosztásának neve.</span><span class="sxs-lookup"><span data-stu-id="71e31-118">The target share name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71e31-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71e31-119">CommonParameters</span></span>
<span data-ttu-id="71e31-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="71e31-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71e31-121">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71e31-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71e31-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="71e31-122">INPUTS</span></span>

## <span data-ttu-id="71e31-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="71e31-123">OUTPUTS</span></span>

### <span data-ttu-id="71e31-124">Microsoft. AzureStack. Management. kiszámítás. admin. models. DiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="71e31-124">Microsoft.AzureStack.Management.Compute.Admin.Models.DiskMigrationJob</span></span>

## <span data-ttu-id="71e31-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="71e31-125">NOTES</span></span>

## <span data-ttu-id="71e31-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="71e31-126">RELATED LINKS</span></span>

