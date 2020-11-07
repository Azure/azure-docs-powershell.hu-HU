---
external help file: Azs.Backup.Admin-help.xml
Module Name: Azs.Backup.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1f3a965d287aa266683636b4b17a8d8954cace8f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839911"
---
# <span data-ttu-id="2ef90-101">Get-AzsBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="2ef90-101">Get-AzsBackupConfiguration</span></span>

## <span data-ttu-id="2ef90-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2ef90-102">SYNOPSIS</span></span>
<span data-ttu-id="2ef90-103">A biztonságimásolat-konfigurációk listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="2ef90-103">Returns the list of backup configurations.</span></span>

## <span data-ttu-id="2ef90-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2ef90-104">SYNTAX</span></span>

### <span data-ttu-id="2ef90-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2ef90-105">List (Default)</span></span>
```
Get-AzsBackupConfiguration [-ResourceGroupName <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="2ef90-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="2ef90-106">Get</span></span>
```
Get-AzsBackupConfiguration [[-Location] <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="2ef90-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="2ef90-107">ResourceId</span></span>
```
Get-AzsBackupConfiguration -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="2ef90-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="2ef90-108">DESCRIPTION</span></span>
<span data-ttu-id="2ef90-109">A biztonságimásolat-konfigurációk listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="2ef90-109">Returns the list of backup configurations.</span></span>

## <span data-ttu-id="2ef90-110">Példák</span><span class="sxs-lookup"><span data-stu-id="2ef90-110">EXAMPLES</span></span>

### <span data-ttu-id="2ef90-111">PÉLDA 1</span><span class="sxs-lookup"><span data-stu-id="2ef90-111">EXAMPLE 1</span></span>
```
Get-AzsBackupConfiguration
```

<span data-ttu-id="2ef90-112">Azure-halom biztonsági mentése konfigurációjának beszerzése</span><span class="sxs-lookup"><span data-stu-id="2ef90-112">Get Azure Stack backup configuration.</span></span>

## <span data-ttu-id="2ef90-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2ef90-113">PARAMETERS</span></span>

### <span data-ttu-id="2ef90-114">-Hely</span><span class="sxs-lookup"><span data-stu-id="2ef90-114">-Location</span></span>
<span data-ttu-id="2ef90-115">Biztonsági mentési hely</span><span class="sxs-lookup"><span data-stu-id="2ef90-115">Backup location.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ef90-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ef90-116">-ResourceGroupName</span></span>
<span data-ttu-id="2ef90-117">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="2ef90-117">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: List, Get
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ef90-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2ef90-118">-ResourceId</span></span>
<span data-ttu-id="2ef90-119">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="2ef90-119">The resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ef90-120">-Top</span><span class="sxs-lookup"><span data-stu-id="2ef90-120">-Top</span></span>
<span data-ttu-id="2ef90-121">A paraméterben megadott módon adja vissza a legfelső N-elemeket.</span><span class="sxs-lookup"><span data-stu-id="2ef90-121">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="2ef90-122">A-kihagyás paraméter után érvényes.</span><span class="sxs-lookup"><span data-stu-id="2ef90-122">Applies after the -Skip parameter.</span></span>

```yaml
Type: System.Int32
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ef90-123">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="2ef90-123">-Skip</span></span>
<span data-ttu-id="2ef90-124">Az első N elem kihagyása a paraméterben megadott értékkel.</span><span class="sxs-lookup"><span data-stu-id="2ef90-124">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: System.Int32
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ef90-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ef90-125">CommonParameters</span></span>
<span data-ttu-id="2ef90-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2ef90-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ef90-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ef90-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ef90-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2ef90-128">INPUTS</span></span>

## <span data-ttu-id="2ef90-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2ef90-129">OUTPUTS</span></span>

### <span data-ttu-id="2ef90-130">Microsoft. AzureStack. Management. backup. admin. models. BackupLocation</span><span class="sxs-lookup"><span data-stu-id="2ef90-130">Microsoft.AzureStack.Management.Backup.Admin.Models.BackupLocation</span></span>

## <span data-ttu-id="2ef90-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2ef90-131">NOTES</span></span>

## <span data-ttu-id="2ef90-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2ef90-132">RELATED LINKS</span></span>
