---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 07F9EE13-9874-42FC-A17E-7615419F1381
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryPolicy.md
ms.openlocfilehash: 443abbab086fe08ac0a667776a07c792115aa5dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503184"
---
# <span data-ttu-id="febd5-101">Get-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="febd5-101">Get-AzureRmSiteRecoveryPolicy</span></span>

## <span data-ttu-id="febd5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="febd5-102">SYNOPSIS</span></span>
<span data-ttu-id="febd5-103">A webhely-helyreállítási védelem házirendjeit kapja.</span><span class="sxs-lookup"><span data-stu-id="febd5-103">Gets Site Recovery protection policies.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="febd5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="febd5-104">SYNTAX</span></span>

### <span data-ttu-id="febd5-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="febd5-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryPolicy [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="febd5-106">ByName</span><span class="sxs-lookup"><span data-stu-id="febd5-106">ByName</span></span>
```
Get-AzureRmSiteRecoveryPolicy -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="febd5-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="febd5-107">ByFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryPolicy -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="febd5-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="febd5-108">DESCRIPTION</span></span>
<span data-ttu-id="febd5-109">A **Get-AzureRmSiteRecoveryPolicy** parancsmag a beállított Azure-webhely-helyreállítási védelmi házirendek listáját, illetve egy bizonyos védelmi házirendet tartalmaz a név szerint.</span><span class="sxs-lookup"><span data-stu-id="febd5-109">The **Get-AzureRmSiteRecoveryPolicy** cmdlet gets the list of configured Azure Site Recovery protection policies or a specific protection policy by name.</span></span>

## <span data-ttu-id="febd5-110">Példák</span><span class="sxs-lookup"><span data-stu-id="febd5-110">EXAMPLES</span></span>

## <span data-ttu-id="febd5-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="febd5-111">PARAMETERS</span></span>

### <span data-ttu-id="febd5-112">-Típusú megjelenített</span><span class="sxs-lookup"><span data-stu-id="febd5-112">-FriendlyName</span></span>
<span data-ttu-id="febd5-113">A webhely-helyreállítási replikációs házirend rövid nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="febd5-113">Specifies the friendly name of the Site Recovery replication policy.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="febd5-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="febd5-114">-Name</span></span>
<span data-ttu-id="febd5-115">A webhely-helyreállítási replikációs házirend nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="febd5-115">Specifies the name of the Site Recovery replication policy.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="febd5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="febd5-116">-DefaultProfile</span></span>
<span data-ttu-id="febd5-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="febd5-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="febd5-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="febd5-118">CommonParameters</span></span>
<span data-ttu-id="febd5-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="febd5-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="febd5-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="febd5-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="febd5-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="febd5-121">INPUTS</span></span>

## <span data-ttu-id="febd5-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="febd5-122">OUTPUTS</span></span>

### <span data-ttu-id="febd5-123">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. commands. SiteRecovery. ASRPolicy]</span><span class="sxs-lookup"><span data-stu-id="febd5-123">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRPolicy]</span></span>

## <span data-ttu-id="febd5-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="febd5-124">NOTES</span></span>

## <span data-ttu-id="febd5-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="febd5-125">RELATED LINKS</span></span>

[<span data-ttu-id="febd5-126">Új – AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="febd5-126">New-AzureRmSiteRecoveryPolicy</span></span>](./New-AzureRmSiteRecoveryPolicy.md)

[<span data-ttu-id="febd5-127">Remove-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="febd5-127">Remove-AzureRmSiteRecoveryPolicy</span></span>](./Remove-AzureRmSiteRecoveryPolicy.md)
