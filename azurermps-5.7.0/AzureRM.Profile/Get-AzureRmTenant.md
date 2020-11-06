---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/get-azurermtenant
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmTenant.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmTenant.md
ms.openlocfilehash: 7d9687877e3a27d175719a7a7b9ec6c78a529e52
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500476"
---
# <span data-ttu-id="fbfa9-101">Get-AzureRmTenant</span><span class="sxs-lookup"><span data-stu-id="fbfa9-101">Get-AzureRmTenant</span></span>

## <span data-ttu-id="fbfa9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fbfa9-102">SYNOPSIS</span></span>
<span data-ttu-id="fbfa9-103">Az aktuális felhasználótól kapott bérlői fiókokat kapja.</span><span class="sxs-lookup"><span data-stu-id="fbfa9-103">Gets tenants that are authorized for the current user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fbfa9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fbfa9-104">SYNTAX</span></span>

```
Get-AzureRmTenant [[-TenantId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fbfa9-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="fbfa9-105">DESCRIPTION</span></span>
<span data-ttu-id="fbfa9-106">A Get-AzureRmTenant parancsmag az aktuális felhasználóhoz tartozó bérlői fiókokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="fbfa9-106">The Get-AzureRmTenant cmdlet gets tenants authorized for the current user.</span></span>

## <span data-ttu-id="fbfa9-107">Példák</span><span class="sxs-lookup"><span data-stu-id="fbfa9-107">EXAMPLES</span></span>

### <span data-ttu-id="fbfa9-108">Példa 1: az összes bérlő beszerzése</span><span class="sxs-lookup"><span data-stu-id="fbfa9-108">Example 1: Getting all tenants</span></span>
```
PS C:\> Connect-AzureRmAccount
PS C:\> Get-AzureRmTenant

TenantId : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Domain   : microsoft.com

TenantId : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Domain   : microsoft.com
```

<span data-ttu-id="fbfa9-109">Ebben a példában bemutatjuk, hogy miként szerezheti be az Azure-fiókok összes hivatalos bérlőjét.</span><span class="sxs-lookup"><span data-stu-id="fbfa9-109">This example shows how to get all of the authorized tenants of an Azure account.</span></span>

### <span data-ttu-id="fbfa9-110">2. példa: adott bérlő beszerzése</span><span class="sxs-lookup"><span data-stu-id="fbfa9-110">Example 2: Getting a specific tenant</span></span>
```
PS C:\> Connect-AzureRmAccount
PS C:\> Get-AzureRmTenant -TenantId xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx

TenantId : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Domain   : microsoft.com
```

<span data-ttu-id="fbfa9-111">Ebben a példában bemutatjuk, hogyan lehet egy Azure-fiók meghatalmazott bérlői fiókját beszerezni.</span><span class="sxs-lookup"><span data-stu-id="fbfa9-111">This example shows how to get a specific authorized tenant of an Azure account.</span></span>

## <span data-ttu-id="fbfa9-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fbfa9-112">PARAMETERS</span></span>

### <span data-ttu-id="fbfa9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbfa9-113">-DefaultProfile</span></span>
<span data-ttu-id="fbfa9-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="fbfa9-114">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fbfa9-115">-Bérlői azonosító megkeresése</span><span class="sxs-lookup"><span data-stu-id="fbfa9-115">-TenantId</span></span>
<span data-ttu-id="fbfa9-116">Annak a bérlőnek az AZONOSÍTÓját adja meg, akinek a parancsmagja van.</span><span class="sxs-lookup"><span data-stu-id="fbfa9-116">Specifies the ID of the tenant that this cmdlet gets.</span></span>

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

### <span data-ttu-id="fbfa9-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbfa9-117">CommonParameters</span></span>
<span data-ttu-id="fbfa9-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fbfa9-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbfa9-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fbfa9-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbfa9-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fbfa9-120">INPUTS</span></span>

### <span data-ttu-id="fbfa9-121">Nincs</span><span class="sxs-lookup"><span data-stu-id="fbfa9-121">None</span></span>
<span data-ttu-id="fbfa9-122">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="fbfa9-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fbfa9-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fbfa9-123">OUTPUTS</span></span>

### <span data-ttu-id="fbfa9-124">PSAzureTenant</span><span class="sxs-lookup"><span data-stu-id="fbfa9-124">PSAzureTenant</span></span>
<span data-ttu-id="fbfa9-125">Ez a parancsmag a bérlői azonosítót és a kapcsolódó tartomány adatait számítja ki az aktuális fiókhoz engedélyezett bérlői fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="fbfa9-125">This cmdlet returns the tenant ID and associated domain information for tenants authorized for the current account.</span></span>

## <span data-ttu-id="fbfa9-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fbfa9-126">NOTES</span></span>

## <span data-ttu-id="fbfa9-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fbfa9-127">RELATED LINKS</span></span>

