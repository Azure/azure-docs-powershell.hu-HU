---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 6802F2E9-5925-4E92-AEB8-827B5A303617
online version: ''
schema: 2.0.0
ms.openlocfilehash: 153e30c03de7a0a5c404526bd06b9acb2f0678f3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016217"
---
# <span data-ttu-id="9c8ea-101">New-AzureSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="9c8ea-101">New-AzureSiteRecoveryNetworkMapping</span></span>

## <span data-ttu-id="9c8ea-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9c8ea-102">SYNOPSIS</span></span>
<span data-ttu-id="9c8ea-103">Társítást hoz létre a virtuális hálózatok között.</span><span class="sxs-lookup"><span data-stu-id="9c8ea-103">Creates a mapping between virtual networks.</span></span>

## <span data-ttu-id="9c8ea-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9c8ea-104">SYNTAX</span></span>

### <span data-ttu-id="9c8ea-105">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="9c8ea-105">EnterpriseToEnterprise</span></span>
```
New-AzureSiteRecoveryNetworkMapping -PrimaryNetwork <ASRNetwork> -RecoveryNetwork <ASRNetwork>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="9c8ea-106">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="9c8ea-106">EnterpriseToAzure</span></span>
```
New-AzureSiteRecoveryNetworkMapping -PrimaryNetwork <ASRNetwork> -AzureSubscriptionId <String>
 -AzureVMNetworkId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="9c8ea-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="9c8ea-107">DESCRIPTION</span></span>
<span data-ttu-id="9c8ea-108">A **New-AzureSiteRecoveryNetworkMapping** parancsmag létrehoz egy megfeleltetést két virtuális hálózat között, és egy Azure webhely-helyreállítási feladatot ad eredményül a követéshez.</span><span class="sxs-lookup"><span data-stu-id="9c8ea-108">The **New-AzureSiteRecoveryNetworkMapping** cmdlet creates a mapping between two virtual networks and returns an Azure Site Recovery job to track it.</span></span>

## <span data-ttu-id="9c8ea-109">Példák</span><span class="sxs-lookup"><span data-stu-id="9c8ea-109">EXAMPLES</span></span>

### <span data-ttu-id="9c8ea-110">1. példa: megfeleltetés létrehozása a hálózat és a helyreállítási hálózat között</span><span class="sxs-lookup"><span data-stu-id="9c8ea-110">Example 1: Create a mapping between a network and a recovery network</span></span>
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> $Networks = Get-AzureSiteRecoveryNetwork -Server $Servers[0]
PS C:\> New-AzureSiteRecoveryNetworkMapping -PrimaryNetwork $Networks[0] -RecoveryNetwork $Networks[1]
```

<span data-ttu-id="9c8ea-111">Az első Command parancsmag a **Get-AzureSiteRecoveryServer** parancsmaggal kapja meg az aktuális Azure-webhely helyreállítási boltozatának kiszolgálóit.</span><span class="sxs-lookup"><span data-stu-id="9c8ea-111">The first command cmdlet gets servers for the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryServer** cmdlet.</span></span>
<span data-ttu-id="9c8ea-112">A parancs a $Servers Array változóban tárolja a webhely-helyreállítási kiszolgálókat.</span><span class="sxs-lookup"><span data-stu-id="9c8ea-112">The command stores the Site Recovery servers in the $Servers array variable.</span></span>

<span data-ttu-id="9c8ea-113">A második parancs a **Get-AzureSiteRecoveryNetwork** parancsmaggal kapja meg az első kiszolgálónak a webhely-helyreállítási hálózatát a $Servers tömbben.</span><span class="sxs-lookup"><span data-stu-id="9c8ea-113">The second command gets the site recovery network for the first server in the $Servers array by using the **Get-AzureSiteRecoveryNetwork** cmdlet.</span></span>
<span data-ttu-id="9c8ea-114">A parancs a $Networks változóban tárolja a hálózatokat.</span><span class="sxs-lookup"><span data-stu-id="9c8ea-114">The command stores the networks in the $Networks variable.</span></span>

<span data-ttu-id="9c8ea-115">A végleges parancs az elsődleges hálózat és a helyreállítási hálózat között hoz létre megfeleltetést.</span><span class="sxs-lookup"><span data-stu-id="9c8ea-115">The final command creates a mapping between the primary network and the recovery network.</span></span>
<span data-ttu-id="9c8ea-116">A parancs az elsődleges hálózatot az $Networks első elemeként adja meg.</span><span class="sxs-lookup"><span data-stu-id="9c8ea-116">The command specifies the primary network as the first element of $Networks.</span></span>
<span data-ttu-id="9c8ea-117">A parancs a $Networks második elemeként adja meg a helyreállítási hálózatot.</span><span class="sxs-lookup"><span data-stu-id="9c8ea-117">The command specifies the recovery network as the second element of $Networks.</span></span>

## <span data-ttu-id="9c8ea-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9c8ea-118">PARAMETERS</span></span>

### <span data-ttu-id="9c8ea-119">-AzureSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9c8ea-119">-AzureSubscriptionId</span></span>
<span data-ttu-id="9c8ea-120">Az Azure-előfizetés AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="9c8ea-120">Specifies the ID of your Azure subscription.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c8ea-121">-AzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="9c8ea-121">-AzureVMNetworkId</span></span>
<span data-ttu-id="9c8ea-122">Az Azure virtuális hálózat AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="9c8ea-122">Specifies the Azure virtual network ID.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c8ea-123">-PrimaryNetwork</span><span class="sxs-lookup"><span data-stu-id="9c8ea-123">-PrimaryNetwork</span></span>
<span data-ttu-id="9c8ea-124">Az elsődleges hálózat objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="9c8ea-124">Specifies the primary network object.</span></span>

```yaml
Type: ASRNetwork
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c8ea-125">-Profil</span><span class="sxs-lookup"><span data-stu-id="9c8ea-125">-Profile</span></span>
<span data-ttu-id="9c8ea-126">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="9c8ea-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9c8ea-127">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="9c8ea-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9c8ea-128">-RecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="9c8ea-128">-RecoveryNetwork</span></span>
<span data-ttu-id="9c8ea-129">A helyreállítási hálózat objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="9c8ea-129">Specifies the recovery network object.</span></span>

```yaml
Type: ASRNetwork
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c8ea-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c8ea-130">CommonParameters</span></span>
<span data-ttu-id="9c8ea-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9c8ea-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c8ea-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c8ea-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c8ea-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9c8ea-133">INPUTS</span></span>

## <span data-ttu-id="9c8ea-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9c8ea-134">OUTPUTS</span></span>

## <span data-ttu-id="9c8ea-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9c8ea-135">NOTES</span></span>

## <span data-ttu-id="9c8ea-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9c8ea-136">RELATED LINKS</span></span>

[<span data-ttu-id="9c8ea-137">Get-AzureSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="9c8ea-137">Get-AzureSiteRecoveryNetworkMapping</span></span>](./Get-AzureSiteRecoveryNetworkMapping.md)

[<span data-ttu-id="9c8ea-138">Get-AzureSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="9c8ea-138">Get-AzureSiteRecoveryServer</span></span>](./Get-AzureSiteRecoveryServer.md)

[<span data-ttu-id="9c8ea-139">Remove-AzureSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="9c8ea-139">Remove-AzureSiteRecoveryNetworkMapping</span></span>](./Remove-AzureSiteRecoveryNetworkMapping.md)


