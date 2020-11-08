---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: BB36A434-6BE3-46BF-B10A-FCD6C766CB84
online version: ''
schema: 2.0.0
ms.openlocfilehash: 87414a56778123053615bb36a06113e2b0b0633f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016110"
---
# <span data-ttu-id="f00bb-101">Remove-AzureSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="f00bb-101">Remove-AzureSiteRecoveryNetworkMapping</span></span>

## <span data-ttu-id="f00bb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f00bb-102">SYNOPSIS</span></span>
<span data-ttu-id="f00bb-103">Eltávolít egy hálózati megfeleltetést egy webhely-helyreállítási boltozatból.</span><span class="sxs-lookup"><span data-stu-id="f00bb-103">Removes a network mapping from a Site Recovery vault.</span></span>

## <span data-ttu-id="f00bb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f00bb-104">SYNTAX</span></span>

```
Remove-AzureSiteRecoveryNetworkMapping -NetworkMapping <ASRNetworkMapping> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="f00bb-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f00bb-105">DESCRIPTION</span></span>
<span data-ttu-id="f00bb-106">A **Remove-AzureSiteRecoveryNetworkMapping** parancsmag eltávolít egy hálózati megfeleltetést az aktuális Azure webhely-helyreállítási boltozatból.</span><span class="sxs-lookup"><span data-stu-id="f00bb-106">The **Remove-AzureSiteRecoveryNetworkMapping** cmdlet removes a network mapping from the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="f00bb-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f00bb-107">EXAMPLES</span></span>

### <span data-ttu-id="f00bb-108">1. példa: a hálózat és a helyreállítási hálózat közötti megfeleltetés eltávolítása</span><span class="sxs-lookup"><span data-stu-id="f00bb-108">Example 1: Remove the mapping between a network and a recovery network</span></span>
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> $NetworkMapping = Get-AzureSiteRecoveryNetworkMapping -PrimaryServer $Servers[0] -RecoveryServer $Servers[0]
PS C:\> Remove-AzureSiteRecoveryNetworkMapping -NetworkMapping $NetworkMapping
```

<span data-ttu-id="f00bb-109">Az első Command parancsmag a **Get-AzureSiteRecoveryServer** parancsmaggal kapja meg az aktuális Azure-webhely helyreállítási boltozatának kiszolgálóit.</span><span class="sxs-lookup"><span data-stu-id="f00bb-109">The first command cmdlet gets servers for the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryServer** cmdlet.</span></span>
<span data-ttu-id="f00bb-110">A parancs a $Servers Array változóban tárolja a webhely-helyreállítási kiszolgálókat.</span><span class="sxs-lookup"><span data-stu-id="f00bb-110">The command stores the Site Recovery servers in the $Servers array variable.</span></span>

<span data-ttu-id="f00bb-111">A második parancs az elsődleges hálózat és a helyreállítási hálózat közötti megfeleltetést kapja, majd a $NetworkMapping változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="f00bb-111">The second command gets the mapping between the primary network and the recovery network, and then stores it in the $NetworkMapping variable.</span></span>
<span data-ttu-id="f00bb-112">A parancs a hálózati megfeleltetés elsődleges kiszolgálóját adja meg az $Servers első elemeként.</span><span class="sxs-lookup"><span data-stu-id="f00bb-112">The command specifies the primary server for the network mapping as the first element of $Servers.</span></span>
<span data-ttu-id="f00bb-113">A parancs a helyreállítási hálózatnak azt a kiszolgálóját adja meg, amely a $Servers második eleme.</span><span class="sxs-lookup"><span data-stu-id="f00bb-113">The command specifies the server for the recovery network as the second element of $Servers.</span></span>

<span data-ttu-id="f00bb-114">A végleges parancs eltávolítja a hálózati megfeleltetést a $NetworkMappingban.</span><span class="sxs-lookup"><span data-stu-id="f00bb-114">The final command removes the network mapping in $NetworkMapping.</span></span>

### <span data-ttu-id="f00bb-115">2. példa: a megfeleltetés eltávolítása a hálózat és az Azure Virtual Machine-hálózat között</span><span class="sxs-lookup"><span data-stu-id="f00bb-115">Example 2: Remove the mapping between a network and an Azure virtual machine network</span></span>
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> $NetworkMapping = Get-AzureSiteRecoveryNetworkMapping -PrimaryServer $Servers[0] -Azure
PS C:\> Remove-AzureSiteRecoveryNetworkMapping -NetworkMapping $NetworkMapping
```

<span data-ttu-id="f00bb-116">Az első Command parancsmag az aktuális webhely-helyreállítási boltozat kiszolgálóira kerül.</span><span class="sxs-lookup"><span data-stu-id="f00bb-116">The first command cmdlet gets servers for the current Site Recovery vault.</span></span>
<span data-ttu-id="f00bb-117">A parancs a $Servers Array változóban tárolja a webhely-helyreállítási kiszolgálókat.</span><span class="sxs-lookup"><span data-stu-id="f00bb-117">The command stores the Site Recovery servers in the $Servers array variable.</span></span>

<span data-ttu-id="f00bb-118">A második parancs az elsődleges hálózat és egy Azure Virtual Machine-hálózat közötti megfeleltetést kapja, majd a $NetworkMapping változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="f00bb-118">The second command gets a mapping between the primary network and an Azure virtual machine network, and then stores it in the $NetworkMapping variable.</span></span>
<span data-ttu-id="f00bb-119">A parancs a hálózat elsődleges kiszolgálóját adja meg az $Servers első elemeként.</span><span class="sxs-lookup"><span data-stu-id="f00bb-119">The command specifies the primary server for the network as the first element of $Servers.</span></span>
<span data-ttu-id="f00bb-120">A parancs az *Azure* paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="f00bb-120">The command specifies the *Azure* parameter.</span></span>
<span data-ttu-id="f00bb-121">Ezért a parancs az Azure Virtual Machine-hálózathoz való megfeleltetést kapja.</span><span class="sxs-lookup"><span data-stu-id="f00bb-121">Therefore, the command gets the mapping to an Azure virtual machine network.</span></span>

<span data-ttu-id="f00bb-122">A végleges parancs eltávolítja a hálózati megfeleltetést a $NetworkMappingban.</span><span class="sxs-lookup"><span data-stu-id="f00bb-122">The final command removes the network mapping in $NetworkMapping.</span></span>

## <span data-ttu-id="f00bb-123">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f00bb-123">PARAMETERS</span></span>

### <span data-ttu-id="f00bb-124">-NetworkMapping</span><span class="sxs-lookup"><span data-stu-id="f00bb-124">-NetworkMapping</span></span>
<span data-ttu-id="f00bb-125">Az eltávolítandó hálózati megfeleltetést adja meg.</span><span class="sxs-lookup"><span data-stu-id="f00bb-125">Specifies the network mapping to remove.</span></span>

```yaml
Type: ASRNetworkMapping
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f00bb-126">-Profil</span><span class="sxs-lookup"><span data-stu-id="f00bb-126">-Profile</span></span>
<span data-ttu-id="f00bb-127">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="f00bb-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f00bb-128">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="f00bb-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f00bb-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f00bb-129">CommonParameters</span></span>
<span data-ttu-id="f00bb-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f00bb-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f00bb-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f00bb-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f00bb-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f00bb-132">INPUTS</span></span>

## <span data-ttu-id="f00bb-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f00bb-133">OUTPUTS</span></span>

## <span data-ttu-id="f00bb-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f00bb-134">NOTES</span></span>

## <span data-ttu-id="f00bb-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f00bb-135">RELATED LINKS</span></span>

[<span data-ttu-id="f00bb-136">Get-AzureSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="f00bb-136">Get-AzureSiteRecoveryNetworkMapping</span></span>](./Get-AzureSiteRecoveryNetworkMapping.md)

[<span data-ttu-id="f00bb-137">Új – AzureSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="f00bb-137">New-AzureSiteRecoveryNetworkMapping</span></span>](./New-AzureSiteRecoveryNetworkMapping.md)

[<span data-ttu-id="f00bb-138">Get-AzureSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="f00bb-138">Get-AzureSiteRecoveryServer</span></span>](./Get-AzureSiteRecoveryServer.md)


