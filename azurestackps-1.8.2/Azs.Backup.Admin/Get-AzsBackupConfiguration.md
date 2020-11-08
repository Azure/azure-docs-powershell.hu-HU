---
external help file: Azs.Backup.Admin-help.xml
Module Name: Azs.Backup.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 25091f0cb439e0447d19b534d59a0084a5b05c6e
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94016641"
---
# <span data-ttu-id="10354-101">Get-AzsBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="10354-101">Get-AzsBackupConfiguration</span></span>

## <span data-ttu-id="10354-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="10354-102">SYNOPSIS</span></span>
<span data-ttu-id="10354-103">A biztonságimásolat-konfigurációk listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="10354-103">Returns the list of backup configurations.</span></span>

## <span data-ttu-id="10354-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="10354-104">SYNTAX</span></span>

### <span data-ttu-id="10354-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="10354-105">List (Default)</span></span>
```
Get-AzsBackupConfiguration [-ResourceGroupName <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="10354-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="10354-106">Get</span></span>
```
Get-AzsBackupConfiguration [[-Location] <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="10354-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="10354-107">ResourceId</span></span>
```
Get-AzsBackupConfiguration -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="10354-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="10354-108">DESCRIPTION</span></span>
<span data-ttu-id="10354-109">A biztonságimásolat-konfigurációk listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="10354-109">Returns the list of backup configurations.</span></span>

## <span data-ttu-id="10354-110">Példák</span><span class="sxs-lookup"><span data-stu-id="10354-110">EXAMPLES</span></span>

### <span data-ttu-id="10354-111">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="10354-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsBackupConfiguration
```

<span data-ttu-id="10354-112">Azure-halom biztonsági mentése konfigurációjának beszerzése</span><span class="sxs-lookup"><span data-stu-id="10354-112">Get Azure Stack backup configuration.</span></span>

## <span data-ttu-id="10354-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="10354-113">PARAMETERS</span></span>

### <span data-ttu-id="10354-114">-Hely</span><span class="sxs-lookup"><span data-stu-id="10354-114">-Location</span></span>
<span data-ttu-id="10354-115">Biztonsági mentési hely</span><span class="sxs-lookup"><span data-stu-id="10354-115">Backup location.</span></span>

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

### <span data-ttu-id="10354-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10354-116">-ResourceGroupName</span></span>
<span data-ttu-id="10354-117">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="10354-117">Name of the resource group.</span></span>

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

### <span data-ttu-id="10354-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="10354-118">-ResourceId</span></span>
<span data-ttu-id="10354-119">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="10354-119">The resource id.</span></span>

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

### <span data-ttu-id="10354-120">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="10354-120">-Skip</span></span>
<span data-ttu-id="10354-121">Az első N elem kihagyása a paraméterben megadott értékkel.</span><span class="sxs-lookup"><span data-stu-id="10354-121">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="10354-122">-Top</span><span class="sxs-lookup"><span data-stu-id="10354-122">-Top</span></span>
<span data-ttu-id="10354-123">A paraméterben megadott módon adja vissza a legfelső N-elemeket.</span><span class="sxs-lookup"><span data-stu-id="10354-123">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="10354-124">A-kihagyás paraméter után érvényes.</span><span class="sxs-lookup"><span data-stu-id="10354-124">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="10354-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10354-125">CommonParameters</span></span>
<span data-ttu-id="10354-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="10354-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10354-127">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10354-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10354-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="10354-128">INPUTS</span></span>

## <span data-ttu-id="10354-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="10354-129">OUTPUTS</span></span>

### <span data-ttu-id="10354-130">Microsoft. AzureStack. Management. backup. admin. models. BackupLocation</span><span class="sxs-lookup"><span data-stu-id="10354-130">Microsoft.AzureStack.Management.Backup.Admin.Models.BackupLocation</span></span>

## <span data-ttu-id="10354-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="10354-131">NOTES</span></span>

## <span data-ttu-id="10354-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="10354-132">RELATED LINKS</span></span>

