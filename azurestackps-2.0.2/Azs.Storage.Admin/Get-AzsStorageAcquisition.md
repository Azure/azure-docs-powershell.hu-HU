---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/get-azsstorageacquisition
schema: 2.0.0
ms.openlocfilehash: 098c268d3894d85efe0e17618b5d7ec46b82b0f2
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94016845"
---
# <span data-ttu-id="bf225-101">Get-AzsStorageAcquisition</span><span class="sxs-lookup"><span data-stu-id="bf225-101">Get-AzsStorageAcquisition</span></span>

## <span data-ttu-id="bf225-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bf225-102">SYNOPSIS</span></span>
<span data-ttu-id="bf225-103">A BLOB-beszerzések listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="bf225-103">Returns a list of BLOB acquisitions.</span></span>

## <span data-ttu-id="bf225-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bf225-104">SYNTAX</span></span>

```
Get-AzsStorageAcquisition [-Location <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="bf225-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="bf225-105">DESCRIPTION</span></span>
<span data-ttu-id="bf225-106">A BLOB-beszerzések listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="bf225-106">Returns a list of BLOB acquisitions.</span></span>

## <span data-ttu-id="bf225-107">Példák</span><span class="sxs-lookup"><span data-stu-id="bf225-107">EXAMPLES</span></span>

### <span data-ttu-id="bf225-108">Példa 1:</span><span class="sxs-lookup"><span data-stu-id="bf225-108">Example 1:</span></span>
```powershell
PS C:\> Get-AzsStorageAcquisition
```

<span data-ttu-id="bf225-109">A blob-acquistions listájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="bf225-109">Get the list of blob acquistions.</span></span>

## <span data-ttu-id="bf225-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bf225-110">PARAMETERS</span></span>

### <span data-ttu-id="bf225-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf225-111">-DefaultProfile</span></span>
<span data-ttu-id="bf225-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bf225-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bf225-113">-Hely</span><span class="sxs-lookup"><span data-stu-id="bf225-113">-Location</span></span>
<span data-ttu-id="bf225-114">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="bf225-114">Resource location.</span></span>

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

### <span data-ttu-id="bf225-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bf225-115">-SubscriptionId</span></span>
<span data-ttu-id="bf225-116">Előfizetés azonosítója</span><span class="sxs-lookup"><span data-stu-id="bf225-116">Subscription Id.</span></span>

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

### <span data-ttu-id="bf225-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf225-117">CommonParameters</span></span>
<span data-ttu-id="bf225-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bf225-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf225-119">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="bf225-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf225-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bf225-120">INPUTS</span></span>

## <span data-ttu-id="bf225-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bf225-121">OUTPUTS</span></span>

### <span data-ttu-id="bf225-122">Microsoft. Azure. PowerShell. parancsmagok. StorageAdmin. modellek. Api201908Preview. IAcquisition</span><span class="sxs-lookup"><span data-stu-id="bf225-122">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.IAcquisition</span></span>



## <span data-ttu-id="bf225-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bf225-123">NOTES</span></span>

## <span data-ttu-id="bf225-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bf225-124">RELATED LINKS</span></span>

