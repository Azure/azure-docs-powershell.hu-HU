---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/get-azsstoragesettings
schema: 2.0.0
ms.openlocfilehash: 3ad33f83a4e8f96124682bbb189f210f813ead25
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94016751"
---
# <span data-ttu-id="414e7-101">Get-AzsStorageSettings</span><span class="sxs-lookup"><span data-stu-id="414e7-101">Get-AzsStorageSettings</span></span>

## <span data-ttu-id="414e7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="414e7-102">SYNOPSIS</span></span>
<span data-ttu-id="414e7-103">A tárolási erőforrás-szolgáltató beállításait számítja ki.</span><span class="sxs-lookup"><span data-stu-id="414e7-103">Returns the storage resource provider settings.</span></span>

## <span data-ttu-id="414e7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="414e7-104">SYNTAX</span></span>

```
Get-AzsStorageSettings [-Location <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="414e7-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="414e7-105">DESCRIPTION</span></span>
<span data-ttu-id="414e7-106">A tárolási erőforrás-szolgáltató beállításait számítja ki.</span><span class="sxs-lookup"><span data-stu-id="414e7-106">Returns the storage resource provider settings.</span></span>

## <span data-ttu-id="414e7-107">Példák</span><span class="sxs-lookup"><span data-stu-id="414e7-107">EXAMPLES</span></span>

### <span data-ttu-id="414e7-108">Példa 1:</span><span class="sxs-lookup"><span data-stu-id="414e7-108">Example 1:</span></span>
```powershell
PS C:\> Get-AzsStorageSettings
```

<span data-ttu-id="414e7-109">A tárterület beállításainak beszerzése</span><span class="sxs-lookup"><span data-stu-id="414e7-109">Get the storage settings.</span></span>

## <span data-ttu-id="414e7-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="414e7-110">PARAMETERS</span></span>

### <span data-ttu-id="414e7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="414e7-111">-DefaultProfile</span></span>
<span data-ttu-id="414e7-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="414e7-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="414e7-113">-Hely</span><span class="sxs-lookup"><span data-stu-id="414e7-113">-Location</span></span>
<span data-ttu-id="414e7-114">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="414e7-114">Resource location.</span></span>

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

### <span data-ttu-id="414e7-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="414e7-115">-SubscriptionId</span></span>
<span data-ttu-id="414e7-116">Előfizetés azonosítója</span><span class="sxs-lookup"><span data-stu-id="414e7-116">Subscription Id.</span></span>

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

### <span data-ttu-id="414e7-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="414e7-117">CommonParameters</span></span>
<span data-ttu-id="414e7-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="414e7-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="414e7-119">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="414e7-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="414e7-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="414e7-120">INPUTS</span></span>

## <span data-ttu-id="414e7-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="414e7-121">OUTPUTS</span></span>

### <span data-ttu-id="414e7-122">Microsoft. Azure. PowerShell. parancsmagok. StorageAdmin. modellek. Api201908Preview. ISettings</span><span class="sxs-lookup"><span data-stu-id="414e7-122">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.ISettings</span></span>



## <span data-ttu-id="414e7-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="414e7-123">NOTES</span></span>

## <span data-ttu-id="414e7-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="414e7-124">RELATED LINKS</span></span>

