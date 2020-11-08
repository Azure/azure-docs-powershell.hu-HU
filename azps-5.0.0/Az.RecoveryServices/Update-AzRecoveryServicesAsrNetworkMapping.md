---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: 09e6cbbbae30d1a2e43d8292573f4bf45d9db461
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186841"
---
# <span data-ttu-id="f3d77-101">Update-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="f3d77-101">Update-AzRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="f3d77-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f3d77-102">SYNOPSIS</span></span>
<span data-ttu-id="f3d77-103">Frissíti a megadott Azure-webhely-helyreállítási hálózati megfeleltetést.</span><span class="sxs-lookup"><span data-stu-id="f3d77-103">Updates the specified azure site recovery network mapping.</span></span>

## <span data-ttu-id="f3d77-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f3d77-104">SYNTAX</span></span>

### <span data-ttu-id="f3d77-105">ByNetworkObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f3d77-105">ByNetworkObject (Default)</span></span>
```
Update-AzRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping> -RecoveryNetwork <ASRNetwork>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3d77-106">ById</span><span class="sxs-lookup"><span data-stu-id="f3d77-106">ById</span></span>
```
Update-AzRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping> -RecoveryAzureNetworkId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f3d77-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="f3d77-107">DESCRIPTION</span></span>
<span data-ttu-id="f3d77-108">Az **Update-AzRecoveryServicesAsrNetworkMapping** parancsmag frissíti a megadott Azure-webhely-helyreállítási hálózati megfeleltetést.</span><span class="sxs-lookup"><span data-stu-id="f3d77-108">The **Update-AzRecoveryServicesAsrNetworkMapping** cmdlet updates the specified Azure Site Recovery network mapping.</span></span>

## <span data-ttu-id="f3d77-109">Példák</span><span class="sxs-lookup"><span data-stu-id="f3d77-109">EXAMPLES</span></span>

### <span data-ttu-id="f3d77-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="f3d77-110">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrNetworkMapping -Mapping $NetworkMapping -RecoveryNetwork $RecoveryNetwork
```

<span data-ttu-id="f3d77-111">Elindítja a hálózati megfeleltetési műveletet a megadott paraméterekkel, és a művelet nyomon követéséhez használt ASR-feladatot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="f3d77-111">Starts the update network mapping operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="f3d77-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f3d77-112">PARAMETERS</span></span>

### <span data-ttu-id="f3d77-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3d77-113">-DefaultProfile</span></span>
<span data-ttu-id="f3d77-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f3d77-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="f3d77-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f3d77-115">-InputObject</span></span>
<span data-ttu-id="f3d77-116">Beviteli objektum: Itt adhatja meg, hogy az ASR-hálózati megfeleltetési objektum az ASR-hálózati megfeleltetésnek megfelelően frissüljön-e.</span><span class="sxs-lookup"><span data-stu-id="f3d77-116">Input Object: Specifies the ASR network mapping object corresponding to the ASR network mapping to be updated.</span></span>

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

### <span data-ttu-id="f3d77-117">-RecoveryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="f3d77-117">-RecoveryAzureNetworkId</span></span>
<span data-ttu-id="f3d77-118">A helyreállítási Azure hálózati AZONOSÍTÓját adja meg a hálózati megfeleltetéshez.</span><span class="sxs-lookup"><span data-stu-id="f3d77-118">Specifies the recovery azure network ID for the network mapping.</span></span>

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

### <span data-ttu-id="f3d77-119">-RecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="f3d77-119">-RecoveryNetwork</span></span>
<span data-ttu-id="f3d77-120">A hálózati megfeleltetéshez a helyreállítási hálózat objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="f3d77-120">Specifies the recovery network object for the network mapping.</span></span>

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

### <span data-ttu-id="f3d77-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f3d77-121">-Confirm</span></span>
<span data-ttu-id="f3d77-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f3d77-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3d77-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3d77-123">-WhatIf</span></span>
<span data-ttu-id="f3d77-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f3d77-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f3d77-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f3d77-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3d77-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3d77-126">CommonParameters</span></span>
<span data-ttu-id="f3d77-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f3d77-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3d77-128">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="f3d77-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3d77-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f3d77-129">INPUTS</span></span>

### <span data-ttu-id="f3d77-130">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="f3d77-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping</span></span>

## <span data-ttu-id="f3d77-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f3d77-131">OUTPUTS</span></span>

### <span data-ttu-id="f3d77-132">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="f3d77-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="f3d77-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f3d77-133">NOTES</span></span>

## <span data-ttu-id="f3d77-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f3d77-134">RELATED LINKS</span></span>
