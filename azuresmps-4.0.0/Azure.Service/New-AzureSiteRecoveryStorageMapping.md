---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 2D09422F-82B1-4243-B835-8BF223A6F936
online version: ''
schema: 2.0.0
ms.openlocfilehash: a6f02f333601172341de4fe8a0bf629037f712a5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015975"
---
# <span data-ttu-id="77ced-101">New-AzureSiteRecoveryStorageMapping</span><span class="sxs-lookup"><span data-stu-id="77ced-101">New-AzureSiteRecoveryStorageMapping</span></span>

## <span data-ttu-id="77ced-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="77ced-102">SYNOPSIS</span></span>
<span data-ttu-id="77ced-103">Az Azure Storage Object és a helyreállítási tároló objektum között megfeleltetést hoz létre.</span><span class="sxs-lookup"><span data-stu-id="77ced-103">Creates a mapping between an Azure Storage object and recovery Storage object.</span></span>

## <span data-ttu-id="77ced-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="77ced-104">SYNTAX</span></span>

```
New-AzureSiteRecoveryStorageMapping -PrimaryStorage <ASRStorage> -RecoveryStorage <ASRStorage>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="77ced-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="77ced-105">DESCRIPTION</span></span>
<span data-ttu-id="77ced-106">A **New-AzureSiteRecoveryStorageMapping** parancsmag létrehoz egy megfeleltetést az Azure webhely-helyreállítási felügyelt elsődleges Azure Storage Object és a helyreállítási tároló objektum között.</span><span class="sxs-lookup"><span data-stu-id="77ced-106">The **New-AzureSiteRecoveryStorageMapping** cmdlet creates a mapping between an Azure Site Recovery managed primary Azure Storage object and a recovery Storage object.</span></span>

## <span data-ttu-id="77ced-107">Példák</span><span class="sxs-lookup"><span data-stu-id="77ced-107">EXAMPLES</span></span>

### <span data-ttu-id="77ced-108">1. példa: megfeleltetés létrehozása tárolási objektum és helyreállítási tároló objektum között</span><span class="sxs-lookup"><span data-stu-id="77ced-108">Example 1: Create a mapping between a storage object and a recovery storage object</span></span>
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> $Storages = Get-AzureSiteRecoveryStorage -Server $Servers[0]
PS C:\> New-AzureSiteRecoveryStorageMapping -PrimaryStorage $Storages[0] -RecoveryStorage $Storages[1]
```

<span data-ttu-id="77ced-109">Az első Command parancsmag a **Get-AzureSiteRecoveryServer** parancsmaggal kapja meg az aktuális Azure-webhely helyreállítási boltozatának kiszolgálóit.</span><span class="sxs-lookup"><span data-stu-id="77ced-109">The first command cmdlet gets servers for the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryServer** cmdlet.</span></span>
<span data-ttu-id="77ced-110">A parancs a $Servers Array változóban tárolja a webhely-helyreállítási kiszolgálókat.</span><span class="sxs-lookup"><span data-stu-id="77ced-110">The command stores the Site Recovery servers in the $Servers array variable.</span></span>

<span data-ttu-id="77ced-111">A második parancs beolvassa a webhely-helyreállítási tárterületet az $Servers tömb első kiszolgálójára, majd a $Storages tárolja.</span><span class="sxs-lookup"><span data-stu-id="77ced-111">The second command gets the site recovery storage for the first server in the $Servers array, and then stores it in the $Storages.</span></span>

<span data-ttu-id="77ced-112">A végleges parancs az elsődleges hálózat és a helyreállítási hálózat között hoz létre megfeleltetést.</span><span class="sxs-lookup"><span data-stu-id="77ced-112">The final command creates a mapping between the primary network and the recovery network.</span></span>
<span data-ttu-id="77ced-113">A parancs az elsődleges tárterület-objektumot az $Storages első elemeként adja meg.</span><span class="sxs-lookup"><span data-stu-id="77ced-113">The command specifies the primary Storage object as the first element of $Storages.</span></span>
<span data-ttu-id="77ced-114">A parancs a helyreállítási tárterület objektumot a $Storages második elemeként adja meg.</span><span class="sxs-lookup"><span data-stu-id="77ced-114">The command specifies the recovery Storage object as the second element of $Storages.</span></span>

## <span data-ttu-id="77ced-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="77ced-115">PARAMETERS</span></span>

### <span data-ttu-id="77ced-116">-PrimaryStorage</span><span class="sxs-lookup"><span data-stu-id="77ced-116">-PrimaryStorage</span></span>
<span data-ttu-id="77ced-117">A helyreállítási tárterülethez rendelhető elsődleges tárterületet adja meg.</span><span class="sxs-lookup"><span data-stu-id="77ced-117">Specifies the primary Storage to map to the recovery Storage.</span></span>
<span data-ttu-id="77ced-118">**ASRStorage** objektum beolvasásához használja az Get-AzureSiteRecoveryStorage parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="77ced-118">To obtain an **ASRStorage** object, use the Get-AzureSiteRecoveryStorage cmdlet.</span></span>

```yaml
Type: ASRStorage
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77ced-119">-Profil</span><span class="sxs-lookup"><span data-stu-id="77ced-119">-Profile</span></span>
<span data-ttu-id="77ced-120">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="77ced-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="77ced-121">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="77ced-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77ced-122">-RecoveryStorage</span><span class="sxs-lookup"><span data-stu-id="77ced-122">-RecoveryStorage</span></span>
<span data-ttu-id="77ced-123">A helyreállítási tárterület objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="77ced-123">Specifies the recovery Storage object.</span></span>
<span data-ttu-id="77ced-124">Ez a parancsmag az elsődleges tárterületet az a tárterület-objektumhoz rendeli, amelyet a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="77ced-124">This cmdlet maps the primary Storage object to the Storage object that this parameter specifies.</span></span>
<span data-ttu-id="77ced-125">**ASRStorage** -objektum beszerzéséhez használja a **Get-AzureSiteRecoveryStorage**.</span><span class="sxs-lookup"><span data-stu-id="77ced-125">To obtain an **ASRStorage** object, use **Get-AzureSiteRecoveryStorage**.</span></span>

```yaml
Type: ASRStorage
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77ced-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77ced-126">CommonParameters</span></span>
<span data-ttu-id="77ced-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="77ced-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77ced-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77ced-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77ced-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="77ced-129">INPUTS</span></span>

## <span data-ttu-id="77ced-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="77ced-130">OUTPUTS</span></span>

## <span data-ttu-id="77ced-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="77ced-131">NOTES</span></span>

## <span data-ttu-id="77ced-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="77ced-132">RELATED LINKS</span></span>

[<span data-ttu-id="77ced-133">Get-AzureSiteRecoveryStorage</span><span class="sxs-lookup"><span data-stu-id="77ced-133">Get-AzureSiteRecoveryStorage</span></span>](./Get-AzureSiteRecoveryStorage.md)

[<span data-ttu-id="77ced-134">Get-AzureSiteRecoveryStorageMapping</span><span class="sxs-lookup"><span data-stu-id="77ced-134">Get-AzureSiteRecoveryStorageMapping</span></span>](./Get-AzureSiteRecoveryStorageMapping.md)

[<span data-ttu-id="77ced-135">Remove-AzureSiteRecoveryStorageMapping</span><span class="sxs-lookup"><span data-stu-id="77ced-135">Remove-AzureSiteRecoveryStorageMapping</span></span>](./Remove-AzureSiteRecoveryStorageMapping.md)


