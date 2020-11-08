---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 4F083EBC-7D7E-4836-8AAB-6BF2B08162DF
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6a69d54b315319e3dacc150edc2a8737be9b96e3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015575"
---
# <span data-ttu-id="8da16-101">Get-AzureSiteRecoveryStorageMapping</span><span class="sxs-lookup"><span data-stu-id="8da16-101">Get-AzureSiteRecoveryStorageMapping</span></span>

## <span data-ttu-id="8da16-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8da16-102">SYNOPSIS</span></span>
<span data-ttu-id="8da16-103">Beilleszti a hely helyreállítási tároló objektumait a boltozathoz.</span><span class="sxs-lookup"><span data-stu-id="8da16-103">Gets mappings of Site Recovery Storage objects for a vault.</span></span>

## <span data-ttu-id="8da16-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8da16-104">SYNTAX</span></span>

```
Get-AzureSiteRecoveryStorageMapping -PrimaryServer <ASRServer> -RecoveryServer <ASRServer>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="8da16-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8da16-105">DESCRIPTION</span></span>
<span data-ttu-id="8da16-106">A **Get-AzureSiteRecoveryStorageMapping** parancsmag az Azure webhely-helyreállítási tároló objektumait az aktuális Azure webhely-helyreállítási boltozathoz rendeli.</span><span class="sxs-lookup"><span data-stu-id="8da16-106">The **Get-AzureSiteRecoveryStorageMapping** cmdlet gets mappings of Azure Site Recovery Storage objects for the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="8da16-107">Példák</span><span class="sxs-lookup"><span data-stu-id="8da16-107">EXAMPLES</span></span>

### <span data-ttu-id="8da16-108">Példa 1: a tárterület és a helyreállítási tároló objektum közötti megfeleltetés beszerzése</span><span class="sxs-lookup"><span data-stu-id="8da16-108">Example 1: Get the mapping between a Storage object and a recovery Storage object</span></span>
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> Get-AzureSiteRecoveryStorageMapping -PrimaryServer $Servers[0] -RecoveryServer $Servers[1]
PrimaryServerId     : 774859b0-1966-48cc-9df7-759c441b7a8c
PrimaryStorageId    : 1c1d0c0b-0c50-4675-af1a-1fdac70dbb6d
PrimaryStorageName  : phase2PrimaryStorageClassification
RecoveryServerId    : 774859b0-1966-48cc-9df7-759c441b7a8c
RecoveryStorageId   : 20cf8d92-fd5d-4872-985a-0f4562b8a0bf
RecoveryStorageName : phase2RecoveryStorageClassification
```

<span data-ttu-id="8da16-109">Az első Command parancsmag a **Get-AzureSiteRecoveryServer** parancsmaggal kapja meg az aktuális Azure-webhely helyreállítási boltozatának kiszolgálóit.</span><span class="sxs-lookup"><span data-stu-id="8da16-109">The first command cmdlet gets servers for the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryServer** cmdlet.</span></span>
<span data-ttu-id="8da16-110">A parancs a $Servers Array változóban tárolja a webhely-helyreállítási kiszolgálókat.</span><span class="sxs-lookup"><span data-stu-id="8da16-110">The command stores the Site Recovery servers in the $Servers array variable.</span></span>

<span data-ttu-id="8da16-111">A második parancs a két Azure-tárterület közötti megfeleltetést kapja.</span><span class="sxs-lookup"><span data-stu-id="8da16-111">The second command gets the mapping between two Azure Storage objects.</span></span>
<span data-ttu-id="8da16-112">A parancs a tároló objektum elsődleges kiszolgálóját adja meg $Servers első elemeként.</span><span class="sxs-lookup"><span data-stu-id="8da16-112">The command specifies the primary server for the Storage object mapping as the first element of $Servers.</span></span>
<span data-ttu-id="8da16-113">A parancs a helyreállítási tárterület-objektum kiszolgálóját adja meg a $Servers második elemeként.</span><span class="sxs-lookup"><span data-stu-id="8da16-113">The command specifies the server for the recovery Storage object as the second element of $Servers.</span></span>

## <span data-ttu-id="8da16-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8da16-114">PARAMETERS</span></span>

### <span data-ttu-id="8da16-115">-PrimaryServer</span><span class="sxs-lookup"><span data-stu-id="8da16-115">-PrimaryServer</span></span>
<span data-ttu-id="8da16-116">Az elsődleges kiszolgálót adja meg.</span><span class="sxs-lookup"><span data-stu-id="8da16-116">Specifies the primary server.</span></span>
<span data-ttu-id="8da16-117">Ha kiszolgálót szeretne beolvasni, használja a **Get-AzureSiteRecoveryServer** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="8da16-117">To obtain a server, use the **Get-AzureSiteRecoveryServer** cmdlet.</span></span>

```yaml
Type: ASRServer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8da16-118">-Profil</span><span class="sxs-lookup"><span data-stu-id="8da16-118">-Profile</span></span>
<span data-ttu-id="8da16-119">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="8da16-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8da16-120">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="8da16-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8da16-121">-RecoveryServer</span><span class="sxs-lookup"><span data-stu-id="8da16-121">-RecoveryServer</span></span>
<span data-ttu-id="8da16-122">A helyreállítási kiszolgálót adja meg.</span><span class="sxs-lookup"><span data-stu-id="8da16-122">Specifies the recovery server.</span></span>
<span data-ttu-id="8da16-123">A kiszolgáló beszerzéséhez használja a **Get-AzureSiteRecoveryServer**.</span><span class="sxs-lookup"><span data-stu-id="8da16-123">To obtain a server, use **Get-AzureSiteRecoveryServer**.</span></span>

```yaml
Type: ASRServer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8da16-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8da16-124">CommonParameters</span></span>
<span data-ttu-id="8da16-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8da16-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8da16-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8da16-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8da16-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8da16-127">INPUTS</span></span>

## <span data-ttu-id="8da16-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8da16-128">OUTPUTS</span></span>

## <span data-ttu-id="8da16-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8da16-129">NOTES</span></span>

## <span data-ttu-id="8da16-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8da16-130">RELATED LINKS</span></span>

[<span data-ttu-id="8da16-131">Get-AzureSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="8da16-131">Get-AzureSiteRecoveryServer</span></span>](./Get-AzureSiteRecoveryServer.md)

[<span data-ttu-id="8da16-132">Új – AzureSiteRecoveryStorageMapping</span><span class="sxs-lookup"><span data-stu-id="8da16-132">New-AzureSiteRecoveryStorageMapping</span></span>](./New-AzureSiteRecoveryStorageMapping.md)

[<span data-ttu-id="8da16-133">Remove-AzureSiteRecoveryStorageMapping</span><span class="sxs-lookup"><span data-stu-id="8da16-133">Remove-AzureSiteRecoveryStorageMapping</span></span>](./Remove-AzureSiteRecoveryStorageMapping.md)


