---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: BDEA3F9D-AC23-402D-BA1F-AC617C7480A1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryNetworkMapping.md
ms.openlocfilehash: 03bd15f1071ac223ba7460c27bcfd9ce96a55dda
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496835"
---
# <span data-ttu-id="6a8fb-101">Remove-AzureRmSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="6a8fb-101">Remove-AzureRmSiteRecoveryNetworkMapping</span></span>

## <span data-ttu-id="6a8fb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6a8fb-102">SYNOPSIS</span></span>
<span data-ttu-id="6a8fb-103">Hálózati megfeleltetés eltávolítása az aktuális webhely-helyreállítási boltozatról.</span><span class="sxs-lookup"><span data-stu-id="6a8fb-103">Removes a network mapping from the current Site Recovery vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6a8fb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6a8fb-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryNetworkMapping -NetworkMapping <ASRNetworkMapping>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6a8fb-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6a8fb-105">DESCRIPTION</span></span>
<span data-ttu-id="6a8fb-106">A **Remove-AzureRMSiteRecoveryNetworkMapping** parancsmag eltávolít egy hálózati megfeleltetést az aktuális Azure webhely-helyreállítási boltozatból.</span><span class="sxs-lookup"><span data-stu-id="6a8fb-106">The **Remove-AzureRMSiteRecoveryNetworkMapping** cmdlet removes a network mapping from the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="6a8fb-107">Példák</span><span class="sxs-lookup"><span data-stu-id="6a8fb-107">EXAMPLES</span></span>

## <span data-ttu-id="6a8fb-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6a8fb-108">PARAMETERS</span></span>

### <span data-ttu-id="6a8fb-109">-NetworkMapping</span><span class="sxs-lookup"><span data-stu-id="6a8fb-109">-NetworkMapping</span></span>
<span data-ttu-id="6a8fb-110">A hálózati megfeleltetési objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="6a8fb-110">Specifies the network mapping object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRNetworkMapping
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6a8fb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a8fb-111">-DefaultProfile</span></span>
<span data-ttu-id="6a8fb-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6a8fb-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6a8fb-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a8fb-113">CommonParameters</span></span>
<span data-ttu-id="6a8fb-114">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6a8fb-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a8fb-115">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a8fb-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a8fb-116">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6a8fb-116">INPUTS</span></span>

### <span data-ttu-id="6a8fb-117">ASRNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="6a8fb-117">ASRNetworkMapping</span></span>
<span data-ttu-id="6a8fb-118">A ' NetworkMapping ' paraméter az "ASRNetworkMapping" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="6a8fb-118">Parameter 'NetworkMapping' accepts value of type 'ASRNetworkMapping' from the pipeline</span></span>

## <span data-ttu-id="6a8fb-119">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6a8fb-119">OUTPUTS</span></span>

### <span data-ttu-id="6a8fb-120">Microsoft. Azure. Command. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="6a8fb-120">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="6a8fb-121">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6a8fb-121">NOTES</span></span>

## <span data-ttu-id="6a8fb-122">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6a8fb-122">RELATED LINKS</span></span>

[<span data-ttu-id="6a8fb-123">Get-AzureRmSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="6a8fb-123">Get-AzureRmSiteRecoveryNetworkMapping</span></span>](./Get-AzureRmSiteRecoveryNetworkMapping.md)

[<span data-ttu-id="6a8fb-124">Új – AzureRmSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="6a8fb-124">New-AzureRmSiteRecoveryNetworkMapping</span></span>](./New-AzureRmSiteRecoveryNetworkMapping.md)
