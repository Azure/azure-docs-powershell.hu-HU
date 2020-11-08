---
external help file: ''
Module Name: Azs.Gallery.Admin
online version: https://docs.microsoft.com/powershell/module/azs.gallery.admin/remove-azsgalleryitem
schema: 2.0.0
ms.openlocfilehash: c39a6cd64f48a7d8d6657499357daa1dd70fc091
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/24/2020
ms.locfileid: "94015264"
---
# <span data-ttu-id="d0a23-101">Remove-AzsGalleryItem</span><span class="sxs-lookup"><span data-stu-id="d0a23-101">Remove-AzsGalleryItem</span></span>

## <span data-ttu-id="d0a23-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d0a23-102">SYNOPSIS</span></span>
<span data-ttu-id="d0a23-103">Adott gyűjtemény törlése</span><span class="sxs-lookup"><span data-stu-id="d0a23-103">Delete a specific gallery item.</span></span>

## <span data-ttu-id="d0a23-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d0a23-104">SYNTAX</span></span>

### <span data-ttu-id="d0a23-105">Delete (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d0a23-105">Delete (Default)</span></span>
```
Remove-AzsGalleryItem -Name <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d0a23-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d0a23-106">DeleteViaIdentity</span></span>
```
Remove-AzsGalleryItem -InputObject <IGalleryIdentity> [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d0a23-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="d0a23-107">DESCRIPTION</span></span>
<span data-ttu-id="d0a23-108">Adott gyűjtemény törlése</span><span class="sxs-lookup"><span data-stu-id="d0a23-108">Delete a specific gallery item.</span></span>

## <span data-ttu-id="d0a23-109">Példák</span><span class="sxs-lookup"><span data-stu-id="d0a23-109">EXAMPLES</span></span>

### <span data-ttu-id="d0a23-110">Példa 1: Remove-AzsGalleryItem</span><span class="sxs-lookup"><span data-stu-id="d0a23-110">Example 1: Remove-AzsGalleryItem</span></span>
```powershell
PS C:\> Remove-AzsGalleryItem -Name TestUbuntu.Test.1.0.0

```

<span data-ttu-id="d0a23-111">A TestUbuntu. próba. 1.0.0 törlése az Azure-halom gyűjteményből</span><span class="sxs-lookup"><span data-stu-id="d0a23-111">Deletes TestUbuntu.Test.1.0.0 from Azure Stack gallery.</span></span>

### <span data-ttu-id="d0a23-112">2. példa: Remove-AzsGalleryItem csővezetéken keresztül</span><span class="sxs-lookup"><span data-stu-id="d0a23-112">Example 2: Remove-AzsGalleryItem through pipeline</span></span>
```powershell
PS C:\> Get-AzsGalleryItem -Name TestUbuntu.Test.1.0.0 | Remove-AzsGalleryItem

```

<span data-ttu-id="d0a23-113">A TestUbuntu. próba. 1.0.0 törlése a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="d0a23-113">Deletes TestUbuntu.Test.1.0.0 through pipeline.</span></span>

## <span data-ttu-id="d0a23-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d0a23-114">PARAMETERS</span></span>

### <span data-ttu-id="d0a23-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0a23-115">-DefaultProfile</span></span>
<span data-ttu-id="d0a23-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d0a23-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d0a23-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d0a23-117">-InputObject</span></span>
<span data-ttu-id="d0a23-118">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d0a23-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Gallery.Models.IGalleryIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="d0a23-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d0a23-119">-Name</span></span>
<span data-ttu-id="d0a23-120">A gyűjtemény elemeinek azonosítása</span><span class="sxs-lookup"><span data-stu-id="d0a23-120">Identity of the gallery item.</span></span>
<span data-ttu-id="d0a23-121">Tartalmazza a közzétevő nevét, az elem nevét, valamint tartalmazhat az időszak karakterrel elválasztott verziót.</span><span class="sxs-lookup"><span data-stu-id="d0a23-121">Includes publisher name, item name, and may include version separated by period character.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: GalleryItemName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d0a23-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d0a23-122">-PassThru</span></span>
<span data-ttu-id="d0a23-123">Igaz érték visszaadása a parancs sikeressége után</span><span class="sxs-lookup"><span data-stu-id="d0a23-123">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="d0a23-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d0a23-124">-SubscriptionId</span></span>
<span data-ttu-id="d0a23-125">A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="d0a23-125">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="d0a23-126">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="d0a23-126">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d0a23-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d0a23-127">-Confirm</span></span>
<span data-ttu-id="d0a23-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d0a23-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0a23-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0a23-129">-WhatIf</span></span>
<span data-ttu-id="d0a23-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d0a23-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0a23-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d0a23-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0a23-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0a23-132">CommonParameters</span></span>
<span data-ttu-id="d0a23-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d0a23-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0a23-134">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d0a23-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0a23-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d0a23-135">INPUTS</span></span>

### <span data-ttu-id="d0a23-136">Microsoft. Azure. PowerShell. parancsmagok. Gallery. models. IGalleryIdentity</span><span class="sxs-lookup"><span data-stu-id="d0a23-136">Microsoft.Azure.PowerShell.Cmdlets.Gallery.Models.IGalleryIdentity</span></span>

## <span data-ttu-id="d0a23-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d0a23-137">OUTPUTS</span></span>

### <span data-ttu-id="d0a23-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d0a23-138">System.Boolean</span></span>



## <span data-ttu-id="d0a23-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d0a23-139">NOTES</span></span>

<span data-ttu-id="d0a23-140">KOMPLEX paraméterek: az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="d0a23-140">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d0a23-141">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="d0a23-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="d0a23-142">INPUTOBJECT <IGalleryIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="d0a23-142">INPUTOBJECT <IGalleryIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d0a23-143">`[GalleryItemName <String>]`: A gyűjtemény elemeinek identitása.</span><span class="sxs-lookup"><span data-stu-id="d0a23-143">`[GalleryItemName <String>]`: Identity of the gallery item.</span></span> <span data-ttu-id="d0a23-144">Tartalmazza a közzétevő nevét, az elem nevét, valamint tartalmazhat az időszak karakterrel elválasztott verziót.</span><span class="sxs-lookup"><span data-stu-id="d0a23-144">Includes publisher name, item name, and may include version separated by period character.</span></span>
  - <span data-ttu-id="d0a23-145">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="d0a23-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d0a23-146">`[SubscriptionId <String>]`: A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="d0a23-146">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="d0a23-147">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="d0a23-147">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="d0a23-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d0a23-148">RELATED LINKS</span></span>

