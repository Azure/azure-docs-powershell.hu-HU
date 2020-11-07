---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 7C15B0AA-D97E-4715-9AD4-971731527D09
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVault.md
ms.openlocfilehash: 37e0096dd6f279c13909f1b542e603faebfd1e97
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679326"
---
# <span data-ttu-id="4ad61-101">Get-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="4ad61-101">Get-AzureRmSiteRecoveryVault</span></span>

## <span data-ttu-id="4ad61-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4ad61-102">SYNOPSIS</span></span>
<span data-ttu-id="4ad61-103">Webhely-helyreállítási boltozatokat kap a jelenlegi előfizetésből.</span><span class="sxs-lookup"><span data-stu-id="4ad61-103">Gets Site Recovery vaults from the current subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4ad61-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4ad61-104">SYNTAX</span></span>

```
Get-AzureRmSiteRecoveryVault [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4ad61-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4ad61-105">DESCRIPTION</span></span>
<span data-ttu-id="4ad61-106">A **Get-AzureRmSiteRecoveryVault** parancsmag a jelenlegi előfizetésből kapja meg az Azure webhelyek helyreállítási boltozatai vagy egy bizonyos webhely-helyreállítási tároló listáját.</span><span class="sxs-lookup"><span data-stu-id="4ad61-106">The **Get-AzureRmSiteRecoveryVault** cmdlet gets a list of Azure Site Recovery vaults or a specific Site Recovery vault from the current subscription.</span></span>

## <span data-ttu-id="4ad61-107">Példák</span><span class="sxs-lookup"><span data-stu-id="4ad61-107">EXAMPLES</span></span>

## <span data-ttu-id="4ad61-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4ad61-108">PARAMETERS</span></span>

### <span data-ttu-id="4ad61-109">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4ad61-109">-Name</span></span>
<span data-ttu-id="4ad61-110">A boltozat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4ad61-110">Specifies the name of the vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ad61-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ad61-111">-ResourceGroupName</span></span>
<span data-ttu-id="4ad61-112">Annak az Azure erőforrás-csoportnak a nevét adja meg, amelyből a helyreállítási szolgáltatások objektumot be szeretné szerezni.</span><span class="sxs-lookup"><span data-stu-id="4ad61-112">Specifies the name of the Azure resource group from which to get the recovery services object.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ad61-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ad61-113">-DefaultProfile</span></span>
<span data-ttu-id="4ad61-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4ad61-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4ad61-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ad61-115">CommonParameters</span></span>
<span data-ttu-id="4ad61-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4ad61-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ad61-117">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ad61-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ad61-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4ad61-118">INPUTS</span></span>

## <span data-ttu-id="4ad61-119">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4ad61-119">OUTPUTS</span></span>

### <span data-ttu-id="4ad61-120">System. Collections. Generic. list ' 1 [Microsoft. Azure. commands. SiteRecovery. ASRVault]</span><span class="sxs-lookup"><span data-stu-id="4ad61-120">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.SiteRecovery.ASRVault]</span></span>

## <span data-ttu-id="4ad61-121">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4ad61-121">NOTES</span></span>

## <span data-ttu-id="4ad61-122">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4ad61-122">RELATED LINKS</span></span>

[<span data-ttu-id="4ad61-123">Új – AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="4ad61-123">New-AzureRmSiteRecoveryVault</span></span>](./New-AzureRmSiteRecoveryVault.md)

[<span data-ttu-id="4ad61-124">Remove-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="4ad61-124">Remove-AzureRmSiteRecoveryVault</span></span>](./Remove-AzureRmSiteRecoveryVault.md)
