---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-aztenant
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzTenant.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzTenant.md
ms.openlocfilehash: 936eb5bb7f49c2530a325b3bfa8c369b8f097711
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183419"
---
# <span data-ttu-id="2e734-101">Get-AzTenant</span><span class="sxs-lookup"><span data-stu-id="2e734-101">Get-AzTenant</span></span>

## <span data-ttu-id="2e734-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2e734-102">SYNOPSIS</span></span>
<span data-ttu-id="2e734-103">Az aktuális felhasználótól kapott bérlői fiókokat kapja.</span><span class="sxs-lookup"><span data-stu-id="2e734-103">Gets tenants that are authorized for the current user.</span></span>

## <span data-ttu-id="2e734-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2e734-104">SYNTAX</span></span>

```
Get-AzTenant [[-TenantId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2e734-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2e734-105">DESCRIPTION</span></span>
<span data-ttu-id="2e734-106">A Get-AzTenant parancsmag az aktuális felhasználóhoz tartozó bérlői fiókokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="2e734-106">The Get-AzTenant cmdlet gets tenants authorized for the current user.</span></span>

## <span data-ttu-id="2e734-107">Példák</span><span class="sxs-lookup"><span data-stu-id="2e734-107">EXAMPLES</span></span>

### <span data-ttu-id="2e734-108">Példa 1: az összes bérlő beszerzése</span><span class="sxs-lookup"><span data-stu-id="2e734-108">Example 1: Getting all tenants</span></span>
```
PS C:\> Connect-AzAccount
PS C:\> Get-AzTenant

Id                                   Name        Category Domains
--                                   ----------- -------- -------
xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Microsoft   Home     {test0.com, test1.com, test2.microsoft.com, test3.microsoft.com...}
yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy Testhost    Home     testhost.onmicrosoft.com
```

<span data-ttu-id="2e734-109">Ebben a példában bemutatjuk, hogy miként szerezheti be az Azure-fiókok összes hivatalos bérlőjét.</span><span class="sxs-lookup"><span data-stu-id="2e734-109">This example shows how to get all of the authorized tenants of an Azure account.</span></span>

### <span data-ttu-id="2e734-110">2. példa: adott bérlő beszerzése</span><span class="sxs-lookup"><span data-stu-id="2e734-110">Example 2: Getting a specific tenant</span></span>
```
PS C:\> Connect-AzAccount
PS C:\> Get-AzTenant -TenantId xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx

Id                                   Name        Category Domains
--                                   ----------- -------- -------
xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Microsoft   Home     {test0.com, test1.com, test2.microsoft.com, test3.microsoft.com...}
```

<span data-ttu-id="2e734-111">Ebben a példában bemutatjuk, hogyan lehet egy Azure-fiók meghatalmazott bérlői fiókját beszerezni.</span><span class="sxs-lookup"><span data-stu-id="2e734-111">This example shows how to get a specific authorized tenant of an Azure account.</span></span>

## <span data-ttu-id="2e734-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2e734-112">PARAMETERS</span></span>

### <span data-ttu-id="2e734-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e734-113">-DefaultProfile</span></span>
<span data-ttu-id="2e734-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="2e734-114">The credentials, tenant and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e734-115">-Bérlői azonosító megkeresése</span><span class="sxs-lookup"><span data-stu-id="2e734-115">-TenantId</span></span>
<span data-ttu-id="2e734-116">Annak a bérlőnek az AZONOSÍTÓját adja meg, akinek a parancsmagja van.</span><span class="sxs-lookup"><span data-stu-id="2e734-116">Specifies the ID of the tenant that this cmdlet gets.</span></span>

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

### <span data-ttu-id="2e734-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e734-117">CommonParameters</span></span>
<span data-ttu-id="2e734-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2e734-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e734-119">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e734-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e734-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2e734-120">INPUTS</span></span>

### <span data-ttu-id="2e734-121">System. String</span><span class="sxs-lookup"><span data-stu-id="2e734-121">System.String</span></span>

## <span data-ttu-id="2e734-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2e734-122">OUTPUTS</span></span>

### <span data-ttu-id="2e734-123">Microsoft. Azure. Command. profil. models. PSAzureTenant</span><span class="sxs-lookup"><span data-stu-id="2e734-123">Microsoft.Azure.Commands.Profile.Models.PSAzureTenant</span></span>

## <span data-ttu-id="2e734-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2e734-124">NOTES</span></span>

## <span data-ttu-id="2e734-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2e734-125">RELATED LINKS</span></span>
