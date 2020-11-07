---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: C4C624DB-BBE8-4F94-BDC6-C012482F7271
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryPolicy.md
ms.openlocfilehash: 3b01e089271cc131af5a4258c46836a87104ef62
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672683"
---
# <span data-ttu-id="2cf42-101">Remove-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="2cf42-101">Remove-AzureRmSiteRecoveryPolicy</span></span>

## <span data-ttu-id="2cf42-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2cf42-102">SYNOPSIS</span></span>
<span data-ttu-id="2cf42-103">Webhely-helyreállítási replikációs házirend eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="2cf42-103">Removes a Site Recovery replication policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2cf42-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2cf42-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryPolicy -Policy <ASRPolicy> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2cf42-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2cf42-105">DESCRIPTION</span></span>
<span data-ttu-id="2cf42-106">A **Remove-AzureRMSiteRecoveryPolicy** parancsmag eltávolít egy Azure-webhely-helyreállítási replikációs házirendet.</span><span class="sxs-lookup"><span data-stu-id="2cf42-106">The **Remove-AzureRMSiteRecoveryPolicy** cmdlet removes an Azure Site Recovery replication policy.</span></span>

## <span data-ttu-id="2cf42-107">Példák</span><span class="sxs-lookup"><span data-stu-id="2cf42-107">EXAMPLES</span></span>

## <span data-ttu-id="2cf42-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2cf42-108">PARAMETERS</span></span>

### <span data-ttu-id="2cf42-109">-Házirend</span><span class="sxs-lookup"><span data-stu-id="2cf42-109">-Policy</span></span>
<span data-ttu-id="2cf42-110">A webhely-helyreállítási házirend objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="2cf42-110">Specifies the Site Recovery policy object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRPolicy
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2cf42-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cf42-111">-DefaultProfile</span></span>
<span data-ttu-id="2cf42-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2cf42-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2cf42-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cf42-113">CommonParameters</span></span>
<span data-ttu-id="2cf42-114">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2cf42-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cf42-115">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2cf42-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cf42-116">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2cf42-116">INPUTS</span></span>

### <span data-ttu-id="2cf42-117">ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="2cf42-117">ASRPolicy</span></span>
<span data-ttu-id="2cf42-118">A ' Policy ' paraméter az "ASRPolicy" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="2cf42-118">Parameter 'Policy' accepts value of type 'ASRPolicy' from the pipeline</span></span>

## <span data-ttu-id="2cf42-119">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2cf42-119">OUTPUTS</span></span>

## <span data-ttu-id="2cf42-120">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2cf42-120">NOTES</span></span>

## <span data-ttu-id="2cf42-121">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2cf42-121">RELATED LINKS</span></span>

[<span data-ttu-id="2cf42-122">Get-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="2cf42-122">Get-AzureRmSiteRecoveryPolicy</span></span>](./Get-AzureRmSiteRecoveryPolicy.md)

[<span data-ttu-id="2cf42-123">Új – AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="2cf42-123">New-AzureRmSiteRecoveryPolicy</span></span>](./New-AzureRmSiteRecoveryPolicy.md)
