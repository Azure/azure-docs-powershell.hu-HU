---
external help file: ''
Module Name: Azs.Subscriptions
online version: https://docs.microsoft.com/powershell/module/azs.subscriptions/get-azsoffer
schema: 2.0.0
ms.openlocfilehash: 7b2fcb224486915e78bdd90a84941ac0207a45c3
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/24/2020
ms.locfileid: "94015334"
---
# <span data-ttu-id="d2032-101">Get-AzsOffer</span><span class="sxs-lookup"><span data-stu-id="d2032-101">Get-AzsOffer</span></span>

## <span data-ttu-id="d2032-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d2032-102">SYNOPSIS</span></span>
<span data-ttu-id="d2032-103">A legfelső szintű szolgáltató nyilvános ajánlatok listájának beszerzése.</span><span class="sxs-lookup"><span data-stu-id="d2032-103">Get the list of public offers for the root provider.</span></span>

## <span data-ttu-id="d2032-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d2032-104">SYNTAX</span></span>

```
Get-AzsOffer [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="d2032-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d2032-105">DESCRIPTION</span></span>
<span data-ttu-id="d2032-106">A legfelső szintű szolgáltató nyilvános ajánlatok listájának beszerzése.</span><span class="sxs-lookup"><span data-stu-id="d2032-106">Get the list of public offers for the root provider.</span></span>

## <span data-ttu-id="d2032-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d2032-107">EXAMPLES</span></span>

### <span data-ttu-id="d2032-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d2032-108">Example 1</span></span>
```powershell
PS C:\> Get-AzsOffer | fl *

Description : 
DisplayName : TestOffer-fef68214-ba47-469c-89a7-07faf7947ad6
Id          : /delegatedProviders/default/offers/TestOffer-fef68214-ba47-469c-89a7-07faf7947ad6
Name        : TestOffer-fef68214-ba47-469c-89a7-07faf7947ad6

Description : 
DisplayName : TestOffer-8322dc27-47a0-4446-89a0-eb5a0ec3b12b
Id          : /delegatedProviders/default/offers/TestOffer-8322dc27-47a0-4446-89a0-eb5a0ec3b12b
Name        : TestOffer-8322dc27-47a0-4446-89a0-eb5a0ec3b12b
```

<span data-ttu-id="d2032-109">A nyilvános ajánlatok listájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="d2032-109">Get the list of public offers</span></span>

## <span data-ttu-id="d2032-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d2032-110">PARAMETERS</span></span>

### <span data-ttu-id="d2032-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2032-111">-DefaultProfile</span></span>
<span data-ttu-id="d2032-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d2032-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d2032-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2032-113">CommonParameters</span></span>
<span data-ttu-id="d2032-114">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d2032-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2032-115">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d2032-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2032-116">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d2032-116">INPUTS</span></span>

## <span data-ttu-id="d2032-117">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d2032-117">OUTPUTS</span></span>

### <span data-ttu-id="d2032-118">Microsoft. Azure. PowerShell. parancsmagok. előfizetés. models. Api20151101. IOffer</span><span class="sxs-lookup"><span data-stu-id="d2032-118">Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.Api20151101.IOffer</span></span>



## <span data-ttu-id="d2032-119">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d2032-119">NOTES</span></span>

## <span data-ttu-id="d2032-120">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d2032-120">RELATED LINKS</span></span>

