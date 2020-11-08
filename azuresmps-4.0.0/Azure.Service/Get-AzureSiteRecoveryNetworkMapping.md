---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: F6C01C25-655C-4798-9826-F7CB168181C7
online version: ''
schema: 2.0.0
ms.openlocfilehash: bc8b7dc7e23a98111e75c2b2c9c079f010e3c5dc
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015590"
---
# <span data-ttu-id="dd82d-101">Get-AzureSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="dd82d-101">Get-AzureSiteRecoveryNetworkMapping</span></span>

## <span data-ttu-id="dd82d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="dd82d-102">SYNOPSIS</span></span>
<span data-ttu-id="dd82d-103">A webhely-helyreállítási boltozat hálózati megfeleltetéseit kapja.</span><span class="sxs-lookup"><span data-stu-id="dd82d-103">Gets network mappings for a Site Recovery vault.</span></span>

## <span data-ttu-id="dd82d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="dd82d-104">SYNTAX</span></span>

### <span data-ttu-id="dd82d-105">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="dd82d-105">EnterpriseToEnterprise</span></span>
```
Get-AzureSiteRecoveryNetworkMapping -PrimaryServer <ASRServer> -RecoveryServer <ASRServer>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="dd82d-106">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="dd82d-106">EnterpriseToAzure</span></span>
```
Get-AzureSiteRecoveryNetworkMapping -PrimaryServer <ASRServer> [-Azure] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="dd82d-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="dd82d-107">DESCRIPTION</span></span>
<span data-ttu-id="dd82d-108">A **Get-AzureSiteRecoveryNetworkMapping** parancsmag információkat kap az Azure webhely-helyreállítási hálózati megfeleltetésekről az aktuális webhely-helyreállítási boltozathoz.</span><span class="sxs-lookup"><span data-stu-id="dd82d-108">The **Get-AzureSiteRecoveryNetworkMapping** cmdlet gets information about Azure Site Recovery network mappings for the current Site Recovery vault.</span></span>

## <span data-ttu-id="dd82d-109">Példák</span><span class="sxs-lookup"><span data-stu-id="dd82d-109">EXAMPLES</span></span>

### <span data-ttu-id="dd82d-110">Példa 1: a hálózat és a helyreállítási hálózat közötti megfeleltetés beszerzése</span><span class="sxs-lookup"><span data-stu-id="dd82d-110">Example 1: Get the mapping between a network and a recovery network</span></span>
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> Get-AzureSiteRecoveryNetworkMapping -PrimaryServer $Servers[0] -RecoveryServer $Servers[0]
PrimaryServerId     : 774859b0-1966-48cc-9df7-759c441b7a8c
PrimaryNetworkId    : 7cfd636e-5cc2-4e01-873b-8a7aa4962341
PrimaryNetworkName  : phase2RecoveryVMNetwork
RecoveryServerId    : 774859b0-1966-48cc-9df7-759c441b7a8c
RecoveryNetworkId   : d903e2c6-3141-4cef-bfe1-04616cd43cbb
RecoveryNetworkName : phase2PrimaryVMNetwork
PairingStatus       : OK
```

<span data-ttu-id="dd82d-111">Az első Command parancsmag a **Get-AzureSiteRecoveryServer** parancsmaggal kapja meg az aktuális Azure-webhely helyreállítási boltozatának kiszolgálóit.</span><span class="sxs-lookup"><span data-stu-id="dd82d-111">The first command cmdlet gets servers for the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryServer** cmdlet.</span></span>
<span data-ttu-id="dd82d-112">A parancs a $Servers Array változóban tárolja a webhely-helyreállítási kiszolgálókat.</span><span class="sxs-lookup"><span data-stu-id="dd82d-112">The command stores the Site Recovery servers in the $Servers array variable.</span></span>

<span data-ttu-id="dd82d-113">A második parancs az elsődleges hálózat és a helyreállítási hálózat közötti megfeleltetést kapja.</span><span class="sxs-lookup"><span data-stu-id="dd82d-113">The second command gets the mapping between the primary network and the recovery network.</span></span>
<span data-ttu-id="dd82d-114">A parancs a hálózati megfeleltetés elsődleges kiszolgálóját adja meg az $Servers első elemeként.</span><span class="sxs-lookup"><span data-stu-id="dd82d-114">The command specifies the primary server for the network mapping as the first element of $Servers.</span></span>
<span data-ttu-id="dd82d-115">A parancs a helyreállítási hálózatnak azt a kiszolgálóját adja meg, amely a $Servers második eleme.</span><span class="sxs-lookup"><span data-stu-id="dd82d-115">The command specifies the server for the recovery network as the second element of $Servers.</span></span>

### <span data-ttu-id="dd82d-116">2. példa: a megfeleltetés beszerzése a hálózat és az Azure virtuális gép hálózata között</span><span class="sxs-lookup"><span data-stu-id="dd82d-116">Example 2: Get the mapping between a network and an Azure virtual machine network</span></span>
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> Get-AzureSiteRecoveryNetworkMapping -Azure -PrimaryServer $Servers[0] 
PrimaryServerId     : 774859b0-1966-48cc-9df7-759c441b7a8c
PrimaryNetworkId    : 7cfd636e-5cc2-4e01-873b-8a7aa4962341
PrimaryNetworkName  : phase2RecoveryVMNetwork
RecoveryServerId    : 21a9403c-6ec1-44f2-b744-b4e50b792387
RecoveryNetworkId   : ecb3a462-664f-4f57-873e-d09b5925e1a1
RecoveryNetworkName : AzureVMNetwork
PairingStatus       : OK
```

<span data-ttu-id="dd82d-117">Az első Command parancsmag az aktuális webhely-helyreállítási boltozat kiszolgálóira kerül.</span><span class="sxs-lookup"><span data-stu-id="dd82d-117">The first command cmdlet gets servers for the current Site Recovery vault.</span></span>
<span data-ttu-id="dd82d-118">A parancs a $Servers Array változóban tárolja a kiszolgálókat.</span><span class="sxs-lookup"><span data-stu-id="dd82d-118">The command stores the servers in the $Servers array variable.</span></span>

<span data-ttu-id="dd82d-119">A második parancs az elsődleges hálózat és az Azure Virtual Machine-hálózat közötti megfeleltetést kapja.</span><span class="sxs-lookup"><span data-stu-id="dd82d-119">The second command gets a mapping between the primary network and an Azure virtual machine network.</span></span>
<span data-ttu-id="dd82d-120">A parancs a hálózat elsődleges kiszolgálóját adja meg az $Servers első elemeként.</span><span class="sxs-lookup"><span data-stu-id="dd82d-120">The command specifies the primary server for the network as the first element of $Servers.</span></span>
<span data-ttu-id="dd82d-121">A parancs az *Azure* paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="dd82d-121">The command specifies the *Azure* parameter.</span></span>
<span data-ttu-id="dd82d-122">Ezért a parancs az Azure Virtual Machine-hálózathoz való megfeleltetést kapja.</span><span class="sxs-lookup"><span data-stu-id="dd82d-122">Therefore, the command gets the mapping to an Azure virtual machine network.</span></span>

## <span data-ttu-id="dd82d-123">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="dd82d-123">PARAMETERS</span></span>

### <span data-ttu-id="dd82d-124">-Azure</span><span class="sxs-lookup"><span data-stu-id="dd82d-124">-Azure</span></span>
<span data-ttu-id="dd82d-125">Azt jelzi, hogy ez a parancsmag hálózati megfeleltetéseket kap az elsődleges kiszolgálón az Azure virtuális hálózatokhoz rendelt hálózatokhoz.</span><span class="sxs-lookup"><span data-stu-id="dd82d-125">Indicates that this cmdlet gets network mappings for networks on the primary server mapped to Azure virtual networks.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd82d-126">-PrimaryServer</span><span class="sxs-lookup"><span data-stu-id="dd82d-126">-PrimaryServer</span></span>
<span data-ttu-id="dd82d-127">Itt adhatja meg azt az elsődleges kiszolgálót, amelyhez megfeleltetéseket szeretne kapni.</span><span class="sxs-lookup"><span data-stu-id="dd82d-127">Specifies a primary server for which to get mappings.</span></span>

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

### <span data-ttu-id="dd82d-128">-Profil</span><span class="sxs-lookup"><span data-stu-id="dd82d-128">-Profile</span></span>
<span data-ttu-id="dd82d-129">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="dd82d-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="dd82d-130">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="dd82d-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="dd82d-131">-RecoveryServer</span><span class="sxs-lookup"><span data-stu-id="dd82d-131">-RecoveryServer</span></span>
<span data-ttu-id="dd82d-132">Azt a helyreállítási kiszolgálót adja meg, amelyhez megfeleltetéseket szeretne kapni.</span><span class="sxs-lookup"><span data-stu-id="dd82d-132">Specifies a recovery server for which to get mappings.</span></span>

```yaml
Type: ASRServer
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd82d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd82d-133">CommonParameters</span></span>
<span data-ttu-id="dd82d-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="dd82d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd82d-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd82d-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd82d-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="dd82d-136">INPUTS</span></span>

## <span data-ttu-id="dd82d-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dd82d-137">OUTPUTS</span></span>

## <span data-ttu-id="dd82d-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="dd82d-138">NOTES</span></span>

## <span data-ttu-id="dd82d-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dd82d-139">RELATED LINKS</span></span>

[<span data-ttu-id="dd82d-140">Új – AzureSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="dd82d-140">New-AzureSiteRecoveryNetworkMapping</span></span>](./New-AzureSiteRecoveryNetworkMapping.md)

[<span data-ttu-id="dd82d-141">Remove-AzureSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="dd82d-141">Remove-AzureSiteRecoveryNetworkMapping</span></span>](./Remove-AzureSiteRecoveryNetworkMapping.md)


