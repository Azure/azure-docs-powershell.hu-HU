---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: C4C624DB-BBE8-4F94-BDC6-C012482F7271
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/remove-azurermsiterecoverypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryPolicy.md
ms.openlocfilehash: f09ca4bb6c033b954542d6c734b27bf5f2236d87
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492179"
---
# <span data-ttu-id="14c8b-101">Remove-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="14c8b-101">Remove-AzureRmSiteRecoveryPolicy</span></span>

## <span data-ttu-id="14c8b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="14c8b-102">SYNOPSIS</span></span>
<span data-ttu-id="14c8b-103">Webhely-helyreállítási replikációs házirend eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="14c8b-103">Removes a Site Recovery replication policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="14c8b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="14c8b-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryPolicy -Policy <ASRPolicy> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="14c8b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="14c8b-105">DESCRIPTION</span></span>
<span data-ttu-id="14c8b-106">A **Remove-AzureRMSiteRecoveryPolicy** parancsmag eltávolít egy Azure-webhely-helyreállítási replikációs házirendet.</span><span class="sxs-lookup"><span data-stu-id="14c8b-106">The **Remove-AzureRMSiteRecoveryPolicy** cmdlet removes an Azure Site Recovery replication policy.</span></span>

## <span data-ttu-id="14c8b-107">Példák</span><span class="sxs-lookup"><span data-stu-id="14c8b-107">EXAMPLES</span></span>

## <span data-ttu-id="14c8b-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="14c8b-108">PARAMETERS</span></span>

### <span data-ttu-id="14c8b-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14c8b-109">-DefaultProfile</span></span>
<span data-ttu-id="14c8b-110">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="14c8b-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="14c8b-111">-Házirend</span><span class="sxs-lookup"><span data-stu-id="14c8b-111">-Policy</span></span>
<span data-ttu-id="14c8b-112">A webhely-helyreállítási házirend objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="14c8b-112">Specifies the Site Recovery policy object.</span></span>

```yaml
Type: ASRPolicy
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="14c8b-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14c8b-113">CommonParameters</span></span>
<span data-ttu-id="14c8b-114">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="14c8b-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14c8b-115">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14c8b-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14c8b-116">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="14c8b-116">INPUTS</span></span>

### <span data-ttu-id="14c8b-117">ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="14c8b-117">ASRPolicy</span></span>
<span data-ttu-id="14c8b-118">A ' Policy ' paraméter az "ASRPolicy" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="14c8b-118">Parameter 'Policy' accepts value of type 'ASRPolicy' from the pipeline</span></span>

## <span data-ttu-id="14c8b-119">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="14c8b-119">OUTPUTS</span></span>

## <span data-ttu-id="14c8b-120">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="14c8b-120">NOTES</span></span>

## <span data-ttu-id="14c8b-121">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="14c8b-121">RELATED LINKS</span></span>

[<span data-ttu-id="14c8b-122">Get-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="14c8b-122">Get-AzureRmSiteRecoveryPolicy</span></span>](./Get-AzureRmSiteRecoveryPolicy.md)

[<span data-ttu-id="14c8b-123">Új – AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="14c8b-123">New-AzureRmSiteRecoveryPolicy</span></span>](./New-AzureRmSiteRecoveryPolicy.md)
