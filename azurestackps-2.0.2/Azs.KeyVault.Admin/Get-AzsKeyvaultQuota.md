---
external help file: ''
Module Name: Azs.KeyVault.Admin
online version: https://docs.microsoft.com/powershell/module/azs.keyvault.admin/get-azskeyvaultquota
schema: 2.0.0
ms.openlocfilehash: 813e0e7dc2535b3c7cd424e55ff924c380d84e2f
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94017102"
---
# <span data-ttu-id="8d6c4-101">Get-AzsKeyvaultQuota</span><span class="sxs-lookup"><span data-stu-id="8d6c4-101">Get-AzsKeyvaultQuota</span></span>

## <span data-ttu-id="8d6c4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8d6c4-102">SYNOPSIS</span></span>
<span data-ttu-id="8d6c4-103">A "minden" lemezkvóta-objektum listája az adott helyen.</span><span class="sxs-lookup"><span data-stu-id="8d6c4-103">Get a list of all quota objects for KeyVault at a location.</span></span>

## <span data-ttu-id="8d6c4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8d6c4-104">SYNTAX</span></span>

```
Get-AzsKeyvaultQuota [-Location <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="8d6c4-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8d6c4-105">DESCRIPTION</span></span>
<span data-ttu-id="8d6c4-106">A "minden" lemezkvóta-objektum listája az adott helyen.</span><span class="sxs-lookup"><span data-stu-id="8d6c4-106">Get a list of all quota objects for KeyVault at a location.</span></span>

## <span data-ttu-id="8d6c4-107">Példák</span><span class="sxs-lookup"><span data-stu-id="8d6c4-107">EXAMPLES</span></span>

### <span data-ttu-id="8d6c4-108">Példa 1:</span><span class="sxs-lookup"><span data-stu-id="8d6c4-108">Example 1:</span></span>
```powershell
PS C:\> Get-AzsKeyVaultQuota

Location  Name                Type
--------  ----                ----
northwest northwest/Unlimited Microsoft.KeyVault.Admin/locations/quotas

```

<span data-ttu-id="8d6c4-109">A "minden" lemezkvóta-objektum listája az adott helyen.</span><span class="sxs-lookup"><span data-stu-id="8d6c4-109">Get a list of all quota objects for KeyVault at a location.</span></span>

## <span data-ttu-id="8d6c4-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8d6c4-110">PARAMETERS</span></span>

### <span data-ttu-id="8d6c4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d6c4-111">-DefaultProfile</span></span>
<span data-ttu-id="8d6c4-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8d6c4-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d6c4-113">-Hely</span><span class="sxs-lookup"><span data-stu-id="8d6c4-113">-Location</span></span>
<span data-ttu-id="8d6c4-114">A kvóta helye.</span><span class="sxs-lookup"><span data-stu-id="8d6c4-114">The location of the quota.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8d6c4-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8d6c4-115">-SubscriptionId</span></span>
<span data-ttu-id="8d6c4-116">Az előfizetési hitelesítő adatok, amelyek egyedileg azonosíthatják a Microsoft Azure-előfizetést. Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="8d6c4-116">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8d6c4-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d6c4-117">CommonParameters</span></span>
<span data-ttu-id="8d6c4-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8d6c4-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d6c4-119">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="8d6c4-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d6c4-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8d6c4-120">INPUTS</span></span>

## <span data-ttu-id="8d6c4-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8d6c4-121">OUTPUTS</span></span>

### <span data-ttu-id="8d6c4-122">Microsoft. Azure. PowerShell. parancsmagok. KeyVaultAdmin. modellek. Api20170201Preview. IQuota</span><span class="sxs-lookup"><span data-stu-id="8d6c4-122">Microsoft.Azure.PowerShell.Cmdlets.KeyVaultAdmin.Models.Api20170201Preview.IQuota</span></span>



## <span data-ttu-id="8d6c4-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8d6c4-123">NOTES</span></span>

## <span data-ttu-id="8d6c4-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8d6c4-124">RELATED LINKS</span></span>

