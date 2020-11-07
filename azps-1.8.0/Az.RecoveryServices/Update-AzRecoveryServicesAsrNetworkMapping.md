---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: 32412127388e233af303cc29de8ecf66304a0bf3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669579"
---
# <span data-ttu-id="92738-101">Update-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="92738-101">Update-AzRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="92738-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="92738-102">SYNOPSIS</span></span>
<span data-ttu-id="92738-103">Frissíti a megadott Azure-webhely-helyreállítási hálózati megfeleltetést.</span><span class="sxs-lookup"><span data-stu-id="92738-103">Updates the specified azure site recovery network mapping.</span></span>

## <span data-ttu-id="92738-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="92738-104">SYNTAX</span></span>

### <span data-ttu-id="92738-105">ByNetworkObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="92738-105">ByNetworkObject (Default)</span></span>
```
Update-AzRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping> -RecoveryNetwork <ASRNetwork>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92738-106">ById</span><span class="sxs-lookup"><span data-stu-id="92738-106">ById</span></span>
```
Update-AzRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping> -RecoveryAzureNetworkId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="92738-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="92738-107">DESCRIPTION</span></span>
<span data-ttu-id="92738-108">Az **Update-AzRecoveryServicesAsrNetworkMapping** parancsmag frissíti a megadott Azure-webhely-helyreállítási hálózati megfeleltetést.</span><span class="sxs-lookup"><span data-stu-id="92738-108">The **Update-AzRecoveryServicesAsrNetworkMapping** cmdlet updates the specified Azure Site Recovery network mapping.</span></span>

## <span data-ttu-id="92738-109">Példák</span><span class="sxs-lookup"><span data-stu-id="92738-109">EXAMPLES</span></span>

### <span data-ttu-id="92738-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="92738-110">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrNetworkMapping -Mapping $NetworkMapping -RecoveryNetwork $RecoveryNetwork
```

<span data-ttu-id="92738-111">Elindítja a hálózati megfeleltetési műveletet a megadott paraméterekkel, és a művelet nyomon követéséhez használt ASR-feladatot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="92738-111">Starts the update network mapping operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="92738-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="92738-112">PARAMETERS</span></span>

### <span data-ttu-id="92738-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92738-113">-DefaultProfile</span></span>
<span data-ttu-id="92738-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="92738-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="92738-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="92738-115">-InputObject</span></span>
<span data-ttu-id="92738-116">Beviteli objektum: Itt adhatja meg, hogy az ASR-hálózati megfeleltetési objektum az ASR-hálózati megfeleltetésnek megfelelően frissüljön-e.</span><span class="sxs-lookup"><span data-stu-id="92738-116">Input Object: Specifies the ASR network mapping object corresponding to the ASR network mapping to be updated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping
Parameter Sets: (All)
Aliases: NetworkMapping

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="92738-117">-RecoveryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="92738-117">-RecoveryAzureNetworkId</span></span>
<span data-ttu-id="92738-118">A helyreállítási Azure hálózati AZONOSÍTÓját adja meg a hálózati megfeleltetéshez.</span><span class="sxs-lookup"><span data-stu-id="92738-118">Specifies the recovery azure network ID for the network mapping.</span></span>

```yaml
Type: System.String
Parameter Sets: ById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92738-119">-RecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="92738-119">-RecoveryNetwork</span></span>
<span data-ttu-id="92738-120">A hálózati megfeleltetéshez a helyreállítási hálózat objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="92738-120">Specifies the recovery network object for the network mapping.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork
Parameter Sets: ByNetworkObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92738-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="92738-121">-Confirm</span></span>
<span data-ttu-id="92738-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="92738-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92738-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92738-123">-WhatIf</span></span>
<span data-ttu-id="92738-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="92738-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="92738-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="92738-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92738-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92738-126">CommonParameters</span></span>
<span data-ttu-id="92738-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="92738-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92738-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92738-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92738-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="92738-129">INPUTS</span></span>

### <span data-ttu-id="92738-130">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="92738-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping</span></span>

## <span data-ttu-id="92738-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="92738-131">OUTPUTS</span></span>

### <span data-ttu-id="92738-132">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="92738-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="92738-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="92738-133">NOTES</span></span>

## <span data-ttu-id="92738-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="92738-134">RELATED LINKS</span></span>
