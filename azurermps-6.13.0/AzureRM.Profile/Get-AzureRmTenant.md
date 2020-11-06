---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/get-azurermtenant
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmTenant.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmTenant.md
ms.openlocfilehash: 1d5312cfaf7afb96149ae00b0e7900905206fb3d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495787"
---
# <span data-ttu-id="22b4c-101">Get-AzureRmTenant</span><span class="sxs-lookup"><span data-stu-id="22b4c-101">Get-AzureRmTenant</span></span>

## <span data-ttu-id="22b4c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="22b4c-102">SYNOPSIS</span></span>
<span data-ttu-id="22b4c-103">Az aktuális felhasználótól kapott bérlői fiókokat kapja.</span><span class="sxs-lookup"><span data-stu-id="22b4c-103">Gets tenants that are authorized for the current user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="22b4c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="22b4c-104">SYNTAX</span></span>

```
Get-AzureRmTenant [[-TenantId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="22b4c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="22b4c-105">DESCRIPTION</span></span>
<span data-ttu-id="22b4c-106">A Get-AzureRmTenant parancsmag az aktuális felhasználóhoz tartozó bérlői fiókokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="22b4c-106">The Get-AzureRmTenant cmdlet gets tenants authorized for the current user.</span></span>

## <span data-ttu-id="22b4c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="22b4c-107">EXAMPLES</span></span>

### <span data-ttu-id="22b4c-108">Példa 1: az összes bérlő beszerzése</span><span class="sxs-lookup"><span data-stu-id="22b4c-108">Example 1: Getting all tenants</span></span>
```
PS C:\> Connect-AzureRmAccount
PS C:\> Get-AzureRmTenant

Id                                   Directory
--                                   ---------
xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx microsoft.com
yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy microsoft.com
```

<span data-ttu-id="22b4c-109">Ebben a példában bemutatjuk, hogy miként szerezheti be az Azure-fiókok összes hivatalos bérlőjét.</span><span class="sxs-lookup"><span data-stu-id="22b4c-109">This example shows how to get all of the authorized tenants of an Azure account.</span></span>

### <span data-ttu-id="22b4c-110">2. példa: adott bérlő beszerzése</span><span class="sxs-lookup"><span data-stu-id="22b4c-110">Example 2: Getting a specific tenant</span></span>
```
PS C:\> Connect-AzureRmAccount
PS C:\> Get-AzureRmTenant -TenantId xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx

Id                                   Directory
--                                   ---------
xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx microsoft.com
```

<span data-ttu-id="22b4c-111">Ebben a példában bemutatjuk, hogyan lehet egy Azure-fiók meghatalmazott bérlői fiókját beszerezni.</span><span class="sxs-lookup"><span data-stu-id="22b4c-111">This example shows how to get a specific authorized tenant of an Azure account.</span></span>

## <span data-ttu-id="22b4c-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="22b4c-112">PARAMETERS</span></span>

### <span data-ttu-id="22b4c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22b4c-113">-DefaultProfile</span></span>
<span data-ttu-id="22b4c-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="22b4c-114">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="22b4c-115">-Bérlői azonosító megkeresése</span><span class="sxs-lookup"><span data-stu-id="22b4c-115">-TenantId</span></span>
<span data-ttu-id="22b4c-116">Annak a bérlőnek az AZONOSÍTÓját adja meg, akinek a parancsmagja van.</span><span class="sxs-lookup"><span data-stu-id="22b4c-116">Specifies the ID of the tenant that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Domain, Tenant

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22b4c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22b4c-117">CommonParameters</span></span>
<span data-ttu-id="22b4c-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="22b4c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22b4c-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22b4c-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22b4c-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="22b4c-120">INPUTS</span></span>

### <span data-ttu-id="22b4c-121">System. String</span><span class="sxs-lookup"><span data-stu-id="22b4c-121">System.String</span></span>

## <span data-ttu-id="22b4c-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="22b4c-122">OUTPUTS</span></span>

### <span data-ttu-id="22b4c-123">Microsoft. Azure. Command. profil. models. PSAzureTenant</span><span class="sxs-lookup"><span data-stu-id="22b4c-123">Microsoft.Azure.Commands.Profile.Models.PSAzureTenant</span></span>

## <span data-ttu-id="22b4c-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="22b4c-124">NOTES</span></span>

## <span data-ttu-id="22b4c-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="22b4c-125">RELATED LINKS</span></span>
