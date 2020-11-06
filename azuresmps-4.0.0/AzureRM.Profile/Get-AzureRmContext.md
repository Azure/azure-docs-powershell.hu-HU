---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 914b75e3952f7841aaf3ff505f51f7b4ebdc6044
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491171"
---
# <span data-ttu-id="ee7b6-101">Get-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="ee7b6-101">Get-AzureRmContext</span></span>

## <span data-ttu-id="ee7b6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ee7b6-102">SYNOPSIS</span></span>
<span data-ttu-id="ee7b6-103">Az Azure Resource Manager-kérések hitelesítéséhez használt metaadatot kapja meg.</span><span class="sxs-lookup"><span data-stu-id="ee7b6-103">Gets the metadata used to authenticate Azure Resource Manager requests.</span></span>

## <span data-ttu-id="ee7b6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ee7b6-104">SYNTAX</span></span>

```
Get-AzureRmContext [<CommonParameters>]
```

## <span data-ttu-id="ee7b6-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ee7b6-105">DESCRIPTION</span></span>
<span data-ttu-id="ee7b6-106">A Get-AzureRmContext parancsmag az Azure Resource Manager-kérések hitelesítéséhez használt jelenlegi metaadatot kapja meg.</span><span class="sxs-lookup"><span data-stu-id="ee7b6-106">The Get-AzureRmContext cmdlet gets the current metadata used to authenticate Azure Resource Manager requests.</span></span>

<span data-ttu-id="ee7b6-107">Ez a parancsmag az Active Directory-fiókot, az Active Directory-bérlőt, az Azure-előfizetést és a célzott Azure-környezetet kapja meg.</span><span class="sxs-lookup"><span data-stu-id="ee7b6-107">This cmdlet gets the Active Directory account, Active Directory tenant, Azure subscription, and the targeted Azure environment.</span></span>
<span data-ttu-id="ee7b6-108">Az Azure Resource Manager-parancsmagok alapértelmezés szerint ezeket a beállításokat használják az Azure Resource Manager-kérések készítésekor.</span><span class="sxs-lookup"><span data-stu-id="ee7b6-108">Azure Resource Manager cmdlets use these settings by default when making Azure Resource Manager requests.</span></span>

## <span data-ttu-id="ee7b6-109">Példák</span><span class="sxs-lookup"><span data-stu-id="ee7b6-109">EXAMPLES</span></span>

### <span data-ttu-id="ee7b6-110">Példa 1: a jelenlegi környezet beszerzése</span><span class="sxs-lookup"><span data-stu-id="ee7b6-110">Example 1: Getting the current context</span></span>
```
PS C:\> Add-AzureRmAccount
PS C:\> Get-AzureRmContext

Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :
```

<span data-ttu-id="ee7b6-111">Ebben a példában egy Azure-előfizetéssel jelentkezik be a fiókba a AzureRmAccount használatával, és az aktuális munkamenet kontextusát a Get-AzureRmContext.</span><span class="sxs-lookup"><span data-stu-id="ee7b6-111">In this example we are logging into our account with an Azure subscription using Add-AzureRmAccount, and then we are getting the context of the current session by calling Get-AzureRmContext.</span></span>

## <span data-ttu-id="ee7b6-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ee7b6-112">PARAMETERS</span></span>

### <span data-ttu-id="ee7b6-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee7b6-113">CommonParameters</span></span>
<span data-ttu-id="ee7b6-114">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ee7b6-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee7b6-115">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee7b6-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee7b6-116">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ee7b6-116">INPUTS</span></span>

## <span data-ttu-id="ee7b6-117">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ee7b6-117">OUTPUTS</span></span>

### <span data-ttu-id="ee7b6-118">PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="ee7b6-118">PSAzureContext</span></span>
<span data-ttu-id="ee7b6-119">Ez a parancsmag az Azure Resource Manager-parancsmagok által használt fiókot, bérlőt és előfizetést számítja ki.</span><span class="sxs-lookup"><span data-stu-id="ee7b6-119">This cmdlet returns the account, tenant, and subscription used by Azure Resource Manager cmdlets.</span></span>

## <span data-ttu-id="ee7b6-120">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ee7b6-120">NOTES</span></span>

## <span data-ttu-id="ee7b6-121">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ee7b6-121">RELATED LINKS</span></span>

[<span data-ttu-id="ee7b6-122">Set-AzureRMContext</span><span class="sxs-lookup"><span data-stu-id="ee7b6-122">Set-AzureRMContext</span></span>]()

