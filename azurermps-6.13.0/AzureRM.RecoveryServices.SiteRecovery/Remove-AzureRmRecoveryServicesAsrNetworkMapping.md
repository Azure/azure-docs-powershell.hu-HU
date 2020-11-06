---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/remove-azurermrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: 56c188b6b6e902fffa9cd777d6a5acf3b38cb2fe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493975"
---
# <span data-ttu-id="a082b-101">Remove-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="a082b-101">Remove-AzureRmRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="a082b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a082b-102">SYNOPSIS</span></span>
<span data-ttu-id="a082b-103">Törli a megadott ASR-hálózati megfeleltetést a helyreállítási szolgáltatások pincéjében.</span><span class="sxs-lookup"><span data-stu-id="a082b-103">Deletes the specified ASR network mapping from the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a082b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a082b-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a082b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a082b-105">DESCRIPTION</span></span>
<span data-ttu-id="a082b-106">A **Remove-AzureRmRecoveryServicesAsrNetworkMapping** parancsmag törli a megadott ASR-hálózati megfeleltetést.</span><span class="sxs-lookup"><span data-stu-id="a082b-106">The **Remove-AzureRmRecoveryServicesAsrNetworkMapping** cmdlet deletes the specified ASR network mapping.</span></span>

## <span data-ttu-id="a082b-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a082b-107">EXAMPLES</span></span>

### <span data-ttu-id="a082b-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="a082b-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrNetworkMapping -NetworkMapping $networkmapping
```

<span data-ttu-id="a082b-109">Elindítja a megadott ASR-hálózati megfeleltetés törlését, és a művelet nyomon követéséhez használt ASR-feladatot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="a082b-109">Starts the deletion of specified ASR network mapping and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="a082b-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a082b-110">PARAMETERS</span></span>

### <span data-ttu-id="a082b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a082b-111">-DefaultProfile</span></span>
<span data-ttu-id="a082b-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a082b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a082b-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a082b-113">-InputObject</span></span>
<span data-ttu-id="a082b-114">A bemeneti objektum a parancsmag: az ASR hálózati megfeleltetési objektum, amely megfelel a törölni kívánt ASR-hálózati megfeleltetésnek.</span><span class="sxs-lookup"><span data-stu-id="a082b-114">The input object to the cmdlet: The ASR network mapping object corresponding to the ASR network mapping to be deleted.</span></span>

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

### <span data-ttu-id="a082b-115">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a082b-115">-Confirm</span></span>
<span data-ttu-id="a082b-116">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a082b-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a082b-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a082b-117">-WhatIf</span></span>
<span data-ttu-id="a082b-118">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a082b-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a082b-119">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a082b-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a082b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a082b-120">CommonParameters</span></span>
<span data-ttu-id="a082b-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a082b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a082b-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a082b-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a082b-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a082b-123">INPUTS</span></span>

### <span data-ttu-id="a082b-124">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="a082b-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping</span></span>

## <span data-ttu-id="a082b-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a082b-125">OUTPUTS</span></span>

### <span data-ttu-id="a082b-126">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="a082b-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="a082b-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a082b-127">NOTES</span></span>

## <span data-ttu-id="a082b-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a082b-128">RELATED LINKS</span></span>

[<span data-ttu-id="a082b-129">Get-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="a082b-129">Get-AzureRmRecoveryServicesAsrNetworkMapping</span></span>](./Get-AzureRmRecoveryServicesAsrNetworkMapping.md)

[<span data-ttu-id="a082b-130">Új – AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="a082b-130">New-AzureRmRecoveryServicesAsrNetworkMapping</span></span>](./New-AzureRmRecoveryServicesAsrNetworkMapping.md)
