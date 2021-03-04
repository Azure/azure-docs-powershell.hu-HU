---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/get-aztenant
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzTenant.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzTenant.md
ms.openlocfilehash: 4ef371f26eeca71edda42a6aca5e7d5ad28fe753
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101920130"
---
# <span data-ttu-id="7825d-101">Get-AzTenant</span><span class="sxs-lookup"><span data-stu-id="7825d-101">Get-AzTenant</span></span>

## <span data-ttu-id="7825d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7825d-102">SYNOPSIS</span></span>
<span data-ttu-id="7825d-103">Az aktuális felhasználóhoz engedélyezett bérlőket kapja meg.</span><span class="sxs-lookup"><span data-stu-id="7825d-103">Gets tenants that are authorized for the current user.</span></span>

## <span data-ttu-id="7825d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7825d-104">SYNTAX</span></span>

```
Get-AzTenant [[-TenantId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7825d-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7825d-105">DESCRIPTION</span></span>
<span data-ttu-id="7825d-106">A Get-AzTenant parancsmag az aktuális felhasználó számára engedélyezett bérlőket kap.</span><span class="sxs-lookup"><span data-stu-id="7825d-106">The Get-AzTenant cmdlet gets tenants authorized for the current user.</span></span>

## <span data-ttu-id="7825d-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7825d-107">EXAMPLES</span></span>

### <span data-ttu-id="7825d-108">1. példa: Az összes bérlő beszerzése</span><span class="sxs-lookup"><span data-stu-id="7825d-108">Example 1: Getting all tenants</span></span>
```
PS C:\> Connect-AzAccount
PS C:\> Get-AzTenant

Id                                   Name        Category Domains
--                                   ----------- -------- -------
xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Microsoft   Home     {test0.com, test1.com, test2.microsoft.com, test3.microsoft.com...}
yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy Testhost    Home     testhost.onmicrosoft.com
```

<span data-ttu-id="7825d-109">Ez a példa azt mutatja be, hogy miként szerezheti be egy Azure-fiók összes engedélyezett bérlői webhelyét.</span><span class="sxs-lookup"><span data-stu-id="7825d-109">This example shows how to get all of the authorized tenants of an Azure account.</span></span>

### <span data-ttu-id="7825d-110">2. példa: Egy adott bérlő lekérte</span><span class="sxs-lookup"><span data-stu-id="7825d-110">Example 2: Getting a specific tenant</span></span>
```
PS C:\> Connect-AzAccount
PS C:\> Get-AzTenant -TenantId xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx

Id                                   Name        Category Domains
--                                   ----------- -------- -------
xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Microsoft   Home     {test0.com, test1.com, test2.microsoft.com, test3.microsoft.com...}
```

<span data-ttu-id="7825d-111">Ebben a példában azt mutatjuk be, hogy miként lehet azure-fiókhoz egy adott engedélyezett bérlői fiókot szerezni.</span><span class="sxs-lookup"><span data-stu-id="7825d-111">This example shows how to get a specific authorized tenant of an Azure account.</span></span>

## <span data-ttu-id="7825d-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7825d-112">PARAMETERS</span></span>

### <span data-ttu-id="7825d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7825d-113">-DefaultProfile</span></span>
<span data-ttu-id="7825d-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="7825d-114">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7825d-115">-TenantId</span><span class="sxs-lookup"><span data-stu-id="7825d-115">-TenantId</span></span>
<span data-ttu-id="7825d-116">Annak a bérlőnek az azonosítóját adja meg, amelybe a parancsmagot be kapja.</span><span class="sxs-lookup"><span data-stu-id="7825d-116">Specifies the ID of the tenant that this cmdlet gets.</span></span>

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

### <span data-ttu-id="7825d-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7825d-117">CommonParameters</span></span>
<span data-ttu-id="7825d-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7825d-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7825d-119">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7825d-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7825d-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7825d-120">INPUTS</span></span>

### <span data-ttu-id="7825d-121">System.String</span><span class="sxs-lookup"><span data-stu-id="7825d-121">System.String</span></span>

## <span data-ttu-id="7825d-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7825d-122">OUTPUTS</span></span>

### <span data-ttu-id="7825d-123">Microsoft.Azure.Commands.Profile.Models.PSAzureTenant</span><span class="sxs-lookup"><span data-stu-id="7825d-123">Microsoft.Azure.Commands.Profile.Models.PSAzureTenant</span></span>

## <span data-ttu-id="7825d-124">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7825d-124">NOTES</span></span>

## <span data-ttu-id="7825d-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7825d-125">RELATED LINKS</span></span>
