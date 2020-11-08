---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: ef251bb9d1060e511658f9174cde2c04ab288ed7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94188044"
---
# <span data-ttu-id="2f196-101">Remove-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="2f196-101">Remove-AzRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="2f196-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2f196-102">SYNOPSIS</span></span>
<span data-ttu-id="2f196-103">Törli a megadott ASR-hálózati megfeleltetést a helyreállítási szolgáltatások pincéjében.</span><span class="sxs-lookup"><span data-stu-id="2f196-103">Deletes the specified ASR network mapping from the Recovery Services vault.</span></span>

## <span data-ttu-id="2f196-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2f196-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f196-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2f196-105">DESCRIPTION</span></span>
<span data-ttu-id="2f196-106">A **Remove-AzRecoveryServicesAsrNetworkMapping** parancsmag törli a megadott ASR-hálózati megfeleltetést.</span><span class="sxs-lookup"><span data-stu-id="2f196-106">The **Remove-AzRecoveryServicesAsrNetworkMapping** cmdlet deletes the specified ASR network mapping.</span></span>

## <span data-ttu-id="2f196-107">Példák</span><span class="sxs-lookup"><span data-stu-id="2f196-107">EXAMPLES</span></span>

### <span data-ttu-id="2f196-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="2f196-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrNetworkMapping -NetworkMapping $networkmapping
```

<span data-ttu-id="2f196-109">Elindítja a megadott ASR-hálózati megfeleltetés törlését, és a művelet nyomon követéséhez használt ASR-feladatot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="2f196-109">Starts the deletion of specified ASR network mapping and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="2f196-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2f196-110">PARAMETERS</span></span>

### <span data-ttu-id="2f196-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f196-111">-DefaultProfile</span></span>
<span data-ttu-id="2f196-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2f196-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="2f196-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2f196-113">-InputObject</span></span>
<span data-ttu-id="2f196-114">A bemeneti objektum a parancsmag: az ASR hálózati megfeleltetési objektum, amely megfelel a törölni kívánt ASR-hálózati megfeleltetésnek.</span><span class="sxs-lookup"><span data-stu-id="2f196-114">The input object to the cmdlet: The ASR network mapping object corresponding to the ASR network mapping to be deleted.</span></span>

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

### <span data-ttu-id="2f196-115">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2f196-115">-Confirm</span></span>
<span data-ttu-id="2f196-116">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2f196-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f196-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f196-117">-WhatIf</span></span>
<span data-ttu-id="2f196-118">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2f196-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2f196-119">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2f196-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f196-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f196-120">CommonParameters</span></span>
<span data-ttu-id="2f196-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2f196-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f196-122">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="2f196-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f196-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2f196-123">INPUTS</span></span>

### <span data-ttu-id="2f196-124">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="2f196-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping</span></span>

## <span data-ttu-id="2f196-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2f196-125">OUTPUTS</span></span>

### <span data-ttu-id="2f196-126">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="2f196-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="2f196-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2f196-127">NOTES</span></span>

## <span data-ttu-id="2f196-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2f196-128">RELATED LINKS</span></span>

[<span data-ttu-id="2f196-129">Get-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="2f196-129">Get-AzRecoveryServicesAsrNetworkMapping</span></span>](./Get-AzRecoveryServicesAsrNetworkMapping.md)

[<span data-ttu-id="2f196-130">Új – AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="2f196-130">New-AzRecoveryServicesAsrNetworkMapping</span></span>](./New-AzRecoveryServicesAsrNetworkMapping.md)
