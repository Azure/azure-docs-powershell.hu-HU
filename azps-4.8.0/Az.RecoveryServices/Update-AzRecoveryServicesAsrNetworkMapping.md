---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: 09e6cbbbae30d1a2e43d8292573f4bf45d9db461
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181006"
---
# <span data-ttu-id="86bcd-101">Update-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="86bcd-101">Update-AzRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="86bcd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="86bcd-102">SYNOPSIS</span></span>
<span data-ttu-id="86bcd-103">Frissíti a megadott Azure-webhely-helyreállítási hálózati megfeleltetést.</span><span class="sxs-lookup"><span data-stu-id="86bcd-103">Updates the specified azure site recovery network mapping.</span></span>

## <span data-ttu-id="86bcd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="86bcd-104">SYNTAX</span></span>

### <span data-ttu-id="86bcd-105">ByNetworkObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="86bcd-105">ByNetworkObject (Default)</span></span>
```
Update-AzRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping> -RecoveryNetwork <ASRNetwork>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86bcd-106">ById</span><span class="sxs-lookup"><span data-stu-id="86bcd-106">ById</span></span>
```
Update-AzRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping> -RecoveryAzureNetworkId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="86bcd-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="86bcd-107">DESCRIPTION</span></span>
<span data-ttu-id="86bcd-108">Az **Update-AzRecoveryServicesAsrNetworkMapping** parancsmag frissíti a megadott Azure-webhely-helyreállítási hálózati megfeleltetést.</span><span class="sxs-lookup"><span data-stu-id="86bcd-108">The **Update-AzRecoveryServicesAsrNetworkMapping** cmdlet updates the specified Azure Site Recovery network mapping.</span></span>

## <span data-ttu-id="86bcd-109">Példák</span><span class="sxs-lookup"><span data-stu-id="86bcd-109">EXAMPLES</span></span>

### <span data-ttu-id="86bcd-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="86bcd-110">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrNetworkMapping -Mapping $NetworkMapping -RecoveryNetwork $RecoveryNetwork
```

<span data-ttu-id="86bcd-111">Elindítja a hálózati megfeleltetési műveletet a megadott paraméterekkel, és a művelet nyomon követéséhez használt ASR-feladatot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="86bcd-111">Starts the update network mapping operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="86bcd-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="86bcd-112">PARAMETERS</span></span>

### <span data-ttu-id="86bcd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86bcd-113">-DefaultProfile</span></span>
<span data-ttu-id="86bcd-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="86bcd-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="86bcd-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="86bcd-115">-InputObject</span></span>
<span data-ttu-id="86bcd-116">Beviteli objektum: Itt adhatja meg, hogy az ASR-hálózati megfeleltetési objektum az ASR-hálózati megfeleltetésnek megfelelően frissüljön-e.</span><span class="sxs-lookup"><span data-stu-id="86bcd-116">Input Object: Specifies the ASR network mapping object corresponding to the ASR network mapping to be updated.</span></span>

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

### <span data-ttu-id="86bcd-117">-RecoveryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="86bcd-117">-RecoveryAzureNetworkId</span></span>
<span data-ttu-id="86bcd-118">A helyreállítási Azure hálózati AZONOSÍTÓját adja meg a hálózati megfeleltetéshez.</span><span class="sxs-lookup"><span data-stu-id="86bcd-118">Specifies the recovery azure network ID for the network mapping.</span></span>

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

### <span data-ttu-id="86bcd-119">-RecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="86bcd-119">-RecoveryNetwork</span></span>
<span data-ttu-id="86bcd-120">A hálózati megfeleltetéshez a helyreállítási hálózat objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="86bcd-120">Specifies the recovery network object for the network mapping.</span></span>

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

### <span data-ttu-id="86bcd-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="86bcd-121">-Confirm</span></span>
<span data-ttu-id="86bcd-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="86bcd-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86bcd-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86bcd-123">-WhatIf</span></span>
<span data-ttu-id="86bcd-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="86bcd-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="86bcd-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="86bcd-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="86bcd-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86bcd-126">CommonParameters</span></span>
<span data-ttu-id="86bcd-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="86bcd-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86bcd-128">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="86bcd-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86bcd-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="86bcd-129">INPUTS</span></span>

### <span data-ttu-id="86bcd-130">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="86bcd-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping</span></span>

## <span data-ttu-id="86bcd-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="86bcd-131">OUTPUTS</span></span>

### <span data-ttu-id="86bcd-132">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="86bcd-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="86bcd-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="86bcd-133">NOTES</span></span>

## <span data-ttu-id="86bcd-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="86bcd-134">RELATED LINKS</span></span>
