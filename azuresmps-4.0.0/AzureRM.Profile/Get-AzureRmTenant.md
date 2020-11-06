---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2cabb88c490c7fdea56fd5ffde280cfd55bc8f3d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491164"
---
# <span data-ttu-id="6a891-101">Get-AzureRmTenant</span><span class="sxs-lookup"><span data-stu-id="6a891-101">Get-AzureRmTenant</span></span>

## <span data-ttu-id="6a891-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6a891-102">SYNOPSIS</span></span>
<span data-ttu-id="6a891-103">Az aktuális felhasználótól kapott bérlői fiókokat kapja.</span><span class="sxs-lookup"><span data-stu-id="6a891-103">Gets tenants that are authorized for the current user.</span></span>

## <span data-ttu-id="6a891-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6a891-104">SYNTAX</span></span>

```
Get-AzureRmTenant [[-TenantId] <String>] [<CommonParameters>]
```

## <span data-ttu-id="6a891-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6a891-105">DESCRIPTION</span></span>
<span data-ttu-id="6a891-106">A Get-AzureRmTenant parancsmag az aktuális felhasználóhoz tartozó bérlői fiókokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="6a891-106">The Get-AzureRmTenant cmdlet gets tenants authorized for the current user.</span></span>

## <span data-ttu-id="6a891-107">Példák</span><span class="sxs-lookup"><span data-stu-id="6a891-107">EXAMPLES</span></span>

### <span data-ttu-id="6a891-108">Példa 1: az összes bérlő beszerzése</span><span class="sxs-lookup"><span data-stu-id="6a891-108">Example 1: Getting all tenants</span></span>
```
PS C:\> Add-AzureRmAccount
PS C:\> Get-AzureRmTenant

TenantId : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Domain   : microsoft.com

TenantId : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Domain   : microsoft.com
```

<span data-ttu-id="6a891-109">Ebben a példában bemutatjuk, hogy miként szerezheti be az Azure-fiókok összes hivatalos bérlőjét.</span><span class="sxs-lookup"><span data-stu-id="6a891-109">This example shows how to get all of the authorized tenants of an Azure account.</span></span>

### <span data-ttu-id="6a891-110">2. példa: adott bérlő beszerzése</span><span class="sxs-lookup"><span data-stu-id="6a891-110">Example 2: Getting a specific tenant</span></span>
```
PS C:\> Add-AzureRmAccount
PS C:\> Get-AzureRmTenant -TenantId xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx

TenantId : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Domain   : microsoft.com
```

<span data-ttu-id="6a891-111">Ebben a példában bemutatjuk, hogyan lehet egy Azure-fiók meghatalmazott bérlői fiókját beszerezni.</span><span class="sxs-lookup"><span data-stu-id="6a891-111">This example shows how to get a specific authorized tenant of an Azure account.</span></span>

## <span data-ttu-id="6a891-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6a891-112">PARAMETERS</span></span>

### <span data-ttu-id="6a891-113">-Bérlői azonosító megkeresése</span><span class="sxs-lookup"><span data-stu-id="6a891-113">-TenantId</span></span>
<span data-ttu-id="6a891-114">Annak a bérlőnek az AZONOSÍTÓját adja meg, akinek a parancsmagja van.</span><span class="sxs-lookup"><span data-stu-id="6a891-114">Specifies the ID of the tenant that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Domain, Tenant

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a891-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a891-115">CommonParameters</span></span>
<span data-ttu-id="6a891-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6a891-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a891-117">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a891-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a891-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6a891-118">INPUTS</span></span>

## <span data-ttu-id="6a891-119">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6a891-119">OUTPUTS</span></span>

### <span data-ttu-id="6a891-120">PSAzureTenant</span><span class="sxs-lookup"><span data-stu-id="6a891-120">PSAzureTenant</span></span>
<span data-ttu-id="6a891-121">Ez a parancsmag a bérlői azonosítót és a kapcsolódó tartomány adatait számítja ki az aktuális fiókhoz engedélyezett bérlői fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="6a891-121">This cmdlet returns the tenant ID and associated domain information for tenants authorized for the current account.</span></span>

## <span data-ttu-id="6a891-122">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6a891-122">NOTES</span></span>

## <span data-ttu-id="6a891-123">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6a891-123">RELATED LINKS</span></span>

