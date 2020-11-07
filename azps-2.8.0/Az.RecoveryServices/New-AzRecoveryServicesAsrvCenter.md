---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrvCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrvCenter.md
ms.openlocfilehash: 8039da508110b47024be75967932719e5436f73b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839059"
---
# <span data-ttu-id="193db-101">New-AzRecoveryServicesAsrvCenter</span><span class="sxs-lookup"><span data-stu-id="193db-101">New-AzRecoveryServicesAsrvCenter</span></span>

## <span data-ttu-id="193db-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="193db-102">SYNOPSIS</span></span>
<span data-ttu-id="193db-103">Felvesz egy vCenter-kiszolgálót a védett elemek felfedezéséhez.</span><span class="sxs-lookup"><span data-stu-id="193db-103">Adds a vCenter server to discover protectable items from.</span></span>

## <span data-ttu-id="193db-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="193db-104">SYNTAX</span></span>

```
New-AzRecoveryServicesAsrvCenter -Fabric <ASRFabric> -Name <String> -Account <ASRRunAsAccount> -Port <Int32>
 -IpOrHostName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="193db-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="193db-105">DESCRIPTION</span></span>
<span data-ttu-id="193db-106">A **New-AzRecoveryServicesAsrvCenter** parancsmag felveszi a vCenter kiszolgálóját a védett elemek felfedezéséhez.</span><span class="sxs-lookup"><span data-stu-id="193db-106">The **New-AzRecoveryServicesAsrvCenter** cmdlet adds a vCenter server to discover protectable items from.</span></span> <span data-ttu-id="193db-107">Ez a parancsmag a vCenter-kiszolgálót regisztrálja a konfigurációs kiszolgálóval való felderítéshez.</span><span class="sxs-lookup"><span data-stu-id="193db-107">This cmdlet registers the vCenter server for discovery with the Configuration server.</span></span>

## <span data-ttu-id="193db-108">Példák</span><span class="sxs-lookup"><span data-stu-id="193db-108">EXAMPLES</span></span>

### <span data-ttu-id="193db-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="193db-109">Example 1</span></span>
```
PS C:\> New-AzRecoveryServicesAsrvCenterServer -Account $ConfigServer.FabricSpecificDetails.RunAsAccounts[1] -Fabric $ConfigServer -Name InmTest59 -Port 443 -Server 10.150.209.6

Asr Job for vCenter creation.
```

<span data-ttu-id="193db-110">Felvesz egy vCenter-kiszolgálót a védett elemek felfedezéséhez.</span><span class="sxs-lookup"><span data-stu-id="193db-110">Adds a vCenter server to discover protectable items from.</span></span>

## <span data-ttu-id="193db-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="193db-111">PARAMETERS</span></span>

### <span data-ttu-id="193db-112">-Fiók</span><span class="sxs-lookup"><span data-stu-id="193db-112">-Account</span></span>
<span data-ttu-id="193db-113">Bejelentkezési hitelesítőadat-fiók.</span><span class="sxs-lookup"><span data-stu-id="193db-113">User login credential Account.</span></span>

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

### <span data-ttu-id="193db-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="193db-114">-DefaultProfile</span></span>
<span data-ttu-id="193db-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="193db-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="193db-116">-Szövet</span><span class="sxs-lookup"><span data-stu-id="193db-116">-Fabric</span></span>
<span data-ttu-id="193db-117">A konfigurációs kiszolgálónak megfelelő ASR-anyag.</span><span class="sxs-lookup"><span data-stu-id="193db-117">ASR fabric corresponding to the Configuration server.</span></span>

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

### <span data-ttu-id="193db-118">-IpOrHostName</span><span class="sxs-lookup"><span data-stu-id="193db-118">-IpOrHostName</span></span>
<span data-ttu-id="193db-119">Az vCenter-kiszolgáló IPv4-címe vagy FQDN-je.</span><span class="sxs-lookup"><span data-stu-id="193db-119">IPv4 address or FQDN of the vCenter server.</span></span>

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

### <span data-ttu-id="193db-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="193db-120">-Name</span></span>
<span data-ttu-id="193db-121">A vCenter-kiszolgáló rövid neve.</span><span class="sxs-lookup"><span data-stu-id="193db-121">A friendly name for the vCenter server.</span></span>

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

### <span data-ttu-id="193db-122">-Port</span><span class="sxs-lookup"><span data-stu-id="193db-122">-Port</span></span>
<span data-ttu-id="193db-123">A vCenter-kiszolgáló TCP-portja, amelyet a felderítéshez szeretne használni.</span><span class="sxs-lookup"><span data-stu-id="193db-123">The TCP port on the vCenter server to use for discovery.</span></span>

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

### <span data-ttu-id="193db-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="193db-124">-Confirm</span></span>
<span data-ttu-id="193db-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="193db-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="193db-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="193db-126">-WhatIf</span></span>
<span data-ttu-id="193db-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="193db-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="193db-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="193db-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="193db-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="193db-129">CommonParameters</span></span>
<span data-ttu-id="193db-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="193db-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="193db-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="193db-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="193db-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="193db-132">INPUTS</span></span>

### <span data-ttu-id="193db-133">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="193db-133">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="193db-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="193db-134">OUTPUTS</span></span>

### <span data-ttu-id="193db-135">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="193db-135">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="193db-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="193db-136">NOTES</span></span>

## <span data-ttu-id="193db-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="193db-137">RELATED LINKS</span></span>
