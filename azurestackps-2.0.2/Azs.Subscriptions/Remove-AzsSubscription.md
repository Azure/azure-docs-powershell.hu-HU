---
external help file: ''
Module Name: Azs.Subscriptions
online version: https://docs.microsoft.com/powershell/module/azs.subscriptions/remove-azssubscription
schema: 2.0.0
ms.openlocfilehash: b6fddf677cd619dad577b7bca8286671b85d0791
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94017021"
---
# <span data-ttu-id="f1b52-101">Remove-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="f1b52-101">Remove-AzsSubscription</span></span>

## <span data-ttu-id="f1b52-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f1b52-102">SYNOPSIS</span></span>


## <span data-ttu-id="f1b52-103">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f1b52-103">SYNTAX</span></span>

### <span data-ttu-id="f1b52-104">Delete (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f1b52-104">Delete (Default)</span></span>
```
Remove-AzsSubscription -SubscriptionId <String> [-DefaultProfile <PSObject>] [-Force] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f1b52-105">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f1b52-105">DeleteViaIdentity</span></span>
```
Remove-AzsSubscription -InputObject <ISubscriptionIdentity> [-DefaultProfile <PSObject>] [-Force] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f1b52-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="f1b52-106">DESCRIPTION</span></span>


## <span data-ttu-id="f1b52-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f1b52-107">EXAMPLES</span></span>

### <span data-ttu-id="f1b52-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="f1b52-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzsSubscription -SubscriptionId d387f779-85d8-40b6-8607-8306295ebff9

```

<span data-ttu-id="f1b52-109">Törölje a megadott előfizetést.</span><span class="sxs-lookup"><span data-stu-id="f1b52-109">Delete the specifed subscription.</span></span>

## <span data-ttu-id="f1b52-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f1b52-110">PARAMETERS</span></span>

### <span data-ttu-id="f1b52-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1b52-111">-DefaultProfile</span></span>


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

### <span data-ttu-id="f1b52-112">-Force</span><span class="sxs-lookup"><span data-stu-id="f1b52-112">-Force</span></span>


```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f1b52-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f1b52-113">-InputObject</span></span>
<span data-ttu-id="f1b52-114">A kivitelezéshez tekintse meg a INPUTOBJECT tulajdonságainak megjegyzések szakaszát, és hozzon létre egy ujjlenyomat-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="f1b52-114">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.ISubscriptionIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="f1b52-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f1b52-115">-PassThru</span></span>


```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f1b52-116">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f1b52-116">-SubscriptionId</span></span>


```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f1b52-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f1b52-117">-Confirm</span></span>
<span data-ttu-id="f1b52-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f1b52-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f1b52-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1b52-119">-WhatIf</span></span>
<span data-ttu-id="f1b52-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f1b52-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1b52-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f1b52-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f1b52-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1b52-122">CommonParameters</span></span>
<span data-ttu-id="f1b52-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f1b52-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1b52-124">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="f1b52-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1b52-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f1b52-125">INPUTS</span></span>

### <span data-ttu-id="f1b52-126">Microsoft. Azure. PowerShell. parancsmagok. előfizetés. models. ISubscriptionIdentity</span><span class="sxs-lookup"><span data-stu-id="f1b52-126">Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.ISubscriptionIdentity</span></span>

## <span data-ttu-id="f1b52-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f1b52-127">OUTPUTS</span></span>

### <span data-ttu-id="f1b52-128">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f1b52-128">System.Boolean</span></span>



## <span data-ttu-id="f1b52-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f1b52-129">NOTES</span></span>

<span data-ttu-id="f1b52-130">KOMPLEX paraméterek: az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="f1b52-130">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f1b52-131">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="f1b52-131">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="f1b52-132">INPUTOBJECT <ISubscriptionIdentity> :</span><span class="sxs-lookup"><span data-stu-id="f1b52-132">INPUTOBJECT <ISubscriptionIdentity>:</span></span> 
  - <span data-ttu-id="f1b52-133">`[DelegatedProviderId <String>]`: A delegált szolgáltató azonosítója.</span><span class="sxs-lookup"><span data-stu-id="f1b52-133">`[DelegatedProviderId <String>]`: Id of the delegated provider.</span></span>
  - <span data-ttu-id="f1b52-134">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="f1b52-134">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f1b52-135">`[OfferName <String>]`: Az ajánlat neve.</span><span class="sxs-lookup"><span data-stu-id="f1b52-135">`[OfferName <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="f1b52-136">`[SubscriptionId <String>]`: Az előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="f1b52-136">`[SubscriptionId <String>]`: Id of the subscription.</span></span>

## <span data-ttu-id="f1b52-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f1b52-137">RELATED LINKS</span></span>

