---
external help file: Azs.Backup.Admin-help.xml
Module Name: Azs.Backup.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 500a8e28ceb4eb452d788574b8a80865b5e54b14
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491686"
---
# <span data-ttu-id="e3fd3-101">Get-AzsBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="e3fd3-101">Get-AzsBackupConfiguration</span></span>

## <span data-ttu-id="e3fd3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e3fd3-102">SYNOPSIS</span></span>
<span data-ttu-id="e3fd3-103">A biztonságimásolat-konfigurációk listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="e3fd3-103">Returns the list of backup configurations.</span></span>

## <span data-ttu-id="e3fd3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e3fd3-104">SYNTAX</span></span>

### <span data-ttu-id="e3fd3-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e3fd3-105">List (Default)</span></span>
```
Get-AzsBackupConfiguration [-ResourceGroupName <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="e3fd3-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="e3fd3-106">Get</span></span>
```
Get-AzsBackupConfiguration [[-Location] <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="e3fd3-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="e3fd3-107">ResourceId</span></span>
```
Get-AzsBackupConfiguration -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="e3fd3-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="e3fd3-108">DESCRIPTION</span></span>
<span data-ttu-id="e3fd3-109">A biztonságimásolat-konfigurációk listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="e3fd3-109">Returns the list of backup configurations.</span></span>

## <span data-ttu-id="e3fd3-110">Példák</span><span class="sxs-lookup"><span data-stu-id="e3fd3-110">EXAMPLES</span></span>

### <span data-ttu-id="e3fd3-111">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="e3fd3-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsBackupConfiguration
```

<span data-ttu-id="e3fd3-112">Azure-halom biztonsági mentése konfigurációjának beszerzése</span><span class="sxs-lookup"><span data-stu-id="e3fd3-112">Get Azure Stack backup configuration.</span></span>

## <span data-ttu-id="e3fd3-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e3fd3-113">PARAMETERS</span></span>

### <span data-ttu-id="e3fd3-114">-Hely</span><span class="sxs-lookup"><span data-stu-id="e3fd3-114">-Location</span></span>
<span data-ttu-id="e3fd3-115">Biztonsági mentési hely</span><span class="sxs-lookup"><span data-stu-id="e3fd3-115">Backup location.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3fd3-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3fd3-116">-ResourceGroupName</span></span>
<span data-ttu-id="e3fd3-117">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e3fd3-117">Name of the resource group.</span></span>

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

### <span data-ttu-id="e3fd3-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e3fd3-118">-ResourceId</span></span>
<span data-ttu-id="e3fd3-119">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="e3fd3-119">The resource id.</span></span>

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

### <span data-ttu-id="e3fd3-120">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="e3fd3-120">-Skip</span></span>
<span data-ttu-id="e3fd3-121">Az első N elem kihagyása a paraméterben megadott értékkel.</span><span class="sxs-lookup"><span data-stu-id="e3fd3-121">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3fd3-122">-Top</span><span class="sxs-lookup"><span data-stu-id="e3fd3-122">-Top</span></span>
<span data-ttu-id="e3fd3-123">A paraméterben megadott módon adja vissza a legfelső N-elemeket.</span><span class="sxs-lookup"><span data-stu-id="e3fd3-123">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="e3fd3-124">A-kihagyás paraméter után érvényes.</span><span class="sxs-lookup"><span data-stu-id="e3fd3-124">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3fd3-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3fd3-125">CommonParameters</span></span>
<span data-ttu-id="e3fd3-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e3fd3-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3fd3-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3fd3-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3fd3-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e3fd3-128">INPUTS</span></span>

## <span data-ttu-id="e3fd3-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e3fd3-129">OUTPUTS</span></span>

### <span data-ttu-id="e3fd3-130">Microsoft. AzureStack. Management. backup. admin. models. BackupLocation</span><span class="sxs-lookup"><span data-stu-id="e3fd3-130">Microsoft.AzureStack.Management.Backup.Admin.Models.BackupLocation</span></span>

## <span data-ttu-id="e3fd3-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e3fd3-131">NOTES</span></span>

## <span data-ttu-id="e3fd3-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e3fd3-132">RELATED LINKS</span></span>

