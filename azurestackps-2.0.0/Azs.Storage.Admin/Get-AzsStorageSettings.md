---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/get-azsstoragesettings
schema: 2.0.0
ms.openlocfilehash: 3ad33f83a4e8f96124682bbb189f210f813ead25
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842505"
---
# <span data-ttu-id="75372-101">Get-AzsStorageSettings</span><span class="sxs-lookup"><span data-stu-id="75372-101">Get-AzsStorageSettings</span></span>

## <span data-ttu-id="75372-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="75372-102">SYNOPSIS</span></span>
<span data-ttu-id="75372-103">A tárolási erőforrás-szolgáltató beállításait számítja ki.</span><span class="sxs-lookup"><span data-stu-id="75372-103">Returns the storage resource provider settings.</span></span>

## <span data-ttu-id="75372-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="75372-104">SYNTAX</span></span>

```
Get-AzsStorageSettings [-Location <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="75372-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="75372-105">DESCRIPTION</span></span>
<span data-ttu-id="75372-106">A tárolási erőforrás-szolgáltató beállításait számítja ki.</span><span class="sxs-lookup"><span data-stu-id="75372-106">Returns the storage resource provider settings.</span></span>

## <span data-ttu-id="75372-107">Példák</span><span class="sxs-lookup"><span data-stu-id="75372-107">EXAMPLES</span></span>

### <span data-ttu-id="75372-108">Példa 1:</span><span class="sxs-lookup"><span data-stu-id="75372-108">Example 1:</span></span>
```powershell
PS C:\> Get-AzsStorageSettings
```

<span data-ttu-id="75372-109">A tárterület beállításainak beszerzése</span><span class="sxs-lookup"><span data-stu-id="75372-109">Get the storage settings.</span></span>

## <span data-ttu-id="75372-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="75372-110">PARAMETERS</span></span>

### <span data-ttu-id="75372-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75372-111">-DefaultProfile</span></span>
<span data-ttu-id="75372-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="75372-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75372-113">-Hely</span><span class="sxs-lookup"><span data-stu-id="75372-113">-Location</span></span>
<span data-ttu-id="75372-114">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="75372-114">Resource location.</span></span>

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

### <span data-ttu-id="75372-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="75372-115">-SubscriptionId</span></span>
<span data-ttu-id="75372-116">Előfizetés azonosítója</span><span class="sxs-lookup"><span data-stu-id="75372-116">Subscription Id.</span></span>

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

### <span data-ttu-id="75372-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75372-117">CommonParameters</span></span>
<span data-ttu-id="75372-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="75372-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75372-119">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="75372-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75372-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="75372-120">INPUTS</span></span>

## <span data-ttu-id="75372-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="75372-121">OUTPUTS</span></span>

### <span data-ttu-id="75372-122">Microsoft. Azure. PowerShell. parancsmagok. StorageAdmin. modellek. Api201908Preview. ISettings</span><span class="sxs-lookup"><span data-stu-id="75372-122">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.ISettings</span></span>



## <span data-ttu-id="75372-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="75372-123">NOTES</span></span>

## <span data-ttu-id="75372-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="75372-124">RELATED LINKS</span></span>

