---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrVCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrVCenter.md
ms.openlocfilehash: 1d298a543071c879e2279734247febba00b8da21
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492224"
---
# <span data-ttu-id="96630-101">New-AzureRmRecoveryServicesAsrvCenter</span><span class="sxs-lookup"><span data-stu-id="96630-101">New-AzureRmRecoveryServicesAsrvCenter</span></span>

## <span data-ttu-id="96630-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="96630-102">SYNOPSIS</span></span>
<span data-ttu-id="96630-103">Felvesz egy vCenter-kiszolgálót a védett elemek felfedezéséhez.</span><span class="sxs-lookup"><span data-stu-id="96630-103">Adds a vCenter server to discover protectable items from.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="96630-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="96630-104">SYNTAX</span></span>

```
New-AzureRmRecoveryServicesAsrvCenter -Fabric <ASRFabric> -Name <String> -Account <ASRRunAsAccount>
 -Port <Int32> -IpOrHostName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="96630-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="96630-105">DESCRIPTION</span></span>
<span data-ttu-id="96630-106">A **New-AzureRmRecoveryServicesAsrvCenter** parancsmag felveszi a vCenter kiszolgálóját a védett elemek felfedezéséhez.</span><span class="sxs-lookup"><span data-stu-id="96630-106">The **New-AzureRmRecoveryServicesAsrvCenter** cmdlet adds a vCenter server to discover protectable items from.</span></span> <span data-ttu-id="96630-107">Ez a parancsmag a vCenter-kiszolgálót regisztrálja a konfigurációs kiszolgálóval való felderítéshez.</span><span class="sxs-lookup"><span data-stu-id="96630-107">This cmdlet registers the vCenter server for discovery with the Configuration server.</span></span>

## <span data-ttu-id="96630-108">Példák</span><span class="sxs-lookup"><span data-stu-id="96630-108">EXAMPLES</span></span>

### <span data-ttu-id="96630-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="96630-109">Example 1</span></span>
```
PS C:\> New-AzureRmRecoveryServicesAsrvCenterServer -Account $ConfigServer.FabricSpecificDetails.RunAsAccounts[1] -Fabric $ConfigServer -Name InmTest59 -Port 443 -Server 10.150.209.6

Asr Job for vCenter creation.
```

<span data-ttu-id="96630-110">Felvesz egy vCenter-kiszolgálót a védett elemek felfedezéséhez.</span><span class="sxs-lookup"><span data-stu-id="96630-110">Adds a vCenter server to discover protectable items from.</span></span>

## <span data-ttu-id="96630-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="96630-111">PARAMETERS</span></span>

### <span data-ttu-id="96630-112">-Fiók</span><span class="sxs-lookup"><span data-stu-id="96630-112">-Account</span></span>
<span data-ttu-id="96630-113">Felhasználó bejelentkezési creadential-fiókja.</span><span class="sxs-lookup"><span data-stu-id="96630-113">User login creadential Account.</span></span>

```yaml
Type: ASRRunAsAccount
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96630-114">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="96630-114">-Confirm</span></span>
<span data-ttu-id="96630-115">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="96630-115">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96630-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96630-116">-DefaultProfile</span></span>
<span data-ttu-id="96630-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="96630-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96630-118">-Szövet</span><span class="sxs-lookup"><span data-stu-id="96630-118">-Fabric</span></span>
<span data-ttu-id="96630-119">A konfigurációs kiszolgálónak megfelelő ASR-anyag.</span><span class="sxs-lookup"><span data-stu-id="96630-119">ASR fabric corresponding to the Configuration server.</span></span>

```yaml
Type: ASRFabric
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="96630-120">-IpOrHostName</span><span class="sxs-lookup"><span data-stu-id="96630-120">-IpOrHostName</span></span>
<span data-ttu-id="96630-121">Az vCenter-kiszolgáló IPv4-címe vagy FQDN-je.</span><span class="sxs-lookup"><span data-stu-id="96630-121">IPv4 address or FQDN of the vCenter server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96630-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="96630-122">-Name</span></span>
<span data-ttu-id="96630-123">A vCenter-kiszolgáló rövid neve.</span><span class="sxs-lookup"><span data-stu-id="96630-123">A friendly name for the vCenter server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96630-124">-Port</span><span class="sxs-lookup"><span data-stu-id="96630-124">-Port</span></span>
<span data-ttu-id="96630-125">A vCenter-kiszolgáló TCP-portja, amelyet a felderítéshez szeretne használni.</span><span class="sxs-lookup"><span data-stu-id="96630-125">The TCP port on the vCenter server to use for discovery.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96630-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96630-126">-WhatIf</span></span>
<span data-ttu-id="96630-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="96630-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="96630-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="96630-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96630-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96630-129">CommonParameters</span></span>
<span data-ttu-id="96630-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="96630-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96630-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96630-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96630-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="96630-132">INPUTS</span></span>

### <span data-ttu-id="96630-133">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="96630-133">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="96630-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="96630-134">OUTPUTS</span></span>

### <span data-ttu-id="96630-135">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob, Microsoft. Azure. commands. RecoveryServices. SiteRecovery; Version = 0.1.1.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="96630-135">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=0.1.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="96630-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="96630-136">NOTES</span></span>

## <span data-ttu-id="96630-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="96630-137">RELATED LINKS</span></span>
