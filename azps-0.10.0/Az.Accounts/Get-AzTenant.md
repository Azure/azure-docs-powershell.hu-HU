---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-aztenant
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Get-AzTenant.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Get-AzTenant.md
ms.openlocfilehash: 4465ee73eba81f2973e3fbb5787c74fa7b3b63e9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841049"
---
# <span data-ttu-id="97a32-101">Get-AzTenant</span><span class="sxs-lookup"><span data-stu-id="97a32-101">Get-AzTenant</span></span>

## <span data-ttu-id="97a32-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="97a32-102">SYNOPSIS</span></span>
<span data-ttu-id="97a32-103">Az aktuális felhasználótól kapott bérlői fiókokat kapja.</span><span class="sxs-lookup"><span data-stu-id="97a32-103">Gets tenants that are authorized for the current user.</span></span>

## <span data-ttu-id="97a32-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="97a32-104">SYNTAX</span></span>

```
Get-AzTenant [[-TenantId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="97a32-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="97a32-105">DESCRIPTION</span></span>
<span data-ttu-id="97a32-106">A Get-AzTenant parancsmag az aktuális felhasználóhoz tartozó bérlői fiókokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="97a32-106">The Get-AzTenant cmdlet gets tenants authorized for the current user.</span></span>

## <span data-ttu-id="97a32-107">Példák</span><span class="sxs-lookup"><span data-stu-id="97a32-107">EXAMPLES</span></span>

### <span data-ttu-id="97a32-108">Példa 1: az összes bérlő beszerzése</span><span class="sxs-lookup"><span data-stu-id="97a32-108">Example 1: Getting all tenants</span></span>
```
PS C:\> Connect-AzAccount
PS C:\> Get-AzTenant

Id                                   Directory
--                                   ---------
xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx microsoft.com
yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy microsoft.com
```

<span data-ttu-id="97a32-109">Ebben a példában bemutatjuk, hogy miként szerezheti be az Azure-fiókok összes hivatalos bérlőjét.</span><span class="sxs-lookup"><span data-stu-id="97a32-109">This example shows how to get all of the authorized tenants of an Azure account.</span></span>

### <span data-ttu-id="97a32-110">2. példa: adott bérlő beszerzése</span><span class="sxs-lookup"><span data-stu-id="97a32-110">Example 2: Getting a specific tenant</span></span>
```
PS C:\> Connect-AzAccount
PS C:\> Get-AzTenant -TenantId xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx

Id                                   Directory
--                                   ---------
xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx microsoft.com
```

<span data-ttu-id="97a32-111">Ebben a példában bemutatjuk, hogyan lehet egy Azure-fiók meghatalmazott bérlői fiókját beszerezni.</span><span class="sxs-lookup"><span data-stu-id="97a32-111">This example shows how to get a specific authorized tenant of an Azure account.</span></span>

## <span data-ttu-id="97a32-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="97a32-112">PARAMETERS</span></span>

### <span data-ttu-id="97a32-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97a32-113">-DefaultProfile</span></span>
<span data-ttu-id="97a32-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="97a32-114">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="97a32-115">-Bérlői azonosító megkeresése</span><span class="sxs-lookup"><span data-stu-id="97a32-115">-TenantId</span></span>
<span data-ttu-id="97a32-116">Annak a bérlőnek az AZONOSÍTÓját adja meg, akinek a parancsmagja van.</span><span class="sxs-lookup"><span data-stu-id="97a32-116">Specifies the ID of the tenant that this cmdlet gets.</span></span>

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

### <span data-ttu-id="97a32-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97a32-117">CommonParameters</span></span>
<span data-ttu-id="97a32-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="97a32-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97a32-119">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="97a32-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97a32-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="97a32-120">INPUTS</span></span>

### <span data-ttu-id="97a32-121">System. String</span><span class="sxs-lookup"><span data-stu-id="97a32-121">System.String</span></span>

## <span data-ttu-id="97a32-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="97a32-122">OUTPUTS</span></span>

### <span data-ttu-id="97a32-123">Microsoft. Azure. Command. profil. models. PSAzureTenant</span><span class="sxs-lookup"><span data-stu-id="97a32-123">Microsoft.Azure.Commands.Profile.Models.PSAzureTenant</span></span>

## <span data-ttu-id="97a32-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="97a32-124">NOTES</span></span>

## <span data-ttu-id="97a32-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="97a32-125">RELATED LINKS</span></span>
