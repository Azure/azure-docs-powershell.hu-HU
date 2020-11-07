---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrvCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrvCenter.md
ms.openlocfilehash: 98bc2dfde30357e7f6a3db62ec550a2a0c173bb8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669658"
---
# <span data-ttu-id="e8753-101">New-AzRecoveryServicesAsrvCenter</span><span class="sxs-lookup"><span data-stu-id="e8753-101">New-AzRecoveryServicesAsrvCenter</span></span>

## <span data-ttu-id="e8753-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e8753-102">SYNOPSIS</span></span>
<span data-ttu-id="e8753-103">Felvesz egy vCenter-kiszolgálót a védett elemek felfedezéséhez.</span><span class="sxs-lookup"><span data-stu-id="e8753-103">Adds a vCenter server to discover protectable items from.</span></span>

## <span data-ttu-id="e8753-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e8753-104">SYNTAX</span></span>

```
New-AzRecoveryServicesAsrvCenter -Fabric <ASRFabric> -Name <String> -Account <ASRRunAsAccount> -Port <Int32>
 -IpOrHostName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8753-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e8753-105">DESCRIPTION</span></span>
<span data-ttu-id="e8753-106">A **New-AzRecoveryServicesAsrvCenter** parancsmag felveszi a vCenter kiszolgálóját a védett elemek felfedezéséhez.</span><span class="sxs-lookup"><span data-stu-id="e8753-106">The **New-AzRecoveryServicesAsrvCenter** cmdlet adds a vCenter server to discover protectable items from.</span></span> <span data-ttu-id="e8753-107">Ez a parancsmag a vCenter-kiszolgálót regisztrálja a konfigurációs kiszolgálóval való felderítéshez.</span><span class="sxs-lookup"><span data-stu-id="e8753-107">This cmdlet registers the vCenter server for discovery with the Configuration server.</span></span>

## <span data-ttu-id="e8753-108">Példák</span><span class="sxs-lookup"><span data-stu-id="e8753-108">EXAMPLES</span></span>

### <span data-ttu-id="e8753-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e8753-109">Example 1</span></span>
```
PS C:\> New-AzRecoveryServicesAsrvCenterServer -Account $ConfigServer.FabricSpecificDetails.RunAsAccounts[1] -Fabric $ConfigServer -Name InmTest59 -Port 443 -Server 10.150.209.6

Asr Job for vCenter creation.
```

<span data-ttu-id="e8753-110">Felvesz egy vCenter-kiszolgálót a védett elemek felfedezéséhez.</span><span class="sxs-lookup"><span data-stu-id="e8753-110">Adds a vCenter server to discover protectable items from.</span></span>

## <span data-ttu-id="e8753-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e8753-111">PARAMETERS</span></span>

### <span data-ttu-id="e8753-112">-Fiók</span><span class="sxs-lookup"><span data-stu-id="e8753-112">-Account</span></span>
<span data-ttu-id="e8753-113">Felhasználó bejelentkezési creadential-fiókja.</span><span class="sxs-lookup"><span data-stu-id="e8753-113">User login creadential Account.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRunAsAccount
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8753-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8753-114">-DefaultProfile</span></span>
<span data-ttu-id="e8753-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e8753-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8753-116">-Szövet</span><span class="sxs-lookup"><span data-stu-id="e8753-116">-Fabric</span></span>
<span data-ttu-id="e8753-117">A konfigurációs kiszolgálónak megfelelő ASR-anyag.</span><span class="sxs-lookup"><span data-stu-id="e8753-117">ASR fabric corresponding to the Configuration server.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e8753-118">-IpOrHostName</span><span class="sxs-lookup"><span data-stu-id="e8753-118">-IpOrHostName</span></span>
<span data-ttu-id="e8753-119">Az vCenter-kiszolgáló IPv4-címe vagy FQDN-je.</span><span class="sxs-lookup"><span data-stu-id="e8753-119">IPv4 address or FQDN of the vCenter server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8753-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e8753-120">-Name</span></span>
<span data-ttu-id="e8753-121">A vCenter-kiszolgáló rövid neve.</span><span class="sxs-lookup"><span data-stu-id="e8753-121">A friendly name for the vCenter server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8753-122">-Port</span><span class="sxs-lookup"><span data-stu-id="e8753-122">-Port</span></span>
<span data-ttu-id="e8753-123">A vCenter-kiszolgáló TCP-portja, amelyet a felderítéshez szeretne használni.</span><span class="sxs-lookup"><span data-stu-id="e8753-123">The TCP port on the vCenter server to use for discovery.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8753-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e8753-124">-Confirm</span></span>
<span data-ttu-id="e8753-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e8753-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8753-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8753-126">-WhatIf</span></span>
<span data-ttu-id="e8753-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e8753-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8753-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e8753-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8753-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8753-129">CommonParameters</span></span>
<span data-ttu-id="e8753-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e8753-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8753-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8753-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8753-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e8753-132">INPUTS</span></span>

### <span data-ttu-id="e8753-133">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="e8753-133">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="e8753-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e8753-134">OUTPUTS</span></span>

### <span data-ttu-id="e8753-135">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="e8753-135">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="e8753-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e8753-136">NOTES</span></span>

## <span data-ttu-id="e8753-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e8753-137">RELATED LINKS</span></span>
